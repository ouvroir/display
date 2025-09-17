---
title: "liste Tractr"
description: 
author: ouvroir
date: 2025-08-04
draft: false
tags:
    - cr 

---

Les formats de dates doivent être au standard du W3C et permettre la saisie de date plus ou moins précises ou d’intervales. ex : 2025-01 ou 2025, ou 2025-10/2026 ou 2025/2026 ou 2025-01/2026-08


## Projets (tractr.ca/projects)

- Nom du projet : string
- Description : string
- Date de création : date
- Date de mise à jour : date
- Statut : (à faire, en cours, à réviser, fait)
- Observation : string [note de travail]

Remarques : Discuter du partage avec d’autres utilisateurs

## Users

- Nom : string
- Prénom : string
- Description : string
- Username : string
- Password : xxx

## Sources

### Dossier
- Titre : string
- Description : string
- Lieu de conservation : string
- Cote : string
- Type : (Folder | Subfolder)
- Dates : date avec possibilité d’intervale (format W3C)
- Lien : uri
- Statut : (à faire | en cours | à réviser | fait)
- Observation : string [note de travail]

### Item
- Titre : string
- Description : string
- Lieu de conservation : string
- Cote : string
- Type : (photographie | document technique | document écrit | document de gestion | autre)
- Dates : date avec possibilité d’intervale (format W3C)
- Lien : uri
- Statut : (à faire, en cours, à réviser, fait)
- Observation : string [note de travail]

Icones pour les types de sources.

## Spaces

- ID : uui
- Label : string
- Description : string
- Dimensions : format ??

## Exhibits

- Label (*label*) : string
- ID : IRI
- Description : string
- Dimensions : format???
- Catégorie : (élément scénographique | élément communicationnel | objet exposé | dispositif)

Élément scénographique : `furnishings (works)` http://vocab.getty.edu/page/aat/300037336
Élément communicationnel : `information forms (objects)` http://vocab.getty.edu/page/aat/300220751
Objet exposé : `object genres (object classifications)`   http://vocab.getty.edu/page/aat/300185712
Dispositif : E78 Curated Holding https://cidoc-crm.org/Entity/e78-curated-holding/version-6.2.2

### objet exposé

- Titre : string
- Date : date
- Auteur(s) : string
- Type d’objet : (Termes dans http://vocab.getty.edu/page/aat/300185712 Est-il possible de proposer dans une liste déroulante les termes déja utilisés et en autocomplétion l’ensemble des termes (il existe des traductions) ?)

### dispositif

- Date : date
- Auteurs : string
- Liste d’exhibit : ??
- cf. partage des méta de Exhibits

### élément scénographique

- Type d’élément : (Termes dans http://vocab.getty.edu/page/aat/300037336 Est-il possible de proposer dans une liste déroulante les termes déja utilisés et en autocomplétion l’ensemble des termes (il existe des traductions) ?)
- cf. partage des méta de Exhibits

### élément communicationnel

- Type d’élément : (Termes dans http://vocab.getty.edu/page/aat/300220751 Est-il possible de proposer dans une liste déroulante les termes déja utilisés et en autocomplétion l’ensemble des termes (il existe des traductions) ?)
- cf. partage des méta de Exhibits