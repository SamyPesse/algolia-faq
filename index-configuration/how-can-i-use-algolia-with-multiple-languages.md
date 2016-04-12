By design the engine is not only data agnostic, but also language agnostic. It supports out of the box, without any extra work, all languages / alphabets (including symbol based languages like Chinese, Japanese, Korean, Russian, …) used in the world.

The only thing you need to do is:1\. At indexing time, add extra attributes containing the translated version of your values

<pre>{
  "name": "Paris",
  "name_kr": "파리",
  "name_jp": "パリ",
  ...
  population: 2138551
}</pre>

And then add those new attributes to the list of [attributesToIndex](https://www.algolia.com/doc/ruby#attributesToIndex).2\. At query time, restrict the attributes used by the engine, according to the language you want to use. That can be easily done using the [restrictSearchableAttributes](https://www.algolia.com/doc/ruby#restrictSearchableAttributes) search parameter.