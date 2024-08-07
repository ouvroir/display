<style display="none">
.flex-1 {
  flex: 1;
}
.flex-1-5 {
  flex: 1.5;
}
#udem {
  position: relative;
  bottom: 40px;
}
</style>

# Documenter les accrochages d’exposition ou de collection muséales : une approche ontologique

<!-- Documenting exhibition or museum collections hangings: an ontological approach -->

**Emmanuel Château-Dutier, David&#0160;Valentine, Zoë&#0160;Renaudie et Lena&#0160;Krause**

19 janvier 2024

<div style="display: flex">
  <div class="flex-1">
    <img src="./img/logo-ouvroir.svg">
  </div>
  <div class="flex-1">
    <img id="udem" src="./img/logo-udem.png">
  </div>
</div>

/** Notes **/

- Hi!

<!-- Cette démonstration vise à présenter une ontologie informatique développée au sein du laboratoire Ouvroir d’histoire de l’art et de muséologie numérique de l’Université de Montréal. Cette ontologie se destine à décrire de manière explicite et formelle les traits d’un accrochage ou d’une exposition (proximité et contiguïté des œuvres, vis-à-vis, etc.). Dans un contexte documentaire souvent lacunaire, ce modèle abstrait permet l’enregistrement de l’information historique concernant les accrochages grâce à une approche spatiale définissant les possibilités d’inférences topologiques entre les objets de l’espace expographique. La démonstration s’appuie sur un jeu de données décrivant l’exposition Feux pâles de Philippe Thomas (CAPC de Bordeaux, 1990) et sur l’utilisation d’un outil graphique pour la formulation de requêtes et l’exploration des données. -->

===vvvvvv===

# Plan de la présentation

1. Le projet Display
1. Approche ontologique de la topologie de l’exposition
1. Étude de cas&#0160;: *Feux pâles*
1. Entrepôt RDF et interface Web

===vvvvvv===

# Le projet Display

- **Reconstitution** d’accrochages d’exposition ou de collection muséales
- **Basée** sur de la documentation historique hétérogène et lacunaire

/** Notes **/

- D'abord, l'utilisation des outils que je vous présente s'inscrit dans le cadre du projet Display, réalisé au laboratoire L'Ouvroir d'histroire de l'art et de muséologie numériques.
- C'est un projet qui vise la reconstitution d'exposition et d'accrochages historiques, dans divers types d'environnements numériques
- Et ce, à partir d'une documentation historique de nature hétérogène (vues d’exposition, des listes de prêts, plans des salles d’exposition, des catalogues, etc.), donc une documentation qui comporte toute sorte de lacunes et d'incertitudes en lien avec les informations que l'on peut utiliser pour procéder à ces reconstitutions.

===vvvvvv===

# Modèle de documentation des accrochages

- Modèle de documentation :
    - pérennisation et interopérabilité des données sur les expositions
    - prise en charge des incertitudes liées aux sources historiques
- Ontologie informatique pour décrire les expositions ou les accrochages dans une perspective **topologique**

/** Notes **/

- Pour palier ce problème, la première phase du projet consiste à élaborer un modèle de documentation, qui se veut pérenne et interopérable
- et qui vise à prendre en charge les incertitudes liées aux sources historiques
- La solution qu'on explorons actuellement est celle d'une ontologie informatique qui vient soutenir la recherche et la collecte de l’information historique
- et qui vient permettre la description formelle des expositions dans une perspective particulière, qui est celle des relations topologiques des objets dans l'espace de l'exposition.
- que l'on peut visualiser ainsi.

# varia

la formulation des hypothèses et la génération de reconstitutions, éventuellemetn de faire usage des données dans les reconstitutions, mais aussi dans n'imoprte quel projet

- idée de la disposition spatiale des objets, dans une exposition, à l’aide d’un modèle documentaire qui permet la description des relations topologiques abstraites entre les objets
- Pourquoi abstraite? Documentation lacunaire, qui est loin de tout nous révèler sur les expositions, 

===vvvvvv===

<!-- .slide: data-background-iframe="https://ouvroir.github.io/display-ontology/" data-background-interactive class="stack" -->

/** Notes **/

