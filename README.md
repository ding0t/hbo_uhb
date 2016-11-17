# UHB
The resource we are using as our UHB is the [Open Scriptures Hebrew Bible](https://github.com/openscriptures/morphhb).  This project is the Westminster Leningrad Codex with Strongs lexical data and morphological data marked up in OSIS files.


## Parsing Status

* [Genesis First Pass](http://hb.openscriptures.org/status_gen.html)
* [Exodus First Pass](http://hb.openscriptures.org/status_exo.html)
* [Leviticus First Pass](http://hb.openscriptures.org/status_lev.html)
* [Numbers First Pass](http://hb.openscriptures.org/status_num.html)
* [Deuteronomy First Pass](http://hb.openscriptures.org/status_deu.html)
* [Joshua First Pass](http://hb.openscriptures.org/status_jos.html)
* [Judges First Pass](http://hb.openscriptures.org/status_jdg.html)
* [Ruth First Pass](http://hb.openscriptures.org/status_rut.html)
* [1 Samuel First Pass](http://hb.openscriptures.org/status_1sa.html)
* [2 Samuel First Pass](http://hb.openscriptures.org/status_2sa.html)
* [1 Kings First Pass](http://hb.openscriptures.org/status_1ki.html)
* [2 Kings First Pass](http://hb.openscriptures.org/status_2ki.html)
* [1 Chronicles First Pass](http://hb.openscriptures.org/status_1ch.html)
* [2 Chronicles First Pass](http://hb.openscriptures.org/status_2ch.html)
* [Ezra First Pass](http://hb.openscriptures.org/status_ezr.html)
* [Nehemiah First Pass](http://hb.openscriptures.org/status_neh.html)
* [Esther First Pass](http://hb.openscriptures.org/status_est.html)
* [Job First Pass](http://hb.openscriptures.org/status_job.html)
* [Psalms First Pass](http://hb.openscriptures.org/status_psa.html)
* [Proverbs First Pass](http://hb.openscriptures.org/status_pro.html)
* [Ecclesiastes First Pass](http://hb.openscriptures.org/status_ecc.html)
* [Song of Songs First Pass](http://hb.openscriptures.org/status_sng.html)
* [Isaiah First Pass](http://hb.openscriptures.org/status_isa.html)
* [Jeremiah First Pass](http://hb.openscriptures.org/status_jer.html)
* [Lamentations First Pass](http://hb.openscriptures.org/status_lam.html)
* [Ezekiel First Pass](http://hb.openscriptures.org/status_ezk.html)
* [Daniel First Pass](http://hb.openscriptures.org/status_dan.html)
* [Hosea First Pass](http://hb.openscriptures.org/status_hos.html)
* [Joel First Pass](http://hb.openscriptures.org/status_jol.html)
* [Amos First Pass](http://hb.openscriptures.org/status_amo.html)
* [Obadiah First Pass](http://hb.openscriptures.org/status_oba.html)
* [Jonah First Pass](http://hb.openscriptures.org/status_jon.html)
* [Micah First Pass](http://hb.openscriptures.org/status_mic.html)
* [Nahum First Pass](http://hb.openscriptures.org/status_nam.html)
* [Habakkuk First Pass](http://hb.openscriptures.org/status_hab.html)
* [Zephaniah First Pass](http://hb.openscriptures.org/status_zep.html)
* [Haggai First Pass](http://hb.openscriptures.org/status_hag.html)
* [Zechariah First Pass](http://hb.openscriptures.org/status_zec.html)
* [Malachi First Pass](http://hb.openscriptures.org/status_mal.html)


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
