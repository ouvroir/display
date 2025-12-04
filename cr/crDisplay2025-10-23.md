---
title: "Reunion hebdo Display"
description: "Prise de notes"
author: ouvroir
date: 2025-10-23
draft: false
tags:
    - cr 
    
---

Travail au cours de la semaine passé, dessin des exhibit. Un peu challengeant. Possibilité de dessiner verticalement et possibilités de dessin 2D.
Possibilité de déplacer les exhibits, rotations, redimensionnement et suppression. = refactorisation des exhibits.

Création du mur. Rotation possible. Redimensionnement par valeurs, ou autres.
Possibilité de positionner des éléments sur le mur.

Sélection et focus = changement de vue, passage en vue 2D pour travailler sur un élément. Création des expôts sur mur en 2D 

Retour possible en vue 3D. Solution très générique qui pemret de placer des éléments sur des socles, etc. On pourrait même dessiner à l’arrière de la cimaise... (Buren est ton ami) haha

Multisélection finalisée. 
On peut deplacer une salle entière, avec ses expôts. 

Plusieurs pts bugs affichage, rotation.
Déployé lundi en production pour tests.

Pathways mis de côté pour le moment mais y a réfléchi. Implémentation dans les 2 prochaines semaines. De même que la vue listing.

La vue listing va être utilisée dans la vue source (du coup pas disponible la démo). Développements qui devraient être rapides.

Sujets relations Scene - onto


Revenir sur les connexions d’espace

Nous avions besoin d’une façon de regrouper les différentes versions de l’exposition. Pour ce faire nous utilisons un mécanisme assez simple qui consiste à créer des graphes nommés ce qui permet de regrouper les informations.

Ne change pas grand chose, simplement l’API doit pouvoir receoir une indication de version. Il faudrait passer une nouvelle valeur dans la requête.

Les graphes nommés sont identifiés de la même manière que les IRI. Ajouter un query parameter dans la requête.

Whip des données à la fin du projet. 

enregistrement prise de notes [Loom](https://www.loom.com/)