title: **Documenting exhibition and collection displays: an ontological approach**

---

Atelier Display (fr)

auteur·rice·s : David Valentine, Zoë Renaudie, Emmanuel Château-Dutier

Slides : https://ouvroir.github.io/atelier-display/

# **Intro (10 min)**

Tour de table

Mots d’introduction

- se réjouir de la rencontre

- préparation ontologie, début proche d’un travail avec prestataire

- objectifs de la rencontre : 

- - présenter le travail réalisé
  - valider les choix de modélisation
  - échanger sur les cas d’usage

# **Partie 1 (40 minutes max)**

## Présentation du projet (Emmanuel) 10 min

La recherche historique sur les expositions suppose la mobilisation et l’exploitation d’une large documentation archivistique pour renseigner l’histoire des accrochages des collections dans les musées d’art. Si la reconstitution d’accrochages se heurte à plusieurs difficultés pratiques et méthodologiques qui tiennent notamment à la partialité de la documentation conservée et à la nécessité de composer avec des sources d’information hétérogènes (vues d’exposition, liste de prêts, plans des salles d’exposition, projets expographiques ou scénographiques), ce processus peut fortement bénéficier d’une approche numérique qui tirerait parti de la modélisation en trois dimensions.

*L’Ouvroir d’histoire de l’art et de muséologie numériques* (https://ouvoir.umontreal.ca) est une infrastructure numérique destinée à supporter le travail conduit dans le cadre du Partenariat *Des nouveaux usages des collections dans les musées d’art* (CIÉCO https://www.cieco.co). Parmi les livrables du laboratoire, celui-ci est chargé de produire un outil pour la documentation des accrochages de collections en lien avec le travail mené par Marie Fraser dans le cadre de l’axe 1 de la recherche *La collection exposée*. En mobilisant des approches numériques, notre équipe cherche à mettre au point des processus de documentation et de visualisation destinés à la fois à garantir la pérennité et la conservation d’un patrimoine documentaire sur les expositions et à utiliser cette documentation sous exploitée par les musées dans différents contextes numériques. 

Depuis les années 90, les institutions culturelles ont développé plusieurs modèles documentaires pour rendre compte de l’information muséale. Le modèle conceptuel de référence développé par le groupe de documentation de l’ICOM, le CIDOC, propose par exemple une ontologie générique, orientée événement, qui permet de décrire la vie des objets culturels. Des travaux ont également été menés au sujet de la provenance et, plus récemment, sur la documentation des expositions. Mais il n’existe jusqu’à présent pas de modèle spécialisé pour la documentation des accrochages d’exposition ou de collection.

Nous formulons l’hypothèse que l’utilisation d’un modèle documentaire exprimé sous la forme d’une ontologie informatique en OWL, indépendant de toute technologie de visualisation *a priori*, présente l’avantage de pouvoir raisonner sur les données en garantissant leur conservation à long terme tout en ménageant toutes sortes de réutilisations dans différents contextes numériques. Après avoir présenté le point de vue spatial que nous adoptons à l’égard de l’exposition, nous introduirons les éléments structurants de cette ontologie puis nous exposerons un premier cas d’usage.

→ Artefact informatique qui exprime une modélisation formelle et explicite d’une conceptualisation partagée dans une communauté d’un domaine de connaissance (Gruber 1993).

### Historique du travail

Les membres impliqués dans la production du projet viennent de divers horizons et ont des rôles variés. Le projet a suivi trois principales étapes : 

1. Déterminer ce qui existe/ce dont nous avons besoin : discussions et ateliers entre les utilisateurs de l’équipe et l’équipe DH. 
2. Concevoir l'outil : travail de l'équipe DH. 
3. Produire l'outil : développeur externe. 

#### 2021

- **Novembre - Décembre :** Amorce de la définition des besoins avec les acteurs de l’axe 1 du partenariat pour **colliger les informations retrouvées dans les archives lorsque l’on fait de la recherche sur les expositions de collections**. 

#### 2022

- **Janvier - Mars :** Étude des outils disponibles et mise à disposition d’un tableur excel.

#### 2023

- **Juillet - Août** : Début du projet avec la mise en place de l'ontologie et des discussions sur la modélisation documentaire pour la documentation des expositions. Un modèle de documentation basé sur des relations topologiques et la perspective des objets (au lieu de l'espace) est privilégié. Le prototype est testé avec l'exposition *Feux Pâles*.
- **Septembre - Octobre** : Affinement de l'ontologie, notamment avec l'alignement sur CIDOC-CRM et la définition des relations entre objets exposés. Introduction de propriétés topologiques pour modéliser les relations spatiales entre les expôts. Discussions sur les outils de visualisation et d'édition.
- **Décembre** : Avancée sur l'implémentation des modèles. La question de la gestion des points de vue multiples et des relations entre les objets est examinée. Test de visualisation avec des requêtes SPARQL et discussion sur les technologies comme WebGL pour la visualisation 3D. Discussions sur l’interface de l’outil..

