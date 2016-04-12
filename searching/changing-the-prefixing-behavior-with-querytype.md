Algolia is built for search as-you-type, which means that by default, when a user searches for **ipho**, we’ll try to match all the objects that have the prefix **ipho**, like **iphone**.

You can modify this behavior with the settings **queryType:**

*   <u>prefixLast</u>: only the last query word is interpreted as a prefix (default behavior).
*   <u>prefixAll</u>: all query words are interpreted as prefixes.
*   <u>prefixNone</u>: no query word is interpreted as a prefix. This option is not recommended, because it breaks the “as-you-type” experience.