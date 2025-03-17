---
title: réunion hebdo display x Tractr
description: "Travail sur l'application"
author: ouvroir
date: 2025-02-26
draft: true
tags: 
    - cr


---

# Point fonctionnel Saisie des données

### Objectif :

- Mieux comprendre comment la saisie est faite aujourd’hui avec les outils et process actuel, afin de mieux comprendre comment retranscrire dans une interface

- Discuter des pistes de solutions

- Rappel sur les demandes au niveau saisie présente dans le cahier des charges

  ## Modes de saisie multiple

  L'application propose trois approches complémentaires pour la saisie des données :

  1. Mode liste et formulaire

      :

     - Affichage textuel traditionnel adapté à la saisie sérielle
     - Consultation rapide de l'ensemble des informations disponibles
     - Listes configurables pour des affichages à différentes échelles (exposition, salles, murs, expôts)
     - Exploration d'une saisie textuelle avec autocomplétion basée sur les propriétés du modèle

  2. Mode programmation visuelle

      :

     - Interface graphique inspirée de Scratch ou Max/MSP
     - Permet d'enregistrer facilement des informations complexes sur le positionnement
     - Adapté pour définir des espaces connexes, placer des expôts dans des salles
     - Traitement schématique des relations topographiques

  3. Mode 3D

      :

     - Approche mimétique pour faciliter la saisie des données spatiales
     - Ne nécessite pas de représentations exactes des dimensions
     - Peut être traité conjointement avec le mode programmation visuelle

  ## Types de données à saisir

  1. Les expôts

      (œuvres d'art et autres objets exposés) :

     - Auteur(s)
     - Titre
     - Date de création
     - Numéro d'inventaire
     - Éléments composants
     - Visuels

  2. Les espaces d'exposition

      :

     - Nom
     - Dimensions (si connues)
     - Forme
     - Points d'accès (portes, passages)
     - Possibilité de définir des espaces abstraits sans dimensions précises

  3. La topographie

      (relations spatiales) :

     - Relations entre expôts (à côté de, en face de, etc.)
     - Relations entre espaces
     - Positionnement des œuvres par rapport à l'espace (sur un mur, sur un socle, etc.)

  ## Fonctionnalités facilitant la saisie

  1. Saisie sérielle de sources :

      - Traitement par lots pour éviter de saisir le contexte à chaque information
     - Importation de listes d'œuvres depuis des sources d'archives
     
  2. Sourçage des informations :

      - Chaque donnée est liée à sa source documentaire
     - Gestion des conflits entre sources contradictoires
     - Visualisation des contradictions avec codes couleur
     
  3. Assistance par moteur d'inférence :
  
      - Suggestions de relations topographiques déduites des informations déjà saisies
     - Alertes en cas de doublons ou de contradictions
     - Aide à la gestion des incohérences dans les données
     
  4. Différentes échelles de visualisation

      pendant la saisie :
  
     - Vue par liste : toutes les œuvres, toutes les salles, toutes les sources
     - Vue par élément : toutes les assertions liées à une œuvre spécifique
     - Vue d'ensemble : visualisation spatiale des salles

  Ce système de saisie est conçu pour être flexible et adapté aux besoins de chercheurs travaillant avec des données souvent incomplètes ou contradictoires, tout en maintenant une rigueur documentaire permettant de tracer l'origine de chaque information.

### Notes

- Pas d’outils complet qui existe réellement
  - Les musées ne font pas se travail, ils ont seulement des outils de base de données des collections
  - Souvent de simples listes textuelles
- Prise de note manuelle dans des carnets
- Souvent les archives d’expo qu’ils ont sont vieille et ils font avec de vieux documents papier
- Elle va dans l’institution pour consulter toutes les archives papier ou numérique
  - Elle va chercher la trace d’une oeuvre dans une salle précise
  - Elle trouve la liste d’oeuvre, elle va la rentrer de son côté
  - Ensuite elle regarde dans la feuille de prêt
  - Elle trouve une oeuvre, elle prend des notes, elle note aussi les meta-données
    - L’oeuvre est toujours créer à une source
  - Elle rentre une nouvelle source qui a des oeuvres communes avec la première, et elle va vouloir en premier valider les oeuvres qui sont dans les deux en les cherchant par leur nom ou le nom de la collection

Parfois certains documents changent en cours d’exposition

Les sources ont souvent un code d’archive

Dans son rapport elle fait des schémas des pièces et les positions des oeuvre (en InDesign)

Certaines fois on bosse uniquement sur une salle dans un projet et pas nécessairement sur toute l’expo

La liste d’oeuvre n’est pas forcément une liste d’oeuvre mais plutôt une liste d’élément, les éléments peuvent être des sous-ensemble d’une même oeuvre

Quand il n’y a pas d’idée de comment disposer les oeuvres, création d’un display (un accrochage), regroupement d’éléments, peu importe leur type, et en même temps elles ne sont pas obligatoirement dans un display

Un display est fait pour regrouper des objets qui ont un lien entre eux, et une intentions communes

Jeter un oeil au logiciel Ikea

Logiciel de 3d pour aménagement de ta maison pour des particulier

Ce dont elle a besoin quand on parle d’une liste : https://miro.com/app/board/uXjVNzCVdjo=/

### Idée d’implémentation en vrac

- Importer tout un tas de document disponible (via OCR notamment)
- L’aspect prise de note doit-il être présent? ⇒ Oui ça peut être bien notamment dans une optique pour re-créer l’expo
- Chaque salle a un nom
  - Possibilité de lister les murs, les points d’accroche et de lier des oeuvres à ça
  - Possibilité de lié une oeuvre à une salle sans qu’elle est de mur
- Dans le cas où on a pas de plan du tout et aucune idée, on pourrait créer une salle fictive, une sorte de salle à determiner (un display qui relie les oeuvres) à laquelle on rattache toutes les oeuvres
- On pourra partir d’une liste d’oeuvre sans forcément qu’on est de plan physique pendant un certain temps
  - Puis on match les oeuvres sur des emplacements faits dans le plan
- Création d’un projet sur une expo avec la date de l’expo
  - Est-ce que chaque oeuvre doit avoir une date ?
- La création d’une nouvelle source doit être assez simple à faire à la volée
- Vue en tableau importante ⇒ à determiner comment les tableaux seront affichés
- Ajouter des notes sur une oeuvre (comme un genre de commentaire ?)
- On pourrait mettre de côté/highlight différemment toutes les oeuvres à identifié
  - Valider le status d’une oeuvre, un niveau de fiabilité, de validation
- Potentiel de fusion entre deux oeuvres quand on réalise qu’en fait deux oeuvre saisie séparément via des sources différentes sont en fait les mêmes
  - Dans pas mal de cas on veut pas forcément garder l’historique, et juste écraser les données
- Voir éventuellement si on a une solution en mode Canva pour créer des plans ?
  - On peut utiliser React-flow pour ça notamment
  - Une fois que le plan est saisie grace à une source plan, on veut pouvoir revenir dessus plus tard quand on a des photos de l’expo pour re-valider le plan
  - Il faut aussi pouvoir placer les objets comme les armoires ou bien des éléments comme des textes écrit sur les murs
    - Possibilité de zoomer sur une armoire une vitrine et voir la vue de côté
    - Même logic pour des murs
  - Besoin de mettre des filtres pour choisir ce qu’on peut afficher ou non dans la vue
- Faire matcher les photos avec les oeuvres
- Highlight les éléments qui font partie d’un display
- Réfléchir à une façon de catégoriser des objets
- Besoin de retrouver les sources en liste (elle sera hebergé sur Zotero chez eux), pas forcément besoin de l’afficher