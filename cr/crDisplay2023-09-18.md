---
title: CR display 18 sept 2023
author: ouvroir
date: 2023-09-18
draft: 
tags:
     - cr

---
# Display

hiérarchie de différents types d'entités
essayer d'intégrer la building topology ontology (BOT)

tester les cas pratiques

## Etat de l'art
recherche de modèles pour représenter sémantiquement une exposition et son espace
entre VIMCOX et nous, il faut s'assurer qu'il n'y a rien d'autre qui nous passe sous le nez

EM a épluché
- DH conferences
- IEEE 
- Google Scholar

Rien de concluant par rapport à la représentation d'une exposition et une ontologie
Il reste le ACM[https://dl.acm.org/ccs] à éplucher. 

Trouvailles intéressantes (entrées sur zotero Ouvroir_display)
- *Towards a semantic indoor trajectory model* Kontarinis et al 2021 → fait écho à la conversation sur la façon de représenter la séquence des œuvres dans l'optique d'une visite d'un espace d'exposition. à lire (case study au Louvre)
- *Museum Ontology-based Metadata* Hajmoosaei 2016 à lire (ne semble pas parler de CIDOC)

OGC's IndoorGML standard, à rechercher http://www.indoorgml.net/

Davallon: relations topologiques (proximal) vs relations séquentielles (temporel)

## BOT
Présentation de BOT pour les nuls : c'est une ontologie assez simple. Besoin de l'étendre pour nos besoins. C'est un module parmis d'autres en rédaction. 
- visualisation en graphe permet de comprendre les relations
- regarder la spécification pour comprendre les classes

entité de plus haut niveau: zone 
Toutes sont les entités suivantes sont des sous-classes de Zone mais sont différentes
site 
↓ 
building
↓ 
storey : étage
↓ 
space: relation topolgique entre les espaces ex: espace A a pour zone adjacente B
Possibilité de définir des sous-propriété pour 

Elements: portes, fenêtres, murs, on doit créer les sous-classes : pour nous les expôts sont un element
Interface est une classe : nature des relations entre différents éléments
- accroché
- posé sur

interface permet d'évacuer la notion de surface
- entre les expots et les murs?
- devient l'espace d'accrochage
- interface met en relation des choses

on va définir des sous-classes de interface
- propriété interfaceOf 

interface: on peut mettre plusieurs choses dessus.
Element
- artwork
    - item

## Test avec «Feux pâles»

building
↓
storey

plan de salle: 12 salles = 12 spaces ? ou l'expo entière est un space? 

→

pas de portes entre les salles → ouverture tout le long
m
entrée
- salle 0  (préambule) = space 
    - 1 élément mur
    - 1 interface 
        - 1 artifact: toile
        - element informationExhibit. value = titre de l'expo
        - element informationExhibit. value = réalisé...
    - 1 élément mur
    - 1 interface
        - artifact: cartel topo = en bas à droite de l'œuvre
- salle 1 = space

distribution du bâtiment, définit/découle des circulations
- espaces servant
- espace distribuant

Espace qui dispose de deux interfaces
Est-ce que les interfaces sont localisées? 

interface
- interface de circulation
- interface d'accrochage

- espace A (salle 0) → interface de circulation 1  → espace B (salle 1)
     - géolocalisation 1
- espace A (salle 0) → interface d'accrochage
    - artifact
    - informationExhibit 
- espace A (salle 0) → interface de circulation 2 → espace B (salle 1)
    - géolicalisation 2

- vitrine est un expôt
  - la vitrine est sur l'interface sol (partie du sol)
  - 3 elements showcase
      - interface du sol Z
- relation avec le mur
- chaque showcase est ensuite une interface pour des expôts


entre salle 7 et salle 8
1 œuvre: parquet qui traverse les 2 espaces → intersect zone?

expôt ne peut pas être une sous-classe de Element car element est trop spécifique
mais on aurait besoin de la propriété d'Element pour intersectZone
Il faudrait définir d'autres propriétés au niveau de l'expôt pour établir le type de relations topologiques qu'il peut y avoir entre les expôts et les espaces

## Suite

essayer de garder ça minimal pour la représentation des espaces, dont on ne connaît pas nécessairement les dimensions et qui ne sont pas nécessairement des boîtes

Spatialisation non prise en compte par BOT?

dissocier l'espace et les artefacts: pour les disposer "en face", "à côté" et modéliser l'espace "en creux"

Relations topologiques (et non géospatiales)
Vérifier les ontologies qui peuvent inclure topographie. 

- En vis à vis
- Dans 
- au-dessus
- en-dessous
- à côté
    - à droite
    - à gauche

**prochaine étape**: mettre les expôts en relation topologique

s'assurer que les espaces non pas besoins d'être définis par des propriétés trop définies/précises

idée de brainstorm
- comment est-ce que les gens vont renseigner ça? 
- base de données avec des propriétés à renseigner
- [scratch](https://scratch.mit.edu/): langage de programmation visuel (python)
    - briques/blocs que l'on connecte entre elles
    - briques abstraites: salles dans lesquelles on met des objets
    - approche visuelle: dessin qui n'est pas un dessin
    - À cheval entre la modélisation 3D mais sans la contrainte de la précision: exprime la schématisation

comment travailler de manière schématique
si le schéma embarque une sémantique, alors il y a un modèle en dessous

exercice: penser en blocs
échelle générique → échelle géospatiale