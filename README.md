# Expots, Outil pour la documentation des accrochages de collection et de visualisation 3D

## Meta
- [feuille de route](https://github.com/ouvroir/expots/milestones?direction=asc&sort=due_date&state=open)

## Description (fr)

La recherche historique portée par le premier axe du partenariat CIÉCO implique la mobilisation et l’exploitation de nombreuses sources archivistiques afin de documenter l’histoire des accrochages de collections dans les musées d’art et pouvoir procéder à leur reconstitution. Un outil permet d’accompagner l’ensemble des opérations de recherche, depuis la collecte de l’information historique, à la formulation des hypothèses et à l’enregistrement des résultats.

La solution logicielle que nous développons s’appuie sur la création d’un modèle documentaire indépendant de toute technologie de visualisation a priori, afin de garantir la pérennité et la conservation à long terme des données enregistrées et de ménager des réutilisations possibles dans différents contextes numériques. Ce modèle consiste en la production d’une ontologie informatique destinée à décrire de manière explicite et
formelle les traits d’un accrochage ou d’une exposition (identification de l’exposition, proximité et contiguïté des œuvres, vis-à-vis, etc.).
- Cette ontologie permet de faciliter l’enregistrement de l’information historique concernant les accrochages et propose des solutions pour rendre compte de l’incertitude et des lacunes documentaires. Elle sera compatible avec l’ontologie CIDOC-CRM, un modèle conceptuel de référence promu par l’organisation internationale des musées dont elle formera une extension pour couvrir le domaine spécifique des accrochages et des expositions.
- Le modèle qui aura été mis au point sera publié pour être soumis à commentaires (Request for Comments) au sein de la communauté de la documentation muséale (LinkedArt, CIDOC, RCIP).

Les fonctionnalités offertes par le modèle de données et l’application reposent sur une approche spatiale et le recours à la modélisation 3D pour faciliter la reconstitution des accrochages de collections. Le système exploite la numérisation des données pour proposer des reconstitutions calculées basées sur l’analyse des contraintes spatiales des lieux d’exposition et des informations sur les œuvres exposées (dimensions, poids, éclairage).

Cet outil réalisé par un prestataire de service externe propose une interface graphique ergonomique afin de travailler à partir du modèle documentaire exprimé sous la forme d’une ontologie OWL pour l’enregistrement de l’information historique sur les accrochages défini par le responsable du développement de l’infrastructure numérique à partir du travail des chercheurs. De prise en main aisée, il peut être utilisé par des historiens de l’art sans compétences techniques particulières. Il facilite notamment : 
- la création ou l’importation automatisée de listes d’œuvres
- l’enregistrement ou la définition de la géométrie d’un espace expographique
- la localisation des œuvres dans cet espace

Grâce au modèle documentaire mobilisé, cette information peut être qualifiée par niveau de preuve et sourcée, mais aussi partagée sous forme de données ouvertes et liées. L’outil permet de générer des visualisations tridimensionnelles à partir des informations spatiales enregistrées. Plusieurs moteurs de rendu sont implémentés pour produire des hypothèses de restitution sous la forme de table lumineuse ou d’espaces parcourables en 3D dans un navigateur web. Les développements logiciels sont libres et ouverts. Les données de l’application doivent pouvoir être sérialisées en JSON-LD, en respectant le modèle de données exprimé en OWL à des fins d’interopérabilité. Les développements permettent de générer des visualisations 3D à la volée basées sur le standard WebGL.

Pour parvenir à la conception de cet outil de recherche, on prévoit deux étapes de conception (réalisation d’un pilote en année 2, suivie d’une mise en pratique et d’une évaluation puis une deuxième itération en année 3) qui seront prolongées par une étape de dissémination associée à des recherche de financement subséquents en fonction de l’intérêt des partenaires muséaux.

## Description (en)

The historical research carried out by the first axis of the CIÉCO partnership involves the mobilization and exploitation of numerous archival sources in order to document the history of collections displays in art museums and to be able to proceed with their reconstitution. A tool is needed to support the entire research process, from the collection of historical information to the formulation of hypotheses and the recording of results.

The software solution we are developing is based on the creation of a documentary model independent of any a priori visualization technology, in order to guarantee the durability and long-term conservation of the recorded data and to allow for possible reuses in different digital contexts. This model consists in the production of a computer ontology intended to describe in an explicit and formal way the features of a collection display or an exhibition (identification of the exhibition, proximity and contiguity of the works, vis-à-vis, etc.).

This ontology facilitates the recording of historical information about hangings and proposes solutions to account for uncertainty and documentary gaps. It will be compatible with the CIDOC-CRM ontology, a conceptual reference model promoted by the International Organization of Museums, of which it will form an extension to cover the specific domain of hangings and exhibitions. The developed model will be published for comments (Request for Comments) within the museum documentation community (LinkedArt, CIDOC, CHIN).

The functionalities offered by the data model and the application are based on a spatial approach and the use of 3D modeling to facilitate the reconstruction of collection hangings. The system exploits the digitization of data to propose calculated reconstructions based on the analysis of the spatial constraints of the exhibition spaces and information on the works exhibited (dimensions, weight, lighting).

This tool, developed by an external service provider, offers an ergonomic graphical interface to work from the documentary model expressed in the form of an OWL ontology for the recording of historical information on hangings defined by the person in charge of developing the digital infrastructure based on the work of researchers. Easy to use, it can be used by art historians without any particular technical skills. It facilitates in particular :

    the creation or automated import of lists of works
    recording or defining the geometry of an exhibition space
    the location of works in this space

Thanks to the documentary model used, this information can be qualified by level of proof and sourced, but also shared in the form of open and linked data. The tool allows to generate three-dimensional visualizations from the recorded spatial information. Several rendering engines are implemented to produce restitution hypotheses in the form of light tables or 3D browsable spaces in a web browser. The software developments are free and open. The application data must be serialized in JSON-LD, respecting the data model expressed in OWL for interoperability purposes. The developments allow to generate 3D visualizations on the fly based on the WebGL standard.

To achieve the design of this research tool, two design stages are planned (realization of a pilot in year 2, followed by a practical implementation and evaluation, and a second iteration in year 3) which will be extended by a dissemination stage associated with subsequent funding research depending on the interest of museum partners.

*Expot is designed by the laboratory in the framework of the Partnership New uses of collections in art museums. Project manager: Lena Krause. Scientific director: Emmanuel Chateau-Dutier.


## Axe 1 – LA COLLECTION EXPOSÉE 

MARIE FRASER , UQAM

Cet axe étudie diachroniquement les expositions de collections depuis 1960 afin de retracer l’émergence des nouveaux usages, de les documenter et de les analyser. Il entreprend la première histoire transversale des expositions de collections et mise sur l’analyse critique de trois aspects des mises à vue : le déploiement, la circulation et la trajectoire de l’œuvre d’art. Le premier vise à interroger le format et la nature des expositions de collections et à montrer qu’il existe des conventions muséographiques (chronologiques, thématiques, nationales (Lacroix privilégiant certains types d’accrochages et de mises en séries d’œuvres (Greenberg 1986). Si les musées cherchent à redynamiser leurs collections, c’est pour les sortir des systèmes de convention et des modèles de permanence qui ont longtemps déterminé leur présentation et les arrimer aux enjeux du contemporain (Camart 2018; Fraser et Dubé-Moreau 2016-2017). Il s’agit de voir jusqu’à quel point les nouveaux usages correspondent à l’éclatement de ces modèles narratifs et temporels hérités d’une histoire de l’art occidentale canonique (Beal 2016; Champion 2011), universelle et coloniale. Le second aspect examine la circulation des collections comme modèle de renforcement et de dissémination des savoirs. Quels rôles les collections muséales ont-elles joués dans la propagation des grands récits qui ont façonné la discipline (Griener 2007; Haskell 2002) ? Le troisième aspect est inspiré d’une approche anthropologique (Appadurai 1986; Kopytoff 1986; Latour 2000; Morton 2013; Van Eck 2015). Il s’intéresse à la façon dont l’exposition des collections influence le statut, la valeur et la médiation des œuvres d’art et examine comment les nouveaux usages engagent une réflexion critique sur les collections et leur histoire. Cet axe s’accompagnera d’une réflexion sur le caractère souvent lacunaire de la documentation des expositions, et sur les problèmes historiographiques et épistémologiques qu’une telle situation entraine.
