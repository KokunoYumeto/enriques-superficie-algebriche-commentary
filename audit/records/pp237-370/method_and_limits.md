# Method and limits

## Materials and exact coverage

The audit uses the two supplied witnesses: `enriques_pp237-370.tex` and `enriques_scans_pp237-370.pdf`. The mathematical source is Federigo Enriques, *Le superficie algebriche* (Zanichelli, 1949); the scan is authoritative for its visible printed readings. The transcription and its editorial apparatus are aids to locating passages. Neither the `% edition note:` labels nor the incoming `RISOLTO` annotations were treated as independent evidence.

The PDF has 133 images. The prompt's 132-page chapter excerpt consists of 131 text-bearing pages and the blank final image; the supplementary leaf adds one image. The inventory is:

| Material | Printed or assigned pages | PDF images, counted from 1 | Available text-bearing pages |
|---|---|---|---:|
| Supplement to Chapter V | 186, assigned by supplied apparatus | 1 | 1, partly occluded |
| Chapter VII | 237–266 | 2–31 | 30 |
| Chapter VIII, first part | 267–283 | 32–48 | 17 |
| Missing interval | 284–285 | None | 0 |
| Chapter VIII, continuation | 286–324 | 49–87 | 39 |
| Chapter IX | 325–369 | 88–132 | 45, including partly occluded 368 |
| Final blank image | Handwritten 370; scan label s198L | 133 | 0 |

The three chapter-opening pages have no visible printed folio and are assigned 237, 267, and 325 by their positions. The first image's underlying folio is not independently legible. The displaced numbers 184 and 185 belong to overlapping material and must not silently replace the supplied assignment 186. On the image assigned 368, the exposed displaced numbers 352 and 353 likewise belong to overlapping leaves.

The **Introduzione** in `commentary.md` is the audit's own introduction and notation/proof framework. No separate introductory chapter of Enriques's book was included in the supplied excerpt, and none is represented as having been read.

## Reading, comparison, and integration

The complete supplied TeX was read in page order, including displays, footnotes, prose assertions, qualifications such as “in generale,” retractions, and edition warnings. Separate chapter audits were prepared in parallel. The integrating reviewer also read the entire supplied source text and then read and reconciled all three chapter commentaries and registers. This was not a summary generated from chapter titles or selected pages.

The chapter reviewers inspected the available page images, using enlarged crops for doubtful type, signs, subscripts, primes, punctuation, and overlapping fragments. The integrating review independently inspected the supplement and critical chapter images where a substantive mathematical error, ambiguous reading, or proposed emendation affected the result. The work therefore combines a complete textual reading, chapter-level visual comparison, and a second visual check of material findings. It does not claim that the integrating reviewer personally repeated every crop inspection performed in the chapter audits.

Arguments were checked by translating the historical notation into divisor classes and line-bundle cohomology. Recurring checks include adjunction; surface and curve Riemann–Roch; the distinction between arithmetic and geometric genus; correction terms for blowups; trace splitting and canonical bundles of double covers; moving self-intersection versus image degree; the dimensions of complete versus incomplete linear systems; and the difference between tangent vectors and actual divisor deformations. A shared notation framework in the Introduzione makes these checks reproducible.

Independent computations were used where a numerical claim could be tested directly. Examples include the cusp sign in the p.186 correspondence calculation; parameter counts; the degree-seven tricanonical image of the classical Godeaux quotient; the weighted canonical ring with $p_g=2$, $K^2=1$; the corrected numerical Campedelli counts; and the dimensions of paracanonical systems. These calculations are explicitly distinguished from facts recovered from an occluded scan and from proofs attributed to named later authors.

Modern literature was consulted to identify appropriate statements and hypotheses. The references distinguish a checked theorem or passage from a bibliographically verified title and from a citation merely appearing in Enriques's footnotes. An author-hosted or institutional manuscript was preferred when a publisher's full text was unavailable. A search-indexed passage was sometimes usable even when its PDF URL could not be fetched; such a case is not described as a full-paper reading. The commentary gives APA-style author-date references, publication details, URLs or DOIs, and verified theorem/section locations where available. It does not invent page numbers for books or claim independent examination of every historical paper named by Enriques.

## How to read the claim register

