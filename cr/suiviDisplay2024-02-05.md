---
title: Suivi de projet display
author: ouvroir
date: 2024-02-05
draft: false
tags:
     - cr
     - display

---
## 2024-09-06

## 2024-09-03

## 2024-07-31

## 2024-06-27

## 2024-06-18

## 2024-03-27

## 2024-03-13

## 2024-03-07

## 2024-02-28
WD, ECD, LK, DV, ZR

- Établissement des 3 personae
- discussion modèle de saisie de données
- discussion articulation modèle de données avec l’app


## 2024-01-17
WD, ECD, ZR

Enlever les mentions graphs et mettre plus en avant les fonctionnalités. 
Gestions utilisateurs par Common. Éliminer ces questions.
Réintroduction d’un outil de visualisation et de saisie 2D de l’espace 

## 2023-12-20
DV, ZR, ECD

Ontologie : 
- Défi points de vue multiples : qu'est-ce qu'on fait pour placer les objet les uns par rapport aux autres dans ce cas là?
- 2 sortes de topologique ?: 
 une basée sur les points de vue : à gauche à droite ambiguë
  une basée sur les relations entre les expôts. : ECD pour cette sorte afin d'exclure la visite. 
- On a fini de décrire les 6 premières salles de Feux Pâles
- visualisation requête sparql pour vitrine DH : Sparnatural

Interface : 
- Pas de dimensions mais des relations topo. Comment faire pour un export de plan éclaté dans ce cas là?
- Regarder Ikea Kitchen Planner et app pour mapping archeology pour gestion des sources et placement d'objet:  https://www.fulcrumapp.com/apps/archaeological-sites/

Biblio : 
- Zr a cherché des ouvrages museo/hida sur display : tout dans zotero


## 2023-12-13
DV, ZR, ECD

