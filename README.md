# Algolia FAQ

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
