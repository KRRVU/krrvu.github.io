---
layout: post
title: "Update: Provenance Reconstruction"
date: "2012-11-07"
categories: 
  - "collaboration"
  - "computer-science"
  - "large-scale"
  - "semantic-web"
  - "vu-university-amsterdam"
---

Source: [Data2Semantics](http://www.data2semantics.org/feed/)

Work package 5 of Data2Semantics focuses on the **reconstruction** of **[provenance](http://en.wikipedia.org/wiki/Provenance "Provenance") [information](http://en.wikipedia.org/wiki/Information "Information")**. Provenance is a hot topic in many domains, at it is believed that accurate provenance information can benefit measures of trust and quality. In science, this is certainly true. Provenance information in the form of [citations](http://en.wikipedia.org/wiki/Citation "Citation") is a centuries old practice. However, this is not enough:

- What **[data](http://en.wikipedia.org/wiki/Data "Data")** is a scientific conclusion based on?
- How was that data **gathered**?
- Was the data **altered** in the process?
- Did the authors **cite** all sources?
- What **part** of the cited paper is used in the article?

Detailed provenance of [scientific articles](http://en.wikipedia.org/wiki/Scientific_literature "Scientific literature"), presentations, data and images is often missing. Data2Semantics investigates the possibilities for **reconstructing** provenance information.

Over the past year, we have implemented a pipeline for provenance reconstruction (see picture), that is based on four steps: **preprocessing, hypotheses generation, hypotheses pruning, aggragation and ranking.** Each of these steps perform multiple analyses on a document that can be run in parallel.

![](images/provenance-pipeline.png)

Our first results, running this pipeline on a [Dropbox](http://www.dropbox.com "Dropbox") folder (including version history), are encouraging. We achieve an [F-score](http://en.wikipedia.org/wiki/F1_score "F1 score") of 0.7  when we compare **generated** dependency relations to manually specified ones (our gold standard).

Sara Magliacane has a paper accepted at the ISWC 2012 Doctoral Consortium, where she explains her approach and methodology.

[![Enhanced by Zemanta](http://img.zemanta.com/zemified_e.png?x-id=62e751c0-f56e-48f0-bc3e-70d46e54f3ce)](http://www.zemanta.com/?px "Enhanced by Zemanta")
