An operation is an atomic action performed on our engine.

It can be:

*   A search query (for instance, a character typed in the search bar - or a filter selected by the user)
*   An indexing operation (an object added/updated/deleted from one of your indices)

Batches of queries or indexing operations count for as many operations as the number of items they contain. So if you send a batch modifying 1000 objects, it will count as 1000 operations.If you use the [disjunctive faceting](https://www.algolia.com/doc/ruby#disjunctive-faceting) feature in your search, the number of operations for each query will depend on the number of disjunctive facets you use.