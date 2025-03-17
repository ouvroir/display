---
title: réunion display x David
description: "Travail sur l'ontologie"
author: ouvroir
date: 2025-02-04
draft: true
tags: 
    - cr

---

Extraction de l’information par l'IA est un autre projet.

## Presentation API

Utilisation du framework [Apache Jena](https://jena.apache.org).

[Shiro](https://shiro.apache.org) pour l’authentification directement dans Jena. 

[CRAFTS](https://crafts.gsic.uva.es) API Configurable RESTful APIs For Triple Stores
Application. 

CRAFTS est une application JavaScript développée en Node.js conçue pour créer des APIs REST à partir d’un triple store. Il s’agit d’une couche logicielle placée entre SPARQL et l’utilisateur afin de lui permettre de consulter les données par l’intermédiaire de REST.

L’application permet de définir des ressources qui fourniront des points d’accès, de les associer à des requêtes SPARQL tout en produisant automatiquement une documentation avec Swagger.

Le résultat d’une requête (avec le membre quetyTemplate de la config d'une API) est un tableau (le résultat std d’une requête SPARQL avec SELECT)

Peut-on renvoyer des réponses structurées en JSON ? 
Dans le fichier de config de l'api, on peut dans "model" définir la description des ressources (RDF) dans une structure en JSON. On peut également avec les query template produire du contenu structuré avec la construction de graph en SPARQL.

## Génération des identifiants
- URI minting? voir https://github.com/ai/nanoid/
- existe-il quelque chose par défaut dans jena?

## Réfléchir aux réponses de l’API
Par exemple, pour la création de ressource, il peut être utile de retourner un identifiant.
A priori, SPARQL renvoie un message "success" par défaut. Est-il possible de produire un message HTTP plus riche en SPARQL ? Jena propose-t-il des fonctionnalités.

## Définition des points d’accès

Créer un Exhibit
---
Cette ressource génère un exhibit 
@path exhibits/create
@param label désignation
@param title? titre de l’exhibit
@param creator? auteur de l’exhibit
@param type? type d’exhibit
@param exhibitionSpace? espace d’exposition
@param tt les métadonnées d’un exhibit

Lister les exhibits par espace
---
@path exhibits/{spaceId}
@param spaceId

Lister tous les exhibits
---
@path exhibits

Créer un espace d’exposition
---
Cette ressource instancie un espace d’exposition
@param label désignation

comment passer les interfaces

Lister les espaces d’exposition
---

Créer un Display
---
@param label désignation
@param title? titre du display
@param creator? auteur du display

Lister les exhibits dans un espace

Insérer un exhibit dans un espace

Définir les propriétés spatiales d’un exhibit

Définir les 


## Évolutions à apporter au modèle de données.
- ajout de labels
- description des expositions : LinkedArt voir https://github.com/ai/nanoid/
- peut-
- jena?
- description des exhibits : LinkedArt
- ajouter les sources : DC qualifié dc:title, dc:description, dc:source, dc:creation + qualificateur, dc:type + qualificateur
- faire un jeu de données enrichi

[Zoë : Aller réviser REST.]

-> Inviter Bob ducharme et Jenny Tennisson au colloque web semantique Links