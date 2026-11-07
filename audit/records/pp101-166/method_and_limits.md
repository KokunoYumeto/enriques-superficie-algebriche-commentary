# Method, coverage, and limits

## Materials and endpoint

The audit concerns Federigo Enriques, *Le superficie algebriche* (Bologna: Zanichelli, 1949), Chapter IV, as represented by the two supplied source files. The accompanying prompt requests four deliverables; those four files, and no supplementary files, are contained in the delivered archive.

| Supplied material | What was inspected |
|---|---|
| PROMPT(3).md | The complete task specification. |
| enriques_pp101-166.tex | All 2,272 source lines, including comments, notes, every displayed formula, and all 31 “% ??” markers and 29 “[sic]” annotations. |
| enriques_scans_pp101-166.pdf | All 66 supplied scan positions. Positions 1–65 contain the printed mathematical text on pp. 101–165; position 66 is blank. The scan, rather than the first-pass transcription or its comments, controls the reported printed reading. |

The chapter has 21 numbered sections. Its §1 is the *Introduzione*. There is no separate introductory chapter or other chapter in the supplied excerpt. The commentary consequently has one Chapter IV treatment, subdivided into all 21 source sections, followed by independent modern proofs, examples, and references.

Source identities are recorded by SHA-256 so that page and line references remain reproducible:

| File | SHA-256 |
|---|---|
| Prompt | 1b2322caf20ea372e5b825b217a1aa62907a129cea6ec72a317282d0c611d100 |
| LaTeX transcription | c6cf72b1eff46b419e0267264457776dc885283160bb3c043305497e99beb3aa |
| PDF scan | d456aa4705f70a7581663832eb995ae8d13baee1d8ed9159acf32a58c197da85 |

## Reading and verification procedure

The source text was read sequentially through the final degeneration formulas. Parallel audits of §§1–7, §§8–14, and §§15–21 provided independent local checking. The principal reviewer read the entire transcription, integrated every section report and claim record, and independently recomputed the principal identities, examples, counterexamples, and repairs. All scans were inspected in the section audits; disputed mathematical readings received additional visual checks during integration.

The scans were rendered at 150 dpi for page-by-page inspection, with higher-resolution crops where small signs, indices, or punctuation required them. Rendered files were checked for completeness; incomplete initial image renders were regenerated before they were used. Printed page numbers, PDF page positions, and global transcription line numbers were kept separate. In the correction register, “TeX line” means the global line in the original, unmodified attached transcription, not a line in this commentary.

For each mathematical passage the audit asked four distinct questions:

1. What is the statement on a smooth projective surface, and what is the relevant divisor or sheaf?
2. What argument does the excerpt actually supply, and which assertions are imported from earlier work?
3. Does the argument establish the stated result with its printed hypotheses?
4. If it does not, is the problem a transcription error, a printed local slip, an omitted hypothesis, or a genuinely incomplete argument?

This separation matters. An index corrected by arithmetic is not automatically a transcription error: the scan must first show whether the incorrect index was printed. Conversely, the transcription's own “[sic]” annotations are hypotheses to check, not authoritative editorial judgments.

The main computations were independently reconstructed with exact sequences for effective Cartier divisors; curve and surface Riemann–Roch; Serre duality and ample-twist vanishing; adjunction; the Hodge index theorem; point-blowup formulas; numerical connectedness; and canonical double-cover resolution. The argument for nonreduced connectedness is given explicitly, rather than referred to by name alone. Worked examples test both the mathematical statements and their scope.

## How to use the files

**commentary.md** follows the printed section order. It states the modern content, identifies what the author proves or only sketches, evaluates dependencies, and supplies modern repairs and worked examples. The independent proofs at the end gather mechanisms used repeatedly, avoiding a separate full proof of surface Riemann–Roch in every section.

**claims.csv** is an assertion register. Its columns are:

- **id**: stable identifier within this audit;
- **page**: printed page or page range;
- **statement_modern**: the assertion in current mathematical language;
- **kind**: one of the five proof-status categories requested in the prompt;
- **gap_or_error**: the diagnostic, if any;
- **repair_and_reference**: a derivation or a verified replacement reference;
- **notes**: the source section and transcription location, with interpretive qualifications.

