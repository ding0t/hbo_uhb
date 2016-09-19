# UHB

## Roadmap

### Initial Inclusion in tC

Get tC to support OSIS XML files like https://github.com/openscriptures/morphhb/blob/master/wlc/Ruth.xml
  * Lexical data is encoded in `lemma` attribute
  * Morph data is encoded in `morph` attribute

May as well read the files directly from https://github.com/openscriptures/morphhb/blob/master/wlc/ unless we want to create a process to put this into our container format.

Currently, I'm only seeing about 1% of the words in those files has having morphological data.


### Finishing Morphological Data

### Option 1

Include morph from Shebanq if possible.  Looks like we would need to grab the parsing out of https://shebanq.ancient-data.org/shebanq/static/docs/tools/shebanq/plain.html and then splice them into the OSIS files.  **If** this necessitates a license change then we can work in our own fork.

### Option 2

Create a process that takes parsings available https://github.com/openscriptures/morphhb/blob/master/wlc/ and programmatically guess at all the rest of the words in the OT (e.g. strip cantillation and find and replace for unknowns).  Feed these back into the parsing system at http://hb.openscriptures.org/OshbParse/ and have a team go through and update and verify them.

If we can make this an iterative process then we would be able to cut down the amount of manual intervention necessary to get the morph data.