- Ce que vous voyez ici, c’est une représentation visuelle de l'ontologie, donc du modèle
- Qui définit les entités et le vocabulaire que l'on peut utiliser poutr procéder à nos descriptions
- En bleu foncé, c'est notre point de départ, BOT, une petite ontologie qui sert à décrire les relations topologiques abstraites des espaces d'un bâtiment
- En bleu pâle, c'est la spécialisation de ce modèle que nous avons préparé, dans le cadre du projet, pour décrire plus spécifiquement les accrochages dans une exposition
- Et ça passe par deux entités, espace et l'expôt, et les relations topologiques entre ces expôts peuvent être décrites par ce vocabualire.
- Et ça nous donne un contexte qui se prête bien la description topologique, en permettant de décrire, par exemple, la symétrie ou la transitivité des propriétés, et d'utiliser des inférences qui viennent enrichir les données historiques

# varia

- Par exemple, l'adjacence des espaces dans un bâtiment
- Ce qu'on fait essentiellement, c'est une spécialisation de la Building Topology Ontology pour la description de la topologie des objets dans un espace expographique
- Un travail particulier a été mené sur les relations topologiques destiné à pouvoir tirer au maximum parti des inférences.

===vvvvvv===

# Mise à l’épreuve

*Feux pâles*, Philippe Thomas, CAPC de Bordeaux, 1990

/** Notes **/

- Par la suite, ce qu'on a voulu faire c'est de mettre à l'épreuve ce modèle en décrivant une exposition
- donc on a choisi Feux pâles, de Philippe Thomas, 1990. Suggestion de ma collègue Zoë, qui travaille avec moi sur ce projet
- Donc on a décrit cette exposition en vertu du modèle
- On a mis les données dans un entrepôt de données RDF
- À partir de là, on peut accéder aux données
- soit en formualant des requêtes SPARQL, ce qui n'est pas l'idéal
- Alors on peut utiliser une interface Web un peu plus conviviale et intuitive, en attendant d'apprendre SPARQL
- Et ça ressemble à ça

===vvvvvv===

<!-- .slide: data-background-iframe="http://127.0.0.1/~david/dev-web/display-vitrine/feux-pales/" data-background-interactive class="stack" -->

/** Notes **/

- chercher dans cet espace
- les expôts qui sont vis-à-vis les uns les autres
- et qui entretiennent une relation topologique quelconque
- avec des éléments structurants de l'espace
- alors j'esssaie de construire un espace, abstrait, en exploitant les relation topologiques entre les objets qui sont exposés
- et par inférence, parce que les expôts sont en relation avec les éléments structurant et parce que la propriété faces est symétrique, à ce que ces deux élgalements structrurant soitent également vis-à-vis
- et je découvre effectivement qu'ily a deux...
- alors voilà, ce sont les outils que nous pourrons utiliser bientôt dans ce projet pour soutenir la formulation d’hypothèses l’enregistrement des interprétations.

===vvvvvv===

# Références

