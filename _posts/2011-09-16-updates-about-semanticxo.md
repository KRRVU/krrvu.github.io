---
title: "Updates about SemanticXO"
date: "2011-09-16"
categories: 
  - "science-blogging"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Semantic Web world for you](http://semweb4u.wordpress.com/feed/)

With the last post about SemanticXO dating back from April, it’s time for an update, isn’t it? ![;-)](images/icon_wink.gif)

A lot of things happened since April. First, a paper about the project was accepted for presentation at the [First International Conference on e-Technologies and Networks for Development (ICeND2011)](http://www.sdiwc.net/tn/ "The First International Conference on e-Technologies and Networks for Development (ICeND2011)"). Then, I spoke about the project during the [symposium](http://www.networkinstitute.nl/symposium "NI symposium") of the [Network Institute](http://www.networkinstitute.nl/ "NI") as well as during the [SugarCamp #2](http://fr.amiando.com/olpcfrance-sugarcamp2011.html "SugarCamp#2"). Lastly, a first release of a [triple-store powered Journal](http://git.sugarlabs.org/~cgueret/sugar-datastore/semanticxo-mainline "Gte the source code") is now available for testing.

## Publication

The paper entitled “SemanticXO : connecting the XO with the World’s largest information network ” is available from [Mendeley](http://mnd.ly/rjPZ3C "SemanticXO : connecting the XO with the World's largest information network"). It explains what the goal of the project is and then report on some performance assessement and a first test activity. Most of the information contained has actually been blogged before on this blog (_c.f._ [there](http://wp.me/p1ffiZ-l "RedStore running on the XO") and [there](http://wp.me/p1ffiZ-1H "Clustering activity for the XO")) but if you want a global overview of the project, this paper is still worth a read. The conference in itself was very nice and I did some networking. I came back with a lot of business card and the hope of keeping in touch with the people I met there. The slides from the presentation are available from [SlideShare](http://www.slideshare.net/cgueret/semanticxo-connecting-the-xo-with-the-worlds-largest-information-network "see the presentation on slideshare")

## Presentations

[![](http://semweb4u.files.wordpress.com/2011/09/poster.png?w=130&h=185)](http://semweb4u.files.wordpress.com/2011/09/poster.png)The Network Institute of [Amsterdam](http://maps.google.com/maps?ll=52.3730555556,4.89222222222&spn=0.1,0.1&q=52.3730555556,4.89222222222%20%28Amsterdam%29&t=h "Amsterdam") organised on May 10 the Network Institute organized a one-day symposium to strengthen the ties between its members and to stimulate further collaboration. This institute is a long-term collaboration between groups from the Department of Computer Science, the Department of Mathematics, the Faculty of Social Sciences and the Faculty of Economics and Business Administration. I presented a [poster](http://www.mendeley.com/c/3885380991/p/18928/gueret-2011-semanticxo/ "Get the poster") about SemanticXO and an [abstract](http://mnd.ly/oXuxW3) went into the proceedings of the event.

More recently, I spent the 10 and the 11 of September at [Paris](http://www.paris.fr "Paris") for the Sugar Camp #2 organised by [OLPC France](http://olpc-france.org). Bastien managed me a bit of time on Sunday afternoon to re-do the presentation from ICeND2011 (thanks again for that!) and get some feedback. This was a very well organised event held at a cool location (“[La cité des sciences](http://www.cite-sciences.fr)“), it was also the first time I met so many other people working on Sugar and I could finally put some faces on the name I saw so many time on the mailing lists and on the GIT logs ![:)](images/icon_smile.gif)

## First SemanticXO prototype

The project developement effort is split in 3 parts: a common layer hidding the complexity of SPARQL, a new implementation of the journal datastore and the coding of diverse activities making use of the new semantic capabilities. All three are going more or less in parallel, at different speed, as, for instance, the work on activities direct what the common layer will contain. I’ve focused my efforts on the journal datastore to get something ready to test. It’s a very first prototype that has been coded starting with the genuine datastore 0.92 and replacing the part in charge of the metadata. The code taking care of the files remains the same. This new datastore is available from [Gitorious](http://git.sugarlabs.org/~cgueret/sugar-datastore/semanticxo-mainline) but because installing the triple store and replacing the journal is a tricky manual process, I bundled all of that ![;-)](images/icon_wink.gif)

### Installation

The installation bundle consists of two files, a “[semanticxo.tgz](https://github.com/cgueret/SemanticXO/raw/master/patch_my_xo/semanticxo.tgz)” and a script “[patch-my-xo.sh](https://raw.github.com/cgueret/SemanticXO/master/patch_my_xo/patch-my-xo.sh)“. To install SemanticXO, you need to download the two and put them in the same location somewhere on your machine and then type (as root):

sh ./patch-my-xo.sh setup

This will install a triple store, add it to the daemons to start at boot time and replace the default journal by one using the triple store. Be careful to have backups if needed as this will remove all the content previously stored in the journal! Once the script has been executed, reboot the machine to start using the new software.

The bundle has been tested on an XO-1 running the software release 11.2.0 but it should work on any software release on both the XO-1 and XO-1.5. This bundle won’t work on the 1.75 has it contains a binary (the triple store) not compiled for ARM.

### What now?

Now that you have the thing installed, open the browser and go to “http://127.0.0.1:8080″. You will see the web interface of the triple store which allows you to make some SPARQL queries and see which named graphs are stored. If you are not fluent in SPARQL, the named graph interface is the most interesting part to play with. Every entry in the journal gets its own named graph, after having populated the journal with some entries you will see this list of named graphs growing. Click on one of them and the content of the journal entry will be displayed. Note that this web interface is also accessible from any other machine on the same network as the XO. This yields new opportunities in terms of backup and information gathering: a teacher can query the journal of any XO directly from a school server, or an other XO.

### Removing

The patch script comes with an install function if you want to revert the XO to its original setup. To use it, simply type (as root):

sh ./patch-my-xo.sh remove

and then reboot the machine.

  
[![](http://feeds.wordpress.com/1.0/comments/semweb4u.wordpress.com/204/)](http://feeds.wordpress.com/1.0/gocomments/semweb4u.wordpress.com/204/) [![](http://feeds.wordpress.com/1.0/delicious/semweb4u.wordpress.com/204/)](http://feeds.wordpress.com/1.0/godelicious/semweb4u.wordpress.com/204/) [![](http://feeds.wordpress.com/1.0/facebook/semweb4u.wordpress.com/204/)](http://feeds.wordpress.com/1.0/gofacebook/semweb4u.wordpress.com/204/) [![](http://feeds.wordpress.com/1.0/twitter/semweb4u.wordpress.com/204/)](http://feeds.wordpress.com/1.0/gotwitter/semweb4u.wordpress.com/204/) [![](http://feeds.wordpress.com/1.0/stumble/semweb4u.wordpress.com/204/)](http://feeds.wordpress.com/1.0/gostumble/semweb4u.wordpress.com/204/) [![](http://feeds.wordpress.com/1.0/digg/semweb4u.wordpress.com/204/)](http://feeds.wordpress.com/1.0/godigg/semweb4u.wordpress.com/204/) [![](http://feeds.wordpress.com/1.0/reddit/semweb4u.wordpress.com/204/)](http://feeds.wordpress.com/1.0/goreddit/semweb4u.wordpress.com/204/) ![](http://stats.wordpress.com/b.gif?host=semweb4u.wordpress.com&blog=18410093&post=204&subd=semweb4u&ref=&feed=1)
