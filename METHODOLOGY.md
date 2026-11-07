# How this edition was made

Federigo Enriques, *Le superficie algebriche* (Bologna: Zanichelli, 1949). Everything below was done by AI models,
directed by KokunoYumeto, in November 2026. Numbers are measured unless marked as estimates. The prompts are in
[`methodology/prompts`](methodology/prompts).

## 1. The source

Maxim Leyenson's scan of the 1949 print: a DjVu file of 246 bitonal images at 300 dpi, each a two-page spread turned
sideways. A script rotated each spread and cut it into two printed pages (478 page images, front matter included).
Some spreads are in the scan twice (images 61 and 62 both show pp. 102–103). One leaf is missing: printed pages
284–285 are not in the scan, and no other copy was available, so the edition marks the gap and translates nothing
there.

## 2. Transcription

- Model: OpenAI gpt-6-astra (Responses API, Flex tier, reasoning effort max), 6 November 2026.
- Pilot on pp. 100–107 against a cheaper model (gpt-6.1-sol): the two agreed on 3,298 of 3,299 words. A line-by-line
  check of p. 107 against the scan found no error in gpt-6-astra's text; gpt-6.1-sol misread two places that
  gpt-6-astra had right. gpt-6-astra was used for the whole book.
- Each page was sent whole and as three enlarged overlapping strips, so that small type stays readable after the API
  scales the image down. The model marked readings it was unsure of (`% ?? uncertain: ...`) and apparent misprints of
  the print (`[sic]`).
- Whole book: 50 requests, 4.46 million input tokens, 2.11 million output tokens, $75.06 at Flex prices.

## 3. The reader edition

ChatGPT (Pro mode) typeset the transcription as one LaTeX book (pdfLaTeX, 374 pages): the original page numbers in the
margin, the author's footnotes, the INDICE linked to the pages, and numbered margin notes for doubtful readings
("Dubbio", 119) and apparent misprints kept as printed ("Stampa", 201). Every doubtful reading was checked against the
scan. Claude (Anthropic) made further corrections and checks. The ledger `corrections.csv` records each change with its
reason (995 rows in the first version).

## 4. The audits

ChatGPT (Pro mode) audited the edition page by page against the scans, in six runs:

| audit | pages | claims recorded | transcription findings |
|---|---|---|---|
| Introduzione and Capitolo I (detailed) | 1–40 | 379 | 53 |
| Introduzione and Capitoli I–III | 1–100 | 718 | 106 |
| Capitolo IV | 101–166 | 397 | 91 |
| Capitoli V–VI | 167–236 | 521 | 72 |
| Capitoli VII–IX | 237–370 | 1,116 | 185 |
| Capitoli X–XI | 371–464 | 615 | 174 |

Each audit got the edition's LaTeX for its pages, the scans of the same pages and, from the second audit on, the
results of the earlier audits. Its tasks: state every definition, theorem, lemma, formula and claim in modern terms;
say what Enriques proves, sketches or assumes; work through every argument, give repairs for gaps and errors with
references; and check the transcription against the scan wherever the mathematics looked wrong. Each returned a claim
register (`claims.csv`), the transcription findings (`transcription_corrections.csv`), a commentary and a note on
method and limits. All of these are in the commentary's repository.

Across the six audits, the transcription findings were: 35 transcription errors, 244 doubtful readings settled,
177 misprints of the print and 207 slips of the author (some pages were audited twice).

## 5. The commentary