<div class="csl-bib-body" style="line-height: 1.35; margin-left: 2em; text-indent:-2em; font-size: 1.5rem">
  <div class="csl-entry" style="margin-bottom: 0.5em;">Guillem, A., Gros, A., Reby, K., Abergel, V. et DeLuca, L. (2023). RCC8 for CIDOC CRM: Semantic Modeling of Mereological and Topological Spatial Relations in Notre-Dame de Paris. Dans A. Bikakis, R. Ferrario, S. Jean, B. Markhoff, A. Mosca et M. Nicolosi Asmundo (dir.), <em>SWODCH’23&#0160: International Workshop on Semantic Web and Ontology Design for Cultural Heritage</em>. <a href="https://hal.science/hal-04275714">https://hal.science/hal-04275714</a></div>
  <span class="Z3988" title="url_ver=Z39.88-2004&amp;ctx_ver=Z39.88-2004&amp;rfr_id=info%3Asid%2Fzotero.org%3A2&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Abook&amp;rft.genre=proceeding&amp;rft.atitle=RCC8%20for%20CIDOC%20CRM%3A%20Semantic%20Modeling%20of%20Mereological%20and%20Topological%20Spatial%20Relations%20in%20Notre-Dame%20de%20Paris&amp;rft.btitle=SWODCH%202023&amp;rft.place=Athens%2C%20Greece%2C%20November%207%2C%202023.&amp;rft.aufirst=Ana%C3%AFs&amp;rft.aulast=Guillem&amp;rft.au=Ana%C3%AFs%20Guillem&amp;rft.au=Antoine%20Gros&amp;rft.au=Kevin%20Reby&amp;rft.au=Violette%20Abergel&amp;rft.au=Livio%20DeLuca&amp;rft.au=Antonis%20Bikakis&amp;rft.au=Roberta%20Ferrario&amp;rft.au=St%C3%A9phane%20Jean&amp;rft.au=B%C3%A9atrice%20Markhoff&amp;rft.au=Alessandro%20Mosca&amp;rft.au=Marianna%20Nicolosi%20Asmundo&amp;rft.date=2023&amp;rft.language=en"></span>
  <div class="csl-entry" style="margin-bottom: 0.5em;">Rasmussen, M. H., Lefrançois, M., Schneider, G. F. et Pauwels, P. (2021a). BOT: The building topology ontology of the W3C linked building data group. <em>Semantic Web</em>, <em>12</em>(1), 143‑161. <a href="https://doi.org/10.3233/SW-200385">https://doi.org/10.3233/SW-200385</a></div>
  <span class="Z3988" title="url_ver=Z39.88-2004&amp;ctx_ver=Z39.88-2004&amp;rfr_id=info%3Asid%2Fzotero.org%3A2&amp;rft_id=info%3Adoi%2F10.3233%2FSW-200385&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Ajournal&amp;rft.genre=article&amp;rft.atitle=BOT%3A%20The%20building%20topology%20ontology%20of%20the%20W3C%20linked%20building%20data%20group&amp;rft.jtitle=Semantic%20Web&amp;rft.stitle=SW&amp;rft.volume=12&amp;rft.issue=1&amp;rft.aufirst=Mads%20Holten&amp;rft.aulast=Rasmussen&amp;rft.au=Mads%20Holten%20Rasmussen&amp;rft.au=Maxime%20Lefran%C3%A7ois&amp;rft.au=Georg%20Ferdinand%20Schneider&amp;rft.au=Pieter%20Pauwels&amp;rft.au=Krzysztof%20Janowicz&amp;rft.date=2021-01-01&amp;rft.pages=143-161&amp;rft.spage=143&amp;rft.epage=161&amp;rft.issn=22104968%2C%2015700844"></span>
  <div class="csl-entry" style="margin-bottom: 0.5em;">Rasmussen, M. H., Pauwels, P., Lefrançois, M. et Schneider, G. F. (2021b, 28 juin). Building Topology Ontology [Draft Community Group Report]. <a href="https://w3c-lbd-cg.github.io/bot/">https://w3c-lbd-cg.github.io/bot/</a></div>
  <span class="Z3988" title="url_ver=Z39.88-2004&amp;ctx_ver=Z39.88-2004&amp;rfr_id=info%3Asid%2Fzotero.org%3A2&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Adc&amp;rft.type=standard&amp;rft.title=Building%20Topology%20Ontology&amp;rft.identifier=https%3A%2F%2Fw3c-lbd-cg.github.io%2Fbot%2F&amp;rft.aufirst=Mads%20Holten&amp;rft.aulast=Rasmussen&amp;rft.au=Mads%20Holten%20Rasmussen&amp;rft.au=Pieter%20Pauwels&amp;rft.au=Maxime%20Lefran%C3%A7ois&amp;rft.au=Georg%20Ferdinand%20Schneider&amp;rft.date=2021-06-28"></span>
  <div class="csl-entry">Renaudie, Z. (2019). <em>Le monde de <em>Feux pâles</em>, l’exposition à l’épreuve de la conservation-restauration, tome I</em> [Mémoire Master II, École supérieure d’art d’Avignon]. <a href="https://www.academia.edu/40627194/Renaudie_Zo%C3%AB_Le_monde_de_Feux_p%C3%A2les_lexposition_%C3%A0_l%C3%A9preuve_de_la_conservation_restauration_TOME_I">https://www.academia.edu/40627194/Renaudie_Zoë_Le_monde_de_Feux_pâles lexposition_à_l’épreuve_de_la_conservation_restauration_TOME_I</a></div>
  <span class="Z3988" title="url_ver=Z39.88-2004&amp;ctx_ver=Z39.88-2004&amp;rfr_id=info%3Asid%2Fzotero.org%3A2&amp;rft_val_fmt=info%3Aofi%2Ffmt%3Akev%3Amtx%3Adissertation&amp;rft.title=Le%20monde%20de%20%3Cem%3EFeux%20p%C3%A2les%3C%2Fem%3E%2C%20l%26%2339%3Bexposition%20%C3%A0%20l%26%2339%3B%C3%A9preuve%20de%20la%20conservation-restauration%2C%20tome%20I&amp;rft.aufirst=Zo%C3%AB&amp;rft.aulast=Renaudie&amp;rft.au=Zo%C3%AB%20Renaudie&amp;rft.date=2019&amp;rft.language=fr"></span>
</div>