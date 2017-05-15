---
layout: page
author: Cristi Constantin
comments: true
categories: article
tags: software programming graph db
---

So what's this all about? This is my first article *(hopefully out of many)*, where I'll describe my journey of learning how to build a **[Graph Database](https://en.wikipedia.org/wiki/Graph_database){:target="_blank"}**.

:memo:: I'm not sure how far I'll go yet, I'm doing this in my spare time, so I make no promises...

My background is: software developer :computer: for about 10 years now. I've written many kinds of software and used several databases: MySql, Microsoft SQL Server, SQLite, MongoDb, RethinkDB, LevelDB; but I'm no expert, just your regular user.
I've also used IPFS and Ethereum, not the regular kind of databases, but fun to learn nonetheless.

And this is how I want to do it: I'll imagine that what I'm trying to do is already finished, then I'll explain to you how I did it :scream_cat:
This mental hack keeps me focused and confident, even though it's a HUGE task...

:question:: So why am I doing this?
:exclamation:: Because it's fun. Because it's a huge challenge, way more than I can handle. Because I need this kind of library. Because I'll use this knowledge, even if it doesn't become a stable product.

:question:: What are the challenges?
:exclamation:: I don't know anything about how databases work internally (well, I have some ideas, but I didn't study much). I don't really know how indexing works. I don't know much about graphs.

:question:: So why the heck am I doing this again?!
:exclamation:: In the end, I want to create a better alternative to table-based and document-based databases, so that I can connect data infinitely and navigate the resulting spider web. And of course, I want to learn in the process.

:question:: What's my use-case?
:exclamation:: I want to save all the countries in the world and all their relations; and all the animals and plants in the world and all the data I can find about them; and all my favorite movies, with all the actors and the most relevant relations between them; quantity conversion (length, weight, temperature). I want to use this data in a normal application, where I would use a NoSql database. *Maybe in the future, I'll implement a nice GUI to visualize and edit the nodes and edges*.

:question:: What's the maximum data size?
:exclamation:: I'm thinking 10 million edges. It's a pretty big number for a toy database (see [Visualizing 1 million](https://en.wikipedia.org/wiki/1,000,000) and multiply by 10). And if this becomes serious, I'll target more.

:question:: What programming languages will I use?
:exclamation:: Any, or all of: **Elixir, Python, Node**. In this exact order. I prefer Elixir the most, because it's really fun to play with and I want to learn it better. But I might end up using Python, because I'm the most productive with it. Node is also a great option, because there are hundreds of thousands of libs to help me.

:question:: Can I really do this?
:exclamation:: Time will tell. If I can't do it, I'll resume watching Game of Thrones, I haven't finished the last season.

:question:: Will this be open-source?
:exclamation:: Yes. Most of it, anyway.
<br />
The tasks:

- study Neo4J, Titan, DataStax
- study MongoDB, RethingDB, CouchDB
- study LevelDB, RocksDB, Redis, Riak
- study what exactly is a graph, the math, the theory
- study how to store a graph on a computer

The first things that I found:

- [Network Theory: Graph Theory - Youtube.com/watch?v=82zlRaRUsaY](https://www.youtube.com/watch?v=82zlRaRUsaY){:target="_blank"} (from Complexity Labs)
- [Graph Theory: An Introduction - Youtube.com/watch?v=HmQR8Xy9DeM](https://www.youtube.com/watch?v=HmQR8Xy9DeM){:target="_blank"} (from PatrickJMT)

Until the next time!

-----

This blog is open source. You can check the [history of this post](https://github.com/croqaz/croqaz.github.io/commits/master/{{page.path}}).

If you have any thoughts, suggestions, criticism, or whatever, please drop me a line in the comments section.
If I have some audience, I'll be more focused on details and I'll write more often, obviously.
