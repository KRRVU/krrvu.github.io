---
title: "Trip Report: ESWC 2013"
date: "2013-06-03"
categories: 
  - "science-blogging"
  - "vu-university-amsterdam"
---

Source: [Think Links](http://thinklinks.wordpress.com/feed/)

I think since I’ve moved to Europe I’ve been attending [ESWC](http://2013.eswc-conferences.org/) (Extended/European Semantic Web Conference) and I always get something out of the event. There are plenty of familiar faces but also quite a few new people and it’s a great environment for having chats. In addition, the quality of the content is always quite good. This year the event was held in [Montpellier](http://en.wikipedia.org/wiki/Montpellier) and was for the most part well organized: the main conference wifi worked!

The stats:

- 300 participants
- 42 accepted papers from 162 submissions
- 26% acceptance rate
- 11 workshops + 7 tutorials

So what was I doing there:

- I presented a paper in the [Sepublica workshop](http://sepublica.mywikipaper.org/) co-authored with [Sara Magliacane](http://www.few.vu.nl/~sme340/) on [Repurposing Benchmarks for Provenance Reconstruction](http://www.mendeley.com/download/public/229912/5821740274/e6768447fdb142c59b163040be652c69128c3a46/dl.pdf).
- With Jun Zhao and Olaf Hartig, we gave a [half-day tutorial on PROV](http://www.w3.org/2001/sw/wiki/ESWC2013ProvTutorial).
- I presented [Open PHACTS](http://www.openphacts.org/) at the EU Project Networking Session.

The [VU Semantic Web group](http://semanticweb.cs.vu.nl) also had a strong showing:

- [Albert Meroño-Peñuela](http://www.albertmeronyo.org/) won the best PhD symposium paper for his work on digital humanities and the semantic web.
- The USEWOD workshop’s (led by Laura Hollink) datasets were used by a number of main track papers for evaluation.
- Stefan Schlobach and Laura Hollink were on the organizing committee. And we organized a couple of workshops & tutorials.
- Posters/Demos:
    - Albert Meroño-Peñuela, Rinke Hoekstra, Andrea Scharnhorst, Christophe Guéret and Ashkan Ashkpour. _Longitudinal Queries over Linked Census Data._
    - Niels Ockeloen, Victor de Boer and Lora Aroyo. _LDtogo: A Data Querying and Mapping Framework for Linked Data Applications._
- Several workshop papers.

I’ll try to pull out what I thought were the highlights of the event.

## What is a semantic web application?

[![Can you escape Frank?](http://thinklinks.files.wordpress.com/2013/06/2013-05-28-09-44-13.jpg?w=300&h=225)](http://thinklinks.files.wordpress.com/2013/06/2013-05-28-09-44-13.jpg)

Can you escape Frank?

The [keynotes](http://2013.eswc-conferences.org/program/keynote-speakers) from Enrico Motta and David Karger focused on trying to define what a semantic web application was. This starts out in the form of does a Semantic Web application need to use the Semantic Web set of standards (e.g. RDF, OWL, etc). So from my perspective, the answer is no. These standards are great infrastructure for building these applications but are they necessary, no (see google knowledge graph).  Then what is a semantic web application?

From what I could gather, Motta would define it as an application that is scalable, uses the web and embraces Model Theoretic semantics. For me that’s rather limiting, there are many other semantics that may be appropriate… we can ground meaning in something else other than model theory. I think a good example of this is the work on [Pragmatic Semantics](http://www-sop.inria.fr/members/Fabien.Gandon/docs/eswc2013/KeyNoteSchlobachGueretAImWD.pdf) that my colleague Stefan Schlobach presented at the [Artificial Intelligence meets the Semantic Web workshop](https://sites.google.com/site/aimwd13/). Or we can reach back into AI and see discussion’s from Brooks’ classic paper [Elephant’s Don’t Play Ches](http://rair.cogsci.rpi.edu/pai/restricted/logic/elephants.pdf)s.  I felt that Karger’s definition (in what was a great keynote) was getting somewhere. He defined a semantic web application essentially as:

> An application whose schema is expected to change.

This seems to me to capture the semantic portion of the definition, in a sense that the semantics need to be understood on the fly. However, I think we need to role the web back into this definition… Overall, I thought this discussion was worth having and helps the field define what it is that we are aiming at. To be continued…

## Homebrew databases

[![2013-05-29 09.18.05](http://thinklinks.files.wordpress.com/2013/06/2013-05-29-09-18-05.jpg?w=300&h=277)](http://thinklinks.files.wordpress.com/2013/06/2013-05-29-09-18-05.jpg)

Homebrew databases

As I said, I thought Karger’s keynote was great. He gave a talk within a talk, on the subject of homebrew databases from [this paper in CHI 2011](http://ellieharmon.com/wp-content/papercite-data/pdf/voida-2011.pdf):

Amy Voida, Ellie Harmon, and Ban Al-Ani. 2011. Homebrew databases: complexities of everyday information management in nonprofit organizations. In _Proceedings of the SIGCHI Conference on Human Factors in Computing Systems_ (CHI ’11). ACM, New York, NY, USA, 915-924. DOI=10.1145/1978942.1979078 [http://doi.acm.org/10.1145/1978942.1979078](http://doi.acm.org/10.1145/1978942.1979078)

They define a homebrew database as “an assemblage of information management resources that people have pieced together to satisfice their information management needs.” This is just what we see all the time, the combination of excel, word, email, databases and don’t forget normal paper brought together to try to attack information management problems. A number of our use cases from the pharma industry as well as science reflect essentially this practice. It’s great to see a good definition of this problem grounded in ethnographic studies.

## The Concerns of Linking

There were a couple of good papers on generating linkage across datasets (the central point of linked data). In Open PHACTS, we’ve been dealing with the notion of essentially context dependent linkages. I think this notion is becoming more prevalent in the community. We had a lot of positive response on this in the poster session when presenting Open PHACTS. Probably, my favorite paper was on linking the Smithsonian American Art museum to the Linked Data cloud. They use PROV to drive their link generation. Essentially, proposing links to human’s who then verify the connections. See:

- Pedro Szekely, Craig Knoblock, Fengyu Yang, Xuming Zhu, Eleanor Fink, Rachel Allen and Georgina Goodlander._[Connecting the Smithsonian American Art Museum to the Linked Data Cloud](http://eswc-conferences.org/sites/default/files/papers2013/szekely.pdf)._

I also liked the following paper on which hardware environment you should use when doing link discovery. Result: use GPU’s there fast!

- Axel-Cyrille Ngonga Ngomo, Lars Kolb, Norman Heino, Michael Hartung, Sören Auer andErhard Rahm. _[When to Reach for the Cloud: Using Parallel Hardware for Link Discovery](http://eswc-conferences.org/sites/default/files/papers2013/ngomo_cloud.pdf)._

Additionally, I think the following paper is cool because they use network statistics not just to measure but to do something, namely create links:

- Bernardo Pereira Nunes, Stefan Dietze, Marco Antonio Casanova, Ricardo Kawase, Besnik Fetahu and Wolfgang Nejdl._[Combining a co-occurrence-based and a semantic Measure for Entity Linking](http://eswc-conferences.org/sites/default/files/papers2013/nunes.pdf)._

## APIs

[APIs](http://liris.cnrs.fr/~pchampin/2013/salad/#1) were a growing theme of the event with things like the [Linked Data Platform working group](http://www.w3.org/2012/ldp/wiki/Main_Page) and  the successful [SALAD workshop](http://salad2013.linkedservices.org). (Fantastic acronym). Although I was surprised people in the workshop hadn’t heard of the [Linked Data API.](http://code.google.com/p/linked-data-api/) We had a lot of good feedback on the Open PHACTS API. It’s just the case that there is more developer expertise for using web service apis rather than semweb tech. I’ve actually seen a lot of demand for Semweb skills and while we our doing our best to train people there is still this gap. It’s good then that we are thinking about how these two technologies play together nicely.

## Random Notes

- We should support content negotiation in [dev.openphacts.org](http://dev.openphacts.org/).
- The  Semantic Graph Management Tutorial had good introductory slides (ask me if you want them).
- [The Benchmark Handbook edited by Jim Gray](http://research.microsoft.com/en-us/um/people/gray/BenchmarkHandbook/TOC.htm)
- [http://sdshare.org](http://sdshare.org/) is worth a look for publishing updates for RDF based info.
- [Bio2RDF version 2 is looking great.](http://eswc-conferences.org/sites/default/files/papers2013/callahan.pdf) Lots of updates and they use PROV.
- Tobias Kuhn [talked about nanopublications](http://eswc-conferences.org/sites/default/files/papers2013/kuhn.pdf).
- I’m getting more and more convinced that you can get good results with [SPARQL to SQL translators](http://www.rdb2rdf.org/eswc2013-tutorial/).
    - [Prefetch data anyone?](http://eswc-conferences.org/sites/default/files/papers2013/lorey.pdf)
- [IPTC news subject codes in skos.](http://cv.iptc.org/newscodes/subjectcode/)
- [LOD cloud colored by license](http://ns.inria.fr/l4lod/). Huge and neglected issue.
- I should stop having high hopes for panels.
- Golden rule of session organization: be on time.

  
Filed under: [events](http://thinklinks.wordpress.com/category/events/), [linked data](http://thinklinks.wordpress.com/category/linked-data/) Tagged: [conference](http://thinklinks.wordpress.com/tag/conference/), [eswc2013](http://thinklinks.wordpress.com/tag/eswc2013/), [linked data](http://thinklinks.wordpress.com/tag/linked-data/), [semantic web](http://thinklinks.wordpress.com/tag/semantic-web/) [![](http://feeds.wordpress.com/1.0/comments/thinklinks.wordpress.com/533/)](http://feeds.wordpress.com/1.0/gocomments/thinklinks.wordpress.com/533/) ![](http://stats.wordpress.com/b.gif?host=thinklinks.wordpress.com&blog=5274753&post=533&subd=thinklinks&ref=&feed=1)
