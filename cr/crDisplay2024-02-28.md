---
title : CR Display 28 fev 2024
author: ouvroir
date: 2023-02-28
draft: false
tags:
    - cr

---

La réunion a été programmée il y a deux semaines. Entre temps Zoë a été malade. Un point préparatoire a eu lieu lundi.
Retour de Josselin : intéressé

## personnas

### Personnas 1

Il s’agit de fournir un outil destiné aux auxiliaires de recherche et aux chercheurs pour travailler sur les expositions. L’application est destinée à enregistrer l’information collectée notamment dans les archives sur les expositions. 

Le plus souvent il s’agit de rechercher des informations de localisation sur les objets dans l’espace d’exposition. Type de documentations disponibles, listes d’oeuvres, vues d’expositions, plan plus ou moins précis. Recherche d'informations sur les expôts et les espaces. 

Un des atouts du logiciel est de permettre d’organiser un travail collectif sur la documentation des expositions. La base de données sert de support à l’organisation du travail des auxiliaires de recherche pour un chercheur ? 

- compiler des sources pour renseigner la position des objet dans l'espace
- travail à partir de sources documentaires et archivistiques parfois contradictoires

Beaucoup d’information, réussir à déterminer celle qui est correcte.
Traduire spatialement de l’information.

Saisie en série de l’information et utilisation de l’application pour identifier des problèmes liés aux sources.

Utilisation de la visualisation pour clarifier la compréhension de l’exposition. La visualisation peut servir à identifier de l’information contradictoire au cours du processus.

Visualisation pour valider les contradictions.

### Personna 2 : 

=> Utiliser l’application pour formuler des hypothèses de restitution à partir d’informations très lacunaires.

Ex. Marie 

- tester les hypothèses de restitutions (reconstitution)
- confronter des solutions 

Système plus heuristiques, sert à raisonner sur les informations qu’on a et avoir du feedback.

Visualisation qui pourrait permettre de proposer des hypothèses de restitutions.

Ex : Modélisation autour d'une salle seulement. ou modélisation autour d'une oeuvre dans plusieurs projets. 

### Personna 3

On cherche à concevoir une exposition. L’application est utilisée pour accompagner le dispositif de création de l’exposition.

=> Projection / conception d'un projet d'exposition

La visualisation permet de proposer des scénarios. Les commissaires ont besoin d’amener de la documentation visuelle pour parler de leur projet. Un document prélimaire au montage d’exposition.