`claims.csv` has the seven requested fields: `id`, `page`, `statement (modern)`, `kind`, `gap or error (if any)`, `repair and reference`, and `notes`. Identifiers are unique. Page ranges indicate arguments that cross a page boundary; the missing interval is identified explicitly and is not filled with invented assertions.

The register records mathematical assertions rather than every sentence of rhetoric. Definitions, intermediate equations, incidence assertions, numerical inequalities, dimension counts, existence and classification claims, and substantive steps in arguments are included. Equivalent algebraic versions of one formula can occur together; a distinct claim is not treated as proved merely because it shares a paragraph with a correct formula. Historical priority statements are discussed as source history, not converted indiscriminately into mathematical theorems.

The `kind` field reports the **presentation and proof status in the supplied book**:

- `definition`: terminology or notation introduced by the source.
- `proved`: an argument is actually supplied, subject to the qualifications in the error and repair fields.
- `sketched`: the source gives a recognizable route but compresses, omits, or defers a substantive step.
- `stated without proof`: the assertion is given without a supporting argument; explicitly tentative claims and questions are identified in the notes.
- `assumed from earlier work`: the source invokes an earlier chapter, a previously established criterion, or an external result rather than proving it here.

Thus a row classified `proved` may still contain an invalid argument. Conversely, a row classified `sketched` may state a correct theorem with a rigorous modern replacement. The error column, not the `kind` label alone, gives the mathematical verdict. The repair column distinguishes a genuine proof under clarified hypotheses, a counterexample to the literal assertion, a modern replacement theorem, and a step that remains unverified. Modern additions are expressly identified as audit derivations or modern replacements rather than silently attributed to Enriques. On those marked additional rows, `proved` refers to a reproduced audit proof and `assumed from earlier work` to an identified modern theorem. Neither label asserts that the book contains the modern addition or its proof.

Modern notation is interpreted on a smooth projective complex model unless a row says otherwise. Regularity $q=0$ does not imply the vanishing of $H^1(X,\mathcal O_X(D))$ for an arbitrary divisor. A projective model need not be the minimal model. A “simple” system means a birational map, not an embedding. A pencil of elliptic curves and a pencil over an elliptic base describe different genera. These distinctions materially affect several verdicts.

## How to read the transcription register

`transcription_corrections.csv` has the six requested fields: `page`, `line (approximate)`, `transcribed reading`, `scan reading`, `decision`, and `evidence`. Each of the 81 literal `% ??` occurrences has an explicit entry, tracked by identifiers U001–U081. The distribution is four in the supplement, sixteen in Chapter VII, twenty-six in Chapter VIII, and thirty-five in Chapter IX. Entries also address mathematical misprints and contested editorial suggestions that were not marked with `% ??`.

The approximate line field gives an identifiable page location and, where useful, a source-line or flag identifier. A line is a locator, not a claim that the source has a universal line-numbering system. The `scan reading` field states what the image supports. The `decision` field separates transcription errors from original slips/misprints and from correctly transcribed uncertainty markers.

Additional concise categories are necessary for an honest audit: an unreadable or covered reading is `unresolved`; a correct or properly qualified reading can be `verified`; a rejected proposal is `emendation rejected`; and a substantive proof defect with no warranted textual emendation is `mathematical gap`. Detailed explanations remain in the evidence field. These categories prevent a mathematical repair from being misrepresented as a different visible word or glyph. A mathematically necessary correction is not entered as a visible scan reading if it is absent from the image. In particular, the apparatus's proposed $C_8\to C_5$ change on p.349 is not accepted merely because it was labeled “Stampa”: quintics through fifteen points of the $(4,4)$ complete intersection must pass through the sixteenth, whereas degree-eight forms with the stated simple conditions need not.

The register is an audit of readings and proposed changes, not a silently amended replacement TeX. Printed errors remain attributed to the book. Modern replacements appear alongside them. No unreadable passage has been certified by using a plausible mathematical completion.

## Material limits that remain

### Missing and occluded source material

**Pages 284–285.** Both are missing from the supplied scan and are marked as a gap in the TeX. No text is reconstructed. The commentary identifies the argument entering the gap, the assumptions needed by the continuation, and what can independently be checked from p.286 onward. A plausible modern proof of the resumed conclusion is not evidence of what the absent pages said.

