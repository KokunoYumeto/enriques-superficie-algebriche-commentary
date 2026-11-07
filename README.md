# A mathematical commentary on Federigo Enriques, *Le superficie algebriche* (1949)

A chapter-by-chapter commentary on Enriques's treatise on algebraic surfaces, in English: what each chapter states and
proves, section by section, in modern terms; the status of each proof (complete, sketched, stated without proof,
assumed from earlier work); every gap and error found, with its repair and a reference; counterexamples; worked
examples; page references to the book. It covers the Introduzione and all eleven chapters (317 pages).

It accompanies the edition of the book, which gives the Italian text as printed, a corrected Italian text and English
translations: [KokunoYumeto/enriques-superficie-algebriche](https://github.com/KokunoYumeto/enriques-superficie-algebriche).

- [Commentary, PDF](https://github.com/KokunoYumeto/enriques-superficie-algebriche-commentary/releases/download/commentary-2026-11-08/Enriques_Superficie_algebriche_commentary.pdf)
- [LaTeX source](commentary/): `main.tex` with Part 1 (Introduzione, Capitoli I–VI) and Part 2 (Capitoli VII–XI);
  it compiles with LuaLaTeX.
- [Audit records](audit/records/): the page-by-page audits the commentary is built from. For each range of pages:
  `claims.csv` (every definition, theorem, lemma, formula and claim, with its status, the gap or error found and the
  repair), `transcription_corrections.csv` (readings checked against the scans), `commentary.md` (the auditor's notes)
  and `method_and_limits.md` (what was read and what could not be settled).
- [Methodology](METHODOLOGY.md), with the prompts used.

## How it was made

The commentary is AI-produced. An AI model (ChatGPT, Pro mode) audited the published edition page by page against the
scans of the 1949 print, in six audits (November 2026), and then wrote the commentary from those audits, checking the
text and the scans wherever the audits disagreed. Some sentences of Part 1 were revised for the reader by another AI
model (Claude Opus 5.5, Anthropic). No human mathematician has reviewed it. Errors certainly remain: please report them
as issues, with the page.

Pages 284–285 of the book are missing from the only available scan, so the commentary does not cover them.

## Rights

The commentary quotes Enriques's book, which is in the public domain in the European Union (Enriques died in 1946).
To the extent that we hold rights in the AI-produced commentary and audit records, they are dedicated to the public
domain under CC0 1.0. This work is published for educational, non-profit purposes, and we claim no rights we do not
hold. If you hold rights in this work and object to its publication here, please open a GitHub issue and we will take
it down.

---

[Sponsor this work](https://github.com/sponsors/KokunoYumeto)
