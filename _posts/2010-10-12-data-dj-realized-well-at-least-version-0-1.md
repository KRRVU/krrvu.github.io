---
layout: post
title: "Data DJ realized….well at least version 0.1"
date: "2010-10-12"
categories: 
  - "science-blogging"
  - "vu-university-amsterdam"
---

Source: [Think Links](\"http://thinklinks.wordpress.com/feed/\")

I wrote a post a while back around the [idea of Data DJs](http://thinklinks.wordpress.com/2009/11/29/data-djs/): **how do we make it as easy to mix data as it is to mix music**. This notion requires advances on several fronts from data and knowledge integration, to user interfaces, along with data provenance and semantics. Most of the research I do then somehow relates to this Data DJ’s in some form or anther.

However, I always thought I it would be fun to push the analogy as far as I could. Last Christmas, I got a DJ deck (specifically a [Numark Stealth Control](http://www.numark.com/stealthcontrol)\-fantastic name, right?) with the idea of actually using it to mix data sets. For a host of reasons, including time but also a lack of a clear vision of what an integration interface should look like, I never got past just toying around with it. However, over the past couple of weekends I found time to revisit it and develop a super alpha version of a data integration system using the deck. Here’s a video to see what I’ve done, read on to get more details.

[![](images/2.jpg)](http://thinklinks.wordpress.com/2010/10/12/data-dj-0-1/)

What really got me going was the notion that events (or who, what, when, where and why) are a perfect substrate for data integration. This is not my idea but has been something I’ve been hearing from a number of sources including from a number of people in the [VU’s Web and Media Group](http://wiki.cs.vu.nl/web-media/Main_Page) down the hall, [Raphaël Troncy](http://homepages.cwi.nl/~troncy/), and probably best summed up by [Mor Naaman](http://www.ayman-naaman.net/2010/08/30/w4-semantic-web-is-facebook/). With this as inspiration, I developed a preliminary interface around integrating/and summarizing events (well actually tweets, but hopefully this will expand to other event sources) that you saw in the video above. The components of the interface (shown in the picture below) are as follows:

[![](http://thinklinks.files.wordpress.com/2010/10/screencap.jpg?w=717&h=392 "DataDj interface")](http://thinklinks.files.wordpress.com/2010/10/screencap.jpg)

- On the top is a list of the search terms that were used to retrieve the tweets. The tweets for each search term can be hidden and unhidden.
- On the right is a list of the users (i.e. sources) who made the tweets. Each source can be filtered in and out impacting the term summary graph
- In the middle are all the tweets on the same timeline.
- On the right, is a bar graph that summarizes the most common terms across the tweets.
- Below the bar graph, is the time span of the tweets and the current time of the selected tweet.
- On the far right are hashtags that are selected by the user.

As you saw in the video it’s pretty fast to scroll through both sources and tweets. With a quick flick it’s easy to apply a filter and pretty natural to select and deselect search terms. Furthermore, we can easily delete tweets and data sources with the push of a button. There’s still much much more to be done to make this a viable user interface for the kind of data mixing task we want to support. But standing in front of the projector today scrolling through tweets, eliminating sources and seeing an overview fly-up really convinced me that this type of interaction is really suited to the data integration task. That being said any advice or comments on the interface would be greatly appreciated. In particular, suggestions for good infographics pertaining to events would be appreciated.

### Technical Details:

The interface was completely implemented using HTML5. In particular, I used the nice [ProtoVis framework](http://vis.stanford.edu/protovis/) along with JQuery and [JQuery Tools](http://flowplayer.org/tools/index.html). To get the fast updates from the deck, we use WebSockets. I have a small Java program reading midi off the deck which then acts as a socket server for WebSockets and pipes the midi signals (after translation to JSON) to the connected sockets. I’ve been using Google Chrome for development so I don’t know how it works in other browsers. To get data, we use the search interface of twitter and JSONP. In general, I was very impressed with what you can do in the browser. I felt like I wasn’t even pushing the capabilities especially since I don’t do web programming everyday.

### What’s next?

Lots! This was really just a proof of concept. There’s a bunch of directions to go in: improved graphics, better use of the decks, social interaction around integration (two djs at once!), more data sources beyond twitter, experiments on task performance, live mixing of an event…. If you have any ideas, suggestions, or comments, I’d love to hear them.

How do you want to data DJ?

  
Filed under: [data dj](http://thinklinks.wordpress.com/category/data-dj/) Tagged: [data dj](http://thinklinks.wordpress.com/tag/data-dj/), [decks](http://thinklinks.wordpress.com/tag/decks/), [infographics](http://thinklinks.wordpress.com/tag/infographics/), [mixing data](http://thinklinks.wordpress.com/tag/mixing-data/) [![](http://feeds.wordpress.com/1.0/comments/thinklinks.wordpress.com/247/)](http://feeds.wordpress.com/1.0/gocomments/thinklinks.wordpress.com/247/) [![](http://feeds.wordpress.com/1.0/delicious/thinklinks.wordpress.com/247/)](http://feeds.wordpress.com/1.0/godelicious/thinklinks.wordpress.com/247/) [![](http://feeds.wordpress.com/1.0/facebook/thinklinks.wordpress.com/247/)](http://feeds.wordpress.com/1.0/gofacebook/thinklinks.wordpress.com/247/) [![](http://feeds.wordpress.com/1.0/twitter/thinklinks.wordpress.com/247/)](http://feeds.wordpress.com/1.0/gotwitter/thinklinks.wordpress.com/247/) [![](http://feeds.wordpress.com/1.0/stumble/thinklinks.wordpress.com/247/)](http://feeds.wordpress.com/1.0/gostumble/thinklinks.wordpress.com/247/) [![](http://feeds.wordpress.com/1.0/digg/thinklinks.wordpress.com/247/)](http://feeds.wordpress.com/1.0/godigg/thinklinks.wordpress.com/247/) [![](http://feeds.wordpress.com/1.0/reddit/thinklinks.wordpress.com/247/)](http://feeds.wordpress.com/1.0/goreddit/thinklinks.wordpress.com/247/) ![](http://stats.wordpress.com/b.gif?host=thinklinks.wordpress.com&blog=5274753&post=247&subd=thinklinks&ref=&feed=1)
