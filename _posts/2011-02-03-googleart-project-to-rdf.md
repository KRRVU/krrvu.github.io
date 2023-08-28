---
title: "GoogleArt project to RDF"
date: "2011-02-03"
categories: 
  - "science-blogging"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Semantic Web world for you](http://semweb4u.wordpress.com/feed/)

[![LOD Around The Clock (LATC) logo](http://semweb4u.files.wordpress.com/2011/01/logo-latc.png?w=112&h=26 "latc")](http://semweb4u.files.wordpress.com/2011/01/logo-latc.png)Google [recently announced](http://googleblog.blogspot.com/2011/02/explore-museums-and-great-works-of-art.html) a new project, named the Google Art, which give access to paints from around the world in very high definition. It also provides some information related to these paintings.This is a very cool service but the data is not provided in a machine-friendly way. So we thought it would be nice to have a wrapper exporting in [RDF](http://en.wikipedia.org/wiki/Resource_Description_Framework "Resource Description Framework") so that this data could be more easily consumed by any semantic-aware application.

The [GoogleArt2RDF wrapper](http://linkeddata.few.vu.nl/googleart/) offers such a wrapping service for any painting made available through GoogleArt. In order to use it, just copy the name of the artwork and paste it after “http://linkeddata.few.vu.nl/googleart/”. For instance, change “[http://www.googleartproject.com/museums/rijks/night-watch](http://www.googleartproject.com/museums/rijks/night-watch)” into “[http://linkeddata.few.vu.nl/googleart/museums/rijks/night-watch](http://linkeddata.few.vu.nl/googleart/museums/rijks/night-watch)“.

The data is expressed using essentially the [FOAF](http://www.foaf-project.org/ "FOAF") and [Dublin Core](http://en.wikipedia.org/wiki/Dublin_Core "Dublin Core") ontologies. When possible, the resources are linked to DBPedia for the author of the painting and the medium used (oil on canvas, etc). This is a first version of the system which does not yet export all the data from Google, comments and suggestions on how to improve it are much welcome!

###### Related Articles

- [Google Art Project brings world’s best museums into your home](http://www.zdnet.com/blog/gadgetreviews/google-art-project-brings-worlds-best-museums-into-your-home/21962) (zdnet.com)
- [We Are All Google’s Art Project](http://greg.org/archive/2011/02/01/we_are_all_googles_art_project.html) (greg.org)

  
[![](http://feeds.wordpress.com/1.0/comments/semweb4u.wordpress.com/83/)](http://feeds.wordpress.com/1.0/gocomments/semweb4u.wordpress.com/83/) [![](http://feeds.wordpress.com/1.0/delicious/semweb4u.wordpress.com/83/)](http://feeds.wordpress.com/1.0/godelicious/semweb4u.wordpress.com/83/) [![](http://feeds.wordpress.com/1.0/facebook/semweb4u.wordpress.com/83/)](http://feeds.wordpress.com/1.0/gofacebook/semweb4u.wordpress.com/83/) [![](http://feeds.wordpress.com/1.0/twitter/semweb4u.wordpress.com/83/)](http://feeds.wordpress.com/1.0/gotwitter/semweb4u.wordpress.com/83/) [![](http://feeds.wordpress.com/1.0/stumble/semweb4u.wordpress.com/83/)](http://feeds.wordpress.com/1.0/gostumble/semweb4u.wordpress.com/83/) [![](http://feeds.wordpress.com/1.0/digg/semweb4u.wordpress.com/83/)](http://feeds.wordpress.com/1.0/godigg/semweb4u.wordpress.com/83/) [![](http://feeds.wordpress.com/1.0/reddit/semweb4u.wordpress.com/83/)](http://feeds.wordpress.com/1.0/goreddit/semweb4u.wordpress.com/83/) ![](http://stats.wordpress.com/b.gif?host=semweb4u.wordpress.com&blog=18410093&post=83&subd=semweb4u&ref=&feed=1)
