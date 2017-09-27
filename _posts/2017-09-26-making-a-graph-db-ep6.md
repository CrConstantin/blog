---
layout: page
author: Cristi Constantin
comments: true
categories: article
tags: software programming graph db
excerpt: "Libraries I might use for persistence, compatibility formats and some basic specs."
---

Oh man, long time and no updates. I'm sorry about that. I'm writing a few words every few days, but it doesn't seem to finish.

In the meantime, I created a [repo on Github](https://github.com/croqaz/Graphh){:target="_blank"}.

In my [previous article about my Graph Database](/2017/05/making-a-graph-db-ep4), I studied some methods for representing graphs in memory and persistent.

In this episode, I want to look at the actual libraries that I might use for persistence.

## Embedded databases for Node.js or Python

This is the internal persistence layer, required to be as fast as possible:

- LevelDB - the most popular
- RocksDB - an alternative to LevelDB
- Lightning DB - only Python: https://github.com/dw/py-lmdb
- Berkeley DB - only Node: https://www.npmjs.com/package/berkeleydb
- there are other portable DBs available too, less popular and probably less efficient


## Compatibility formats

These formats are not particulary speed efficient, nor storage efficient, so they can't be used for instant snapshots. But to be compatible with other Graph implementations, my Graph should be exported to at least one of these:

- [Gephi GEXF](https://gephi.org/gexf/format){:target="_blank"} - XML format
- [GraphML](http://graphml.graphdrawing.org){:target="_blank"} - pure XML format, similar with GEXF
- [DOT format](https://en.wikipedia.org/wiki/DOT_(graph_description_language)){:target="_blank"} - simple format
- [Graph Modelling Language, or Graph Meta Language](https://en.wikipedia.org/wiki/Graph_Modelling_Language){:target="_blank"} - precursor of DOT
- [LEDA (Library of Efficient Datatypes)](http://www.algorithmic-solutions.info/leda_guide/graphs/leda_native_graph_fileformat.html){:target="_blank"} - fast text-based file format for storing a single directed, or undirected graphs
- [Pajek](https://gephi.org/users/supported-graph-formats/pajek-net-format){:target="_blank"} - easy text-based file format for storing a single directed, or undirected graph
- Graph6 si Sparse6 - somewhat exotic graph storage


## Graph query languages

- Cypher - Neo4j's query language
- SPARQL - https://www.w3.org/TR/rdf-sparql-query
- Gremlin
- GraphQL
- Dgraph's query language (inspired from GraphQL)

Also, [An overview of Graph database query languages](https://developer.ibm.com/dwblog/2017/overview-graph-database-query-languages){:target="_blank"} from IBM developers.


### Desired technical requirements:

- follow KISS principle (keep it simple stupid)
- target data size: 5 million nodes and 10 million edges on a standard laptop
- the graph should be directed, because in reality all things have a direction
- no need to store metadata about nodes, or edges
- persist the smallest possible set of data that can be reconstructed entirely, even it takes more time to init
- query the data: edges and triples. I'm not sure if I'll be using any of the existing graph query languages, they're ugly as hell and they don't seem productive at all; but I might reconsider later;
- all the data will be used in a normal application, atempting to replace a RDBM or NoSql database
- the database should be easy to merge with another database and all the data should merge perfectly (nice to have)
- I should also construct a visual tool to explore and discover the data, without knowing what's in there (nice to have). That would be beautiful, because graphs are really simple to understand mentally.


I want to hash the nodes using a standard hashing algorithm. The nodes must be hashed and stored in a special table, to avoid duplication of data. Hashing is less space efficient than, for example, giving an arbitrary number for each node in the de-duplication table, but has huge advantage that when you merge your nodes with the nodes from another database, the hashes will match perfectly.
In the same way, the edges should be hashed so that when you create a connection between 2 nodes, it's exactly the same connection as another database who created a connection between the same nodes.

For example, my database:
node: horse = 091b5035885c00170fec9ecf24224933e3de3fcc
node: grass = bbc29b76c59b382aca12201c44929002ef1778ae
edge: horse -> grass = da19c89bcc24bdc54041df2cbb2e7e5bc639809a

Another database:
node: horse = 091b5035885c00170fec9ecf24224933e3de3fcc
node: animal = 3199ea056253916c41d65c6fd39b52e5f239873c
edge: animal -> horse = e2fe5ce1a2d0ff363cda9862ed72e1b30a777b62

When joining the two databases, you'll gain more knowledge about the horse for free, without any unnecessary duplication: horse is an animal and eats grass.
This is just an example using SHA1 hashing. I'll probably use something different in the real implentation.

-----

This blog is open source. You can check the [history of this post](https://github.com/croqaz/croqaz.github.io/commits/master/{{page.path}}).

If you have any thoughts, suggestions, criticism, or whatever, please drop me a line in the comments section.
If I have some audience, I'll be sharing details and I'll write more often, obviously.
