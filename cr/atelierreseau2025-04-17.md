title: "Atelier analyse de réseaux"
description: ""
author: ouvroir
date: 2025-04-17
draft: false
tags:

   - cr 

---

## Présentation atelier

Emmanuel 

https://ouvroir.umontreal.ca/actualites/evenement/2025-04-17-fr

## Programme 

11h – 13h : Présentation de projets

    Talitha Motter, Bâtir des liens : l’analyse des réseaux d’une revue d’art
    
    Talitha Motter est titulaire d’un doctorat en histoire de l’art de l’Université de Montréal. Ses recherches portent sur les réseaux de l’art actuel formés par les revues d’art numériques au Brésil, notamment à partir de l’analyse des critiques d’art publiées par ces revues (FRQSC, https://resensibles.hypotheses.org et http://www.reseaux-sensibles.art). Intéressée par la diffusion de l’art sous toutes ses formes, elle a cofondé la revue d’art collaborative Arte ConTexto (https://artcontexto.com.br) et réalisé divers projets d’exposition.
    
    Emmanuel Château-Dutier, L’analyse de réseau dans le projet d’ANR Experts, expertises du bâtiment, Paris 1690-1790
    
    Kristine Tanton, Considérations relatives aux modèles de réseaux et à leur analyse : premiers pas
    
    Pascal Martinolli, Bibliothécaire en histoire et pour la formation
    
    Discussion ouverte


14h – 16h : Atelier pratique

    Initiation à la manipulation des données et à la visualisation avec Gephi.

Cet atelier est ouvert à tous, sans prérequis techniques. Venez explorer comment les outils d’analyse de réseaux peuvent enrichir vos recherches !

Si vous ratez ça, nous vous conseillons la formation de Martin Grandjean.

## Présentation des projets 

### Analyse de réseau, introduction

Emmanuel 

Désigne un ensemble de méthodes fondées sur la théorie des graphes pour étudier un phénomeme relationnel. 
faible appropriation de ces méthodes pour l'HDA 
_The Network Turn_ 

[NA+DAH](https://sites.haa.pitt.edu/na-dah/), A Getty Advenced Workshop

analyse de réseau en shs.
démarche quantitative 

Social Network Analysis

L'analyse repose sur une modelisation, c'est-à-dire la transformation de phenomenes du monde social en données 

Réseaux visuels les plus habituels. 

Definiton d'un graphe : Graphe, structure de données abstraites. Peut être orienté ou non. 

Pour utiliser l'analyse de reseaux en SHS : il faut def un type de relations entre les entites etudiés. (mots clefs, signature, liens entre la population et la revue par exemple). Cela depend des questions de recherche que nous posons. 

(Beauguitte, 2016)
Ensemble fini et non vide de points symbolisant les acteurs et d'un ensemble fini et eventuellement de ligne symbolisant ???


réseaux orienté-désorienté. 

Représentaiton réseau tabulaire, régulière, hierarchique, irrégulières, sur matrice. 

Representation graphique. 

Type de question : 

- comment qualifer le réseau ? 
- certains individus occupent-ils une place particuliere dans le reseau? 
- certaines relations sont-elles spe? 
- les individus partagent des caracteristiques? 
- peut-on créé sous ensemble pertinents ?

Vocabulaire de base : 
G = {V, E}
sommets, noeuds, points ou acteurs
liens : relations, arcs, ou arretes
ordre d'un graphe : nombre de sommets
taille du graphe : nombre de liens 
graphe vs réseaux : présence d'attributs 

Des **objets construits**

- choisir de modeliser ses relations par un réseau simple est une simplification. 

Exemples : 

- Francis Bacon Network
- Tudor Networks 
- Mapping the Republic of ?

### Bâtir des liens: analyse des reseauc d'une revue d'art

Talitha Motter 

Côte plus technique et méthodo

question du réseau : "editer une revue, c'est coudre avec des lignes de pensée "
Fraga 2013
lien entre l'art et la science 

"rendre visible, ces petits noeuds"

réseau sensible : 
ces revues vont influencer les membres du réseau. 

Critiques d'art en TEI-XML 

Réseau en GraphML 

- graphe vers le réseau 
- noeud avec des attributs

Dans le cadre de sa recherche à étudié trois réseaux : 

- artistes-thèmes
- auteur·es et artistes-themes
- artistes-referencés 

Revista Desvio, revue brésilienne d'étudiants en art. Prouver que les auteurs sont fondamentaux pour l'etabilissement du discours d,une revue. 

requete XQuery : 
Pour repérer tous les artistes-thèmes du corpus d'une revue donnée. Pour chaque artiste-thème : Id, Nom, Pays de naissance, EIC, WKD. 

Création des noeuds
pour chaque artiste-theme (ville de naissance, etat de naissance ect). Attributs? 

Création des liens

Création des réseaux
Cytoscape, app facile d'utilisation. 
utilisation de la couleur pour la visualisation 

Groupements 
Connecteurs : artistes entre les groupements, centralité d'intermedialité sup à zéro. 

Approfondir la compréhension de l'approche éditoriale d'une revue

Questions: 

Limites d'une visualisation de réseaux? 
une facon de modeliser un pb. Depend aussi bcp de questions qui sont posées. 

A fait une analyse qualitative plus que quantitative. L'exercice de visualier le réseau a fait naitre les questions. 

Est-ce-que la visualisation a permis d'ordonner l'attention ? 
Oui, aider à naviguer et voir les "rencontres" entre les textes et les auteur·rices. 
Est-ce-qu'une fois, le corpus a été parcouru, est-ce-que Talitha était satisfaite? 
Plus organique, pas d'ordre bien def. 


## Réseau de l'architecture médiévale en Amerique du Nord : le cas de Henri Focillon

Kristine Tanton

Henri F. comme une figure importante du domaine aux US. Interet de Kritsine pour mieux comprnedre non suelement l'historiographie, mais aussi d'une genealogie intellectuelle. Pour se poser la question, qui nous(histoirien en architecture mediévale) a formé, qui les a formé. 

comment tracer les fluctuactions d'interet dans l'architecture medievale occidentale et les "trends" dans la formation des étudiant·es? 

Yale epicentre de Focillon aux US, avant sa mort en 1943. 
poste prof 33-44 ------ il est mort en 43 mais faisait cours jusqu'en 44 ?!!!!--
Pas mal des étudiant·es ont donné des séminaires
il a donné des séminaires en francais à Yale, ce qui a attiré intellectuels français à Yale. 

Dictionnaire critique des historiens d'art. Entrées catalogue inha. 
Mathemaics Genealogy Project 
Six Degrees of Francis Bacon 
Art History Tree

Récolte des données : 
Nombreuses sources : liste des departements, site web des diplomés, soit de la bd ProQuest, recolte des informations a partir des tables des matieres des essais. Mais aucune de ces sources sont parfaites. Les données relatives aux directeur·rices ne sont pas structurées de maniere cohérente. Toutes les universités ne fournissent pas non plus obligatoirement les comités de thèse. 

Ce projet nécessite unne collete de données en masse

Palladio, gephi

[Visualizing Historical Networks ](https://histecon.fas.harvard.edu/visualizing/index.html)

comment organiser et structurer les données ? 

Conseille la lecture de cet [article](https://programminghistorian.org/en/lessons/creating-network-diagrams-from-historical-sources)

### Timeline Tree. Developper un code reproductible pour la visualisation de données liées historiques

Pascal Martinolli

Bibliothecaire pour l'histoire et la formation. 

Coucher données du cloud sur une chronologie. 

a la base : ameliorer la dataviz dans Wikidata

Pourquoi un arbre de relations sur une chrono ? 

- visualiser des donnees dirigiees et relationnelles
- pertinente
  - add une dimension historique (réduit la centralité)
  - facilement comprehensible/lisbile
- peu dev
  - pas de modele générique
  - rien de facile à utiliser


Inventaire de l'existant? 
EntiTree : ne fait pas un graphique de tout l'arbre. 
Irish Electoral Parties : assez complexe a comprendre quand même 

Comment ? 
Données en entrée CSV 

- facile a générer et a manipuler
- 2 colonnes

Code simple et generique dans un navigateur: 

- visuelement non-rigide
- zoom

Avancé

- le contacter si on voit des projets
- article a venir dans programming historian 

Avancement? 
need une forme graphique et visuelle?


Une prosopographie pourrait être définie, a minima, comme une étude collective qui cherche à dégager les caractères communs d'un groupe d'acteurs historiques en se fondant sur l'observation systématique de leurs vies et de leurs parcours.

Intéret d'une collection d'outils minimals pour l'ouvroir

- reframe

## La repartition des affaires au sein de NA+DAH


Maitre maçon sur son arbre perché, tenais dans son bec un fromage

Relation archi - maçon

Difficile a faire dans cytoscape ou gephi donc ont utilisé Julia. 

