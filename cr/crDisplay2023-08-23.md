---
title: CR display 23 août 2023
since: 2023-08-23

---
Participants : Emmanuel, Lena, David et Zoë 
# Rencontre display

modèle documentaire qui permet de prendre en charge l'information lacunaire. Intérêt aussi pour faire des inférences et émettre des hypothèses.

Nouvelle ébauche de modèle à partir de la dernière conversation
hiérarchie d'expots, en considérant que tout ce qui fait partie d'un display est un expot. 

Typage d'expots à partir d'un vocabulaire contrôlé 


Relations topologiques (entre les expots) comme entités avec des attributs

La salle d'exposition devient plutôt secondaire car on centre sur le display, qui est ensuite dans la salle. La question qui se pose est l'ordre de visite, modélisé à l'échelle du display, propriété follows/isFollowedBy (pour donner une idée)

Perspective centrée sur les objets. Requiert une seconde perspective sur la représentation topologique / dans l'espace. Question des expositions et de l'instantiation des expositions (inspiré de RiCO)

David n'est pas très à l'aise avec la notion de display.
Emmanuel fait remarquer qu'il faut aussi évaluer la différence entre display et showroom

Séparation entre l'objet et sa place (topologie)

Experience Zoé: expot prêté à un événement, exposition lié à un lieu et une date. Photographies en lieu d'information topologique.

Questions et rmq

Typage est-ce la bonne solution ?
Approche en sous-classe permettrait de mieux documenter les attributs des expots.
Chaque sous-classe aurait un type, qui serait déclaré dans le modèle / base de connaissance. 
Réfléchir à l'idée que ce ne sont pas des classes disjointes → une surface peut instancier une œuvre?

Travailler sur les contraintes pour améliorer l'ontologie.

Comment définit-on un lieu? 

Distinction display et salle. Diplay séquence. Display au centre.
Exposition et instanciation de l’exposition cf. Record (ne devrait-on pas plutôt pour le coup adopter un modèle proche de CIDOC)

Le lieu reste toujours contraignant donc il y a toujours un ajustement → crée une déclinaison de l'exposition.

Qu'est-ce qui fait display? Le rassemblemet d'expots, selon un agencement spécifique et dans un instantiation physique? (aller cherche le livre display)

Séquence vs modèle labyrinthique : plusieurs séquences possibles en même temps. Affordances. Séquences distributives: manière dont les pièces/display communiquent les uns entre les autres → chemins possibles.

Faut-il représenter l'espace? Pourrait-il s'exprimer autrement? 
Est-ce que l'espace expographique se définit par la présence d'expots/display? Choix du négatif/positif, plein/vide : œuvres qui génère l'espace expographique, ou espace qui accueille des œuvres.

test avec l'[exposition de la collection par Geneviève Cadieux](https://macrepertoire.macm.org/evenement/l-oeil-et-l-esprit-point-de-vue-de-genevieve-cadieux/) au MAC

Première question pour trancher: 
- orienté objet ou événement? 
- comment traiter l'espace et la topologie? 
- combiner CIDOC mais avec d'autres modèle au besoin

Building Topology ontology BOT → mécanique du batiment et flux
À analyser. BIM

Test de modélisation avec Protégé 

https://linked.art/model/exhibition/

Artefact versus Artwork
--> on choisit d’adopter une approche très matérielle dans la définition de l’ontologie.

définition de la circulation dans l'espace

description de l'architecture, utiliser BOT? Est-ce qu'on doit voir s'il y en a d'autres (contacter Nicola Carboni?)