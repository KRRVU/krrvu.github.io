---
title: "5 heuristics for writing better SPARQL queries"
date: "2013-04-03"
categories: 
  - "science-blogging"
  - "vu-university-amsterdam"
---

Source: [Think Links](http://thinklinks.wordpress.com/feed/)

In the context of the [Open PHACTS](http://www.openphacts.org) and the [Linked Data Benchmark Council](http://ldbc.eu) projects, [Antonis Loizou](http://www.few.vu.nl/~alu900/) and I have been looking at how to write better SPARQL queries. In the Open PHACTS project, we’ve been writing super complicated queries to integrate multiple data sources and from experience we realized that different combinations and factors can dramatically impact performance. With this experience, we decided to do something more systematic and test how different techniques we came up with mapped to database theory and worked in practice. We just submitted a paper for review on the outcome. You can find a preprint (On the Formulation of Performant SPARQL Queries) on arxiv.org at [http://arxiv.org/abs/1304.0567](http://arxiv.org/abs/1304.0567). The abstract is below. The fancy graphs are in the paper.

But if you’re just looking for ways to write better queries, here are the main rules-of-thumb that we found.

1. Minimise optional triple patterns : Reduce the number of optional triple patterns by identify-ing those triple patterns for a given query that will always be bound using dataset statistics.
2. Localise SPARQL subpatterns: Use named graphs to specify the subset of triples in a dataset that portions of a query should be evaluated against.
3. Replace connected triple patterns: Use property paths to replace connected triple patterns where the object of one triple pattern is the subject of another.
4. Reduce the effects of cartesian products: Use aggregates to reduce the size of solution sequences.
5. Specifying alternative URIs: Consider different ways of specifying alternative URIs beyond UNION.

Finally, one thing we did learn was test, test, test. The performance of the same query can vary dramatically across stores.

> Title: [On the Formulation of Performant SPARQL Queries](http://arxiv.org/abs/1304.0567)  
> Authors: Antonis Loizou and Paul Groth
> 
> The combination of the flexibility of RDF and the expressiveness of SPARQL  
> provides a powerful mechanism to model, integrate and query data. However,  
> these properties also mean that it is nontrivial to write performant SPARQL  
> queries. Indeed, it is quite easy to create queries that tax even the most optimised triple stores. Currently, application developers have little concrete guidance on how to write “good” queries. The goal of this paper is to begin to bridge this gap. It describes 5 heuristics that can be applied to create optimised queries. The heuristics are informed by formal results in the literature on the semantics and complexity of evaluating SPARQL queries, which ensures that queries following these rules can be optimised effectively by an underlying RDF store. Moreover, we empirically verify the efficacy of the heuristics using a set of openly available datasets and corresponding SPARQL queries developed by a large pharmacology data integration project. The experimental results show improvements in performance across 6 state-of-the-art RDF stores.

  
Filed under: [linked data](http://thinklinks.wordpress.com/category/linked-data/) Tagged: [heuristics](http://thinklinks.wordpress.com/tag/heuristics/), [performance](http://thinklinks.wordpress.com/tag/performance/), [sparql](http://thinklinks.wordpress.com/tag/sparql/), [triple store](http://thinklinks.wordpress.com/tag/triple-store/) [![](http://feeds.wordpress.com/1.0/comments/thinklinks.wordpress.com/499/)](http://feeds.wordpress.com/1.0/gocomments/thinklinks.wordpress.com/499/) ![](http://stats.wordpress.com/b.gif?host=thinklinks.wordpress.com&blog=5274753&post=499&subd=thinklinks&ref=&feed=1)
