---
title: "Display tractr
author: ouvroir
date: 2025-12-04
draft: false
tags:
    - cr 

---
Finalisation du listing, maintenant accessible. Les filtres ont été revus notamment pour les sélections. Certains champs d’édition étaient encore manquants ou non-fonctionnels.

Ajout des listes manquantes pour auteurs, œuvres abstraites et espaces.

Certains détails ont été améliorés : sélection/désélection multiples. Personnalisation des colonnes, clics droits sur header pour raccourcis d’action de colonne.

Œuvres abstraites, espaces, etc. ajout d’un compteur.

--> Sera déployé dans la journée pour tests.

Quelques changements mineurs ont été apportés à la vue scène. Les couleurs ont été revues. Ici pastels pour que cela ne soit pas trop violent mais doit choisir une couleur correcte pour chacun. Jeu de bordures en sélection.

@todiscuss Couleurs
Un truc un peu classe en noir et blanc ? 
Le pb du noir, c’est le tracé de la grille
ah oui
bi color alors ? 
On va discuter avec lui.


Pour les œuvres abstraites, jusqu’à présent seuelemnt avec un nom, ajout des champs manquants : description, date ou intervale, auteurs, classification. 

Travaille sur l'héritage des champs. Par défaut prends les champs de l'oeuvre abstraite. 
Travaille la dessus pour que ce soit clean. 

Pour la semaine pro : 
- pousser cette verison pour test
- terminer héritage oeuvre abstraite
- vue source


David soulève la question de la gestion des versions différentes d’une même exposition. Actuellement, il est possible de créer plusieurs expositions dans un même projet.
Dans un meme projet on peut gérer une nouvelle exposition. 
Mise à jour de l’API qui permet de rassembler les triplets dans des versions d’exposition.

Chaque expo est un graphe nommé, dans l'interface un groupement aussi. 
Un projet aurait plusieurs groupements ? 
Un regroupement d'expo est une oeuvre abstraite ? PAs sur, ne devrait pas etre dans l'ontologie
les expos sont des activités