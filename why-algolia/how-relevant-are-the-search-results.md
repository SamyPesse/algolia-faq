Relevance is extremely complex to handle with every other Search Engine (Elasticsearch, Solr…) we’ve seen.

We believe that relevance shouldn’t be a bonus, it’s part of our core engine, and we built it from the ground up with this in mind.Algolia manages to be relevant from the very first keystrokes thanks to its unique indexing and ranking algorithms.It’s a tie-breaking algorithm based on selected criteria (7 rules), which can be entirely customized (although the default setting – based on our experience – is good for 99% of the cases).One of the key elements of this ranking formula is the existence of the custom ranking criteria, that enables developers to integrate a business-specific metric describing the popularity of each records. Thus, users don't only get the most relevant results (according to the search query and other refinements), but also the most populars ones.This value can either be:

*   a raw value: like the number of views, number of sales these last 30 days, number of likes, number of followers
*   a computed value: like a score calculated based on business-specific algorithm.

Moreover, whereas other solutions available on the market compute very complex and obscure scorings, Algolia enables you to configure this scoring intuitively, directly in the dashboard or programmatically.Not convinced? Put us to  [the test](mailto:hey@algolia.com).