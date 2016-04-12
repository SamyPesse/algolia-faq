In the case you've built specific landing pages to display search results, it becomes really handy to be able to redirect users to those dedicated pages in the case their search query matches one of those.

<section class="callout-yellow">

### Example

Let's say you have an e-commerce website where you sell "star wars" related goods, and you'd like to redirect the user searching for "star wars" (or any related words) to a shiny Star Wars page. 

</section>

No problem, that can be easily done in a few steps:

<dl>

<dt>1</dt>

<dd>Create a new index that will contain all the redirection rules. _We can, for instance, name it 'redirects'._</dd>

</dl>

<dl>

<dt>2</dt>

<dd>Add to that index records containing the URL of the landing page and an array of keywords that will trigger the redirection.</dd>

</dl>

<pre>{
  "url": "https:// ....",
  "query_terms": ["star wars", "jedi", "darth vader", "george lucas", "luke skywalker"]
}
	</pre>

<dl>

<dt>3</dt>

<dd>Configure the index settings:</dd>

</dl>

*   Add the 'query_terms' attribute to the attributesToIndex list.   
    _If _the query terms order doesn't matter, _set the attribute to 'unordered'._

![](https://s3.amazonaws.com/helpscout.net/docs/assets/557c2386e4b01a224b42b2b3/images/56961ae19033603f7da30506/file-phekJbVAy4.png)

*   <span style="background-color: initial;">Set the Typo Tolerance to min</span>

![](https://s3.amazonaws.com/helpscout.net/docs/assets/557c2386e4b01a224b42b2b3/images/56961f339033603f7da3052d/file-UqHM0ctdIt.png)

*   <span style="background-color: initial;">Enable the ignorePlural option</span>

![](https://s3.amazonaws.com/helpscout.net/docs/assets/557c2386e4b01a224b42b2b3/images/5696247cc69791436155e2ec/file-cf3q0nIqA0.png)  

*   Enable the removeWordsIfNotResults option and set it to 'allOptional'

![](https://s3.amazonaws.com/helpscout.net/docs/assets/557c2386e4b01a224b42b2b3/images/56962490c69791436155e2ed/file-6EeyZYqpr1.png)  

<dl>

<dt>4</dt>

<dd>Implement a small business logic on the client side:</dd>

</dl>

*   At each new keystroke in the search field, perform a search against that index to retrieve a single result (hitsPerPage=1).  

_If you're using Javascript, you can find more details about the way to call multiple indices at the same time at [https://github.com/algolia/algoliasearch-client-js#multiple-queries](https://github.com/algolia/algoliasearch-client-js#multiple-queries)_

*   When the user presses enter (or clicks on the search icon) and if there is a result returned by that search query, use the "url" value to redirect the user to the correct page. 

Happy coding! If you have any question, feel free to reach out to our support!