**Supplementary page 186.** Overlapping paper hides the underlying folio and portions of the opening paragraphs. The visible lower passage and correspondence calculation are audited. The clipped word beginnings and hidden earlier formula are not completed. The derived Euler-characteristic relation is labeled as a calculation from visible equations, not as recovered text from beneath the overlap.

**Page 368.** The supplied transcription attributes restoration of its first two paragraphs to another scan called s197L. That image is not included. The restored mathematical argument is assessed as received text, but its covered wording remains unverifiable. The exposed historical notice is a separate, directly readable part of the image. Agreement with a modern Albanese proof cannot certify the hidden words.

**Blank page 370.** The final image has no mathematical body text. Its handwritten number and marks do not justify a mathematical entry.

### Mathematical and historical limits

The excerpt repeatedly relies on earlier equivalence criteria, adjunction theory, generic projection statements, and classification results from Chapters I–VI, X–XI, and the Enriques–Chisini volumes. These texts were not supplied. Their applications in the available arguments are checked, and modern substitutes are given where established. Their original proofs are not represented as having been audited in full.

Some historical constructions require nonemptiness, irreducibility, independence of imposed singularity conditions, or control of simultaneous resolution that a parameter count alone does not establish. The commentary records the precise missing claim. It does not convert every family-dimension calculation into a complete global moduli theorem. Where a literal universal assertion is false, the deliverable gives a counterexample or a verified modern theorem with the correct hypotheses; it does not claim that all possible singular models in the historical notation have thereby been classified anew.

The characteristic-system argument of Chapter IX is explicitly unfinished in the source. The audit locates concrete defects and supplies a rigorous modern proof of the principal result by the Picard scheme and positive divisors. That replacement is not a reconstruction of a lost or unwritten completion of Enriques's own proof. Semiregularity, smoothness of the Picard scheme, smoothness of a divisor parameter space, and extension of an individual section are kept distinct.

The principal setting is characteristic zero. Extensions to positive characteristic are restricted to identities and theorems whose hypotheses are stated; the Picard scheme may be nonreduced, and complex period arguments cannot be transferred unchanged. References to later classification theory are not claims that a characteristic-free version of every historical construction has been proved here.

Questions and “own ideas” in the commentary are labeled with confidence and rationale. They are proposed examples, extensions, or precise further checks, not unverified claims of novelty or blanket statements about the present research frontier. The audit does not infer that a question remains open in 2026 merely because Enriques left it open in 1949.

## Deliverable integrity

The final archive contains exactly the four requested files at its top level. The CSV files use UTF-8 and standard quoting, including quoted cells when a statement contains a comma or line break. The final checks verify unique claim identifiers, the requested field names, coverage of the available text pages, accounting for all 81 uncertainty markers, the absence of accidental control characters, and the integrity and membership of the ZIP. These checks establish file and coverage consistency; they are not substitutes for the mathematical reading described above.

The integrated totals, remaining uncertainties, and complete page-coverage ledger follow.


## Input identity

- `enriques_pp237-370.tex`: 423,440 bytes; SHA-256 `b7239829f948878e0346a71647eeb508996ce438ca1ccd27770e4a218d992cf7`.
- `enriques_scans_pp237-370.pdf`: 92,505,299 bytes; SHA-256 `1395c8145e592ab191bb816d123765058d53a8b92995719551c34dedefeca16f`.

## Integrated register totals

| Part | Available text pages | Claim rows | Correction/reading rows | Original uncertainty flags | Unresolved flags |
|---|---:|---:|---:|---:|---:|
| Chapter VII | 30 | 351 | 38 | 16 | 3 |
| Chapter VIII | 56 | 414 | 67 | 26 | 6 |
| Chapter IX | 45 | 333 | 76 | 35 | 14 |
| Supplement: page 186 | 1 | 18 | 4 | 4 | 4 |
| **Total** | **132** | **1116** | **185** | **81** | **27** |

The 132 text-bearing pages include the partly visible supplement and p.368. They do not include the blank p.370 or the missing pp.284–285. The claim total includes explicitly identified modern audit calculations and one documentary gap record for pp.284–285; it is not a count of numbered theorems in the book. Of the 81 original uncertainty flags, **54 have determinate or explicitly qualified readings and 27 remain unresolved**. “Determinate” includes confirmed printed errors: it does not mean that the printed mathematics is correct. Additional non-flag records may identify an unresolved mathematical reconstruction.

