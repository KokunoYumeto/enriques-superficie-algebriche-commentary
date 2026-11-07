# Method and limits

## 1. Scope and completion

This audit covers the supplied front matter and all of the Introduzione and Chapters I–III of Federigo Enriques, *Le superficie algebriche* (Bologna: Nicola Zanichelli, 1949), through printed page 100. It ends with Chapter III, §13. Chapter IV begins on page 101 and is outside the supplied packet. The contents name later results but do not supply their statements or proofs; they have not been treated as additional chapters to audit.

The final archive contains exactly the four requested files:

| File | Function |
|---|---|
| **commentary.md** | Mathematical exposition, source-proof assessments, modern statements and proofs, examples, counterexamples, and annotated APA-style references. |
| **claims.csv** | 718 granular entries, preserving the five requested kinds and distinguishing source assertions from explicitly marked auxiliary results of this audit. |
| **transcription_corrections.csv** | 106 entries, including a decision for every one of the **59 original "% ??" locations**, with additional scan-confirmed discrepancies. |
| **method_and_limits.md** | Coverage, conventions, verification procedure, limitations, and reproducibility information. |

The source PDF and TeX have not been overwritten or silently corrected. A corrected full transcription, a translation, and a facsimile edition were not requested and are not substituted for the commentary.

## 2. What was read

Every line of the supplied transcription was read, including the title, copyright, foreword, preface, contents, notes, footnotes, displays, exercises, running-head flags, and the final paragraph on page 100. Every physical PDF page was visually inspected within the audit. Three parallel reviewers handled the individual chapters; the integrating review independently read the entire transcription and all chapter commentaries, claims, correction records, and verification reports. It also independently reinspected decisive enlarged passages, including the page 43 bibliographic locator, page 45 determinant sign, and page 39 exceptional-curve subscripts. This is combined coverage, not a claim that one reviewer performed every image inspection.

| Unit | Printed pages | One-based PDF pages | Sections | Claim prefix | Original flags |
|---|---|---:|---:|---|---:|
| Front matter | Title, copyright, V–XV, intervening blanks | 1–15 | Editorial material and contents | IN | 6 |
| Introduzione | 1–13; blank 14 | 16–29 | 1–5 | IN | 8 |
| Chapter I | 15–40 | 30–55 | 1–13 | I | 12 |
| Chapter II | 41–65; blank 66 | 56–81 | 1–9 | II | 14 |
| Chapter III | 67–100 | 82–115 | 1–13 | III | 19 |

For Arabic pages, **PDF page = printed page + 15**. Printed 15, 41, and 67 have suppressed page numerals. The numeral on page 89 is not visible or legible in the supplied scan; its placement follows from the sequence and neighboring pages. Printed 14 and 66 are blank. Preliminary physical pages 1 and 15 are also blank. The title and copyright are PDF 2–3; Castelnuovo's foreword is PDF 4–7, Enriques's preface PDF 8–9, and the contents PDF 10–14.

All source pages containing substantive text have claim records or, for editorial and contents material, explicit coverage in the front-matter records. Identical recurring formulas can be grouped into one row with a page range; distinct uses, changes of hypothesis, and nontrivial intermediate determinant or intersection calculations receive their own records. The row count describes the audit's identified units, not a number of theorems formally numbered by Enriques.

The footnote beginning on page 91 continues on page 92 **inside** the packet. Both parts were read. The transcription's comments suggesting otherwise were rejected. The endpoint was checked against both page 100 and the contents: no beginning of §14 has been invented.

## 3. How the scans were used

The facsimile is the textual authority. Its pages were rendered directly with PyMuPDF. The front matter and Introduzione were reviewed at approximately 180 dpi, with uncertain regions at approximately 360 dpi. Chapter I used full pages at roughly 122 dpi and selected crops up to 432 dpi; Chapter II used full pages at roughly 144 dpi and selected crops up to 576 dpi. Chapter III likewise used full-page renders followed by enlarged local regions. No generative image enhancement or reconstructed letterform was used as evidence.

A mathematically implausible expression was not automatically assigned to Enriques. Its scan was checked before classification. The decisions distinguish:

- **Transcription error:** the TeX differs from the visible source. Examples include the false prime on page 80, the overline on the final \(K\) on page 46, the inequality on page 72, and the page 39 footnote marker.
- **Author's slip:** a printed label or mathematical wording is inconsistent with the construction. This identifies a fault in the printed witness; it cannot establish whether Enriques, an editor, or a compositor introduced it.
- **Misprint:** an apparent typographical or indexing fault in the printed witness, such as the missing square on page 22 or the minus in the page 45 determinant.
- **"% ??" resolved:** an editorial reading is selected after inspection, often confirming the transcription. This does not imply that every minute spot has a uniquely knowable physical origin.

