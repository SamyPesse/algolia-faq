By default all the attributes you push in your records are searchable. The attributeToIndex list allows to restrict the list of attributes the users will be able to search in, to just a few of them.

Take for example this record:

<pre>{
  name: 'Algolia',
  description: 'Algolia is a Search as a Service focused on providing the best UX',
  url: 'http://www.algolia.com',
  popularity_score: 42
}</pre>

You don't want to search on the URL or the popularity score, only on the text. In this case, your attributesToIndex would be like that:

![](https://s3.amazonaws.com/helpscout.net/docs/assets/557c2386e4b01a224b42b2b3/images/55df04c7e4b01d7a6a9bdc02/file-3PC7Ow9IdQ.png)

Additionally to adding the attribute you want to search in, you can easily prioritize each attribute against each other by ordering them in that list. Depending on which attribute has been used to match your records, the engine will give an higher priority/rank to the records where the matches are on top of the attributeToIndex list.