### Presentation kinds in the claim register

| Kind | Rows |
|---|---:|
| definition | 91 |
| proved | 491 |
| sketched | 249 |
| stated without proof | 144 |
| assumed from earlier work | 141 |

These are source-presentation categories, with the expressly marked audit-derivation exception explained above. They are not a tally of true and false theorems.

### Unresolved original uncertainty flags

| Part | Flags | Nature of the remaining uncertainty |
|---|---|---|
| Chapter VII | U013, U018, U020 | Damaged letter or extra-mark shapes; intended words can be clear without the physical glyph being recoverable. |
| Chapter VIII | U021, U027, U035, U040, U043, U046 | Low punctuation marks, possible primes, and a joined apostrophe/letter sequence. Mathematical context is not used to invent a visible glyph. |
| Chapter IX | U050, U052, U054, U056, U057, U059, U064, U065, U070, U073, U078, U079, U080, U081 | Damaged letters, punctuation and historical Greek-type variants; U078–U081 concern physical overlap on p.368 and the unavailable alternate scan. |
| Supplement: page 186 | U001, U002, U003, U004 | Underlying folio and clipped or covered text. The assigned page number is preserved without claiming it is visible. |


## Chapter-specific mathematical limits

### Chapter VII

The p.242 tangent-branch argument has a complete repair when the half-fibres have no common components; the full local-length-one conclusion also needs unique factorization branches, which integral half-fibres supply. Extra branches for reducible half-fibres and shared-component configurations are not dismissed by the tangent calculation. The stated blanket prohibition of rational bisections is false, with a modern existence reference and a concrete intersection-theoretic counterexample supplied.

For the Comessatti construction, both the five-dimensional incidence count and the nonzero two-torsion obstruction are calculated. The latter disproves splitting for the printed configuration. Dominance of a modified construction that actually splits has not been proved. The two limiting tetrahedral configurations and the original Franchetta/du Val arguments behind the compressed account remain qualified. The type-II exceptional configuration, in contrast, is explicitly resolved by two successive rational contractions; it is no longer listed as an uncompleted calculation.

The bibliography distinguishes the 2024 author draft of Dolgachev and Kondō from the published 2025 book. The special-bisection locator is Definition 6.3.2 and Theorem 6.3.3, printed p.29/PDF p.43 of that draft. Huybrechts's projective-model and moduli statements are cited to the inspected prepublication text. Saint-Donat's article is bibliographically verified; the operational theorem was checked through Huybrechts. Dolgachev's 1981 treatment supplies the multiple-fibre formula; the Schütt–Shioda section formula is not silently extended to the multiple-fibre case.

### Chapter VIII

The audit supplies calculations or modern proofs for adjunction and the complete-intersection list, the regular Noether inequality including its equality case, the canonical birational Castelnuovo bound with fixed parts, the Hodge-index exclusions, double-cover invariant corrections, and the explicit Godeaux quotient, bidouble cover, and weighted canonical hypersurface. Bombieri's uniform pluricanonical theorem is supplemented by a Reider-based proof of birationality for every $m\ge5$. Peters's author-hosted Theorem 7.2 is the checked formulation of Reider used in that proof; the 1990 meeting date is not presented as a verified publication year.

The correction of the final $p_g=0$ conjecture is separated from the false universal $p_g>0$ assertion. The historical Campedelli existence claim and later valid examples are also distinguished in the commentary. Horikawa's local two-branch Kuranishi result is not converted into an unsupported exact count of global components. The Catanese–Debarre five-case theorem is checked against the first three pages of the primary paper; its 1989 conjecture about the entire torsion-zero moduli space is not asserted to remain open today.

Some nonnormal spatial models still require a local conductor calculation, a simultaneous-resolution argument, or a proof of dominance and generic fibre dimension. In particular, numerical counts alone do not certify every prescribed tacnode or oscillating singularity, every half-curve realization, or all proposed inclusions of deformation families. The ledger identifies these missing assertions. A direction such as “resolve the homaloidal system” in a repair field means a required calculation, not a completed proof. The original Franchetta, Pompilj, Fano, Godeaux, Bourniat, Maxwell, and Rosenblatt papers were not all independently obtained and audited. The full modern deformation classification across every numerical range in this chapter is not claimed.

