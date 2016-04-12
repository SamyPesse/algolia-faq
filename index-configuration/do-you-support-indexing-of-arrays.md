Algolia is schemaless, and can index data attributes having the following format:

*   string
*   integer / float
*   boolean
*   nested objects
*   array of (string, integers, floats, booleans, nested objects)

If you add an array in the list of attributes to index, we extract and index all strings in the array. The even take into account in the textual relevance if the terms are matched in the same string of the array via the "proximity" element of the ranking formula. For example, the "first second" query will be considered with a proximity of 1 for the array ["first second", "other string"] but with a proximity of 8 (maximum value) for the array ["first string", "second string"].