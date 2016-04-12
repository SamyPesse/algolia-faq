If you're using a facet, Algolia will automatically calculate and send you the count (number of items) for each value of the facet. You can find this information in the JSON answer of a search query.

Each value is associated with its count:

<pre>"facets" : {
  "category" : {
    "Movies & TV Shows" : 85,
    "Cell Phones" : 24,
    "Headphones" : 24,
    ...
}</pre>