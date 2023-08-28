---
title: "Update: Machine Learning and Linked Data"
date: "2012-11-07"
categories: 
  - "collaboration"
  - "computer-science"
  - "large-scale"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Data2Semantics](http://www.data2semantics.org/feed/)

[![Mathematics](images/5748830377_bb6a9070ec_m.jpg)](http://www.flickr.com/photos/59619742@N00/5748830377)

Part of work package 2 is developing [machine learning](http://en.wikipedia.org/wiki/Machine_learning "Machine learning") techniques to automatically enrich [linked data](http://en.wikipedia.org/wiki/Linked_Data "Linked Data"). The web of data has become so large, that maintaining it by hand is no longer possible. In contrast to existing techniques for learning for the [semantic web](http://en.wikipedia.org/wiki/Semantic_Web "Semantic Web"), we aim at applying the techniques directly to the linked data.

We use kernel based machine learning techniques, which can deal well with structured data, such as [RDF](http://en.wikipedia.org/wiki/Resource_Description_Framework "Resource Description Framework") graphs. Different [graph](http://en.wikipedia.org/wiki/Graph_%28mathematics%29 "Graph (mathematics)") kernels exist, typically developed in the bioinformatics domain, thus which kernels are most suited to RDF is an unanswered question. A big advantage of the graph kernel approach is that relatively little preprocessing/feature selection of the RDF graph is necessary and graph kernels can be applied for a wide range of tasks, such as property prediction, link prediction, node clustering, node ranking, etc.

Currently our research focusses on:

- which graph kernels are best suited to RDF,
- what part of the RDF graph do we need for the graph kernel,
- which tasks are well suited to solve using kernels.

A paper with the most recent results is currently under submission at SDM 2013. Code for different graph kernels and for redoing our experiments is available at: [https://github.com/Data2Semantics/d2s-tools](https://github.com/Data2Semantics/d2s-tools).

[![Enhanced by Zemanta](http://img.zemanta.com/zemified_e.png?x-id=2bf7bb0b-ee53-4383-8359-1b8e380b783e)](http://www.zemanta.com/?px "Enhanced by Zemanta")
