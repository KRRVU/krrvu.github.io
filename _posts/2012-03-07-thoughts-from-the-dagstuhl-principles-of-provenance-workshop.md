---
title: "Thoughts from the Dagstuhl Principles of Provenance Workshop"
date: "2012-03-07"
categories: 
  - "science-blogging"
  - "vu-university-amsterdam"
---

Source: [Think Links](http://thinklinks.wordpress.com/feed/)

Last week, I attended a workshop at [Dagstuhl](http://www.dagstuhl.de/ueber-dagstuhl/konzept/) on the Principles of Provenance. Before talking about the content of the workshop itself, it’s worth describing the experience of Dagstuhl. The venue itself is a manor house located pretty much in the middle of nowhere in southwest Germany.  The nature around the venue is nice and it really is away from it all. All the attendees stay in the manor house so you spend not only the scheduled workshop times with your colleagues but also breakfast, lunch, dinner and evenings. They also have small tricks to ensure that everyone mingles, for example, by pseudo-randomly seating people at different tables for meals. Additionally, Dagstuhl is specifically for computer science – they have a good internet connection and one of the best computer science libraries I’ve seen.  All these things together make Dagstuhl a unique  intellectually intense environment. It’s one of the nicest traditions in computer science.

[![](http://thinklinks.files.wordpress.com/2012/03/dagstuhl-prov-me.jpg?w=300&h=225 "dagstuhl-prov-me")](http://thinklinks.files.wordpress.com/2012/03/dagstuhl-prov-me.jpg)

Me at the Principles of Provenance workshop

With that context in mind, the organizers of the [Principles of Provenance](http://www.dagstuhl.de/12091) workshop (James Cheney, Wang-Chiew Tan, Bertram Ludaescher, Stijn Vansummeren) brought together computer scientists studying provenance from the perspective of databases, the semantic web, scientific workflow, programming languages and software engineering. While I knew most of the people in this broad community (at least from paper titles), I met some new people and got to know people better. The organizers started the workshop with overviews of provenance work from 4 areas:

1. Provenance in Database Systems
2. Provenance in Workflows and Scientific Computation
3. Provenance in Software Engineer, programming languages and security
4. Provenance interchange on the web (i.e. the w3C standardization effort)

These tutorials were a great idea because they provided a common basis for communication throughout the week. The rest of the week combined quite a few talks and plenty of discussion The organizers are putting together a report right now containing abstracts and presentations so I won’t go into that more here. What I do want to do is pull out 3 take-aways that I had from the week.

1) Connecting consensus models to formal foundations

Because provenance often spans multiple systems (my data is often sourced from somewhere else), there is a need for provenance systems to interoperate. There have be a number of efforts to enable this interoperability including the creation of the [Open Provenance Model](http://openprovenance.org/) as well as the current [standardization effort at the W3C](http://www.w3.org/2011/prov/wiki/Main_Page). Because these efforts are trying to bridge across multiple implementation, they are driven by community consensus: what models can we agree upon, what is minimally necessary for interchange, what is easy to understand and implement.

Separately, there is quite a lot of work on formal foundations of provenance especially within the database community. This work is grounded in applications but also in formal theory that ensures that provenance information has nice properties. Concretely, one can show that certain types of provenance within a database context can be expressed as polynomials, algebraically manipulated, and also related. ([semirings](http://en.wikipedia.org/wiki/Semiring)!) Plus, provenance polynomials sounds nice. Check out T.J. Green’s thesis for starters:

Todd J. Green. [_Collaborative Data Sharing with Mappings and Provenance_.](http://www.cs.ucdavis.edu/~green/papers/dissertation.pdf) PhD thesis, University of Pennsylvania, 2009

During the workshop, it became clear to me that the consensus based models (which are often graphical in nature) can not only be formalized but also be directly connected to these database focused formalizations. I just needed to get over the differences in syntax.  This could imply that we could have nice way to trace provenance across systems and through databases and be able to understand the mathematical properties of this interconnection.

2) Social implications of producing provenance

For a couple of years now, I’ve been asked by people and have asked myself, so what do you do with provenance? I think there are a lot of good answers for that (e.g. [requirements for provenance in e-science](http://www.springerlink.com/content/8257g3g11571n271/)). However, the community has spent a lot of time thinking about how to capture provenance from a technical point of view asking questions like: how do we instrument systems? how do we store provenance efficiently? can we leverage execution environments for tracing?

At Dagstuhl, Carole Goble asked another question, why would people record and share provenance in the first place? There are big social implications that we need to grapple with: producing provenance may expose information that we are not ready to share, it may require us to change work practice  leading to effort that we may not want to give or it may be in form that is to raw to be useful. Developing techniques to address these issues is from my point of view a new and important area of work.

From my perspective, we are starting to work on the ideas of how to reconstruct provenance from data that will hopefully reduce the effort for producers of provenance.

3) Provenance is important for messy data integration

A key usecase for  provenance is tracking back to original data sources after data has been integrated. This is particularly important when the data integration requires complex processing (e.g. natural language processing). Christopher Ré gave a fantastic example of this with a demonstration the WiscI system part of the [Hazy](http://research.cs.wisc.edu/hazy/) project. This application enriches Wikipedia pages with facts collected from a (~40 TB) web crawl and provides links back to a supporting source for those facts. It was a great example of how provenance is really foundational to providing confidence in these systems.

Beyond these points, there was a lot more discussed, which will be summarized in the forthcoming report. This was a great workshop for me. From my point of view, I wanted to thank the organizers for putting it together. It’s a lot of effort. Additionally, thanks to all of the participants for really great conversations.

  
Filed under: [academia](http://thinklinks.wordpress.com/category/academia/) Tagged: [dagstuhl](http://thinklinks.wordpress.com/tag/dagstuhl/), [provenance](http://thinklinks.wordpress.com/tag/provenance/) [![](http://feeds.wordpress.com/1.0/comments/thinklinks.wordpress.com/359/)](http://feeds.wordpress.com/1.0/gocomments/thinklinks.wordpress.com/359/) [![](http://feeds.wordpress.com/1.0/delicious/thinklinks.wordpress.com/359/)](http://feeds.wordpress.com/1.0/godelicious/thinklinks.wordpress.com/359/) [![](http://feeds.wordpress.com/1.0/facebook/thinklinks.wordpress.com/359/)](http://feeds.wordpress.com/1.0/gofacebook/thinklinks.wordpress.com/359/) [![](http://feeds.wordpress.com/1.0/twitter/thinklinks.wordpress.com/359/)](http://feeds.wordpress.com/1.0/gotwitter/thinklinks.wordpress.com/359/) [![](http://feeds.wordpress.com/1.0/stumble/thinklinks.wordpress.com/359/)](http://feeds.wordpress.com/1.0/gostumble/thinklinks.wordpress.com/359/) [![](http://feeds.wordpress.com/1.0/digg/thinklinks.wordpress.com/359/)](http://feeds.wordpress.com/1.0/godigg/thinklinks.wordpress.com/359/) [![](http://feeds.wordpress.com/1.0/reddit/thinklinks.wordpress.com/359/)](http://feeds.wordpress.com/1.0/goreddit/thinklinks.wordpress.com/359/) ![](http://stats.wordpress.com/b.gif?host=thinklinks.wordpress.com&blog=5274753&post=359&subd=thinklinks&ref=&feed=1)
