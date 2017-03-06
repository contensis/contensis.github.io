# Localization

Localization for an entry is identified by a language code which is formed using either a ISO 639-1 language code or a combination of a [ISO 639-1](https://en.wikipedia.org/wiki/ISO_639-1) language code and a [ISO 3166-1](https://en.wikipedia.org/wiki/ISO_3166-1) country code. Effectively, a Contensis language code can represent a language generically or specifically for a certain country.

The language code is lowercased and if the country code part is included, then that part is separated with a dash and uppercased.

For example:

* Standard English is represented as **en**
* American English is represented as **en-US**
* Germany German is represented as **de-DE**

[Contensis currently supports a subset of language codes](https://contensis.github.io/docs/entries/multi-language-support.html) which can be specfied when creating projects, content types and entries.
