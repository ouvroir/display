---
title: CR display 07 sept 2023
author: ouvroir
date: 2023-09-27
draft: 
tags:
     - cr

---
Présents : Emmanuel, Lena, David, Zoë

# Display

T box: Termes de l'ontologie
A box : Assertions (déclarations)

salle préambule de *feux pâles* 
test d'utilisation du modèle pour décrire l'espace

moteur d'inférence: déduire des connaissances qui ne sont pas déclarées à partir de l'ontologie

Présentation des modifications faites dans l'ontologie par David.

Relations topologiques sont entre les exhibit, mais décrites à la hauteur des objet Thing 
Avec format OWL existe propriétés dans moteur d'inférence.  
déclaration avec moteur d'inférence
- symétrique (si c'est vrai dans un sens, c'est vrai dans l'autre)
- transitivité (a → b → c ) alors a → c

permet de raisonner sur des données manquantes. On peut déduire ce qu'on ne sait pas par un ensemble de conjonctions réunies.


plan de salle du préambule
- 2 arches : adjacents des arches
- 1 cimaise: est en avant des arches
- 1 œuvre visualArtefact
- 2 text d'expo

objet physique
- artefact
- spécimen (objet naturel)

attention, si on considère que les exhibit sont des choses physiques (E18), ça peut poser des problèmes pour prendre en charge la réalité virtuelle, ou du moins la réduit à sa dimension matérielle (Casque de VR)
comme le modèle est orienté vers la topologie de l'exposition, ça justifie cette simplification, tout comme le retrait de artwork

exhibit, puis utiliser CIDOC pour qualifier les objets

Device pour le matériel multimédia.
Les oeuvres sont décrites par CIDOC CRM.

comment arrimer les œuvres déjà décrites, héritage de leurs propriétés, comment les connecter. On ne devrait pas avoir besoin de redéfinir des œuvres
CIDOC n'est pas toujours très commode pour prendre en charge la description des caractéristiques physiques des œuvres, donc est-ce qu'il y aurait des choses à ajouter? 

une des difficultés des relations topologiques est qu'il faut choisir dans quel ordre on va décrire les choses
- ordre de visite? 
- 3 objets (alignés sur la verticale) 

minimum pour le moteur d'inférence mais avec un cas simple il arrive à générer, à partir the isAbove, isBelow et vice versa.

besoin de distinguer support vs surface d'accrochage? 
relation séquentielle entre le titre et le sommaire, plus important que l'inscription détaillée dans l'inscription dans l'architecture.

structure définit des espaces
- supports: bâtiment décrit dans son axialité, corps de logis. espaces articulés entre eux avec une géométrie propre. les aîles sont des corps. 
- Dans le corps de logis, identifier la distribution, logique de distribution interne. Dépend de la structuration du bâtiment , ex: colonnes, piliers qui définissent des travées et des vaisseaux (définis par des fils de colonnes par exemple) alignement des supports, rythme parallèle est une travée
- plutôt des refends percés par des arcades
- description dépend du choix de description, arbitraire et normatif

garder une description minimale, et voir si on peut utiliser bot pur décrire l'espace?
intérêt d'avantage pour l'enchaînement des espaces

si on réussit à partir des œuvres pour partir l'espace, on pourrait envisager l'espace de manière très abstraite sans décrire l'espace depuis l'architecture

ontologie sur BIMERR s'inspire de BOT mais plus pour la ventilation. Nombre de personne / salle. 

qualification d'espace comme espace servant possible? 

dans bot, les espaces contiennent des zones

element 
- "passage" ou "communication"
- interface de circulation? 
~~typer~~sous-classes interfaces au lieu de typer les éléments

manifestement on ne peut pas déclarer seulement que deux zones sont communiquantes. On est obligés de créer une interface pour ensuite créer la communication.



montrer les affordances des outils
ne pas être dans l'attente d'une demande / en réponse à une demande
plutôt aborder la chose sous l'angle d'une proposition/provocations

globalinks Zoe pour tester? MNBAQ, MAC pour Camille



Todo: 
- identifier un cas de documentation partielle
- Essayer de décrire cette expo de plusieurs manières (granulaire et interface)
- Enlever Artwork
- Vérifier la cidoc-crm


jeu: construit une exposition (toolbox)
- avec stylo sur carton plastifié pour écrire-dessiner/effacer
- vue plan de salle; "zoom" sur des murs
- grilles pour proportions? 