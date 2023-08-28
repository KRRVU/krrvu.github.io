---
title: "Does it scale?"
date: "2011-11-02"
categories: 
  - "science-blogging"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Semantic Web world for you](http://semweb4u.wordpress.com/feed/)

Scaling is often a central question for data intensive projects, making use of [Semantic Web](http://semanticweb.org "Semantic Web") technologies or not, and SemanticXO is no exception to that. The [triple store](http://en.wikipedia.org/wiki/Triplestore "Triplestore") is used as a back end for the Journal of Sugar, which is a central component recording the usage of the different activities. This short post discusses the results found for two questions: “how many journal entries can the triple store sustain?” and “hoe much disk space is used to store the journal entries?”

Answering these questions means loading some Journal entries and measuring the read and write performances along with the disk space used. This is done by a [script](https://github.com/cgueret/SemanticXO/blob/master/performances/src/performances_test.py "Performance measuring script") which randomly generate Journal entries and insert them in the store. A text sampler and the real names of activities are used to make these entries realistic in terms of size. An example of such generated entry, serialised in [HTML](http://en.wikipedia.org/wiki/HTML "HTML"), can be seen [there](https://gist.github.com/1333351). The following graphs show the results obtained for inserting 2000 journal entries. These figures have been averaged over 10 runs, each of them starting with a freshly created store. The triple store used is called “[RedStore](http://www.aelius.com/njh/redstore/)“, it is called with an hash based [BerkleyDB](http://www.oracle.com/us/products/database/berkeley-db/index.html "Berkeley DB") backend. The test machine is an [XO-1](http://en.wikipedia.org/wiki/OLPC_XO-1 "OLPC XO-1") running the software 11.2.0.

The disk space is minimal for up to 30 entries, grows rapidly between 30 and 70 entries and continues on a linear basis from that number on. The maximum space occupied is a bit less than 100MB which is few of the 1GB of storage of the XO-1.

 [![](http://semweb4u.files.wordpress.com/2011/11/space.jpg?w=360&h=210)](http://semweb4u.files.wordpress.com/2011/11/space.jpg) 

Amount of disk space used by the triple store

The results for the read and write delay are a bit less of a good news. Write operations are constant in time and always take around 0.1 s. Getting an entry from the triple store proves to get linearly slower as the triple store gets filled. It can be noticed that for up to 600 entries, the retrieval time of an entry is below a second. This should provide a reasonable response time. However, with 2000 entries stored the retrieval time goes as high as 7 seconds ![:-(](images/icon_sad.gif)

[![](http://semweb4u.files.wordpress.com/2011/11/time.jpg?w=360&h=210)](http://semweb4u.files.wordpress.com/2011/11/time.jpg)

Read and write access time

The answer to the question we started with (“Does it scale?”) is then “yes, for up to 600 entries” considering a first generation device and the current status of the software components (SemanticXO/Redstore/…). This answers also yields new questions, among which: Are 600 entries enough for a typical usage of the XO? Is it possible to improve the software to get better results? How are the result on some more recent hardware?

I would appreciate a bit of help for answering all of these, and especially the last one. I only have an XO-1 and can not thus run my script on an XO-1.5 or XO-1.75. If you have such device and are willing to help me getting the results, please download the [package containing the performance script and the triple store](https://github.com/downloads/cgueret/SemanticXO/performances.tar.gz) and [follow the instructions for running it](https://gist.github.com/1333307). After a day of execution or so, this script will generate three [CSV](http://en.wikipedia.org/wiki/Comma-separated_values "Comma-separated values") files that I could then postprocess to get similar curves as the one showed.

###### Related articles

- [Is data sharing the privilege of a few?](http://semweb4u.wordpress.com/2011/10/27/is-data-sharing-the-privilege-of-a-few/) (semweb4u.wordpress.com)
- [Updates about SemanticXO](http://semweb4u.wordpress.com/2011/09/16/204/) (semweb4u.wordpress.com)

  
[![](http://feeds.wordpress.com/1.0/comments/semweb4u.wordpress.com/319/)](http://feeds.wordpress.com/1.0/gocomments/semweb4u.wordpress.com/319/) [![](http://feeds.wordpress.com/1.0/delicious/semweb4u.wordpress.com/319/)](http://feeds.wordpress.com/1.0/godelicious/semweb4u.wordpress.com/319/) [![](http://feeds.wordpress.com/1.0/facebook/semweb4u.wordpress.com/319/)](http://feeds.wordpress.com/1.0/gofacebook/semweb4u.wordpress.com/319/) [![](http://feeds.wordpress.com/1.0/twitter/semweb4u.wordpress.com/319/)](http://feeds.wordpress.com/1.0/gotwitter/semweb4u.wordpress.com/319/) [![](http://feeds.wordpress.com/1.0/stumble/semweb4u.wordpress.com/319/)](http://feeds.wordpress.com/1.0/gostumble/semweb4u.wordpress.com/319/) [![](http://feeds.wordpress.com/1.0/digg/semweb4u.wordpress.com/319/)](http://feeds.wordpress.com/1.0/godigg/semweb4u.wordpress.com/319/) [![](http://feeds.wordpress.com/1.0/reddit/semweb4u.wordpress.com/319/)](http://feeds.wordpress.com/1.0/goreddit/semweb4u.wordpress.com/319/) ![](http://stats.wordpress.com/b.gif?host=semweb4u.wordpress.com&blog=18410093&post=319&subd=semweb4u&ref=&feed=1)