Miyaoka's theorem and p.106 base-point statement were verified in indexed primary text after the direct PDF endpoint failed. Catanese's accessible 1981 exposition provides an additional direct check of the low-invariant pluricanonical results. Bibliographic verification of the 1978 Bombieri–Catanese item is distinguished from reading its inaccessible original PDF. The 1981 original volume and its later Springer reprint are not conflated.

### Chapter IX

The main characteristic-system theorem has a modern Picard-scheme proof for sufficiently positive divisors. This does not make every divisor parameter space smooth, every characteristic system complete, or every tangent direction integrable in the original family. The concrete defects in the unfinished integration and auxiliary-curve arguments are identified; no intended missing completion is claimed. The p.327 semicontinuity argument is retained in its correct family-of-classes interpretation.

The paracanonical assertions are checked with the Albanese-dimension hypothesis where generic vanishing requires it. Explicit examples and alternating-form calculations settle the unrestricted dimension claim and the genus-four special-complex reversal. Symmetric products, Jacobians, and translation-plus-inversion groups are distinguished. The finite unramified-cover statement is proved for connected complex covers; the $p_g=0$ Albanese-pencil theorem is proved without relying on the occluded wording of p.368.

Kleiman's precise Picard and semiregularity statements were checked in the primary manuscript. The Kodaira–Spencer and Green–Lazarsfeld bibliographic records are verified, while the formulations actually used were checked in the identified later primary literature. The modern splitting theorem of Felisetti and Fontanari is used with its hypotheses. Sheridan's symmetric-product statements are not stripped of their curve-generality assumptions. The Lewis–Lyons example confirms that an elliptic Albanese base need not mean elliptic fibres. Exact checked locations and access qualifications appear in the chapter bibliography.

## Complete page-coverage ledger

“Claim rows” assigns a record to the first page in its page field, so a cross-page record is counted once. Flags are assigned to their actual source page. A row for a missing leaf records absence, not a textual reading. The chapter reviewers inspected every available scan page; the integrating reviewer read every supplied text page and all final registers and independently checked the critical images described above. Rendered crop filenames in the correction evidence identify audit intermediates; the original-PDF locators remain usable without those intermediate images, which are not additional archive members.

