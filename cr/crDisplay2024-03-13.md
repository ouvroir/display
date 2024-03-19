---
title : Notes rdv Display
author: ouvroir
date: 2023-03-13
draft: false
tags:
    - display
    
---
Présents : WD, DV, ECD, ZR

- revenir très rapidement sur les conclusions de la dernière réunion 
- discuter des questions restantes
- rédiger bullet point des fonctionnalités ?

## Questions prochaines réunions

### comment tirer parti du modèle de données pour la saisie

Modèle de données : permet de faire des inférences pour avoir un retour de saisie. Retours visuels? Indications? Contraintes? 

2 modèles de saisie : 
- libre mais renseigne messages
- Un plus fermé ou choix contraigne les solutions possibles. 

Modèle de données peut permettre d'assister la saisie de manière interactive. Epuiser les objets dans une liste. 

Validation/inscription des inférences. Est-ce qu'on peut rejeter des inférences cad ne pas les inscrire en base de données ? Pourquoi devraient-elles être rejetées ? 

Le moteur d'inférences : 
si inférence de l'entrepot de données : requetes sparql va faire toutes les inférences en liens. générent les inférences. 
Sortie peuvent etre csv ou json. Comment cette sortie est structurée? 
La meme chose quand t'utilises des règles. Ne change rien aux interactions sur modeles de données. Regles permettent de créer des inférences supplémentaires pas de contraindre. Comment contraindre alors? Définir des règles [SHACL](https://www.w3.org/TR/shacl/).

Types infos dont on a besoin? Pas toutes les inférences : 
Si qqchose deja déclaré : cela devient contradictoire. 

Il y a deux modes de saisie :
- un mode tolérant aux incohérences pour traiter des sources
- un mode plus contraint pour tirer parti des informations déjà saisies

Règles de validation

Intérêts du modèle de données pour la saisie : 
- assister la saisie par l’auto-complétion grâce au moteur d’inférences
- informer l’utilisateur d’incohérences dans la saisie en utilisant la validation
- contraindre ou assister l’utilisateur dans les déclarations


Les modèles d’inférence fonctionnent sur des modèles logiques. Si des informations incohérentes sont saisies, cela ne permet pas de formuler des inférences. 

Il faut pouvoir travailler sur des données incohérentes. Il n’y a pas besoin de faire des inférences pour savoir s’il y a des incohérences dans les données.

Entrepot Shacl permet de créer contrainte. 

À partir de quand l’outil cesse de fonctionner quand il y a des incohérences ? 

À quelle échelle l’application fonctionne-t-elle ? Ensemble de l’exposition ? Salle ou espaces ? C’est sans doute au niveau de l’espace qu’il sera le plus important de travailler:
- avoir ensemble des déclarations topologiques d’un espace
- etc.

L’utilisation du modèle de données apporte des fonctionnalités supplémentaires par rapport à une saisie simple.

Un des intérêts de l’utilisation des inférences est de permettre d’éviter la saisie d’informations implicites. Mais si le système s’arrête de fonctionner en raison d’une incohérence dans la salle, alors

Faut-il envisager le système de manière fluide ou bien fonctionner par mode (contraint ou libre) ?

Si j'accepte d'entrer des incohérences... aimerait pouvoir travailler tout de même avec ces outils.
Est-il possible d’au moins faire des inférences sur les attributs qui restent encore cohérent.

inférence : compléter propriété
validation : renvoie message d'erreur
contrainte : application de règles pour assiter la saisie

-> Faire des essais pour savoir si ces outils sont capables de faire des inférences partielles sur les seules données cohérentes. C’est souvent mal documenté. Dans Protégé, rien ne marche s’il y a une incohérence. Mais il est possible qu’un moteur d’inférences continue de fonctionner partiellement.

Shacl permet d'etre très granulaire : validation globale, partielle... A tester. 

Trouver la fluidité entre les modes. 

