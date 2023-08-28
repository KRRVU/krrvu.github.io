---
title: "One SPARQL end point per dataset, One end point to query them all"
date: "2011-01-07"
categories: 
  - "science-blogging"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Semantic Web world for you](http://semweb4u.wordpress.com/feed/)

[![LOD Around The Clock (LATC) logo](http://semweb4u.files.wordpress.com/2011/01/logo-latc.png?w=112&h=26 "latc")](http://latc-project.eu/)  
Althought being commonly depicted as one giant graph, the Web of Data is not a single entity that can be queried. Instead, it’s a distributed architecture made of different datasets each providing some triples (see the [LOD Cloud picture](http://richard.cyganiak.de/2007/10/lod/) and [CKAN.net](http://www.ckan.net)). Each of these data source can be queried separately, most often through an end point understanding the SPARQL query language. Looking for answers making use of information spanning over different data sets is a more challenging task as the mechanisms used internally to query one data set (database-like joins, query planning, …) do not scale easily over several data sources.

When you want to combine information from, say [DBPedia](http://dbpedia.org) and the [Semantic Web doog food](http://data.semanticweb.org/) site, the easiest and quickest workaround is to download the content of the two datasets, eventually filtering out triples you don’t need, and load the content retrieved into a single data store. This approach as some limitations: you must have a store running somewhere (that may require a significantly powerful machine to host it), the downloaded data must be updated from time to time and the data you need may not be available for downloading at the first place.

When used along with a SPARQL datalayer, eRDF offers you a solution when one of these limitation prevents you from executing your SPARQL query over several datasets. The applications runs on a low-end laptop and can query, and combine the results from, several SPARQL end points. eRDF is a novel RDF query engine making use of evolutionary computing to search for the solution. Instead of the traditional resolution mecanism, an iterative trial and error process is used to progressively find some answers to the query (more information can be found in the published papers which are listed on [erdf.nl](http://www.erdf.nl) and in this [technical report](http://semweb4u.files.wordpress.com/2011/01/erdf_technical_report.pdf)). It’s a versatile optimisation tool that can run other different kind of data layers and the SPARQL data layer offers an abstraction over a set of SPARQL end points.

Let’s suppose you want to find some persons and the capital of the country they live in:

PREFIX rdf: <http://www.w3.org/1999/02/22-rdf-syntax-ns#>
PREFIX foaf: <http://xmlns.com/foaf/0.1/>
PREFIX rdfs: <http://www.w3.org/2000/01/rdf-schema#>
PREFIX db: <http://dbpedia.org/ontology/>

SELECT DISTINCT ?person ?first ?last ?home ?capital WHERE {
	?person  rdf:type         foaf:Person.
	?person  foaf:firstName   ?first.
	?person  foaf:family\_name ?last.
	OPTIONAL {
	?person  foaf:homepage    ?home.
	}
	?person  foaf:based\_near  ?country.
	?country rdf:type         db:Country.
	?country db:capital       ?capital.
	?capital rdf:type         db:Place.
}
ORDER BY ?first

Such a query can be answered by combining data from the dog food server and dbpedia. More data sets may also contain list of people but let’s focus on researchers as a start. We’ll have to indicate to eRDF which are the end points to query, this is done with a simple csv listing:

DBpedia;http://dbpedia.org/sparql
Semantic Web Dog Food;http://data.semanticweb.org/sparql

Assuming the query is saved into a “people.sparql” file and the end points list goes into a “endpoints.csv”, the query engine is called like this:

java -cp nl.erdf.datalayer-sparql-0.1-SNAPSHOT.jar nl.erdf.main.SPARQLEngine -q people.sparql -s endpoints.csv -t 5

The query will first be scanned for its basic graph patterns, all of them will be grouped and sent to the eRDF optimiser as a set of constraints to solve. Then, eRDF will look for solutions matching as many of these constraints as possible and push back all the relevant triples found back into an RDF model. After some time (set with the parameter “t”), eRDF is stopped and Jena is used to issue the query over the model that was just populated. The answers are then displayed, along with a list of the data sources that contributed in finding them.

If you don’t know which end points are likely to contribute to the answers, you can just query all of the WOD and see what happens… ![;-)](images/icon_wink.gif)  
The package comes with a tool to fetch a list of SPARQL end points from CKAN, test them and create a configuration file. It gets called like that:

java -cp nl.erdf.datalayer-sparql-0.1-SNAPSHOT.jar nl.erdf.main.GetEndPointsFromCKAN

After a few minutes, you will get a “ckan-endpoints.csv” allowing you to run query the WoD from your laptop.

The source code along with a package including all the dependencies are available on [GitHub](https://github.com/downloads/cgueret/eRDF/eRDF.zip). Please note that this is a first public release of the tool still in snapshot state so bugs are expected to show up. If you spot some, report them and help us improve the software. Comments and suggestions are also much welcome ![:)](images/icon_smile.gif)

_  
The work on eRDF is supported by the [LOD Around-The-Clock (LATC)](http://latc-project.eu/) Support Action funded under the European Commission FP7 ICT Work Programme, within the Intelligent Information Management objective (ICT-2009.4.3)._

  
[![](http://feeds.wordpress.com/1.0/comments/semweb4u.wordpress.com/53/)](http://feeds.wordpress.com/1.0/gocomments/semweb4u.wordpress.com/53/) [![](http://feeds.wordpress.com/1.0/delicious/semweb4u.wordpress.com/53/)](http://feeds.wordpress.com/1.0/godelicious/semweb4u.wordpress.com/53/) [![](http://feeds.wordpress.com/1.0/facebook/semweb4u.wordpress.com/53/)](http://feeds.wordpress.com/1.0/gofacebook/semweb4u.wordpress.com/53/) [![](http://feeds.wordpress.com/1.0/twitter/semweb4u.wordpress.com/53/)](http://feeds.wordpress.com/1.0/gotwitter/semweb4u.wordpress.com/53/) [![](http://feeds.wordpress.com/1.0/stumble/semweb4u.wordpress.com/53/)](http://feeds.wordpress.com/1.0/gostumble/semweb4u.wordpress.com/53/) [![](http://feeds.wordpress.com/1.0/digg/semweb4u.wordpress.com/53/)](http://feeds.wordpress.com/1.0/godigg/semweb4u.wordpress.com/53/) [![](http://feeds.wordpress.com/1.0/reddit/semweb4u.wordpress.com/53/)](http://feeds.wordpress.com/1.0/goreddit/semweb4u.wordpress.com/53/) ![](http://stats.wordpress.com/b.gif?host=semweb4u.wordpress.com&blog=18410093&post=53&subd=semweb4u&ref=&feed=1)
