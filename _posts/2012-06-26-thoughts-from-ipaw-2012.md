---
title: "Thoughts from IPAW 2012"
date: "2012-06-26"
categories: 
  - "science-blogging"
  - "vu-university-amsterdam"
---

Source: [Think Links](http://thinklinks.wordpress.com/feed/)

This year I had the opportunity to be program co-chair and help organize the [4th International Provenance and Annotation Workskhop (IPAW)](http://ipaw2012.bren.ucsb.edu/). The event went great, really, better than I imagined. First, I was fortunate to be organizing it with [James Frew](http://frew.eri.ucsb.edu/) from the [Bren School of Environmental Science and Management a the University of California, Santa Barabara](http://bren.ucsb.edu/). He not only helped coordinate the program but along with his team took care of all the local organization. It’s hard to beat sunny Santa Barbara as a location, but they also made sure that everything ran smoothly: great wifi, shuttles to and from the location, tasty outdoor lunches looking over the ocean, an open air poster session with wine and cheese, and a BBQ on the beach for a workshop dinner:

[![](http://thinklinks.files.wordpress.com/2012/06/bbq.jpeg?w=500&h=374)](http://thinklinks.files.wordpress.com/2012/06/bbq.jpeg)

The IPAW workshop dinner. Photo from Andreas Schrieber.

So big kudos to Frew and his team. Obviously, beyond being well run we covered a lot in the two days of the main workshop. The workshop had 47 attendees and you can find the twitter log [here](http://ipaw2012.bren.ucsb.edu/index.php/TwitterLog).

### Research Highlights

I think the [program](http://ipaw2012.bren.ucsb.edu/index.php/Program) really highlighted where we are at in provenance research today and the directions forward. I won’t go through every paper but  just try to pick 3 interesting trends.

#### 1) Using Provenance to Address the Messiness of the Web

The Web provides us a fantastic source of knowledge. But the problem is that knowledge is completely unclean and unintegrated. Even efforts such as Linked Data while giving us better data our still messy and still under-integrated. Both researchers and firms have been trying to make clean integrated  knowledge, but then they are faced with what Timothy Lebo in his [paper](http://bit.ly/lebo-ipaw-2012-slides) termed the _Integrator’s Dilemma_. A integrator may produce a clean well-structured data set, but in the process the resulting data set looses authority and a connection to domain expertise. To rectify this problem, provenance can be used to identify the authoritative source and connect back to domain expertise. Indeed, Jim McCusker and colleagues argued that provenance is the [3rd step to Data Sanity.](http://bit.ly/mccusker-ipaw-2012-slides)

However, then we run into Tim’s 1st law of producing provenance:

> For any provenance record, there exists a provenance consumer that will need it, but will not like how it is provided.

Tim suggests a service based solution to provide provenance at the correct granularity for provenance. While I don’t know if that is the right solution, it’s clear that providing provenance at the right level of granularity is one foundation to building confidence in integrated web data sources.

Another example of trying different ways of using provenance to address messiness is the use of [network analysis](http://eprints.soton.ac.uk/340068/) to understand provenance captured from crowd sourced applications.

#### **2**) Provenance and Credit are Intertwined

Science has always been a driver of research in provenance and we saw a number of good pieces of work addressing domains ranging from c[limate analysis](http://vgc.poly.edu/~dakoop/pubs/uvcdat-prov.pdf) to [archeology](http://eprints.soton.ac.uk/340405/). However, as our key note speaker Phil Bourne [pointed out in his talk](http://ipaw2012.bren.ucsb.edu/images/c/cf/Bourne-keynote-ipaw12.pdf), scientists are not using provenance technologies in their work. He argued that this is for two reasons: 1) because they are not given credit for all parts of the scientific process and 2) provenance infrastructure is still not easy enough to use.  Phil argued that it was fundamental that more artifacts of the research lifecycle need to be given credit to facilitate sharing and thus increase the pace of innovation particularly in the life sciences. Thus, for scientists to capture their information in a sharable fashion they need to be given credit for doing so. (Yes, he connected [altmetrics](http://altmetrics.org) to provenance – very cool from my point of view). To do this, he argued, we need better support for provenance throughout the research lifecycle. However, while tools exist, they are far from being usable and integrated enough into everyday science practice. This is a real challenge to the provenance community. We need to do better at getting our approaches into scientists hands.

### 3) The Problem of Post-hoc

Much work in the provenance literature has asked the question of how does one capture provenance effectively in computational systems. But many times this is just not possible. The user may not have thought about installing the system to capture provenance in the first place or may not have chosen to write down their rational for taking some action. This is an area that I’m [actively researching](http://ceur-ws.org/Vol-856/paper_4.pdf) so it was a great to see others starting to address the problem. [Tom De Neiss attacked the problem](http://eprints.dcs.kcl.ac.uk/1400/) of reconstructing provenance for a collection of newspaper articles using semantic similarity. An even more farther out idea presented at the workshop was to try and [reconstruct the provenance of decision made by a human](http://eprints.dcs.kcl.ac.uk/1400/) using simulation. Both works highlight the need for dealing with incomplete or even non-existant provenance.

These were just some of the themes that I saw. Overall, the presentations were good and the audience was engaged. We had lots of hall time and I heard many intense discussions so I’m hoping that the event spurred more research. I know personally we will try to pursue a collaboration to build a provenance corpus to study this reconstruction problem.

### A Provenance Week

IPAW has a tradition of being hosted as an independent event, which allows us to not only have the two day workshop but also organize collocated events. This IPAW was the same. The Data Observation Network for Earth organized a [meeting on provenance and scientific workflow](http://www.dataone.org/working_groups/scientific-workflows-and-provenance-working-group) collocated with IPAW. Additionally, the W3C Provenance Working Group both gave a [tutorial](http://www.w3.org/blog/SW/2012/06/25/prov-tutorial/) before the workshop and held their [two day face-to-face meeting](http://www.w3.org/blog/SW/2012/06/25/report-provenance-working-group-3rd-face-to-face-meeting/) afterwards. Here’s me presenting the core of the provenance data model to the 28 tutorial participants.

[![](http://thinklinks.files.wordpress.com/2012/06/prov-dm-paul.jpeg?w=500&h=375)](http://thinklinks.files.wordpress.com/2012/06/prov-dm-paul.jpeg)

The Provenance Data Model. It’s easy! Photo prov:wasAttributedTo Andreas Schrieber

### Conclusion

IPAW 2012 was a lot effort but it was worth it – fun discussion, beautiful weather and research insight.  Again, the community voted to have another IPAW in 2014. The community is continuing to play to its strengths in workflows, databases and science applications while exploring novel areas. In the CFP for IPAW, we wrote that “2012 will be a watershed year for provenance/annotation research.” For me, IPAW confirmed that statement.

  
Filed under: [academia](http://thinklinks.wordpress.com/category/academia/), [events](http://thinklinks.wordpress.com/category/events/) Tagged: [#ipaw2010](http://thinklinks.wordpress.com/tag/ipaw2010/), [international provenance and annotation workshop](http://thinklinks.wordpress.com/tag/international-provenance-and-annotation-workshop/), [ipaw](http://thinklinks.wordpress.com/tag/ipaw/) [![](http://feeds.wordpress.com/1.0/comments/thinklinks.wordpress.com/417/)](http://feeds.wordpress.com/1.0/gocomments/thinklinks.wordpress.com/417/) [![](http://feeds.wordpress.com/1.0/delicious/thinklinks.wordpress.com/417/)](http://feeds.wordpress.com/1.0/godelicious/thinklinks.wordpress.com/417/) [![](http://feeds.wordpress.com/1.0/facebook/thinklinks.wordpress.com/417/)](http://feeds.wordpress.com/1.0/gofacebook/thinklinks.wordpress.com/417/) [![](http://feeds.wordpress.com/1.0/twitter/thinklinks.wordpress.com/417/)](http://feeds.wordpress.com/1.0/gotwitter/thinklinks.wordpress.com/417/) [![](http://feeds.wordpress.com/1.0/stumble/thinklinks.wordpress.com/417/)](http://feeds.wordpress.com/1.0/gostumble/thinklinks.wordpress.com/417/) [![](http://feeds.wordpress.com/1.0/digg/thinklinks.wordpress.com/417/)](http://feeds.wordpress.com/1.0/godigg/thinklinks.wordpress.com/417/) [![](http://feeds.wordpress.com/1.0/reddit/thinklinks.wordpress.com/417/)](http://feeds.wordpress.com/1.0/goreddit/thinklinks.wordpress.com/417/) ![](http://stats.wordpress.com/b.gif?host=thinklinks.wordpress.com&blog=5274753&post=417&subd=thinklinks&ref=&feed=1)
