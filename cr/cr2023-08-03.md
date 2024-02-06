---
title: CR display 03 aout 2023
since: 2023-08-03
draft: false
tags:
     - cr
     - display

---

# Rencontre display

## Compte rendu des avancements concernant l'état de l'art

De façon générale: a laissé pas mal de notes de lectures, dans Zotero

travaux de Biella et al.
- projet qui a débuté ~2000 
- ARCO~
- modèle VIMCOX (XML) a examiner, mais n'est pas détaillé dans les articles (tag vimcox dans Zotero)
- beaucoup de liens morts → spécification du modèle VIMCOX 1.0, trouvé sur internetArchive. A décortiqué la spécification de la description technique du modèle, on trouve tous les éléments du modèle (Wolf et al.)
    - peu de détails sur la nature des entités
    - ça prendrait des cas d'utilisation pour comprendre plus précisément comment ils s'en servait. Pas convaincu que ce soit super important
    - donne une certaine hiérarchie d'éléments, à réfléchir
- on représenté des salles d'exposition
- Autres articles: 
    - ecosystème d'applications: VIMCOX, VIMEDEAS, Replicave (X3D), E-curator
    - thèse de Daniel Sacher: publication la plus récente de ces travaux? est-ce qu'on a accès à la thèse? (version payante sur Barnes and Nobles)
    modèle arborescent n'est pas forcément le plus judicieux

conférence de Carboni et Al. (DH Unige) circulation des objets muséeaux, participation d'artistes à des expositions
- patrons conceptuels à partir de CIDOC-CRM
- patron conceptuel: prendre une ontologie et définir des façons de l'utilisation
- Carboni et al représente des expositions et liste les artistes participants, source historique → archives lacunaires. Ont une façon qui rend compte des sources historiques
- mobilise CIDOC, liens entre expositions, objets, artistes
- prise en charge des incertitude
- pistes pour la question des lacunes dans les archives: gérer et représenter l'incertitude des sources historiques (hypothèses à partir des sources)
- pourrait être un bon point de départ pour représenter des objets périphériques 
Carboni a publié avec Bruseker aussi

CRM archeo, Doerr
- a commencé (pas encore terminé)
- extension archeo de CIDOC, modèle de représentation 
- pas convaincu que ça nous sera utile
- CIDOC n'est déjà pas très simple. CRM arche est une extension qui vise à représenter des choses très spécifique comme des couches stratigraphiques et des procédés de fouilles archéologiques
- axé sur la dimension temporelle: transformation des couches stratigraphiques dans le temps
- représentation d'un espace volumique: embedding est un objet pris dans une couche stratigraphique
- propriétés qui pourraient peut-être nous être utiles → dans les notes
    - hasPhysicalRelation: relation entre unités stratigraphiques
    - très dans le volume, espaces volumiques
    - relations topologiques
    à discuter, relations topologiques: à côté, en avant vs précision de mesures
    voir s'il y a des modèles en lien avec l'archéologie qui sont un peu plus "digestes"

