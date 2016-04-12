Yes, but not directly.

You'll have to first extract the textual content of your documents and index that information.

If you happen to have big documents, we also recommend to split the content into smaller chunks. You could for example split your text into paragraphs, and index those independently. Then, you can use our [distinct](https://www.algolia.com/doc/ruby#Distinct) feature to return each document only once.