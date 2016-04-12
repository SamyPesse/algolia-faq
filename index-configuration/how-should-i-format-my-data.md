Algolia is schemaless, and can index data attributes having the following format:

*   string
*   integer / float
*   boolean
*   nested objects
*   array of (string, integers, floats, booleans, nested objects)

Providing an objectID with your objects is not mandatory. If you don't provide one, we'll generate one automatically, but it'll be easier for you to remove or update the record if you have stored its unique identifier in the objectID attribute.For now, the only format we accept for the dates is the Unix timestamp (e.g. 1435735848), if you want to filter by date.Here's an example of a record:

<pre>{
  "objectID": 42,             // record identifier
  "title": "Breaking Bad",    // string attribute
  "episodes": [               // array of strings attribute
    "Crazy Handful of Nothin'",
    "Gray Matter"
  ],
  "like_count": 978,          // integer attribute
  "avg_rating": 1.23456,      // float attribute
  "featured": true,           // boolean attribute
  "actors": [                 // nested objects attribute
    {
      "name": "Walter White",
      "portrayed_by": "Bryan Cranston"
    },
    {
      "name": "Skyler White",
      "portrayed_by": "Anna Gunn"
    }
  ]
}</pre>