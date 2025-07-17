---
title: "Réunion Tractr"
description: "Compte-rendu de la réunion hebdomadaire du 19 juin 2025"
author: ouvroir
date: 2025-06-26
draft: false
tags:
    - cr 


---

Olivier n’a pas pu être au front cette seamine (maladie).
Glenn prendra le lead sur la réunion.

Préparage du cablage pour l’API, interviendra dans les prochaine semaine.
Affinage de la vue liste.
Révision des priorités en prévoyant le départ d’Oliver la semaine prochaine. Le calcul de relation a été repriorisé.

Les vues filtres termineés. Version avec les opérateurs OU repoussée.
Ajout d’une barre de recherche sur les listes. Encore du travail d’interface à faire (actuellement seulement fonctionnel). Filtrage sur champs multiples. 

Se sont ensuite penchés sur les relations qui pouvaient être déduites de la scène.

mise en place de librairies tres génériques. 
Vecteur 3D/2D : lignes, boxes, et objets orientés. Pour les espaces polygones 3D.

Dans cette version, transforme un polygone en une boite. Permet d’utiliser les mêmes calculs qu’un exhibit. Sans doute suffisant pour avoir des résultats rapides. Voir si besoin de plus.

Calcul des relations par rapport à la scène : 
Adaptation des détails des espaces et des exhibits dans l’onglet relation. 

Projet assez simple :

4 exhibit et un espace. 
3 sur la scène un exhibit qui n’y est pas sur la scène pour montrer les relations.
Sélection, onglet relation, voit deux espaces. Nouveau travail sur le visuel à faire. Relations validées, celles enregistrées dans l’ontologie, les relations suggérées qui ressortent de la scène. 

relations validées + relations suggérées
Relations qui sont ressorties directement de la scène. 

Voudraient avoir un bouton pour valider. Relation entre les éléments.
Se sont imaginés un système de statut. Des relations enregistrées.  Autres relations calculées dans la scène et validé avec l’ontologie.

Ce qui est dans l'ontoogie correspond a ce qui est dans la scène = check vert. 

@quest quid validation séparée = 3 niveaux.
Ce qu’a besoin c’est le placement sur la scène.

incohérence : à modérer par humain. 
idée de faire vivre dans l’interface. Peut faire des déclarations mais aussi dessiner des choses pour restituer sous la forme de croquis. Idée avec relations suggérées de donnée une représentation dans l’ontologie.

Suggestion à partir du dessin.
Lors de modération : clic sur Check vert : passe dans la validation. 
Correspondance parfait mais aussi possibilité d'accepter incohérence. 

@quest incohérences plutôt déclarations multiples qui sont contradictoires


Mais ici leur propre logique. On se pose la question de les récupérer depuis l’ontologie directement. 
Ah ? Je pensais que c'etait ça justement. 
Mais bien que raisonnent sur les données à partir du positionnement car besoin d’enregistrer info

--> Mais pourquoi y'a des enregistrements qui sont pas dans l'ontologie ? 
l'onto reste la source de vérité. 

Scène qui sert seulement à vérifier et valider en temps réel et de manière visuelle.

Validation d’un humain pour enregistrement dans l’ontologie.

Vu que dessine dans la scène beaucoup de choses tt fait. Simplifier la création de choses que peut déduire de la scène. Mais aussi à chq fois que relations. Que puisse dire un contrôle visuel automatique.

Pas vocation à avoir persistance mais travail à la volée. 
Une forme de saisie d’informations dans l’ontologie.

Dès que dessine une salle, ne l’enregistre pas dans l’ontologie. Permet de valider l’information avant 

--> voir les exhibits non présents

Avoir des logs ?
Qq chose qui pourrait être fait côté interface car refresh possible de l’exposition

Pb rattacher information à une source.
Mécanique qui pourrait également servir dans la vue source.

Avec LLM pourrait avoir relations suggérées 
mecanique upload pdf : suggestions de triplets a partir de ça. 

Sourçage des saisies. 
Pouvoir traiter successivement les sources. Hightlight captures visuelles. 

Pouvoir croiser les sources.
N'aura probablement pas tjrs le temps de numériser tts les sources. Pas tjs de pdf.

pouvoir sourcer autrement que par un highlight. 


Questions
Caméra
Visualisation