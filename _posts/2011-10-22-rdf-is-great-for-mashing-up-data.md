---
layout: post
title: "RDF is great for mashing up data"
date: "2011-10-22"
categories: 
  - "science-blogging"
  - "vu-university-amsterdam"
---

Source: [Think Links](http://thinklinks.wordpress.com/feed/)

Yesterday, I had the pleasure of giving a tutorial at the [NBIC PhD Course on Managing Life Science Information](http://www.nbic.nl/education/nbic-phd-school/course-schedule/managing-life-science-information/). This week long course focused on applying semantic web technologies to getting to grips with integrating heterogenous life science information.

The tutorial I gave focused on exposing relational databases to the web using the awesome [D2R Server](http://www4.wiwiss.fu-berlin.de/bizer/d2r-server/). It’s really a great piece of software that shows results right away. Perfect for a tutorial. I also covered how to get going with [LarKC](http://www.larkc.eu/) and where that software fit in the whole semantic web data management space.

On to the story…

The students easily exposed our test database ([GPCR receptor](http://www.w3.org/2009/08/7tmdemo)s) as RDF using D2R. Now the cool part: I found out just before the start of my tutorial  that the day before they had setup an RDF repository (Sesame) with some personal profile information. So on the fly I had them take the RDF produced by the database conversion and load that into the repository from the day before . This took a couple of clicks. They were then able to query over both their personal information and this new GPCR dataset. With not much work we hand munged together two really different data sets.

This is old hat to any Semantic Web person, but it was a great reminder of how the flexibility of RDF makes it easy to mashup data. No messing with about with tables or figuring out if the schema is right, just load it up into your triple store and start playing.

  
Filed under: [academia](http://thinklinks.wordpress.com/category/academia/), [linked data](http://thinklinks.wordpress.com/category/linked-data/) Tagged: [mashup](http://thinklinks.wordpress.com/tag/mashup/), [rdf](http://thinklinks.wordpress.com/tag/rdf/), [semantic web](http://thinklinks.wordpress.com/tag/semantic-web/) [![](http://feeds.wordpress.com/1.0/comments/thinklinks.wordpress.com/327/)](http://feeds.wordpress.com/1.0/gocomments/thinklinks.wordpress.com/327/) [![](http://feeds.wordpress.com/1.0/delicious/thinklinks.wordpress.com/327/)](http://feeds.wordpress.com/1.0/godelicious/thinklinks.wordpress.com/327/) [![](http://feeds.wordpress.com/1.0/facebook/thinklinks.wordpress.com/327/)](http://feeds.wordpress.com/1.0/gofacebook/thinklinks.wordpress.com/327/) [![](http://feeds.wordpress.com/1.0/twitter/thinklinks.wordpress.com/327/)](http://feeds.wordpress.com/1.0/gotwitter/thinklinks.wordpress.com/327/) [![](http://feeds.wordpress.com/1.0/stumble/thinklinks.wordpress.com/327/)](http://feeds.wordpress.com/1.0/gostumble/thinklinks.wordpress.com/327/) [![](http://feeds.wordpress.com/1.0/digg/thinklinks.wordpress.com/327/)](http://feeds.wordpress.com/1.0/godigg/thinklinks.wordpress.com/327/) [![](http://feeds.wordpress.com/1.0/reddit/thinklinks.wordpress.com/327/)](http://feeds.wordpress.com/1.0/goreddit/thinklinks.wordpress.com/327/) ![](http://stats.wordpress.com/b.gif?host=thinklinks.wordpress.com&blog=5274753&post=327&subd=thinklinks&ref=&feed=1)