When a flagged location also contains a source misprint or transcription error, its decision uses the substantive category and its evidence identifies the flag. Counting only rows with decision '"% ??" resolved' would therefore undercount the checked locations.

Line numbers refer to the **original supplied TeX**, not to the Markdown commentary. They are approximate locators for an affected expression; a following comment can identify a display on the preceding line. The original flagged lines are:

| Unit | Original TeX lines |
|---|---|
| Front matter and Introduzione | 27, 131, 133, 178, 197, 199, 434, 502, 506, 533, 561, 592, 632, 651 |
| Chapter I | 707, 900, 901, 909, 1069, 1090, 1201, 1353, 1354, 1362, 1376, 1378 |
| Chapter II | 1390, 1391, 1426, 1438, 1562, 1573, 1584, 1915, 2013, 2030, 2124, 2134, 2161, 2176 |
| Chapter III | 2258, 2262, 2345, 2347, 2399, 2440, 2455, 2558, 2625, 2652, 2665, 2679, 2704, 2709, 2752, 2791, 2911, 2921, 2973 |

Small typographic uncertainties remain explicit. Examples are isolated dots in the title and preface, the small mark near \(S_r\) on page 5, damaged 'di' on page 23, the comma on page 34, the minute mark after \(n\) on page 41, dotted equalities on page 61, and 'Math-Annalen' on page 62. The register gives a best diplomatic reading, confidence, and mathematical normalization where relevant. A cleaner impression could settle some of these. None is concealed as a secure mathematical error.

Historical spelling, repeated operators used at line breaks, and harmless variants were not automatically treated as errors. Franchetta's double-curve date, 1941 in Enriques versus 1940 in the inspected modern bibliography, remains a reference discrepancy; it is not classified as a proven misprint.

## 4. Mathematical comparison

The setting is smooth projective surfaces over \(\mathbb C\), with singular models treated by normalization and resolution. Characteristic-zero hypotheses are made visible without turning positive-characteristic phenomena into objections to Enriques's setting.

The audit separates linear, algebraic, and numerical equivalence; geometric and arithmetic genus; full divisor classes and moving parts; vector-space and projective dimensions; assigned and actual base conditions; total and strict transforms; scheme normality and historical linear normality; and connected support versus numerical 1-connectedness.

Calculations were checked from adjunction, surface and curve Riemann–Roch, restriction exact sequences, the first-principal-parts sequence, intersection bilinearity, blowup formulas, double-cover algebra, conductor duality, and local valuations. Main proofs are stated relative to these identified inputs. Direct derivations include the homogeneous determinant factorization, contraction bookkeeping, virtual-remainder decomposition, the composite exceptional criterion with an explicit sufficient hypothesis, the projected del Pezzo quintic, the tacnodal and Noether models, the flex dimension, the Campedelli conic/quartic system, and the equivalence criteria.

The kind column usually describes what Enriques supplies **at the cited place**. 'Proved' means an argument is supplied there; it does not say that every foundational theorem is reproved in the excerpt. 'Sketched' records a compressed argument whose missing hypotheses or construction are identified. 'Stated without proof' includes exercises and forward assertions. 'Assumed from earlier work' identifies cited or standard inputs instead of treating their omission as a new gap. Audit-only auxiliary results and counterexamples are explicitly labeled in notes; for those rows, 'proved' refers to the displayed modern proof.

A repair can be an added hypothesis, a corrected source expression, a fuller argument, or a modern replacement. In particular:

1. The page 59 orthogonal-addition statement is false under an effective-remainder reading but valid with a possibly virtual remainder. Both the counterexample and general virtual proof are supplied.
2. Numerical 1-connectedness is a sufficient hypothesis added to the page 60 characterization. It is not falsely attributed to a definition in Chapter I.
3. The page 80 adjunction equations are correct in the scan. The TeX introduces a prime and then proposes a false correction to the other equation.
4. The trace normalization on pages 97–99 introduces unaccounted vertical poles. An explicit example verifies that defect. The second criterion is repaired by a generic-fiber divisor argument; the index-greater-than-one result is proved with a complete flat family of integral curves and the stated restriction hypotheses.

The audit does not reprove all of resolution of singularities, secant-defective surface classification, Kodaira vanishing, or minimal ruled surface classification from first principles. These are named modern inputs with checked references. Their use is visible and is not attributed to an unverified historical repair.

## 5. Reference verification and historical attribution