ChatGPT (Pro mode) turned the audits into one commentary in two parts: Part 1 (Introduzione to Capitolo VI) from the
first four audits, Part 2 (Capitoli VII–XI) together with the audit of Capitoli X–XI. Each part was written with the
text and the scans at hand, to settle the points where audits disagreed and to quote Enriques exactly. Claude Opus 5.5
then rewrote the 112 sentences of Part 1 that spoke of how the commentary was made ("the supplied audits") so that they
speak to the reader of the book; a script checked that no other line changed and that every formula and reference was
kept ($1.36). The commentary has 317 pages and is published separately:
[enriques-superficie-algebriche-commentary](https://github.com/KokunoYumeto/enriques-superficie-algebriche-commentary).

## 6. This version: the text as printed, the corrected text, and the English

All three steps used Claude Opus 5.5 through Anthropic's Message Batches API (reasoning effort max), one request per
24 printed pages (20 requests per step).

1. **Italian, as printed.** Each request got the LaTeX of its pages, the open doubtful readings, the Stampa notes and
   all audit findings for those pages, and returned exact edits. Applied: 17 transcription errors corrected and 74 open
   doubts settled (the "Dubbio" notes went from 119 to 51). Two proposed edits were rejected on review: they would have
   reproduced a minus sign that the print repeats at a line break. Cost $18.27.
2. **Italian, corrected.** The same requests decided, for each misprint and slip found by the audits and for each
   Stampa note, whether the corrected text should change: yes only for a genuine error whose intended reading is
   certain, with the smallest change; no for anything that would rewrite Enriques's argument (that belongs in the
   commentary). Applied: 232 corrections (136 misprints, 42 slips, 29 calculations, 18 references, 7 spellings); 146
   proposals kept as printed. Each correction is listed with its reason in `corrections_corretto.csv`.
3. **English.** The Italian as printed was translated part by part, keeping every formula, page marker and macro, with
   a fixed glossary of the classical terms (genere lineare: linear genus, bigenere: bigenus, ...).
   The translation cost $32.33. A script then checked every part against the Italian: every formula, page marker and footnote is the same, apart from translated ordinals (6º becomes 6th) and words inside formulas and tables. A second model, OpenAI gpt-6-astra (Flex, effort max), read each part of the English against the Italian and reported 17 problems ($10.97). A last Claude batch judged them (all 17 were real), fixed 20 further occurrences of the same kinds across the book (mostly classical terms: Enriques's *linea* is a curve, not a straight line; surfaces *irriducibili per trasformazioni birazionali* are birationally inequivalent, not irreducible), and carried the corrections of the corrected Italian into the English: 174 made, 58 with no English counterpart (Italian spelling, agreement and prepositions) ($8.55).

## 7. What went wrong, and what was done about it

- The audit package for Capitoli V–VI dropped p. 186: the raw transcription packet labelled it 184, and pages were
  de-duplicated by printed number. Later packages were built from the published edition's LaTeX, and p. 186 was
  audited as a supplement to Capitoli VII–IX.
- The audit of Capitoli VII–IX came back without its part of the commentary. Part 1 of the commentary was then given
  its own prompt, and Part 2 was written together with the last audit.
- The run for Capitoli X–XI first delivered a working checkpoint: Part 2 written, but the Chapter X claims, the
  transcription findings and the notes missing. A second prompt gave the model its checkpoint to continue from (not
  to redo); 94% of the checkpoint's lines were kept, and the missing pieces were added.
- The checkpoint's LaTeX did not compile with Part 1 (a formula in a section title, parentheses written as math
  delimiters inside formulas, a ≥ the text font lacks). These were fixed mechanically.
- Both parts of the commentary spoke of "the supplied audits", "the supplied transcription" and audit claim numbers.
  The second prompt told the model to write Part 2 for the reader; the 112 sentences of Part 1 were rewritten as
  described above.

## 8. Costs

| step | model | cost |
|---|---|---|
| transcription | OpenAI gpt-6-astra (Flex) | $75.06 |
| reader edition, audits, commentary | ChatGPT Pro (subscription) | — |
| commentary wording (Part 1) | Claude Opus 5.5 (batch) | $1.36 |
| Italian as printed and corrected | Claude Opus 5.5 (batch) | $18.27 |
| English translation | Claude Opus 5.5 (batch) | $32.33 |
| independent check of the English | OpenAI gpt-6-astra (Flex) | $10.97 |
| final English (review and corrections) | Claude Opus 5.5 (batch) | $8.55 |
| **total of the API steps** | | **$146.54** |

API costs are computed from the token counts at the published batch and Flex prices.
