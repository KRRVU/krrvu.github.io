---
layout: post
title: "HBase RDF Loading – Do Coprocessors Help?"
date: "2012-10-07"
categories: 
  - "science-blogging"
  - "vu-university-amsterdam"
---

Source: [Think Links](http://thinklinks.wordpress.com/feed/)

If you read this blog a bit, you’ll know I’m a fairly [big fan of RDF](http://thinklinks.wordpress.com/2011/10/22/rdf-is-great-for-mashing-up-data/) as a data format. It’s really great for easily mashing different data sources together. The common syntax gets rid of a lot of headaches before you can start querying the data and you get nice things like simple reasoning to boot.

One thing that I’ve been looking for is a nice way to store a ton of RDF data, which is

1. easy to deploy;
2. easy to query;
3. works well with scalable analysis & [reasoning techniques](http://www.few.vu.nl/~jui200/webpie.html) (e.g. stuff built using MapReduce/Hadoop);
4. oh and obviously scalable.

This past spring I was at a dagstuhl workshop where I had the chance to briefly talk to [Chris Ré](http://pages.cs.wisc.edu/~chrisre/) about the data storage environment used  by the [Hazy](http://hazy.cs.wisc.edu/hazy/) – one of the leading projects in the world on large scale statistical inference. At the time, he was fairly enthusiastic about using [HBase](http://hbase.apache.org) as a storage layer.

Based on that suggestion, I [played around with deploying HBas](https://github.com/pgroth/hbase-rdf/blob/master/docs/hbase-setup-ec2.md)e myself on Amazon. Using whirr it was pretty straightforward to deploy a pretty nice environment in a matter of hours. In addition, HBase has the nice side effect that it uses the same file system as Hadoop  (HDFS) so you can run Hadoop jobs over the data that’s stored in the database.

With that I wanted to see a) what was a good way to store a bunch of RDF in HBase and b) if the retrieval of RDF was performant. Sever Fundatureanu worked on this as his master’s thesis.

One of the novel things he looked at was using coprocessors (built in user defined functions in  hbase) to try and improve the building of indexes for RDF within the database. That is instead of running multiple hadoop load jobs you run ~one and then let the coprocessors in each worker node build the rest of the x indexes you want to improve retrieval. While it didn’t improve performance, I thought the idea was cool. I’m still interested in how much user side processing you can shove into the worker nodes within HBase. Below you’ll find an abstract and link to his full thesis.

I’m still keen on using HBase as the basis for the analysis and reasoning over RDF data. We’re continuing to look into this area. If you have some cool ideas, let us know.

[**A Scalable RDF Store Based on HBase**](http://wiki.cs.vu.nl/mp/images/a/a6/Thesis-submitted.pdf)  -

Sever Fundatureanu

> The exponential growth of the Semantic Web leads to a need for a scalable storage solution for RDF data. In this project, we design a quad store based on HBase, a NoSQL database which has proven to scale out to thousands of nodes. We adopt an Id-based schema and argue why it enables a good trade-off between loading and retrieval performance. We devise a novel bulk loading technique based on HBase coprocessors and we compare it to a traditional Map-Reduce technique. The evaluation shows that our technique does not scale as well as the traditional approach. Instead, with Map-Reduce, we achieve a loading throughput of 32152 quads/second on a cluster of 13 nodes. For retrieval, we obtain a peak throughput of 56447 quads/second.

  
Filed under: [linked data](http://thinklinks.wordpress.com/category/linked-data/) Tagged: [coprocessors](http://thinklinks.wordpress.com/tag/coprocessors/), [hbase](http://thinklinks.wordpress.com/tag/hbase/), [rdf](http://thinklinks.wordpress.com/tag/rdf/) [![](http://feeds.wordpress.com/1.0/comments/thinklinks.wordpress.com/432/)](http://feeds.wordpress.com/1.0/gocomments/thinklinks.wordpress.com/432/) ![](http://stats.wordpress.com/b.gif?host=thinklinks.wordpress.com&blog=5274753&post=432&subd=thinklinks&ref=&feed=1)
