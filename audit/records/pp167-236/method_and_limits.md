# Method, coverage, and limits

## 1. Materials and scope

This audit used the supplied scans as the authority and the supplied first-pass TeX as the searchable reading text. The instruction file was read in full. No corrected TeX file is substituted for the requested deliverables: the correction register preserves the distinction between the transcription, the printed reading, and a mathematical emendation.

The actual excerpt is Chapter V, §§1–14, pp. 167–215 with **p. 186 absent**; Chapter VI, §§1–4, pp. 217–235; and the opening of Chapter VII, inferred p. 237. There are 71 PDF images: 68 contain text and three are blank. Chapter-opening folios are inferred where not printed. The attribution of 167 also has handwritten support. The apparent gaps at 216 and 236 are blank leaves that are present; the gap at 186 is an absent leaf. The book's historical *Introduzione* is not supplied. The commentary's Introduzione is expressly editorial.

The PDF and TeX were identified by their SHA-256 checksums:

- PDF: dbc47dc04cd0e6c651096171fc2e59b224560cd89f6b97e509400ba414752a66.
- TeX: 85e346fedaeeafd2716af364e99bb924867ac4579dd32e0e0b7cd5d77522ad5b.

All TeX line references refer to the original supplied file, before editing. PDF page positions are one-based. Printed page references, including those in the claim register, refer to the book's pagination.

## 2. Reading and integration

The principal reviewer read the entire 2,247-line TeX transcription, not only its displayed formulas or flagged passages. Parallel mathematical reviews covered all of Chapter V and all of Chapter VI together with the supplied Chapter VII opening. A separate scan review compared every one of the 71 PDF images against its corresponding transcription block, including headings, prose, inline notation, equations, footnotes, and blanks. Enlarged crops were used for small or damaged symbols. The principal reviewer then read both mathematical reviews, all entries in both claim registers, and the complete correction register, reconciled their conventions, and independently rechecked the most consequential derivations and selected scan pages.

The division of work was an additional check, not a substitution of an unreviewed summary for reading the text. An independent final comparison of the chapter drafts with the source sequence identified further small claims to include, including the double-plane normal forms on p. 185, Kummer-system details on pp. 189–190, and the exceptional curve in the last Chisini degeneration on p. 203. Contradictory provisional findings were reconsidered. In particular, the hypothesis on p. 221 is printed \(d\geq0\), exactly as transcribed; it is not a transcription error. Its boundary case is treated as a mathematical qualification in the commentary.

The claim register records definitions, theorems, intermediate formulas, numerical examples, qualitative geometric assertions, historical dependencies, and forward references. Related conditions defining one object, or a single named classification statement, may occupy one row; separate numerical conclusions and substantive intermediate deductions are generally separated. Repeated occurrences are recorded where their local status or use changes. A row that gives a corrected modern formula also reports the original error in the gap column. The correction register supplies the literal reading and line locator.

## 3. What proof-status labels mean

The five labels describe the treatment in the supplied historical pages:

- **definition**: a term, invariant, or construction is introduced.
- **proved**: an argument is supplied in the excerpt. This label is qualified by the adjacent gap/error column and does not mean that every implicit hypothesis is harmless.
- **sketched**: a real argument is present, but a geometric, local, deformation, or cohomological step needs further justification.
- **stated without proof**: the conclusion is asserted without an argument at that location.
- **assumed from earlier work**: the text relies on an earlier chapter, a cited paper, or a standard theorem. The source's citation is recorded without pretending that the absent material was also audited.

A theorem announced on one page and proved later may consequently have different local entries. Forward references to Chapter VII are not counted as proofs completed by the first page of that chapter. The missing p. 186 has no invented claim rows.

The registers distinguish two kinds of modernization. Translating a smooth regular surface into \(q=0\), or a virtual curve genus into arithmetic genus, usually clarifies a correct argument. Replacing an invalid torsion cancellation, an unsupported integrability claim, or a wrong numerical expression is a genuine repair. The source's own qualifications and admissions are retained.

## 4. Mathematical checks

### Numerical identities

The calculations were checked both by hand in modern intersection notation and, where useful, by exact symbolic simplification. The latter checks were consistency checks, not automated proofs of geometric existence.

The seven ordinary-projection relations on pp. 174–176 were reconstructed after correcting the p. 175 intersection product and equation (6). Eliminating their dependent variables reproduces the five p. 176 expressions for the discriminant degree, double-curve genera, triple points, and pinch points. The result recovers \(I+p^{(1)}=12p_a+9\). Thus the printed intermediate errors were not merely guessed from the desired final theorem.

The branch formulas on pp. 181–182 were checked against the plane-curve genus formula and the three relevant Plücker relations: class, flexes, and genus of the dual. Their inverses were also checked. The cusp count for a net was derived intrinsically from the universal first-jet bundle and the Hessian determinant, which isolates the required transversality assumptions. Plane pencils and quartic K3 projections provide explicit numerical examples.

