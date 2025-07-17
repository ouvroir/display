---

title: "Réunion Tractr"
description: "Compte-rendu de la réunion hebdomadaire du 12 juin 2025"
author: ouvroir
date: 2025-06-12
draft: false
tags:

   - cr 

---

Continuer la préparation du cablage avec l’API, sait que déjà eu un point technique.
Bases solides sur le vue liste.

Moins de temps que prévu car audit RSDE du Gouvernement. Pas contrôlés depuis 12 ans. Financier et technique.

Glenn a toutefois pu mettre une 30aine d’heures sur le projet.

Qu’est-ce qui a été fait ?
Une bonne première base de la vue liste pour gérer les spaces, exihibits, etc.
Centrage de la caméra.

Olivier peu de temps passé de son côté. Quelques réunions internes.

15h sur vue tabulaire.
194 sur 390h pour le projet total. Reste 200h. Sachant que le début pas que du Dev. Il faudra faire attention à ne pas se perdre. Pas d’alerte particulières à dates.


Présentation de la vue tableur
Suivi le style des tableurs pour disposer d’informations condencées et visibles.
Spaces et exhibits, possibilités de filtres.
Colonnes avec les espaces renseignés dans la scène. Certains champs sont modifiables in line. Pas les IRI et les types (@quest oui mais où). Peut choisir dans la liste des espaces les espaces parents. Pourra améliorer des règles métiers ici (actuellement liste complète). Peut actuellement choisir plusieurs. Idem pour les enfants. 

@quest colones interchangeables, choix des colonnes configurables. 

L’interface sera revue pour prendre moins de place. pour le détail sur les espaces.

Indicateur si déjà dessiné sur la scène. Modification possible des paramètres.

L’idée est d’avoir des modules universels qui puissent être repris à travers l’interface.

Peut être des actions à avoir pour redessiner, qui ramènent sur la scène, etc. Vue qui servirait plutôt à des détails. 

Élévation pour le tri car pense que information lisible.
Petit œil pour réordonner les colonnes et choisir celles qui s’affichent.

Dans la version finale, pourra avoir un choix par défaut visible par l’utilisateur. Comme sait que plus tard plus de colonnes.

Un champ de filtres (ni encore joli ni fonctionnel). Mais permettrait ajouter filtres ET pour réadapter le contenu de la liste.

Benchmark fait pour ce genre de solutions. Seulement ET pour le moment. Pourrait plus tard ajouter OU ou SAUF. 

@quest a-t-on besoin de ET/OU

Souhaitent aussi ajouter recherche dans la liste.

Pour le moment pas encore de passerelle depuis la vue source aux contenus. À faire, lien entre les deux.

@quest sur le traitement des listes d’œuvres. Actuellement pas de croisement. Avoir listes liées à des documents.
Listes œuvres sources différentes. --> ajouter colonne suplémentaire. Rendre saisie facile autocomplétion.

@todo Attendre Zoë pour discuter des versions

Création simplifiée où créée juste un label pour éviter d’avoir plein de champ. Label pas forcément obligatoire. 

David les label, pas dans les données structurées en tant que telles.

quid modification des ID, pas iri en entier.
Possibilité de changer la fin de l’IRI. Implique vérifier unicité de l’URI.

Sources qui pourraient ne pas avoir de fichier.

--> dans zotero on localise comment le lieu de conservation de la source ?
Dans Zotero quand c’est une archive/ms tu peux mettre une cote. Pour le livres aussi dailleurs. 


@to
métadonnées de base pour les sources

- titre/libellé (dc:title)
- description (dc:description)
- source/lieu de conservation (dc:source)
- cote (dc:source???)
- date (dc:date)
- statut
- commentaire/observation

Statuts : 

- lu/pas lu/ traité/à traiter
- todo / à faire, in progress / en cours, to review / à revoir, done / fait

Caméra, ajout un focus pour voir bas de la salle, etc.
A fait un test.

vue liste
Finaliser les filtres Ou et Sauf
Ajouter search
Highlights dans les colonnes

- supabase et react