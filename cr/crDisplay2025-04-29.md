title: "Réunion Display x Tractr"
description: "Prises de notes réunion"
author: ouvroir
date: 2025-04-29
draft: false
tags:

   - cr 

---

Bcp discussion sur le placement automatique : pose problème. 

Pb erreur manque de précision.
Besoin d’une surcouche où devra forcer le plaçage automatique et pouvoir déplacer des éléments.

Dès lors qu’accepte de déplacer des elmt et déplacer des zones, le placement auto devient secondaire. Seulement une aide au placement et au dessin.

Attention : cas où l'on a aucune info. 
Les restituer avec une convention graphique

On attend de vous que vous proposiez des solution graphiques de visualisation.

Idée de pouvoir visualiser des objets pas encore placés autant que déjà placés.

Dans tous les cas le placement automatique ne résoudrait pas ts les pb. S’est dit que devrait dans tous les cas dessiner quitte à ce qu’un engin de placement vienne les placer sur la scène ou ailleurs.

Mise en place de la stack finale.
Passé d’un projet de test, vérification de possibilités et orientation dans une direction qui repose sur supabase.

Besoin d’avoir persistance de données pour faire le proxy avec API

- supabase
- postgresql
- authentification

Valider ensemble. 
Pas de coût, par rapport au projet pas de coût en plus que le serveur. À part si besoin de service tiers.

Installation de Coolify. Déploiement sur cette base sur notre serveur. 
[Coolify](https://coolify.io) qui dev la liste sql

Supabase, react. Mise à jour des librairies. Récupéré les avancements du POC. 

Ajout de persistance pas cablée avec Supabase. Deux niveaux de persistances :

- sur les données API supabase + API
- locales pour les settings de vues

Récupération du projet Corner (datait de 3 ans). Beaucoup de problématiques déjà résolues. Storage
Glenn a récupérer les features et bonnes pratiques. 

Niveau visuel pas beaucoup changé mais gros travail de mise à jour et de nettoyage.

Zone/space rectangles, passé en polygone. 

Grille adaptative. Reprise du système de grille et de voxel de Corner qui permet d’avoir une unité de dessin simplifiée. Mais si pour ce projet parfois pas besoin d’être précis pourrait avoir besoin de l’être.

Grille adaptative plus ou moins précise. = échelles de dessin variable

Refactorisation affichage des zones et des espaces.

Mise en place d’un système de dessin.

Tooltip rapidement prototypé.
Direction avec vue.

Pb caméra 2D 3D à régler
Système de layer pour choisir affichage.

3 modes : sélection, plan et dessin
pas encore repis info métadonnées. Olivier va travailler sur la partie récupération.

Partie dessin pour dessinner des zones.

Reprendre les contrôles clavier dessin d'adobe. 

## À faire : 

organiser atelier : visualisation d'entité sans relation

Conceptualiser le produit avec wireframe. 
Avoir une démarche de design. 

faire reunion de deux heures. 

Glenn donnera le cr en amont pour qu'on prepare nos questions-reponses. 