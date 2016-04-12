Even better! Giving more or less importance to an attribute of your records is a built-in feature of Algolia.

The setting [attributesToIndex](https://www.algolia.com/doc/ruby#attributesToIndex) is not only used to specify the attributes you want to search on. It’s also used to specify the relative importance of each attribute.For instance, if you want to give more importance to the keywords in the name than the description, then you would place the attribute “name” before the attribute “description” in your attributesToIndex.

![](https://s3.amazonaws.com/helpscout.net/docs/assets/557c2386e4b01a224b42b2b3/images/55df04c7e4b01d7a6a9bdc02/file-3PC7Ow9IdQ.png)

If you want multiple attributes to have the same importance, you can just group them by making a comma-separated list.

![](https://s3.amazonaws.com/helpscout.net/docs/assets/557c2386e4b01a224b42b2b3/images/55df04e8e4b01d7a6a9bdc03/file-WY0orOZAS0.png)