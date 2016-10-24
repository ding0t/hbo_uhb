# UHB
The resource we are using as our UHB is the [Open Scriptures Hebrew Bible](https://github.com/openscriptures/morphhb).  This project is the Westminster Leningrad Codex with Strongs lexical data and morphological data marked up in OSIS files.

## Roadmap


### Initial Inclusion in tC

Get tC to support OSIS XML files like https://github.com/openscriptures/morphhb/blob/master/wlc/Ruth.xml

  * Lexical data is encoded in `lemma` attribute, which is the word's Strongs number
  * Morph data is encoded in `morph` attribute, [key here](http://openscriptures.github.io/morphhb/parsing/HebrewMorphologyCodes.html)

May as well read the files directly from https://github.com/openscriptures/morphhb/blob/master/wlc/ unless we want to create a process to put this into our container format.

Currently, I'm only seeing about 1% of the words in those files has having morphological data.


### Finishing Morphological Data

#### Stage 1

Write a comparer script that can verify our proposed parsings from http://hb.openscriptures.org/OshbParse/ against an existing dataset (such as https://shebanq.ancient-data.org/shebanq/static/docs/tools/shebanq/plain.html).  If they check out then they can be marked as verified and included in the XML files.

#### Stage 2

Create a process that takes verified parsings from https://github.com/openscriptures/morphhb/blob/master/wlc/ and programmatically guess at the rest of the words in the OT (e.g. strip cantillation and find and replace for unknowns).  Feed these back into the parsing system at http://hb.openscriptures.org/OshbParse/ and verify them against an existing dataset and/or Editors.

If we can make this an iterative process then we would be able to cut down the amount of manual intervention necessary to get the morph data.

### Completion

After the morphology data is complete, the UHB project will effectively be completed.  At the moment there are no further plans to markup the text with other information.
