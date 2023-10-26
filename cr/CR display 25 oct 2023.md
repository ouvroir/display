---
title: CR Réunion display 
author : ouvroir
date : 2023-10-25
draft: flase
tags:
     - cr
     - display
     
---

Présents : Emmanuel, David, Zoë

## Questions posées à la dernière réunion : 
- Créer questions à poser à Sparql
- Trouver déclaration de niveau de certitude. 1 à 4 (1 étant le moins certain) : Lire ontologie sur Fuzzyness
A réfléchir. Proposition : info à mettre dans commentaires en RDF*?
- Ajouter propriétés : LaysOn; LeanOn; Between
Ajout de LiesOn. LeanOn et Between pas pour l'instant. 
- Créer notion de lot?
 Résolu par la nouvel def de display
- Définir que c'est la gauche/droite du regardeur face à l'objet. 
Dans le comment du point de vue. 
- Mettre nouvelle version sur github
En attente
- Blocage sur Artifact 
Résolu

### Réflexions sur définitions d'expôt/exhibit : 

Ca serait plus facile qu'un expôt concerne l'objet d'intérêt exposé (l'artfact, le bien culturel, l'oeuvre...) et non le reste des élements du display. Si le display est le texte composé d'éléments pour sa publicisation : l'expôt est le mot, la sceno et le texte c'est la mise en page.  

#### Chaumier, Serge. 2011. « Les écritures de l’exposition ». Hermès, La Revue 61 (3): 45‑51. https://doi.org/10.3917/herm.061.0045.

Cite: 

« unité élémentaire mise en exposition, quelles qu’en soient la nature et la forme, qu’il s’agisse d’une vraie chose, d’un original ou d’un substitut, d’une image ou d’un son. Selon la forme prise par l’exposition et sa nature, il peut s’agit d’un simple objet de musée, d’une unité écologique ou même d’une installation complexe ». 
Desvallées, A., « Cent quarante termes muséologiques ou petits glossaire de l’exposition » *in* De Bary, M.-O. et Tobelem, J-M. (dir.), *Manuel de muséographie*, Biarritz, Séguier, 1998, p. 223

« Expôt ou exponat : concept désignant tous les objets au sens large, incluant donc les matériaux visuels, sonores, tactiles ou olfactifs, **susceptibles d’être porteurs de sens** dans le cadre de l’exposition »    
Gonseth, Marc-Olivier, « L’Illusion muséale » in *La Grande illusion*, Neuchâtel, Musée d’Ethnographie, 2000.p. 157)

#### Lemay-Perreault, R. (2015). Les oeuvres d’art contemporain dans les musées de société : que nous disent-elles ? Muséologies, 7(2), 111–136. https://doi.org/10.7202/1030253ar

Cite : 

POMIAN, Krysztof. « Histoire culturelle, histoire des sémiophores ». In. RIOUX, Jean-Pierre et Jean-François SINIRELLI (dir.). Pour une histoire culturelle.Paris : Seuil, 1994, p. 83 et 88-89. 
Dans cet article, Pomian établit une classification des objets et analyse la **catégorie des sémiophores**, celle des objets porteurs de signes faisant office de langage et imposant « à ses destinataires l’attitude des spectateurs ». De cette catégorie, l’auteur fait ressortir une classe particulière de sémiophores, soit celle des expôts, qui, arrachés à leur contexte d’usage, profitent d’une mise en valeur par le biais de l’exposition. 

Jean DAVALLON emploie aussi ce terme
dans L'exposition à l'oeuvre. Paris : L'Harmattan, 1999.
[je ne trouve pas de mention de l'expôt chez Davallon, je continue de chercher. Je peux le contacter si besoin.]

#### Recherche Zoë 

Test de si on sépare sous Classe Elements : 
Exhibition IsComposedOf PhysicalElements
Display includes PhysicalElements
Exhibit SubClassOf Elements
Support SubClassOf Elements
InfoTxt SubClassOf Elements
Base SubClassOf Support
VideoDevice SubClassOf Support
AudioGuide SubClassOf 

Dans le cadre d'une video présentée sur un tube cathodique l'expôt est l'oeuvre, le tube un VideoDevice. Les deux sont des éléments du display. 
Si un musée propose dans une expo de diffuser une odeur de café comme part de l'exposition : le café est l'expôt, le diffuseur est le support. Les deux sont des éléments du display. 

#### Présentation de la visualisation de David

Petite finesse à expliquer mais c'est interessant. Assez logique. 


La modélisation proposée adopte principalement une logique spatiale. Elle définit un ensemble de classes pour la description des expositions en s’appuyant sur l’ontologie architecturale Bot. L’alignement ontologique est réalisé en spécialisant la classe bot:space par une sous-classe exhibitionSpace.

L’ontologie utilise des superproprités pour définir des relations topologiques en suivant le patron définit par Bot. 
`hasTopologicalRelationWith`, les zones ont une propriété `hasElement`

Patron pour modifier comportement de la classe, voir ce qui est partiqué par CIDOC. Emmanuel a introduit (DOPHEDA)[https://chin-rcip.github.io/collections-model/fr/a-propos]

Support et devices sont devenus des sous-classes de Element/BuldingElement. 
Display devient une sous classe de Exhibit et includes exhibit. 
On enlève les artefacts et informativeInfo de l'ontologie laissant ainsi la def à Cidoc. Branchement de Cidoc sur Exhibit. 
DisplayWall est une sous-classe de Wall mais devient Support quand est en relation avec un exhibit. 

On peut pas mettre Exhibit dans Element parce que la définition de BOT de Element n'est pas applicable : Element - Constituent of a construction entity with a characteristic technical function, form or position [[ISO-12006], 3.4.7].

Etrange de ne pas avoir d'ontologie sur la topologie. 

SupeProperty of (Chain) 
Zone containsZone o hasExhibit SubPropertyOf hasExhibit 
est une zone. 

Ontology en owl, RDF serialisé en Turtle. 

#### A faire
- Planifier avec atelier avec Marie Fraser
- Décrire le lien entre les exhibits et l’ontologie CIDOC-CRM
- Chercher dans les ontologies toplogiques, la mathématique, des réseaux. Verifier réf ajouter à la biblio par Emmanuel. 
- Choisir notre moteur d'inférence. 
- Pousser en ligne