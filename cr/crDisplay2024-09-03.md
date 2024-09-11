---
title: Réunion Display
description: Compte-rendu de la réunion sur l'organisation de la journée d'étude
author: ouvroir
date: 2024-09-03
draft: false
tags:
    - cr 


---

Présents : EM DV ZR 

## Bilan ontologie

Présentation DH2024. Trop de diapositives mais c'était bien. 
Bon snapshot d'où en est l'ontologie.
Bilan : 
On décrit précisions sur la localisation mais pas de meta-data sur l'exposition. Description d'un expôt. 
Utiliser CIDOC : Lido 
et celui sur les prêts. 
et linked Art. 
ou SARI https://docs.swissartresearch.net/et/artwork/

Decrire dans cidoc permet de dire que c'est un événement. On pourrait décrire l'expo de notre coté. 

DOLCE est une ontologie fondationnelle qui pourrait nous permettre d’unifier le domaine. 

Est-il possible d’exprimer des données enregistrées dans notre ontologie en CIDOC-CRM ? Ne pourrait-on pas par exemple développer des solutions comme les chaînes de propriétés qui servent de raccourcis dans CIDOC, ce qui permettrait de maintenir en quelque sorte une unité entre les deux modèles.

Classer les expôts avec E18_Physical_Thing présente le mérite de la simplicité et une certaine cohérence avec l’utilisation de E_78 pour les expositions. Les deux classes de CIDOC présentent suffisamment de généricité pour traiter les différents cas de figure en même temps que le même niveau dans l’ontologie.

Difficile d’envisager d’autres alternatives étant donné la prévalence de CIDOC dans le milieu. Le seul problème que cela pose c’est celui de la consistance ontologique.

CIDOC fera bien l’affaire pour la description des expôts. De même pour l’identification des expositions qui sont typiquement des événements temporels. Cependant, le modèle s’avèrera limité pour traiter du contenu réel de l’exposition du point de vue curatorial.

Sur la précision de la description
L’application de l’ontologie pour la description des espaces fonctionne bien. Toutefois, il y a plusieurs façons de décrire des espaces complexes. C’est flexible mais peut amener une certaine complexité.

Pour le moment l’ontologie n’a pas pris en compte les dimensions. Il convient désormais de voir comment nous pourrions introduire des notions de mesure et d’échelle ? Comment documenter les propriétés spatiales de tous nos expôts (œuvres ou cimaises, etc.) et de nos espaces. 

Est-ce que cela doit se faire dans un autre module ? On peut donner des dimensions à des objets dans CIDOC. Toutefois les espaces ne sont pas dans CIDOC actuellement dans notre modèle.

