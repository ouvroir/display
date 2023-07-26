# Exemples d'expositions

Recherche de la documentation disponible et cas types pour les tests de modélisation



## MNBAQ

- collections en ligne: il existe des albums par exposition (sans savoir si l'album est une liste d'œuvre complètes de l'exposition : pour cet [exemple](https://collections.mnbaq.org/fr/album/816), ce sont les œuvres présentées issues de la collection)
- plans de salle: mediaGuide liste les expositions et permet de voir où elles se trouvent (quel pavillon) mais sans plus
- le musée à la maison [visites virtuelles](https://www.mnbaq.org/activites/le-musee-a-la-maison)
  - plusieurs visites "immersives" disponibles
  - outil pour mesurer les dimensions
  - vue 2D ("plan" mais généré par photogrammétrie): on peut quand même mesurer les dimensions des salles comme ça
  - on peut lire les cartels mais ils sont un peu flous. Les métadonnées sur les œuvres ne sont pas directement disponibles

## MAC

exemples de documentation expositions disponibles sur le MAC répertoire

- [Mika Rottenberg](https://macrepertoire.macm.org/evenement/mika-rottenberg/) vues de salle mais pas complètes <!--plus facile à identifier et reconstruire car Ville-Marie est un petit espace et j'y suis allée-->. Pas de liste d'œuvre ni autre

- [**La Collection : tableau inaugural**  1992-05-28 au 1994-04-03](https://macrepertoire.macm.org/evenement/la-collection-tableau-inaugural/) (identifié lors de discusison avec Marie pour préparer la [JE](https://observablehq.com/d/5bb271dcc95dc196))

  - liste d'œuvres et d'artistes
  - vues d'exposition
  - affiche, carton d'invitation
  - audioguide imprimé

  beaucoup de documentation mais cas probablement trop complexe, a une série de sous-événements (itérations de l'exposition, très variables)

- exposition virtuelle Leonard Cohen 

- [Peindre la nature avec un miroir](https://macrepertoire.macm.org/evenement/peindre-la-nature-avec-un-miroir/)

  - exposition très simple, 20 tableaux

- [L’Œil et l’esprit : Point de vue de Geneviève Cadieux sur la Collection](https://macrepertoire.macm.org/evenement/l-oeil-et-l-esprit-point-de-vue-de-genevieve-cadieux/) 

  - beaucoup d'œuvres.... 120! trop pour un prototype

-  [bleu](https://macrepertoire.macm.org/evenement/bleu/)

  - 39 œuvres
  - 11 vues d'exposition
  - pas de catalogue d'exposition (que pour les expos temporaires?)

[tests données ouvertes sur les expositions](https://observablehq.com/d/3975a22a5d9ccb85)

- pas de données qui pourraient nous servir à priori...

## MoMA

- [plan d'exposition de Herbert Bayer](https://www.moma.org/collection/works/287), objet conservé dans la collection du MoMA, identifié (vision artificielle) dans des vues d'expositions 

- [From the Collection: 1960–1969](https://www.moma.org/calendar/exhibitions/1624)

  > *This exhibition contains over 350 works. However, MoMA's collection  holds over 7,000 objects from the 1960s that span a range of mediums and departments—many more than visitors will encounter in the galleries.  Explore some of these works in [MoMA's online collection](https://www.moma.org/collection). Search the entire [decade of the 1960s](https://www.moma.org/collection/works?locale=en&utf8=✓&q=&classifications=&date_begin=1960&date_end=1969&with_images=1), or a [particular year](https://www.moma.org/collection/works?locale=en&utf8=✓&q=&classifications=&date_begin=1963&date_end=1963&with_images=1). You can also [filter by department](https://www.moma.org/collection/works?locale=en&utf8=✓&q=&classifications=6&date_begin=1963&date_end=1963&with_images=1) to focus on a specific medium.*

- [New to the Print Collection: Matisse to Bourgeois ](https://www.moma.org/calendar/exhibitions/1272)

  > This exhibition, which showcases some 80 prints and artists’ books the  Museum has acquired over the past two years, reveals how an art  collection is always a work in progress. 

le MoMA a une [API](https://api.moma.org/) (qui n'est pas encore publique) et des données ouvertes sur Github notamment. Les expositions ne documentent pas la liste des œuvres, seulement aux artistes et commissaires (humains, rôles).