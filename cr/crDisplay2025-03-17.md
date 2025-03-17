---
title: réunion hebdo display x Tractr
description: "Travail sur l'application"
author: ouvroir
date: 2025-03-17
draft: true
tags: 
    - cr



---

Commencer à faire des points hebdo normés
Structure de réunion chaque semaine
- discussion
    - suivi du planning
    - questions techniques
    - proposition approche technique
- notes
- planning et budget, tracking (suivi du temps passé)

Partage du notion
- compte rendus
- Temps mis à jour hebdo

Garder grandes proportions de travail. Savent que pas mal d’AR et de temps d’attente.
Vont pouvoir à passer à la prod.

Comme pas de cascade rester vigileant.
Pas de pb pour eux, aussi l’esprit de pouvoir observer où en est.

2e planning de développement pure lorsqu'on arrivera à cette phase.

Ces dernières semaines surtout passer du temps pour travailler sur les parties techniques.

Les deux réunions ont été très utiles. 
Bdd: stocker les utilisateurs et les projets.

Voir jusqu’où pousse la collaboration. Gestion utilisateur fine qui permet de gérer cela.

Utilisation de [Supabase](https://supabase.com), solution hosted ou hébergée. 25$/mois pour la version hébergée.

Est-ce qu’un élément peut exister..
Notion de monde ouvert

Données non-validées

L’API transforme la donnée de Jena en données relationnelles, est-ce que cela a un impact sur la qualité de la données.

Pas évident qu’il y ait besoin de persistance côté application.

Serait plutôt enrichir votre API sur des données que ne voudrait pas stocker.
Informations de collaborations.

Autre solution à laquelle aurait pensé. De répliquer toute la base dans supabase. Trigger bi-directionnel pour synchroniser. Permettrait de tirer parti de Supabase pour fonctionnement appli. Inférence appel à API.
Nombreux clients d’intégration avec Supabase. Si Mongo ou CouchDB Alors perd tt avantage utiliser Supabase.

Quel niveau de quantité modifié pour renvoyer un retour d’inférence ?
Configurable et peut être ajusté.

Savoir si peut modifier les données autrement dans Jena.
Avoir un endpoint de leur côté et enregitré

Données existentes vrai travail réalisé pour tester l’ontologie.

Garder la possibilité de mettre à jour les données dans SPARQL.

David, Glenn a envoyé un courriel. Accès Spec API