Finite-cover identities were reconstructed from \(K_X=f^*K_Y+R\), adjunction on the ramification curve, and Euler-characteristic stratification of the branch locus. This independently gives the correspondence identity needed across the missing p. 186. It does not recover or quote that page. The calculations distinguish the Euler characteristic of a disconnected normalization from the genus of a connected curve.

The moduli formulas were checked after separating projective dimensions from vector-space dimensions, actual family excess from tangent-space speciality, and those from obstruction spaces. The modern lower bound follows from Riemann–Roch for \(T_S\) and the Kuranishi obstruction map. It does not require universal unobstructedness of nodal/cuspidal strata.

### Double covers and plurigenera

The common calculation uses the cover algebra \(\mathcal O_Y\oplus L^{-1}\), branch class \(2L\), and canonical class \(K_X=\pi^*(K_Y+L)\). At a branch point of multiplicity \(b\), canonical resolution replaces \(L\) by \(\sigma^*L-\lfloor b/2\rfloor E\). Odd branch multiplicities retain the exceptional divisor in the new branch locus. Total transforms provide the diagonal basis for intersection calculations at infinitely near points.

This procedure was applied to the octic and decic examples. The smooth double-cover model was distinguished from its minimal model, and the lifts of branch \((-2)\)-curves were contracted before computing the absolute linear genus. The resulting Euler characteristics, genera, and pluricanonical divisors were compared with the genus-one canonical-bundle formula. These independent routes explain the printed \(P_2,P_3,P_6\) values and the errors on pp. 226, 228, and 230.

For the Halphen examples, the exact index of the pencil was retained and derived from the source's irreducible member, using the fixed-remainder description of multiples of its anticanonical class. Counting sections of multiples of its anticanonical divisor gives floor-function formulas for every plurigenus. The allowed endpoint \(n=2\) was checked separately. This is essential: the missing endpoint is invisible if one checks only a large generic integer.

### Arguments accepted and arguments requiring more

The component proof that an effective pluricanonical class on a minimal surface has \(K^2\geq0\) is accepted and expanded. It is not criticized on the false premise that Enriques needed the entire intersection matrix to be positive semidefinite. Completeness of a linear system's restriction on a fixed regular surface is proved by its cohomology sequence and is distinguished from integrability of first-order deformations.

The rationality proof is followed through both cases, including elliptic systems, hyperelliptic characteristic series, fixed components, the cone estimate, and the adjoint sequence. Its compressed residual-system steps are identified. A complete modern replacement is supplied relative to the surface minimal-model theorem. The use of that theorem is explicit; this audit does not claim to prove the entire minimal-model program from first principles.

## 5. Transcription decisions and remaining image uncertainty

Every literal “% ??” marker has a recorded disposition, including markers resolved as transcription errors rather than placed in the “% ?? resolved” category. Every “[sic]” comment has also been reviewed. Mathematical issues found beyond those existing annotations are included. Several adjacent comments can concern the same printed expression, but their line references remain traceable.

The decision categories are used as follows:

- **transcription error** means that the first-pass transcription differs from the best supported scan reading.
- **misprint** means that the problematic reading is present in print and a local correction is justified.
- **author's slip** marks a substantive source-level numerical, notational, inferential, or scope problem.
- **"% ??" resolved** means that the marker has been examined and an editorial disposition supplied. It does not certify that lost or damaged ink has become physically decidable.

The last two source categories do not establish whether the author, editor, or compositor caused the problem. No manuscript or corrected proof sheets were available. A true source error normally has identical transcribed reading and scan reading; its repair appears in the evidence field and commentary.

Residual palaeographic limits concern the punctuation after *avremo* (p. 168), *delle/dello biaggiunte* (p. 185), punctuation after *hyperelliptiques* (p. 190), the sign-adjacent fleck on p. 191, the punctuation following \(3k\) (p. 208), the damaged first subscript in \(p_a\) (p. 229), and the thin mark after *tacnodali* (inferred p. 237). Each affected row gives its preferred reading and confidence limit. Enlargement improves inspection of existing pixels but cannot restore missing information. The grammatical attachment of *definite* on p. 230 also remains interpretive even though its printed final letter is clear.

The source sometimes repeats an operation or equality sign at a line break. These diplomatic repetitions, preserved in places by the TeX as +{}+, ={}= or -{}-, are not treated as algebraic errors. Historical spelling, the plural *superficie*, line-end hyphenation, and an upright rather than italic \(D_8\) likewise do not change mathematical meaning.

## 6. Literature verification

The modern bibliography gives author–date citations, full publication information where verified, URLs, and precise theorem or section locators. The theorem numbering is tied to the consulted edition: Reid's 1996 preprint, for example, is not silently assigned pagination from its later printed version. Hassett's published chapter and its earlier author PDF have different pagination; the commentary uses the published locator.