Le MAP pour ND de Paris utilise [E53_Place](https://cidoc-crm.org/Entity/e53-place/version-6.0) pour les espaces intérieurs. Il faudrait alors lier notre ontologie aux lieux. Ce qui pourrait également permettre un début d’alignement.

Alternativement, on pourrait explorer la possibilité de connecter notre ontologie à CRM-Geo.

Information sur les déclarations elles-mêmes : Sourçage. 
Piste : CRMAAA
Nous avons besoin de faire, c’est de la réification ou de pouvoir annoter les assertions (avec RDF*). Le framework RDF utilisé Jena gère nativement RDF*.

L’enjeu de la performance pour traiter ces données n’est probablement pas un réel enjeu car les données que nous traitons sont limitées. D’un point de vue de la performance, cette solution demeure plus performante que la réification ou la création de relations naires.

https://www.ontotext.com/knowledgehub/fundamentals/what-is-rdf-star/

Utiliser RDF* impliquerais
Historical context ontology - Provo Décrit la provenance. 

CRM SOC : dim sociale de Cidoc
DOPHEDA : fait ca en attendant CRM SOC
Mais CRM SOC ne sort pas pour faire une equivalence de CRM AAA. 

HiCO Extention de PROVO pour documenter la provenance des sources.

Tout passe par un Interpretation act. Des actes d’interprétations peuvent être en contradiction. L’ontologie présente l’avantage d’être simple. Voir ce que peut faire avec ça. Mais une solution qui ne nous rattache en rien à ce que faire


## Stratégie plus générale 

Comment rejoindre la communauté: 

- Présenter le modèle au niveau local : Marie
- Discuter avec des projets comparables
- Diffuser plus largement

Faire un appel à commentaires ?
D'abord faire un article ? 
Présentation de DH à diffuser.

1. Documenter plus formellement le noyau stable puis la publier pour Version 0.1 
   Doit être prêt en décembre
2. Travailler sur un article de fond
   Quand ? En est-on déjà rendu là ? Il pourrait encore y avoir du mouvement.
   Attendre d'avoir quelque chose de plus avancé. Pour le moment 
3. Conférences
   Une conférence CIDOC/muséo 
   Une conférence web sem
   DH2025 ? travail RDF Star?  Ou l'appli?

## Journée Etude mois de décembre

À cette étape, le format de l’événement reste relativement ouvert. Notre idée est surtout de pouvoir mettre en commun avec les collègues qui travaillent sur la documentation des expositions afin de pouvoir engager une discussion informée sur différentes questions en conviant des spécialistes pouvant apporter un regard critique sur les différentes solutions.

Deux questions nous intéressent particulièrement :

- l’articulation du CIDOC avec des modèles topologiques
- la modélisation des actes d’interprétation (CRM-aaa vs choix adoptés par Onto-Exhibit)

Dans le cadre de notre travail nous avons notamment choisi de privilégier une approche fondée sur la topologie plutôt qu’une orientation événement. Cela nous permettait de disposer d’un modèle plus facile à manier pour les applications que nous souhaitions développer mais pose la question de la manière dont ont peut se raccorder au CIDOC-CRM. Comme c’est un travail initial, nous souhaitons avoir des retours de collègues sur les solutions adoptées. En ce sens, ton travail sur RCC8 et CIDOC nous intéresse particulièrement, et plus généralement votre expérience sur la documentation du patrimoine culturel.

Par ailleurs, en amont du projet nous avions échangé avec Nuria Rodríguez-Ortega sur ses travaux. C’est la raison pour laquelle nous avions laissé de côté la description des expositions comme événement ou acte performatif qu’elle se proposait de traiter. Nous souhaitons maintenant pouvoir discuter plus avant de la manière dont les deux chantiers peuvent se raccorder. 

Il nous semble par ailleurs que le travail mené récemment par George Bruseker autour de CRM-aaa propose sans doute des solutions qui répondraient bien aux besoins pour la description des expositions.

Nicolas Carboni s’intéresse également à la description des expositions pour le projet Visual Contagion et nous avait dit qu’il était très intéressé de pouvoir participer à une telle discussion.

Pour traiter ces questions, nous pensions donc à un format qui associerait de courtes présentation (10 ou 15 min) à une discussion collective dont nous aurions communiqué la trame thématique en amont de la réunion.

Carboni : ont documenté catalogue exposition en web sem


WORKSHOP Documenting exhibitions with Semantic Web - Journée d'étude de la documentation d'exposition avec le Web Sémantique
8h30 - 11h30 : 5 interventions (public)

Wilhem - 12min
Carboni - 12 min
Bruseker - 12min 
---PAUSE---
Nuria - 12min
Display - 12min 

11h00 - 12h30 discussion dirigée (envoyer plan et notre papier)

Rétroplanning

- 17 décembre
- 17 novembre diffusion
- début novembre, finalisation du programme
  - titres de leur présentation
  - affiliation
  - Bio
  - présentation de l’événement
  - matériel en ligne (doc ontologie)
- octobre : rappel contenu
- septembre : confirmer tous les participants
  Présenter comité d'organisation. 
  Donner les informations techniques et besoins. 
  Demander dispo le mardi matin : pour avoir une discussion informelle sur leur présentation pour mettre un accent sur la discussion. 

## Modéliser l'expo comme statement. 

Nuria en parle comme un acte performatif. Mais proposition trop complete. 
Georges plus concise. En parler avec lui. 

A programmer : 

- API