---
layout: post
title: "Linkitup: Lightweight Data Enrichment"
date: "2012-11-07"
categories: 
  - "collaboration"
  - "computer-science"
  - "large-scale"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Data2Semantics](http://www.data2semantics.org/feed/)

![](images/linkitup-logo-150dpi.png)

**Linki**tup is a [Web-based](http://en.wikipedia.org/wiki/Web_application "Web application") dashboard for enrichment of research output published via the Figshare.com repository service. For license terms, see below.

**Linki**tup currently does two things:

- it takes metadata entered through [Figshare.com](http://figshare.com) and tries to find equivalent terms, categories, persons or entities on the Linked Data cloud and several [Web 2.0](http://en.wikipedia.org/wiki/Web_2.0 "Web 2.0") services.
- it extracts references from publications in Figshare.com, and tries to find the corresponding [Digital Object Identifier](http://doi.org/ "Digital object identifier") (DOI).

**Linki**tup is developed as part of our strategy to bring technology for adding semantics to research data to actual users.

**Linki**tup currently contains five plugins:

- [Wikipedia](http://en.wikipedia.org)/[DBPedia](http://dbpedia.org) linking to tags and categories
- Linking of authors to the [DBLP](http://dbis.uni-trier.de/DBL-Browser/ "Digital Bibliography & Library Project") bibliography
- [CrossRef](http://crossref.org "CrossRef") linking of papers to DOIs through bibliographic reference extraction
- [Elsevier](http://www.elsevier.com "Elsevier") Linked Data Repository linking to tags and categories
- [ORCID](http://orcid.org) linking to authors

Using Figshare allows Data2Semantics to:

- tap into a wealth of research data already published
- provide state-of-the art data enrichment services on a prominent platform with a significant user base, and
- bring [RDF](http://en.wikipedia.org/wiki/Resource_Description_Framework "Resource Description Framework") data publishing to a mainstream platform.
- And lastly, Figshare removes the need for a Data2Semantics data repository

Linkitup feeds the enriched metadata back as links to the original article in Figshare, but also builds a RDF representation of the metadata that can be downloaded separately, or published as research output on Figshare.

We aim to extend linkitup to connect to other research repositories such as EASY and the Dataverse Network.

A live version of **Linki**tup is available at [http://linkitup.data2semantics.org](http://linkitup.data2semantics.org). Note that the software is stil in **beta**! You will need a Figshare login and some data published in Figshare to get started.

More information, including installation instructions are available from [Github](http://github.com/Data2Semantics/linkitup).

[![Enhanced by Zemanta](http://img.zemanta.com/zemified_e.png?x-id=2a29c86c-43a1-4d1c-b962-5b86055ae8a4)](http://www.zemanta.com/?px "Enhanced by Zemanta")
