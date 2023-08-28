---
title: "Explosion under inference (or not)"
date: "2011-05-15"
categories: 
  - "cloud-computing"
  - "large-scale"
  - "reasoning"
  - "semantic-web"
---

Should the semantic web be just about querying RDF? Or is it usefual (or even: feasible) to use the semantics of RDF, RDF Schema and OWL to derive additional information from the published RDF graphs? Both the feasibility and the usefulness of this depends on the amount of additional triples that are derived by inference: when almost zero, there is little point to inference, when explosively large, it might become infeasible.

LarKC researchers at [OntoText](http://www.ontotext.com/) produced an informative table showing the amount of additional triples that can be inferred from some of the most popular datasets on the Web. It’s interesting to see how the datasets differ in their semantic richness, with their ratio of explicit triples vs. inferred triples ranging from close to zero ([CIA Factbook](http://en.wikipedia.org/wiki/The_World_Factbook "The World Factbook")) to a 16-fold increase (for [DBPedia](http://dbpedia.org "DBpedia")). Please let us know if you have similar statistics for other datasets.

All of the data below taken from [FactForge](http://factforge.net/) which by itself now contains 1.5billion triples, nearly four times larger than in the beginning of the LarKC project in 2008. All of the figures below obtained with BigOWLIM 3.4, under the OWL-Horst semantics. Size is reported in billions of triples.

| Dataset | Explicit Indexed Triples | Inferred Indexed Triples | Total of Indexed Triples | Entities (nodes in the graph) | Inferred closure ratio |
| --- | --- | --- | --- | --- | --- |
| Schemata (Proton,  
SKOS, FOAF, RSS,  
DC) and ontologies  
(DBpedia, Geonames) | 15 | 9 | 23 | 8 | 0.6 |
| DBpedia (SKOS  
categories) | 2,915 | 47,837 | 50,751 | 1,135 | 16.4 |
| NY Times | 574 | 328 | 902 | 185 | 0.6 |
| UMBEL | 4,638 | 6,936 | 11,575 | 1,190 | 1.5 |
| Lingvoj | 20 | 182 | 201 | 18 | 9.2 |
| CIA Factbook | 76 | 4 | 80 | 24 | 0.1 |
| WordNet | 1,943 | 6,067 | 8,010 | 842 | 3.1 |
| Geonames | 142,011 | 194,191 | 336,202 | 42,738 | 1.4 |
| DBpedia core | 825,162 | 166,740 | 991,902 | 125,803 | 0.2 |
| Freebase | 494,344 | 52,411 | 546,754 | 123,511 | 0.1 |
| MusicBrainz | 45,492 | 36,572 | 82,064 | 15,585 | 0.8 |

###### Related articles

- [BigOWLIM - OWL Semantic Repository](http://www.ontotext.com/owlim/big/) (ontotext.com)

[![Enhanced by Zemanta](http://img.zemanta.com/zemified_e.png?x-id=7b9c6928-8d5b-447b-803d-54101a31dfa8)](http://www.zemanta.com/ "Enhanced by Zemanta")
