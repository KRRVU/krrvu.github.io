---
layout: post
title: "Dagstuhl: Semantic Data Management"
date: "2012-05-01"
categories: 
  - "science-blogging"
  - "vu-university-amsterdam"
---

Source: [Think Links](http://thinklinks.wordpress.com/feed/)

Last week, I was at a seminar on Semantic Data Management at Dagstuhl. A month ago I was at Dagstuhl discussing the principles of provenance. You can read more about the atmosphere and style of a Dagstuhl event at the [post on the provenance event.](http://thinklinks.wordpress.com/2012/03/07/thoughts-from-the-dagstuhl-principles-of-provenance-workshop/) From my perspective, it’s pretty cool to get invited to multiple Dagstuhl events in short succession… I think it just happens that two of my main research areas overlap and were scheduled in the same time period.

[![Semantic Data Management Group photo](images/12171.1.B.JPG)](http://www.dagstuhl.de/Gruppenbilder/12171.1.B.JPG)

Obligatory Dagstuhl Group Photo

Indeed, one of the topics for discussion at the seminar was provenance. The others were scalability, dynamcity, and search. The organizers ([Elena Simprel,](http://www.aifb.kit.edu/web/Elena_Simperl/en) [Karl Aberer](http://lsirpeople.epfl.ch/aberer/), [Grigoris Antoniou](http://www.ics.forth.gr/~antoniou), [Oscar Corcho](http://www.dia.fi.upm.es/index.php?page=oscar-corcho&hl=en_US) and [Rudi Studer](http://www.aifb.kit.edu/web/Rudi_Studer)) will put together a report summarizing all the outcomes. What I wanted to do is focus on the key points that I took away from the seminar.

### Scaling semantic data management = scaling graph databases

There was some discussion around what it means to scale in terms of semantic data management. For the most part this boiled down to, what does it mean to scale RDF databases? The organizers did a good job of bringing members of industry in that have actual experience in building scalable RDF systems. The first day contained some great discussion about the guts of databases and what makes scaling hard – issues such as the latency of storage infrastructure and what the right join algorithm were. Steve Harris brought out the difficulty of backup and restore in real world systems and the lack of research in that area.  But my primary feeling was the challenges of scalability are ones of how we deal with large graphs. In my open work in [Open PHACTs](http://www.openphacts.org/), I’ve seen how using graphs has increased our flexibility but challenged us in terms of scalability.

Dealing with large graphs is hard but I think the Semantic Web community can lead the way here because we have a nice substrate, namely, an exchange model for graphs and a common query language.  This leads to the next point:

### Benchmarks! Benchmarks! Benchmarks!

Throughout the week there was discussion of the need for all types of benchmarks. LUBM and BSBM  have served us well but we need better benchmarks: more and different types of queries, more realistic datasets, configurable benchmarks, etc.  There was also discussions of other types of benchmarks, for example, a provenance corpus or a corpus that combines structured and unstructured data for ranking. One comment that I heard in terms of benchmarks is where should you publish them? Unlike the IR community we don’t have  something thing like TREC. Although, I think [USEWOD](http://data.semanticweb.org/usewod/) is a good example of bootstrapping this sort of activity.

### Let’s just be uncertain

One of the cross-cutting themes of the symposium was the need to deal with uncertainty. From dealing with crawled data, to information extraction systems, to even data created by classic knowledge capture, there is a need to express and use uncertainty.  In the area of provenance, I was impressed Martin Theobald’s [URDF](http://urdf.mpi-inf.mpg.de/) system that deals with both uncertain data and uncertain rules.

One major handicap is that RDF systems have is that reification let’s you associate confidence values with statements but is just extremely verbose. At the symposium, Bryan Thompson  and Orri Erling led the way in constructing a proposal to expose statement level identifiers that are compatible with reification. Olaf Hartig even worked out an approach that makes this compatible with SPARQL semantics. I’m looking forward to seeing their final proposal. This will make associating uncertainity and other evidence related information to triples.

One final thing to say is that these discussions made me glad that attributes are included in the PROV model. This provides an important hook for this kind of uncertainty information.

### Crowdsourcing is a component

There was quite a lot of talk about integrating crowdsourcing into the data management stack (See Wolf-Tilo Balke’s [work](http://www.dagstuhl.de/mat/Files/12/12171/12171.BalkeWolfTilo.Slides.pdf)). It’s clear that when we are designing semantic data management systems that crowdsourcing is clearly an important component. Just as ontology engineers are boxes in many of our architectures maybe the crowd should be there by default as well.

### Provenance – get it out – we’re ready

Beyond being a discussant in the conversation. I also gave an intro to provenance research based on the categorization of content, management and use produced in the Provenance Incubator. Luc Moreau, Olaf Hartig and Paolo Missier gave a walkthrough of the [PROV](http://www.w3.org/2011/prov/wiki/Main_Page) spec coming from the W3C.  We had some interesting technical feedback but the general impression I got was – it looks pretty good, get it out there, this is something we need and can use – now.

For example, I had discussions with [Manuel Salvadores](http://www.stanford.edu/~manuelso/) about using PROV as the ontology for describing provenance in BioPortal. [Satya S. Sahoo](http://cci.case.edu/cci/index.php/Satya_Sahoo) (a working group member) is extending PROV for capturing provenance in [sleep studies](http://www.dagstuhl.de/mat/Files/12/12171/12171.SahooSatya.Slides.pdf). There was discussion of connecting PROV with the [Semantic Sensor Network ontology](http://www.w3.org/2005/Incubator/ssn/ssnx/ssn). As with other Semantic Web standards, PROV will provide the basis for both applications and future research. It’s now up to us as working group to get these documents out.

### Embracing other communities

I think the community as a whole has been doing a good job in embracing other communities. This has been shown by those working on RDF stores who have embraced the database community. Also in semantic search there is a good conversation that is bridging the IR community and the database field. Interestingly, semantic search is really a driver of that conversation. I learned about a [good survey paper](https://8c81217a-a-62cb3a1a-s-sites.googlegroups.com/site/kimducthanh/publication/semsearch-survey.pdf?attachauth=ANoY7cqWF2dTrtRMZy2Z_2HwfamMO19y-puPUsH5M0H4xSDtrpkvCH7XBPxgOORi2MSvBcS3iyuT60x0mYsV0JDI0C8wVPenhjvrrFBG0mDh3Gvjqj6u8SGvdfc_lkw_HZ-ujYob2X00gzmrnOWRHxFES9HWDwbnRUJbzJ9bd4lzVbBzrbv_3lymyUxdKsiAr7zXqs9YUOfBZbhS6fPudxeo4eYB9dC3hXuLf61pGkZ3eMoBgs0Uy7w%3D&attredirects=1) by Thanh Tran and Peter Mika at Dagstuhl – highly recommended.

### Federation is a spectrum

There was lots of talk about federation at the symposium. My general impression is that federation is not something that we can say yes or no. Instead different applications will require different kinds of federation. I think there is lots of room to research how we can systematically place systems on the federation spectrum. I come with a series of requirements, where and how should I include federation in my data management scheme. For example, I may want to trade-of computational overhead for space as suggested by [Olaf Hartig](http://olafhartig.de/) in his [Link Traversal Based Query Execution approach](http://www.dagstuhl.de/mat/Files/12/12171/12171.HartigOlaf1.Slides.pdf) (i.e. follow your nose). This caused some of the most entertaining discussions at the symposium. Should you need a data center to query the Web of Data? Let’s find out.

### Conclusion

I think the report coming from this symposium will provide a good document sketching out the research challenges in semantic data management for the next several years. I’m looking forward to it. I’ll end with a quote from a slide in [José Manuel Gomez-Perez](http://lab.isoco.net/people/jmgomez)‘s talk. According to the IDC 2011 Digital Universe study, _metadata is the fastest growing data category_.

There’s demand for the work we are doing and there are many challenges remaining – this promises to be a fun couple of years.

  
Filed under: [academia](https://thinklinks.wordpress.com/category/academia/), [linked data](https://thinklinks.wordpress.com/category/linked-data/) Tagged: [dagstuhl](https://thinklinks.wordpress.com/tag/dagstuhl/), [research challenges](https://thinklinks.wordpress.com/tag/research-challenges/), [semantic data managment](https://thinklinks.wordpress.com/tag/semantic-data-managment/) [![](http://feeds.wordpress.com/1.0/comments/thinklinks.wordpress.com/402/)](http://feeds.wordpress.com/1.0/gocomments/thinklinks.wordpress.com/402/) [![](http://feeds.wordpress.com/1.0/delicious/thinklinks.wordpress.com/402/)](http://feeds.wordpress.com/1.0/godelicious/thinklinks.wordpress.com/402/) [![](http://feeds.wordpress.com/1.0/facebook/thinklinks.wordpress.com/402/)](http://feeds.wordpress.com/1.0/gofacebook/thinklinks.wordpress.com/402/) [![](http://feeds.wordpress.com/1.0/twitter/thinklinks.wordpress.com/402/)](http://feeds.wordpress.com/1.0/gotwitter/thinklinks.wordpress.com/402/) [![](http://feeds.wordpress.com/1.0/stumble/thinklinks.wordpress.com/402/)](http://feeds.wordpress.com/1.0/gostumble/thinklinks.wordpress.com/402/) [![](http://feeds.wordpress.com/1.0/digg/thinklinks.wordpress.com/402/)](http://feeds.wordpress.com/1.0/godigg/thinklinks.wordpress.com/402/) [![](http://feeds.wordpress.com/1.0/reddit/thinklinks.wordpress.com/402/)](http://feeds.wordpress.com/1.0/goreddit/thinklinks.wordpress.com/402/) ![](http://stats.wordpress.com/b.gif?host=thinklinks.wordpress.com&blog=5274753&post=402&subd=thinklinks&ref=&feed=1)
