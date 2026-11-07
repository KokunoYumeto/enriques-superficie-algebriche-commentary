EDIT FOR THE READER: Part 1 of a mathematical commentary on Federigo Enriques, Le superficie algebriche (1949).

The commentary (LaTeX, between BEGIN TEX and END TEX) was written by an AI model from page-by-page audits of the
published edition of the book and the scans of the print. Some of its sentences talk about how it was made: the
"supplied" audits, transcription, scans or pages; what "the audit", "the broader audit" or "the detailed audit" said;
which audit a result was "retained" from. A reader of the commentary has not seen the audits or any supplied files. The
reader has the book, the published edition (a LaTeX edition with an editorial apparatus) and this commentary.

TASK. Between BEGIN SENTENCES and END SENTENCES are the sentences that may talk about this, as: id | line number in the
TeX | sentence. Rewrite each so that it speaks to the reader of the book:
- Refer to the print, the scan of the print, and the edition with its apparatus. Never refer to supplied pages, files
  or materials, to the audits, or to audit claim ids.
- Where the sentence reports what an audit said, state the mathematics instead, as the commentary concludes it. Where
  two audits disagreed, state the correct point (the surrounding text settles which) and drop the disagreement.
- Where the sentence only reports provenance and carries no mathematics (for example "This counterexample and its
  calculation are retained from the audits."), give an empty replacement, unless the paragraph would then not read
  well; in that case give a short neutral sentence.
- The opening paragraph (line 1) keeps one sentence saying that the commentary was written by an AI model (ChatGPT,
  Pro mode) from page-by-page audits of the published edition and the scans of the print; drop "supplied" there too.
- Keep every piece of mathematics, every citation, \ref, \label, footnote and formula exactly. Change only the wording
  about how the commentary was made. Do not shorten, restyle or improve anything else.
- "X is supplied by Zariski" (meaning provided by) is ordinary English: such a sentence is returned unchanged unless it
  also speaks of the audits or supplied material.
- The replacement takes the place of exactly the listed sentence text, so it must be valid LaTeX there: it must leave
  the same unmatched braces as the original sentence (if the sentence opens a \footnote{ that closes in a later
  sentence, the replacement opens it too; if it closes one, the replacement closes it too).

DELIVER exactly one fenced block ```csv with the header
id,replacement
One row per listed sentence, in order. Quote every replacement field with double quotes (a double quote inside it is
doubled). An unchanged sentence is copied exactly. After the block, one line with the numbers of changed, unchanged
and emptied sentences.

BEGIN TEX
@@TEX@@
END TEX

BEGIN SENTENCES
@@SENTENCES@@
END SENTENCES
