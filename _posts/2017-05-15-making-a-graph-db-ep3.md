---
layout: page
author: Cristi Constantin
comments: true
categories: article
tags: software programming graph db
excerpt: "In this episode, I'll be focusing on finding a list of free & open-source libraries for Elixir, Python and Node, that will inspire me."
---

In my [previous article about my Graph Database](/2017/05/making-a-graph-db-ep2), I found the answers for: who uses graphs, what are they doing with them and why did they choose graphs.

In this episode, I'll be focusing on finding a list of free & open-source libraries for *Elixir, Python and Node*, that will inspire me.
I'm still not writing any code yet. I need to know more.

Graph libraries for **Elixir**:

- [Erlang Digraph](http://erlang.org/doc/man/digraph.html){:target="_blank"} (std library Erlang labeled directed graphs - can be used in Elixir)
- [Github Oakfang/Thoth](https://github.com/oakfang/thoth){:target="_blank"}
- [Github Mikowitz/Graphvix](https://github.com/mikowitz/graphvix){:target="_blank"}
- [Erlang Cayley](https://github.com/davecaos/kylie){:target="_blank"} - wrapper for Cayley graph database

Graph libraries for **Python**:

- [Github PirosB3/Hexagon](https://github.com/PirosB3/Hexagon){:target="_blank"} - LevelGraph for Python
- [Bitbucket Ronaldoussoren/Altgraph](https://bitbucket.org/ronaldoussoren/altgraph){:target="_blank"} - good starting point
- [Graphlite](http://eugene-eeo.github.io/graphlite){:target="_blank"} - edges only in SQLite, very interesting approach
- [Bitbucket Nidusfr/Grapheekdb](https://bitbucket.org/nidusfr/grapheekdb){:target="_blank"} - lots and lots of backends
- [Github Charanpald/APGL](https://github.com/charanpald/APGL) - built on NumPy, Scipy, PySparse
- [NetworkX](https://github.com/networkx/networkx){:target="_blank"} - serious stuff
- [Python igraph](http://igraph.org/python){:target="_blank"} - serious stuff
- [Graph-tool](https://graph-tool.skewed.de/static/doc/index.html){:target="_blank"} -  - massive Graph analysis library
- [SNAP for Python](http://snap.stanford.edu/snappy){:target="_blank"} - analysis and manipulation of large networks (py2 only)
- [Github Ziyasal/Pyley](https://github.com/ziyasal/pyley){:target="_blank"} - wrapper for Cayley graph database

Graph libraries for **Node.js**:

- [Github Oakfang/SynoGraph](https://github.com/oakfang/SynoGraph){:target="_blank"} - Graph DB for humans, very interesting approach
- [Github Ryansmith94/Graph](https://github.com/ryansmith94/Graph){:target="_blank"} - jQuery-like functionality for graph structures
- [Github Cpettitt/Graphlib](https://github.com/cpettitt/graphlib){:target="_blank"} - directed and undirected graphs + algorithms
- [Github Mcollina/LevelGraph](https://github.com/mcollina/levelgraph){:target="_blank"} - graph following the Hexastore approach
- [Github Graphology](https://github.com/graphology/graphology){:target="_blank"} - serious stuff
- [Github Felipernb/algorithms.js](https://github.com/felipernb/algorithms.js){:target="_blank"} - interesting algorithms and data structures in JavaScript (graphs included)
- [Github Tblobaum/Redis-graph](https://github.com/tblobaum/redis-graph){:target="_blank"} - graph implementation using Redis sets

Python is the winner, with the most serious graph implementations :smile: And it's also the language I'm the most experienced in.
<br />
Now, before I start studying what I found, I need to setup my goals. I already mentioned what I want to accomplish in [the first episode](/2017/05/making-a-graph-db-ep1), but I need to go much deeper.
In fact, it's a delicate balance between this and learning more about other people's libraries, because I don't even know enough about graphs to know what I can choose from, what are my options.

So, now that I have a list of libraries for inspiration, I should forget about the implementation and setup a minimum of 3 use-cases. Based on them, I can then focus only on the libraries that I think can help me, because I don't have time to study everything right now and I won't even understand the code; that and I want to start building faster :smile:
While I'm writing the code, I'll understand better and I'll resume studying the more complex libraries. This approach works for me, but as I said, it's a delicate balance...

So, I'm going to start thinking about my use-cases now.

See you later!

-----

This blog is open source. You can check the [history of this post](https://github.com/croqaz/croqaz.github.io/commits/master/{{page.path}}).

If you have any thoughts, suggestions, criticism, or whatever, please drop me a line in the comments section.
If I have some audience, I'll be sharing details and I'll write more often, obviously.