Est-ce qu'ils sortent de l'ontologie CIDOC pour gérer la stratigraphie? 
processus d'accocrochage n'est pas documenté à la même échelle que les processus de fouille (événement = expsition, et non acte d'accrochage)


Ontologie des primitives géométriques, Nathalie Abadie
- représentant la forme et la localisation d'entités topographiques
- visualisation du modèle disponible [en ligne](http://data.ign.fr/def/geometrie/webvowl/index.html#)
- très mathématique: décrit des lignes, des formes, des surfaces
- servirait à décrire des relations topologiques
- va y retourner pour prendre des notes

Dépouillé l’existant sur Zotero.
Reste de l'état de l'art: todos, approfondir, autres recherches
- Computer application archeology CAA: voir s'il y a d'autres choses que la stratigraphie pour réfléchir aux relations topologiques
- Conférences sur le web sémantique + Semantic web journal
- panorama de modèles de métadonées

Aimerait bien être sûrs qu'on n'a pas loupé de travaux sur l'exposition, l'accrochage et sa modélisation mais on ne sait pas comment.
- Google scholar? 
- courriel à Nicola Carboni et George Bruseker?


### À discuter
- Temps accordé à la revue de littérature: s'en servir surtout pour réfléchir et être au courant de ce qui se fait, formuler des hypothèses de départ
Actuellement 10


Quelle forme est-ce que ça devrait prendre? on reviendra là-dessus pour voir si on veut publier ou trouver une modalité profitable

Faire des tests, ensuite revenir sur l'état de l'art en vue d’une publication éventuelle.

2 parties dans le projet
- opérationnal: outil qui opérationnalise un modèle (labo)
- recherche: recherche sur la documentation des expositions en général (CIÉCO)

Objectif: faire réagir les collègues. En ce moment, c'est trop abstrait.


précision de représentation
mise en réseau de données

suivi sur le contrat
- 60h au lieu de 40h, voir par la suite.
- 1/3 pour la revue de l'art donc 20h


## Expérimentation de modélisation: vérifier/confronter les idées
entités, relations
- relations entre expôts et surfaces d'exposition

ensuite on décide comment on l'implémente

concept: ce qui définit une exposition = groupe d'œuvres commissariées 

exposition qui se déploie dans plusieurs lieux, 
- instance d'une exposition

relations entre les surfaces d'exposition 
surface (display) renvoie à un espace construit géométriquement
- avantage: on y appose des propriétés topologique, comme les expots
- que fait-on si l'accrochage n'est pas dans un plan cartésien? 

relation ontologique entre l'expot et la surface

Jean-Luc Raynaud, [container zero](https://www.centrepompidou.fr/fr/ressources/oeuvre/cAbo9BA?hcb=1&cHash=5231ea52f4e583526b8870361015d239)
- container 0 au centre pompidou
- espace d'exposition à l'intérieur du musée

reenactment, artistes dont l'œuvre commissaire des œuvres → oeuvre = exposition

comment on fait pour les œuvres performatives? à discuter avec Mélanie (Axe 3)
certaines expositions ont des caractères performatifs

approche matérielle, challenger voir si on prend des approches moins matérielles? 

performance qui a lieu dans plusieurs salles d'exposition

surfaces sont situées les unes par rapport aux autres

quelle importance pour la circulation dans l'espace? 
- placer un humain dans l'espace
- ordre de visite de l'exposition
- important pour diversifier les cas d'usages
quelle importance des textes et des cartels dans l'exposition? 
expots: texte, cartel

Jean Davallon, Le pouvoir sémiotique de l'espace
tout ce qui est dans la salle est un expot

hiérarchie avec un genre expot, qui contient des œuvres et des objets muséographiques
si la surface est un expot, elle hérite de toutes ses propriétés

tester avec des œuvres problématiques
[Bertrand Lavier](https://fr.wikipedia.org/wiki/Bertrand_Lavier)
- oeuvres compositionnelles, deviennent un display

display
moins centré sur la médiation
s'intéresse plus à la dimension curatoriale de l'exposition

travailler la granularité de l'exposition

@lenamk: retrouver les détails sur la pratique de Szeeman
- documenta 5
- when attitudes become form
livre rouge (publication récente?)

notion en archive, RICO, agrégat documentaire
- est-ce que la stratégie d'agrégat pourrait être intéressante

Comment est-ce qu'on développe la relation entre les espaces? Portes, communication entre les espaces
séquence: cote à cote, ...
- entrée de l'exposition: où commence l'exposition? (œuvres dans les couloirs/escalier avant l'espace )
- quel impact du format? 


inverser le processus de production de la salle? pas l'édifice mais l'accrochage qui crée la salle.
Cimaise qui crée l'espace (dispositif sur le mur qui facilite l'accrochage, ou cloison mobile qui aménage et subdivise l'espace)

Comment modéliser les séquences ordonnée ? distribution

Faut-il traiter les points d’entrée

Daniel Buren, œuvre = installation (cabanes) qui est l'exposition

Sons, odeurs, couleurs, penser tout ce qui n’est pas visuel. L’expérientiel ? Prendre en charge la dimension installative des exposition et des œuvres.

Gonzales Torres
- candy : diverses formes d'exposition
- stack: feulles que les gens peuvent prendre

Boltanski objets

importance de la salle: œuvre dans un salle qui est fermée vs qu'on traverse

## Suite

Implémenter un modèle pour voir ce que ça fait et le soumettre à la critique ?
Ou continuer le travail de modélisation? 

Relation entre expot et surface: retravailler / raffiner avant de mettre à l'épreuve

Implémentation simple: petite ontologie avec [Protégé](https://protege.stanford.edu) et la visualiser avec [WebVowl](http://vowl.visualdataweb.org/webvowl.html)

choisir une exposition, il faut structurer quelque chose avec pour le tester
soit un formulaire, soit on cible des cas de figure qu'on implémente nous et qu'on code à la main

Comment rendre le prototype visible pour en discuter ?

Test de formulaire, quelque chose à traiter dans une étape plus avancée.

Comment montrer les biais ou les raccourcis ontologiques de ce petit modèle.
et les anticiper?

Comment en faire une preuve de concept pour pouvoir se faire les dents dessus? 