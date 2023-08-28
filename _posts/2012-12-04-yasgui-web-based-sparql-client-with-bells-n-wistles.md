---
title: "YASGUI: Web-based SPARQL client with bells ‘n wistles"
date: "2012-12-04"
categories: 
  - "collaboration"
  - "computer-science"
  - "large-scale"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Data2Semantics](http://www.data2semantics.org/feed/)

A few months ago Laurens Rietveld was looking for a query interface from which he could easily query any other [SPARQL](http://en.wikipedia.org/wiki/SPARQL "SPARQL") endpoint.

But he couldn’t find any that fit my requirements:

- Work on all endpoints conforming to the SPARQL protocol (not just the CORS enabled ones)
- Nice / easy to use interface
- [Cross-platform](http://en.wikipedia.org/wiki/Cross-platform "Cross-platform") (preferably a [web interface](http://en.wikipedia.org/wiki/User_interface "User interface"))
- Query highlighter / [syntax checker](http://en.wikipedia.org/wiki/Grammar_checker "Grammar checker")
- Namespace prefix [autocompletion](http://en.wikipedia.org/wiki/Autocomplete "Autocomplete") (through [http://prefix.cc](http://prefix.cc))

So he decided to make his own!

Give it a try at: [http://aers.data2semantics.org/yasgui/](http://aers.data2semantics.org/yasgui/)

Future work (next year probably):

- extend it with functionality such as predicate autocompletion, and
- integration with the [mondeca ‘endpoint status’](http://labs.mondeca.com/sparqlEndpointsStatus/) catalog (instead of ckan)

Comments are appreciated (including feature ideas / bug reports).

Sources are available at [https://github.com/LaurensRietveld/yasgui](https://github.com/LaurensRietveld/yasgui)

[![Enhanced by Zemanta](http://img.zemanta.com/zemified_e.png?x-id=c99dc39e-ceff-4d57-a319-e3a3fd2d34cb)](http://www.zemanta.com/?px "Enhanced by Zemanta")
