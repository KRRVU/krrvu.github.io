---
title: "Update: Complexity, Learning and Semantics"
date: "2012-11-09"
categories: 
  - "collaboration"
  - "computer-science"
  - "large-scale"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Data2Semantics](http://www.data2semantics.org/feed/)

![](images/blog-post-wp1.png)Complexity metrics form the backbone of graph analysis. Centrality, [betweenness](http://en.wikipedia.org/wiki/Centrality "Centrality"), [assortativity](http://en.wikipedia.org/wiki/Assortativity "Assortativity") and scale freeness are just a handful of selections from a large and quickly growing literature. It seems that every purpose has its own notion of [complexity](http://en.wikipedia.org/wiki/Complexity "Complexity"). Can we find a way to tie these disparate notions together?

Algorithmic [statistics](http://en.wikipedia.org/wiki/Statistics "Statistics") provide an answer. It posits that any useful property that is induced from [data](http://en.wikipedia.org/wiki/Data "Data") can be used to compress it—to store it more efficiently. If I know that my network is [scale free](http://en.wikipedia.org/wiki/Scale-free_network "Scale-free network"), or that a set of points is distributed normally, that information will allow me to come up with a more efficient representation of the data. If not, the property we have learned is of no use.

This notion allows us to see [data compression](http://en.wikipedia.org/wiki/Data_compression "Data compression"), learning and [complexity analysis](http://en.wikipedia.org/wiki/Analysis_of_algorithms "Analysis of algorithms") as simply three names for the same thing. The less a dataset can be compressed, the more complex it is, the more it can be compressed the more useful our induced information is.

But we can go further than just complexity. Occam’s razor tells us that the simplest explanation is often the best. Algorithmic statistics provides us with a more precise version. If our data is the result of a [computational process](http://en.wikipedia.org/wiki/Computation "Computation"), and we have found a short description of it, then with high probability the model that allowed that compression is also a description of the process that generated our data. And that is ultimately what semantics is, a description of a generating process. Whether it’s the mental state that led to a linguistic expression, or the provenance trail that turned one form of data into another. When we talk about semantics, we are usually discussing computational processes generating data.

Practically, [algorithmic](http://en.wikipedia.org/wiki/Algorithm "Algorithm") statistics will give us a means to turn any family of network models (from frequent subgraphs to graph grammars) into a family of statistics. If the network model is powerful enough, the statistics should be able to capture any existing property of complex graphs, including scale freeness, assortativity or fractal scaling.

[![Enhanced by Zemanta](http://img.zemanta.com/zemified_e.png?x-id=337f8265-65de-4e8b-b6e7-a23e59c40432)](http://www.zemanta.com/?px "Enhanced by Zemanta")
