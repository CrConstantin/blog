---
layout: page
author: Cristi Constantin
comments: true
categories: article
tags: software programming graph db
teaser: "In this episode, I'll be focusing on learning more about: who uses graphs, what are they doing with them, why did they choose graphs and maybe something about their implementation."
---

In the [first article about my Graph Database](/2017/05/making-a-graph-db-ep1), I had some ideas to start with, and set some tasks. I did my homework and read basic stuff about all the mentioned databases and I discovered lots of new things.

In this episode, I'll be focusing on learning more about: who uses graphs, what are they doing with them, why did they choose graphs and maybe something about their implementation (but that's for the next episodes).

Apparently it's quite a big interest in Graph Databases everywhere and most IT giants have implemented something "in house", using the already available databases and some "software duct-tape".
Obviously, when you already have a huge infrastructure, you want to migrate your data as slowly and painlessly as possible, so you build on top of the old system.

There are many enterprise solutions, crazy expensive and they need weeks of training. There are also a number of free & open-source versions, but most of them are impossible to deploy on my tiny MacBook Air. I'll only use them for inspiration.

Here are some relevant questions & answers on Quora:

- [What are some use cases for Graph databases?](https://www.quora.com/What-are-some-use-cases-for-graph-databases){:target="_blank"}
- [Who uses a graph database in production?](https://www.quora.com/Neo4j-Who-uses-a-graph-database-in-production){:target="_blank"}
- [Why are Graph databases not used in social networks like Facebook and Twitter?](https://quora.com/Why-are-graph-databases-not-used-in-social-networks-like-Facebook-and-Twitter){:target="_blank"}
- [Why the major websites like Facebook, Pinterest, Quora, Google+ are not using Graph databases?](https://quora.com/Why-the-major-websites-like-Facebook-pinterest-quora-google+-are-not-using-Graph-databases){:target="_blank"}
- [Is Facebook Graph actually backed by a graph database](https://www.quora.com/Is-Facebook-Graph-actually-backed-by-a-graph-database){:target="_blank"}
- [What is the best way to represent a graph in MySQL](https://www.quora.com/What-is-the-best-way-to-represent-a-graph-in-MySQL){:target="_blank"}
- [How do graph databases work?](https://www.quora.com/How-do-graph-databases-work){:target="_blank"} :exclamation:

And a few articles:

- [Bloor Graph Databases](http://www.bloorresearch.com/technology/graph-databases){:target="_blank"}
- [Graph Databases: The New Way to Access Super Fast Social Data](http://mashable.com/2012/09/26/graph-databases){:target="_blank"} - not so new anymore
- [NSA Is Building Social Graphs of Americans' Data](http://mashable.com/2013/09/28/nsa-social-graphs){:target="_blank"} - if NSA can do it, so can I :smile:
- [Neo Technology Prepares To Take On All Comers In Graph Database Market](https://techcrunch.com/2015/10/21/neo-technology-ready-to-take-on-competition-in-graph-database-market){:target="_blank"}
- [Many use cases for graph databases and analytics](https://www.oreilly.com/ideas/there-are-many-use-cases-for-graph-databases-and-analytics){:target="_blank"}

Use-cases from the big boys:

- [Neo4j use cases](https://neo4j.com/use-cases){:target="_blank"}
- [DataStax Graph use cases](http://www.datastax.com/products/datastax-enterprise-graph){:target="_blank"}
- [Sparksee use cases](http://www.sparsity-technologies.com/#sparksee){:target="_blank"}
- [InfiniteGraph use cases](http://www.objectivity.com/solutions/use-cases){:target="_blank"}

Things to study more:

- Google's Knowledge Graph
- Facebook's Social Graph
- Twitter's Interest Graph
- Microsoft's Graph


So, to wrap this up, here are some answers to my questions:

:question:: Who uses graphs?
:exclamation:: Everybody who is somebody :grinning:

:question:: What are they using graphs for?
:exclamation:: Diverse stuff. General interaction networks analysis, social networks (following/ follower/ friends), genomics / biology, route finding, modelling risks in financial systems, fraud detection, identity and access management, network and IT operations, recommendation engines, internet of things, machine learning, etc.

:question:: Why are they using graphs, instead of other types of DBs?
:exclamation:: Because some use-cases are more efficient this way. Because they scale more naturally to large data sets as they don't typically need costly join operations. Complex hierarchical structures, like many-to-many, are difficult to model with a table-based or document-based technology. To cite [Dave Stagner's answer](https://www.quora.com/What-are-some-use-cases-for-graph-databases/answer/Dave-Stagner?srid=JyOG){:target="_blank"}: "*You should try to use data persistence that actually reflects the structure of the data. Otherwise, you're introducing a layer of translation in your code that reflects your choice of tools, not your choice of problems.*" Perfect answer.


I didn't write any code yet. Patience is a virtue :pray:
I want to understand what I have to do first.

Until the next time!

-----

This blog is open source. You can check the [history of this post](https://github.com/croqaz/croqaz.github.io/commits/master/{{page.path}}).

If you have any thoughts, suggestions, criticism, or whatever, please drop me a line in the comments section.
If I have some audience, I'll be sharing details and I'll write more often, obviously.