Primary texts or author-hosted expositions were checked for Riemann–Roch and adjunction, minimal models and rationality, Halphen surfaces, canonical-bundle and vanishing formulas, complex Riemann existence, the Enriques quartic/octic models, and deformation-theoretic bounds and counterexamples. The important later attributions are scoped: Deligne and Fulton supply the rigorous nodal-complement theorem; Catanese explicitly identifies the Kuranishi proof of the Enriques inequality; Zariski's positive-characteristic rationality work is identified through a verified modern reference. None is credited with a local printing correction without documentary evidence.

Bibliographic verification is not the same as reading an entire cited work. In particular, the full original Wahl (1974) and Zariski (1958) proofs were not retrieved in this review; their publication data and the specific roles reported here are corroborated by the identified primary or author-written later sources. Guffroy's publisher abstract was checked; no unverified proposition number is assigned to that paper. The older footnotes of Enriques are reported as historical dependencies, with abbreviated titles left abbreviated when they could not be independently completed.

The literature check also distinguishes Kulikov's theorem for generic linear projections from a blanket resolution of every formulation of Chisini's conjecture. A source describing the latter as a conjecture is not transformed into a proof merely because a related theorem has the same informal name.

## 7. Explicit limits

1. **Unavailable source material.** Printed p. 186, the historical Introduzione, earlier chapters relied upon by the excerpt, and the continuation after the opening of Chapter VII were not available. Their absence is material, and the audit makes no claim of having read them.
2. **Geometric hypotheses.** Generic projections, ordinary branch singularities, transverse intersections, connected generic fibres, and the indicated irreducible Halphen configurations are hypotheses, not consequences of a list of numerical invariants. Extra singularities or a different pencil index can alter a double-plane calculation.
3. **Existence versus compatibility.** Numerical checks of the historical branch configurations verify the claimed invariants conditional on the stated construction. They do not independently construct an explicit polynomial for every example or prove that every numerical branch tuple is realizable. Enriques's own unfinished K3 degeneration is left unfinished as a historical construction; its missing smoothing is identified.
4. **Characteristic and field.** The main modern statements are over \(\mathbb C\). Algebraically closed characteristic-zero variants are indicated when appropriate. Wild fibres, inseparable covers, nonreduced Picard schemes, and rationality over nonclosed fields require separate hypotheses and are not covered by blindly copying the complex formulas.
5. **Foundational inputs.** Riemann–Roch, Serre duality, resolution of surface singularities, the surface minimal-model theorem, vanishing, Riemann existence, and Kuranishi theory are invoked with identified sources. Proofs of their application are supplied; a new construction of all these foundational theories is not claimed.
6. **Historical priority and novelty.** A modern replacement proof does not establish who first repaired the particular historical argument. Our calculations, proposed examples, and questions are labelled as this audit's deductions. No claim of new mathematical priority is made.
7. **No formal proof certification.** The mathematical review is a reasoned scholarly audit supported by independent readings and exact checks, not a proof-assistant verification. Remaining textual and construction-level uncertainty is recorded rather than erased.

## 8. Package validation and detailed page map

The final package contains exactly the four requested UTF-8 files. Both CSVs were parsed after assembly, their field names and allowed decision/status labels checked, and claim identifiers checked for uniqueness. The uncertainty-marker and “[sic]” line inventories were compared with the correction register. Page coverage was checked against the physical-page census. The archive was reopened and its four entries read successfully.

The claim register contains **521 rows**: 292 for Chapter V, 222 for Chapter VI, and seven for the supplied Chapter VII opening. The historical-status totals are 37 definition, 299 proved, 82 sketched, 32 stated without proof, 71 assumed from earlier work. These are statuses of the source's treatment, not a tally of modern true and false propositions.

The correction register contains **72 rows**: 7 transcription error, 18 author's slip, 22 misprint, 25 "% ??" resolved. All 31 uncertainty markers and all 32 existing [sic] comments are traceable by original TeX line. Six uncertainty markers are resolved in rows classified as transcription errors; therefore the number of markers exceeds the 25 rows bearing the dedicated resolved category. Every one of the 68 text-bearing images has claim coverage.

The following map makes the correspondence between supplied images, folios, scan identifiers, and transcription lines explicit. Blank leaves have no mathematical claim entries; the absent p. 186 is not assigned a PDF position.

