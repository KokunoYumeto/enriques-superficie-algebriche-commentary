# Method and limits

## Materials and scope

The task was taken from the supplied PROMPT(2).md. The textual materials were the entire first-pass LaTeX file, enriques_pp001-040.tex, and the entire 55-page scan PDF, enriques_scans_pp001-040.pdf. The scan was treated as the authority. No revised transcription was substituted for either original, and neither original was modified.

The substantive scope is the front matter, the whole Introduzione (§§1–5, printed pp. 1–13), and the whole first chapter (§§1–13, printed pp. 15–40). Printed p. 14 is blank. The contents list later chapters, but their headings are not evidence that their proofs have been supplied. The commentary includes modern context for forward references without pretending to have audited those absent chapters.

### Pagination map

| PDF page(s), counted from 1 | Content |
|---|---|
| 1 | Blank opening scan |
| 2 | Title leaf |
| 3 | Copyright and printing leaf |
| 4–7 | Castelnuovo's preface, corresponding to V–VIII; first folio unprinted |
| 8–9 | Enriques's preface, corresponding to IX–X; first folio unprinted |
| 10–14 | Contents, corresponding to XI–XV; first folio unprinted |
| 15 | Blank leaf |
| 16–28 | Introduction, printed pp. 1–13 |
| 29 | Blank printed p. 14 |
| 30–55 | Chapter I, printed pp. 15–40 |

For every Arabic-numbered book page, PDF page = printed page + 15. At the opening of Chapter I the number 15 is handwritten rather than a printed folio. The correction ledger gives both printed positions and approximate TeX line numbers, allowing the readings to be located without relying on line wrapping in a Markdown viewer.

### Input identity

SHA-256 hashes identify the exact supplied files:

| File | SHA-256 |
|---|---|
| enriques_pp001-040.tex | b1c702071721354e220a75c7eba0e76133dffae4aee7537bf7b7789d69a5483e |
| enriques_scans_pp001-040.pdf | afa89e1a93d652d11ef2768df8869c68e752eea7b7f89a587a1cfc87eae18f28 |
| PROMPT(2).md | fd61d2f0ad8c6acdba0c86b6dfb668253863709ffe947dbc168fae15da00fe75 |

## Reading and verification procedure

Every page of the PDF was rendered and visually read, including the front matter and blank leaves. The initial full-page renders used 130 dpi. Ambiguous passages were revisited with enlarged crops from the PDF, including the publisher line, preface punctuation, contents headings, the p. 16 fraction, the p. 23 punctuation, the p. 30 ambient-space index, and the p. 39 footnote and component notation. Enlargement does not create missing optical information; confidence is bounded accordingly.

The full 1,378-line TeX file was read. All 26 occurrences of the exact uncertainty marker “% ??” were enumerated mechanically and compared with the corresponding scans. All explicit “[sic]” annotations were also checked, rather than accepted as evidence that the author made an error. Additional questionable formulas, letters, historical references, and hypotheses were checked whenever the mathematical reconstruction raised an issue.

Three parallel readers prepared working analyses for the Introduction, Chapter I §§1–8, and Chapter I §§9–13. The primary reader independently read the source text and all 55 scan pages, read and integrated all three commentaries and ledgers, and checked the central calculations and counterexamples. Work was divided to gain independent scrutiny, not to replace the requested complete integration.

For mathematical checking, each assertion was translated to a specified smooth projective model over the complex numbers. Definitions and short algebraic arguments were verified directly. Longer arguments were reconstructed using divisor and normal-sheaf sequences, intersection theory, adjunction, surface Riemann–Roch, the Picard scheme, blowups, and proximity. Proof status in the ledger records what the *supplied book pages* do; the repair column and commentary separately explain the modern justification.

The audit distinguishes the following:

1. A transcription error, where the TeX and scan disagree.
2. A source slip or misprint, where the scan confirms the problematic symbol or phrase.
3. A missing hypothesis or incomplete proof, which is usually a claim-ledger issue rather than an emendation of letters.
4. A historical convention whose modern translation requires care but is not itself a mistake.
5. A correct result imported or postponed by the source, for which the audit supplies a modern argument or a precise external dependency.

