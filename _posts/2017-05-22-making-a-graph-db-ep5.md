---
layout: page
author: Cristi Constantin
comments: true
categories: article
tags: software programming graph db
excerpt: "In this episode, I'll be talking about my options for representing graphs in memory and persistent."
---

In my [previous article about my Graph Database](/2017/05/making-a-graph-db-ep4), I found a few use-cases that I want to resolve with my Graph Database.

In this episode, I'll be talking about my options for representing graphs in memory and persistent.

These days, I learned that depending on the storage, there are a few types of graphs:

1. fully in memory and no persistence - I didn't think RAM-only Graphs are real, but that seems to be the case
1. mostly memory, but also persistent - medium size
1. some memory, but mostly persistent - huge graphs

It's a balance between RAM and HDD/SSD and how much of the structure is saved. For example, if only a small portion of the graph is persistent, I'm thinking that on startup, the Graph library will create additional connections and indexes for fast access, that will be kept only in memory.

When I'm thinking about my use-case to store all the countries, the plants and animals and the rest, I don't feel that a RAM-only approach is feasible. I'm saying that because I will implement my graph in a higher level programming language that's less memory efficient then C, Java, or similar compiled languages.

The most obvious choice is 2: mostly memory, but also persistent.

There are many ways to do this, but the primary approach would be to construct a layer, a concept, a convention around an already existing store.

To be perfectly honest, I don't like this approach. I'd rather build a native storage engine from scratch, tailored exactly for my needs... but I won't do it at this point, because I cannot wait months or years to implement something custom. I'm alone in this experiment and after a few months, I might not even be interested in Graphs anymore.


## Graph representations

#### Notable articles:

- [What is the best way to represent a graph in MySQL](https://www.quora.com/What-is-the-best-way-to-represent-a-graph-in-MySQL){:target="_blank"}
- [Khan Academy representing graphs](https://www.khanacademy.org/computing/computer-science/algorithms/graph-representation/a/representing-graphs){:target="_blank"}
- [Khan Academy describing graphs](https://www.khanacademy.org/computing/computer-science/algorithms/graph-representation/a/describing-graphs){:target="_blank"}

#### Edge list
The simplest way to reprent a graph: store the edges, as pairs of nodes.
- Very easy to use and understand, perfect for key-value stores
- Slow to find an edge, slow to remove and lots of duplicates

#### Adjacency list
The graph can be represented as a collection of lists, one list for each different node of the graph. In this way, for a node n1, its adjacency list L1 is composed by all the nodes that are target of any edge which starts in n1.
- Generally preferred because it efficiently represents sparse graphs
- Slow to remove vertices and edges, because it needs to find all vertices or edges

#### Adjacency matrix
A 2D matrix, in which the rows represent source nodes and columns represent destination nodes. Data on edges and nodes must be stored externally. Only the cost for one edge can be stored between each pair of nodes.
* An adjacency matrix is preferred if the graph is dense
* Slow to add or remove vertices, because matrix must be resized/ copied

#### Incidence matrix
A 2D Boolean matrix, in which the rows represent the nodes and columns represent the edges. The entries indicate whether the vertex at a row is incident to the edge at a column.


## Possible storage solutions

- table databases
- document databases
- key-value stores
- HDF5 arrays
- [server](https://en.wikipedia.org/wiki/Database_server){:target="_blank"}, or  [embeded](https://en.wikipedia.org/wiki/Embedded_database){:target="_blank"}

I would prefer to use a portable/ embeded database, rather than a server, because I want my Graph to be more **user friendly**. If I'd choose a database server, that would require the end user to install stuff like MySql, or MongoDB, or Redis, which seems overkill for my toy database.
But if I discover that an embeded database is not enough, of course I'll consider switching to a server.

That's all I have to say for today.

See you next time!

-----

This blog is open source. You can check the [history of this post](https://github.com/croqaz/croqaz.github.io/commits/master/{{page.path}}).

If you have any thoughts, suggestions, criticism, or whatever, please drop me a line in the comments section.
