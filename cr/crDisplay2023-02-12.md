---
title : Réunion display 12 fev 2024
author: ouvroir
date: 2023-02-12
draft: false
tags:
    - display
    
---
## Préparation réunion 

Lena : 
Pensez à la rotation des œuvres dans un espace d'exposition. 
Et définir version. différencier versions dans une même exposition et itinérance ? 
Versions d'accrochage dans des itérations. 
Ex : 
Expo A
Lieu 1 : Paris 
version accrochage 1
version accrochage 2
Lieu 2 : Moscou
version accrochage 3

Reflexions : 
Est-ce qu’on intègre la lumière au display? Les assises? 
Ajouter estrade? 
ex : la fête de Marisol. 

 To do 
- Vérifier les hierarchies pour connecter à Cidocexhibit = E18; display = E78
- organiser une présentation équipe OntoExhibit + présentation de notre projet + Nicolas Carboni? Proposer une revue critique de leur travail.

Trouve aussi qu'ontologie de Nuria est trop complexe. Il travaille sur ontologie d'exposition aussi. Decor peint dans eglise. 
Organiser atelier

- inviter robert.sanderson@yale.edu pour nous présenter discuter de linkedart. 

- Discuter avec Georges Bruseker? à son compte [TAKIN](https://www.takin.solutions/) maintenant donc peut-etre tarifé ? Peut-etre notre prestataire de service?

pour l'implementation des requêtes en fonction rep david. 

- montrer Display à la personne des ontologies du getty et à linked art David Newbury

présents à Conférence dh 2024

- générer taches dans le projet dans github.

- @tous : relire maj définition 
- @tous : réviser les choix de l'ontologie
- @emmanuel : vérifier si AAT fonctionne
- @emmanuel : envoyer notes conf Ontoexhibit
- @emmanuel : article sur OntoExhibit?

Calendrier :
- janvier : rentrer fp OK
- janvier : atelier avec Marie pour un exemple lacunaire
- février : état de l'art
- avril-mai : faire un article 
- avril-mai : prototype pour request for comment

Publications : 
- Semantic Web Journal ? Article difficile à placer? Feedback pertinent. 
- DH 2024 Washington : David et Lena ou Zoë
- Humanistica ?

Implémentation de Shacl dans l’ontologie permettrait de dire des choses et des choses à pas dire  puis de signaler incohérence. 

Ajouter intersectingExhibit
Sparnaturel

## CDC

On procède à un Obétat des lieu du document, Zoe a de la difficulté à définir ce qu'on demande d'un point de vue technique, voudrait savoir à qui s'adresse le CDC, à quel type de développeur.

Le fait de pouvoir écrire les objectifs en liste à puces a beaucoup aidé pour avancé. Avoir un retour sur le contenu écrit. Pour les fonctionnalité pas écrit encore. Travailler sur le schéma.

Difficulté de l'exercice: définir le périmètre du technique et le périmètre fonctionnel. Ce type de document ne doit pas préciser le technique, c'est au prestatire de démontrer sa capacité à proposer un solution adéquate.

Distinction entre front-end et back-end: si David veut bien se charger des requêtes SPARQL, il faudrait cibler un développeur centré front-end (design, interface utilisateur) mais il faudra aussi préciser l'interfaçage front-back, traduction par API. 
Zoe se concentre donc sur le front end, les fonctionnalités de l'applications.

Zoe a travaillé sur un document visuel qui est déjà proche d’un wireframing. Lena proposition d’aborder la question sous la forme d’un storymapping plutôt que d’un wireframing. Cela consiste à dire ce que l’utilisateur peut faire, pourquoi il voudrait faire ça. Centré sur les besoins et les intentions des utilisateurs sans entrer dans les détail.

Cette modalité retenue en partie parcequ’a besoin de travailler visuellement pour bien comprendre les fonctionnalités.

Dans le document écrit: 
- présentation du projet 
- objectifs généraux de Display
- prestation de service
    - outil de saisie de données : produire une liste d'expots
    - liens vers des sources
    - données topo: les placer dans un espace
    - visualisation abstraite des données topo
    - exporter/archiver

est-ce que c'est le backend qui va gérer les inférences? (mais alors, comment le penser du côté du front end)

Objectifs:
1. assister la saisie d’information (listes et types de vues). Il faut énoncer la difficulté, penser une interface adéquate. Interface qui ne soit pas une boîte à clic (plutôt, l'exemple ikea cuisine)
2. travailler avec des données floues ou incomplètes, pour produire des visualisations de données
    - différentes échelles: juste la salle, juste une œuvre
S'il faut couper dans la prestation, c'est ce qu'il y a autour qui couperait, ces deux objectifs sont les piliers. Liste d'œuvre pourrait être un csv. 

Tension entre entre le visuel et les données

Lena est aller voir le planificateur. Une approche visuelle qui permet de placer les objets relativement facilement. Mais si on veut rétirer la notion de dimension des salles on pourrait seulement cacher les dimensions même si informatiquement on en a besoin.

Circularité entre le visuel et les données → on pourrait considérer que ce sont deux vues sur le même objet. 
Permettrait d'avoir un modèle 3D pérenne qui ne dépend pas des stratégies de représentation 3D qui sont techniquement situées.

On va traiter des déployement d’expositions différents, voir ce qui se passe autour d'une œuvre. Ici le besoin de données important.

Traiter données liées d'une oeuvre (ex: sa place dans différentes exposition de collection). 
- produire une vue juste de l'environnement de l'œuvre
Le mettre comme option, permet de faire comprendre le projet au développeur

On n'est pas obligés de faire des reconstitutions complètes. Enjeux de la variabilité des niveaux de précisions. Si on arrive à traiter en même temps l’information très précise ou peu précise.

La prestation de service doit répondre à cet enjeu: doit proposer une solution à la problématique de précision. C’est une question fonctionnelle qui peut être adressée dans le cahier des charges.
Décliner les sous enjeux en laissant ouvert. 

Comment l'interface prend en compte les inférences produites en backend?

Fonctionnalité autour de l'inférence et du raisonnement (ex: un objet n'est qu'à un endroit à la fois)

Ratio vs dim. 

Comment du passe en arriere plan de la boite de visualisation à la base de données. Si on essaye de documenter une exposition soit dans Kitchen Planner soit dans SweetHome 3D, voir comment faire pour avoir les bonnes inférences.
=> paramètre gerable dans l'appli pour avoir statut sur les objets. 

Lister outils mais dev doit nous faire une proposition : 
Il pourrait être possible d’envisager de travailler avec un composant de logiciel libre de dessin 3D. [Sweethome 3D](https://www.sweethome3d.com/fr/) : opensource pour penser espace. 

Demander à sweethome 3D a nous faire une extension? 
On ne veut pas un logiciel local, on veut du web pour ne pas être limités sur les distributions pour les OS.


Interface : réduire niveau de précision. Dire où est l'ouverture sans dire nécessairement quelle forme elle a. Penser en termes d’épures plutôt qu’en terme réalistes.

Légendes: bloc avec couleur, usage fonctionnel qui sert de repères de construction. Afficher les éléments d’identification des œuvres dans les visualisations. Ce qui n’est pas contradictoire avec le fait d’utilisation une numérotation pour la liste.

3 persona

possibilité d'enregistrer un état

descriptions fonctionnelles et chaînes d'activités des utilisateurs
manipulations et interactions avec les listes
versionning
exports

définitions/vocabulaire

Aller de l'avant sur la question des rapports entre la visualisation et les données, décliné sur les personas, pour aller plus loin dans la description fonctionnelle. Répondre aux objectifs scientifiques tout en restant générique.

Question de comment gérer l'information? effort de traduction comptabile avec JSON. Ex: LinkedArt implémente CIDOC-CRM en JSON. Demander à David d'implémenter l'ontologie en JSON-LD. Du point de vue du dev, ce serait juste le JSON-LD avec propriétés et relations.
Base de données documents, indexation des entrées permet de parcourir les fichiers (ex: CouchDB)

Attention, il n’est peut être pas possible de réaliser des inférences avec un stockage des données en JSONLD. Il faut ingérer le fichier pour avoir les inférences.

### Les sources

Lena pose la question des sources. Se posait la question du passage de la source au travail. Est-ce que ce sont des choses que les gens vont faire manuellement. Il avait été aussi évoqué la possibilité de faire de la reconnaissance d'image pour identifier les œuvres dans la salle (exemple du MoMA).

L’idée serait tout de même que les sources soient liées à Commons ou stockées à l’extérieur. Mais au niveau de l’application se dire que l’information est sourcées. Au niveau de l’application se contenter de faire un lien vers l’exposition.

Est-ce qu’on a une interaction avec le logiciel de manière différente en fonction du type de source qu’on a : liste d’œuvre, photographie. Pour Zoë surtout une gestion de certitude. Il serait peut-être 
- liste d'œuvre: ingérer un CSV 
- plan: travail en mode visuel
- photographie: ...

Mode d'interaction entre les types de sources et le logiciel. Ne pas forcément penser la source comme un type de donnée géré par le logiciel mais plutôt penser la source pour réfléchir aux types de saisie.

Question de coordination des sources. Pas forcément efficacité, mais aussi schémas de pensée. Prendre la liste du catalogue, saisir la liste d’œuvre en citant la source. Mais avec les autres documents pouvoir identifier une partie de la salle trois. Œuvres pas présentes au catalogue, alors les ajouter.
Enjeu de coordination des sources et niveaux de preuve, validation, incohérences. --> Une fonctionnalité à discuter.

Lors du dépouillement des archives, on procède souvent document par document. Des informations à noter au fur et à mesure. Alors l’application peut facilement répondre à des questions à partir de la documentation. Possibilité de communiquer les résultats du travail à partir des recherches documentaires.

Réfléchir à l'utilisation Common. Mais une solution standard hyperlien suffirait.
Common: documents et entités (événement type exposition)

Todo pour continuer le CDC
- approfondir la description fonctionnelle
- reprendre les enjeux qu'on a identifiés: utiliser le wireframing ou story map pour identifier les questions par exemple 

le rôle du développeur est de produire des solutions à nos enjeux 

En lien avec la todo.

Emmanuel a discuté avec Nicola Carboni

Question visuelle : 
idée de calques/zones approximatives avec opacité pour degré de certitude.

Multi-utilisateur : gestions d'accès de projets en fonction de common. Plusieurs personnes peuvent contribuer au meme projet mais modification simultanée pas possible. 