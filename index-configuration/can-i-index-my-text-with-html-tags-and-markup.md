Yes you can! Even better: we’ll automatically exclude the non-relevant text from the search.

In order to keep an optimal relevancy, we made the choice to exclude HTML/XML tags, and their attributes, from data being indexed and searchable.In the following example, people would be able to search for any word in the description except the link tag itself. This means that the following record will not be returned when searching for _href_, _target_ or __blank_.

<pre>{
  "name": "Myth #9",
  "description": "In-house <a href=\"http://...\" target=\"_blank\">experts</a> are essential to get search right",
  ...
}</pre>