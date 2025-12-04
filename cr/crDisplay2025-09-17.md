---
title: "Réunion display"
description: 
author: ouvroir
date: 2025-09-17
draft: false
tags:
    - cr 

---
Glenn

ODJ
la possibilité d’afficher la photo des objets dans la scène 3D avec ThreeJS
la possibilité d’ajouter un bouton d’export de scène
les informations sur les auteurs des œuvres
la question des œuvres composées de plusieurs exhibits dont nous avons parl
la connexion des espaces et des exhibits avec les interfaces
une proposition d’utiliser les sets pour gérer les versions de l’exposition


Ce que l’on veut rassembler, ce sont des triplets. Deux solutions s’offrent donc à nous pour traiter les versions des expositions :
- graphes nommés
- rdf-star

Actuellement on utilise les graphes-nommés pour les inférences. Ce qui nous obligerait à gérer dynamiquement des graphes nommés imbriqués.

La solution rdf-star permet d’annoter les triplets. Elle permet donc de rattacher une déclaration par exemple à une source.

Les sets ne permettent pas de réunir toutes les déclarations. Par ailleurs cela génèrerait des entités cidoc que l’on ne souhaite pas

rdf-star permettrait de traiter en même temps la provenance (source) de l’information et les versions d’exposition.

Il s’agirait de partager les métadonnées entre les versions pour les œuvres et les espaces. Les annotations seraient limitées à l’espace Display. Quand on demande la description des ressource. En spécifiant la version, pourrait renvoyer seulement ce qui est propre à cette version.

Pour David, cela implique de pouvoir faire des tests. Jena et Fuseki sont compatibles avec Rdf-star. Il faudrait ajouter un query-parameter dans l’URL et l’ajout d’un identifiant de version. Il peut y avoir des surprises avec le moteur d’API. Complément : https://pad.libreon.fr/WwFA7598TCi5_w9J4VTQXw?both#Suivi-2025-09-04

Cette solution ne devrait pas poser trop problème pour Tractr. Sachant que les requêtes actuelles continueraient de fonctionner et qu’il suffirait d’ajouter un paramètre. Cela peut éventuellement poser des difficultés pour les scènes si on souhaite voir les vues en parallèle.

Quid de la réponse.

Questions :
- mettre photo dans la 3d, seront-elles visibles dans la scène ? Notamment de les voir de biais. une vignette image pour tous les exhibits (elements et display compris) si possible.
affichage des photos
textures facile a mettre en place

- plusieurs exhibits en rapport avec une oeuvre : doit pouvoir traiter information de l'oeuvre. doit pouvoir afficher liste d'oeuvre et liste exhibit : subject of pour aller vers l'oeuvre d'un point de vue conceptuel
entité oeuvre : abstraite
ouvre ref a travaers les exhibit par un champs, besoin d'un point d'accès. Endpoint dispo en début de semaine. 

- pour les auteurs : il faut génerer un identifiant similaire a celui des oeuvres sauf que la fin est la concetanation de la chaine de caractere du label. Optionnellement, l'utilisateur peut le changer l'iri pour un iri de referentiel. Si possible autocompletion depuis wikidata avec API.
personnes et groupes 
on va pas srtructurer données. Champs label pour concatener le nom. 
Autocompletion 

- David a envoyé des listes pour les tests vendredi 4 colonnes
OK

- Quelle est la gestion des "interfaces" dans l'outil ? Comment mettez-vous les exhibits sur les cimaises ? Existe du coté de notre API, David va vous donner des exemples. 
David envoit les exemple déclaration d'interfaces

- export des scènes ?


- versionning
  Quand il y a deux displays a la racine on pourrait considérer qu'il n'y a pas de probleme. resoudre le versionning.
  Considéré comme un graph nommé donc pas d'alerte. 
  Utlisation des graphs nommés serait commpliqué, peut-être utilisation de plusieurs set. 

Avoir deux expositions dans un projet

Travail tractr : 
- finalisation des creation espaces et exhibit. Plus que le champs date. 
- arborescence : actions contextuelles
- meme formulaire dans le volet de droite. 
- nettoyage données
- vocabulaire : apport manuel. On aura accès a supabase pour importe csv. 
- amélioration du dessin space pour l'instant : barre contextuelle. 
- test dessin oeuvre pour mur de face. 
- raccourcis positionnement dans le clic droit volet gauche. Va tester clic droit dans la scene. 
- parametre couleur pour les sols. oeil pour afficher ou masquer element dans la vue. 
- ajouter selection multiple. 


A faire : 

Discussion avec David EM. 
David envoie exemples. 