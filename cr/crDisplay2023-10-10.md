---
title: CR display 10 oct 2023
author: ouvroir
date: 2023-10-10
draft: 
tags:
     - cr
     - display
     - "bot:Interface"
---

# Réunion David et Zoë 10 oct 2023

Participants : David et Zoë 

## revue des termes
def de display : entité à définir et mettre en relation avec les exhibits.
Pour l'instant : ensemble ou agrégat d'expôts agencés pour la présentation d'oeuvre ou arte dans espace expographique. Voir `?comment` dans `display:Display rdfs:comment ?comment .`

exhibit : tout élément expographique mobilisé dans l'expo.
- artifact (sous-classe) : tout objet exposé fait par l'humain ou non. 

Pour Zoë un exhibit/un expôt est l'objet d'intérêt exposé, pas tous les objets dans une expo. permettrait de régler histoire d'artefact. à discuter. Régler l'histoire d'artefact au sens où il n'y aurait finalement que l'expôt, sans nécessité de prendre position sur la notion d'artefact. L'expôt serait l'objet d'intérêt exposé (d'origine humaine ou non).

Socle dans un espace. En face/adjacent.

## ABOX

Données FP

test sur point d'accès Sparql, a mettre en ligne (besoin infrastructure java, à discuter, à suivre)

**Créer questions à poser.**

A tester les deux façons de représentation de la circulation dans l'espace, l'un n'empêche pas l'autre :

- les intersections de certains espaces pourraient permettre de comprendre la circulation
- à un niveau plus fin nous pouvons utiliser `display:PathwayInterface`, et éventuellement qualifier l'interface avec des propriétés (à définir).

## bot:Interface

Note : l'utilité de la notion d'interface n'est toujours pas très claire; nous en testons actuellement l'utilisation, à suivre.

Interface :

> A bot:Interface is a part of the world that is common to some specific zones and elements, and at the boundary of at least one of them. @rasmussen_bot_2020

> The class bot:Interface is used to describe the relationship between some specific zones and elements in detail [...]. This class can be used to qualify (i.e., attach additional information to) any of the aforementioned topological relationships between zones, elements, or zones and elements. @rasmussen_bot_2020

Cas de figure a, b, et c, retenons les cas b et c qui pourraient être intéressant pour nous :

> b) the localisation of the intersection between a pipe and a wall can be used to specify where to apply fire sealing;

> c) the type of access between two zones can be used to specify access restrictions for use in indoor navigation

## Test avec FP

Positionner l'exhibit sur les surfaces (ex: tableau au centre du mur)
Réfléchir les propriétés des interfaces. 
**Réfléchir à propos des propriétés des interfaces**. 

Trouver déclaration de niveau de certitude. 1 à 4 (1 étant le moins certain)
Aller voir ontologies Histoire : celle qui utilise **Fuzzyness** : "Intéger des données historiques spatio-temporelles." de Carboni et al. 

S'intéresser à la notion de "Lot d'archives ou d'expôts" à mettre dans les vitrines par ex. A-t-on besoin de nouvelles classes pour ce faire, ou pourrions-nous travailler avec RDF? Exemples :

- les containers ou collections RDF, exemple : `rdf:Bag` avec `rdfs:member` (non fini, OWA)
- les collections RDF, ex. `rdf:List` qui "describe a closed collection, i.e. one that can have no more members", par contre ça représente un ordonnancement, donc probablement sémantiquement suoperflu, https://www.w3.org/TR/rdf12-schema/#ch_collectionvocab

problème du coin : 
exhib:base001 display:isRightOf exhib:showcase000.
@ -55,9 +58,11 @@ exhib:base000 display:isLeftOf exhib:showcase000.


## A faire :

- Créer questions à poser à Sparql
- Lire ontologie Fuzzyness
- Ajouter propriétés : LaysOn; LeanOn; Between
- Créer notion de lot? 
- Définir que c'est la gauche/droite du regardeur face à l'objet. 
- interface : utilité et propriétés