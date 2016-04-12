Algolia uses a lot of techniques to optimize the speed of its search engine. One of them is to compute most of the search rankings when objects are indexed rather than when a search is performed.

This has a huge impact on performance, but it also implies that we cannot apply multiple ranking strategies for an index.In particular, you cannot have a different ranking strategy for each user on the same index. But there are multiple ways to get around that:**1/ Create one index per user**In some cases it may make sense to duplicate your index for each user. This is the simplest solution, but it'll generate lots of records.**2/ Create categories of users**Instead of having an index for each user, you can group the users in groups having similar behaviors. This approach is less refined for each user, but since you’ll have less categories than users, you’ll need less indices (one index per category). **3/ Merge two queries**You could tag all objects with a list of userIDs of people related to these objects `related_users = [‘user1’, ‘user42’]`.Then, are query time, you could merge the results from two queries:

*   A query that would search only on the objects tagged with the userID of the current user
*   A query that would search on all objects

This way, you’d have personalized results without needing to duplicate your indices.