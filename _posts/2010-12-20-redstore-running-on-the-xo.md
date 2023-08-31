---
layout: post
title: "RedStore running on the XO"
date: "2010-12-20"
categories: 
  - "science-blogging"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Semantic Web world for you](http://semweb4u.wordpress.com/feed/)

A few days ago, I posted about SemanticXO and how you will see how to install a TripleStore on your XO. Here are the steps to follow to compile&install RedStore on the XO, put some triples in it and issue some queries. The following has been tested with an XO-1 running the software 10.1.3 and a MacBookPro running [ArchLinux x64](http://www.archlinux.org "ArchLinux") (it’s not so easy to compile directly on the XO, that’s why you will need a secondary machine). All the scripts are available [here](https://github.com/cgueret/SemanticXO "SemanticXO on GitHub").

### Installation of RedStore

RedStore depends on some external libraries that are not yet packaged for Fedora11, which is used as a base for the operating system of the XO. The script [build\_restore.sh](https://github.com/cgueret/SemanticXO/blob/master/build_redstore.sh "Script to compile redstore") will download and compile all the necessary stuff. You may however need to install external dependencies on your system, such as libxml. That script only takes care of the things [redstore](http://www.aelius.com/njh/redstore/ "RedStore") directly depends on, namely raptor2, rasqal and redland (all available [here](http://librdf.org/)). Here is the full list of commands to issue:

mkdir /tmp/xo
cd /tmp/xo
wget --no-check-certificate https://github.com/cgueret/SemanticXO/raw/master/build\_redstore.sh
sh build\_restore.sh

Once done, you will get four files to copy on the XO and if you don’t, you can also download this [pre-compiled package](https://github.com/cgueret/SemanticXO/raw/master/redstore-for-xo.tar.gz). These files shall be put all together somewhere, for instance “/opt/redstore”. Note that all the data redstore needs will be put into that same directory. In plus of these 4 files, you’ll need a wrapper script and an init scripts. Both are available on the source code repository. So, here what to do on the XO, as root (replacing “cgueret@192.168.1.105″ by the login/IP accurate for you) :

mkdir /opt/redstore
scp cgueret@192.168.1.105:/tmp/xo/libraptor2.so.0 .
scp cgueret@192.168.1.105:/tmp/xo/librasqal.so.2 .
scp cgueret@192.168.1.105:/tmp/xo/librdf.so.0 .
scp cgueret@192.168.1.105:/tmp/xo/restored .
wget --no-check-certificate https://github.com/cgueret/SemanticXO/raw/master/wrapper.sh
chmod +x wrapper.sh
cd /etc/init.d
wget --no-check-certificate https://github.com/cgueret/SemanticXO/raw/master/redstoredaemon
chmod +x redstoredaemon
chkconfig --add redstoredaemon

Then you can reboot your XO and enjoy the triplestore through its http frontend, available on the port 8080 ![:)](images/icon_smile.gif)

### Loading some triples

Now that the triple store is running, it’s time to add some triples. The [SP2Bench](http://dbis.informatik.uni-freiburg.de/index.php?project=SP2B "Homepage of SP2Bench") benchmark comes with a tool (sp2b\_gen) to generate any number of triples. To begin with, you can generate 50000 triples. That should be about of the maximum amount of triples an XO will have to deal with later on when the activities will store data in it. Here is what to do, with “192.168.1.104″ being the IP of the XO:

sp2b\_gen -t 50000
rapper -i guess -o rdfxml sp2b.n3 > sp2b.rdf
curl -T sp2b.rdf 'http://192.168.1.104:8080/data/http://example.com/data'

It takes about 43 minutes to upload these 50k triples which gives an average of **53 milliseconds per triple** or **19 triples per second**. That’s not fast but should be enough to have an API allowing to store a bunch triples with an acceptable response time. The data takes 4Mo of disk space on the XO for an initial RDF file of about 9.8Mo.

### Issue some queries

The SP2Bench benchmark comes with a generator for the triples and a set of 17 SPARQL queries expressed over this data. The queries are of changing complexity in order to benchmark different triple stores. Unfortunately, 9 of them where to complex for RedStore on the XO, with these 50k triples. These queries where not solved, even after being executed over a full night! The 8 remaining queries are solved without much problems, as long as you have enough time to wait for the answer:

| Query file | Execution time |
| --- | --- |
| q1.sparql | 14229.4 ms |
| q2.sparql | 44189.2 ms |
| q3a.sparql | 21506.8 ms |
| q3b.sparql | 19498.4 ms |
| q3c.sparql | 19663.9 ms |
| q10.sparql | 3940.6 ms |
| q11.sparql | 4685.2 ms |
| q12c.sparql | 3539.6 ms |

The queries have been executed using the “sparql-query” command line client that way:

cat q2.sparql | sparql-query http://192.168.1.104:8080/sparql -t -p -n

The long delay can sounds as a bad news but it must be noted that this was with 50k triples and with queries designed to be tricky in order to test triple store capabilities. Considering a normal usage with fewer triples and more standard queries, we can expect things to go better.

  
[![](http://feeds.wordpress.com/1.0/comments/semweb4u.wordpress.com/21/)](http://feeds.wordpress.com/1.0/gocomments/semweb4u.wordpress.com/21/) [![](http://feeds.wordpress.com/1.0/delicious/semweb4u.wordpress.com/21/)](http://feeds.wordpress.com/1.0/godelicious/semweb4u.wordpress.com/21/) [![](http://feeds.wordpress.com/1.0/facebook/semweb4u.wordpress.com/21/)](http://feeds.wordpress.com/1.0/gofacebook/semweb4u.wordpress.com/21/) [![](http://feeds.wordpress.com/1.0/twitter/semweb4u.wordpress.com/21/)](http://feeds.wordpress.com/1.0/gotwitter/semweb4u.wordpress.com/21/) [![](http://feeds.wordpress.com/1.0/stumble/semweb4u.wordpress.com/21/)](http://feeds.wordpress.com/1.0/gostumble/semweb4u.wordpress.com/21/) [![](http://feeds.wordpress.com/1.0/digg/semweb4u.wordpress.com/21/)](http://feeds.wordpress.com/1.0/godigg/semweb4u.wordpress.com/21/) [![](http://feeds.wordpress.com/1.0/reddit/semweb4u.wordpress.com/21/)](http://feeds.wordpress.com/1.0/goreddit/semweb4u.wordpress.com/21/) ![](http://stats.wordpress.com/b.gif?host=semweb4u.wordpress.com&blog=18410093&post=21&subd=semweb4u&ref=&feed=1)
