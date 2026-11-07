UPDATE AN EDITION: Federigo Enriques, Le superficie algebriche (Bologna: Zanichelli, 1949), printed pages @@PAGES@@.

THE EDITION. A LaTeX transcription of the print, between BEGIN TEX and END TEX. Its conventions: each printed page
begins with "% scan: <scan>", "% !PRINTED <page>" and \weberpage{<page>}; a comment "% ?? uncertain: ..." records a
doubtful reading; a doubt that is still open has a margin note "Dubbio. ..." (listed between BEGIN OPEN DOUBTS and END
OPEN DOUBTS, each with an id); a resolved doubt has a comment "% EDITORIAL Dnnnn RISOLTO: ..." and no note; a misprint
of the print is kept as printed and has a margin note "Stampa. ..." (listed between BEGIN STAMPA and END STAMPA, each
with an id and the proposed correction).

THE AUDIT. A page-by-page audit of these pages against the scans of the print produced the findings between BEGIN
FINDINGS and END FINDINGS, one per line: id | page | line | transcribed reading | scan reading | decision | evidence.
The auditors read the scans; the scan is the authority. Take their scan reading as the print, unless their evidence
says that the reading remains uncertain.

TASK 1. THE TEXT AS PRINTED. For every finding whose decision is "transcription error" or "doubt resolved":
- if the LaTeX differs from the print, give the edit that makes it read as the print;
- if the finding settles an open doubt, give that doubt's id and a one-sentence status in Italian, in the style of the
  edition's resolved doubts ("La scansione mostra ...");
- otherwise (the LaTeX already agrees with the print, and no open doubt is involved), action none.
Change nothing else. Misprints and the author's slips stay as printed in this text.
Deliver a fenced block ```csv with the header
finding,action,doubt,tex_snippet,replacement,status
action: fix | resolve | fix+resolve | none. tex_snippet: copied exactly from the LaTeX, at least 20 characters,
occurring exactly once in it; replacement: the same text reading as the print. Leave tex_snippet and replacement empty
when action is resolve or none, and doubt empty when no open doubt is settled.

TASK 2. THE CORRECTED TEXT. A second version of the edition corrects the errors of the print and the author's slips.
For every finding whose decision is "misprint" or "author's slip", and for every Stampa note, decide:
- correct: a genuine error whose intended reading is certain (a wrong or missing letter, word, index, sign, number,
  symbol or cross-reference, a wrong calculation in a formula), corrected with the smallest change;
- keep: anything else: a correction that would rewrite Enriques's argument or statement (that belongs in the
  commentary, not in his text), an archaic spelling or a deliberate notation, a matter of punctuation or style, or a case
  where the intended reading is not certain.
Several items may name the same error: decide it once and mark the others "same as <id>".
Deliver a second fenced block ```csv with the header
item,decision,tex_snippet,replacement,kind,justification
item: the finding id or the Stampa id. decision: correct | keep | same as <id>. tex_snippet: copied exactly from the
text as it reads after your task 1 edits, at least 20 characters, occurring exactly once; replacement: the same text
with only the error corrected. Leave both empty for keep. kind: misprint | slip | reference | calculation | spelling.
justification: one sentence in English.

Quote every field that contains a comma, a quote or a line break (double quotes, a quote inside doubled). One row per
finding or item, in the order given. After the two blocks, one line with the counts.

BEGIN OPEN DOUBTS
@@DOUBTS@@
END OPEN DOUBTS

BEGIN STAMPA
@@STAMPA@@
END STAMPA

BEGIN FINDINGS
@@FINDINGS@@
END FINDINGS

BEGIN TEX
@@TEX@@
END TEX
