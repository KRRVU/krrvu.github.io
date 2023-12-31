---
layout: post
title: "TabLinker"
date: "2012-02-19"
categories: 
  - "collaboration"
  - "computer-science"
  - "large-scale"
  - "semantic-web"
  - "vu-university-amsterdam"
---

TabLinker is experimental software for converting manually annotated Microsoft Excel workbooks to the [RDF Data Cube vocabulary](http://publishing-statistical-data.googlecode.com/svn/trunk/specs/src/main/html/cube.html). It is used in the context of the [Data2Semantics](http://www.data2semantics.org/) project to investigate the use of Linked Data for humanities research ([Dutch census data](http://www.volkstellingen.nl/)produced by [DANS](http://dans.knaw.nl/)).

TabLinker was designed for converting Excel or CSV files to RDF (triplification, RDF-izing) that have a complex layout and cannot be handled by fully automatic csv2rdf scripts.

A presentation about Linked Census Data, including TabLinker is [available from SlideShare](http://www.slideshare.net/rinkehoekstra/linked-census-data).

Please consult the [Github page](http://github.com/Data2Semantics/TabLinker "TabLinker Github page") for the latest release information.

## Using TabLinker

TabLinker takes annotated Excel files (found using the `srcMask` option in the [config.ini](http://github.com/Data2Semantics/TabLinker/tree/master/config.ini) file) and converts them to RDF. This RDF is serialized to the target folder specified using the `targetFolder` option in [config.ini](http://github.com/Data2Semantics/TabLinker/tree/master/config.ini).

Annotations in the Excel file should be done using the built-in **style** functionality of Excel (you can specify these by hand). TabLinker currently recognises seven styles:

- **TabLink Title** - The cell containing the title of a sheet
- **TabLink Data** - A cell that contains data, e.g. a number for the population size
- **TabLink ColHeader** - Used for the headers of columns
- **TabLink RowHeader** - Used for row headers
- **TabLink HierarchicalRowHeader** - Used for multi-column row headers with subsumption/taxonomic relations between the values of the columns
- **TabLink Property** - Typically used for the header cells directly above RowHeader or HierarchicalRowHeader cells, cell values are the properties that relate Data cells to RowHeader and HierarchicalRowHeader cells.
- **TabLink Label** - Used for cells that contain a label for one of the HierarchicalRowHeader cells.

An eight style, **TabLink Metadata**, is currently ignored (See #3).

An [example of such an annotated Excel file](http://github.com/Data2Semantics/TabLinker/tree/master/input/BRT_1889_02_T1_marked.xls) is provided in the [input](http://github.com/Data2Semantics/TabLinker/tree/master/input/) directory. There are ways to import the styles defined in that file into your own Excel files.

**Tip:** If your table contains totals for HierarchicalRowHeader cell values, use a non-TabLink style to mark the cells between the level to which the total belongs, and the cell that contains the name of the total. Have a look at the example [annotated Excel file](http://github.com/Data2Semantics/TabLinker/tree/master/input/BRT_1889_02_T1_marked.xls) to see how this is done (up to row 428).

Once you’re all set, start the TabLinker by cd-ing to the [src](http://github.com/Data2Semantics/TabLinker/tree/master/src/) folder, and running:

`python tablinker.py`

## Requirements

TabLinker was developed under the following environment:

- Python 2.7
- The xlutils and xlrd packages from [http://www.python-excel.org/](http://www.python-excel.org/)
- RDFLib, from [http://www.rdflib.net](http://www.rdflib.net/)
