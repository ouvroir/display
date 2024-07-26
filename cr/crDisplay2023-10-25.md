---
title: CR display 25 octobre 2023
author : ouvroir
date : 2023-10-25
draft: false
tags:
     - cr
     - display
     - modelling
     - "bot:Element"     
---

Présents : Emmanuel, David, Zoë

# display 

Questions posées à la dernière réunion :

- Créer questions à poser à Sparql
- Trouver déclaration de niveau de certitude. 1 à 4 (1 étant le moins certain) : Lire ontologie sur Fuzzyness
     - A réfléchir. Proposition : info à mettre dans commentaires en RDF*?
- Ajouter propriétés : LaysOn; LeanOn; Between
     - Ajout de LiesOn. LeanOn et **Between** pas pour l'instant. 
- Créer notion de lot?
     - Résolu par la nouvel def de display
- Définir que c'est la gauche/droite du regardeur face à l'objet. 
     - Dans le comment du **point de vue** 
- Mettre nouvelle version sur github
     - En attente
- Blocage sur Artifact 
     - Résolu

## Réflexions sur définitions d'expôt/exhibit : 

Ca serait plus facile qu'un expôt concerne l'objet d'intérêt exposé (l'artefact, le bien culturel, l'oeuvre...) et non le reste des éléments du display. Si le display est le texte composé d'éléments pour sa publicisation : l'expôt est le mot, la scéno et le texte c'est la mise en page.

### Chaumier, Serge. 2011. « Les écritures de l’exposition ». Hermès, La Revue 61 (3): 45‑51. https://doi.org/10.3917/herm.061.0045.

Cite: 

« unité élémentaire mise en exposition, quelles qu’en soient la nature et la forme, qu’il s’agisse d’une vraie chose, d’un original ou d’un substitut, d’une image ou d’un son. Selon la forme prise par l’exposition et sa nature, il peut s’agit d’un simple objet de musée, d’une unité écologique ou même d’une installation complexe ». 
Desvallées, A., « Cent quarante termes muséologiques ou petits glossaire de l’exposition » *in* De Bary, M.-O. et Tobelem, J-M. (dir.), *Manuel de muséographie*, Biarritz, Séguier, 1998, p. 223

« Expôt ou exponat : concept désignant tous les objets au sens large, incluant donc les matériaux visuels, sonores, tactiles ou olfactifs, **susceptibles d’être porteurs de sens** dans le cadre de l’exposition »    
Gonseth, Marc-Olivier, « L’Illusion muséale » in *La Grande illusion*, Neuchâtel, Musée d’Ethnographie, 2000.p. 157)

### Lemay-Perreault, R. (2015). Les oeuvres d’art contemporain dans les musées de société : que nous disent-elles ? Muséologies, 7(2), 111–136. https://doi.org/10.7202/1030253ar

Cite : 

POMIAN, Krysztof. « Histoire culturelle, histoire des sémiophores ». In. RIOUX, Jean-Pierre et Jean-François SINIRELLI (dir.). Pour une histoire culturelle.Paris : Seuil, 1994, p. 83 et 88-89. 
Dans cet article, Pomian établit une classification des objets et analyse la **catégorie des sémiophores**, celle des objets porteurs de signes faisant office de langage et imposant « à ses destinataires l’attitude des spectateurs ». De cette catégorie, l’auteur fait ressortir une classe particulière de sémiophores, soit celle des expôts, qui, arrachés à leur contexte d’usage, profitent d’une mise en valeur par le biais de l’exposition. 

