There are multiple ways to filter your results, depending on what you want to achieve:

1/  [TagFilters](https://www.algolia.com/doc/ruby#tagFilters)If your records have an attribute that you'll use to filter by, that contains one or multiple values (for example:  `color: 'blue'`, or `tags: ['Electronics', 'Phones']`), you can then filter the results based on these values.`tagFilters` does just that. It allows you to retrieve all 'blue' items, or all 'Electronics' products.2/  [FacetFilters](https://www.algolia.com/doc/ruby#facetFilters)Facets have the same filtering possibilities as tags, but also have faceting abilities, which means that Algolia will send you the list of the most relevant filters depending on the current search.

![](https://s3.amazonaws.com/helpscout.net/docs/assets/557c2386e4b01a224b42b2b3/images/55e013f8c69791085647d104/file-xf6wFnHrxZ.png)

There are two kinds of facets:

*   Regular (or Conjunctive) facets allow to filter by one value of the attribute (e.g. 'blue'). If records are multi-valued, regular facets can be used to do a conjunction (e.g. 'blue' AND 'red').

*   Disjunctive facets allow to filter by one or multiple values of the attribute with a disjunction (e.g. 'blue' OR 'red')

3/  [NumericFilters](https://www.algolia.com/doc/ruby#numericFilters)Numeric filters are the equivalent of Facets for numeric values. You can for example filter all products whose price equals _19.95_.Numeric filters can also be used to filter by values greater than or smaller than (e.g. find products whose price is higher than $20).

![](https://s3.amazonaws.com/helpscout.net/docs/assets/557c2386e4b01a224b42b2b3/images/55e014469033600a2952886b/file-KI6WvfCsbz.png)