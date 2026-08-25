<img src="https://cdn.door43.org/assets/uw-icons/logo-uhb-256.png" alt="drawing" width="100"/>

# unfoldingWord® Hebrew Bible

*An open-licensed, lexically tagged, morphologically parsed Hebrew Old Testament. It enables the global Church to have access to the original texts of the Old Testament.*

## Basis

The UHB is based on the [Open Scriptures Hebrew Bible](https://github.com/openscriptures/morphhb) (OSHB) version 2.1. The OSHB project is the Westminster Leningrad Codex (WLC) with Strongs lexical data and morphological data marked up in OSIS files.

## Changes from the OSHB

The UHB differs from the OSHB in a few respects (though more may be coming):

* Metadata—The UHB text includes various metadata to mark the text which create links to other content that our software uses. For example, we add links to our [unfoldingWord® Translation Words](https://git.door43.org/unfoldingWord/en_tw) articles where appropriate.
* Joined words (for example: inseparable prepositions, the definite article, conjunctive waw) are separated using a unicode WORD JOINER (U+2060) character instead of the `/` character that the OSHB uses.
* The UHB is encoded in [USFM 3.0](https://ubsicap.github.io/usfm/) instead of the OSIS that the OSHB uses.
* The UHB uses the versification scheme of the [ULT](https://git.door43.org/unfoldingWord/en_ult) instead of that of the OSHB (which is based on the WLC scheme common for Hebrew Bibles). The goal of this change is to simplify the translation and reference process for Gateway Language teams and supplemental resources (such as our translation helps suite). This may make some resources that are keyed to the WLC more difficult to use with the Hebrew text but it will likely simplify the use of many other resources that use an ASV/KJV style of versification.
* In order to avoid subjectivity, the text of the UHB uses the Ketiv of the WLC. The ULT then follows that reading. Any significant Qere difference is noted in a Translation Note and, if we judged that the Qere was the more likely reading, we followed that reading in the UST. 
  
## Related projects

* [unfoldingWord® Hebrew Grammar (UHG)](https://uhg.readthedocs.io/en/latest/)
* [unfoldingWord® Literal Text (ULT)](https://git.door43.org/unfoldingWord/en_ult)
