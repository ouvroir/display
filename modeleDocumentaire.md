# Modèle Documentaire

Marie et Marilie: Les champs que nous compléterions si vous avions à entrer une exposition dans un logiciel de bibliographie seraient : **titre de l'exposition,  dates de début et de fin, musée(s), commissaire(s)**.

Marie: En ce qui concerne la manière de citer une exposition à l'intérieur  d'une bibliographie ou d'une note de bas de page, nous irions avec cette forme : *titre*, lieu, ville, dates, commissaire(s) (s'il y a lieu). - ex. : *Des horizons d'attente. Acquisitions récentes*, Musée d'art contemporain de Montréal, Montréal, 10 février-27 juin 2021, Marie-Ève Beaupré.

Marilie: normalement à même le texte avec le titre de  l'exposition, les dates entre parenthèse ainsi que le musée où elle  prend place ; je n'ai pas encore eu l'occasion d'inscrire une exposition à même une note de bas de page ou dans une bibliographie. Si c'était le cas, je crois que je l'écrirais ainsi : *Titre de l'exposition* (jour mois année au jour mois année), Musée - *D'Afrique aux Amériques : Picasso en face-à-face, d'hier à aujourd'hui* (12 mai au 16 septembre 2018), Musée des beaux-arts de Montréal. 

# Entité exposition

## désignation

- titre de l’exposition [xs:string ou mixed-content]
- sous-titre de l’exposition [xs:string ou mixed-content]

## dates de l’exposition [intervale ISO]

S’il y a plusieurs itérations dans plusieurs lieux ou institutions, prévoir un événement pour rejoindre les informations

## mentions de responsabilité

- commissaire(s)*
- scenographe(s)*
- graphiste(s)
- ...

## indexation / typologie

- catégorie d’exposition
- mots-clefs

## notes


# entité acteurs/œuvres

Les artistes participent-ils aux expositions ? (oui pour le performatif, mais veut-on en faire des actants plutôt que des acteurs ?)

# entités personnes

Identité
- nom
- prénoms
- dates d’existence

- genre
- profession/activité (mais problématique)
- lieu de naissance
- lieu de dècès

- identifiants (isni, wikidata, viaf, etc.)
- note

## institution

L’institution peut avoir plusieurs rôles dans la production ou l’accueil d’une exposition. Dans le cas des expositions de collection la question est triviale.

- nom de l’institution
- localisation
- site
- galerie
- etc.

## espaces d’exposition

- désignation
- salles...
- etc.

## zone de notes

---

# Accrochage

topologie