| PDF page | Book folio | Scan identifier | Original TeX lines | Contents |
|---:|---|---|---|---|
| 1 | 166 (inferred) | s095L | 4–10 | Blank |
| 2 | 167 (inferred) | s095R | 11–31 | Chapter V opening; handwritten 167 |
| 3 | 168 | s096L | 32–77 | Chapter V |
| 4 | 169 | s096R | 78–100 | Chapter V |
| 5 | 170 | s097L | 101–132 | Chapter V |
| 6 | 171 | s097R | 133–184 | Chapter V |
| 7 | 172 | s098L | 185–212 | Chapter V |
| 8 | 173 | s098R | 213–248 | Chapter V |
| 9 | 174 | s099L | 249–281 | Chapter V |
| 10 | 175 | s099R | 282–328 | Chapter V |
| 11 | 176 | s100L | 329–367 | Chapter V |
| 12 | 177 | s100R | 368–426 | Chapter V |
| 13 | 178 | s101L | 427–476 | Chapter V |
| 14 | 179 | s101R | 477–521 | Chapter V |
| 15 | 180 | s102L | 522–543 | Chapter V |
| 16 | 181 | s102R | 544–592 | Chapter V |
| 17 | 182 | s103L | 593–635 | Chapter V |
| 18 | 183 | s103R | 636–658 | Chapter V |
| 19 | 184 | s104L | 659–690 | Chapter V |
| 20 | 185 | s104R | 691–723 | Chapter V |
| 21 | 187 | s105R | 724–770 | Chapter V |
| 22 | 188 | s106L | 771–818 | Chapter V |
| 23 | 189 | s106R | 819–851 | Chapter V |
| 24 | 190 | s107L | 852–879 | Chapter V |
| 25 | 191 | s107R | 880–931 | Chapter V |
| 26 | 192 | s108L | 932–958 | Chapter V |
| 27 | 193 | s108R | 959–984 | Chapter V |
| 28 | 194 | s109L | 985–1001 | Chapter V |
| 29 | 195 | s109R | 1002–1018 | Chapter V |
| 30 | 196 | s110L | 1019–1041 | Chapter V |
| 31 | 197 | s110R | 1042–1057 | Chapter V |
| 32 | 198 | s111L | 1058–1075 | Chapter V |
| 33 | 199 | s111R | 1076–1091 | Chapter V |
| 34 | 200 | s112L | 1092–1112 | Chapter V |
| 35 | 201 | s112R | 1113–1125 | Chapter V |
| 36 | 202 | s113L | 1126–1147 | Chapter V |
| 37 | 203 | s113R | 1148–1164 | Chapter V |
| 38 | 204 | s114L | 1165–1188 | Chapter V |
| 39 | 205 | s114R | 1189–1211 | Chapter V |
| 40 | 206 | s115L | 1212–1261 | Chapter V |
| 41 | 207 | s115R | 1262–1306 | Chapter V |
| 42 | 208 | s116L | 1307–1328 | Chapter V |
| 43 | 209 | s116R | 1329–1350 | Chapter V |
| 44 | 210 | s117L | 1351–1367 | Chapter V |
| 45 | 211 | s117R | 1368–1420 | Chapter V |
| 46 | 212 | s118L | 1421–1470 | Chapter V |
| 47 | 213 | s118R | 1471–1504 | Chapter V |
| 48 | 214 | s119L | 1505–1525 | Chapter V |
| 49 | 215 | s119R | 1526–1556 | Chapter V |
| 50 | 216 (inferred) | s120L | 1557–1563 | Blank |
| 51 | 217 (inferred) | s120R | 1564–1597 | Chapter VI opening |
| 52 | 218 | s121L | 1598–1648 | Chapter VI |
| 53 | 219 | s121R | 1649–1683 | Chapter VI |
| 54 | 220 | s122L | 1684–1712 | Chapter VI |
| 55 | 221 | s122R | 1713–1762 | Chapter VI |
| 56 | 222 | s123L | 1763–1816 | Chapter VI |
| 57 | 223 | s123R | 1817–1867 | Chapter VI |
| 58 | 224 | s124L | 1868–1900 | Chapter VI |
| 59 | 225 | s124R | 1901–1923 | Chapter VI |
| 60 | 226 | s125L | 1924–1950 | Chapter VI |
| 61 | 227 | s125R | 1951–1991 | Chapter VI |
| 62 | 228 | s126L | 1992–2024 | Chapter VI |
| 63 | 229 | s126R | 2025–2053 | Chapter VI |
| 64 | 230 | s127L | 2054–2077 | Chapter VI |
| 65 | 231 | s127R | 2078–2105 | Chapter VI |
| 66 | 232 | s128L | 2106–2121 | Chapter VI |
| 67 | 233 | s128R | 2122–2148 | Chapter VI |
| 68 | 234 | s129L | 2149–2187 | Chapter VI |
| 69 | 235 | s129R | 2188–2207 | Chapter VI |
| 70 | 236 (inferred) | s130L | 2208–2214 | Blank |
| 71 | 237 (inferred) | s130R | 2215–2247 | Chapter VII opening; excerpt ends after item 2 |
