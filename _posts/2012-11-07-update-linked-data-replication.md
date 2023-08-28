---
title: "Update: Linked Data Replication"
date: "2012-11-07"
categories: 
  - "collaboration"
  - "computer-science"
  - "large-scale"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Data2Semantics](http://www.data2semantics.org/feed/)

![](images/sheep.png)

What if Dolly was only a partial replica?

Work package 3 of Data2Semantics centers around the problem of **ranking** [Linked Data](http://en.wikipedia.org/wiki/Linked_Data "Linked Data").

Over the past year, we have identified **partial replication** as a core [use case](http://en.wikipedia.org/wiki/Use_case "Use case") for ranking.

The amount of linked data is rapidly growing, especially in the life sciences and medical domain. At the same time, this data is increasingly dynamic: information is added and removed at a much more granular level than before. Where until recently the Linked Data cloud grew one [dataset](http://en.wikipedia.org/wiki/Data_set "Data set") at a time, these datasets are now \`live\`, and can change as fast as every minute.

For most Linked Data applications, the cloud, but also the individual datasets are too big too handle. In some cases, as in e.g. the [clinical decision support](http://en.wikipedia.org/wiki/Clinical_decision_support_system "Clinical decision support system") use case of Data2Semantics, one may need to support e.g. offline access from a tablet computer. Another use case is where [semantic web](http://en.wikipedia.org/wiki/Semantic_Web "Semantic Web") development requires a testing environment: running your experiment on a full dataset will just take too much time.

The question then is, how can we make a proper **selection** of the original dataset that is sufficiently representative for the application purpose, while at the same time ensuring timely **synchronisation** with the original dataset whenever updates take place.

A first version of the partial replication implementation was integrated in the latest version of the [Hubble CDS Prototype](http://aers.data2semantics.org/hubble).

Laurens Rietveld has an accepted paper at the ISWC 2012 doctoral consortium, where he explains his research approach and methodology. You can find the paper at [http://www.mendeley.com/research/replication-for-linked-data/](http://www.mendeley.com/research/replication-for-linked-data/)

[![Enhanced by Zemanta](http://img.zemanta.com/zemified_e.png?x-id=efed91bc-f5fe-416e-b381-edf5c6dc944e)](http://www.zemanta.com/?px "Enhanced by Zemanta")