Jean DAVALLON emploie aussi ce terme
dans L'exposition à l'oeuvre. Paris : L'Harmattan, 1999.
[je ne trouve pas de mention de l'expôt chez Davallon, je continue de chercher. Je peux le contacter si besoin.]

### Recherche Zoë 

Test de si on sépare sous Classe Elements : 
Exhibition IsComposedOf PhysicalElements
Display includes PhysicalElements
Exhibit SubClassOf Elements
Support SubClassOf Elements
InfoTxt SubClassOf Elements
Base SubClassOf Support
VideoDevice SubClassOf Support
AudioGuide SubClassOf 

Dans le cadre d'une vidéo présentée sur un tube cathodique l'expôt est l'oeuvre, le tube un VideoDevice. Les deux sont des éléments du display. 
Si un musée propose dans une expo de diffuser une odeur de café comme part de l'exposition : le café est l'expôt, le diffuseur est le support. Les deux sont des éléments du display. 

## Présentation de la visualisation de David

Petite finesse à expliquer mais c'est intéressant. Assez logique. 

### Description : Display Ontology

Cette ontologie définit un ensemble de classes et de propriétés pour la description des expositions en s’appuyant sur l’ontologie architecturale [Building Topology Ontology](https://w3c-lbd-cg.github.io/bot/) (BOT). Elle propose une perspective expographique basée sur la notion d'expôt en mobilisant principalement une logique spatiale pour mettre en relation tolopologique les objets dans l'esapce.

L’alignement ontologique est conçu de manière à permettre à la fois l'application des propriétés topologiques de BOT à la description des expositions (espaces expographiques et expôts) et l'application de propriétés topologiques de Display aux éléments du bâtiment. Cet alignement est réalisé en quatre points :

- spécialisation de `bot:Space` par une sous-classe `display:ExhibitionSpace`
- spécialisation de `bot:hasSpace` par une sous-propriété `display:hasExhibitionSpace`
- spécialisation mutuelle des éléments du bâtiment selon BOT et des éléments du bâtiment selon Display (l'un hérite des propriétés topologiquies de l'autre et vice versa) : [voir note rur la relation entre bot:Element et display:Exhibit](#sur-la-relation-entre-botelement-et-displayexhibit)
- spécialisation de `bot:Interface` pour spécifier les propriétés des relations non topologiques entre des espaces ou entre des espaces ou des éléments    

L’ontologie utilise des proprités de haut niveau, suivant un patron semblable à celui de BOT (parallèle à BOT) pour définir les relations topologiques des éléments du bâtiment. Ces propriétés sont donc définies au niveau de l'expôt à partir de super-propriétés (`display:hasTopologicalRelationWith`) permettant l'organisation hiérarchique des relations topologiques. Les divers types d'expôts (sous-classes) héritent intégralement de cette hiérarchie.

Les expôts peuvent être mis en relation avec un espace abstrait soit par la propriété `display:hasExhibit` s'ils sont des expôts, soit par la propriété `bot:hasElement` s'ils sont des éléments du bâtiment (éléments qui permettent la construction de l'espace ou qui remplissent une fonction technique dans l'exposition). Note : éléments du bâtiment, qu'ils soient définis par `bot:Element` ou `display:Element`, sont toujours des expôts.

### Remarques

#### Sur la relation entre bot:Element et display:Exhibit

Solution simple et intuitive, mais sémantiquement incohérente : `display:Exhibit subClassOf bot:Element`.

En effet, la définition de `bot:Element` n'est pas applicable à `display:Exhibit` (incompatibilité sémantique) en raison de la notion de « construction entity » :

> Element - Constituent of a construction entity with a characteristic technical function, form or position [[ISO-12006], 3.4.7].

On ne peut donc pas faire de l'expôt une spécialisation de `bot:Element`. Par contre, dans la perspective expographique de `display:`, nous voulons que `bot:Element` puisse faire partie d'un `display:Display` (donc être de type `bot:Exhibit` par subsomption et hériter des propriétés topologiques définies au niveau de l'expôt). Solution :

- création de `display:Element subClassOf display:Exhibit`
- spécialisation de `bot:Element` comme sous-classe de `display:Element`

De plus, nous voulons que `bot:Element` puisse être un expôt sans nécessairement être un élément au sens de `display:Element` :

- impossible si `display:Element subClassOf bot:Element`
- si `bot:Element subClassOf display:Element`, alors les sous-classes de `display:Element` ne peuvent être `bot:Element`, ce qui pourtant pourrait être avantageux dans certains cas

Solution : classes équivalentes, `display:Element owl:equivalentClass bot:Element` (sucre syntaxique pour sous-classes mutuelles) permettant donc les deux cas de figure avec l'héritage mutuel des propriétés (prévoir une définition de `display:Element` aussi proche que possible de `bot:Element`).

Synthèse :

Dans la perspective expographique de `display:`, `bot:Element` est considéré comme une spécialisation de l’expôt, tandis que `display:Element` est une spécialisation à la fois de `bot:Element` et de l’expôt. Toutefois, `bot:Element` peut être un expôt sans nécessairement être `display:Element`. C’est pourquoi `display:` utilise les classes équivalentes : `display:Element owl:equivalent bot:Element`, permettant leur spécialisation mutuelle et l’existence de leurs définitions respectives.
Note : nous aurions pu simplement déclarer `display:Exhibit` comme sous-classe de `bot:Element`, mais la définition de `bot:Element` ne permet pas la spécialisation de l’expôt en tant que `bot:Element`.

### Autres

Patron pour modifier comportement de la classe, voir ce qui est pratiqué par CIDOC. Emmanuel a introduit (DOPHEDA)[https://chin-rcip.github.io/collections-model/fr/a-propos]

Support et devices sont devenus des sous-classes de Element/BuldingElement.

Display devient une sous classe de Exhibit et includes exhibit.

On enlève les artefacts et informativeInfo de l'ontologie laissant ainsi ces définitions à Cidoc. Branchement de Cidoc sur Exhibit.

DisplayWall est une sous-classe de Wall mais devient Support quand est en relation avec un exhibit.

Etrange de ne pas avoir d'ontologie sur la topologie. Ok, mais GeoSPARQL propose un ensemble de relations topologiques abstraites, dont RCC8.

SubProperty of (Chain) propriété OWL importante :
`containsZone o hasExhibit SubPropertyOf hasExhibit`. Autrement dit, une zoneA, qui contient une zoneB qui a des expôts, a ces expôts. Pourra se matérialiser par inférence.

Ontology en owl, RDF sérialisé en Turtle. 

## A faire
- Planifier avec atelier avec Marie Fraser
- Décrire le lien entre les exhibits et l’ontologie CIDOC-CRM
- Chercher dans les ontologies topologiques, la mathématique, des réseaux. Vérifier réf ajoutées à la biblio par Emmanuel. 
- Choisir notre moteur d'inférence.
- Pousser en ligne l’ontologie.