[Shacl-JS](https://github.com/TopQuadrant/shacl-js)

## quel type de visualisations ? pour quoi faire ?


<!--Note Lena: visualiser les affirmations et les inférences: permet de rajouter une affirmation une fois qu'on a "bougé des œuvres" par exemple -->
## quels formats d’exports


<!--export de projet: exemple de OpenRefine-->
## versionning










## Résumé dernière réunion : 

### modalités de saisie de données : Saisie graphique vs Saisie formulaire

Besoin de pouvoir faire des A/R entre des vues différentes:
- module de saisie textuelle (pas de long formulaires)
- module de visualisation

Avoir des points de vue différents :
- vue par liste : toutes les œuvres, toutes les salles, toutes les sources
- vue par element: toutes les assertions liées à l'œuvre X
- vue d'ensemble : visualisation de salle

Plusieurs niveaux d'échelle. 

Dans le système, chaque information doit être sourcée. Cela implique peut-être un traitement processuel de ces sources. Obtenir la liste des sources et pouvoir traiter toutes les informations de chaque source. Cette solution permet de ne pas avoir l’obligation de renseigner un contexte pour cette information.


### articulation du modèle de données avec l’application

Besoin : stocker l'information pour qu'elle soit disponible dans Javascript.

Dans l'idéal : 
Modèle de travail serait un objet json.
Modèle de données dans entrepot RDF. 

Quelles sont les solutions pour : 
- afficher le back-end RDF dans le front-end Json
- mettre à jour les données rdf depuis le json
- faire des inférences depuis le front end si données dans entrepot rdf

To do : 
- schéma du flux des données
- est-ce qu'on mettre un triplestore en production pour expérimenter avec ? (1 serveur, tomcat, ssh)
- outils à tester :
    - les outils côté clients (jslond, moteur d'inférence?)
    - outils côté backend (ORM)
    - => tester pour comprendre les choses!!

### où sont gérés les inférences

Approche A (front + back) : Quand contacter le triplestore pour réaliser une inférence ? Est-ce qu'on le fait au moment du changement de notice/de vue ? (temporalité)

Approche B (front seul) Il y a peu de données chargées en mémoire, est-ce qu'on peut tout (population + inférence) traité côté client ? (système sans API)
=> comment gérer la potentielle perte de données ? (sauvegarde régulière = mise à jour du triplestore ~ toutes les 3min) 

Approche C (front + un tout petit peu de back) : 
- population faite du côté client (modèle chargé en mémoire) mais inférence côté serveur



## Inspirations 

Ce qu'on aime et ce qu'on aime pas dans : 

- Cuisine IKEA


- Scratch


- (Sweet Home 3D)[http://www.sweethome3d.com/SweetHome3DJSOnline.jsp?id=847367&name=Feux%20Pales&lang=en]
J'aime : 
appli web ou telechargeable
open-source
Prise en main facile
Liste d'objet type 
Objet type peuvent être facilement ajustés, modifiés
permet d'afficher ou non un objet facilement

J'aime pas : 
Design Interface 
export uniquement en .sh3d
pas possible de cacher les dims

- Visualisation abstraite 


Parle-t-on de :
BD-oracle et [docuverse](https://docuverse.io)
Omeka-s
[DSpace](http://e-chastel.huma-num.fr/)
https://strapi.io/


## rédaction 

### description fonctionnelle des besoins

#### Articulation du modèle de données avec l’application
Nous souhaiterions trouver une solution pour : 
- que notre sémantisation soit le plus près possible de l'interface
- utiliser notre modèle de données en rdf mais stocker l'information pour qu'elle soit disponible dans Javascript
- faire des inférences efficaces

#### Topographie de l’exposition

La topographie d’une exposition temporaire ou de collection implique la disposition d’éléments dans l’espace, sur des socles, aux murs, au sol, suspendus au plafond, dans des vitrines, ou selon divers dispositifs d’exposition. L’objectif de notre application est de pouvoir inférer des données topologiques tout en saisissant le minimum d’informations, permettant ainsi de rendre visuellement les aspects spatiaux de l’exposition. Notre modèle vise à établir des relations entre les objets mentionnés dans la liste d’expôts pour décrire l’accrochage.

Ce modèle documentaire est destiné à archiver le processus d’exposition pour les archives, mais aussi à servir de support à la création d’expositions futures. Il doit être adaptable pour fournir des informations aussi lacunaires que très précises.

### Description des fonctionnalités

#### Créer un compte et se connecter 
Chaque utilisateur a son interface et accède à ses projets (pas de multi-utilisateurs). Il doit être envisagé que dans le futur la gestion utilisateur se fasse par le biais d’une autre application que nous développons nommée Common. 

#### Entrer des données 

#### Types de données
Les expôts
Les espaces
La topographie

#### Sources des données

#### Visualiser des données

#### Versionner

#### Exporter

#### Interactions et manipulation de données

#### Autres besoins



ecrire à Digital museum

