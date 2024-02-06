---
title: CR Display 13 dec 2023
desc : réunion sur le projet display du 13 dec 2023
author: ECD, ZR, DV
date: 2023-12-13
draft: false
tags:
    - cr

---
# Display
Emmanuel a répondu à l'appel du dh2024.

## Description de l'alignement ontologique

Voir https://github.com/ouvroir/display/blob/main/cr/cr2023-10-25.md#description-display-ontology

Exhibition Space sous classe de Space
Exhibition Space has exhibit

Element, building element sous classe d'Exhibit

## OntoExhibit
Réunion sur le numérique à Lausanne: Nuria Rodríguez Ortega, sur la description des expositions [OntoExhibit](https://andalexproject.iarthislab.eu/semantic-web-seminar/)

Ont travaillé sur Cidoc pour rendre compte les aspects discursifs. 
Endroit un peu compliqué dans leur ontologie mais critique de cidoc intéressante. 

Modèle influencé par FRBR, pourquoi pas LRMN?

FRBR modèle pour les biblio 
F1 idée de l'œuvre
F2 expression
F4 manifestation
F5 Item 

Biblio sont revenus sur ce modèle et remplacé par lrm (ifla) qui est en cours. 

Ne semble pas trop en contradiction avec notre ontologie. 

Vérifier le but.

## Cidoc - Display

[cidoc](https://cidoc-crm.org/html/cidoc_crm_v7.1.1.html)

pour décrire l'objet connexion par exhibit à : 
- ~~E19 Physical Object (superclaff of E20 human made object et E22 biological object). (parce qu'on se connecte pas à l'immatériel)~~ 
ou
- E18 Physical Thing : on restreint aux objets physique donc pas d'immatériel
ou 
- ~~E70 Thing : parce qu'on veut que ce soit tout (trop general)~~

P16 used specific object (was used for) : c'est une propriété

pour décrire l'exposition connexion par display : 
- E78 Curated Holding (pas utilisé par OntoExhibition)

dans Linked art l'exposition est E89 Propositional Object. C'est un discours. 

E29 Design or Procédure sont trop compliqués

Pourquoi on ne connecte pas l'itération à l'exhibition space? 

Perspective historique donc au centre de cidoc : activité parce qu'avant d'être du contenu c'est du temps. 

E87 Curation activity 

## display:Element, avec ou sans hiérarchie de classe?

Est-ce qu'on s'embarrasse d'une hiérarchie de classe dans élément. Il y a une peut-être une question de cohérence ici en lien avec notre approche de `display:Exhibit`. Suggestion : nous pourrions conserver un seul niveau sous `display:Element`, par exemple support, device, etc. Et n'utiliser que deux sortes d’instanciation, soit les choses sont un exhibit (notre first class citizen) soit les choses sont un Element avec un typage par vocabulaire contrôlé (ex. AAT). Nous pourrons aisément faire usage des restrictions de propriétés en OWL pour classer automatiquement par inférence les Element dans les classes appropriées comme support et device. Éventuellement nous pourrions utiliser SHACL pour contrôler et documenter les usages possibles des vocabulaires et nous assurer que les logiques puissent fonctionner systématiquement. D'ailleurs, il pourrait probablement être une bonne idée de faire intervenir SHACL en lien avec les formulaires pour populer.

## RCC8 

[Lien zotero](zotero://select/groups/2480242/items/3YHP4X2E)

Toutes les choses situées dans l'espace sont des E53 Place. Radical. Les colonnes sont des places. 

CRMgeo (CRM et GeoSPARQL) pour utiliser geoparqle et crm juste pour place.
David ne pense pas qu'il est nécessaire de brancher GeoSPARQL. On utilise certains termes topologiques. Mais on en a plus. 

Très semblable à notre affaire mais ont utilisé une autre stratégie. Le fond très semblable à ce qu'on fait. 

Dans geosparql tout est un objet spatial. 

https://drops.dagstuhl.de/storage/00lipics/lipics-vol086-cosit2017/LIPIcs.COSIT.2017.2/LIPIcs.COSIT.2017.2.pdf

## Interface

ECD trouve que c'est élégant, concis et efficace. Avec économie de classe. 
Mais la question : comment on interface ça pour l'éditer ? N'y a-t-il pas d'enjeux du côté des inférences ?
Peut-être peut-on faire des fiches docu et on exprime ca ensuite par export avec notre ontology
David pense qu'il est important d'avoir accès directement aux inférences. 
Difficile de trouver dev de faire requêtes sparql avec formulaire. David pense qu'on va faire le sparql et le donner au dev. 

On pourrait faire une interface de programmation de triplet simplifiée. 

A-t-on des ex de programmation visuelle en web sémantique ? Sparqlisse ?

Prestataire de service : https://www.takin.solutions/

Est-il possible de faire des visu 3D à partir de notre ontologie ? Avoir un schéma ?

## Article

http://stylo-doc.ecrituresnumeriques.ca/fr/edition-collaborative/ à tester

1_Livrable pour request for comment. 

Publier ontology avec jeux de données : 
avec Feux Pales et une salle de Marie

2_Faire un article en parlant des ontologies choisies et nos choix. 

Pour qui ? : communauté du web sémantique, muséale. 

- Semantic Web Journal ? Article difficile à placer ? Feedback pertinent. 
- DH 2024 Washington : David et Lena ou Zoë
- Humanistica ?

## présentation

Pas forcément l'interopérabilité pour l'instant
Enjeux plutôt du côté de la relation entre objet sont des relations de graphes. 
Technique : on fait du rdf et pas du property graphe. Parce que sinon pas d'ontologie. 
Propriété owl nous intéresse parce que fait déjà bcp de choses rien qu'avec ce qu'on a. 
Expressivité owl est mise à profit grâce aux chaines de propriété, restrictions pas forcément utile ici, mecanisme héritage et propriété c'est rdf. 
Discuter dans l'état de l'art de la docu en xml et modèle hiérarchique. On aurait pu documenter en relationnel mais on peut pas faire d'interférence, on perd en sémantique et les rapports entre les classes. Plus flexible qu'un modèle relationnel. Permet de les lier avec autres ontologies muséales et architecturales. 

Demander à Marie de préparer une salle compliquée et la tester. 

## To do 
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
- @emmanuel : envoyer notes 
- reunion 20 14h. 
- @emmanuel : article sur OntoExhibit?

Calendrier :
- janvier : rentrer fp
- janvier : atelier avec Marie pour un exemple lacunaire
- février : état de l'art
- avril-mai : faire un article 
- avril-mai : prototype pour request for comment


