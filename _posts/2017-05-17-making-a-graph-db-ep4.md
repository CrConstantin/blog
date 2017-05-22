---
layout: page
author: Cristi Constantin
comments: true
categories: article
tags: software programming graph db
excerpt: "I had a homework: to find a minimum of 3 use-cases that I want to resolve with my Graph Database."
---

In my [previous article about my Graph Database](/2017/05/making-a-graph-db-ep3), I found a list of free & open-source libraries for *Elixir, Python and Node*, and I had a homework: to find 3 a minimum of use-cases that I want to resolve with my Graph Database.

I thought about this a lot.

First use-case:

- add all the [countries and their neighbors from Mledoze/Countries](https://github.com/mledoze/countries){:target="_blank"}, the geo coordinates, all the capitals, all the currencies and the most important cities
- that's a small graph, probably around 1k-2k nodes and edges, but is useful, because I want to see how I would replace a classic document-based DB with a graph
- be able to query by continent, by country, by capital, by currency
- find top 3 largest and smallest countries
- find top 3 countries with the most neighbors
- what are the top 3 most popular currencies (by country)
- stupid thinks like: what are the cities with the same name, from different countries
- are there any countries with the same capital? - sanity check
- what are the countries that span on more continents? - don't even know if I have this data

Second use-case:

- add [all my favorite movies](http://www.imdb.com/user/ur30339282/ratings){:target="_blank"}
- that's also a small graph, around 1k-2k nodes and edges, but is useful because the relations are many-to-many
- what period of time is the most dense with favorite movies
- what are my favorite actors
- what are my favorite genres

Third use-case:

- add the [top 100 most popular Node.js libraries](https://www.npmjs.com/browse/star){:target="_blank"}, with their dependencies
- I have no idea how large this graph is, but it's definitely something pretty large and dense; if not I could add the top 1000, or top 5000
- find top 3 libraries with most and least dependencies
- find top 3 libraries with most and least versions

Forth use-case:

- this is just a stress test: add [all english words from Wordnet-DB](https://github.com/moos/wordnet-db){:target="_blank"} by type
- this is a medium graph, around 1 million nodes
- what's the category with the most words

Other notable use-cases:

- lenght converters (eg: meter to km, meter to foot, meter to mile, etc.)
- weight, temperature, time converters as graphs

<br />
With that in mind, I can start studying the popular graph libraries that I found. This might take a lot of time...

Hope to see you again!

-----

This blog is open source. You can check the [history of this post](https://github.com/croqaz/croqaz.github.io/commits/master/{{page.path}}).

If you have any thoughts, suggestions, criticism, or whatever, please drop me a line in the comments section.
If I have some audience, I'll be sharing details and I'll write more often, obviously.
