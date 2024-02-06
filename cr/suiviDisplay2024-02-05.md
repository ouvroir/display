---
title: Suivi de projet display
author: ouvroir
date: 2024-02-05
draft: false
tags:
     - cr
     - display

---

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



## 2023-07-18

## 2022-03-24

## 2022-02-17

## 2021-12-21

## 2021-12-08

## 2021-11-22

## 2021-01-05