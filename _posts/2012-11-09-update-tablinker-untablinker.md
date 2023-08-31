---
layout: post
title: "Update: TabLinker & UnTabLinker"
date: "2012-11-09"
categories: 
  - "collaboration"
  - "computer-science"
  - "large-scale"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Data2Semantics](http://www.data2semantics.org/feed/)

[TabLinker](http://github.com/Data2Semantics/TabLinker), introduced in [an earlier post](http://www.data2semantics.org/2012/02/19/tablinker/), is a [spreadsheet](http://en.wikipedia.org/wiki/Spreadsheet "Spreadsheet") to [RDF](http://en.wikipedia.org/wiki/Resource_Description_Framework "Resource Description Framework") converter. It takes Excel/CSV [files](http://en.wikipedia.org/wiki/Computer_file "Computer file") as input, and produces enriched RDF graphs with cell contents, properties and annotations using the [DataCube](http://www.w3.org/TR/vocab-data-cube/) and [Open Annotation](http://openannotation.org) vocabularies.

TabLinker interprets spreadsheets based on hand-made markup using a small set of predefined styles (e.g. it needs to know what the header cells are). Work package 6 is currently investigating whether and how we can perform this step automatically.

**Features:**

- Raw, model-agnostic conversion from spreadsheets to RDF
- Interactive spreadsheet marking within Excel
- Automatic [annotation](http://en.wikipedia.org/wiki/Annotation "Annotation") recognition and export with [OA](http://openannotation.org)
- Round-trip conversion: revive the original spreadsheet files from the produced RDF (**UnTabLinker**)

In Data2Semantics, we have used TabLinker to publish linked socio-historical data, converting the historical Dutch censuses (1795-1971) to RDF (see slides).

Social historians are actively doing research using these datasets, producing rich annotations that correct or reinterpret data; these annotations are very useful when checking dataset quality and consistency (see model). Published RDF is ready-to-query and [visualze via SPARQL queries](http://cedar-project.nl/visualizing-sparql-query-results-on-the-census/).

![](images/Annotations.png)

[![Enhanced by Zemanta](http://img.zemanta.com/zemified_e.png?x-id=f7118236-c661-4b1e-b2fc-e4cbec2898c9)](http://www.zemanta.com/?px "Enhanced by Zemanta")
