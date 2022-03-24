# Besoins en extraction de contenus Word MS

> Nous avons entamé les démarches auprès du service des archives du Musée  des beaux-arts de Montréal. Nous avons reçu trois listes d'expositions  sur des documents *Word* (voir pièces jointes) desquels nous aimerions éventuellement importer des informations.
>
> Nous aimerions ainsi discuter avec toi et Alexandra qui mène les  recherches sur les expositions du MBAM sur la meilleure façon d'importer ces données. Nous voudrions ainsi, pendant cette rencontre, te  présenter un portrait général de la situation en ce qui concerne le MBAM (notamment les mots clés visés et les données que nous souhaitons conserver).



# 



TXT vers un CSV 

1. mettre chaque ligne entre guillemets pour éviter les problèmes avec les virgules
2. mettre des virgules à la place des sauts de lignes
3. identifier les dates et faire un saut de ligne avant chaque date

Sur word

- remplacer un carriage return = find and replace, find "\n" en activant "regular expression", replace avec un caractère batard
- vérifier l'éventuelle présence de guillemets " "

fichier ods

ligne 2258



OpenRefine:

- ne pas oublier d'enregistrer les fichiers en local (pas sur un drive)

- ne pas essayer d'afficher 1000 entrées ^ 

- GREL

- remove trailing spaces

- format date

  

### Expo temporaires

quand on veut mettre en page et nettoyer le Word, afficher les tous les caractères (*View formatting marks*)

- tout séparé en cases (ça aide de grossir les lignes du tableau)
- mis les titres sur une ligne continue
- remplacé les guillemets anglais ("") par des _
- remplacé la barre oblique dans le titre par \
- remplacer les "carriage return" (qui divisent les dates des titres) par @ (caractère inutilisé dans le fichier)
- copié-collé le contenu du tableau dans un tableur
- enregistrer le tableur comme un csv, en ajoutant les guillemets "" comme StringDelimiter
- sortir du tableur, ouvrir un éditeur de texte (ou de code)
- faire une première ligne avec les colonnes (pour visualiser les couleurs quand on a une extension csv)
- remplacer @ par ","
- vérifier qu'il n'y a pas d'autres couleurs = erreurs
- décision de séparer en deux à la seconde guerre mondiale: parce que la recherche se concentre sur après de toute façon. Parce qu'il y a énormément d'incertitudes dans les dates avant. Il va rester des incertitudes dans les dates après mais ce sera plus *manageable* (on pense, ou du moins on l'espère)

dans openRefine

- 1860-1945

  - séparer dates et enlever _trailing spaces_

- 1945 - 2020. [openRefine project 2358722013759](http://127.0.0.1:3333/project?project=2358722013759)

  - séparer dates et enlever _trailing spaces_

  - split titres: 

    - if value.split('/')

      else 

      return value

    sans succès: on a divisé en titre1 et titre2

    <!-- to do: en anglais aussi? vérifier si tout y est-->

  - **sous-titre**: split at "." or "!" or ":" --> [.:!–;/] 

    - attention remettre le ! 
    - si on le fait pour l'anglais: ([.:!–;-] ) <!-- - et ; et ajoute un espace après le char-->

  - **date**: split(value, value.indexOf("au"))

    - essayer de split à "au" pour avoir la date de fin
    - value.replace("janvier", "january").replace("février", "febuary").replace("mars", "march").replace("avril", "april").replace("mai", "may").replace("juin", "june").replace("juillet", "july").replace("août", "august").replace("septembre", "september").replace("octobre", "october").replace("novembre", "november").replace("décembre", "december")



split "au": 

| date début      | date fin        |      |      |
| --------------- | --------------- | ---- | ---- |
| jour mois       | jour mois année |      |      |
| jour mois année |                 |      |      |

```bash
partition(value, " au ")[0]  #jj mm début
partition(value, " au ")[2]  #jj mm anne fin 
```

date_fin: complet seulement si on avait une date de fin

le faire avec la date en anglais comme ça il reconnaît les mois. split(value,', ')[1] pour avoir juste l'année à partir de la date de fin

date_debut_tentative : continent jj-mm de début + année date_fin (faux si ça commençait exemple en novembre 2012 et se terminait en mars 2013), à corriger manuellement? 

.replace("janvier" ,"january)



split par espace (pas utilisé finalement)

| A    | B    | C     | E    | F    | G     |
| ---- | ---- | ----- | ---- | ---- | ----- |
| jour | mois | au    | jour | mois | année |
| jour | mois | année |      |      |       |

date début = A + B + G ? C

date fin = (E + F + G) ? A + B + C





### Expo itinérantes

Objectifs

- diviser les titres des occurences (date)
- réussir à regrouper les expos

Étapes

- elevé les  → (tabs), enlever les "--"
- tranformé les $ (paragraphe break) en @. Supprimé @ après le / qui indique le titre en anglais ("/@" & "/ @" to @)
- <!--enlever les doubles \n ?-->

tableau1

| id expo | titre | occ1                    | occ2 |
| ------- | ----- | ----------------------- | ---- |
|         |       | jfkdjfd@jfkdljfk@jfdjfk |      |
|         |       |                         |      |
|         |       |                         |      |

Alexandra: Identifie toutes les expos qui sont les mêmes (qui ont le même titre) et les mettre sur une seule ligne

Repasser dans OpenRefine (probablement ) pour: 

<!-- to do-->

- séparer titres fr/en
- séparer titre / sous-titre

- Use "record" mode
- for the first "occurrence colum"
- transpose → transpose cells across columns into rows 
  - key = column *titre*
  - to "last column"
  - one column "Occurrence"
  - fill down in the other columns
- split occurrences par  @ pour les dates et lieux



tableau2

| id expo | titre expo | date debut/fin |      | lieu |      |
| ------- | ---------- | -------------- | ---- | ---- | ---- |
| 1       |            |                |      |      |      |
| 1       |            |                |      |      |      |
|         |            |                |      |      |      |

- séparer titres en / fr
- séparer dates debu date fin







### Au fil des collections openRefine

- splitter la date
- titre fr _ titre en
- spliter responsable