The proof-status label records the author's treatment, not a certification of correctness. Thus a row marked “proved” can have an invalid step identified in its diagnostic. A passage giving several inseparable pieces of one identity or one hypothesis is sometimes retained in one row. Conversely, distinct steps in a longer argument have separate rows. Repeated historical statements are recorded in their respective source locations where their role changes.

**transcription_corrections.csv** preserves both the transcription and the observed scan reading. The mathematical correction, where different from the scan, is stated in the decision or evidence field. Every supplied “% ??” has a disposition, including punctuation doubts that do not affect the mathematics. Every supplied “[sic]” annotation was also examined. Additional unflagged discrepancies discovered by the mathematical audit are included. “Author's slip” and “misprint” distinguish the character of a printed error, not its demonstrable origin: a scan cannot determine whether the author, editor, or compositor introduced it.

The CSV files are UTF-8 and use quoted fields where needed. Mathematical notation is plain Unicode and TeX-style text inside cells. A spreadsheet program may display long cells incompletely unless wrapping is enabled; the file contents are not truncated. No formulas, macros, or executable payloads are used in either CSV.

## Modern hypotheses and historical attribution

The default modern setting is a smooth connected projective surface over the complex numbers. The source's ordinary projected surface in three-space can be nonnormal; it is not silently identified with its smooth model. Arithmetic genus of a surface, arithmetic genus of a divisor, geometric genus of a curve, and geometric genus of a surface are distinguished throughout.

Characteristic zero is retained for the vanishing arguments that require it. No assertion of unrestricted positive-characteristic validity is made. Numerical, algebraic, and linear equivalence are distinguished even when the source uses the same equivalence symbol. “Sufficiently large” is replaced by a precise ample-twist condition when the printed wording does not guarantee the necessary vanishing.

Historical citations printed by Enriques are preserved as historical attributions. A reference appearing in his footnote is not thereby an independently verified proof. The bibliography distinguishes references actually consulted for mathematical statements from older works whose metadata or attribution was checked without a full reading of the original argument. When an older title, date, or pagination could not be verified, no missing detail has been invented.

The modern repair of §17 is attributed specifically to a verified theorem: Ramanujam (1972, Lemma 3; reprint p. 127), with the accessible treatment in Reid (1996, Lemma 3.11). The more general curve-theoretic replacement used for the bicanonical argument is Catanese et al. (1999, Theorem 3.3). These citations identify rigorous subsequent formulations. They are not claims to have established absolute priority among all intervening papers.

The commentary's counterexamples, direct computations, and branch-curve reconstructions are explicitly identified as worked checks supplied for this audit. “Original” in that context describes authorship of the present derivation, not a claim that the example or mathematical idea is new to the literature. Confidence is stated for the additional proposals.

## What remains limited or unsettled

1. **Unprovided context.** Earlier chapters, the complete proofs in Enriques's cited nineteenth- and early-twentieth-century papers, and later chapters are not part of the supplied corpus. Their use is identified at the point of dependence. The audit supplies a modern proof where needed for the main result, but does not claim to have exhaustively audited every cited work.

2. **Historical priority.** Some statements about who first obtained a result, and retrospective judgments about what earlier authors “implicitly” knew, cannot be certified from this excerpt. They are reported as Enriques's claims. The bibliography records verified metadata and flags the limits of original-source inspection.

3. **Genericity in classical geometric constructions.** Generic projection, smoothness of general members, independence of imposed conditions, and algebraicity of a swept-out family are not inferred merely from a dimension count. Where the excerpt compresses these steps, the commentary either supplies a modern exact-sequence or vanishing proof, gives a more explicit construction, or identifies the remaining local limitation. This does not turn every compressed classical argument into a false theorem.

4. **The Campedelli extension on p. 123.** The printed degree and multiplicity letters are inconsistent. Under explicit genericity and ordinary-singularity hypotheses, the commentary independently reconstructs the broader torsion-index family: the quadric pencil has spatial degree $4m$ and eight $m$-fold base points, its section ring has weights $(1,1,m)$, and for $n=ms$ the invariants are $p_a=n-1$ and $q=g(B)=(s-1)(n-2)/2$. For $n\ge3$, irregularity requires $s>1$; the boundary $s=1$ is regular. What remains unverified is Enriques's exact intended lettering and the correspondence with the complete scope of Campedelli's original 1936 article, not the calculation for this explicitly reconstructed generic family.

