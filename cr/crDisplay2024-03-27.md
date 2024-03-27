---
title : Rdv Display
author: ouvroir
date: 2024-03-27
draft: false
tags:
    - display
    
---
Présents : WD, DV, ZR

Peut prévenir s'il manque des infos et lesquelles pour inférences ou pour export. 

## quel type de visualisations ? pour quoi faire ?

Façon de voir les données avec un layout : 

Tableau : consultation rapide des données, ie. vérifier que toutes les informations disponibles dans un dossier d'archives ont bien été inscrites

Schéma 3D et/ou 2D de l'espace : faciliter l'imaginaire de l'espace. Permettre une saisie dans le mode de la création d'exposition. 

Schéma 2D éclaté.

Graph : visualisation la structure RDF => pour les archives : repérer des clusters d'oeuvres, qui est lié avec qui sans que cela indique la disposition spatiale (analyse de réseaux).

Diagramme des ensembles : visualisation des ensembles RDF.  Repérer les espaces, ce qu'ils contiennent. Ex : diagramme de Venn. 

Notice : chaque classe est une ressource (page) et on liste ses propriétés et valeurs.

Blocs (style programmation visuelle) : instrument de saisie, on construit le graph RDF avec des blocs. => Facilement remplaçable par le formulaire.

Formulaire (pas une visualisation en soi)

<!--Note Lena: visualiser les affirmations et les inférences: permet de rajouter une affirmation une fois qu'on a "bougé des œuvres" par exemple -->

## Qu'est-ce qu'on exporte ? pourquoi ? dans quels formats ?

### schémas 

Pourquoi ? pour les archives, pour de la documentation/présentation de projets, pour montrer les incohérences.

Toutes les visualisations doivent être exportable. Niveau de granularité pour tous les objets représentés qui sont des ensembles et donc contiennent d'autres à visualiser également.

Formats envisagés : pdf, img, svg
Pas de format 3D. 

### données

Est-ce que y a des filtres pré-établis ? En fait on peut utiliser les mécanismes du formulaires (ie on choisit une classe dans un menu déroulant, ce qui affiche ses propriétés dans d'autres menus déroulant, etc.) sauf qu'on s'en sert comme paramétrage des filtres pour l'export des données.

- en triplet rdf

- tableaux

- projet entier : 
sérialisation de l'ensemble des données pour partager un projet. 

Formats envisagés : json-ld, csv, rdf-xml

<!--export de projet: exemple de OpenRefine-->
## versionning

Comme versionner le projet ? On peut serialiser la base de données pour backups et versionning.

-- projet tartanpion itération 1 
|------ version 1 du projet tartanpion
|------ version 2 du projet tartanpion


-- copy projet tartanpion itération 2 
|------ version 1 du projet tartanpion
|------ version 2 du projet tartanpion

Il faut pouvoir naviguer entre les versions, 

/!\ Il faut pouvoir conserver les métadonnées sur les projets et leur versions.
=> Quel base de données ?

## Base de données des oeuvres 

Pouvoir sélectionner les oeuvres dans les fiches

