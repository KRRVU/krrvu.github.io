---
layout: post
title: "On the use of HTTP URIs and the archiving of Linked Data"
date: "2013-10-15"
categories: 
  - "semantic-web"
  - "semantic-web-meeting"
tags: 
  - "archiving"
  - "linked-data"
  - "semantic-web-2"
  - "uri"
---

O**[![](images/Archives_Fotolia_27307847_©-Christophe-Fouquin-Fotolia.com_1-1024x682.jpg "Archive of books")](http://krr.cs.vu.nl/wp-content/uploads/2013/10/Archives_Fotolia_27307847_©-Christophe-Fouquin-Fotolia.com_1.jpg)**n Monday the 7th of October the Knowledge, Reasoning and Representation and the Web&Media research groups of the Free University Amsterdam joined for their biweekly Semantic Web (SW) meeting. The topic was on the purpose of using HTTP URIs for denoting SW resources and on the implications for archiving Linked Data (LD).

An important aspect of archiving LD is that in archiving the LD is decoupled from its native Web environment (thus the title of the talk). The two most important Web-based properties that are lost in the process are (1) authority and (2) dereferenceability. We first discussed the relevance of both these properties.

**Authority**

In RFC 3986 _Uniform Resource Identifier (URI): Generic Syntax_ [\[1\]](https://tools.ietf.org/html/rfc3986#section-3.2) the authority of an URI/IRI is defined as follows:

> Many URI schemes include a hierarchical element for a naming authority so that governance of the name space defined by the remainder of the URI is delegated to that authority \[...\].

**Authorities & identity**

In the discussion on the use of authorities the ambiguity of the identity relation was brought up. Within-namespace identity defines an equivalence relation on the data, but between-namespace identity is not even symmetric.

This ties into one of the fundamental principles of RDF, namely that "Anyone can make statements about any resource" [\[2\]](http://www.w3.org/TR/2003/PR-rdf-concepts-20031215/#section-anyone)). But even though anyone can assert a triple, the fact that a triple is hosted at the same authority that is the namespace of the URI that appears in the subject position of the triple is indeed significant.

E.g. if a triple at `http://dbpedia.org` states that `dbpedia:George_H._W._Bush` was a US president and another triple hosted at some arbitrary Web location states that `dbpedia:George_H._W._Bush` was a charlatan, then the former triple is relatively easy to find (every dereference of `dbpedia:George_H._W._Bush` will return it), whereas the latter may be very difficult to find. This has a parallel on the traditional Web, where a crawler can easily identify outgoing links, but back-links are more difficult to find.[\[3\]](http://badfactor.com/how-to-get-backlinks-the-ultimate-guide/)

This means that non-authoritative triples that are too opinionated are given less attention. Another way of formulating this is: alternative views regarding a topic are given less attention.

**Dereferencability**

From a show of hands at the meeting it became apparent that many SW researches actually use dereferenceability! Some even think it is one of the nice things of the SW. However, our research groups may not be indicative on this topic: most of the LOD appears to be not dereferenceable today.

What we did not talk too much about is whether people outside of the LD community, i.e. normal users, are using these dereferences. Surely some of the faceted browsers out there (green-background tables!, e.g. [\[4\]](http://dbpedia.org/ontology/Person)) will not entice too many users, but I may be unaware of some of the innovations that the Web&Media people have come up with in this area. ClioPatria [\[5\]](http://cliopatria.swi-prolog.org/home) for instance provides a standard way of dereferencing and loading linked data sources that are not already in the local triple store.

**Authority & dereferenceability (interaction)**

Authority and dereferenceability are intertwined in the following two ways:

1. The existence of authorities on the Web makes dereferencing possible, since the name of the resource contains the location of the authority that disseminates it.
2. Dereferencing is a way in which authority is effectuated, because it allows the view of the authority that disseminates a specific topic to be easily/standardly retrieved.

**Permanence**

A third property of the use of HTTP URIs is permanence [\[6\]](http://www.w3.org/Provider/Style/URI.html). The service behind a URI should have continuous up-time and should be available for a long period of time. Frank pointed out that the traditional Web never suffered from 404s (although this used to be a big concern for critics of the early Internet). The problem may be different on the SW since it may be harder for machine agents to recover from link rot than human agents.

**Archiving LD: 'dead' or 'alive'?**

What I got from the discussion on archiving LD is that it is basically fine to decouple LD from the Web for archiving purposes and that:

1. dereferenceability is not that important in the case of archived data since it is considered 'dead' (i.e. not actively used), and that
2. the original URI authority should be replaced by meta-data describing the authority (since triples will be stored under a different authority when archived by DANS).

It was pointed out that a potential discrepancy exists between traditional archiving and LD archiving. E.g. in the humanities curated archives are often considered the most 'alive', i.e. the most quoted, referred to, and used in active research. But storing LD decoupled from its original Web architecture may turn them into 'dead' snapshots (whereas active use will be made of the non-archived versions of the LOD).

The use of the words 'dead' and 'alive' was of course metaphorically. As [Antoine Isaac](http://www.few.vu.nl/~aisaac/) pointed out: "The very idea of an archive is that you're ready to accept a lower level of accessibility of stuff in exchange for longer-term preservation of it." Btw. Antoine is working in the Prelida project [\[7\]](http://www.prelida.eu/) one of whose purpose is to inform the LD community of Digital Preservation techniques. A very relevant project for this topic!

**Archiving: human or machine processing?**

The proponents of archived LD dumps assume that, when the data will be used at a later point in time, human agents (e.g. historians) will be needed to add context. This may conflict with the machine-processable nature of SW data, although some of the context may be stored as well using a dataset description language [\[8\]](http://www.w3.org/TR/void/).

Antoine observed that one of the reasons why the question of how many context to include in archiving LD arises since context data is so easy to obtain for it (e.g. using automated crawling methods) when compared to e.g. offline content.

**Archiving URI meaning / context**

Another interesting point is the question as to how much context needs to be stored in order for archived LD to be able to retain its original meaning. This depends on the theory of meaning one adheres to w.r.t. the SW. Memento's [\[9\]](http://mementoweb.org/depot/native/dbpedia/) approach is to archive the dereferenced content. Implicit in this approach is the assumption that the meaning of a resource can be given in a local description. We see this assumption formulated in the COOL URI Interest Group Note [\[10\]](http://www.w3.org/TR/2008/NOTE-cooluris-20081203/#semweb): "\[A dereferencing\] look-up mechanism is important to establish shared understanding of what a URI identifies."

An alternative view is that the meaning of a URI is determined by the set of inferential roles of triples in which the URI occurs.[\[11\]](http://www.iep.utm.edu/conc-rol/#SH1a) In this case all triples related to the archived triples must be stored as well in order for the resource's meanings to be (fully) retained.

**Archiving LD by archiving HTML pages**

Ed Summers wrote a blog post [\[12\]](http://inkdroid.org/journal/2013/09/30/preserving-linked-data/) recently in which he explains how 'traditional' Web archiving may be used for LD archiving. If RDFa or Microformats are embedded in an HTML Web page, then this data can be extracted from the stored HTML.

**Dataset availability**

**[![](images/library_of_congress_reading.jpg "library_of_congress_reading")](http://krr.cs.vu.nl/wp-content/uploads/2013/10/library_of_congress_reading.jpg)**Archiving multiple versions of a dataset is obviously very difficult. [Christophe Guéret](http://www.few.vu.nl/~cgueret/) pointed to a discussion at the open-government mailinglist regarding the US government shutdown [\[13\]](http://lists.okfn.org/pipermail/open-government/2013-October/003157.html) as an example that it is even difficult to reliably disseminate the latest version of a government-backed dataset. (On a related note, we have seen difficulties in the teaching context as well, where a remote dataset goes offline in the midst of a course in which students are querying that dataset for the applications they develop.) In cases such as the US government shutdown, important datasets may go offline overnight causing issues both for applications that depend on them and for other dataset that link to them.
