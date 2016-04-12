Algolia uses 3 features to handle the users’ typing mistakes:**1/ Typo-tolerance**

*   A letter is replaced by another: “iphXne” instead of “iPhone”
*   Two letters switched position: “iPhnoe” instead of “iPhone”

By default, Algolia considers that an object without any typing mistake is more relevant and will therefore rank it higher in the results list.

**2/ Split and Concatenation**

*   A space or a special character is missing: “RayBan” instead of “Ray-Ban”
*   A space or a special character is unnecessary: “i-Phone” or “i Phone” for “iPhone”

**3/ Synonyms**You can define a list of Synonyms to help users find the objects they want even if they don’t use the right words.These features are configurable via the Dashboard or via the API.