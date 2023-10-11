# CR David et Zoë 10 oct 

---

title: Réunion Display David et Zoë 
author: ouvroir
date: 2023-10-10
draft: 
tags:
     - cr
     - display

---

## revue des termes
def de display : entité à définir et mettre en relation avec les exibits
Ens ou agrégat d'expôts agencés pour la présentation d'oeuvre ou arte dans espace expographique. 

exhibit : 
- artifact : tout objet exposé fait par l'humain ou non. 

Pour Zoë un exhibit/un expôt est l'objet d'intérêt exposé pas tous les objets dans une expôt. permettrait de régler histoire d'artefact. a discuter..

Socle dans un espace. En face/adjacent. 

## ABOX

Données FP 

test sur point d'accès Sparql, a mettre en ligne (besoin infrastructure java)

**Créer questions à poser.**

A tester les deux façons de représentation circulation, l'un n'empêche pas l'autre. 



## Test avec FP


Positionner l'exhibit sur les surfaces (ex: tableau au centre du mur)
Réfléchir les propriétés des interfaces. 

Trouver déclaration de niveau de certitude. 1 à 4 (1 étant le moins certain)
Aller voir ontologies Histoire : celle qui utilise **Fuzzyness** : "Intéger des données historiques spatio-temporelles." de Carboni et al. 

S'intéresser à la notion de "Lot d'archives ou d'expôts" à mettre dans les vitrines par ex. 

problème du coin : 
exhib:base001 display:isRightOf exhib:showcase000.
exhib:base001 display:isLeftOf exhib:showcase001.

Le socle est à gauche de la vitrine : 
exhib:base000 display:isLeftOf exhib:showcase000.



## A faire : 
Créer questions à poser à Sparql
Lire ontologie Fuzzyness
Ajouter propriétés : LaysOn; LeanOn; Between
Créer notion de lot? 
Définir que c'est la gauche/droite du regardeur face à l'objet. 
