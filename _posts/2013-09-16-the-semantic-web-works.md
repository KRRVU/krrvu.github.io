---
layout: post
title: "The Semantic Web works!"
date: "2013-09-16"
---

# ![protege logo](images/ProtegeLogo.gif) +![Apache Jena](images/jena-logo-small.png) + YASGUI

 

**This year we again have a nice group of students (almost 70) following the 3rd year bachelor Semantic Web course. Until this year it was quite a hassle to combine the bits and pieces to create a complete workflow starting from ontology creation (in Protégé) to having a nice SPARQL endpoint that reasons in OWL over the ontology+instances.**

Like the previous years, the instructors (Stefan Schlobach and Ronald Siebes) updated the assignment by the latest developments regarding available toolkits and software.  We were surprised that it was very easy to integrate these latest tools and are now able to do the following within 30 minutes on any machine:

\- create a simple ontology in Protégé

\- install a sparql endpoint with OWL reasoning (Jena-Fuseki)

\- import the ontology

\- connect this local endpoint with Yasgui (http://yasgui.laurensrietveld.nl)

\- do via Yasgui a federated query combining results from our local endpoint together with results from other endpoints (e.g. DBPedia)

Conclusion: it is now in reach of many people to get, without a lot of suffering, a nice Semantic Web infrastructure up-and-running, and connect it with the vast amount of external Linked-data from various endpoints.

**The Semantic Web works!**

[Here](http://krr.cs.vu.nl/wp-content/uploads/2013/09/protege-fuseki-yasgui-manual.pdf "Manual on setting up a full-fledged Semantic Web infrastructure in less than 30 minutes") you can find a manual to do this yourself and hopefully share the conclusion.
