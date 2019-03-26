# unfoldingWord® Hebrew Bible

*An open-licensed, lexically tagged, morphologically parsed Hebrew Old Testament. It enables the global Church to have access to the original texts of the Old Testament.*

## Basis

The UHB is based on the [Open Scriptures Hebrew Bible](https://github.com/openscriptures/morphhb) (OSHB) version 2.1. This project is the Westminster Leningrad Codex with Strongs lexical data and morphological data marked up in OSIS files.

## Changes from the OSHB

The UHB differs from the OSHB in two respects (though more may be coming):

* Metadata - The UHB text includes various metadata to mark the text which create links to other content that our software uses. For example, we add links to our [unfoldingWord® Translation Words](https://git.door43.org/unfoldingWord/en_tw) articles where appropriate.
* Joined words (for example: inseparable prepositions, the definite article, conjunctive waw) are separated using a unicode WORD JOINER (U+2060) character instead of the `/` character that the OSHB uses.
* The UHB is encoded in USFM 3.0 instead of the OSIS that the OSHB uses.

## Related projects

* [unfoldingWord® Hebrew Grammar](https://uhg.readthedocs.io/en/latest/)
* [unfoldingWord® Literal Text](https://git.door43.org/unfoldingWord/en_ult)
