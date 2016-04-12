Synonyms in the Algolia configuration are symmetrical. This means that we consider _NES_ to be the same as _Nintendo Entertainment System_ and vice-versa.

Sometimes you want this to flow in one-direction. For example, you want _video game_ to be considered the same as _NES_ and you want _video game_ to also be considered the same as _Sega_, but you do not want _Sega_ to be equivalent with _NES_.

You can set this up leveraging [altCorrections](https://www.algolia.com/doc/ruby#param-altCorrections). Specify the base word (for example, "video game") as the _word_, the alternative as the _correction_, and the _nbTypos_ as 0 since this isn't a misspelling, it's a unidirectional synonym.