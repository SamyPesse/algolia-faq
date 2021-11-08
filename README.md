---
search: false
---

# Algolia FAQ

test gbx 4 !

This is a proof of concept for porting Algolia's FAQ as a GitBook. The search in this FAQ is powered by Algolia using [plugin-algolia](https://github.com/GitbookIO/plugin-algolia).

### Output

The output is available at https://samypesse.gitbooks.io/algolia-faq/content/

### JSON Output

The JSON output is also available using the GitBook.com API:

```
$ curl -H "Accept: application/vnd.gitbook.format.v3" https://api.gitbook.com/book/samypesse/algolia-faq/contents/basics/how-many-index-indices-can-i-create.json

{
  "file": {
    "path": "basics\/how-many-index-indices-can-i-create.md",
    "mtime": "2016-04-14T13:39:28.000Z",
    "type": "markdown"
  },
  "page": {
    "description": "You can create as many indices as you want. If you plan go into the tens of thousands or more, it\u2019s better to contact us to set up an optimized configuration.A few common use cases where several indices are needed:",
    "title": "How many index \/ indices can I create?",
  ...
```

### Relation between article

Article can have "Related Articles" listed in their YAML header.

For example: [why-algolia/what-makes-algolia-better-than-elasticsearch-or-solr.md](https://github.com/SamyPesse/algolia-faq/blob/master/why-algolia/what-makes-algolia-better-than-elasticsearch-or-solr.md)
And related article will be listed at the [bottom of the page](https://samypesse.gitbooks.io/algolia-faq/content/why-algolia/what-makes-algolia-better-than-elasticsearch-or-solr.html
).

