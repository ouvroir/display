---
title: Rencontre David Valentine
description: Compte-rendu de la rencontre
author: ouvroir
date: 2024-09-06
draft: false
tags:
    - cr 
---

## NRdv David Valentine, 6 septembre 2024

Discussion préliminaire

Pb interfaçage de l’API

Intérêt de pouvoir travailler nativement en RDF avec un TripleStore. Les données sont limitées, le contexte de recherche justifie que l’on cherche à implémenter nativement la base en RDF.

Il existe des templates de requêtes SPARQL.

## Gestion des données

Les données à gérées sont peu nombreuses et sont produites dans le contexte de l’application. Ce cas d’usage ne justifie pas l’utilisation d’une base de données relationnelle intermédiare. On propose une gestion native des données RDF.

### Installation et configuration du framework Jena


L’application utilise le framework Jena (Apache). L’application est libre et open source et réunit une importante communauté. Il s’agit aujourd’hui d’une solution standard pour le déploiement d’applications du web sémantique. C’est sans doute actuellement la meilleure option dans l’environnement du logiciel libre. L’environnement est mature et implémente le protocole SPARQL 1.1 mur-à-mur, elle offre des outils pour travailler avec SHACL et RDF star.


#### Création d’un SPARQL endpoint

- serveur SPARQL Apache Jena Fuseki
- protocole SPARQL 1.1

#### Configuration d’un triple store

Les données sont gérées dans le tripleStore TDB2.

Fonctionnalités:

- graphes nommés
- RDF*
- requêtes RDF

### Interface de requête SPARQL (en option)

Configuration d’une interface de requête YASGUI

### Moteur inférence (revoir)

inférences

### Définition des requêtes pour la création de l’API

Requêtes préparées pour les fonctions principales de l’API

Crafts Configurable REST APIs For TRiple Stores

- Analyse des besoins
- définition d’un schème d’API
- rédaction des requêtes SPARQL
- Implémentation des points d’accès

### Documentation de l’API

Documentation de l’API au standard [OpenAPI Specification](https://www.openapis.org)

### User (à discuter selon que Jena...)

### Déploiement

Déploiement sur serveur configuré en environnement Java muni d’un point d’accès SSH.
- configuration du conteneur de servlets Tomcat
- installation des outils du framework Jena (Fuseki, TDB2, etc.) <!-- préciser la liste -->

Scripts pour la configuration et le déploiement de l’API


### à fournir par le client

un environnement serveur sécurisé accessible par SSH

- java
- git
- ssh
- outil systèmes, accès root avec sudo
- nano
- node ?
- https