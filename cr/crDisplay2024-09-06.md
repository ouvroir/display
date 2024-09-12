---
title: Rencontre David Valentine
description: Compte-rendu de la rencontre
author: ouvroir
date: 2024-09-06
draft: false
tags:
    - cr 
---

# Rdv David Valentine, 6 septembre 2024

Discussion préliminaire

Pb interfaçage de l’API

Intérêt de pouvoir travailler nativement en RDF avec un TripleStore. Les données sont limitées, le contexte de recherche justifie que l’on cherche à implémenter nativement la base en RDF.

Il existe des templates de requêtes SPARQL.

## Gestion des données

La quantité de données à gérer est relativement limitée et produite dans le contexte de l’application. Ce cas d’usage ne justifie pas l’utilisation d’une base de données relationnelle intermédiare. On propose une gestion native des données RDF.

### Installation et configuration du framework Jena

L’application utilise le framework Jena (Apache). L’application est libre et open source et réunit une importante communauté. Il s’agit aujourd’hui d’une solution standard pour le déploiement d’applications du web sémantique. C’est sans doute actuellement la meilleure option dans l’environnement du logiciel libre. L’environnement est mature et implémente le protocole SPARQL 1.1 mur-à-mur, elle offre des outils pour travailler avec SHACL et RDF star.

Le framework Jena est constitué de plusieurs composantes à utiliser conjointement ou séparément :

- RDF
  - RDF API
  - ARQ (SPARQL 1.1 compliant query engine)
- Triple Store
  - TDB (strore)
  - Fuseki (SPARQL end-point over HTTP, REST-style)
- OWL
  - Ontology API
  - Inference API

La principale composante que nous utiliserons est celle du Triple Store. Celle-ci repose sur TDB, ARQ et Fuseki. En pratique, les inférences peuvent être implémentées au niveau du Triple Store. Ce dernier s'installe facilement sous forme d'application Tomcat.

#### Création d’un SPARQL endpoint

L'accès aux données est géré dans Fuseki.

- Fuseki : serveur SPARQL over HTTP Apache Jena Fuseki
  - permet de configurer les points d'accès : URL, read, write, authentication, etc.
  - permet de configurer autant de points d'accès que nécessaire (au les organisant par type d'accès, par exemple public, closed, read only, etc.)
- protocole SPARQL 1.1

#### Configuration d’un triple store

Les données sont gérées dans le triple store TDB2.

Fonctionnalités :

- graphes nommés
- RDF*
- requêtes RDF
- inférences

En pratique, lorsque l'on travaille avec le serveur http pour les points d'accès, toutes les configurations sont gérées par la couche Fuseki. 

### Interface de requête SPARQL (en option)

Configuration d’une interface de requête YASGUI. Hautement configurable et flexible, à adapter selon nos besoin, si jugé nécessaire pour une raison ou une autre en cours de route.

Petit écueil potentiel : le module d'affichage des résultats de YASGUI ne prend pas en charge RDF*. Le moteur de requête ARQ et Fuseki sont OK (200, all good), l'erreur vient de l'interface d'édition qui ne peut pas parser. Cela dit, l'affichage des et la transmission des données seront gérés par l'application Display.

### Moteur inférence (revoir)

Les triplets issus des inférences peuvent soit :