#### 2024

- **Janvier - Mars** : Refinement de l'interface utilisateur et des fonctionnalités de saisie de données. Introduction d'un outil de visualisation et saisie 2D des espaces d'exposition. Discussions autour de la réintégration des graphiques pour une meilleure représentation des relations topologiques. Rédaction du cahier des charges pour l’outil.
- **Juin - Septembre** : Continuation des tests, notamment sur la façon de représenter les espaces d'exposition et les relations topologiques. Introduction de la *Building Topology Ontology* (BOT) pour structurer les relations spatiales. Des ajustements sont faits pour améliorer l'intégration avec CIDOC-CRM. Choix du prestataire pour le l’outil : Tractr. 
- **Novembre - Février :** Développement avec les prestataires du prototypage. 

#### Présentations publiques

- Journée d’étude CIECO 2023, Réflexions pour un modèle de documentation des accrochages de collection (Marie + Emmanuel + Lena)
- vitrine du CRIHN : présentation des premières expérimentations : démo de visualisation et de requêtes SPARQL
- DHNB2024 Reykjavik : présentation du projet Display
- DH2024 : présentation de l’ontologie Display

## 1. Un point de vue spatial sur l’exposition

### La 3D au service de la reconstitution

Même si nous privilégions le recours à une modélisation abstraite plutôt qu’à la modélisation 3D, ce projet adopte une perspective spatiale à l’égard de l’exposition. La connaissance historique des accrochages de collections peut bien sûr bénéficier de visualisation sous la forme de modélisations 3D. Depuis quelques années, plusieurs musées proposent des visites en réalité virtuelle ou augmentée de leurs expositions (MOCA, MoMA, etc.). Le Städel Museum présente, par exemple, une reconstitution 3D de l’accrochage d’une de ses salles historiques (http://zeitreise.staedelmuseum.de/vr-app/). Si l’intérêt de ces approches se justifie bien dans une perspective de médiation, du point de vue de la recherche de tels artefacts numériques posent de sérieux problèmes d’obsolescence technique et de conservation, mais également d’interprétation.

La production de modèles 3D pose en effet des difficultés eu égard à la documentation des incertitudes ou des processus d’établissement de la connaissance historique. Dans ce domaine, les archéologues ont développé plusieurs méthodologies et des réflexions qui peuvent s’avérer utiles concernant les enjeux de la modélisation et leur valeur de preuve, par exemple dans le domaine des anastyloses numériques.

### Du modèle documentaire à la visualisation

À l’instar de l’archéologie, l’étude des expositions peut tirer profit des logiques spatiales ou tridimensionnelles afin de formuler des hypothèses ou proposer des reconstitutions à partir d’une documentation lacunaire. Toutefois, les sources pour traiter des accrochages d’exposition d’art sont de nature sensiblement différentes de celles utilisées dans le domaine architectural et archéologique. En effet, les sources archivistiques ou visuelles occupent une place plus importante dans la reconstitution d’accrochages. Surtout, le domaine muséologique ne permet pas de convoquer des logiques constructives qui sont souvent déterminantes pour guider la reconstitution et qui justifient, pour l’essentiel, le recours à des logiciels de dessin architectural en trois dimensions.

Un outil destiné à faciliter la reconstitution d’accrochage d’expositions d’art doit accompagner l’ensemble des opérations de recherche, depuis la collecte de l’information historique, la formulation des hypothèses et la génération de reconstitutions 3D à partir de ces informations. La solution que nous explorons s’appuie sur la création d’un modèle documentaire indépendant de toute technologie de visualisation *a priori*, afin de garantir la pérennité et la conservation à long terme des données enregistrées et de ménager diverses réutilisations des données en contexte numérique comme des visualisations 3D. L’adoption d’une approche formelle avec la création d’une ontologie OWL permet d’inscrire cette démarche dans un cadre méthodologique bien fondé qui tient compte des problèmes posés par la nature de la documentation historique disponible (lacunes, incertitudes), et de viser la réutilisation des données (pérennité et interopérabilité).

### Tout ce que vous avez jamais voulu savoir sur le web sémantique (en 5 min) - (Emmanuel)

L’approche que propose le laboratoire repose sur l’utilisation des technologies du web sémantique. Il s’agit d’un ensemble de solutions techniques destinées à permettre plateforme du web pour publier et partager des données.

Là où le word wide web propose un web de documents reliés entre eux par des hyperliens, l’idée est de pouvoir partager et relier des données entre elles en partageant des identifiants. Ainsi, la publication de données ouvertes en utilisant les standards du web sémantique permet d’envisager la création d’un web de données ouvertes et liées (Linked Open Data LOD).

Dans le contexte de notre travail, il s’agit surtout de tirer partie du formalisme proposé par le web sémantique pour exprimer de manière formelle et explicite l’information topologique sur les accrochages de collections.

Le web sémantique utilise un modèle de triplet.

Le modèle RDF comme modèle de triplet

- un modèle de triplet : sujet prédicat objet
- partage des sujet et des verbe et éventuellement des objet
- identification par des IRIs
- exemple décomposé

Le semantic layer cake

- montrer les enjeux conceptuels en regard des technologies

### Ontologies (David)

- Modélisation par classe

- - L’entité principale de ce type de modélisation est la classe

  - Les classes entretiennent des relations hiérarchiques entre elles

  - Consiste à créer un ensemble de classes qui représente un domaine

  - Classe

  - - La classe représente un concept
    - Concrètement, la classe est un ensemble : elle contient des individus (ou des membres) qui partagent des caractéristiques communes
    - Ces caractéristiques sont définies par le concept que représente la classe
    - Les différentes classes d’un domaine sont organisées dans une structure hiérarchique (classe, sous-classe, sous-sous-classe, etc.)
    - Les sous-classes héritent des caractéristiques des classes supérieures : la profondeur de la hiérarchie va du générique au spécifique; l’existence d’une sous classe se justifie par le fait qu’elle possède au moins une caractéristique plus spécifique que la classe supérieure

- L’approche associative :

- - Les classes entretiennent des relations associatives entre elles, permettant de créer des liens entre les membres des classes
  - Les caractéristiques des classes sont des attributs
  - Certains attributs sont utilisés pour établir des relations d’association entre les membres des classes
  - Ces relations peuvent être définies à n’importe quel niveau de la hiérarchie, ce en fonction des descriptions nécessaires dans le contexte de modélisation
  - Donc aux relations hiérarchiques de la modélisation par classes s’ajoute tout autre type de relation jugé nécessaire par le processus de modélisation

- Les ontologies combinent une approche taxonomique (classement des individus dans une hiérarchie) avec une approche associative (définition des relations entre les membres des classes), nous permettant de créer des modèles complexes et flexibles.

Raisonnement et inférence

- S’ajoute une couche logique qui permet d’inférer (ou déduire) des informations
- Propriétés et contraintes appliquées aux propriétés

donc

- Partage de la conceptualisation : les ontologies sont des modèles auto-descriptifs qui peuvent être traités par les outils qui implémentent les standards du web sem
- Production de descriptions formelles : qui peuvent être 

L’ontologie Display : survol, puis pouvoir y revenir plus en détail.

- domaine : la topologie de l’exposition
- les classes centrales : l’espace et l’expôt
- les propriétés pour reconstituer (décrire) l’espace
- revisiter diapos DH24

### Présentation générale de l’ontologie (David) 15’

# **L’application Display (30 min)**

### Intro (2 min) Zoë

L’évolution des outils numériques pour les historiens de l’art souligne la nécessité de méthodologies simplifiées et d’interfaces intuitives. La conservation numérique des expositions repose principalement sur la modélisation 3D des espaces d’exposition ou la diffusion en ligne de documents d’archives (vues d’exposition, listes d’œuvres, plans, etc.) (Schweibenz et Scopigno 2018). Notre outil est conçu pour accompagner l’équipe de recherche dans la consultation des archives, en documentant les accrochages d’expositions. Il permet de maximiser la modélisation complexe d’une exposition basée sur des informations potentiellement incomplètes. L’objectif est d’offrir aux historiens de l’art un moyen simple de visualiser l’arrangement spatial des œuvres, que ce soit de manière schématique ou en 3D, même en l’absence de données complètes.

L'un des avantages du logiciel est qu'il permet d'organiser un travail collectif sur la documentation des expositions. L'objectif est de fournir un outil pour les assistants de recherche et les chercheurs afin de travailler sur les accrochages d'expositions. L'application est destinée à enregistrer les informations collectées, notamment dans les archives d'expositions. 

### Personnae (5 minutes) Zoë

Nous avons imaginé trois principaux types d’utilisateurs : l’auxiliaire de recherche, le chercheur principal et le commissaire d’exposition. 

L’auxiliaire de recherche utilise une base de données pour organiser et analyser des archives d’exposition, incluant des listes d’œuvres, des vues d’expositions et des plans. En rassemblant ces documents, il compile les informations sur la disposition des objets dans l’espace, malgré des sources parfois contradictoires. L’outil lui permet d’enregistrer ces données de manière rapide et d'identifier les incohérences pour produire des synthèses sous forme de visualisations ou rapports.

Le chercheur principal, quant à lui, utilise l’application pour formuler et tester des hypothèses de restitution d'expositions à partir de données lacunaires. L'outil l'aide à confronter différentes solutions d’accrochage et à visualiser les inférences, tout en isolant des espaces spécifiques pour modéliser des zones particulières.

Le commissaire d’exposition utilise l’application pour concevoir et planifier une exposition. Il peut visualiser et présenter des scénarios d’accrochage, rassembler des œuvres par thème ou salle et produire des documents préliminaires pour le travail avec les scénographes.

### Analyse des besoins (5 min) Zoë

Lorsqu’on travaille sur l’histoire d’expositions passées, il y a plusieurs défis. Les archives contiennent souvent des éléments disparates comme des plans, des photos, des listes d’œuvres, parfois même des notes manuscrites. Les informations sont rarement complètes, et vous êtes parfois amenés à formuler des hypothèses pour essayer de comprendre comment les œuvres étaient disposées dans l’espace. Ce travail prend du temps, et peut être difficile à visualiser de manière claire. C’est là que *Display* intervient. Nous avons établi quelques scénarios auxquels nous aimerions répondre. 

Recherche dans des archives d’exposition :

Un auxiliaire de recherche travaille sur une exposition au Musée d’art contemporain de Bordeaux. En utilisant Display, il saisit les informations trouvées dans les archives, telles que des listes d’œuvres et des plans. Il place les œuvres dans l’espace en fonction des documents disponibles et des vues d’exposition. Une fois son travail terminé, il peut exporter une liste d’œuvres et un rendu visuel de la salle étudiée pour les soumettre à la chercheuse principale.

Documentation lacunaire :

Une chercheuse se concentre sur une exposition d’un artiste pour laquelle peu d’informations sont disponibles. Elle utilise Display pour formuler des hypothèses d’accrochage à partir des vues d’exposition, puis les ajuste au fur et à mesure qu’elle obtient de nouvelles données. Lors d’un entretien avec l’artiste, elle complète ses hypothèses et peut tester plusieurs versions de l’accrochage. Display l’aide à naviguer dans les incertitudes et à visualiser différents scénarios.

Comparaison d’accrochages d’une œuvre dans plusieurs projets :

Un chercheur examine comment une même œuvre a été exposée dans plusieurs expositions différentes. Display lui permet de rechercher cette œuvre dans divers projets, d’exporter les informations relatives à chaque salle où elle a été exposée et de comparer les différents accrochages et interactions avec les autres œuvres.

Préparation d’une exposition :

Une commissaire d’exposition prépare l’accrochage en regroupant les œuvres selon différents critères (chronologiques, thématiques, etc.). Elle utilise Display pour organiser les œuvres dans les salles et préparer un plan initial avant de collaborer avec le scénographe. Cette dernière se sert ensuite de ces données pour créer des plans 3D détaillés. Display accompagne le processus de réflexion et facilite l’échange avec le scénographe, en fournissant les informations topographiques nécessaires.

### Objectifs (3 min) Zoë

*Display* est conçu pour vous aider à centraliser toutes ces informations dans une seule application, et surtout pour vous permettre de reconstituer ces accrochages de manière visuelle. Vous pourrez :

- Importer des listes d’œuvres directement depuis vos archives.
- Travailler sur les espaces d’exposition, même si vous ne disposez pas toujours de plans exacts ou complets.
- Localiser les œuvres dans les espaces, et visualiser comment elles étaient disposées.
- Créer des hypothèses sur la base des informations disponibles, et explorer différentes configurations possibles.

L’idée est de rendre le processus de documentation et de restitution d’une exposition plus fluide et visuel, sans qu’il soit nécessaire d’avoir des compétences techniques particulières.

### Fonctionnalités principales (5 min) Emmanuel ?

Passons maintenant aux fonctionnalités principales de l’outil et à la manière dont il va vous aider dans votre travail quotidien.

1. **Importation et gestion des œuvres** : Vous pouvez créer ou importer automatiquement des listes d’œuvres depuis vos fichiers existants. Ces œuvres sont ensuite centralisées dans *Display*, où elles sont enrichies de métadonnées que vous pouvez compléter : titres, artistes, dimensions, etc.
2. **Modélisation des espaces d’exposition** : Vous avez la possibilité de recréer les espaces d’exposition, même si vous n’avez pas tous les détails précis. *Display* vous permet de définir des espaces avec un certain degré de flexibilité. Vous pouvez, par exemple, indiquer la forme générale d’une salle et les éléments principaux (portes, vitrines, murs), même si vous n’avez pas toutes les dimensions exactes.
3. **Positionnement des œuvres** : Une fois vos espaces définis, vous pouvez commencer à placer les œuvres dans l’espace. *Display* vous aide à organiser ces œuvres de manière logique, en tenant compte de leur disposition les unes par rapport aux autres, et de leur relation avec les éléments de l’espace.
4. **Visualisation des hypothèses** : L’un des grands atouts de *Display*, c’est sa capacité à vous offrir différentes visualisations. Vous pouvez voir les œuvres sous forme de diagrammes ou de visualisations tridimensionnelles. Cela vous permet d’obtenir des représentations simplifiées de l’accrochage, qui sont particulièrement utiles pour explorer des hypothèses sur les placements d'œuvres.

### Interfaces (5 minutes) Emmanuel ? 

Bien que les musées utilisent des logiciels de gestion de collections tels que TMS et Mimsy pour lister les œuvres et créer des plans d'expositions avec des outils comme Sketchup ou Acrobat, ces systèmes ne sont pas conçus pour la recherche sur la disposition spatiale historique des œuvres. *Display* ne cherche pas à remplacer ces outils de scénographie précise, mais à fournir un moyen intuitif de documenter et de visualiser des hypothèses sur l'organisation d'expositions.

L’outil *Display* serait conçu pour faciliter la documentation et la visualisation des accrochages sans chercher à remplacer les logiciels de scénographie précise. Il pourrait s’inspirer d’applications comme le *Kitchen Planner* d’IKEA, en permettant un glisser-déposer intuitif, des suggestions d’espaces de base et des visualisations exportables, sans nécessiter des dimensions exactes dès le départ.

De plus, l’interface pourrait être influencée par *Scratch*, un environnement de codage visuel pour enfants, permettant une utilisation simplifiée avec des blocs de données modulaires. Enfin, plutôt que de viser des modélisations 3D réalistes, *Display* envisagerait d’explorer des visualisations schématiques et abstraites, adaptées aux informations souvent lacunaires disponibles pour les expositions historiques.

Après la consultation de différents prestataires pour effectuer le prototypage de cette application web, nous avons décidé de travailler avec Tractr : https://www.tractr.net/. Le travail va commencer sous peu, les budgets étant engagés depuis cette semaine. 

### Conclusion (2-3 minutes)

Pour conclure, *Display* se veut être un outil qui centralise vos données de recherche et vous permet de les exploiter visuellement. C’est un moyen simple et accessible pour vous aider à reconstituer les accrochages d’expositions, à visualiser vos hypothèses mais aussi à les sourcer, et à mieux comprendre les relations entre les œuvres et l’espace d’exposition. Vous n’avez pas besoin de compétences techniques pour utiliser cet outil, et notre équipe est là pour vous accompagner dans sa prise en main. L’objectif principal est de rendre votre travail plus fluide, plus visuel, et surtout plus facile à partager avec vos collaborateurs.

# **Partie 3**

But :

- À partir d'une documentation d'expo, on interroge l'ontologie. “Confronte” avec leur façon de décrire.
- Traduction en direct : ils décrivent, on encode.

L’ontologie Display :

- L’ontologie Display adopte une perspective spatiale basée sur une topologie abstraite. Celle-ci permet de formuler des descriptions proches de la langue naturelle en utilisant le modèle RDF et le vocabulaire défini par l’ontologie Display.

- Visualiser, modèle fondamentalement très simple

- - Des espaces et des expôts
  - Des propriétés topologiques abstraites, dite abstraites au sens où elle n’expriment pas de valeurs quantitatives

- Survol du vocabulaire avec la documentation, notamment les propriétés et leurs définitions

- - On utilise ces termes pour formuler nos descriptions de la topologie de l’exposition

- Présentation de Feux pâles et de la documentation utilisée