---
title: "Another speed record for OWL Horst inference"
date: "2011-09-19"
categories: 
  - "cloud-computing"
  - "large-scale"
  - "reasoning"
  - "semantic-web"
---

**If you liked WebPIE, you’ll also like QueryPIE**

> WebPIE performed forward inference over up to 100 billion triples (yes, that’s 10^11). Our about-to-be-published QueryPIE can do on the fly _[backward-chaining](http://en.wikipedia.org/wiki/Backward_chaining "Backward chaining")_ inference at query-time, over a billion triples, in milliseconds, on just 8 parallel machines.

Last year, Jacopo Urbani and co-authors from the LarKC team broke the speed record for forward chaining inference over OWL-Horst.  Computing the complete closure over 100 billion of triples in a number of hours using a MapReduce/Hadoop implementation on a medium-sized cluster. The performance of WebPie \[see [conference](http://www.mendeley.com/research/owl-reasoning-webpie-calculating-closure-100-billion-triples/) and [journal](http://www.mendeley.com/c/4426400885/g/1029291/urbani-2011-webpie--a-web-scale-parallel-inference-engine-using-mapreduce/) paper\] is:

- 1 billion FactForge triples in 1.5 hours on 32 compute nodes
- 24 billion [Bio2RDF](http://bio2rdf.org/ "Bio2RDF") triples in 10 hours on 32 compute nodes
- 100 billion LUBM triples in 15 hours on 64 compute notes
- deriving anywhere between 150K-650K triples per second, depending on the dataset
- runtime growing linearly with number of triples
- speedup growing linearly the number of compute nodes

Now, a year later, we’re breaking another speed record, but this time for “_backward chaining_“: not doing all inferencing up front, but doing the inferencing “on the fly”, at query time, as and when they are needed.

Until now, backward-chaining was considered to be unfeasible on very large realistic data, since it would slow down the query response time too much. Our [paper at ISWC this year](http://www.cs.vu.nl/~frankh/postscript/ISWC11.pdf) shows it’s not all that impossible: on different real-life datasets of up to 1 billion triples, QueryPIE can do on the fly backward-chaining inference at query-time, implementing the full OWL Horst fragment with response times in millisecs on just 8 machines.

All code available at [http://few.vu.nl/~jui200/files/querypie-1.0.0.tar.gz](http://few.vu.nl/~jui200/files/querypie-1.0.0.tar.gz)

[![Enhanced by Zemanta](http://img.zemanta.com/zemified_e.png?x-id=2e403695-bc6b-484e-bb54-ec6d50429ba8)](http://www.zemanta.com/ "Enhanced by Zemanta")
