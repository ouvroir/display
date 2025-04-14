---
title: "Réunion de display x Tractr"
description: "Compte-rendu de la réunion hebdomadaire du 19 mars 2025"
author: ouvroir
date: 2025-03-19
draft: false
tags:
    - cr 
    
---

[planning](https://docs.google.com/spreadsheets/d/178JopFtcxpMxuGaGkvoTjWyIvqZj1wV5YBU-SNLQAHw/edit?gid=961118961#gid=961118961)


Commence à définir l'interface sur les interactions globales. 

Préparer un jeu de données en json par rapport À ce que renverra l'API.

Faire point Glenn Pierre et David. 

Api devrait renvoyer toutes les données de l'API mais pas les relations. 

Expression besoin plus d’information API


Proposition langage commun pour l’équipe.
Habituellement toujours des wireframes.
6 catégories qui représentent les grandes classes.
Principe, si CRUD quid

Helpeur pour les définitions.
Du vibe programming (coder des interfaces avec IA)...

Rien en bdd, champ des possibles déduit par IA en partant de l’Ontologie.

Display peu élaboré. Mais imbrication pas traitée.

Tableau avec une colonne à gauche. Centre : liste. 

Dans un contexte applicatif, avoir une entrée par projet.

Display, agrégat d’exhibit.

Actuellement modèle très basique. Proposer des options de type et de relation.

Interface modale un peu systématique. On préfèrerait du wireframing et une réflexion design.

Pourquoi changer les libellés dans l’interface par rapport à la modélisation.

L'IA a compris plus ou moins


Architecture technique
Suite à la discussion de la semaine dernière, ont poursuivi le travail sur l’infrastructure numérique.

- API comme seule source de vérité : utilisation e l'API pour gérer tout le reste.
- Utilisation de Supabase pour les données applicatives : droits utilisateurs, etc.
- système de cache entre les deux pour être moins dépendant de l’API et gain possible de performance. Enregistrer Raw dans une colonne de SupaBase.

Question que pose quand invalide le cache.
- fréquence
- webhook, API dire quand changement


## to do
- Voir comment on affiche les displays 
- Créer des fiches des lieux
- Pathsway a afficher
- donner info qui doivent etre À gauche
- donner un export a plat d'une liste de salle feux pales