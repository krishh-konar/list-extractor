# Wikipedia List-Extractor - Extract Data from Wikipedia Lists

#### This forked repository was a part of GSoC'17 warm-up project. Further work has been done at the main repository.
#### This repository is no longer being maintained. Visit [List-Extractor](https://github.com/dbpedia/list-extractor) for the most recent version of this tool.

#### [GSoC'16 Detailed Progress available here](https://github.com/dbpedia/extraction-framework/wiki/GSoC_2016_Progress_Federica)
#### [GSoC'17 Detailed Progress available here](https://github.com/dbpedia/list-extractor/wiki/GSoC-2017:-Krishanu-Konar-progress)

---

### How to run the script
`python listExtractor.py collect_mode source language`
* `collect_mode` : use `s` to specify a single resource or `a` for a class of resources in the next parameter.
* `source`: a string representing a class of resources from DBpedia ontology (right now it works for Writer and Actor), or a single Wikipedia page of an actor/writer.
* `language`: a two-letter prefix corresponding to the desired language of Wikipedia pages and SPARQL endpoint to be queried (it currently accepts only `en` or `it`).

Examples: `python listExtractor.py a Writer it`  | `python listExtractor.py s William_Gibson en`

If successful, a `.ttl` file containing RDF statements about the specified source is created inside a subdirectory called `extracted`.

### Requirements
* [Python 2.7](https://www.python.org/download/releases/2.7/)
* [RDFlib library](http://rdflib.readthedocs.io/en/stable/gettingstarted.html)
* Stable internet connection
