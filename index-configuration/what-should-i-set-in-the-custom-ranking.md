To provide the best relevance, Algolia uses all the information available. Some of the information is given directly by the user (search keywords, filters applied...), but you can also provide some business information to help us rank the results.

That's the role of the Custom Ranking. You can use it to provide us with the information you have that represents the popularity/importance of a product.These attributes can contain integer, float or boolean values.They can be:

*   a raw value like the number of views, the number of sales, or the timestamp of a date
*   a calculated value that you computed on your side like a popularity_score or a profile_completeness_score
*   a 'human value', for example if you want to manually decide which products are featured, you could have an attribute "featured" that defaults to false and can be manually set to true.

The order of the attributes matters. The Custom Ranking behaves like the Ranking Formula, with a Tie-Breaking Algorithm:

*   we only look at the second attribute if there is an equality of values in the first attribute
*   we only look at the third attribute if there is an equality of values in the first and the second attribute
*   ...

The Custom Ranking is the main reason Algolia can provide relevant results from the very first keystrokes. If you only type one letter, most objects will have the same "textual relevance". In this case, we will return the most popular objects (based on the Custom Ranking) containing this letter. We strongly recommend to have a good custom ranking configured!If you have any question about your Custom Ranking, don't hesitate to [ask us](mailto:support@algolia.com) for more details.