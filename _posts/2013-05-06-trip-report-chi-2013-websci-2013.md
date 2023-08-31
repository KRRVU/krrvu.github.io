---
layout: post
title: "Trip Report: CHI 2013 & WebSci 2013"
date: "2013-05-06"
categories: 
  - "science-blogging"
  - "vu-university-amsterdam"
---

Source: [Think Links](http://thinklinks.wordpress.com/feed/)

Last week, I attended ACM [CHI 2013](http://chi2013.acm.org) and [Web Science 2013](http://www.websci13.org) in Paris. I had a great time and wanted to give a recap of both conferences, which were collocated.

## CHI

[![2013-04-29 18.45.58](http://thinklinks.files.wordpress.com/2013/05/2013-04-29-18-45-58.jpg?w=300&h=225)](http://thinklinks.files.wordpress.com/2013/05/2013-04-29-16-00-21.jpg)

This was my first time at CHI – the main computer-human interaction conference. It’s not my main field of study but I was there to [Data DJ](http://thinklinks.wordpress.com/category/data-dj/). I had an interactivity submission accepted with [Ayman](https://twitter.com/ayman) from Yahoo! Reseach on using turntables to manipulate data. Here’s the abstract:

> Spinning Data: Remixing live data like a music DJ
> 
> This demonstration investigates data visualization as a performance through the use of disc jockey (DJs) mixing boards. We assert that the tools DJs use in-situ can deeply inform the creation of data mixing interfaces and performances. We present a prototype system, DMix, which allows one to filter and summarize information from social streams using a audio mixing deck. It enables the Data DJ to distill multiple feeds of information in order to give an overview of a live event.
> 
> Paul Groth and David A. Shamma. 2013. Spinning data: remixing live data like a music dj. In _CHI ’13 Extended Abstracts on Human Factors in Computing Systems_ (CHI EA ’13). ACM, New York, NY, USA, 3063-3066. DOI=10.1145/2468356.2479611 [http://doi.acm.org/10.1145/2468356.2479611](http://doi.acm.org/10.1145/2468356.2479611) ([PDF](http://www.mendeley.com/download/public/229912/5766814114/a78099c9368c3e4e7b3557b05acf5024bd5b8c68/dl.pdf))

It was a fun experience… although it was a lot of demo giving (reception + all coffee breaks). The reactions were really positive. Essentially, once a person touched the deck they really got the interaction. Plus, a couple of notable people stopped by that seemed to like the interaction: [Jacob Nielsen](http://www.nngroup.com/people/jakob-nielsen/) and [@kristw](https://twitter.com/kristw) from twitter data science. The kind of response I got made me really want to pursue the project more. I also learned about how we can make the interaction better.

The whole [prototype system is available on github](https://github.com/pgroth/datadj). I wrote the whole using node.js and javascript in a web browser.  Warning: this is very ugly code.

In addition to my demo, I was impressed with the cool stuff on display (e.g. [traceable skateboards](http://www.youtube.com/watch?v=xZMBLfZ06bY)) as well as the number of companies there looking for talent. The conference itself was huge with 3500 people and it was the first conference I attended where they had multiple sponsored parties.

## WebSci

Web Science was after CHI and is more in my area of research.

### What we presented

![2013-05-03 15.16.18](http://thinklinks.files.wordpress.com/2013/05/2013-05-03-15-16-18.jpg?w=225&h=300)

I was pleased that the VU had [8 publications](http://webscience.networkinstitute.org/ws-pubs/) at the conference, which is a really strong showing. Also two of our papers were [nominated for the best paper award](http://webscience.networkinstitute.org/content/two-best-paper-nominees-at-websci13/).

The two papers I had in the conference were very interdisciplinary.

- Fabian Eikelboom, Paul Groth, Victor De Boer and Laura Hollink (2013) [A Comparison between Online and Offline Prayer](http://www.mendeley.com/c/5762237034/p/229912/eikelboom-2013-a-comparison-between-online-and-offline-prayer/ "A Comparison between Online and Offline Prayer"). In _Web Science 2013_. [PDF](http://www.mendeley.com/download/public/229912/5762237034/3f869103e5698ddbb2c1a784004041a4abc4ec1f/dl.pdf "Download file")
    
- Anca Dumitrache, Paul Groth, Peter van den Besselaar (2013) [Identifying Research Talent Using Web-Centric Databases](http://www.mendeley.com/research/identifying-research-talent-using-webcentric-databases/ "Identifying Research Talent Using Web-Centric Databases"). In _Web Science 2013_.  [PDF](http://www.mendeley.com/download/public/229912/5630428764/f71460c90ec81439cd10f89da9ee74ba4db5005e/dl.pdf "Download file")

These papers were chiefly done by the first authors both students at the VU. [Anca](http://www.few.vu.nl/~mde430/) attended Web Science and did a great job presenting our poster on using Google Scholar to measure academic independence. There was a lot of interest and we got quite a few ideas on how to improve the paper (bigger sample!).

The other paper by Fabian Eikelboom was very well received. It compared online and offline pray cards and tried to see how the web modified this form of communication. Here’s a couple of tweets:

> Interesting talk on online and offline prayer and comparing them at [#websci13](http://twitter.com/search?q=%23websci13 "#websci13"). First time I've heard of this [http://t.co/i0w0mLWGbK](http://t.co/i0w0mLWGbK)—  
> Alvin Chin (@GadgetMan4U) [May 02, 2013](http://twitter.com/#!/GadgetMan4U/status/329943685850624000)

> Absolutely BRILLIANT [#websci13](http://twitter.com/search?q=%23websci13 "#websci13") Pecha Kucha on comparisons of on and offline prayer @[WebSciDTC](https://twitter.com/WebSciDTC)—  
> maire byrne (evans) (@MaireAByrne) [May 02, 2013](http://twitter.com/#!/MaireAByrne/status/329943099700834305)

### Conference thoughts

I found quite a few things that I really liked at this year’s web science. A couple of pointers:

- Henry S Thompson, Jonathan A Rees and Jeni Tennison: URIs in data: for entities, or for descriptions of entities: A _critical analysis –_ Talked about the http range 14 and the problem of unintended extensibility points within standards. I think a critical area of Web Science is how the social construction of technical standards impacts the Web and its development. This is an example of this kind of research.
- Catherine C. Marshall and Frank M. Shipman: Experiences Surveying the Crowd: R_eflections on methods, participation, and reliability -_ really got me thinking about the notion of hypotheticals in law and how this relates to provenance on the web.
- Panagiotis Metaxas and Eni Mustafaraj: The Rise and the Fall of a Citizen Reporter – a compelling example of how twitter influences the mexican drug war and how trust is difficult to determine online. The subsequent [Trust Trails project](http://cs.wellesley.edu/~pmetaxas/TrustTrails.pdf) looks interesting.
- The folks over at the UvA at  [digitalmethods.net](http://digitalmethods.net) are doing a lot of fun work with respect to studying the web as a social object. It’s worth looking at their work.
- Jérôme Kunegis, Marcel Blattner and Christine Moser. [Preferential Attachment in Online Networks: Measurement and Explanations](http://userpages.uni-koblenz.de/~kunegis/paper/kunegis-blattner-moser-preferential-attachment-in-online-networks-measurement-and-explanations.pdf) – interesting discussion of how good our standard network models are.  [Check out there collection of networks to download and analyze!](http://konect.uni-koblenz.de/networks/)
- Sebastien Heymann and Benedicte Le Grand. Towards A Redefinition of Time in Information Networks?

Unfortunately, there were some things that I hope will improve for next year. First, as you can tell above the papers were not available online during the conference. This is really a bummer when your trying to tweet about things you see and follow-up later. Secondly, I thought there were a few too many philosophy papers. In particular, it worries me when a computer scientist is presenting a philosophy paper at a science conference. I think the program committee needs to watch out for spreading too thinly in the name of interdisciplinarity. Finally, the pecha kucha session was a real  success – short, succinct presentations that really raised interest in the work. This, however, didn’t carry over into the main sessions which often ran too long.

Overall, both CHI and Web Science were well worth the time – I made a bunch of connections and saw some good research that will influence some of my work. Oh and it turns out Paris has some amazing coffee:

[![2013-05-03 10.37.29](http://thinklinks.files.wordpress.com/2013/05/2013-05-03-10-37-29.jpg?w=300&h=225)](http://thinklinks.files.wordpress.com/2013/05/2013-05-03-10-37-29.jpg)

  
Filed under: [data dj](http://thinklinks.wordpress.com/category/data-dj/), [interdisciplinary research](http://thinklinks.wordpress.com/category/interdisciplinary-research/) Tagged: [#chi2013](http://thinklinks.wordpress.com/tag/chi2013/), [conference](http://thinklinks.wordpress.com/tag/conference/), [data dj](http://thinklinks.wordpress.com/tag/data-dj/), [web science](http://thinklinks.wordpress.com/tag/web-science/), [websci13](http://thinklinks.wordpress.com/tag/websci13/) [![](http://feeds.wordpress.com/1.0/comments/thinklinks.wordpress.com/518/)](http://feeds.wordpress.com/1.0/gocomments/thinklinks.wordpress.com/518/) ![](http://stats.wordpress.com/b.gif?host=thinklinks.wordpress.com&blog=5274753&post=518&subd=thinklinks&ref=&feed=1)