| Printed/assigned page | PDF image | Claim rows | Original uncertainty flags | Inspection focus or physical limit |
|---:|---:|---:|---|---|
| 186 | 1 | 18 | U001, U002, U003, U004 | Partly overlapped: visible correspondence calculation checked; covered words and underlying folio unresolved. |
| 237 | 2 | 6 | U005 | U005; branch-octic description; K and plurigenus conventions |
| 238 | 3 | 15 | — | Scope of adjoint-system equality; reducible half-fibres; rational adjoints |
| 239 | 4 | 16 | U006 | U006; false rational-bisection prohibition; Σ degrees and Bezout multiplicity |
| 240 | 5 | 6 | — | Printed `riduzione.`; dependence on proposition 8; moving/fixed parts |
| 241 | 6 | 6 | — | Shared rational components and virtual intersection; reduction hypotheses |
| 242 | 7 | 9 | U007 | U007 at scale 5; integral-half-fibre length-one proof repaired; one ambient divisor with two factorizations; reducible cases qualified |
| 243 | 8 | 12 | — | L²=4; moving degree two; simple-basepoint and branch assumptions |
| 244 | 9 | 11 | U008 | U008; printed four versus five assigned double points; ten-parameter counts |
| 245 | 10 | 19 | — | Generic versus universal automorphism claim; full-branch two-torsion obstruction |
| 246 | 11 | 13 | U009, U010 | U009, U010; exponent 3; non-splitting cubic; genus-four square-six calculation |
| 247 | 12 | 20 | — | Scale-5 π≥0 crop; connected nonreduced counterexample; fixed rational part convention |
| 248 | 13 | 15 | U011 | U011; printed `sisema`; quadric/cubic dimensions and complete-intersection hypotheses |
| 249 | 14 | 11 | — | H+R squares, contraction, smoothing and tangency independence |
| 250 | 15 | 9 | U012, U013 | U012, U013; first printed 6 should be 7; later relative 6 retained |
| 251 | 16 | 6 | — | Printed `siano`; genus of a reducible section; specialization assumptions |
| 252 | 17 | 10 | U014 | U014; both intersection/genus formulas; derivation 3n=Σa_i |
| 253 | 18 | 9 | U015 | U015; very-general independence; “obvious” specialization exclusion |
| 254 | 19 | 10 | — | Dimension-drop assertion; distinction divisor multiplier/cover degree |
| 255 | 20 | 7 | — | Independence of sixteen node smoothings; genus increment 3s |
| 256 | 21 | 4 | — | Rohn title grammar; no invented identification of Severi's small gap |
| 257 | 22 | 11 | U016 | U016; F16 confirmed; primitive versus imprimitive polarization; bibliography defects |
| 258 | 23 | 14 | U017 | U017; weighted Euler interpretation; K3 exception and index definition |
| 259 | 24 | 14 | U018 | U018 at scale 6; printed 2d versus correct RR increment d |
| 260 | 25 | 26 | — | Printed OP/P; canonical resolution; completeness countertest |
| 261 | 26 | 17 | — | Restricted I2-fibre locus; general Weierstrass dimension 10p+8 |
| 262 | 27 | 10 | — | Printed −1 constant; positivity limits and index-divisibility distinction |
| 263 | 28 | 16 | U019 | U019; missing +1, missing −s, 2s−3 versus 2(s−3), stabilizers |
| 264 | 29 | 7 | — | Correct Enriques check; m divides d; floor-formula reconstruction |
| 265 | 30 | 13 | U020 | U020 at scale 5; descent of [d,d] correspondence; equality of χ |
| 266 | 31 | 9 | — | Base genus=q for χ>0; E×B test; Chapter XI deferred |
| 267 | 32 | 6 | U021 | Introduction; regularity and canonical-space notation; U021 remains unresolved. |
| 268 | 33 | 7 | — | High pluricanonical maps, singularity corrections, and quintic constructions. |
| 269 | 34 | 6 | — | Cremona models and numerical-quintic exhaustion; Horikawa countertypes. |
| 270 | 35 | 6 | — | Double-quadric case; the literal base-point assertion checked separately. |
| 271 | 36 | 5 | — | Sextic and double-cubic constructions with K² = 6; adjoint fixed plane. |
| 272 | 37 | 6 | — | Double-cubic degeneration, double-plane corrections, and moduli counts. |
| 273 | 38 | 5 | — | Triple-cone family and incomplete classification; opening of the septic case. |
| 274 | 39 | 9 | U022 | Quadric-cone plane classes and the author’s explicit heuristic qualification. |
| 275 | 40 | 8 | U023 | Auxiliary divisors D and T; the self-residual relation and parameter count. |
| 276 | 41 | 8 | U024, U025 | Hyperelliptic space curves and degeneration; printed 28 versus transcribed 26. |
| 277 | 42 | 6 | U026 | Fixed exceptional line; relative and absolute canonical genera. |
| 278 | 43 | 5 | — | Multiplicity-one calculation and the conditional 37/38/35 parameter counts. |
| 279 | 44 | 5 | — | Double cubic and plane branch of degree 12; one-base-point correction. |
| 280 | 45 | 7 | — | Double-quadric branch cluster; fixed-line incidence conflict and 33-moduli claim. |
| 281 | 46 | 7 | — | Octic model and double curve; printed degree-nine cutting surface should have degree eight. |
| 282 | 47 | 8 | U027 | Half-class construction and independence of seventeen conditions; U027 unresolved. |
| 283 | 48 | 8 | U028, U029 | Double plane of degree 14; start of the nonic construction; text ends at the gap. |
| 284 | — | 1 | — | Missing from the only supplied scan; no text reconstructed. |
| 285 | — | 0 | — | Missing from the only supplied scan; no text reconstructed. |
| 286 | 49 | 6 | — | Five triple points, the Segre cubic, and the kernel-and-Bézout argument. |
| 287 | 50 | 7 | U030 | Projected double curve, trope conic, and K3 restriction/vanishing hypotheses. |
| 288 | 51 | 6 | — | K3 intersection arithmetic, conditional dimension 28, and base-point variants. |
| 289 | 52 | 6 | U031 | Canonical genus eleven; printed branch degree 18 should be 16; threefold Jacobians. |
| 290 | 53 | 7 | — | Jacobian divisor classes and ordinary-singularity correction hypotheses. |
| 291 | 54 | 7 | U032 | Threefold adjunction, invariants, complete intersections, and the residual index. |
| 292 | 55 | 8 | U033 | Higher-codimension adjunction and the canonical complete-intersection list. |
| 293 | 56 | 7 | — | Threefold-section families; missing system bars and the n = p − 1 index slip. |
| 294 | 57 | 5 | — | Historical bibliography and the opening of the Noether inequality proof. |
| 295 | 58 | 6 | U034 | Clifford direction; correct positive base-point term but r/s mismatch; pencil bound. |
| 296 | 59 | 8 | U035 | Noether-line models; repeated confusion between K² and absolute linear genus. |
| 297 | 60 | 5 | U036 | Castelnuovo curve bound and the informal incidence-count argument. |
| 298 | 61 | 7 | U037 | Equality examples and scroll construction; printed degree eight confirmed. |
| 299 | 62 | 7 | U038 | Scroll ambient index, Hodge/Rosenblatt bounds, and moduli formulas. |
| 300 | 63 | 7 | — | Canonical multiple covers; numerical conditions versus converse assertions. |
| 301 | 64 | 6 | — | Oscillating singularities and the incorrect invariant of a degree-18 double plane. |
| 302 | 65 | 6 | — | Triple-cover discriminants and the trigonal theta-characteristic argument. |
| 303 | 66 | 6 | — | Missing z in the cubic equation; low-invariant plurigenus calculations. |
| 304 | 67 | 6 | — | Genus-two pencil, Weierstrass base point, and bicanonical cone. |
| 305 | 68 | 8 | U039 | Wrong p = 1 at the end of §14; transition to the actual geometric-genus-one case. |
| 306 | 69 | 8 | — | Sextic contact model, adjoint counts, and the cubic-degree misprint. |
| 307 | 70 | 7 | U040 | Possible bicanonical fixed part and its numerical bounds; U040 unresolved. |
| 308 | 71 | 21 | U041 | Godeaux nonic assertion, historical Campedelli existence gap, and parameter count. |
| 309 | 72 | 7 | — | False tricanonical freeness; special reducible bicanonical member and cubic-map argument. |
| 310 | 73 | 5 | — | Theta series, adjoint genus, and missing completeness assertions. |
| 311 | 74 | 6 | — | Singular-cubic exclusion; tricanonical/bicanonical word slip; K² = 2 cases. |
| 312 | 75 | 10 | U042 | Double octic fixed part and the geometric-genus-two bicanonical image. |
| 313 | 76 | 8 | — | Singular complete intersection, normalization, projection, and conductor conditions. |
| 314 | 77 | 7 | — | Six-node K3 double cover and the correct plane decic model. |
| 315 | 78 | 9 | — | Restriction argument; the 24-moduli count versus the deformation lower bound 26. |
| 316 | 79 | 10 | — | Fixed-part cases; inconsistent adjoint degree/genus and Hodge-index exclusion. |
| 317 | 80 | 13 | — | Octic double curve, intersection multiplicity, and omitted degree-four bicanonical maps. |
| 318 | 81 | 7 | U043 | Double K3 quartic and ten nodes; surface genus versus sectional genus. |
| 319 | 82 | 7 | — | Half-class residual systems, restriction dimensions, and contact sextics. |
| 320 | 83 | 8 | U044 | Contact counts 12 and 13; dimension comparison alone does not prove component inclusion. |
| 321 | 84 | 10 | — | Numerical Campedelli plurigenus, target, sectional genus, double curve, and characteristic series. |
| 322 | 85 | 11 | U045 | Three summary types; erroneous plane branch degree 12; rational plane systems. |
| 323 | 86 | 8 | — | Plane branch bound and the incorrect type-II tricanonical degree, space, and section genus. |
| 324 | 87 | 8 | U046 | False positive-genus tetracanonical claim; modern pg = 0 resolution and uniform m ≥ 5 theorem. |
| 325 | 88 | 7 | — | Notation; regularity and the characteristic series. |
| 326 | 89 | 8 | — | Residual positive systems and the upper bound on inequivalent classes. |
| 327 | 90 | 10 | — | Arithmetic effectivity and semicontinuity; no invented section-extension gap. |
| 328 | 91 | 8 | — | Class families and the Picard quotient. |
| 329 | 92 | 10 | — | The geometric-genus-zero splitting argument. |
| 330 | 93 | 6 | — | Dimension comparison and the original sign error. |
| 331 | 94 | 4 | — | First-order splitting and normal sections. |
| 332 | 95 | 4 | U047 | Tangent-space dimension versus actual deformations. |
| 333 | 96 | 5 | — | Integration gap; the source revisers’ unfinished-proof notice. |
| 334 | 97 | 6 | U048 | Branched-cover counts and node smoothing. |
| 335 | 98 | 5 | — | Auxiliary completion: degree and speciality contradiction. |
| 336 | 99 | 5 | — | Independent speciality conditions and auxiliary choices. |
| 337 | 100 | 6 | U049 | Uncompleted auxiliary-curve argument and its precise missing conditions. |
| 338 | 101 | 6 | — | Monodromy, component exchange, and descent assertions. |
| 339 | 102 | 3 | — | Historical trace construction and rational parameter families. |
| 340 | 103 | 6 | U050, U051 | Adjoint deficiency, history, and damaged type. |
| 341 | 104 | 7 | — | The genus-two Jacobian/theta example. |
| 342 | 105 | 5 | — | Splitting principles and the overly broad completeness assertion. |
| 343 | 106 | 5 | — | Differential versus integral splitting; missing independence. |
| 344 | 107 | 5 | U052, U053 | Trivial canonical class; elliptic base versus elliptic fibre. |
| 345 | 108 | 4 | — | Holomorphic one-forms, periods, and Picard comparison. |
| 346 | 109 | 5 | U054 | Higher-order integration and translated tangent directions. |
| 347 | 110 | 4 | U055 | End of the unfinished proof; opening of Segre’s argument. |
| 348 | 111 | 10 | U056, U057 | The two characteristic-dimension formulas and Greek-type variants. |
| 349 | 112 | 6 | U058 | Lost limits and the rejected octic-to-quintic emendation. |
| 350 | 113 | 4 | — | Fixed points in all limits: the integration requirement. |
| 351 | 114 | 9 | — | Complete systems, maximal families, and exorbitance. |
| 352 | 115 | 14 | — | Cohomological interpretation of the three cases. |
| 353 | 116 | 10 | — | Ruled-quintic residual divisor and missing ruling fibre. |
| 354 | 117 | 10 | U059 | Paracanonical notation and cohomology. |
| 355 | 118 | 11 | — | Invalid extension of sections; Albanese-dimension counterexample. |
| 356 | 119 | 14 | U060 | Symmetric squares and the special/nonspecial-complex reversal. |
| 357 | 120 | 12 | U061 | Elliptic canonical counts and the missing degree-one bundle. |
| 358 | 121 | 6 | U062, U063 | Abelian factors, cosets, and rational equivalence. |
| 359 | 122 | 8 | — | Translation groups versus projective linear systems. |
| 360 | 123 | 7 | U064 | Connected finite unramified covers of abelian varieties. |
| 361 | 124 | 7 | U065, U066, U067 | Group commutation and symmetric-product canonical systems. |
| 362 | 125 | 10 | U068 | Trace divisors and intersections on symmetric products. |
| 363 | 126 | 9 | — | Adjunction induction and the canonical divisor of the Jacobian. |
| 364 | 127 | 8 | U069, U070 | Segre’s alternative trace-curve construction. |
| 365 | 128 | 8 | U071 | Positive geometric genus in abelian varieties; missing family hypothesis. |
| 366 | 129 | 11 | U072, U073 | Albanese pencil; original invariant misprint; equivalence criterion. |
| 367 | 130 | 8 | U074, U075, U076, U077 | Source incidence argument and fibre-class equivalences. |
| 368 | 131 | 8 | U078, U079, U080, U081 | Physical overlap; restored prose in TeX not authenticated by the supplied image. |
| 369 | 132 | 9 | — | Holomorphic integrals, uniqueness, and irregularity one. |
| 370 | 133 | 0 | — | Blank leaf with handwritten folio; no mathematical body text. |

The single row assigned to 284 in the count above is the documentary gap record whose page field is `284–285`. It asserts the absence of both pages; it supplies no invented mathematical claim from either leaf.