5. **Arbitrary singularities.** The multiple-curve postulation calculation is justified for the smooth curve or ordinary-singularity framework actually used. Multiplicity and geometric genus alone do not determine corrections for an arbitrary singular thickening. The unspecified corrections for more complicated singularities are left dependent on the actual ideal or resolution, rather than replaced with a guessed universal formula.

6. **Degenerations.** The final formulas are proved with the scheme-theoretic gluing and dualizing hypotheses stated in the commentary. They do not prove that every proposed union is smoothable. The invariance claims in a family require flatness and appropriate relative dualizing conditions.

7. **Typographic attribution.** The scan can settle what is printed. It cannot distinguish an author's algebraic slip from a compositorial alteration with certainty. Where that distinction is unknowable, the record identifies a printed source error and gives the verified mathematical correction.

Every supplied uncertainty marker has an explicit disposition. Where the scan does not distinguish a printed glyph from incidental ink, the register records the adopted reading, its contextual justification, and the remaining optical uncertainty. In particular, the apparent prime at TeX line 400 has moderate optical confidence, punctuation at line 1428 remains optically weak, and the damaged subscript at line 2235 is restored from context. The other limitations concern mathematical scope, unprovided historical sources, or intended notation. They are not a request for further pages in order to complete the four requested files.

## Mechanical checks

The archive was checked for the exact four requested members. Both CSV files were parsed after serialization, their headers and field counts checked, and their identifiers and source-flag coverage checked. All 21 numbered sections and all 65 pages containing mathematical text are represented in the claim register. The archive was tested for successful extraction and member integrity.

### Final counts

The register contains **397 claims** and **91 correction/disposition records**. It covers all **21 source sections**, all **65 pages containing mathematical text**, and all **60 supplied editorial flags**: **31 doubts** and **29 “[sic]” annotations**. The final supplied scan position is blank.

| Proof-status category | Records |
|---|---:|
| definition | 33 |
| proved | 177 |
| sketched | 87 |
| stated without proof | 49 |
| assumed from earlier work | 51 |

| Correction decision | Records |
|---|---:|
| transcription error | 4 |
| author's slip | 28 |
| misprint | 28 |
| "% ??" resolved | 31 |

Decision totals must not be confused with source-flag totals. Some flagged readings are settled in records classified as a printed slip or a misprint; three unflagged layout checks also use the resolved-reading category, explicitly identified in their evidence. Several source lines have separate records for a visual question and a mathematical question. These are intentional, not duplicate corrections.

### Section and page coverage

| Source section | Printed pages | Claim records |
|---|---|---:|
| §1 | 101–102 | 10 |
| §2 | 102–106 | 19 |
| §3 | 107–110 | 18 |
| §4 | 110–114 | 27 |
| §5 | 114–117 | 22 |
| §6 | 117–120 | 17 |
| §7 | 120–123 | 31 |
| §8 | 123–127 | 23 |
| §9 | 127–128 | 12 |
| §10 | 128–131 | 14 |
| §11 | 131–134 | 13 |
| §12 | 134–137 | 20 |
| §13 | 137–142 | 18 |
| §14 | 142–147 | 26 |
| §15 | 147–150 | 23 |
| §16 | 150–152 | 12 |
| §17 | 152–156 | 15 |
| §18 | 156–158 | 25 |
| §19 | 158–162 | 31 |
| §20 | 162–163 | 8 |
| §21 | 163–165 | 13 |

All printed page numbers 101 through 165 occur in at least one claim record. Ranges include passages continued across a page boundary. Stable claim identifiers retain their regional prefixes A, B, and C; the rows are ordered by original transcription location, so an identifier added during verification can appear between earlier identifiers.

### Reproducibility and editorial transformations

The supplied transcription was not modified. Final assembly normalized math delimiters in the commentary, unified the four correction-category spellings, expanded a few claim page ranges to match continued source passages, and corrected spacing in the newly authored audit text. None of these transformations changes the recorded source reading. The CSVs were authored as text-valued worksheets, read back, serialized as UTF-8 CSV, and parsed again to verify all cell values. Their content is text, including the mathematical expressions; there are no spreadsheet formulas.

