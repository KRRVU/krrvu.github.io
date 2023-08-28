---
title: "Is data sharing the privilege of a few?"
date: "2011-10-27"
categories: 
  - "science-blogging"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Semantic Web world for you](http://semweb4u.wordpress.com/feed/)

Over the last couple of years, we have engineered a fantastic data sharing technology based on open standards from the W3C: [Linked Data](http://en.wikipedia.org/wiki/Linked_Data "Linked Data"). Using Linked Data, it is possible to express some knowledge with a set of facts and connect the facts together to build a network. Having such networked data openly accessible is a source of economical and societal benefits. It enables sharing data in an unambiguous, open and standard way, just as the [Web](http://en.wikipedia.org/wiki/World_Wide_Web "World Wide Web") enabled document sharing. Yet, the way we designed it deprives the majority of the World’s population from using it.

## Doing “Web-less” Linked Data?

The problem may lay in the fact that Linked Data is based on Web technologies, or in the fact that Linked Data have been designed and engineered by individuals having an easy access to the Web, or maybe a combination of both aspects. Nowadays, Linked Data rhymes with having a Cloud hosted data storing services, a set of (web-based) applications to interact with this service and the infrastructure of the Web. As a result, if you don’t have access to this Web infrastructure, you can not use Linked Data. Which is a pity, because an estimated 4.5B persons don’t have access to it for various reasons (lack of infrastructure, cost of access, literacy issues, …). Wouldn’t it be possible to adjust our design choices to ensure they could also benefit from Linked Data, even if they don’t have the Web? The answer is yes, and the best news is that it wouldn’t be that hard either. But for it to happen, we need to adapt both our mindset and our technologies.

## Changing our mindset

We have tendency to think that any data sharing platform is a combination of a cloud based data store, some client applications to access the data and form to feed new data into the system. This is not always applicable as central hosting of data may not be possible, or its access from client applications may not be guaranteed. We should also think of the part of the World which is illiterate and for which Linked Data, and the Web, are not accessible. In short, we need to think de-centralised, small and vocal in order to widen the access to Linked Data.

### Think de-centralised

Star-shaped networks can be hard to deploy. They imply setting a central producer of resource somewhere and connecting all the clients to it. Electricity networks have already found a better alternative: the microgrids. Microgrids are made of small networks of producers/consumers (the “prosumers”) of electricity that locally manage the electricity needs. We could, and should, copy on this approach to manage local data production and consumption. For example, think of a decentralised [DBpedia](http://dbpedia.org "DBpedia") whose content would be made of the aggregation of several data sources producing part of the content – most likely, the content that is locally relevant to them.

### Think small

Big servers require more energy and more cooling. They usually end up racked into big cabinets that in turn are packed into cooled data centers. These data centers needs to be big in order to cope with the scale issues. Thinking decentralised allow to think small, and we need to think small to provide alternatives to having data centers where these are not available. As the content production and creation goes decentralised, several small servers can be used. To continue with the analogy with microgrids, we can name these small servers taking care of locally relevant content “micro-servers”.

### Think vocal

Unfortunately, not everyone can read and type. In some African areas, knowledge is shared using vocal channels (mobile phone, meetings, …) because there is no other alternative. Getting access to knowledge exchanged that way can not be done using form based data acquisition systems. We need to think of exploiting vocal conversation through [Text To Speech](http://en.wikipedia.org/wiki/Speech_synthesis "Speech synthesis") (TTS) and [Automatic Speech Recognition](http://en.wikipedia.org/wiki/Speech_recognition "Speech recognition") (ASR) rather than staying focused on forms.

## Changing our technologies

Changing the mindsets is not enough, if we aim at stripping down the Web from Linked Data we also need to pay attention to our technologies and adapt them. In particular, there are 5 upcoming challenges that can be phrased as research questions:

1. **Dereferencability**: How do you get a route to the data if you want to avoid using the routing system provided by the Web? For instance, how do you dereference an host-name based [URIs](http://en.wikipedia.org/wiki/Uniform_Resource_Identifier "Uniform Resource Identifier") if you don’t have access to the DNS network?
2. **Consistency**: In a decentralised setting where several publishers produce part of a common data set, how do you ensure URIs are re-used and non colliding? There are chances that two different producers would use the same URI to describe different things.
3. **Reliability**: Unlike centrally hosted data servers, micro-servers can not be asked to provide a 99% availability. They may go on and off unexpectedly. First thing to know is whether that’s an issue or not. The second is, if we should ensure their data remains available, how do we achieve this?
4. **Security**: That’s also related to having a swarm of microservers serving a particular dataset. If any microserver can produce a chunk of that dataset, how do you avoid having a spammer getting in and starting producing falsified content? If we want to avoid centralized networks, authority based solution such as in [Public Key Infrastructure](http://en.wikipedia.org/wiki/Public_key_infrastructure "Public key infrastructure") (PKI) is not an option. We need to find decentralised authentication mechanisms.
5. **Accessibility**: How do we make Linked Data accessible to those that are illiterate? As highlighted earlier, not everyone can read an write but illiterate persons can still talk. We need to take more of the vocal technologies into account in order to make Linked Data accessible to them. We can also investigate graphical based data acquisition techniques with visual representations of information.

## More about this

This is a presentation that [Stefan Schlobach](http://nl.linkedin.com/pub/stefan-schlobach/4/4b9/210) gave at [ISWC2011](http://iswc2011.semanticweb.org/) on this topic:

You are also invited to read the associated paper [“Is data sharing the privilege of a few ? Bringing Linked Data to those without the Web”](http://www.mendeley.com/c/4269436733/p/18928/gueret-2011-is-data-sharing-the-privilege-of-a-few--bringing-linked-data-to-those-without-the-web/) and check out two projects working on the mentioned challenges: [SemanticXO](http://semweb4u.wordpress.com/category/semanticxo/) and [Voices](http://mvoices.eu/).

  
[![](http://feeds.wordpress.com/1.0/comments/semweb4u.wordpress.com/275/)](http://feeds.wordpress.com/1.0/gocomments/semweb4u.wordpress.com/275/) [![](http://feeds.wordpress.com/1.0/delicious/semweb4u.wordpress.com/275/)](http://feeds.wordpress.com/1.0/godelicious/semweb4u.wordpress.com/275/) [![](http://feeds.wordpress.com/1.0/facebook/semweb4u.wordpress.com/275/)](http://feeds.wordpress.com/1.0/gofacebook/semweb4u.wordpress.com/275/) [![](http://feeds.wordpress.com/1.0/twitter/semweb4u.wordpress.com/275/)](http://feeds.wordpress.com/1.0/gotwitter/semweb4u.wordpress.com/275/) [![](http://feeds.wordpress.com/1.0/stumble/semweb4u.wordpress.com/275/)](http://feeds.wordpress.com/1.0/gostumble/semweb4u.wordpress.com/275/) [![](http://feeds.wordpress.com/1.0/digg/semweb4u.wordpress.com/275/)](http://feeds.wordpress.com/1.0/godigg/semweb4u.wordpress.com/275/) [![](http://feeds.wordpress.com/1.0/reddit/semweb4u.wordpress.com/275/)](http://feeds.wordpress.com/1.0/goreddit/semweb4u.wordpress.com/275/) ![](http://stats.wordpress.com/b.gif?host=semweb4u.wordpress.com&blog=18410093&post=275&subd=semweb4u&ref=&feed=1)
