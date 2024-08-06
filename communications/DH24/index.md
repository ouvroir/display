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
.reveal h3 {
  margin-top: 1em;  
  }

.reveal .logos {
  margin-top: 2em;
}
</style>


# Documenting exhibition and collection displays: an ontological approach

<!-- Documenting exhibition or museum collections hangings: an ontological approach -->

**Emmanuel Château-Dutier, David&#0160;Valentine, Zoë&#0160;Renaudie et Lena&#0160;Krause**

DH2024, 19 janvier 2024

<div class="logos" style="display: flex">
  <div class="flex-1">
    <img style="height: 2.5em" src="./img/logo-cieco-grey.svg">
  </div>
  <div class="flex-1">
    <img style="height: 2.5em" src="./img/logo-ouvroir.svg">
  </div>
  <div class="flex-1">
    <img style="height: 3em" id="udem" src="./img/logo-udem-officiel.svg">
  </div>
</div>


===vvvvvv===

![Multiple sources](./img/divers.png)

===vvvvvv===

## Context of the project

### New uses of collections in art museums

- SSHRC Partnership
- ~20 researchers, 6 canadian museums
- First axis : @todo (Marie Fraser)
- [www.cieco.co](https://www.cieco.co)

### Ouvoir d’histoire de l’art et de muséologie numériques

- Digital lab to support the research
- [ouvroir.umontreal.ca](https://ouvroir.umontreal.ca)

===vvvvvv===

## Cultural heritage documentation models

- [CIDOC-CRM](http://www.cidoc-crm.org)
- [CRMgeo](doi:[10.1007/s00799-016-0192-4](https://doi.org/10.1007/s00799-016-0192-4).): A Spatiotemporal Extension of CIDOC-CRM
- Art Tracks http://www.museumprovenance.org
- [OntoExhibit](https://complexhibit-project.github.io/OntoExhibit/index-en.html) (other presentation in this conference)
- [CRMaaa ontology](https://ontome.net/namespace/246)

===vvvvvv===

## Table of content

1. A spatial perspective on the exhibition
1. The Display Ontology
1. Pattern presentation with use case: *Feux pâles*

===>>>>>>===

# A spatial perspective on the exhibition

<!-- @todo check take -->

===vvvvvv===

## 3D for Historical Reconstruction

<iframe width="900" height="506.25" src="https://www.youtube.com/embed/XCqiSbplATU?si=tMcEuk9Lycfnties&amp;start=47" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>

Das Städel museum in 3D, Ihr Virtueller Besuch im Jahr 1878 http://zeitreise.staedelmuseum.de/vr-app/

===vvvvvv===

## From 3D to a documentation model

In our use case

- archival and visual sources are essentials
- limited constructive clues (vs archeology)

-> a spatial documentation model independant of any visualisation techniques

- data exchange and long term preservation
- various applications
- 3D visualisations

===vvvvvv===

## The Display Application

- Graphical user interface for art historian
- hypothesis and analysis
- 3D and simplified visualisation rendering

===>>>>>>===

# The Display Ontology

===vvvvvv===

## Ontological Core

A perspective on the exhibition based on:

- concept of *Exhibit*
- spatial logics (definition of abstract topological relationships)

===vvvvvv===

## The Main Conceptualization

- everything takes place in exhibition spaces
- every exhibition entity (artistic or technical) is an *Exhibit*

/** Notes **/

- And that is the conceptualization we want to share with the museology community using the semantic web tools.

===vvvvvv===

## The Exhibit Class

`display:Exhibit`

![The exhibit class instatiation](./img/ontology-00-display.png)

===vvvvvv===

## Handling Description of Space

Reusing the Building Topology Ontology

> The Building Topology Ontology (BOT) is a minimal OWL DL ontology for defining relationships between the sub-components of a building.

Specification: https://w3c-lbd-cg.github.io/bot/
Namespace: `https://w3id.org/bot#`

===vvvvvv===

## Handling Description of Space

The Building Topology Ontology (BOT)

<figure class="w75">
  <img data-src="./img/bot-zones.png" alt="Salle d'entrée de l’exposition Feux pâles.">
  <figcaption>Classes and relationships involved in Zones (Rasmussen et al., 2021)</figcaption>
</figure>

===vvvvvv===

## The `bot:` & `display:` Alignment Strategy

![Alignment](./img/ontology-02-alignment.png)

===vvvvvv===

## Handling Tolopogical Relationships

![Tolopogical Relationships](./img/ontology-03-bot-display.png)

===vvvvvv===

## Handling Tolopogical Relationships

![Tolopogical Relationships](./img/ontology-03-topology.png)

===vvvvvv===

## Linkage with CIDOC and heritage ontologies

![CIDOC](./img/ontology-041-cidoc.png)

===vvvvvv===

## Linkage with CIDOC and heritage ontologies

![CIDOC](./img/ontology-04-cidoc.png)

===>>>>>>===

<style>
  .reveal #credits {
    position: fixed;
    bottom: 0;
    color: #eee;
    left: 0;
    font-size: 14px;
  }
</style>

<!-- .slide:
data-background-image="./img/use-case-00-front.jpeg" data-background-size="auto 100%"
-->

<div id="credits">Photo. : Frédéric Delpech ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.</div>

/** Notes **/

# Use Case: *Feux pâles*

===vvvvvv===

<!-- What we might need here is the r-stack class with fragments: https://revealjs.com/layout/#stack (but it doesn't work with the need of updating textual content)-->

## Exhibits & Spaces Relationship

`rdf:type`: Instantiation syntax

![Instantiation syntax](./img/use-case-graph-00.png)

/** Notes **/

- We simply populate the `display:Exhibit` class to indicate the presence of an exhibit in the exhibition.

===vvvvvv===

<!-- .slide: data-visibility="hidden" -->

## Exhibits & Spaces Relationship

Combining the instantiation and the instance

![Instantiation combination visual notation](./img/use-case-graph-01.png)

/** Notes **/

- So from now we can combine the instantiation within a single entity, just to make things lighter.

===vvvvvv===

## Exhibits & Spaces Relationship

`display:containsExhibit`: A space contains an exhibit 

![A space contains an exhibit](./img/use-case-graph-02.png)

<!-- <div class="r-stack">
  <img class="fragment fade-out"
    data-fragment-index="0"
    src="./img/tmp-3.png" />
  <img class="fragment current-visible"
    data-fragment-index="0"
    src="./img/tmp-4.png" />
</div> -->

/** Notes **/

- And we put that work in an exhibition space.

===vvvvvv===

## Exhibits & Spaces Relationship

`display:HangingInterface`: Hanging the exhibits

![Hanging the exhibits](./img/use-case-graph-03.png)

/** Notes **/

- Using the Hanging Interface Class it can easily be stated that the CAPC work (the barcode that welcomes visitors, that we have just seen before) is hung on the entrance display wall, and is contained in the exhibition space.

===vvvvvv===

## Exhibits & Spaces Relationship

The `bot:` namespace: Describing spaces

![Describing spaces](./img/use-case-graph-04.png)

/** Notes **/

- The description of spaces uses the classes and properties of the `bot:` namespace.

===vvvvvv===

## Exhibits & Spaces Relationship

`display:hasExhibitionSpace`: Space contains space

![Space contains space](./img/use-case-graph-05.png)

/** Notes **/

- foo

===vvvvvv===

## *Feux pâles*: Préambule

<figure class="w75">
  <img data-src="./img/use-case-01-preambule.png" alt="Salle d'entrée de l’exposition Feux pâles.">
  <figcaption>Vue de l’exposition Feux pâles (1990), “Préambule”. Photo. : Frédéric Delpech  ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.</figcaption>
</figure>

/** Notes **/

- And finally the entrance area communicates with a first room via two passages.

===vvvvvv===

## Exhibits & Spaces Relationship

`display:PathwayInterface`: Circulating between spaces

![Circulating between spaces](./img/use-case-graph-06.png)

===vvvvvv===

## Exhibition Space Configuration

<div style="display: flex">
  <div class="flex-1">
    <figure>
      <img data-src="./img/plan-intersections-couloir.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="./img/use-case-graph-071.png">
  </div>
</div>

===vvvvvv===

## Exhibition Space Configuration

<div style="display: flex">
  <div class="flex-1">
    <figure>
      <img data-src="./img/plan-intersections-spaces.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="./img/use-case-graph-07.png">
  </div>
</div>

===vvvvvv===

## Exhibition Space Configuration

<div style="display: flex">
  <div class="flex-1">
    <figure>
      <img data-src="./img/plan-inventaire.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="./img/use-case-graph-08.png">
  </div>
</div>

/** Notes **/

- So where are now going to the next space!

===vvvvvv===

## *Feux pâles*: De la propriété littéraire et artistique

<figure class="w75">
  <img data-src="./img/use-case-02-parcelle.png" alt="Salle d'entrée de l’expostion Feux pâles.">
  <figcaption>
    Vue de l’exposition Feux pâles (1990), salle 10 “De la propriété littéraire et artistique”. Photo.&#0160;: Frédéric Delpech ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.
  </figcaption>
</figure>

===vvvvvv===

## Intersecting Exhibits

<div style="display: flex">
  <div class="flex-1">
    <figure>
      <img data-src="./img/plan-parcelle.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy. ©&#0160;Zoë&#0160;Renaudie.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="./img/use-case-graph-09.png">
  </div>
</div>

===vvvvvv===

## *Feux pâles*: Le cabinet d’amateur

<figure class="w75">
  <img data-src="./img/use-case-03-cabinets.png" alt="Salle d'entrée de l’expostion Feux pâles.">
  <figcaption>
    Vue de l’exposition Feux pâles (1990), salle 2 “Le Cabinet d’amateur”. Photo. : Frédéric Delpech ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.
  </figcaption>
</figure>


===vvvvvv===

## Topological Relationship Between Exhibits

`display:faces`: vis-à-vis exhibits

<div style="display: flex">
  <div class="flex-1">
    <figure>
      <img data-src="./img/use-case-03-cabinets.png" alt="Détail du plan de l’exposition Feux pâles au CAPC, galerie Foy.">
      <figcaption>
        Vue de l’exposition Feux pâles (1990), salle 2 “Le Cabinet d’amateur”. Photo. : Frédéric Delpech ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.
      </figcaption>
    </figure>
  </div>
  <div class="flex-1">
    <img src="./img/use-case-graph-10.png">
  </div>
</div>

===vvvvvv===

## Topological Relationship Between Exhibits

<figure class="w75">
  <img data-src="./img/use-case-04-inventaire.png" alt="Salle d'entrée de l’expostion Feux pâles.">
  <figcaption>
    Vue de l’exposition Feux pâles (1990), salle 1 “Inventaire du mémorable”. Photo.&#0160;: Frédéric Delpech © ©&#0160;Claire&#0160;Burrus, Paris / Jan Mot, Bruxelles.
  </figcaption>
</figure>

===vvvvvv===

## Topological Relationship Between Exhibits

`display:Display`: aggregate of exhibits

![Instantiation syntax](./img/use-case-graph-11.png)

===vvvvvv===

## Reasoning: Enhance the graph with the `OWL` semantics

![Reasoning](./img/use-case-graph-12.png)

===>>>>>>===

# Conclusion

foo

===vvvvvv===

<!-- .slide: data-background-iframe="https://ouvroir.github.io/display-ontology/" data-background-interactive class="stack" -->

===vvvvvv===

## Merci !

- Display ontology [https://ouvroir.github.io/display-ontology/](https://ouvroir.github.io/display-ontology/)
- [ouvroir.umontreal.ca](https://ouvroir.umontreal.ca)

<div class="logos" style="display: flex">
  <div class="flex-1">
    <img style="height: 1.7em" src="./img/logo-cfi.svg">
  </div>
  <div class="flex-1">
    <img style="height: 2.5em" id="udem" src="./img/logo-quebec.svg">
  </div>
  <div class="flex-1">
    <img style="height: 2.5em" id="udem" src="./img/logo-udem-officiel.svg">
  </div>
</div>
<div>
  <img style="height: 0.9em" src="./img/logo-crsh.svg">
</div>


===vvvvvv===

## Références

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