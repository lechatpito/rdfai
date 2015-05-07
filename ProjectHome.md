A runnable system fuses or interlink rdf datasets according to user config.

RDF-AI includes preprocessing, matching, fusion, interlink and post processing five modules. The system provides flexible user interface to interact with user's config, this approach gives the user an important role for defining the input and output of fusion.

## How to run ##
To run the system, you need install the JDK, [WordNet 2.1](http://wordnet.princeton.edu) and [JWNL 1.4](http://sourceforge.net/projects/jwordnet) and setup them can be used normally. In the command line model, input "java -jar rdfai.jar configfilespath" to start system.

## Config instructions ##
The instructions of config files are as follows, the meanings of some nodes are obvious, here, we explain the points confusing:(Please find the example datasets and config files at the downloads page)

### general.xml ###
"threshold" is the matching threshold
"filename2" and "graph2SPARQLURI" are mutually exclusive. In the later, we need to change server address in this http address. The namespace paramter in the bracket is the contents of initQuery in matching.xml.

### graph1Structure.xml and graph2Structure.xml ###
They are the Ontology descriptions of graph 1 and graph 2. Where, "extendLiteralProperty" can be multiple.

### preprocessing.xml ###
The languages in the "translation" node is the former of [Google Translation API](http://code.google.com/p/google-api-translate-java). If you don't use a function, please comment it.

### matching.xml ###
The optional config is "string comparison"  or "word relation".

### fusion.xml ###
If you don't configure "Add" or "Merge", please comment it. The sub node in the "add" or "merge" node can be multiple.