Ontologie :
- Présentation EM d’[OntoExhibit](https://andalexproject.iarthislab.eu/semantic-web-seminar/) : Ne semble pas trop en contradiction avec notre ontologie. 
- Branchement CIDOC :
Exhibit = E18 Physical Thing
display =  E78 Curated Holding
- Faire intervenir SHACL ?
- Etude RCC8 : trop radical pour nous. 
- pas nécessaire de brancher GeoSPARQL
- ECD trouve notre Ontologie élégante, concise et efficace. Avec économie de classe.

Interface : 
- comment on interface ça pour l'éditer ? N'y a-t-il pas d'enjeux du côté des inférences ?
- faire des fiches docu et on exprime ça ensuite par export avec notre ontologie
- David pense qu'il est important d'avoir accès directement aux inférences : Difficile de trouver dev de faire requêtes sparql avec formulaire. David propose qu'on fasse le sparql et le donner au dev.  On pourrait faire une interface de programmation de triplet simplifiée.
- A-t-on des ex de programmation visuelle en web sémantique ? Sparqlisse ?
- Prestataire de service : https://www.takin.solutions/
- Est-il possible de faire des visu 3D à partir de notre ontologie ? Avoir un schéma ?

Écrire article ensemble :
- http://stylo-doc.ecrituresnumeriques.ca/fr/edition-collaborative/ à tester 
- 1_Livrable pour request for comment. 
Publier ontology avec jeux de données : 
avec Feux Pales et une salle de Marie
- 2_Faire un article en parlant des ontologies choisies et nos choix. 
Pour qui ? : communauté du web sémantique, muséale. 
- Semantic Web Journal ? Article difficile à placer ? Feedback pertinent. 
- DH 2024 Washington : David et Lena ou Zoë
- Humanistica ?

Présentation : 
- Pas forcément l'interopérabilité pour l'instant
- Enjeux plutôt du côté de la relation entre objet sont des relations de graphes. 
- Technique : on fait du rdf et pas du property graphe. Parce que sinon pas d'ontologie. 
- Propriété owl nous intéresse parce que fait déjà bcp de choses rien qu'avec ce qu'on a.
- Expressivité owl est mise à profit grâce aux chaines de propriété, restrictions pas forcément utile ici, mecanisme héritage et propriété c'est rdf. 
- Discuter dans l'état de l'art de la docu en xml et modèle hiérarchique. On aurait pu documenter en relationnel mais on peut pas faire d'interférence, on perd en sémantique et les rapports entre les classes. Plus flexible qu'un modèle relationnel.
- Permet de les lier avec autres ontologies muséales et architecturales.

#todo 
- Vérifier les hiérarchies pour connecter à Cidocexhibit = E18; display = E78
- organiser une présentation équipe OntoExhibit + présentation de notre projet + Nicolas Carboni? Proposer une revue critique de leur travail. 
- inviter robert.sanderson@yale.edu pour nous présenter son projet.
- faire un contrat pour l'hiver pour David
- Discuter avec Georges Bruseker? à son compte [TAKIN](https://www.takin.solutions/) maintenant donc peut-être tarifé ? Peut-être notre prestataire de service
- montrer Display à la personne des ontologies du getty et à linked art David Newbury
- générer taches dans le projet dans github. 
- @tous : relire maj définition 
- @tous : réviser les choix de l'ontologie
- @emmanuel : vérifier si AAT fonctionne
- @emmanuel : envoyer notes sur OntoExhibit
- réunion 20 14h. OK
- @emmanuel : article sur OntoExhibit?
- Organiser réunion de travail avec OntoExhibit pour parler de notre ontologie

Calendrier :
- janvier : rentrer fp OK
- janvier : atelier avec Marie pour un exemple lacunaire
- février : état de l'art
- avril-mai : faire un article 
- avril-mai : prototype pour request for comment

## 2023-12-06
ECD, ZR

Réunion contenu cdc : 
Prob technique : web sémantique. comment géré les données semantiques dans un nouveau format. Faire données sémantique comme données relationnelles. Appli nativement rdf mais pas de dev qui savent pas faire du front end et du back end en rdf. Il nous faut quelqu'un pour les deux. Accent sur la prod des données et formulaire de saisie.
Technologie : choisir quelqu'un de spécialiste en bdd et graph. Graph database. Ou vers bdd orientée document. fichier json stocké dans bdd. Structurer données sous forme de notice editable?
Pas besoin d'aller faire une bdd sql.
Utilisateur, chacun voit ses expositions. Pas d'idée de partage.
Collègue signalement exposition à Malaga.
Fiche signalétique : documentation de l'accrochage.
Comment saisir un document, une source pour attester de l'information.
Information renseignement spatial.
Créé/générer liste d'oeuvre au format CSV
Soit génére salle pour mettre les oeuvres dedans.
Comment elles fonctionnent les unes les autres.
POUVROIR VISUALISER LA SPATIALISATION DES OBJETS DE FAÇON DIAGRAMATIQUE OU 3D. Au dev de trouver.
visualisation simple vue écorchées. représentation abstraite. Comment faire diagram.
Standard du web pour la 3D : Webgl.
Au lieu de se dire de faire la numérisation de 3D. Pas durable. Pas processus de travail.
Partir du modèle pour partir d'un outil. Pas de rendu illusitionniste souhaité. On souhaite une analyse.
Se pose la question du processus analytique. Création d'affordance. Acceptation de l'incertitude et les inconnus.
Processus et modèle docu pour enregistrer les expo. Peut servir à créer des expositions.
Schématisation
Sortir document ?


## 2023-10-25
DV, ZR, ECD

Ontologie :
- Résolution pour l’exhibit/artifact : on ne définit pas la nature de l’expôt dans l’ontologie sauf si c’est un bot:element
- Un display peut être un expôt
- Support et devices sont devenus des sous-classes de Element/BuldingElement.
- Display devient une sous classe de Exhibit et includes exhibit.
- On enlève les artefacts et informativeInfo de l'ontologie laissant ainsi ces définitions à Cidoc. Branchement de Cidoc sur Exhibit.
- Ontology en owl, RDF sérialisé en Turtle. 
- Etrange de ne pas avoir d'ontologie sur la topologie. Ok, mais GeoSPARQL propose un ensemble de relations topologiques abstraites, dont RCC8.
- SubProperty of (Chain) propriété OWL importante :
`containsZone o hasExhibit SubPropertyOf hasExhibit`. Autrement dit, une zoneA, qui contient une zoneB qui a des expôts, a ces expôts. Pourra se matérialiser par inférence.

#todo
- Planifier avec atelier avec Marie Fraser
- Décrire le lien entre les exhibits et l’ontologie CIDOC-CRM
- Chercher dans les ontologies topologiques, la mathématique, des réseaux. Vérifier réf ajoutées à la biblio par Emmanuel. 
- Choisir notre moteur d'inférence.
- Pousser en ligne l’ontologie. OK

## 2023-10-10
DV, ZR

- discussion sur les termes et relations entre expôt, artifacts, element etc. 
- discussion sur les circulations dans l’espace et ABOX
- discussion bot:Interface

#todo 
- Créer questions à poser à Sparql OK
- Trouver déclaration de niveau de certitude. 1 à 4 (1 étant le moins certain)
- Lire ontologie Fuzzyness
- Ajouter propriétés : LaysOn; LeanOn; Between OK
- Créer notion de lot? OK
- Définir que c'est la gauche/droite du regardeur face à l'objet. OK
- interface : utilité et propriétés

## 2023-09-18
LK, DV, ZR, ECD

- hiérarchie de différents types d'entités
- étude et présentation la building topology ontology (BOT)
- réflexion état de l’art
- 1er test avec Feux Pâles
- essayer de garder ça minimal pour la représentation des espaces, dont on ne connaît pas nécessairement les dimensions et qui ne sont pas nécessairement des boîtes
- Relations topologiques (et non géospatiales) : Vérifier les ontologies qui peuvent inclure topographie.
- comment est-ce que les gens vont renseigner ça ? 
- base de données avec des propriétés à renseigner
- comment travailler de manière schématique :  [scratch](https://scratch.mit.edu/): langage de programmation visuel (python)

## 2023-09-07
LK, DV, ZR, ECD

jeu: construit une exposition (toolbox)
- avec stylo sur carton plastifié pour écrire-dessiner/effacer
- vue plan de salle; "zoom" sur des murs
- grilles pour proportions?

#todo 
- identifier un cas de documentation partielle
- Essayer de décrire cette expo de plusieurs manières (granulaire et interface)
- Enlever Artwork
- Vérifier la cidoc-crm

## 2023-08-23
LK, DV, ZR, ECD

- Display = Modèle documentaire qui permet de prendre en charge l'information lacunaire. Intérêt aussi pour faire des inférences et émettre des hypothèses.
Relations topologiques (entre les expots) comme entités avec des attributs
- La salle d'exposition devient plutôt secondaire car on centre sur le display, qui est ensuite dans la salle. La question qui se pose est l'ordre de visite, modélisé à l'échelle du display, propriété follows/isFollowedBy (pour donner une idée)
- Perspective centrée sur les objets. Requiert une seconde perspective sur la représentation topologique / dans l'espace. Question des expositions et de l'instanciation des expositions (inspiré de RiCO)
- Typage des sous-classe pour mieux documenter les attributs des expots ?
- Travailler sur les contraintes pour améliorer l'ontologie.
- Comment définit-on un lieu?
  Exposition et instanciation de l’exposition cf. Record (ne devrait-on pas plutôt pour le coup adopter un modèle proche de CIDOC)
- Séquence vs modèle labyrinthique : plusieurs séquences possibles en même temps. Affordances. Séquences distributives: manière dont les pièces/display communiquent les uns entre les autres → chemins possibles.
- Faut-il représenter l'espace? Pourrait-il s'exprimer autrement?
- Première question pour trancher: 
 orienté objet ou événement? --> on choisit d’adopter une approche très matérielle dans la définition de l’ontologie.
 comment traiter l'espace et la topologie? 
 combiner CIDOC mais avec d'autres modèlesau besoin

#todo
test avec l'[exposition de la collection par Geneviève Cadieux](https://macrepertoire.macm.org/evenement/l-oeil-et-l-esprit-point-de-vue-de-genevieve-cadieux/) au MAC
Building Topology ontology BOT → mécanique du batiment et flux
À analyser. BIM
Test de modélisation avec Protégé 


## 2023-08-03
ECD, LK, DV

Discussion autour :
- de l’état de l’art
- de l’expérimentation de modélisation
- suite envisagée :
Implémenter un modèle pour voir ce que ça fait et le soumettre à la critique ?
Ou continuer le travail de modélisation? 

Relation entre expot et surface: retravailler / raffiner avant de mettre à l'épreuve

Implémentation simple: petite ontologie avec [Protégé](https://protege.stanford.edu) et la visualiser avec [WebVowl](http://vowl.visualdataweb.org/webvowl.html)

choisir une exposition, il faut structurer quelque chose avec pour le tester
soit un formulaire, soit on cible des cas de figure qu'on implémente nous et qu'on code à la main

Comment rendre le prototype visible pour en discuter ?

Test de formulaire, quelque chose à traiter dans une étape plus avancée.

Comment montrer les biais ou les raccourcis ontologiques de ce petit modèle.
et les anticiper?

Comment en faire une preuve de concept pour pouvoir se faire les dents dessus? 

## 2023-07-18
ECD, LK, DV

 Présentation du projet :
pas de réel modèle de documentation des expositions
existant: CIDOC-CRM

dispositif spatial/topologique, pas sûr si c'est compatible avec CIDOC. Fait défaut dans le monde muséal

revue de littérature (partager le [lien Zotero](https://www.zotero.org/groups/2480242/ouvroir/collections/ASCZR3EC))
années 90 : prototype basé sur XML.
[linkedart](https://linked.art/): pattern pour CIDOC CRM (json-ld)

Périmètre du travail - été 2023 : 

- compléter la revue de littérature (~12-15h)
- regarder ce qui se fait en archéologie avec CIDOC pour la stratigraphie
- voir ce qui se fait côté topologie (quelles ontologies? géo, spatial): recherches d'un cadre 
- initier un prototype de modélisation pour comprendre les difficultés liées à l'établissement d'un modèle documentaire

A faire : 
- chercher une exposition sur le macRepertoire qui est bien documentée et où il y a accès à plusieurs documents source
- partir d'une vue d'exposition bien connue, dont les tableaux sont bien identifiés
- partir du contemporain, faire une vue à 360 et travailler avec ça? voir s'il y a des visites virtuelles d'une salle (MNBAQ) disponible en ce moment

Revue de littérature : 

- grandes conférences sur le web sémantiques
- semantic web journal
- routledge: grande séries de volumes, cultural heritage...
- archéo: CAA Computer application in archeology, ex cas anglais de stratigraphie avec cidoc-crm (heritage trust)
- rechercher extension CIDOC archaeo et bibliographie associée au site
- [building topology ontology](https://w3c-lbd-cg.github.io/bot/)

  
## 2022-03-24
Marie-Eve Beaupré, Marianne Longtin, Marie Fraser, Marilie Labonté, ECD, LK

 Rencontre MAC

### Présentation du contexte : 

Histoire de l'exposition des collections avec 2 partenaires institutionnels : MAC et MBAM
- faire des listes des expositions
- nomenclature pour classifier et identifier des cas 

Est-ce que les démarches de recherche avec le MBAM sont déjà entamées ou sont-elles à venir ? 
Recherches déjà entamées avec Alexandra, qui voulait travailler sur l'histoire des collections du MBAC mais les musées étaient fermés, et elle s'est tournée vers un musée montréalais. 

Pour bien arrimer les recherches, afin que les résultats des démarches installent des points de comparaison : dans le programme du stage, mention d'une étude d'histoire de pratiques expographiques et procédés discursifs. 

### Répertoire MAC 
est une sorte de "pellicule", un espace de traduction visuelle de Mimsy
http://repertoires.macm.org/ 

### Besoins Axe 1

Marie besoin d’une vision générale de la collection.
Générer la liste de toutes les collections pour avoir une vision générale du nombre d’expositions, etc. À partir de cette liste possible isoler expositions de collections pour faire un travail plus dans le détail.

Avoir un portrait général des expositions et des expositions de collections, puis va aller cibler des cas exemplaires qui nous permettront d’explorer les choses plus en détail sur des questions, des formats, des dispositifs, des cas exemplaires, etc.

Expositions de type "Points de vue sur la collection".

1. produire (beaucoup) de données de recherches
2. objectifs concrets avec hypothèses de recherches à tester

Former une liste des questions clés à adresser à Mimsy? 
- dégager des axes discursifs
- analyser l'iconographie et la mise en espace des œuvres
- toujours garder dans les documents & tableaux les identifiants des œuvres et des expositions

reconstitution d'une exposition → basculer le point de vue, où l'œuvre a été 
gardons à l'esprit que les artistes et leurs œuvres doivent demeurer le cœur de la perspective (plutôt que la vie du musée, qui serait limite narcissique)

### Suivi

- quand la nomenclature sera terminée
    - exporter la liste de toutes les expositions
    - conserver les possibilités de nourrir leur base par les résultats de recherche scientifique = résonance
- terrain d'expérimentation pour la liste des œuvres dans les expositions
- quand on sera rendu à l'année sur les circulations, clairement on va investiguer les trajectoires des œuvres

- demander le contact d'Etienne (API avec client ou exports? )
    - employé contractuel du musée pour le MAC répertoire
    - requiert une demande un prêt de service de personnel
- faire une liste par points des questions et des besoins (à court et à moyen terme) auxquels il faut répondre → créer un document partagé 
    - commencer plutôt par un export mimsy car le développeur est mobilisé par la livraison du produit
    - bien faire circuler l'information par rapport à la recherche
    - bien expliquer les motifs pour l'export des données
    - circonscrire l'utilisation/éthique etc.

- il faudra, à terme, valider la politique institutionnelle en ce qui concerne la publication en lien avec leurs données? 

- demande d'organigramme mis à jour 

Rencontres
- Andréa (cheffe)
    - Etienne, responsable de la maison, structure 
    - Béatrice informatise/normalise les données produites par les chercheurs
    - Cindy 
- Équipe de gestion des collections: Alexandra
- 
## 2022-02-17
ECD, LK, Alexandra ?

Rencontre Axe 1

Tableur

### Suivi
Avec Alexandra
- Extraire les données des trois listes originales en tableur
- Tableau exposition de collection (liste d'Alexandra)
- Ajouter champs "exposition de collection" (oui/non associé à une couleur)

Identifier et partager un tutoriel pour les règles de bases / bonnes pratiques en tableur
Envisager un atelier sur l'extraction et le nettoyage de données

Avec Emmanuel : soigner les colonnes / fichier
Ajouter la possibilité de multiplier les tags

Prochaine étape : négociation avec les archivistes pour l'obtention des expositions permanentes

## 2022-01-05
Hend Ben Salah, Lisa Bouraly, Emmanuel Château-Dutier et Lena Krause

rencontre Hend Ben Salah

Choix du logiciel : employé dans le quotidien et comme journal de recherche. A considéré utiliser Access ou Excel mais souhaitait avoir l’information sur les expositions, les acteurs d’expositions, les dates, lieux et pays, mais voulait pouvoir faire des liens entre les entités. Un aspect relationnel qui rendait difficile de traiter les informations dans un seul tableau. Or, cela était possible sur Notion.
[Notion](https://www.notion.so)
Autres options:
- [Obsidian](https://obsidian.md/)
- Méthode Zettelkasten 

## 2021-12-21
Lisa Bouraly, ECD, LK ?

Présentation travail de Lisa

## 2021-12-08
Marie Fraser, Marilie Labonté, Alexandra Dumarais, Hend Ben Salah, Didier Prioul,  Emmanuel Château-Dutier, Kristine Tanton, Lena Krause

Calendrier
- Fin janvier, accès à l'ensemble de la documentation du MAC 
- avoir un premier outil disponible pour commencer le travail fin janvier (fichier tabulaire avec explications sur comment renseigner les champs)
- définition d'un modèle documentaire
- travail d'Alexandra: est-ce qu'on adapte le "formulaire"? 
- MAC intéressé à faire une publication pour 2025 (réouverture du musée)


Périmètre à définir: 
- trouver des moyens de réutiliser le travail de documentation effectué par les musées
- ambiguité entre reconstituer l'archive vs produire une documentation

Est-ce qu'un des produits finaux de la recherche serait une publication du type *Biennials and Beyond*? 

Principales étapes de la recherche
1. Repérage chronologique, recherche systématique (travail de dépouillement des auxiliaires). De quoi cette histoire de l'exposition des collections se compose-t-elle? 
2. Identification d'expositions particulières (repérage des co-chercheur·se·s), cas exemplaires, sachant que l'exemplarité peut varier à travers le temps
3. Analyse à différents niveaux: analyse tridimensionnelle d'accrochages d'une salle / d'un contexte, analyse temporelle d'une œuvre (dispositif plus centré sur la narratologie)


• Quel(s) est (sont) le(s) meilleur(s) outil(s) (logiciel, etc.) à favoriser pour faciliter un transfert éventuel de données ?
• À partir des modèles qui constituent nos bases conceptuelles (fiches de Didier Prioul et de Pompidou), quelles sont les informations que nous souhaitons collecter sur les expositions (matériel muséographique, éducatif, scientifique, communicationnel, etc.) ? Ceci permettra de faciliter la construction du modèle type pour l’axe 1.

Systématique
- mandats
- musées
- partenaires
- dates

Suivi 

- demander ce dont dispose chaque musée: prévoir des rencontres avec Marie-Eve (MAC) et Nathalie Thibault (MBAM)? 
- rencontre avec Hend pour voir son travail 
- Marilie met ses documents sur le Drive
- création d'un document martyr à travailler principalement de façon asynchrone, bien expliquer comment renseigner les champs
- réunion pour finaliser à la rentrée (janvier)
- au cours du semestre: comment peut-on passer du dépouillement systématique mais commencer à réfléchir l'analytique, les approches transversales possibles

  Se permettre de gérer les formulaires de façon modulaire, Omeka-S permet de faire évoluer les champs au fur et à mesure, Strapi aussi. 
Evaluer BD-oracle et [docuverse](https://docuverse.io) car [utilisé](http://www.sis.pitt.edu/spring/mlnds/mlnds/node2.html) par plusieurs personnes? [DSpace](http://e-chastel.huma-num.fr/)

## 2021-11-22
 Marie Fraser, Marilie Labonté, Alexandra Dumarais, Hend Ben Salah, Didier Prioul, Emmanuel Château-Dutier, Kristine Tanton, Lena Krause

Définir une manière de **colliger les informations retrouvées dans les archives lorsque l’on fait de la recherche sur les expositions de collections**. Ces expositions sont probablement fort moins documentées que les expositions temporaires, ne serait-ce que par la documentation photographique conservée.

