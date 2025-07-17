---
title: "Réunion Tractr"
description: "Compte-rendu de la réunion hebdomadaire du 10 juin 2025"
author: ouvroir
date: 2025-06-10
draft: false
tags:

   - cr 


---

## État des lieux de l’API

David s’apprête à déployer une nouvelle version de l’API.  

Cf. lien vers les notes de travail au début de CRAFTS qui contient des exemples, des remarques et des détails sur les implications d’inférences.

Création de ressource, on utilisera les mêmes points d’accès avec la méthode PUT. On indique l’API Display et le type comme pour les requêtes GET avec les différents types. On fournit l’IRI de l’exhibit que l’on souhaite créer ou mettre à jour.

Le corps de la requête est un objet JSON formaté conformément au modèle JSONLD comme ce que renvoie l’API avec les relations à la fin.

Il est donc possible en même temps de faire la création d’une ressource avec ses métadonnées ou indiquer en même temps ses relations.

Pour la méthode PUT pour le moment encore en local. Pourra normalement être mis à jour cet apm. Pour le moment testé : exhibit, exhibition, set et spaces encore à revoir. Mais normalement tout est fonctionnel et implémenté.


Pour faire des modifications une route PATCH est disponible.
Utilisation du format JSON PATCH.

Discussion sur les jettons pour mise à jour.

Exemple création d’un exhibit, ajout de relation = OK.

Quand veut créer une relation entre deux Exhibits, comment va-t-on créer la relation ? Dit-on pour un que est en face de l’autre. 

Question inférence. Lister les ressources mises à jour.
Si possible techniquement, éviterait beaucoup de requêtes inutiles. Permettrait de cibler les refresh. Sinon devrait le faire sur tt l’exposition.

Peut-on connaître le résultat de toutes les IRI modifiées ? 
--> David doit regarder quelle approche prendre pour cela et évaluer la faisabilité.

Selon, peut changer notre manière de travailler avec l’API. Mais même si plus tard, pourrait optimiser le traitement.

Discussion pour les types d’information
Format texte