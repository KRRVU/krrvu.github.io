---
layout: post
title: "Golden Demo Hackathon I"
date: "2013-06-12"
categories: 
  - "collaboration"
  - "computer-science"
  - "large-scale"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Data2Semantics](http://www.data2semantics.org/feed/)

This june 10 and 11, the Data2Semantics team locked itself in a room in the [Amsterdam Public Library](http://maps.google.com/maps?ll=52.3758333333,4.90722222222&spn=0.01,0.01&q=52.3758333333,4.90722222222 (Openbare%20Bibliotheek%20Amsterdam)&t=h "Openbare Bibliotheek Amsterdam") to build a first version of the Data2Semantics Golden Demo: a pipeline for publishing enriched data (‘semantics’) directly from Dropbox to Figshare, integrated in the [Linkitup webservice](http://linkitup.data2semantics.org).

In two days, we built and integrated:

- A connector to Dropbox
- [Term extraction](http://en.wikipedia.org/wiki/Terminology_extraction "Terminology extraction") on Word, [Excel](http://office.microsoft.com/en-us/excel "Microsoft Excel") and [text files](http://en.wikipedia.org/wiki/Text_file "Text file")
- Provenance reconstruction from Dropbox edit history
- [Conversion](http://en.wikipedia.org/wiki/Religious_conversion "Religious conversion") from Excel files to [OpenOffice](http://openoffice.org "OpenOffice") ODS
- Cell and sheet dependency extraction from ODS [spreadsheets](http://en.wikipedia.org/wiki/Spreadsheet "Spreadsheet")
- [RDF](http://en.wikipedia.org/wiki/Resource_Description_Framework "Resource Description Framework") (turtle) representation of spreadsheets
- [Complexity analysis](http://en.wikipedia.org/wiki/Analysis_of_algorithms "Analysis of algorithms") of arbitrary RDF graphs
- Report generation for complexity analysis
- Visualization of spreadsheet dependency graphs based on d3.js

Watch the video!

[![Enhanced by Zemanta](http://img.zemanta.com/zemified_e.png?x-id=6f9bc1ab-b287-420d-83ed-9614722e233d)](http://www.zemanta.com/?px "Enhanced by Zemanta")