- être matérialisés, cad insérés dans façon permanente dans le triple store; conditions : inférés avant l'insertion, demande plus d'espace (et plus généralement TDB demande beaucoup plus d'espace disque que les BDD relationnelles)
- être générés au démarrage du serveur (après l'insertion mais pas dynamique, c'est une autre forme de matérialisation moins robuste : si on modifie le moteur d'inférence et on redémarre, les données seront différentes)
- être générés dans le processsus de requêtage et renvoyé dans les résultats; dans ce cas il ne sont pas stockés; conditions : moteur d'inférence côté serveur s'occupe de tout, mais demande plus de calcul, donc potentiellement lourd sur de grands jeux de données, demande moins d'espace disque; exemple d'écueil potentiel : tenter de supprimer un triplet inféré n'a pas d'effet tant que la logique qui soutient sa création est en place...

Du côté serveur, les inférences peuvent être générées par des moteurs prédéfinis par le framework Jena. Intéressant mais peu flexible, ne convient pas nécessairement aux besoins, potentiel très important de bruit dans les données.

La solution efficace pour les inférences côté serveur serait d'implémenter nos propres règles, seulement celles qui nous intéressent, cad celles définies par l'ontologie. Le problème avec les moteurs de Jena est qu'ils vont bien au-delà de nos besoins, comme ressource A owl:differentFrom (toutes les autres ressrouces du jeu de donées, donc des milliers de triplets complètement inutiles), sans pour autant implémenter toutes les choses intéressantes, comme les chaînes de propriétés, qui sont un aspect important de l'ontoliogie Display dans le contexte méréologique.

### API Définition des requêtes pour la création de l’API

Requêtes préparées pour les fonctions principales de l’API

Crafts Configurable REST APIs For TRiple Stores (CRAFTS)

- Analyse des besoins
- définition d’un schème d’API
- rédaction des requêtes SPARQL 
- Implémentation des points d’accès

#### CRAFTS

CRAFTS est un outil facile à utiliser pour tous ses utilisateurs (data consumer and data manager), flexible, générique et domain-agnostic.

Son module de validation est robuste : il ne nous laissera pas implémenter des solutions techniquement problématiques pour le fonctionnement de l'API.

Définition d’un schème d’API : solution clé en main avec CRAFTS, voir Vega-Gorgojo (2022, section III, B)

Rédaction des requêtes SPARQL : prise en charge par CRAFTS des templates de requêtes SPARQL, ce qui permet de configurer une librairie de requêtes basée sur nos besoins. Les requêtes sont exécutées en passant par les point d'accès proposés par CRAFTS.

Deux chemins nous intéressent particulièrement :

- /apis/{apiId}/resource (get, put patch, delete):
  - opérations sur une ressource grâce aux templates de requêtes
  - mapping vers une structure JSON de notre choix pour le body response
- /apis/{apiId}/query : Send a parametrized query as configured in an API
  - on configure des requêtes, donc définition d'une librairie de requête accessible par l'API
    - la réponse de l'API est conforme à SPARQL 1.1 Query Result, selon le type de requête utilisée (l'API transmet la réponse du serveur SPARQL, facile à utiliser pour n'importe quelle équipe de développement)
    - on peut configurer des paramétres d'URL (query parameters) pour sélectionner les requête et passer des valeurs à l'API qui s'en sert pour remplir les templates de requêtes

D'autres chemins existent pour des fins d'administration (générer des tokens, etc.) ou des dumps.

#### Autres possibilités vs CRAFTS

- voir Vega-Gorgojo (2022, section II) : tableau comparatif des outils qui permettent d'opérer une API par-dessus SPARQL
- CRAFTS offre le plus de flexibilité, répond manifestement à tous les besoins de Display

#### Documentation de l’API

Documentation de l’API au standard [OpenAPI Specification](https://www.openapis.org)

### User (à discuter selon que Jena...)

Users : quels accès aux données du Triple Store?

- data manager
- API (requêtes vers localhost)
- éditeur de requêtes SPARQL optionnel (même domaine)
- point d'accès public en lecture?

#### Documentation Jena

- https://jena.apache.org/documentation/fuseki2/fuseki-security
- https://jena.apache.org/documentation/permissions/
  - https://jena.apache.org/documentation/permissions/example.html
- https://shiro.apache.org/configuration.html#Configuration-INIConfiguration-Sections

The Jena Permissions layer can be used to restrict access to specific graphs or triples within graphs.

#### CRAFTS

web developers: « programmers that develop applications for the World Wide Web » 

craftsperson (data manger): « knowledge engineers that are in charge of setting up CRAFTS APIs »

- web developers use tokens (gérer par CRAFTS)
- data manager uses authentication pour configurer l'API

### Déploiement

#### Serveur Fuseki et triple store

Déploiement sur serveur configuré en environnement Java muni d’un point d’accès SSH.

- configuration du conteneur de servlets Tomcat
- installation des outils du framework Jena
  - Fuseki2 (.WAR)
  - l'installantion de l'application  dans Tomcat vient avec tout le nécessaire pour un serveur HTTP fonctionnel et pleinement compatible avec SPARQL 1.1 (UI, HTTP, points d'accès, ARQ, TDB2 et moteurs d'inférence)

Les fichiers de configuration de Fuseki sont au format Turtle. Ils sont consitutés de deux principales composantes :

1. Fuseki Server configuration file : configuration pour chaque jeu de données
2. shiro.ini : configuration des paramètres de sécurité du serveur

Ces fichiers sont suivis avec Git et déployés lorsque nécessaire :

- soit directement avec `scp`
- soit avec `git` à l'aide d'un dépôt vide distinct du working directory sur le serveur de prod

Le serveur Fuseki doit être redémarré pour prendre en compte les nouvelles configurations. Cela peut être effectué en exécutant un script déclenché par les hooks de git.

Tâches cron avec scripts pour backup de données (fréquence à discuter)

#### Serveur CRAFTS

Le serveur CRAFTS est une application Node.js. Il peut être déployé et mis à jour en utilisant les hooks de git.

### à fournir par le client

un environnement serveur sécurisé accessible par SSH

- java
- git
- ssh
- outil systèmes, accès root avec sudo
- nano
- node ?
- https