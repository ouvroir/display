---
title: "Réunion display"
description: 
author: ouvroir
date: 2025-09-03
draft: false
tags:
    - cr 

---

- l'interface de dessin

Refactorisation de l’ensemble du code de l’interface pour partir sur une base propre.

Nouvelle version
UX très inspiré de clickup dont retrouve les fondamentaux de navigation.

Top nav : Ont fait des tests sans mais préfère

Ouvroir, vue dans un projet

Autre layout inspirée de Miro qui permet de naviguer dans les projets et navboard applicatif

Entrée dans le projet

## Général

### Top nav
- identité
- barre de recherche qqst le contexte
- rappel du profil

### Barre de gauche
Sélecteur de vue dans la barre de gauche
Permet à l’avenir d’ajouter un module complémentaire à l’avenir comme IA p.e.

### Volet exploration à gauche
Partie contenu en fonction de la partie dans laquelle on est. 
Un seul contenu, permet harmonisation des parties de fenêtres

### Volet minifiche à droite
Inspiration Notion/clickup pour le panneau d’édition à droite. Si possible inclu dans le volet exploration.
Essayer d’avoir une icone, un label et une zone d’action à droite.
Fenêtre modale qui sera unifiée avec la même approche. = moins de bruit.

### Ajout des oeuvres / volet minifiche de droite
Le plus minimaliste possible, en hover voir les éléments actionnables. cf. Notion. 
Lecture/ecriture le même champ. 
Pour les champs descriptions et relation qui sont destinés à plus de contenu, pleine largeur.

L’idée de cette interface modale, c’est qu’elle soit présente pour tous les ajouts : 
- à la fois dans la vue scène
- pour la création des sources

Full screen ? peut être pas nécesaire

travail de simplification des actions le plus possible. Travail de mise en cohérence avec l’interface des sources. Pourra revoir les couleurs, les hover et les icônes au besoin.

= Prendre des repères sur les façons de faire. Un explorateur.

Bouton + header : ajout general
Bouton + barre de gauche : dans le header du volet de gauche. 

## Scène

Simplification de la barre d’outil dans la scène.
Grosse problématique sur le dessin car les actions pas cohérentes.
Besoin être cotextualisé. Savoir ce que veut dessiner

Simplification de la barre. Ajout barre à gauche qui en fonction de ce que l’on a sélectionné proposera une liste d’action adaptée à la situation.

Travail débuté mais pas implémenté.

Actions rapides pour voir tous les objets de type, etc. Peut être besoin d’avoir une recherche, ou filtres

Barre de recherche qui pourrait faire apparaître

Rmq
- pouvoir tt faire à la souris
- raccourcis claviers
- Question drag and drop
- Placement objet dans l’espace

## Onglet source

Mise en place des répertoires de sources.
Création de répertoire
Mise à jour des informations

Sur les sources, deux 
- formulaire source
- possibilité lier listing (à retravailler via interface synthétique)

Modale : Seule chose qui peut être utile passer vers le tableau.

Highlights : Il faut le surlignage texte mais aussi la capture image. 

Retravailler le haut de la zone. 

## Onglet tableau

Pas fini du tout. 

Veulent grouper comme sur clickup. 

On pourra grouper par n'importe quelle colonne (avec champs texte) mais on ne pourra pas regrouper plusieurs colonnes. 

Avoir une phase de vérification nécesaire. 

## Divers

vue triplet réutilisée dans le modal
Peut être ajouter une déclaration

Format d'export CSV
Importation facile sur ce modele la, sans message d'erreur.

## Questions

où saisie triplet ? sera un onglet dans la fenetre d'ajout

versions ?

les warning visuels ?

Se ménager un délai A/R 

## Réunion David 
PRIORITÉ : Oeuvre en plusieurs parties. 
Question sur les auteurs
Liste du Getty : donner 3/4 exemples déjà : Nom - label - traduction - iri

Marie nous fait penser qu'il faut une vignette image pour tous les exhibits (elements et display compris) si possible. 

Seront-elles visibles dans la scène ? Notamment de les voir de biais.

Export des visualisations ?

Quand il y a deux displays a la racine on pourrait considérer qu'il n'y a pas de probleme. resoudre le versionning.

## pt choses à terminer
Barre de recherche: recherche contextuelle à droite du volet de gauche

Gestion des conflits : dans le volet de droite. Avec une surbrillance dans la scène. 