The labels “author's slip” and “misprint” describe the kind of source-level problem. The scan cannot establish whether an individual wrong symbol originated with Enriques, a copyist, an editor, or the compositor. No claim about personal responsibility is intended.

## Mathematical checks with concrete outcomes

The main independent checks include the following:

- The graph-closure counterexample was verified by its explicit inverse rational map, twisted-cubic equations, dimension, and tangent space.
- The degree of a system of order-n cones on a degree-m surface was recomputed as mn² by pullback and intersection.
- The cubic-map counterexample on the blowup of one plane point was checked through its base ideal, rational inverse, exceptional restriction, and moving square.
- The residual-system theorem was proved using multiplication of sections. The completeness of adjoint cuts was checked through the conductor ideal and vanishing of intermediate cohomology on projective three-space.
- Surface Riemann–Roch was reduced to curve Riemann–Roch and adjunction, and all virtual degree/genus, sum, multiple, difference, and blowup formulas were expanded.
- The free exceptional chain and first satellite configuration were checked with their full intersection matrices and total-transform multiplicities. The indexing defects on p. 38 were separated from the correct final invariants.
- The p. 40 auxiliary-series claim was tested with its cohomological obstruction formula and an explicit elliptic-product example.
- The distinction between characteristic directions and actual deformations was expressed through both connecting homomorphisms, with the semiregularity theorem explicitly identified as an additional input.

The ordinary-model existence argument is proved after a sufficiently ample re-embedding, using bounded jet separation and the explicit crosscap normal form. The stronger ordinary-projection theorem for an arbitrary fixed smooth embedding is separately identified. The Franchetta theorem for a smooth surface in projective five-space is proved using the secant incidence and Bertini, with the defective-surface classification stated as the precise additional dependency needed to identify the Veronese exception.

This is a complete audit of the supplied pages, not a claim to derive all of algebraic geometry from first principles. Surface resolution, the Hodge index theorem, Stein factorization, coherent cohomology and duality, the construction and smoothness of the Picard scheme, the semiregularity theorem, and the classification implication “all plurigenera vanish implies birationally ruled” are explicit external theorems where used. Reproducing the entire proof of each foundational theorem would go well beyond the statements and arguments in this extract.

## Reference policy

References were checked against primary papers, author preprints, journal or publisher records, and the Stacks Project. The commentary uses author–date citations and APA-style bibliography entries with page, section, theorem, or stable-tag pointers when these were verifiable. An exact original proof was not declared inspected merely because a bibliographic record was found.

The most consequential historical comparison was with Enriques's 1893 linearity paper: its original statement already imposes irreducibility and its text supplies the reducible counterexample. The repair in this audit therefore restores his own earlier hypothesis. The component-family gap in the Bertini argument is distinguished from that case: Kleiman's checked historical analysis documents van der Waerden's use of Chow coordinates and Zariski's alternative.

For the characteristic-series problem, the reference check distinguishes Grothendieck's Exposé 221, §§5.4–5.6, from his later Picard exposés 232 and 236. It also distinguishes Kleiman's two publications titled The Picard scheme (2005 and 2014). A page-range discrepancy for Kleiman's 1973 paper is disclosed rather than copied silently.

The independent examples and reconstructions in the commentary are labelled as the commentator's, with confidence and reasons. They are not assigned invented historical priority. A modern textbook citation means a source for a theorem or language, not evidence that its author repaired the particular line under discussion.

## Limits and unsettled details

### Optical and editorial limits

Every “% ??” has an editorial decision, but not every tiny mark has a physically demonstrable origin. The title and contents specks, the dot after page reference 56, and the tiny prime-like mark after S on p. 5 cannot always be distinguished definitively as deliberate type, stray ink, or scanning dirt. The correction ledger states the best diplomatic reading and the normalized editorial decision separately. The p. 12 minute punctuation is also given with bounded confidence. No mathematical conclusion depends on these optical uncertainties.

The log is a targeted complete resolution of the flagged readings and mathematically significant discrepancies, with additional observed spelling and bibliographic issues. It is not a claim that every accent, space, capitalization choice, line break, or stain has been exhaustively catalogued. A full diplomatic edition would be a separate deliverable.

### Historical-source limits

