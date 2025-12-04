title: "Réunion display"
description: 
author: ouvroir
date: 2025-09-04
draft: false
tags:

    - cr 

---

ECD, ZR, DV

ODJ

- Oeuvre en plusieurs parties
  Donner exemples à David
  Une oeuvre peut avoir plusieurs exhibit. David va peut-être devoir ajouter une petite propriété à l'API

- Question de David sur les auteurs
  Auteurs et createur à identifier. 
  Alignement d'entité ce serait super mais gros dev. 
  Pas de solution interessante a notre problème. 
  Utiliser propriété Dublin Core.
  Rendre id optionnel ?
  Avoir un referentiel ?

Champs multiple dans l'interface et Glenn fait la concetation

- Liste du Getty : donner 3/4 exemples déjà : Nom - label - traduction - iri

A nous de faire la selection. 
Regarder la liste des termes de linked art. Ils ont une liste de voca controlés obligatoire. 

A demander à Glenn rdv : 

- mettre photo dans la 3d, seront-elles visibles dans la scène ? Notamment de les voir de biais. une vignette image pour tous les exhibits (elements et display compris) si possible.

- plusieurs exhibits en rapport avec une oeuvre : doit pouvoir traiter information de l'oeuvre. doit pouvoir afficher liste d'oeuvre et liste exhibit

- pour les auteurs : il faut génerer un identifiant similaire a celui des oeuvres sauf que la fin est la concetanation de la chaine de caractere du label. Optionnellement, l'utilisateur peut le changer l'iri pour un iri de referentiel. Si possible autocompletion depuis wikidata avec API. 

- David a envoyé des listes pour les tests vendredi 4 colonnes

- Quelle est la gestion des "interfaces" dans l'outil ? Comment mettez-vous les exhibits sur les cimaises ? Existe du coté de notre API, David va vous donner des exemples. 

- export des scènes ?

- versionning
  Quand il y a deux displays a la racine on pourrait considérer qu'il n'y a pas de probleme. resoudre le versionning.
  Considéré comme un graph nommé donc pas d'alerte. 
  Utlisation des graphs nommés serait commpliqué, peut-être utilisation de plusieurs set. 

  