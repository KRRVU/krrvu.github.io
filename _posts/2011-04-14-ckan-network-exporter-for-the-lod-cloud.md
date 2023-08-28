---
title: "CKAN->network exporter for the LOD Cloud"
date: "2011-04-14"
categories: 
  - "science-blogging"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Semantic Web world for you](http://semweb4u.wordpress.com/feed/)

[![](http://semweb4u.files.wordpress.com/2011/04/cloud-14-04-2011.png?w=211&h=300 "cloud-14-04-2011")](http://semweb4u.files.wordpress.com/2011/04/cloud-14-04-2011.png)

The LOD cloud as rendered by Gephi

One year ago, [we posted on the LarkC blog a first network model of the LOD cloud](http://blog.larkc.eu/?p=1941 "LOD cloud shows surprisingly lumpy structure"). N[etwork analysis](http://en.wikipedia.org/wiki/Network_analysis_%28electrical_circuits%29 "Network analysis (electrical circuits)") software can highlight some aspects of the cloud that are not directly visible otherwise. In particular, the presence of dense sub-groups and several hubs – whereas in the [classical picture](http://richard.cyganiak.de/2007/10/lod/lod-datasets_2010-09-22_colored.html), [DBPedia](http://en.wikipedia.org/wiki/DBpedia "DBpedia") is easily perceived as being the only hub.

Computing network measures such as centralities, [clustering coefficient](http://en.wikipedia.org/wiki/Clustering_coefficient "Clustering coefficient") or the [average path length](http://en.wikipedia.org/wiki/Average_path_length "Average path length") can reveal much more about the content of a graph and the interplay of its nodes. As shown since that blog post, these information can be used to appreciate the evolution of the Web of Data and devise actions to improve it (see the [WoD analysis](http://linkeddata.few.vu.nl/wod_analysis/) page for more information about our research on this topic). Unfortunately, the picture provided by Richard and Anja on [lod-cloud.net](http://lod-cloud.net) can not be fitted directly into a network analysis software which expects a .net or CSVs files instead. Fortunately, thanks to the very nice [API](http://en.wikipedia.org/wiki/Application_programming_interface "Application programming interface") of [CKAN.net](http://ckan.net) it is easy to write a script generating such files. We made such a script and thought it would be a good idea to share it ![:-)](images/icon_smile.gif)

The script is [hosted on GitHub](https://github.com/cgueret/CKAN-network-builder/blob/master/main.py). It produces a “.net” file according to the format of [Pajek](http://vlado.fmf.uni-lj.si/pub/networks/pajek/) and two [CSV](http://en.wikipedia.org/wiki/Comma-separated_values "Comma-separated values") files, one for the nodes and one for the edges. These CSV can then easily be imported into [Gephi](http://gephi.org/), for instance, or any other software of your choice. We also made a dump of the cloud as of today and [packaged the resulting files](https://github.com/downloads/cgueret/CKAN-network-builder/cloud_network_14-04-11.zip).

Have fun analysing the graph and let us know if you find something interesting ![;-)](images/icon_wink.gif)

  
[![](http://feeds.wordpress.com/1.0/comments/semweb4u.wordpress.com/184/)](http://feeds.wordpress.com/1.0/gocomments/semweb4u.wordpress.com/184/) [![](http://feeds.wordpress.com/1.0/delicious/semweb4u.wordpress.com/184/)](http://feeds.wordpress.com/1.0/godelicious/semweb4u.wordpress.com/184/) [![](http://feeds.wordpress.com/1.0/facebook/semweb4u.wordpress.com/184/)](http://feeds.wordpress.com/1.0/gofacebook/semweb4u.wordpress.com/184/) [![](http://feeds.wordpress.com/1.0/twitter/semweb4u.wordpress.com/184/)](http://feeds.wordpress.com/1.0/gotwitter/semweb4u.wordpress.com/184/) [![](http://feeds.wordpress.com/1.0/stumble/semweb4u.wordpress.com/184/)](http://feeds.wordpress.com/1.0/gostumble/semweb4u.wordpress.com/184/) [![](http://feeds.wordpress.com/1.0/digg/semweb4u.wordpress.com/184/)](http://feeds.wordpress.com/1.0/godigg/semweb4u.wordpress.com/184/) [![](http://feeds.wordpress.com/1.0/reddit/semweb4u.wordpress.com/184/)](http://feeds.wordpress.com/1.0/goreddit/semweb4u.wordpress.com/184/) ![](http://stats.wordpress.com/b.gif?host=semweb4u.wordpress.com&blog=18410093&post=184&subd=semweb4u&ref=&feed=1)