The original full texts of every work mentioned in the 1949 footnotes were not accessible or not supplied. In particular, the complete Enriques–Chisini volumes, the full early resolution papers of Levi, Chisini, and Albanese, all of Franchetta's original proof, and the specific Castelnuovo letter referred to on p. 40 were not independently audited. Their references are preserved with the level of verification actually achieved.

The 1940/1941 discrepancy in later references to Franchetta's first paper is disclosed. Missing titles, page ranges, or exact Lefschetz passages are not fabricated. Barber–Zariski (1935) and Du Val (1936) were identified bibliographically, but their full proofs were not represented as directly inspected. The specific obstruction-theory pages in Mumford are verified through Kleiman's checked account rather than a complete independent reading of the book. Exact verification notes accompany the relevant bibliography entries.

### Interpretive and mathematical limits

The source's word “series” on p. 40 may intend the completed intrinsic linear series, or may suppress a sufficiently-positive auxiliary condition. The supplied sentence alone does not decide that intention. The unrestricted equality of actually cut subseries is tested and fails; the line-bundle/completed-series statement is proved.

Likewise, some “virtual” numbers depend on the assigned base cluster. The audit does not erase that historical convention and then manufacture counterexamples to a different statement. When the original wording is genuinely ambiguous, both the safe interpretation and the failure of a stronger literal assertion are described.

The highly compressed specialization steps in Franchetta's printed argument are not claimed to have been recovered verbatim as a complete scheme-theoretic proof. A rigorous alternative is supplied, and the remaining textual reconstruction problem is identified. The underlying characteristic-zero theorem is not described as currently open.

No general positive-characteristic extension is claimed. Separability, generic smoothness, the Wronskian argument, and smoothness of the Picard scheme have been used where stated. No unsupported appeal to Kodaira or Bombieri–Mumford substitutes for proving a step relevant to this extract.

## Deliverable conventions

The ZIP contains exactly four UTF-8 files. The two CSVs use quoted fields and one header row. Claim identifiers are stable within this package and preserve source order by section. “Proved” records the presence of a proof in the source; the error column must still be read. Repeated explanatory modern formulas do not create fictitious new source claims.

The final package was checked for CSV parseability, duplicate identifiers, coverage of every uncertainty marker, complete page and section coverage, stray placeholders and control characters, and ZIP integrity. The original supplied files were left unchanged.

## Coverage and package checks

The integrated ledger has **379 claim rows** and the correction ledger has **53 entries**. The exact uncertainty marker occurs on **26 TeX lines**; '[sic]' occurs on **12 lines**. Every such line has a corresponding correction record. One flagged line can support more than one entry—for example, p. 39's footnote has both a transcription discrepancy and a printed misreference—so row totals are not counts of independent source errors.

| Source range | Claim identifiers | Claims | '% ??' TeX lines |
|---|---|---:|---|
| Front matter | FM001–FM003 | 3 | 27, 131, 133, 178, 197, 199 |
| Introduction, pp. 1–13 | IN001–IN104 | 104 | 434, 502, 506, 533, 561, 592, 632, 651 |
| Chapter I §§1–8, pp. 15–30 | LS001–LS156 | 156 | 707, 900, 901, 909, 1069 |
| Chapter I §§9–13, pp. 30–40 | EC001–EC116 | 116 | 1090, 1201, 1353, 1354, 1362, 1376, 1378 |

The '[sic]' lines are 131, 336, 453, 634, 645, 647, 773, 803, 876, 910, 1004, 1352.

| Source presentation status | Claim rows |
|---|---:|
| definition | 57 |
| proved | 115 |
| sketched | 114 |
| stated without proof | 58 |
| assumed from earlier work | 35 |

These counts classify the presentation, not the truth value. A source argument containing a local slip can still be marked proved when an argument is actually supplied; its error and repair fields must be read. Conversely, a sound modern proof in the commentary does not change a source announcement into a proof on the supplied page.

Final validation decodes all four files as UTF-8, parses both CSVs, checks their exact headers and allowed category values, checks unique claim identifiers and all nonblank numbered pages, checks every flagged line against the correction ledger, checks Markdown math-delimiter balance and control characters, verifies the original input hashes, and tests the ZIP's member list and CRCs. The archive contains only commentary.md, claims.csv, transcription_corrections.csv, and method_and_limits.md, with no enclosing directory or working files.
