---
title : Notes rdv Display David et William
author: ouvroir
date: 2024-03-07
draft: false
tags:
    - display
    
---

Présents : WD, DV

**Protege** : écrit en Java, pour la **modélisation** d'ontologies. 
Définir la symétrie/transitivité des propriétés qui permettent de faire des inférences

**Moteur d'inférence** : parse l'ontologie et les données qui popule l'ontologie. Il existe des moteurs dans Protege qui permettent de valider la cohérence sémantique d'une ontologie et d'effectuer des tests sur quelques individus. Mais Protégé n'est pas conçu pour traiter des jeux de données volumineux.

Les moteurs interprètent différement OWL (implémentent selon les différents [profils OWL](https://www.w3.org/TR/owl2-profiles/), conformément ou partiellement, ou uniquement les relations de subsomption RDFS, ou seulement des propriétés spécifiques, etc.) et donc les moteurs d'inférences ne produisent pas les même résultats.

Manipulation des inférences : les moteurs peuvent être intégrés à des environnements et leurs sorties peuvent être intégrées dans un graphe vivant en mémoire pour être manipulées (comme dans Protégé, qui utilise L'API Java OWL API, ou dans les librairies comme Apache Jena, rdflib, en py ou js mais dont les développements sont complètement indépendants, ou encore EasyRDF très utilisée en PHP).

Matérialisation d'inférence : les inférences sont éventuellement dites *matérialisées* (cad enregistrées dans un dispositif de stockage permanent).

**Les triplestores** implémentent leur propres moteurs d'inférence ou des adaptations de moteurs utilisés dans des environnements de modélisation. Il y a des logiques internes à chaque moteur+triplestore. 

Turtle, sérialisation la plus lisible. Les triplestores implémentent le standard SPARQL, un protocole du W3C. Donc peu importe le format d'entrée (sérialisation avec LOAD ou requête avec INSERT, par exemple), c'est très simple de populer un store.

Les packages (ie côté client) donne la possibilité de faire des requêtes SPARQL ou de manipuiler des graphes en mémoire.

Les inférences peuvent être générées à plusieurs endroits dans un flow selon les besoins : règles côté client ou serveur, moteur d'inférence sur l'output d'une requête à un entrepôt, requête SPARQL avec CONSTRUCT, etc.

**Note** : la modélisation en OWL permet de décrire formellement la logique des inférences dans notre modèle, mais l'implémentation des mécanismes d'inférences est flexible et peut s'effectuer de plusieurs manières. Les moteurs d'inférences ont des avantages (différentes options préprogrammées selon les profils qui permettent de faire beaucoup avec le modèle), mais ont aussi des désavantages (limites, par exemple : les property chains ou certains types d'axiomes; puissance, par exemple : quantité importante de bruit dû à l'inférence de l'ensemble des relations de subsomption qui ne sont souvent pas pertinentes et qui multiplie le poids des output). En ce sens, il faut gérer ces désavantages à travers le flow, et l'idée de faire reposer ce processus que sur le modèle et un moteur n'est peut-être pas l'option qui apparait la plus judicieuse. Il est fort probable que nous devrons créer des user-defined rules avec [Fuseki](https://jena.apache.org/documentation/fuseki2/).

**Sur la question de où sont gérés les inférences**

C'est une question de temporalité fonction des besoins et des contraintes techniques.

Approche A (front + back) : Quand contacter le triplestore pour réaliser une inférence ? Est-ce qu'on le fait au moment du changement de notice/de vue ? (temporalité)

Approche B (front seul) Il y a peu de données chargées en mémoire, est-ce qu'on peut tout (population + inférence) traité côté client ? (système sans API)
=> comment gérer la potentielle perte de données ? (sauvegarde régulière = mise à jour du triplestore ~ toutes les 3min) 

Approche C (front + un tout petit peu de back) : population faite du côté client (modèle chargé en mémoire) mais inférence côté serveur

En fait ces approches traite de la même question : avec quelle abstraction travailler ?

Produire une inférence ne requiert pas nécessairement que l'on ait accès à l'ensemble des données stockées dans le triplestore. 

// Session 1 + Salle 1

objA : -> mis à jour à la cloture de la session 1
objB : faces objA


// Session 2 + salle 2

objC : prop objA
objD : prop objA
objE : prop objA

Note : le fait de déclarer objC prop objA pour avoir des incidences sur d'autres objets (ni A, ni C). Les inférences deviendront intéressantes lorsque l'on voudra connaitre, par exemple, pour un espace donné l'ensemble des relations topologiques découlant des déclarations. Aussi, scénario envisagé ou non : la personne qui saisit veut visualiser des inférences sans les rendre permanentes (sans les matérialiser) en les stockant dans un triplestore, pour des test par exemple : des tactiques d'inférence côté client pourraient être utiles.

Questions pratiques :

- est-ce qu'on mettre un triplestore en production pour expérimenter avec ? (1 serveur avec environement Java, Apache Tomcat, accès ssh, idéalement git)
    - j'ai un balbutiment d'app svelte avec formualaire et librairie pour manipuler RDF; on peut donc parser une sérilisation, manipuler, requêter sur la représentation interne (un objet JSOn), faire du JSON-ld, etc. Il suffit de se donner un jeu de données test sérialisé ou de jouer avec des données saisies.
    - cela dit, je pense que nous pouvons beaucoup préciser la production des inférences du côté serveur
- outils à tester :
    - les outils côté clients (jslond, moteur d'inférence? [côté client on se trouvera dans les eaux des règles d'inférence sur mesure ou des processeurs SHACL])
    - outils côté backend (ORM -> pas convaincu, cela me semble conçu pour des modèles relationnels); si on veut une API entre l'entrepôt et le client, il faut considérer implémenter la **spécification d'API de Linked Art**, bien documentée, full json-ld extensible pour besoins spécifiques, et conçue pour travailler avec CIDOC (qui va très bientôt se ratacher au modèle)
    - => tester pour comprendre les choses!!

