Yes, records are not expected to go beyond 10KB of minified JSON. You'll get the `Record is too big` error if you try to index a record bigger than the limit.

If you need to search for bigger objects, please contact us at [enterprise@algolia.com](mailto:enterprise@algolia.com) and we’ll increase your limit. There are three reasons for this limit:

1.  Our pricing is based on it
2.  In most cases, having bigger objects is a sign that you’re not using Algolia at its full capacity:
    *   Having very big chunks of text is usually bad for relevance, because most objects end-up having a lot of similar words, and they will match with a lot of irrelevant queries.
    *   It’s often better to de-duplicate big objects into several smaller ones
3.  It increases latency: big objects with a lot of unnecessary information take a long time to be uploaded/downloaded