---
title: "GoogleArt project to RDF, now available as a dump"
date: "2011-04-01"
categories: 
  - "science-blogging"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Semantic Web world for you](http://semweb4u.wordpress.com/feed/)

_This post is a re-blog of [this post](http://semanticweb.com/googleart-semantic-data-wrapper-technical-update_b18726) published on semanticweb.com_

Some weeks ago, a first version of a wrapper for the GoogleArt project from Google [was put on line](http://semanticweb.com/googleart-gets-a-semantic-touch-up_b17540) (see also [this blog post](http://semweb4u.wordpress.com/2011/02/03/googleart-project-to-rdf/)). This wrapper that was first offering data only data may only be available for individual paintings has now been extended to museums. The front page of GoogleArt is also available as RDF, providing a machine-readible [list of museums](http://linkeddata.few.vu.nl/googleart/index.rdf). This index page makes it possible, and easy, to download an entire snapshot of the data set so let’s see how to do that ![;-)](images/icon_wink.gif)

###### Downloading the data set from a wrapper

Wrappers around web services offer an RDF representation of a content available at the original source. For instance, the [SlideShare wrapper](http://linkeddata.few.vu.nl/slideshare/) provides an RDF representation of a presentation page from the SlideShare web site. The [GoogleArt wrapper](http://linkeddata.few.vu.nl/googleart/) takes the same approach for paintings and museums listed on the GoogleArt site. Typically, these wrapper would work by mimicking the URI scheme of the site they are wrapping. Changing the hostname, and part of the path, of the URL of the original resource for that of the wrapper gives you access to the seeked data.

From a linked data perspective, wrappers are doing a valid job at providing de-referencable URIs for the entities they described. However, the “de-referencing only” scheme makes them more difficult to query. Wrappers don’t offer SPARQL end points as they don’t store the data they serve, that data being computing on-the-fly when the URIs are accessed. To query a wrapper one has to rely on an indexing service harvesting the different document and indexing them. Something that reminds us of the way to find Web documents and for which the semantic web index [Sindice](http://sindice.com/) is the state of the art solution.

But such external indexing service may not provide you with the entire set of triples or not allow to download big chunks of their harvested data. In that case, the best way to get the entire dataset locally is to use a spider to download the content published under the different URIs.

[LDSpider](http://code.google.com/p/ldspider/), an application developped by [Andreas Harth](http://harth.org/andreas/) ([AIFB](http://www.aifb.kit.edu/)), [Juergen Umbrich](http://umbrich.net)([DERI](http://www.deri.ie/)), [Aidan Hogan](http://sw.deri.org/~aidanh/) and [Robert Isele](http://www.wiwiss.fu-berlin.de/en/institute/pwo/bizer/team/IseleRobert.html), is the perfect tool for doing that. LDSpider crawls linked data resources, looking for triples it stores in a Nquad file. Nquads are triples to which a named graph has been added. By using it, LDSpider keeps track of the sources of the triples in the final result.

Using a few simple commands, it is possible to harvest all the triples published by the GoogleArt Wrapper. As of the time of writting, there seems to be a bug with the latest release of LDSpider (1.1d) that prevented us from downloading the data. However, everything works fine with the trunk version which can be downloaded and compile that way:

svn checkout http://ldspider.googlecode.com/svn/trunk/ ldspider-read-only
cd ldspider-read-only
ant build

One we have LDSpider ready to go, point it to the index page “-u http://linkeddata.few.vu.nl/googleart/index.rdf”, ask for a load balanced crawl “-c” and request to stay within the same domain name “-y” as the starting resource. This last option is very important! Since the resources published by the wrapper are connected to DBpedia resources, omitting the “-y” would allow the crawler to download the content of the resources that are pointed to in DBpedia, and then download the content of the resources DBpedia points to, and so on… The last parameter to set is the name of the output file “-o data.nq” and you are ready:

java -jar dist/ldspider-trunk.jar -u http://linkeddata.few.vu.nl/googleart/index.rdf -y -c -o data.nq

After some time (24 minutes in our case), you get a file with all the data + some header information with extra information about the downloaded resource:

<http://linkeddata.few.vu.nl/googleart/museums/vangogh/orchards-in-blossom-view-of-arles-30> <http://code.google.com/p/ldspider/ns#headerInfo> \_:header1087646481301043174989 <http://linkeddata.few.vu.nl/googleart/museums/vangogh/orchards-in-blossom-view-of-arles-30> .
\_:header1087646481301043174989 <http://www.w3.org/2006/http#responseCode> "200"^^<http://www.w3.org/2001/XMLSchema#integer> <http://linkeddata.few.vu.nl/googleart/museums/vangogh/orchards-in-blossom-view-of-arles-30> .
\_:header1087646481301043174989 <http://www.w3.org/2006/http#date> "Fri, 25 Mar 2011 08:51:04 GMT" <http://linkeddata.few.vu.nl/googleart/museums/vangogh/orchards-in-blossom-view-of-arles-30> .
\_:header1087646481301043174989 <http://www.w3.org/2006/http#server> "TornadoServer/1.0" <http://linkeddata.few.vu.nl/googleart/museums/vangogh/orchards-in-blossom-view-of-arles-30> .
\_:header1087646481301043174989 <http://www.w3.org/2006/http#content-length> "5230" <http://linkeddata.few.vu.nl/googleart/museums/vangogh/orchards-in-blossom-view-of-arles-30> .
\_:header1087646481301043174989 <http://www.w3.org/2006/http#content-type> "application/rdf+xml" <http://linkeddata.few.vu.nl/googleart/museums/vangogh/orchards-in-blossom-view-of-arles-30> .
\_:header1087646481301043174989 <http://www.w3.org/2006/http#connection> "Keep-Alive" <http://linkeddata.few.vu.nl/googleart/museums/vangogh/orchards-in-blossom-view-of-arles-30> .

To filter these out and get only the data contained in the document, simply use a grep:

grep -v "\_:header" data.nq > gartwrapper.nq

The final document “gartwrapper.nq” contains around 37k triples, out of which 1.6k are links to DBpedia URIs. More information about the data set is available through it [CKAN package description](http://ckan.net/package/googleart-wrapper). That description also contains a link to a [pre-made dump](https://github.com/downloads/cgueret/GoogleArt-wrapper/gartwrapper.nq.gz).

###### Concluding remarks

This download technique is applicable to downloading the content provided by any wrapper or, in general, data set for which only de-refenrencable URIs are provided. However, we should stress that to ensure completness an seed URI listing all (or most of) the published resources: the spider works by following links so be sure to have access to well connected resources. If several seeds are needed to cover the entire data set, iterate the same process starting at every one of them or use the dedicated option from LDSpider (“-d”).

###### Related Articles

- [GoogleArt – Semantic Data Wrapper (Technical Update)](http://semanticweb.com/googleart-semantic-data-wrapper-technical-update_b18726) (semanticweb.com)
- [GoogleArt project to RDF](http://semweb4u.wordpress.com/2011/02/03/googleart-project-to-rdf/) (semweb4u.wordpress.com)
- [Linked Data | Strategies for Building Semantic Web Applications](http://notes.3kbo.com/linked-data) (notes.3kbo.com)
- [Survey of Pythonic tools for RDF and Linked Data programming](http://www.michelepasin.org/techblog/2011/02/24/survey-of-pythonic-tools-for-rdf-and-linked-data-programming/) (michelepasin.org)

  
[![](http://feeds.wordpress.com/1.0/comments/semweb4u.wordpress.com/89/)](http://feeds.wordpress.com/1.0/gocomments/semweb4u.wordpress.com/89/) [![](http://feeds.wordpress.com/1.0/delicious/semweb4u.wordpress.com/89/)](http://feeds.wordpress.com/1.0/godelicious/semweb4u.wordpress.com/89/) [![](http://feeds.wordpress.com/1.0/facebook/semweb4u.wordpress.com/89/)](http://feeds.wordpress.com/1.0/gofacebook/semweb4u.wordpress.com/89/) [![](http://feeds.wordpress.com/1.0/twitter/semweb4u.wordpress.com/89/)](http://feeds.wordpress.com/1.0/gotwitter/semweb4u.wordpress.com/89/) [![](http://feeds.wordpress.com/1.0/stumble/semweb4u.wordpress.com/89/)](http://feeds.wordpress.com/1.0/gostumble/semweb4u.wordpress.com/89/) [![](http://feeds.wordpress.com/1.0/digg/semweb4u.wordpress.com/89/)](http://feeds.wordpress.com/1.0/godigg/semweb4u.wordpress.com/89/) [![](http://feeds.wordpress.com/1.0/reddit/semweb4u.wordpress.com/89/)](http://feeds.wordpress.com/1.0/goreddit/semweb4u.wordpress.com/89/) ![](http://stats.wordpress.com/b.gif?host=semweb4u.wordpress.com&blog=18410093&post=89&subd=semweb4u&ref=&feed=1)
