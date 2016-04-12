There are two types of operations:

1.  The **Search** operations:  

    *   Each individual full-text search counts as an operation. If you implement a search-as-you-type experience, each keystroke represents one operation
    *   If you decide to batch queries, say for instance you want to query 2 indices at a time, it will use 2 operations 
    *   For disjunctive faceting, the number of operations equals 1 + the number of refined disjunctive facets (because we're performing additional queries to display the associated facet counts)
2.  The **Indexing** operations:
    *   Each add, update or delete of an object or part of an object counts for 1 operation
    *   If you chose to batch you indexing calls, each object modified will be counted as a single operation

In terms of pricing, we count the number of operations performed every month. If you hit the limit of your plan, we'll charge you a fee for the extra operations you've performed, based on the [over-quota pricing](https://www.algolia.com/pricing) of your current plan.