Annotation sémantique sur le regroupement des œuvres? Permet de grouper les œuvres par idée/concepts. (Correspondrait potentiellement à la classe Display? pas tant, car c'est plus conceptuel que topologique)


## modalités de saisie de données : Saisie graphique vs Saisie formulaire

Un modèle qui mobilise de l’information topologique ce qui dans le principe doit permettre de travailler sur différentes vues du modèles.

Une saisie formulaire est plus rapide pour certaines tâches (particulièrement l'entrée de données sérielles). La visualisation graphique permet de travailler sur l’espace de manière plus intuitive et plus globale.

- Saisie ou importa des listes d’œuvres
- Saisie des listes d’espaces
- Saisies d’assertions topologiques simples : Pouvoir procéder rapidement à une saisie assertions simples : telle œuvre à côté d’une autre sans même avoir d’idées claire sur le positionnement des choses.

Pouvoir consulter les assertions contradictoires

Dans certains cas la solution du formulaire est beaucoup trop lourde. Mais lors de la consultation des documents, on a besoin de rapidement pouvoir noter des informations en renseignant la source.

Dans le système, chaque information doit être sourcée. Cela implique peut-être un traitement processuel de ces sources. Obtenir la liste des sources et pouvoir traiter toutes les informations de chaque source. Cette solution permet de ne pas avoir l’obligation de renseigner un contexte pour cette information.

Penser autrement qu'un formulaire. Ne peut-on pas penser une solution graphique de type scratch ? qui permette d’enregistrer tous les triplets ? Une solution avec raccourcis ?

Il est important de pouvoir travailler sur différentes vues.

Dans la visualisation 3D, pas besoin de tout représenter. Logiciels de modélisation 3D versus outil de composition de cuisine d’Ikea qui présente une vue partielle. Comment travailler sur des informations partielles, comment travailler sur des échelles différentes.

Tant que pas de dimensions précises, travailler sur des relations relatives. Par défaut, tous les objets sont de même taille. Puis possible de travailler sur des relations relatives entre les objets : plus grand que, plus petit que. <!-- Note Lena: par défaut, les objets sont considérés de taille équivalente, pour ensuite pouvoir appliquer l'idée d'une dimension relative "plus grand", "plus petit", et on peut grouper les tailles: le mur X est plus grand que le groupe OeuvreA + OeuvreB + OeuvreC-->


Il y a une ambiguïté sur le fait d’avoir une notion d’échelle relative. Pour nous, cela a du sens de dire qu’une œuvre est en face de l’autre. Mais comment faire si on doit placer des choses spatialement. En face ou en diagonale. Retour visuel possible qui peut permettre d’assister le travail.

Intéressant de pouvoir utiliser les inférences comme des retours visuels.

Est-il possible de nommer des inférences selon l'ontologie si on les place spatialement ? 
Exemple: on a affirmé que l'œuvre A est à côté de l'œuvre B. Si je déplace l'œuvre A dans une autre salle, l'œuvre B va suivre ?

Comment renseigner les espaces ? Avoir l’alternative de donner des informations métriques ou de simples rectangles. Distinguer visuellement les informations en fonction de leur échelle. Il est important de pouvoir renseigner la connectivité des espaces. 

exemple William : Notion (interface uniforme, fonctionnelle, penser les continuités entre les interfaces)

Besoin de pouvoir faire des A/R entre des vues différentes:
- module de saisie
- module de visualisation

Avoir des points de vue différents :
- vue par liste : toutes les œuvres, toutes les salles, toutes les sources
- vue par element: toutes les assertions liées à l'œuvre X
- vue d'ensemble : visualisation de salle

Plusieurs niveaux d'échelle. 

Module Espaces inspiré par SCRATCH? 


## articulation du modèle de données avec l’application

Pas si simple: stocker l'information pour qu'elle soit disponible dans Javascript.

Modèle de travail serait un objet json. Si objets json mis a jour en direct dans l'application = les données sont pas stockées dans bdd rdf directement. Donc potentiellement on peut pas avoir inférences directement. 

Modèle libre au dev pour l'interface? Ou est-ce qu'on traduit notre modèle en json? 
Est ce que cette traduction (expression jsonLD) serait suffisante pour travailler en 3D? 

David : Approche de la semantisation le plus proche de l'interface ou avoir un tampon entre les deux? David il faut approcher le plus la semantisation possible de l'interface. 

Les inférences pourraient être implémentées à plein d’endroit. Elles pourraient être générées seulement pour la visualisation avant d’être pérennisées.

Dynamiques entre le backend et le frontend à déterminer. On devrait avoir un niveau de contrôle important sur la manière dont le développeur va gérer les données si on veut pouvoir bénéficier du modèle côté interface.

William : 
Passer les données en json du coté application parait inevitables. 
Même entre JSON et JSONLD, regarderait si nécessaire d’être en JSONLD car ne sert à rien terme d’interface d’avoir des objets trop compliqués à manipuler.

Quels sont les outils pour faire de la manip jsonld si sont trop compliqué à utiliser? 

Lorsque l’on a une API que l’on se préoccupe des enjeux de modélisation. La problématique de sémantisation peut sans doute se faire à ce moment là.

Dans la discussion que l’on a eu jusqu’à présent, on s’est efforcé de segmenter les différents objets dans l'interfaces. Toutes ces informations vont être représentées sous forme d’objet JSON qui vont représenter une notice.

Sans doute pas au prestataire de représenter le modèle de données. Définir l’API, la spécifier et dire que le modèle de données, c’est celui-ci. 

Definisson l’api, la specifier et donner au dev le modèle de saisie. 

Bien sûr, important de penser des systèmes dynamiques pour générer directement les inférences.

Emmanuel : 
Problème de l'api : laquelle on crée pour pouvoir être fonctionnelle avec la 3D? 
On sait créer api qui crée rdf mais comment dev celle efficace pour le dev?? 

En toute logique jsonld est un objet Json. Simplement des informations spécifiques qui permettent de générer des triplets.

Par rapport a notre modèle dev devrait rajouter les dims, ... Rien n'empêche pour lui de nous dire ce dont il a besoin et qu'on le rajoute? 

Interface en webgl? 

William : 

Modèle déjà connu, une ontologie qui existe, peut produire des inférences, etc. API qui peut être sans doute plus légère. Mais possible de dire que si renvoie des informations de listes d’œuvres positionnées sur un mur, nous te renvoyons ça avec telles inférences.

Implique toujours un dialogue entre la base de données et l’interface. Grande fluidité. Besoin de pouvoir le faire en temps réel. Pouvoir réfléchir en temps réel.

David : 
Ca veut dire qu'il y a constamment des inserts au niveau de la base de données. Beaucoup de données? Ca peut être lourd. 


William : 
Possibilité d'avoir requêtes non bloquante au serveur. Insertion vs retour: le retour peut être non bloquant. 

Emmanuel : 
Bcp d'avoir des retours sans cesse. Modèle documentaire très precis, pas d'api, en direct et ensuite avoir un service web qui fait les inférences quand besoin. 

David : 
Visualisation d'inférences en direct : les inférences virtuelles gérées au niveau de l'inférence. Autre point : vérifier les données avant de les envoyer dans l'entrepot rdf. 

ECD : 
[Ruben Verborgh](https://ruben.verborgh.org/blog/2017/12/20/paradigm-shifts-for-the-decentralized-web/) : bdd document rdf 

On veut un base de données rdf dans laquelle on stocke les données et qu'on poste un fichier jasonld. 
On ne veut pas populer une base de données rdf granulairement.

David : 
Il va falloir créer beaucoup de requêtes sparql. 
Générer URI dans le process. ne se fait pas au niveau de la base de données, il faut arriver avec l'uri pour rentrer dans la base de données. 

William :
Espace que prend ce modèle?

ECD : Pas un prob : sérialise pas tous les triplets. 
Problème : récupérer les inférences. Peut être asynchrone. 

Quand est-ce qu'on fait les mises à jours du triplestore ? Est-ce qu'il n'y a pas des risques de pertes de données ? 

=> question pas assez claire pour le cahier des charges. 
faire des scenari sur les différents fonctionnements possibles. 





<!-- Lena : 
- requêtes asynchrones pour faire une sémantisation "quasi-continue" avec l'entrepôt RDF (déclencheurs exemple quitter l'entrée de données par liste X)? ou action consciente de l'utilisateur: ingérer ces nouvelles données dans la bdd
- penser un schéma du flux des données (jusqu'aux exports)
-->

## comment tirer parti du modèle de données pour la saisie



<!--Note Lena: règles de validation-->
## quel type de visualisations ? pour quoi faire ?


<!--Note Lena: visualiser les affirmations et les inférences: permet de rajouter une affirmation une fois qu'on a "bougé des œuvres" par exemple -->
## quels formats d’exports


<!--export de projet: exemple de OpenRefine-->
## versionning




<!--Note Lena: version d'une exposition (itération) vs version (hypothèse) vs version (historique de l'utilisation du logiciel)-->







## notes rdv lena zr
Faire table des matière contenus que je veux avoir : 
Quand pas sur rester flous. 

Relation entre interface et modèle de données : en discuter avec le prestataire. 

Terminer la semaine pro. 

Objectif à refaire mais en dernier. 

Le modèle documentaire est important parce que nous voulons une perenité dans la conservation des données. 

Cadre de référence : 
- Inspiration : 
faire paragraphe : il existe pas grand chose. 
Nommer avantages et inconvénients
- Scénario : 
Rendre plus court le 1er. Type de sources dans les sources. 

Description fonctionnelle
verbe : 
- Créer un compte et se connecter : 
Common
- Entrer des données : 
plusieurs façons de rentrer des données. A partir de sources. Qui permet de le faire de mainière particulière. 
- Visualiser des données : 
Listes des vues
- Versionner : 
itérations et versions
- Exporter : 
quel types d'exports. 

Générer URI lors de la saisie des données. 

Travailler avec données sémantiques faisables, enjeux techniques. 

Par où commencer? 
1ere partie : faire des formulaires pour asseoir application sur des bases
2eme partie : la saisie en visualisation. 

Mini cahier des charges pour faire un petit essai. William en dev, David en production de données ? 

David a un article et un doc technique à lire. 


Zoë : Bdd est nativement en rdf ou comment intégrer sparql à bdd ? Inférences gérées par plug in ? Est-ce que la bdd soit nativement autre chose (xml, document) mais David peut travailler à côté sur la trad de cette bdd pour renvoyer vers inférences ?

David répond : La bdd est nativement RDF, pas sparql. Sparql c'est le protocole permettant de requêter et manipuler les données RDF de l'entrepôt (j'utilise souvent le terme entrepôt RDF, = bdd RDF). Plusieurs scénarios envisageables pour les inférences probablement gérées par une dynamique client-serveur pour la consultation des inférences pendant la saisie. Selon moi, utiliser une bdd nativement autre chose (xml, document) complique les projets de gestion de données sémantiques et reduit potentiellment la puissance et la flxibilité de ces modèles, en particulier si on veut travailler avec les fameuses inférences. Les technologies semblent assez mûres pour une exploration intéressante d'une interface de saisie qui travaille nativement avec des données sémantiques.
Il semble toutefois se dégager le besoin d'un modèle de données pivot pour les sessions de travail de saisie, mais il ne devrait pas s'agir d'un modèle de données destiné à la pérennisation. Il est difficile à ce stade d'envisager les relations entre un modèle de données pivot lié aux manipulations client, le modèle de données sémantiques (ontologies, données liées, sparql) et la question des inférences, considérant qu'il existera probablement des données sémantiques pertinentes préexistantes à une session de saisie. Si ce besoin se confirme, je pense qu'il vaut la peine d'envisager un modèle pivot résolument tourné vers les données nativement sémantiques en tout cas.

Qui exporte quoi a quel moment, bonne question, car en lisant je me demande, il s'agit de export depuis une bdd RDF (données sémantiques) ou depuis une session de saisie par l'utilisateur? Ou alors un export depuis une session de saisie vers le modèle de données sémantiques?

Elle pourrait être dans un doc JSON LD : Traduction d’un modèle traductible avec json. ex : Linked art implémente Cidoc en json. demander à David de passer JSON LD. Mais pas d’inférence en direct.

C'est une piste de solution à envisager. La question des inférences demande recherche et réflexion à ce stade. Il y a d'autres pistes à mentionner dont on pourra rediscuter bientôt.

