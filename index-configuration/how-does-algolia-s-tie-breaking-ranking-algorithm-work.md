Most search engines rank results based on a unique float value that is hard, if not impossible, to decipher. This is because their ranking algorithm has been designed for search in very large documents. They take into account the number of occurrences of query words in matching documents to determine their relevance, usually using a [tf-idf](https://en.wikipedia.org/wiki/Tf%E2%80%93idf)-based scoring.

This approach works very well for very complex operations, to search in very large documents, or to process analytics.We designed Algolia as a user-facing tool, built to provide the best user experience. Instead of assigning a global float score to each result, our ranking algorithm rates each matching record on 7 criteria, to which we individually assign an integer value score. To sort the results, the engine compares the matching records 2 by 2 against each of those 7 ranking criteria one after another and continues as soon as the current ranking criteria has the same value: this is a tie-breaking algorithm.By default - and we recommend to keep it that way - the 6 first ranking criteria are related to “text relevance”: the number of typos, the number of matching query words, the proximity between words, etc. If all text-based criteria have the same value, then we use the (last) “custom” criteria (reflecting the  [customRanking](https://www.algolia.com/doc/ruby#CustomRanking)) to rank the results.At the end, the matching results will be sorted with that kind of order:

<pre>- 0 typos
   - 0 typos && MAX(words)
     - 0 typos && MAX(words) && MIN(proximity)
       - 0 typos && MAX(words) && MIN(proximity) && MAX(attribute)
         - 0 typos && MAX(words) && MIN(proximity) && MAX(attribute) && MAX(exact)
           - 0 typos && MAX(words) && MIN(proximity) && MAX(attribute) && MAX(exact) && MAX(custom)
           - 0 typos && MAX(words) && MIN(proximity) && MAX(attribute) && MAX(exact) && MAX(custom)-1
           - 0 typos && MAX(words) && MIN(proximity) && MAX(attribute) && MAX(exact) && MAX(custom)-2
           - ...
         - 0 typos && MAX(words) && MIN(proximity) && MAX(attribute) && MAX(exact)-1
         - 0 typos && MAX(words) && MIN(proximity) && MAX(attribute) && MAX(exact)-2
         - ...
       - 0 typos && MAX(words) && MIN(proximity) && MAX(attribute)-1
       - 0 typos && MAX(words) && MIN(proximity) && MAX(attribute)-2
       - ...
     - 0 typos && MAX(words) && MIN(proximity)+1
     - 0 typos && MAX(words) && MIN(proximity)+2
     - ...
   - 0 typos && MAX(words)-1 matching words
   - 0 typos && MAX(words)-2 matching words
   - ...
- 1 typo
  - ...
- 2 typos
  - ...<br></pre>