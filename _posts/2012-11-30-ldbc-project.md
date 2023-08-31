---
layout: post
title: "LDBC project"
date: "2012-11-30"
categories: 
  - "ldbc-2"
---

The mission of the LDBC can be compared to that of the Transaction Processing Council (TPC) that Jim Gray founded in the area of relational database technology ([www.tpc.org](http://www.tpc.org)). LDBC will create a body in which vendors of RDF and graph database systems agree on relevant benchmarks and benchmark practices; and will publish official benchmark results. The objective of the project is to highlight the functional and performance characteristics of Graph and RDF systems, viz-a-viz each other and established relational data management technology. The motivation for this is to help IT practitioners understand and select Graph and RDF data management products, and thus, help make the emerging Graph and RDF data management industry more mature. Additionally, we hope that LDBC will spur competition and thereby accelerate technical progress.

In detail:

- “agreeing on benchmark practices” means agreeing on the exact rules and metrics with which products can be compared. Without such rules, which include having benchmark results checked by independent auditors, it is very easy to skew any benchmark result in one’s favor; e.g. by precomputing (partial) answers; by implementing benchmark-special functionalities, by being not open about hot or cold runs; by comparing results on wholly different hardware (with wholly different price-tags). There are many ways in which one can game a result.
- “agreeing on metrics” is important as, without balanced metrics, it is easy to pick the benchmark observations or statistics that favor one algorithm/system/product (conveniently forgetting about other metrics relevant for the benchmark on which the performance maybe favorable — often systems must make trade-offs, so a win on one metric can become a loss on another; see e.g. the difference between OLTP and OLAP workloads). This will include a notion of score-per-EURO (or $), taking into account hardware+software+maintenance cost aspects in the results.

These points underline the industrial nature of the project, since such elements are not usually present in academic benchmark work. The industry participation in LDBC include Ontotext, Openlink and Neo Technologies (neo4j), which are European industrial leaders in this emerging technological space. The council itself is international, so other companies will be able to join the non-profit body of LDBC as well. More than ten such companies have approached LDBC already: effectively the great majority of RDF and Graph database companies are interested. We expect the council to start growing by March 2013, when a non-profit legal entity for it will have been formed; and membership will become formally possible.

The LDBC EU project has also a research participation in the form of UPC Barcelona, VUA Amsterdam, Technical University Munich, FORTH and STI Innsbruck. The research task is to kick-start the LDBC by helping in selecting/defining an initial set of benchmarks. Even though in RDF and graph databases there already exist benchmarks, aspects like cost metrics, rules for running the benchmark, and benchmark audits are generally underdeveloped; so LDBC here will extend existing benchmark components were possible and create new ones where necessary. The academic partners have been selected to include groups that have technical expertise in data management (e.g. RDF-3X -- Munich; MonetDB, VectorWise - Amsterdam, Sparsity - Barcelona) so benchmarks will stress systems in relevant areas "where it hurts" in order to maximize the potential for progress.

In order to ensure that benchmarks represent usage scenarios that matter for technology users, LDBC has a Technical User Community (TUC). This TUC had its first meeting last week November 19/20 in Barcelona, that was well attended and quite productive. A digital record is found on: ldbc.eu:8090/display/TUC/First+TUC+meeting+Nov+2012

We see it as a sign of relevance for LDBC that these users spent two days to talk in-depth about their technical challenges with Graph and RDF software, multiple of them flying in from the US (on their own cost). The TUC includes participants from the publishing, life sciences, security and marketing domains. The outcomes of the first TUC meeting have been used to determine the direction in establishing the first LDBC benchmark task forces; and the TUC will remain continuously involved in providing information on relevant datasets and workloads, and feedback to benchmark specifications as they evolve.

In case this description got you interested, and specifically if you are a user of RDF, graph or relational technology, we would like to invite you take a short survey: [http://goo.gl/PwGtK](http://goo.gl/PwGtK)

More about the project, its activities and its benchmarks in the future are found on: [www.ldbc.eu](http://www.ldbc.eu). We are also on twitter @LDBCproject.  
You can contact me via: larri "at" ac.upc.edu

Yours,  
Josep Lluis Larriba Pey  
LDBC coordinator

## Tags: 

- [LDBC](http://www.ldbc.eu/tags/ldbc)
- [benchmarks](http://www.ldbc.eu/tags/benchmarks)
