---
title: CFP DH Showcase 2024, 19 janvier 2024 @ UdeM
---

# Contexte

Démonstrations de projets et outils dans le champ des humanités numériques.

## Quoi

Par exemple :

- bases de données et répertoires
- outils d'analyse numériques
- des revues ou publications électroniques
- des applications mobiles

## Comment

- trois sessions de cinq ou six démonstrations
- commencent par une présentation de trois minutes
- ensuite période de discussion au cours de laquelle les spectateurs pourront circuler d'un projet à l’autre pour discuter avec les participants, qui auront un ordinateur à leur disposition pour poursuivre la démonstration

# Proposition

Emmanuel Château-Dutier\*\*, Lena Krause\*\*, Zoë Renaudie\*\* et David Valentine\*

\* Présentateur, EBSI, Université de Montréal<br>
\*\* Département d'histoire de l'art, Université de Montréal

Titre : Documenter les accrochages d’exposition ou de collection muséales : une approche ontologique

Cette démonstration vise à présenter une ontologie informatique développée au sein du laboratoire Ouvroir d’histoire de l’art et de muséologie numérique de l’Université de Montréal. Cette ontologie se destine à décrire de manière explicite et formelle les traits d’un accrochage ou d’une exposition (proximité et contiguïté des œuvres, vis-à-vis, etc.). Dans un contexte documentaire souvent lacunaire, ce modèle abstrait permet l’enregistrement de l’information historique concernant les accrochages grâce à une approche spatiale définissant les possibilités d’inférences topologiques entre les objets de l’espace expographique. La démonstration s’appuie sur un jeu de données décrivant l’exposition *Feux pâles* de Philippe Thomas (CAPC de Bordeaux, 1990) et sur l’utilisation d’un outil graphique pour la formulation de requêtes et l’exploration des données.

117/100 mots

# Plan de travail

Heures estimées en date du vendredi 5 janvier 2024.

## Phase 1 : modélisation

estimation : 10h

échéance : 10 janiver

- [ ] valider l'encodage de Feux pâles (analyse, suivi et ajustements sur l'encodage accompli par Zoë); 5
- [ ] parallèlement au point ci-dessus (back-and-forth) : stabiliser l'ontologie, en particulier à partir du développement des propriétés topologiques; 5
- [ ] tag v0.0.0 alpha vitrine 2401
- [ ] dresser la liste des fonctionalités manquantes (si nécessaire)

## Phase 2 : entrepôt RDF et SPARQL

estimation : 12h

échéance : 14 janvier

- [ ] import local des données dans Fuseki
- [ ] préparer et tester les points d'accès; 2
- [ ] valider les inférences et les graphes nommés (deux versions de l'entrepôt, avec et sans matérialisation des inférences) : quelques cas de test; 5
- [ ] préparer et tester des requêtes pour la démo; 5
- facultatif : visualisation comparative des graphes

## Phase 3 : outil graphique pour exploration des données

estimation : 9h

échéance : 17 janvier

- [ ] brancher Sparnatural sur les différents points d'accès pour comparer avec et sans inférences; 2
- [ ] préparer et tester les versions graphiques des requêtes; 5
- [ ] présentation préliminaire à l'Ouvroir et récolte des commentaires (ajustements finaux le 18 janvier); 1
- démonstration le 19 janvier; 1

## Phase 4 : déploiement

Phase facultative. Permettrait aux membres de l'équipe de tester les propositions du projet.

Besoins :

- Apache Tomcat
- Git
- accès SSH
- domaine

## Remarques

Plusieurs étapes déjà avancées sur la base du projet Display. On stabilise les travaux et on en paufine certains aspects.

Il serait utile de déployer le projet en ligne (phase 4), mais le temps nous manquera assurément. Comme l'ensemble du travail sera développé localement, je propose d'utiliser ma machine pour la démonstration (modalités à confirmer avec l'organisation de l'évènement).

L'utilisation de Sparnatural est documentée de façon assez exhaustive et ne semble pas poser de défis particuliers, mis à part le temps requis pour faire fonctionner l'application de façon satisfaisante d'ici le 19 janvier.