References use author–date form, stable URLs, and verified theorem, proposition, section, or page locators. The annotations distinguish inspected mathematical text; inspected publisher, journal, author, or institutional metadata; and a citation reported by Enriques or another checked bibliography.

Primary modern materials consulted include the Stacks Project on resolution, contraction, divisors, principal parts, and see-saw; author-hosted notes of Brosnan and Milne; Ciliberto–Flamini and Lopez–Ran on generic projection; Kleiman on Bertini; Friedman–Lehman–Leyenson–Teicher on projected models; Ein–Lazarsfeld on adjoint ideals; Calabri–Ferraro on double-point resolution; and Dolgachev on Enriques surfaces. Textbook locators are qualified when checked through an accessible mathematical source instead of by reading the entire textbook.

A historical repair attribution requires documentary evidence. The algebraicity issue in the classical proof of Bertini's second theorem is a case where Kleiman documents van der Waerden's 1937 contribution with a precise locator. Independent reconstructions here are not assigned to Zariski, Kodaira, Mumford, or another mathematician merely because their methods are used.

Several original historical texts were not available or were not inspected in full: some Enriques–Chisini and Enriques–Conforto passages; original Franchetta double-curve and exceptional-curve papers; the full Barber–Zariski and Du Val proofs; Pedoe's article; and parts of the Noether, Segre, Bertini, Severi, and Torelli literature. Identified titles and dates are separated from readings of proofs. The page 43 citation really says **Book XV, volume II**; no replacement locator is fabricated. The official Enriques archive verifies the 1893 *Ricerche* offprint and 1894 journal version, so the earlier date is not automatically corrected.

## 6. Substantive limits that remain

The complete review does not turn every historical sketch into a verified original projective construction.

- **Introduzione, pages 12–13:** the principal irreducibility theorem has a modern proof under its stated embedding and projection hypotheses. The original specialization argument and every formulation for a singular \(\mathbb P^4\) model were not independently verified in Franchetta's original paper. The commentary identifies the omitted specialization justification without claiming that the cited paper repeats it.
- **Chapter II, page 60 footnote:** the \(p_g>0\) composite exceptional criterion receives a full proof with numerical 1-connectedness. The exact scope of Franchetta's broader \(p_g=0\) exception was not independently recovered and is retained as a qualified earlier-work assumption.
- **Chapter III, page 89:** the full imposed system at the specified flex has projective dimension four. Its degree, genus, elliptic contraction data, and inverse divisor class are checked. An explicit four-section subsystem is constructed by projecting the complete image from a suitable point of its rank-four quadric. The proof establishes the ordinary quadruple and triple lines, the isolated double point with an infinitely near tacnode, the canonical adjoint cubic, and coordinate formulas for the inverse. This is the audit's reconstruction under sufficient general-position hypotheses, including exact order-two tangent-plane contact and no further line on the quartic; it does not assert the same projective configuration for every specialized input or arbitrary subsystem. The quartic coordinate representatives of the inverse are not claimed to have minimal degree.
- **Chapter III, page 100:** Torelli's assertion appears without an explicit inequality or normalization. Its bibliographic record was located, but the original full text was not inspected. No formula or equality hypothesis was invented. Baker's related Severi-lemma discussion is not represented as a verified repair of the surface trace proof.

These are disclosed mathematical or documentary boundaries, not omitted pages. Further examples are labeled as the audit's ideas with confidence and reasons. Historical verification questions are not described as open mathematical conjectures.

## 7. File validation and reproducibility

The CSVs use UTF-8, RFC 4180 quoting, and the requested column order. All fields are literal text, including Unicode or TeX formulas. Empty fields mean no additional qualification is supplied there; they are not missing columns. Text was authored as worksheet values and exported without formula evaluation. Every cell was compared with its source record and the CSV reimported to verify exact preservation.

Validation checked unique claim IDs, allowed proof-status and decision values, required fields, nonblank-page coverage, all 59 flagged-line inclusions, complete CSV round trips, balanced Markdown math delimiters, absence of unintended control characters or working citation IDs, and the archive's exact four-member list and integrity. Selected worksheet ranges were visually inspected. These checks validate structure and preservation; they do not replace mathematical reading.

The source witnesses have these SHA-256 hashes:

| Source | SHA-256 |
|---|---|
| enriques_pp001-100.tex | 0cad2d42fd59e08b8ca1ee1e5fd976df1fb0731bec1b85ffebf32f6903f45d47 |
| enriques_scans_pp001-100.pdf | 99faa1cde87cc0cbbeec7931ade38a2770fa08264927b8aad1b03f8ead38ffa3 |

The review and reference-access date is **6 November 2026**.
