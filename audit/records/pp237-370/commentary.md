# Mathematical commentary and transcription audit

## Introduzione: scope, notation, and rules of interpretation

**Primary source.** Enriques, F. (1949). *Le superficie algebriche*. Zanichelli, Chapters VII–IX, the supplied images assigned to pp. 237–370, together with the supplementary image assigned to p. 186. All page references below are to this supplied source unless a modern reference is expressly named. The supplied transcription is a finding aid, not an independent witness. The PDF contains 133 images: the supplementary leaf; 131 text-bearing chapter pages (237–369 except 284–285); and a blank final image with a handwritten “370.” The three chapter openings have no printed folio but are assigned 237, 267, and 325 by sequence. The assignment of the occluded supplement to 186 comes from the supplied apparatus, not from a legible underlying folio. Pages 284–285 are not available. No text has been invented to fill them.

### What the accompanying registers record

`claims.csv` separates statements about mathematical objects from the status of their arguments in this book. In particular, **“proved” describes an argument actually supplied by Enriques; it is not an assertion that every unexpressed hypothesis or step is correct**. The gap/error and repair columns qualify that status. “Sketched” means that a recognizable argument is present but a substantive step is deferred, compressed, or unproved. “Stated without proof” includes questions and conjectural conclusions, which are identified as such in the notes. “Assumed from earlier work” records internal cross-references and historical citations rather than pretending that the cited proof occurs in these pages. A formula and its immediate algebraic restatement may share a row; distinct hypotheses, geometric assertions, and independent intermediate steps have separate entries. Additional rows expressly marked as audit derivations or modern replacements record modern repairs. On those marked rows, “proved” refers to a proof reproduced in this audit and “assumed from earlier work” to an identified modern theorem; neither attributes the modern addition or its proof to Enriques.

The transcription register distinguishes what is **visible** from what is **mathematically preferable**. In particular, a printed wrong inequality is not an OCR error, and a mathematically necessary word beneath an opaque leaf is not a recovered reading. The register accounts for every literal `% ??` occurrence, including markers that the incoming edition already labels “RISOLTO.” Those labels were rechecked, not accepted as evidence. Where the source image cannot decide, the decision is explicitly “unresolved”; this is a necessary extension of the four proposed decision labels. A closed audit entry can therefore record an unresolved reading. It cannot truthfully record an unreadable passage as resolved.

The exposition below uses three distinct forms of attribution. “Enriques argues…” describes the supplied pages. “A modern replacement is…” gives a rigorous route to the result, with its hypotheses. “Audit derivation/example” identifies calculations or examples worked out for this commentary; such a derivation is not an asserted original research result and is not attributed retrospectively to a later mathematician. Historical priority is claimed only where a checked source supports it. In particular, the mere availability of Zariski, Kodaira, Mumford, or Bombieri does not justify attaching their names to a local repair.

### The ambient category matters

Unless expressly changed, $X$ is a smooth, connected, projective surface over $\mathbb C$. A singular double plane, sextic with a double curve, or canonical image is compared with $X$ through normalization and resolution. The arithmetic genus of a singular projective model can differ from that of its smooth birational model. A numerical assertion about the latter must not be computed by applying the smooth hypersurface formula directly to the former.

The principal dictionary is as follows.

| Enriques's notation or phrase | Modern interpretation and qualification |
|---|---|
| $p_g$ | $h^0(X,\omega_X)=h^2(X,\mathcal O_X)$ |
| $p_a$, *genere numerico* | $\chi(\mathcal O_X)-1=p_g-q$ for the smooth projective model |
| $q=p_g-p_a$ | $h^1(X,\mathcal O_X)=h^0(X,\Omega_X^1)=\dim\operatorname{Pic}^0(X)$ over $\mathbb C$ |
| $p$, in the regular chapters | $p_g=p_a$, with $q=0$; not the genus of a section curve |
| $P$, $P_i$ | $P_2=h^0(2K_X)$, $P_i=h^0(iK_X)$; $P$ is not $p_g$ |
| absolute $p^{(1)}$ | $K_{X_{\min}}^2+1$ in the nonruled minimal situation under discussion |
| relative $p^{(1)}$, $p^{(2)}$ | Arithmetic genus of the relevant canonical divisor and its self-intersection on the stated model; base points, fixed divisors, and blow-ups must be tracked |
| genus $\pi$, *genere virtuale* of $D$ | Arithmetic genus $p_a(D)=1+(D^2+D K_X)/2$, not necessarily the genus of its normalization |
| *grado* of a system | Its intersection number/self-intersection; the *effective* degree removes base-point contributions |
| $\vert D\vert $, dimension $r$ | Complete linear system $\mathbb P H^0(X,\mathcal O_X(D))$, $r=h^0(D)-1$ |
| *aggiunto* $D'$ | $D+K_X$, interpreted as a divisor class, with the stated exceptional corrections on a chosen singular model |
| *equivalenti* | Usually linearly equivalent, $D\sim D'$; in continuous systems algebraic equivalence is a different relation |
| continuous inequivalent curves | Divisors varying nontrivially in a translate of $\operatorname{Pic}^0(X)$, not merely moving inside one $\vert D\vert $ |
| *semplice* linear system | The associated rational map is birational onto its image; it need not be an embedding |
| an involution of order $d$ | A generically finite correspondence/map of degree $d$; “involution” here need not mean an automorphism of order two |
| $\infty^r$ | Dimension $r$, normally projective dimension; it is not a cardinality computation |
| *normale* projective model | Must be read locally in context: often “linearly normal,” not automatically normal as a scheme |
| elliptic pencil / irrational pencil | A fibration by genus-one curves / a fibration over a curve of positive genus; these concern different genera |

Numerical equivalence $\equiv_{\rm num}$, algebraic equivalence, and linear equivalence $\sim$ are kept distinct throughout. This is essential already on an Enriques surface: $K_X\equiv_{\rm num}0$, $2K_X\sim0$, but $K_X\not\sim0$. The printed $=$, $\equiv$, and dotted equality are not, by themselves, reliable indicators of which modern equivalence relation is intended.

### A common proof calculus

The following calculations explain the recurring repairs. They are included so that a reference to “Riemann–Roch” in the chapter commentary specifies what is actually being used. Standard reference locations were checked in Beauville (1996), Chapter I, especially I.10–I.17, and Hartshorne's surface formula is also explicitly identified as V.1.6 in Brosnan's course notes, Theorem 3.4.

For any divisor $D$,

$$
\chi(\mathcal O_X(D))=\chi(\mathcal O_X)+\frac{D(D-K_X)}2,
\qquad h^2(D)=h^0(K_X-D).
$$

Consequently

$$
\dim\vert D\vert =\chi(\mathcal O_X)-1+\frac{D(D-K_X)}2
 +h^1(D)-h^0(K_X-D).
$$

The correction terms cannot be discarded merely because the **surface** is regular. Regularity means $h^1(\mathcal O_X)=0$, not $h^1(\mathcal O_X(D))=0$ for every $D$. A claimed dimension is therefore checked either by proving a vanishing statement or by calculating the correction terms. “More parameters than conditions” proves neither independence of conditions nor existence of an irreducible member.

One elementary derivation of surface Riemann–Roch, useful for interpreting the older language, starts with a smooth very ample curve $A$ and the restriction sequence for $D+A$. Curve Riemann–Roch and adjunction give

$$
\chi(D+A)-\chi(D)=(D+A)A+1-g(A)
 =DA+\frac{A^2-AK_X}{2}.
$$

This is exactly the difference of the quadratic expression $D(D-K_X)/2$ when $D$ is replaced by $D+A$. Writing an arbitrary divisor as a difference of two sufficiently positive smooth divisors and iterating the same identity determines the constant as $\chi(\mathcal O_X)$. This is a proof of the numerical formula, not a vanishing theorem.

The sequence

$$
0\longrightarrow\mathcal O_X(-D)\longrightarrow\mathcal O_X
\longrightarrow\mathcal O_D\longrightarrow0
$$

then gives $p_a(D)=1+D(D+K_X)/2$. For a smooth curve, the conormal exact sequence gives the stronger line-bundle identity

$$
\omega_D\simeq(\omega_X\otimes\mathcal O_X(D))\vert _D.
$$

For an effective Cartier divisor this remains true with its dualizing sheaf. Thus the formula is still meaningful for reducible or nonreduced divisors, but the arithmetic genus need not be a nonnegative geometric genus. In particular, connected support alone does not license every argument valid for an integral curve. For a reduced irreducible singular curve $D$, normalization yields

$$
p_a(D)=g(\widetilde D)+\sum_x\delta_x.
$$

This is why a “rational” nodal member of a genus-one pencil still has arithmetic genus one, whereas a smooth rational $(-2)$-curve on a surface with numerically trivial canonical class has arithmetic genus zero.

For a blow-up $\sigma:\widetilde X\to X$ at a smooth point with exceptional curve $E$,

$$
K_{\widetilde X}=\sigma^*K_X+E,\quad E^2=-1,\quad
K_{\widetilde X}^2=K_X^2-1.
$$

The birational invariants $p_g,q,P_m$ are unchanged. If $D$ has multiplicity $a$ there, its strict transform is $\sigma^*D-aE$, with square $D^2-a^2$ and arithmetic genus lowered by $a(a-1)/2$. A canonical map of degree $d$, after resolving its base ideal and removing its fixed divisor, satisfies

$$
M^2=d\,\deg\phi_M(X).
$$

One must not identify $K_X^2$ with the degree of the image when there are base points, fixed divisors, or $d>1$. Several classifications in Chapter VIII depend precisely on these distinctions.

For a smooth double cover $\pi:X\to Y$ with branch divisor $B\in\vert 2L\vert $,

$$
\pi_*\mathcal O_X=\mathcal O_Y\oplus L^{-1},\quad
K_X=\pi^*(K_Y+L),\quad
\chi(\mathcal O_X)=2\chi(\mathcal O_Y)+\frac{L(L+K_Y)}2.
$$

The first identity follows from the trace splitting and the local algebra $\mathcal O_Y\oplus L^{-1}$; duality or local differentials give the second; the third follows by applying surface Riemann–Roch to $L^{-1}$. Also

$$
H^0(X,K_X)=H^0(Y,K_Y)\oplus H^0(Y,K_Y+L).
$$

These formulas apply directly to smooth branch or to a resolved cover with the appropriately transformed $L$. If a blow-up center has branch multiplicity $m$, put $a=\lfloor m/2\rfloor$: the transformed covering data are $L'=\sigma^*L-aE$, and the exceptional curve belongs to the transformed branch exactly when $m$ is odd. At this step $K^2$ drops by $2(a-1)^2$ and $\chi$ by $a(a-1)/2$; subsequent contraction of a $(-1)$-curve increases $K^2$ by one. Infinitely near singularities therefore require a sequence of calculations, not a single correction for the proper point. These identities are audit derivations from the preceding formulas; they do not assert that every plane curve with specified singularities exists or that its resolution is minimal.

For a minimal complex surface of general type, $K_X$ is nef and big. Applying a vanishing theorem to $K_X+(m-1)K_X$, $m\ge2$, gives

$$
P_m=\chi(\mathcal O_X)+\frac{m(m-1)}2K_X^2.
$$

On a regular surface this is $p+1+\binom m2(p^{(1)}-1)$. In particular $P_2=p+p^{(1)}$ and $P_3=p+3p^{(1)}-2$. This is the numerical framework behind the small-invariant cases in Chapter VIII. It is not the formula for Kodaira dimension one, and it must not be used to “repair” Chapter VII's elliptic cases. Likewise, eventual birationality of pluricanonical maps is a theorem about the canonical model; it does not erase the exceptional curves of a nonminimal smooth model. Bombieri (1973) provides the precise general-type theorem and its low-invariant exceptions.

### Continuous systems: the exact sequence behind Chapter IX

For an effective Cartier divisor $D$, let $N_{D/X}=\mathcal O_D(D)$. The sequence

$$
0\to\mathcal O_X\to\mathcal O_X(D)\to N_{D/X}\to0
$$

identifies the characteristic series of the complete linear system with the image of $H^0(\mathcal O_X(D))$ in $H^0(N_{D/X})$. Its vector-space dimension is $r=h^0(D)-1$, whereas the complete characteristic system has dimension $h^0(N_{D/X})-1$. The deficiency is

$$
\delta=h^0(N_{D/X})-r
 =\dim\ker\bigl(H^1(\mathcal O_X)\to H^1(\mathcal O_X(D))\bigr)\le q.
$$

This is a cohomological identity, independent of whether all infinitesimal deformations of $D$ integrate to an actual family. Equality holds, for example, if $H^1(\mathcal O_X(D))=0$. The tangent space to the divisor scheme at $D$ is $H^0(N_{D/X})$; its tangent dimension may exceed the dimension of the underlying reduced parameter space. The semiregularity map

$$
H^1(N_{D/X})\longrightarrow H^2(\mathcal O_X)
$$

and deformation obstructions are therefore essential in a modern formulation of a completeness theorem. Smoothness of $\operatorname{Pic}^0(X)$ over $\mathbb C$ does not on its own imply smoothness of every divisor parameter space over it. These distinctions prevent both an unjustified endorsement of Enriques's difficult proof and an equally unjustified claim that its valid numerical preliminaries are false.

The exponential sequence and Hodge theory identify $\operatorname{Pic}^0(X)$ analytically with $H^1(\mathcal O_X)/H^1(X,\mathbb Z)$, a projective complex torus of dimension $q$. Sufficiently positive twists have uniform higher-cohomology vanishing over this compact parameter space. A Poincaré bundle then produces a projective bundle of divisors over $\operatorname{Pic}^0(X)$. This supplies actual complete continuous systems in the positive range. It does not give the same conclusion for every special or obstructed divisor. The chapter commentary gives the applicable precise statements and the historical discussion verified in Kleiman (2005, 2013).

### How much of a classification has actually been proved?

The words “family,” “general,” and “all” require separate checks. A parameter count for a constructed family does not show that all surfaces with the same invariants belong to it; it does not prove that a smaller-dimensional family is in its closure; and it does not prove that a specialization preserves the normalization, smooth structure, or polarization intended in the argument. A flat family of equations with central member $G^2=0$ is not automatically a smooth family whose central member is the normalization of a double cover. A base change, normalization, and control of the relative dualizing sheaf may be needed.

Similarly, on a K3 surface, “nineteen moduli” concerns a fixed primitive polarization; the local deformation space of the unpolarized complex surface has dimension twenty. A Picard-rank-one assertion generally holds **very generally**, outside a countable union of Noether–Lefschetz loci. That is stronger information about quantifiers than a loose identification with a Zariski-open condition. A multiple polarization has square multiplied by the square of the integer multiplier. A degree-$d$ projective map is a different notion of multiplicity.

The audit uses modern results to repair conclusions where possible, but does not turn the book's questions into proved assertions. Where the supplied pages say that a classification is tentative, or explicitly defer a special case, that limitation is preserved. Where a modern counterexample invalidates a universal statement, the actual statement is recorded before its replacement.

### Common references and verified locations

Beauville, A. (1996). *Complex algebraic surfaces* (2nd ed.). Cambridge University Press. Chapter I, I.10–I.17 (Picard group, duality, Riemann–Roch, Noether's formula, genus formula, adjunction). Publisher excerpt: https://assets.cambridge.org/97805214/95103/excerpt/9780521495103_excerpt.pdf . Publisher metadata: https://www.cambridge.org/core/books/complex-algebraic-surfaces/E242F9DDB71DFB9B060ED6311400B5FA . The cited theorem locations, not merely the title, were checked.

Bombieri, E. (1973). Canonical models of surfaces of general type. *Publications Mathématiques de l'IHÉS, 42*, 171–219. https://doi.org/10.1007/BF02685880 . Open primary text: https://www.numdam.org/item/PMIHES_1973__42__171_0.pdf . Used for the modern pluricanonical theory; the numerical formulas displayed above are also independently derived in this audit.

Brosnan, P. (n.d.). *UMD 808J: Algebraic surfaces*, §3.2, Theorem 3.4. https://www.math.umd.edu/~pbrosnan/notes/Surfaces/sect0017.html . This openly accessible authored course text identifies Hartshorne's surface Riemann–Roch as Theorem V.1.6. No inference is made from its minor typesetting errors.

Hartshorne, R. (1977). *Algebraic geometry*. Springer. Surface Riemann–Roch, V.1.6, is cross-verified by the preceding source; exact locations not independently checked elsewhere are not silently asserted.

Further chapter-specific references and historical citations appear with the corresponding discussion below. An original footnote is evidence of what Enriques cited; it is not evidence that the cited work was independently read in full.



## Chapter VII: Surfaces of absolute linear genus one (pp. 237–266)

### VII.0. Reading conventions and scope

This audit reads all thirty printed pages, including the footnotes, historical notices, parameter counts, and degenerations. Page numbers below are the printed numbers. The companion claim register separates assertions finely; its `kind` records how Enriques presents a statement, not a certification that the argument is valid. Thus an assertion accompanied by an invalid proof can have kind `proved` and an explicit error in the next column. There is one explicit exception: rows whose notes begin “Audit derivation; not a separately proved source assertion” record intermediate claims in this audit’s modern reconstructions, and `proved` there refers to the proof reproduced here.

All mathematical statements in the reconstruction concern smooth projective surfaces over $\mathbb C$, unless an intermediate singular model is expressly named. Let $q=h^1(\mathcal O_X)$, $p_g=h^0(K_X)$, $\chi=1-q+p_g$, and $P_m=h^0(mK_X)$. In the regular cases of this chapter, Enriques's $p$ is $p_g=p_a(X)$, and his $P$ is $P_2$. His absolute linear genus $p^{(1)}$ is $K_{X_{\min}}^2+1$, not necessarily $K_X^2+1$ on a blown-up model. The genus of a divisor in intersection calculations is its arithmetic genus $p_a(D)=1+(D^2+D K_X)/2$. A singular rational curve can have positive arithmetic genus; assertions about a genus-zero irreducible divisor here concern a smooth rational curve. The word “elliptic” often includes a genus-one fibre divisor whose reduced components need not individually be elliptic.

A double plane is first a finite normal double cover of a plane or a suitable blow-up; its branch singularities must then be resolved, and vertical exceptional curves of self-intersection $-1$ contracted when discussing a minimal elliptic surface. The sextic with a double tetrahedron is nonnormal. Its surface invariants belong to its normalization and, if necessary, a resolution, not to the singular hypersurface's arithmetic invariants. This distinction is essential throughout §1. For an ordinary generic tetrahedral sextic the normalization is already smooth; special degenerations require additional analysis (Dolgachev, 2016, §2).

The most consequential findings are: proposition 8 on p. 239 is false for nodal Enriques surfaces; the specific cubic on pp. 245–246 does not split in the double cover with the full stated branch; connectedness on p. 247 needs a scheme-theoretic strengthening for nonreduced divisors; the dimension increment on p. 259 is $d$, not $2d$; and the determinant-one normal forms in §4 describe restrictive loci, not all Jacobian elliptic surfaces. Several further defects are identifiable printing slips. These distinctions matter more than the fact that many of the chapter's eventual classification statements have correct modern versions.

### VII.1. Enriques surfaces: adjunction, low-degree models, and ten moduli (§1, pp. 237–247)

#### VII.1.1. The eight preliminary propositions (pp. 237–239)

The minimal surfaces under discussion have $q=p_g=0$, $K_X\not\sim0$, and $2K_X\sim0$. They are complex Enriques surfaces. Their plurigenus sequence is $P_{2r}=1$, $P_{2r+1}=0$. Indeed the even powers of the canonical line bundle are trivial, and a nontrivial numerically trivial line bundle has no nonzero section: a nonzero effective divisor numerically equivalent to zero would have zero intersection with an ample divisor. This proves the displayed values $P_3=0$ and $P_6=1$ once the classification criterion imported from Chapter VI is accepted. The converse criterion is assumed here, not proved afresh.

Adjunction and surface Riemann–Roch give, for a nonzero effective divisor $D$,

$$
D^2=2p_a(D)-2,\qquad
\chi(\mathcal O_X(D))=1+\frac{D^2}{2}=p_a(D),\qquad
h^2(D)=h^0(K_X-D)=0.
$$

Consequently $\dim\vert D\vert \ge p_a(D)-1$. If $D$ is nef and big, vanishing applied to $K_X+(D-K_X)$ gives $h^1(D)=0$, so equality holds. An irreducible moving positive-square class has the required nefness: it has nonnegative intersection with every other irreducible curve, and positive self-intersection. This is a precise repair of the scope of propositions 2–3. “Virtually without basepoints” is not a proof that an actual linear system is generated by sections.

For these positive-square systems, adjunction sends $D$ to $D+K_X$; the two classes are distinct, have equal numerical invariants and equal dimensions, and have the same double. Proposition 4 must retain this positive-square context. Taken for every effective divisor it contradicts proposition 7: a $(-2)$-curve $R$ has $\vert R\vert \ne\varnothing$ but $\vert R+K_X\vert =\varnothing$.

For a primitive nef isotropic class $E$, the standard Enriques theorem gives a genus-one pencil $\vert 2E\vert $, with exactly two double fibres $2E$ and $2E'$, where $E'=E+K_X$. Its adjoint fibre class is $2E+K_X=E+E'$. The effective half-fibres can be reducible; they are not necessarily smooth elliptic curves. The terse argument on p. 238 identifies the expected vertical classes but relies on this structure theorem for effectivity, primitiveness, and completeness. It does not establish the entire fibre classification from the numerical equality alone. A horizontal curve meets $2E$ in an even number of points, because $E$ is an integral divisor. These standard facts are treated in Cossec et al. (2025, Generalities and Linear Systems) and Dolgachev (2016, §§3–4).

Proposition 7 is correct. If $R$ is an irreducible genus-zero divisor, then $R^2=-2$. Were $R+K_X$ effective, its negative intersection with $R$ would force $R$ to be a component, leaving an effective divisor in class $K_X$, which is impossible. The argument needs this component-and-residual reasoning; negative intersection alone does not literally make two arbitrary effective divisors equal.

**Proposition 8 is false as printed.** It prohibits an irreducible rational bisection of any genus-one pencil on $X$. A pencil $\vert 2E\vert $ with a smooth rational curve $R$ satisfying $E R=1$ is precisely a special genus-one fibration. Such fibrations exist on nodal Enriques surfaces: Dolgachev and Kondō's 2024 author draft, Definition 6.3.2 and Theorem 6.3.3, printed p. 29, states that every nodal Enriques surface admits one. The draft locator is not silently transferred to the published 2025 edition.

The internal failure can be pinpointed. Put $C=2E$ and $D=C+R$. Then

$$
D^2=0+4-2=2,\quad p_a(D)=2,\quad
D+K_X=R+E+E',\quad\chi(D+K_X)=2.
$$

The restrictions of members of $\vert D+K_X\vert $ to the half-fibres have degree one, and therefore fixed intersection points when the half-fibres are smooth. Enriques infers that the remaining moving curves have no intersection with a general fibre. That inference does not follow: fixed intersections with two distinguished fibres do not make a horizontal moving part vertical. Moreover $\vert C+R\vert $ need not be an irreducible pencil; fixed components must be tracked. Riemann–Roch is entirely compatible with the displayed effective adjoint. The contradiction claimed on p. 239 is therefore artificial. Restricting to an unnodal Enriques surface makes the prohibition vacuous, but does not repair its asserted general proof.

#### VII.1.2. The splitting argument and descent to low genus (pp. 239–243)

For a nef big class $C$ with $p_a(C)=\pi$, the numerical calculations for $2C$ are correct:

$$
(2C)^2=8\pi-8,\quad p_a(2C)=4\pi-3,\quad
\dim\vert 2C\vert =4\pi-4.
$$

The locus $\Sigma$ of unordered sums of two members of $\vert C\vert $ has dimension $2\pi-2$, and the same holds for the locus $\Sigma'$ from $\vert C+K_X\vert $. Under the expected generic injectivity of factorization into members, their degree is

$$
i=\frac12\binom{2\pi-2}{\pi-1}.
$$

One modern derivation pulls the hyperplane class back to $\mathbb P^{\pi-1}\times\mathbb P^{\pi-1}$, where it is $h_1+h_2$, and divides the top intersection by the degree two of the ordered-to-unordered map. The map is generically two-to-one because a general member of either original system is irreducible. This justifies the degree computation in its intended situation.

In $\mathbb P^{4\pi-4}$, two complementary-dimensional projective varieties of degree $i$ have intersection degree $i^2$ if the intersection is proper, and positive-dimensional intersection otherwise. This is a statement about cycle-theoretic length with multiplicities. It does not produce $i^2$ distinct decompositions. A common divisor gives two different partitions of its components, yielding the relations written on pp. 239–240, including $C_3\sim C_2+K_X$ and $C_4\sim C_1+K_X$ after a compatible labelling. Excluding a rational irreducible component with an effective adjoint uses proposition 7 correctly. But arbitrary pieces in the partitions need not themselves be irreducible, so each later use of a genus or a moving system requires component control.

The proposed descent either finds a moving system of smaller positive genus or reduces to genus-one components. The case analysis on p. 240 excludes some systems composed with an elliptic pencil by proposition 8. That exclusion is invalid. On p. 241 Enriques correctly allows shared rational components of two genus-one divisors and uses virtual intersection numbers rather than counting only visible distinct points. This acknowledgment does not remove the nodal cases from the earlier argument; it makes their omission more conspicuous.

The next step starts with half-fibres $E_1,E_2$ satisfying $E_1E_2=s>1$. Their sum has arithmetic genus $s+1$. Since the degree calculation gives $i^2\ge9$, the text seeks another decomposition beyond the displayed factorizations and thereby smaller $s$. Here the argument should be classified more favorably when the four half-fibres are integral, in particular in the unnodal case: the required local intersection calculation follows from regularity, infinitesimal rigidity, and uniqueness of factorization. It is an omitted explanation in that setting, rather than an independent genuine gap.

**Auditor's cohomological completion; high confidence under the stated factorization hypothesis.** For any effective isolated half-fibre $E$, the exact sequence

$$
0\longrightarrow\mathcal O_X\longrightarrow\mathcal O_X(E)
\longrightarrow N_{E/X}\longrightarrow0
$$

and $q=0$, $h^0(E)=1$ give $H^0(N_{E/X})=0$. Write the sections of the four half-fibres as $a,a',b,b'$, where $E_1\cap E'_1=E_2\cap E'_2=\varnothing$, and assume no two of the four divisors have a common component. At the common divisor $D=E_1+E'_1+E_2+E'_2$, the affine tangent spaces of the two pair loci are

$$
 ab\,H^0(L)+a'b'\,H^0(L),\qquad
 ab'\,H^0(L+K_X)+a'b\,H^0(L+K_X),
 \quad L=E_1+E_2.
$$

If $\delta$ lies in both, restriction to $E_1$, followed by cancellation of the nowhere-zero $a'$, gives $b'u=bv$ for suitable restricted sections. Since $b$ and $b'$ never vanish simultaneously, the local quotients $u/b=v/b'$ glue to a section of $N_{E_1/X}$. It is zero, so $\delta$ vanishes on $E_1$. Repeating this for all four half-fibres shows that $\delta$ is a multiple of the defining section of $D$. Projectivizing leaves zero intersection between these two tangent branches. To conclude that these are the entire local pair loci, one must also exclude additional factorization preimages. This is automatic when all four half-fibres are integral: the only partition into two members of $\vert L\vert $ is the first displayed pairing, and the only partition into two members of $\vert L+K_X\vert $ is the cross-pairing. The finite addition maps are immersive at these unique preimages, so the image branches are smooth and the common point is transverse of length one. Hence this point cannot absorb the intersection degree $i^2\ge9$. If the global intersection is positive dimensional, additional points exist anyway.

There is also a small parameter-space confusion in the printed phrase “due punti”: the two displayed pairings have the same total divisor $D$, so they are the two factorizations of one common point in the ambient $\vert 2L\vert $, not two distinct common divisors. Counting one transverse point only strengthens the conclusion.

This completion applies in particular to the unnodal configuration. With reducible half-fibres, even when they share no components, one must check that further partitions of their rational components do not create extra local image branches. If half-fibres share rational components, as the text explicitly permits on p. 241, vanishing on each divisor does not imply divisibility by their product with the required multiplicities; the tangent calculation itself then stops at that step. Separate analysis is needed for these reducible configurations, and the unrestricted reduction also still suffers from the false proposition 8. The audit therefore distinguishes the repairable integral-half-fibre argument from the substantive nodal obstruction.

The **modern replacement** for this descent is the lattice-and-linear-system theory of Enriques surfaces: one uses nef isotropic sequences and the associated low-degree polarizations, allowing configurations of $(-2)$-curves explicitly. In characteristic zero there are sufficiently long nef isotropic sequences to obtain the sextic and double-octic models; Dolgachev (2016, §5, pp. 15–16 of the author version) records the nondegeneracy result and its model consequence. This replaces the argument, not merely one missing algebraic manipulation. It does not authorize attributing the present audit's diagnosis or reconstruction to Enriques or to the authors of that theorem.

Once suitable half-fibres with $E_1E_2=1$ have been secured, the arithmetic of the proposed genus-three net is coherent. For

$$
L=E_1+E_2+E_2'=E_1'+2E_2,
$$

one has $L^2=4$, $p_a(L)=3$, and, when nef and big, $h^0(L)=3$. The stated two simple basepoints lower the moving self-intersection to two after blowing them up, producing a degree-two rational map to the plane. Their precise locations and simplicity require the relevant basepoint theorem or the generic configuration assumed by the construction; these are not consequences of the numerical equalities alone. Restricting the pencil $\vert 2E_2\vert $ to a general member of $\vert L\vert $ gives its degree-two map to $\mathbb P^1$, explaining the hyperelliptic genus-three sections. The contracted curves and branch singularities lead to the octic $D_8=D_6+p+q$, with the stated ordinary node and two tacnodal clusters on the residual sextic. The branch calculation is sketched and refers back to Chapter V, §7; it must be made on the resolved cover, rather than treating the singular plane branch as smooth.

#### VII.1.3. Parameter counts, the tetrahedral sextic, and Comessatti's construction (pp. 244–247)

The count on p. 244 contains a definite printing defect. Plane sextics form $\mathbb P^{27}$. The written subtraction $27-5\cdot3=12$ counts **five**, not four, assigned double points: the node $O$, each of the two tacnodes, and one infinitely-near double point at each tacnode. The tacnodal directions are prescribed by the lines to $O$. After allowing $O,M,N$ to vary, six parameters are restored; subtracting $\dim\operatorname{PGL}_3=8$ gives ten. Independence of these conditions and finite generic stabilizers are assumptions to verify on the appropriate open locus. The count is not, by itself, a proof that every Enriques surface has that model.

For the tetrahedral sextic, the space with a fixed coordinate tetrahedron has projective dimension thirteen. Its diagonal stabilizer has dimension three, giving ten parameters. The nonnormal model has degree six and ordinary double edges. A general transversal to two opposite edges has used four of its six intersection points and leaves two; this accounts for the double projection. A generic plane choice produces the stated degree-ten branch model, while the special choice through an adjacent edge yields the degree-eight version. Quadrics through three relevant edges induce genus-three hyperelliptic curves on the normalization. The inverse image of an ordinary double edge is a double cover of that line branched at four pinch points, hence is elliptic by Riemann–Hurwitz. Thus “the neighbourhood of the double line” must be interpreted through normalization; the singular line itself is rational.

A useful direct modern check of the general model is the conductor formula. If $\nu:X\to Y\subset\mathbb P^3$ normalizes an ordinary tetrahedral sextic and $\Delta$ is its conductor divisor, then

$$
\omega_X\simeq\nu^*\mathcal O_Y(2)(-\Delta).
$$

There is no quadric through all six edges, so $p_g=0$; the standard conductor exact sequence gives $q=0$; and the union of the four faces trivializes $2K_X$. This verifies the Enriques invariants without confusing the hypersurface dualizing sheaf with the canonical bundle of its normalization. Dolgachev (2016, §2) gives this normalization calculation. Special degenerations require checking that the normalization or minimal resolution remains in the desired class.

The ten-dimensional conclusion also has an intrinsic proof. The canonical étale double cover of a complex Enriques surface is a K3 surface. Pullback shows $H^0(T_X)=0$ and $H^0(\Omega_X^1\otimes K_X)=0$. Therefore $H^2(T_X)=0$ by duality. The tangent-bundle Riemann–Roch formula $\chi(T_X)=2K_X^2-10\chi(\mathcal O_X)=-10$ gives $h^1(T_X)=10$; the local deformation space is smooth of dimension ten. Global irreducibility requires the period/moduli theorem, not this local calculation. It is stated in Dolgachev (2016, §4). The discreteness of divisor classes when $q=0$, invoked on p. 245, is relevant to comparing a fixed polarization family with abstract surfaces, but it does not alone prove every parameter-count quotient is faithful or finite.

The footnote about infinitely many birational automorphisms must remain generic. Translation along an elliptic pencil by the difference of multisection classes can give an infinite group if the resulting Jacobian section is nontorsion. Intersection of the original curves is not a general substitute for a nontorsion proof. Some special Enriques surfaces have finite automorphism group; the modern theory explicitly treats this distinction (Dolgachev & Kondō, 2025). Since an Enriques surface is minimal with nonnegative Kodaira dimension, its birational self-maps are regular automorphisms.

The proposed Comessatti construction on pp. 245–246 has a stronger defect than an omitted dominance check: its stated cubic has a **connected**, rather than split, inverse image under the double cover with the full branch $D_8=D_6+p+q$. The following divisor calculation uses exactly the incidences printed here; it is the auditor's derivation, not a claim about the original Comessatti paper.

Let $E=K_3$ be the smooth plane cubic and $H=\mathcal O_E(1)$. The two distinct points $P,Q$ have the same tangential point $O$, so

$$
 p\vert _E=2P+O\sim H,\qquad q\vert _E=2Q+O\sim H.
$$

Put $T=A_1+\cdots+A_4$. The stipulated second cubic $K'_3$ gives

$$
3H\sim O+2P+2Q+T.
$$

The residual sextic therefore restricts with divisor $2O+4P+4Q+2T$, the double of the divisor of $K'_3\vert _E$. Up to a nonzero complex scalar its restriction is a square. But the actual branch section is the product of that sextic with **both** tangent lines. Its half-intersection divisor on $E$ is

$$
D=2O+3P+3Q+T\sim3H+O+P+Q.
$$

Since the plane octic cover uses the line bundle $\mathcal O_{\mathbb P^2}(4)$, normalization of its restriction to $E$ gives the unramified quadratic algebra governed by

$$
\eta=\mathcal O_E(4H-D)
      =\mathcal O_E(H-O-P-Q)
      =\mathcal O_E(P-Q).
$$

This is nontrivial two-torsion: $2(P-Q)\sim0$ follows from the two tangencies, while $P-Q\not\sim0$ for distinct points on a smooth elliptic curve. Thus the normalized inverse image is the connected étale double cover associated with $\eta$, itself of genus one. It is not two elliptic curves each mapping isomorphically to $E$. Blow-ups and resolution cannot turn this nontrivial generic quadratic field extension into a split algebra. To obtain a split cubic, the residual half-contact divisor must be shifted by this nonzero two-torsion class; the printed condition puts it in the wrong class. This establishes a definite error in the reproduced construction, without disproving the independent modern tetrahedral-sextic model theorem.

The asserted $\infty^5$ family for the **printed**, nonsplitting incidence is nevertheless correct and has a direct construction. Fix equations $e,e'$ for $E,K'_3$. Every compatible sextic has the form

$$
f=c(e')^2+e g,
$$

where $g$ is a cubic through $O$ and tangent to $E$ at $P,Q$, allowing higher order as a closed condition. These five linear conditions cut a five-dimensional vector space of cubics. More intrinsically, restriction to $E$ has the one-dimensional kernel spanned by $e$, while $\mathcal O_E(3H-O-2P-2Q)$ has degree four and hence four sections. Adding the coefficient $c$ gives six independent sextic sections, a projective space of dimension five. Conversely the prescribed contacts force $f\vert _E=c(e'\vert _E)^2$, so the difference is divisible by $e$, and the same singularity constraints force precisely these conditions on $g$.

The singularities also have the intended generic type. In local coordinates at $P$, write $e=y+a x^2+\cdots$, $e'=b y+c_2x^2+\cdots$, and $g=d y+e_2x^2+\cdots$. Then $f$ starts with a nonzero multiple of $y^2$, a possible $yx^2$ term, and an $x^4$ term. A general choice gives two smooth tangent branches with intersection multiplicity two, an ordinary tacnode; the same calculation holds at $Q$. The quadratic part at $O$ is generically nondegenerate, giving a node, and the four $A_i$ are ordinary contacts with $E$. Bertini applies away from this finite base scheme. This repairs the dimension and nonemptiness of the specified incidence family while confirming, rather than removing, the global two-torsion obstruction.

Even after correcting that class, a proof that the corrected incidence construction dominates the branch family would require nonemptiness, independent tangency conditions, and a dominance calculation. Those steps are not supplied here. No unverified historical repair is attributed to Comessatti.

For a correctly chosen split cubic, the subsequent divisor construction would be numerically clear: add an elliptic bisection to the genus-two pencil. If its classes are $A$ and $B$, with $A^2=2$, $B^2=0$, $AB=2$, then $(A+B)^2=6$, $p_a(A+B)=4$, and $h^0(A+B)=4$ under nefness. This yields the proposed sextic map. The scan confirms $\infty^3$, not $\infty^2$, for the plane sextics representing its hyperplane sections. Three suitable half-fibres meeting pairwise once account for one triangular set of double edges; their partners account for the complementary edges. This is a sketch of projective realization, not a complete verification of birationality and the entire conductor scheme.

The concurrent-face degeneration on p. 246 and the infinitely-near opposite-edge degeneration on p. 247 are also sketches. Their asserted quadruple vertex, triple line, residual double lines, and corresponding infinitely-near tacnode are recorded separately in the claim register. A rigorous treatment needs explicit equations or a flat family and resolution of the limiting nonnormal surface. No such family is supplied here, and these delicate degeneration assertions are not certified merely by the correct invariants of the generic model.

### VII.2. K3 surfaces: linear systems, models, and Noether–Lefschetz (§2, pp. 247–254)

#### VII.2.1. The exact dimension formula and its exceptions (p. 247)

A minimal regular surface with $K_X\sim0$ is a K3 surface in the present complex projective setting. Every $P_m=1$. For a divisor $D$, adjunction gives $D^2=2p_a(D)-2$; for a smooth member $C$, its normal bundle is $\mathcal O_C(C)=\omega_C$. This explains the canonical characteristic series without presupposing an embedding of $X$.

The statement that every connected effective divisor has $\dim\vert D\vert =p_a(D)$ is too broad. The exact result, for a nonzero effective $D$, is

$$
h^1(\mathcal O_X(D))=h^0(\mathcal O_D)-1,
\qquad
\dim\vert D\vert =p_a(D)+h^0(\mathcal O_D)-1.
$$

To prove it, use $0\to\mathcal O_X(-D)\to\mathcal O_X\to\mathcal O_D\to0$, the vanishings $H^0(\mathcal O_X(-D))=H^1(\mathcal O_X)=0$, and Serre duality $h^1(-D)=h^1(D)$. Surface Riemann–Roch then gives the second equality. A reduced connected proper curve has only constant global functions, so the desired equality holds in that case. It also holds for a 1-connected effective divisor. Huybrechts (2016, Chapter 2, Proposition 3.1 and Remark 3.2) explains the stronger connectedness/vanishing argument.

**Auditor's explicit counterexample; high confidence.** Take an elliptic K3 with fibre $F$ and section $R$. Then $F^2=0$, $R^2=-2$, and $FR=1$. The connected nonreduced divisor $D=4F+3R$ has $D^2=6$, $p_a(D)=4$, and $DR=-2$. Thus $R$ is fixed. The class $D-R=4F+2R=2(2F+R)$ is nef and big: $(2F+R)R=0$, and every other irreducible curve has nonnegative intersection with both $F$ and $R$. Its square is eight, so vanishing gives $h^0(D-R)=6$. Hence $\dim\vert D\vert =5$, not four. Equivalently $h^0(\mathcal O_D)=2$. This identifies precisely the missing hypothesis.

The example $sF$, $s>1$, is correct: $p_a(sF)=1$, but $h^0(sF)=s+1$, so $\dim\vert sF\vert =s$. The claim that systems with a fixed rational component are always superabundant needs a convention. For $D=sF+R$, $s\ge2$, the restriction to the generic fibre has degree one and its unique effective divisor is the section point. Therefore every member contains $R$, and $h^0(D)=h^0(sF)=s+1$. But $p_a(D)=s$, so $h^1(D)=0$. It is superabundant only relative to the genus-one moving part, not relative to the arithmetic genus of the full divisor. Enriques's following exception about adding a rational unisection to a multiple fibre system is consistent with this same calculation. A general assertion about enlarging a linear system upon adding a component requires the restriction exact sequence and its connecting map, not just the number of intersection points.

#### VII.2.2. Low-genus projective models (pp. 248–249)

For a nef big generated class $H$, set $H^2=2g-2$. Then $h^0(H)=g+1$. The map has degree two onto $\mathbb P^2$ for genus two, with branch sextic in the smooth generic case. The double-cover formula gives $K_X=f^*(K_{\mathbb P^2}+\mathcal O(3))=0$ and $q=0$. A nonhyperelliptic genus-three polarization gives a quartic in $\mathbb P^3$; genus four gives a $(2,3)$ complete intersection in $\mathbb P^4$; and the appropriate nontrigonal genus-five case gives an intersection of three quadrics in $\mathbb P^5$. Smooth complete intersections of those degrees have trivial canonical bundle by adjunction and irregularity zero by their Koszul resolutions.

The genus-four calculation can be completed without assuming restriction-map surjectivity in advance. Once the image is known to be an integral nondegenerate degree-six surface in $\mathbb P^4$, the inequality $15>h^0(2H)=14$ gives at least one containing quadric. It is irreducible, since a reducible quadric would force the integral surface into a hyperplane. Two independent quadrics would intersect in a degree-four surface, which cannot contain this degree-six surface, so the quadric is unique. Likewise $35-h^0(3H)=6$ gives at least six independent cubic equations. The linear multiples of the quadric span only five dimensions, so an independent cubic exists. Its complete intersection with the irreducible quadric has degree six and contains the image; Bézout and unmixedness identify the two surfaces. The Koszul resolution then verifies the exact dimensions and projective normality. Thus the genuine prerequisites are the birational, nondegenerate degree-six model and the cohomology values, not a separately assumed restriction-surjectivity theorem.

For genus five, $h^0(2H)=18$, against twenty-one quadrics, gives at least three independent equations; projective normality makes this exactly a net. Having three equations does not alone prove a complete intersection: one must exclude a containing scroll or other exceptional base locus. The minimum-genus premise is intended to exclude smaller pencils, but its connection to these projective exceptions needs proof. Modern statements are provided by Saint-Donat (1974) and Huybrechts (2016, Chapter 2, including Corollary 2.5 on projective normality). The original Saint-Donat paper's metadata and DOI were verified; its interior theorem and section locations were not independently checked. Huybrechts's inspected account supplies the working theorem references.

One must keep the map and the embedded model distinct. Even an ample class may have a degree-two map in a special case. For example a genus-two class $L$ has $L^2=2$; $2L$ has square eight and six sections, but maps two-to-one onto the Veronese surface of degree four in $\mathbb P^5$. The same numerical self-intersection as a complete intersection of three quadrics does not force the same map.

#### VII.2.3. The conic induction and the count of nineteen (pp. 249–251)

Enriques proposes an induction using a conic $R$ on a model of degree $2g-2$. Such a conic is rational, with $R^2=-2$ and $HR=2$. Then

$$
(H+R)^2=2g,\qquad p_a(H+R)=g+1,\qquad (H+R)R=0.
$$

A suitable generated $H+R$ contracts $R$ to an ordinary double point on a model of the next degree. Conversely projection from such a node recovers the conic model. These numerical identities are correct. Generation, the identification of the singularity as an ordinary double point, and smoothing inside a complete family need additional geometric arguments.

The count via hyperplanes with multiple tangencies predicts codimension one for the conic locus. The text then uses triple-point rational models to argue that the full family has nineteen parameters and the nodal locus has eighteen. Its first triple-point count is wrong by one even in the quartic case: a triple point at a fixed point of $\mathbb P^3$ imposes ten linear jet conditions, and a moving point restores three parameters, giving codimension seven. Quartic equations form $\mathbb P^{34}$; modulo $\operatorname{PGL}_4$, smooth quartics have nineteen parameters, and the ordinary triple-point locus has twelve. The later number six, for making an already nodal quartic triple, is correct as a relative codimension $7-1$. The two occurrences must not both be corrected to seven.

The plane representation of a rational triple-point model uses twelve base points on a cubic subject to one divisor-class relation; together with the cubic's modulus this motivates the twelve-parameter count. It does not prove that every surface in a proposed higher-genus family can be specialized to that rational model with independent conditions. On p. 251 Enriques explicitly admits that the reducible-section parameter argument, derived from Noether, is not rigorous. For a transverse union $C_1+C_2$ meeting in $m$ points, the correct arithmetic genus is $g_1+g_2+m-1$. The subsequent “number of parameters minus number of conditions” calculation presumes independence and a dominating incidence map. Neither follows from arithmetic genus. This is an acknowledged sketch, not evidence that the true Noether–Lefschetz statement is false.

Here is a modern proof of the main dimension assertion. A nowhere-zero holomorphic two-form identifies $T_X$ with $\Omega_X^1$. Thus $h^1(T_X)=h^{1,1}(X)=20$ and $H^2(T_X)=H^0(\Omega_X^1)^*=0$. The Kuranishi space is smooth of dimension twenty. Requiring a fixed nonzero integral polarization class to stay of type $(1,1)$ cuts out one smooth equation: in the period domain it is one nontrivial orthogonality condition. Therefore the locally polarized deformation space has dimension nineteen. The global period theorem gives an irreducible nineteen-dimensional moduli space for each primitive positive degree. Huybrechts (2016, Chapter 6, §2 and Corollary 4.4) is a verified locator for these period and moduli statements. This proof replaces the condition counts; it is not a claim about what a historical author had already proved.

The same method proves the required Noether–Lefschetz assertion. In the polarized period domain, every additional independent integral $(1,1)$-class imposes a proper hyperplane condition. There are countably many integral classes. Outside their union the Picard group is $\mathbb Z H$. Accordingly “general” must mean **very general**, not all members of one Zariski-open set. With $H$ primitive and $H^2=2g-2$, every effective positive-square class is a positive multiple of $H$, so the minimum genus of a moving positive-square system is $g$. Existence for every $g\ge2$ follows from the existence and period theory of primitive degree-$2g-2$ polarized K3 surfaces. A birational map between smooth minimal K3 surfaces is an isomorphism; their Picard lattices then distinguish the very general rank-one examples of different primitive degree.

#### VII.2.4. Franchetta's degeneration as reproduced by Enriques (pp. 251–254)

The reproduced argument specializes a smooth quartic to a monoid $\Phi_4$ with a triple point. Its resolution is presented by blowing up twelve points $A_i$ on a plane cubic $C_3$. Let $H$ be the pullback of a line and $E_i$ the exceptional classes. The quartic hyperplane class is $4H-\sum E_i$, with square four, while the cubic class $3H-\sum E_i$ is contracted in the model. A curve in the limit is allowed to contain a moving plane part, the cubic with multiplicity $s$, and exceptional components with multiplicities $h_i$. Writing its resulting plane degree as $n$ and multiplicities as $a_i=r_i+s-h_i$, the two equalities printed on p. 252 are

$$
n^2-\sum a_i^2=2\pi-2,
\qquad n(n-3)-\sum a_i(a_i-1)=2\pi-2.
$$

Subtracting gives $3n=\sum a_i$, equivalently zero intersection with the cubic class. These formal intersection calculations are correct provided the chosen total-transform classes, arithmetic genus, and degree are in fact preserved in the specialization.

The preceding opening argument on p. 252 also needs its exact conditional reading. If a specialized curve is a complete intersection with a degree-$m$ surface, Enriques compares $\vert C\vert $ with $\vert mH\vert $, then invokes the impossibility of a $g^{\pi}_{2\pi-2}$ on a smooth genus-$\pi$ curve. The curve-theoretic statement is valid for $\pi\ge2$: RR gives $h^0(A)=\pi-1+h^0(K_C-A)\le\pi$ for a degree-$2\pi-2$ line bundle $A$. The unresolved part is the comparison of the original and limiting systems and their numerical intersections. If the degeneration has already established $H C=mH^2$ and $C^2=m^2H^2$ on the original quartic, the Hodge index theorem provides a clean modern route: $C-mH$ has square zero and is orthogonal to the ample class $H$, hence is numerically zero; torsion-freeness of the K3 Picard group then gives $C\sim mH$. That is a conditional completion, not a substitute for proving the specialization hypotheses.

In the first case, with no added cubic or exceptional pieces, restricting the plane divisor to the cubic gives $\sum r_iA_i\sim nG$, while the quartic base relation gives $\sum A_i\sim4G$. Subtracting $r_1$ times the latter yields the displayed relation among the eleven remaining points. For very general points subject to the one quartic relation, no other integral relation holds, so $r_i=r$ and $n=4r$. The required genericity is stronger than arbitrary distinct points: special points on an elliptic curve can satisfy additional torsion or divisor relations.

The second case appends exceptional curves but no cubic; the assertion that the resulting limiting divisor cannot arise is called “obvious,” but the reproduction supplies no flat-family or relative-Hilbert-scheme justification. In the third case, with $s>0$, the inequalities involving $\ell=C_m C_3$, $t$ exceptional components, and $s$ organize the numerical possibilities. The argument that $\ell+t\ge4$ enlarges the limiting system, whereas $\ell+t<4$ forces a loss of one dimension, relies on the specialized system remaining complete and on control of fixed parts. Upper semicontinuity alone does not preserve completeness of a selected limiting subspace of sections, nor does it prevent vertical components. The missing ingredients are a specified family, a relative line bundle or appropriate cycle, constancy of the relevant Hilbert polynomial, and a comparison of the actual limiting section spaces.

This audit therefore records a gap in **the proof as reproduced on these pages**, not a verdict on the entire original Franchetta paper, which was not independently obtained. The period proof above establishes the modern very-general conclusion without those unproved specialization steps. No attribution of that replacement proof to Franchetta is intended.

The concluding formula $n=s\nu$, $\pi-1=s(\gamma-1)$ is ambiguous because the text moves between multiples of divisor systems and multiple coverings of projective models. If $H=mL$, then

$$
H^2=m^2L^2,\qquad p_a(H)-1=m^2(p_a(L)-1).
$$

If instead a map defined by $H$ has degree $s$ onto a surface of projective degree $\nu$, then $H^2=s\nu$. These are different integers. No blanket replacement of $s$ by $s^2$ can repair every interpretation. This distinction also governs the examples on p. 257.

### VII.3. Historical notice and the scope of the irreducibility claim (§3, pp. 254–257)

The notice is part of the audit. Enriques credits Castelnuovo's 1893 work, his own 1896 double-plane paper, his 1908 study of genus-one surfaces, Severi's 1909 work on a canonical curve of order zero, Franchetta's 1942 argument, and d'Orgeval's 1945 volume. He mentions Noether's 1883 method, Rohn's 1897 discussion, Fano's 1909 argument, Lefschetz's 1921 and 1923 treatments, and du Val's two 1932 notes. These are **attributions reported in the supplied primary source**. Unless separately identified in the bibliography below, their full original publication metadata and the interiors of their proofs were not verified in this audit. Dates and theorem locations must not be manufactured from a modern recollection.

The Kummer-surface argument starts with three moduli and sixteen nodes. It predicts nineteen after smoothing the nodes independently. Independence is the issue to prove, not something obtained by adding sixteen to three. Simultaneous resolution, lattice-polarized deformation theory, and the period description give the appropriate modern setting. The analogous argument using a quartic with four disjoint rational curves also requires independent deformation conditions. Enriques himself notes a small gap in Severi's proof but does not identify it precisely; this audit does not invent its location or a named repair.

The elliptic examples on p. 255 are a useful construction of polarizations. If $F$ is an elliptic fibre and $H F=3$, then $(H+sF)^2=H^2+6s$, so the genus rises by $3s$. Starting from genera two, three, and four supplies the three residue classes modulo three. This does not show that the general polarized K3 of those genera carries an elliptic pencil. It gives special examples and possible starting points for deformation. Generation and contraction of any $(-2)$-classes must still be checked for the chosen divisor.

The projective examples on p. 257 distinguish two questions. A degree-eight polarized map may be a complete intersection of three quadrics, or may be the degree-two map associated with $2L$, $L^2=2$, onto the Veronese surface. The branch sextic has degree twelve after the Veronese embedding. Likewise a quartic with hyperplane class $H$ has $(2H)^2=16$ and $h^0(2H)=10$, giving a degree-sixteen embedding in $\mathbb P^9$; this is not a four-sheeted cover of a quartic. The scan securely reads $F_{16}$, not $F_{18}$.

The final “one family” assertion is correct in a modern formulation with a fixed **primitive** polarization degree and the appropriate moduli space; Huybrechts's Chapter 6, Corollary 4.4 verifies irreducibility. It cannot be taken to say that primitive and imprimitive integral polarizations of the same square are automatically joined in a smooth family of polarized K3 surfaces. Divisibility in the integral cohomology lattice is locally constant under parallel transport. Nor do distinct maps on one K3 automatically give distinct unpolarized surfaces. The two nodal degree-ten examples mentioned by du Val may have a common smoothing in their stated setting, but the original notes were not checked here and are recorded as cited results, not newly verified smoothing theorems.

### VII.4. Genus-one fibrations and their limitations as a classification (§4, pp. 257–266)

#### VII.4.1. From linear genus one to a genus-one pencil (pp. 257–259)

On a minimal surface of nonnegative Kodaira dimension with $K_X^2=0$, there are two possibilities relevant here: $\kappa(X)=0$ or $\kappa(X)=1$. In the latter case abundance for surfaces makes a positive multiple of $K_X$ semiample. Its Stein factorization is a morphism $f:X\to B$ with connected fibres. A general fibre $F$ has $F^2=0$ and $K_XF=0$, hence genus one by adjunction. The sketch in the text is in this direction, but needs semiampleness, removal of fixed components, and Stein factorization. A regular surface has $g(B)=0$, since pullback injects $H^1(\mathcal O_B)$ into $H^1(\mathcal O_X)$.

The regular $\kappa=0$ cases are Enriques and K3. Enriques surfaces have genus-one pencils by the theorem used in §1. K3 surfaces may or may not have one: for instance a K3 with $\operatorname{Pic}(X)=\mathbb Z H$, $H^2>0$, has no nonzero isotropic divisor. Thus the exception in the italic conclusion on p. 258 means that an elliptic pencil is not automatic for K3 surfaces, not that no K3 surface can be elliptic.

For an effective pluricanonical divisor on a minimal $K^2=0$ surface, $p_a(mK)=1$, but this does not make its support a single smooth elliptic curve. It is usually a sum of vertical components. The distinction between arithmetic genus, reducibility, and support is indispensable.

Noether's formula gives $e(X)=12\chi(\mathcal O_X)=12(p+1)$. For a genus-one fibration, the Euler number is the sum of the Euler contributions of singular fibres, since the smooth fibre has Euler number zero. Enriques's count $S=12p+12$ can be read as the number of nodal singularities after an appropriate generic deformation, or as a weighted singular-fibre count. It is not the number of singular fibres for an arbitrary fibration: an $I_n$-fibre contributes $n$, and the other Kodaira types have their own contributions. This is the necessary interpretation of the Zeuthen formula $I=S-4=12p+8$ imported from Chapter V. Schütt and Shioda (2010, §§4 and 6) supply the modern elliptic-surface context.

Enriques's determinant $d$ is the minimum positive degree of a multisection, equivalently the index of the generic genus-one curve over $\mathbb C(B)$. It is not its discriminant or the determinant of the Néron–Severi lattice. A degree-one multisection is a section; a section excludes multiple fibres. Over the generic field a degree-$d$ divisor yields a degree-two map to a rational curve when $d=2$, and a degree-$d$ projective embedding for $d\ge3$. Over $\mathbb C(t)$ the necessary degree-two target conic is rational; over other fields a conic obstruction would have to be retained. These generic maps extend after resolving indeterminacies and passing to ruled models. Existence of a genus-one curve with a given index does not make the pair $(p,d)$ a complete birational invariant.

The Riemann–Roch step on p. 259 has a printed numerical error. If $L F=d$, then

$$
(L+F)^2-L^2=2d,\quad
p_a(L+F)-p_a(L)=d,\quad
\chi(L+F)-\chi(L)=d.
$$

Only the first increment is $2d$. For a rigorous eventual statement, let $E=f_*\mathcal O_X(L)$, a vector bundle of rank $d$ away from possible finite issues that can be absorbed in the sheaf. The projection formula gives $H^0(X,L+sF)=H^0(\mathbb P^1,E(s))$; for large $s$ the dimension grows by exactly $d$ with each increment. This proves eventual section growth. It does not itself prove irreducibility; that follows by the generic-fibre map and an appropriate generated moving system. In the degree-one case $\vert L+sF\vert $ retains the section as a fixed horizontal part; one uses a higher multiple such as $3L+sF$ to obtain the Weierstrass model.

#### VII.4.2. Types I and II do not exhaust determinant one (pp. 259–262)

The two stated plane branch forms have the asserted invariants under their generic singularity assumptions. Type I has a branch curve of degree $2n$ with an ordinary $(2n-3)$-fold point. Blow up that point to obtain $\mathbb F_1$, with negative section $S$ and fibre $F$, $S^2=-1$, $SF=1$. The total branch divisor for the normalized double cover is

$$
B=S+(3S+2nF)=4S+2nF=2(2S+nF).
$$

Since $K_{\mathbb F_1}=-2S-3F$, the double-cover formula gives $K=(n-3)F$ after resolving the ordinary branch crossings, and $\chi=n-1$, hence $p_g=n-2$ and $P_m=m(p-1)+1$ for $p\ge1$. There is a ramification section, so the index is one. Type II's additional quadruple-point resolution lowers $\chi$ by one and produces $p_g=n-3$, with the same minimal canonical formula in terms of $p$. The footnote's letters $OP,P$ must be $OB,B$.

The exceptional curves in type II can also be checked explicitly. **Auditor's resolution calculation; high confidence for ordinary branch tangents.** Blow up $O$, then the ordinary quadruple point $B$, and resolve all the ordinary branch crossings of the exceptional section over $O$ with the residual branch. One of those crossings is on the strict transform of $OB$; call its exceptional curve $E_1$. In total-transform notation, the relevant branch line is

$$
\ell=H-E_O-E_B-E_1,\qquad \ell^2=-2.
$$

It is a branch component, so $\pi^*\ell=2R$ and $R^2=-1$. The inverse image $V$ of $E_B$ is a smooth elliptic curve of square $-2$, since it is a double cover branched at four distinct points. The inverse image $W$ of $E_1$ is rational of square $-2$, branched at two points. Their fibre is

$$
2R+V+W,\qquad R V=R W=1,\qquad V W=0.
$$

Contracting $R$ makes $W$ a rational $(-1)$-curve, gives $V^2=-1$, and makes $V W=1$. Contracting $W$ then makes $V^2=0$: it is the smooth fibre on the relatively minimal model. There are **two successive rational contractions**, not two disjoint lifts of the branch line, and not two rational curves both of square $-1$ on the first resolved cover. This is the coherent interpretation of the footnote's compressed wording.

As a consistency check, after the first two base blow-ups,

$$
K_Y+L=(n-3)(H-E_O)-E_B,
$$

whose square is $-1$. Ordinary branch-node resolutions do not change the cover's canonical square, so the resolved cover has $K^2=-2$. The two contractions raise it to zero. The quadruple-point correction to $\chi$ is one, while ordinary branch-node corrections are zero; hence $\chi=n-2$ and $p_g=n-3$. This resolves the geometric issue in the footnote under the stated genericity assumptions.

The claimed **completeness** of these two forms is the serious issue. There is a concrete test, not just a disagreement of formal counts.

**Auditor's derivation, checked also against the parameter difference; high confidence.** In generic type I, the residual branch curve $3S+2nF$ meets $S$ transversely in $2n-3=2p+1$ points. At each crossing the double cover has an $A_1$ singularity. In a local fibre coordinate $u$ with section $u=0$, the cover has the form $w^2=u(u-t)$ up to units and the remaining nonvanishing branch factors. The special fibre's normalization is rational; resolving the surface node adds another rational component joining its two branches, yielding an $I_2$-fibre. These fibres persist on the relatively minimal model for $p\ge1$. Type I therefore imposes $2p+1$ reducible fibres.

In contrast a general Weierstrass surface over $\mathbb P^1$, with $\chi=p+1$, is given by

$$
y^2=x^3+A(t)x+B(t),\quad
A\in H^0(\mathcal O(4\chi)),\quad B\in H^0(\mathcal O(6\chi)).
$$

For general coefficients its discriminant has $12\chi$ simple zeros and all singular fibres are $I_1$. The coefficient dimension, minus one scaling and three base automorphisms, is

$$
(4\chi+1)+(6\chi+1)-1-3=10\chi-2=10p+8.
$$

Type I's printed count $8p+7$ is lower by $2p+1$, exactly the number of imposed $I_2$-fibres. For $p>1$, the genus-one fibration is the Iitaka fibration and is determined birationally. A general Jacobian surface with only $I_1$-fibres cannot be birationally changed into this type-I fibration. Type II likewise retains branch-section crossings away from its distinguished quadruple-point fibre, and thus does not supply the omitted general surfaces. The claimed minimal-degree Cremona reduction must have omitted necessary infinitely-near or other singularity possibilities, or must be restricted to a smaller class. The text supplies no proof capable of deciding a complete corrected list.

The individual plane parameter calculations are still useful descriptions of their loci. Type I with fixed $O$ has $8n-3$ coefficients projectively; subtracting the six-dimensional stabilizer gives $8n-9=8p+7$. Type II gives the printed $8n-13$ and $8n-19=8p+5$, conditional on the stated transformation group and condition independence. Those calculations cannot be promoted to the dimension of all index-one surfaces.

The response to the Chapter V lower bound explains that an index can drop on special members of a degree-two model family. This phenomenon is reasonable, but does not cure the missing generic Jacobian models. Types $\mathrm I'$ and $\mathrm{II}'$ have a $(2n-4)$-fold point, and their counts $10n-12=10p+8$ and $10n-22=10p+8$ match the natural genus-one parameter dimension. With the generic branch conditions they are index-two families; a degree-two map alone only implies index divides two, since special members can have sections.

#### VII.4.3. Multiple fibres, the canonical bundle formula, and the printed constants (pp. 262–264)

For a relatively minimal complex genus-one fibration $f:X\to B$, write its multiple fibres as $m_jF_j$, with primitive fibre divisors $F_j$, and put $\mathcal L=(R^1f_*\mathcal O_X)^{-1}$. Then

$$
K_X\sim f^*(K_B+\mathcal L)+\sum_j(m_j-1)F_j,
\qquad \deg\mathcal L=\chi(\mathcal O_X).
$$

This formula is for a relatively minimal smooth surface. Blow-ups add exceptional divisors to the canonical class. It is also specifically characteristic zero; wild fibres in positive characteristic require further terms. For the regular case $B=\mathbb P^1$, $\deg(K_B+\mathcal L)=p-1$, and taking pushforward of the pluricanonical sheaf yields

$$
P_m=\max\left\{0,\,1+m(p-1)+\sum_j
\left\lfloor\frac{m(m_j-1)}{m_j}\right\rfloor\right\}.
$$

The floor appears because $m_jF_j$ is the pullback of a base point, whereas a residual coefficient strictly between zero and $m_j$ remains fixed. This gives both the variable and fixed parts and proves all the required dimension formulas. A verified general reference is Dolgachev (1981, Chapter II, §1, canonical-divisor theorem and corollaries in author-PDF pp. 32–34); Schütt and Shioda's Theorem 6.8 is the section case and is not used alone to justify the multiple-fibre terms.

If there are $s$ double fibres and no other multiples, the formula becomes

$$
P_{2i}=\max\{0,1+2i(p-1)+si\},\qquad
P_{2i+1}=\max\{0,1+(2i+1)(p-1)+si\}.
$$

Under the positivity assumptions of pp. 262–263 the maxima can be omitted. In particular $P_2=2(p-1)+s+1$. The minus-one constant on p. 262 is a printed misprint. The missing $+1$ in $P=2(p-1)$ for $\mathrm I',\mathrm{II}'$ on p. 263 is another. Finally $p=n-2-s$ implies $p-1=n-3-s$, not the printed $n-3$. All three were checked against the scan before assigning them to the original printing.

Type III adds $s$ branch lines through $O$ and $s$ $[3,3]$-clusters. The residual curve has degree $2n-s$, multiplicity $2n-s-4$ at $O$, and the stated tacnodes. The double-cover/canonical-resolution calculation gives $p=n-2-s$, and these clusters correspond to double fibres. This records the intended generic configuration; completeness of the purported normal-form list is not independently supplied.

The residual-branch parameter calculation gives $5(2n-s)-6-6s$ with the point cluster prescribed. Allowing the $s+1$ points and quotienting by $\operatorname{PGL}_3$ gives the formal contribution $2(s+1)-8=2(s-3)$, not $2s-3$. The following printed total already uses the correct value:

$$
M=10n-9s-12=10p+s+8=8p+P_2+9.
$$

For $s=1,2$, a negative formal contribution is not literally a negative-dimensional moduli space of configurations: the point configuration has a positive-dimensional stabilizer, which must act on the curve coefficients in the combined calculation. As always, independence and finite generic stabilizer of the full object are required. The specialization $p=0,s=2$ gives $P_2=1$ and $M=10$, agreeing with Enriques surfaces and providing an internal check on the corrected constants.

For general determinant $d$, every fibre multiplicity divides $d$, because $d=L\cdot(m_jF_j)=m_j(LF_j)$. This is a genuine necessary condition. The counts $s_r$ of fibres of each multiplicity, together with $p$, determine the displayed plurigenera via the floor formula. They do not classify the surface. A Jacobian elliptic surface, a torsor class over its generic fibre, and the global gluing and local multiple-fibre data remain necessary. Enriques acknowledges the difficulty of the arithmetic description for $d>2$; the phrase that the classification is substantially solved should not be read as a theorem that these integers are complete birational invariants.

#### VII.4.4. The Jacobian and the irregular extension (pp. 265–266)

Let $C$ be the generic genus-one curve over $K=\mathbb C(B)$, and $J=\operatorname{Pic}^0(C)$. A degree-$d$ divisor class identifies $\operatorname{Pic}^d(C)$ with $J$ by translation. This does not identify $C$ with $J$ over $K$ unless the torsor has a $K$-rational point. They become isomorphic over an algebraic closure. The relatively minimal surface with generic fibre $J$ is the Jacobian fibration and has a section.

The text's $[d,d]$ correspondence can be made precise without assuming a rationally varying choice of effective divisors over the whole Picard variety. **Auditor's construction; high confidence.** Fix a separable degree-$d$ multisection divisor $p_1+\cdots+p_d$ on $C$. Over a splitting field take the union of the graphs of the maps

$$
x\longmapsto[x-p_i]\in J.
$$

The union is Galois invariant and descends to a correspondence $C\dashrightarrow J$. Each projection has generic degree $d$, and its closure gives the surface correspondence over the base. This is a multivalued correspondence, not a claimed single birational map. It avoids the descent and universal-divisor issue concealed in selecting representatives of all $g_d^{d-1}$'s at once.

A genus-one fibration and its Jacobian have corresponding reduced singular-fibre Euler contributions and the same $\chi(\mathcal O)$. In particular their arithmetic genera agree. When they are regular, their geometric genera agree as well. Multiple smooth fibres contribute zero Euler number; multiple singular fibres must not simply be called smooth. Dolgachev (1981, Chapter II, §1, Propositions 1–2) verifies the local comparison with the Jacobian; its treatment also exhibits the torsor data omitted by numerical invariants alone.

For irregular surfaces with $\chi>0$, the genus of the base equals $q$. Indeed the fundamental line bundle has positive degree, so the $H^0(B,R^1f_*\mathcal O_X)$ term in Leray vanishes, leaving $h^1(\mathcal O_X)=g(B)$. In Enriques's notation this is $g(B)=p_g-p_a$. The chapter refers this extension to continuous systems and to Chapter IX; it does not prove all of it here.

The $p_a=-1$, equivalently $\chi=0$, case needs care. It includes abelian and bielliptic surfaces, but also properly elliptic surfaces such as $E\times B$ with $g(B)\ge2$. For this product, $K^2=0$, $p_g=g(B)$, $q=g(B)+1$, and translation in $E$ gives a one-dimensional connected automorphism group. An abelian surface gives a two-dimensional translation group. Thus Enriques's historical words “elliptic and hyperelliptic” should not be equated with only the modern Kodaira-dimension-zero classes. The group statement is deferred to Chapter XI, outside the supplied extract. This audit verifies the examples and explains the scope, rather than supplying an absent proof of that entire later classification.

### VII.5. Further examples, extensions, and unresolved questions

The examples in this section are the auditor's, except where a source is expressly identified. They are not historical claims about who first repaired Enriques's arguments.

1. **A concrete connectedness test.** On any elliptic K3 with section, the family $aF+bR$ lets one test which fixed rational parts create nonzero $H^1$. The divisor $4F+3R$ above gives a fully checked counterexample, whereas $sF+R$ demonstrates that a fixed rational part alone is insufficient. Confidence: high, because all dimensions follow from exact sequences and nef-big vanishing.

2. **A geometric explanation of a parameter deficit.** Type I's missing $2p+1$ parameters correspond exactly to $2p+1$ imposed $I_2$-fibres. This suggests studying the normal-form construction as a lattice-polarized or prescribed-fibre stratum, rather than discarding its useful equations. Confidence: high for the generic type-I local and dimension calculation; no assertion of a globally complete stratification is made.

3. **A corrected incidence problem for the adjoint cubic.** The explicit calculation in VII.1.3 proves that the printed construction carries nonzero two-torsion $P-Q$ and therefore does not split. A worthwhile extension is to impose the opposite residual contact class and then prove that the resulting incidence family dominates the double-plane family. Confidence: high for the obstruction and correction of the class; nonemptiness and dominance of the corrected family remain unproved here.

4. **The shared-component intersection problem.** The cohomological argument in VII.1.2 completes the local intersection proof for four integral half-fibres. For reducible half-fibres one must additionally exclude extra factorization branches; with shared components one must also control product divisibility. Computing these local ideals would isolate the remaining issue in this particular descent proof. It is an unresolved task within this audit, not a declaration that the modern model theorem is open.

5. **Scope of remaining uncertainty.** The exact $(-1)$-curve configuration in the type-II footnote, the two special tetrahedral degenerations, the completeness of the historical plane normal forms, and the original Franchetta and du Val arguments are not fully resolved here. Each has been isolated from the numerical assertions that can be proved. The ambiguity of several damaged scan marks is likewise retained in the corrections register. Mathematical correctness is not inferred from the editorial notes.

### VII.6. References and verified locations

Cossec, F. R., Dolgachev, I. V., & Liedtke, C. (2025). *Enriques surfaces I* (2nd ed.). Springer. https://doi.org/10.1007/978-981-96-1214-7. Publisher metadata and contents verified; relevant chapters: Generalities, pp. 199–252; Linear Systems, pp. 253–297; Projective Models, pp. 299–358. No theorem numbering from the 1989 edition is transferred to this edition.

Dolgachev, I. (1981). Algebraic surfaces with $q=p_g=0$. In *Algebraic surfaces: C.I.M.E., Cortona 1977*. Liguori. Author's scan: https://sites.lsa.umich.edu/idolga-new/wp-content/uploads/sites/1467/2024/08/cortona81.pdf. Verified locations: Chapter II, §1, local Jacobian comparison (Propositions 1–2, author-PDF pp. 24–25), canonical-divisor theorem and corollaries (author-PDF pp. 32–34). The author's publication list reports pp. 97–217, whereas the Springer reprint contents give pp. 97–215; that pagination discrepancy is left explicit. Reprint metadata: https://link.springer.com/book/10.1007/978-3-642-11087-0.

Dolgachev, I. V. (2016). A brief introduction to Enriques surfaces. In *Development of moduli theory—Kyoto 2013* (Advanced Studies in Pure Mathematics, Vol. 69, pp. 1–32). Mathematical Society of Japan. https://arxiv.org/abs/1412.7744. Author version consulted: https://sites.lsa.umich.edu/idolga-new/wp-content/uploads/sites/1467/2024/08/Kyoto13.pdf. Verified locations in that version: §2, normalization of the tetrahedral sextic; §4, dimension and moduli; §5, nodal surfaces and nef isotropic sequences. Publication metadata checked against the author's bibliography and the Mathematical Society of Japan's volume contents, https://www.mathsoc.jp/assets/pdf/publications/aspm/CFM69.pdf.

Dolgachev, I., & Kondō, S. (2024). *Enriques surfaces II* [Author draft, April 19]. https://sites.lsa.umich.edu/idolga/wp-content/uploads/sites/1334/2024/08/EnriquesTwo.pdf. The specifically verified counterexample locator is Definition 6.3.2 and Theorem 6.3.3, printed p. 29 (PDF page 43): special bisections and their existence on every nodal Enriques surface. This draft locator is distinguished from the final book.

Dolgachev, I., & Kondō, S. (2025). *Enriques surfaces II*. Springer. https://doi.org/10.1007/978-981-96-1513-1. Publisher metadata verified. Used as the current bibliographic reference for the broader automorphism and nodal-surface theory, without asserting that its theorem numbers coincide with the draft.

Enriques, F. (1949). *Le superficie algebriche*. Zanichelli. Chapter VII, pp. 237–266, supplied scans and transcription. This is the primary text audited; historical citations in §3 are attributed to this source when their originals were not independently checked.

Huybrechts, D. (2016). *Lectures on K3 surfaces*. Cambridge University Press. Author's book page/PDF: https://www.math.uni-bonn.de/people/huybrech/K3Global.pdf. The accessible prepublication copy consulted was https://ncatlab.org/nlab/files/HuybrechtsLecturesOnK3.pdf; its opening notice identifies it as a draft, so its locators are explicitly version-specific. Verified locations: Chapter 2, Corollary 2.5 (projective normality), Proposition 3.1 and Remark 3.2 (nef-big/1-connected vanishing); Chapter 6, §2 (local periods and Noether–Lefschetz), Corollary 4.4 (irreducible nineteen-dimensional polarized moduli); Chapter 17, §2 (algebraic Noether–Lefschetz examples). Publisher chapter metadata: https://www.cambridge.org/core/books/abs/lectures-on-k3-surfaces/moduli-spaces-of-polarized-k3-surfaces/1F0539571009BF3A02FB405E1372E929.

Matsuki, K. (2002). *Introduction to the Mori program*. Springer. https://doi.org/10.1007/978-1-4757-5602-9. Publisher metadata and the chapter “Birational Geometry of Surfaces,” pp. 9–108, verified. This is a general reference for the modern minimal-model and abundance framework; no unverified interior theorem number is relied on.

Saint-Donat, B. (1974). Projective models of K-3 surfaces. *American Journal of Mathematics, 96*(4), 602–639. https://doi.org/10.2307/2373709. The article's bibliographic metadata was verified through journal/DOI records and the Magma algebraic-surfaces bibliography. Its interior theorem and section locations were not independently checked; Huybrechts's inspected account supplies the working theorem references.

Schütt, M., & Shioda, T. (2010). Elliptic surfaces. In *Algebraic geometry in East Asia—Seoul 2008* (Advanced Studies in Pure Mathematics, Vol. 60, pp. 51–160). Mathematical Society of Japan. https://arxiv.org/abs/0907.0298. Author institutional metadata verified at https://www.iag.uni-hannover.de/en/forschung/publikationen/publikation-detail/publications/elliptic-surfaces. Verified locations in arXiv v3: §§3–4 for the generic fibre and singular fibres, Theorem 6.8 for the canonical bundle formula **with section**. Its section hypothesis is not suppressed in applying it.


## Chapter VIII — Regular canonical and pluricanonical surfaces (pp.267–324)

### Scope, notation, and principal conclusions

This chapter was checked against all **56 supplied scan pages** in its range, and against every corresponding TeX page. Printed pp.284–285 are missing. The text stops in the middle of a word on p.283; p.286 begins §8. Neither the missing continuation nor §7 has been reconstructed. The accompanying claim ledger records the arguments and intermediate formulas separately; a claim's classification describes **what Enriques does**, not whether the assertion is true. In particular, a false assertion can still be classified as “stated without proof” or “sketched.”

Throughout this commentary, $X$ is a smooth projective complex surface. Numerical statements about a surface of general type refer to its **minimal** smooth model unless another model is explicitly named. A nonnormal surface in projective space is first normalized and resolved. Its projective degree, its hyperplane section's arithmetic genus, the normalization's geometric genus, and the minimal surface's $K^2$ must not be conflated. On the minimal model the historical dictionary is

$$
p_g=h^0(X,K_X),\qquad q=h^1(X,\mathcal O_X),\qquad
p_a=\chi(\mathcal O_X)-1=p_g-q,\qquad p^{(1)}=K_X^2+1.
$$

Enriques's regular case is $q=0$, hence $p=p_g=p_a$. His $P$ is $P_2=h^0(2K_X)$, whereas the projective dimension of the bicanonical system is $P_2-1$. This last distinction explains several errors near the end of the chapter. A “simple” system means one whose map is birational onto its image; it does not mean smooth, base-point-free, or very ample.

Several central conclusions need substantive correction. Numerical quintics with $p_g=4,K^2=5$ need not have a birational canonical map. The $p_g=4,K^2=6$ classification is incomplete by modern standards. The assertion that $\vert 3K\vert $ is base-point-free on numerical Godeaux surfaces is false, although tricanonical birationality is true. The $p_g=1,K^2=2$ discussion omits degree-four bicanonical maps. Finally, the claimed universal tetracanonical birationality for $p_g>0$ is false for $p_g=2,K^2=1$. These are errors of mathematics, not merely uncertain transcription. Horikawa (1973), Bombieri (1973), Miyaoka (1976), Catanese (1981), Bauer et al. (2006), and Catanese and Debarre (1989) provide the primary comparisons specified below.

#### Tools used in the modern checks

Surface Riemann–Roch and adjunction give

$$
\chi(\mathcal O_X(D))=\chi(\mathcal O_X)+\frac{D(D-K_X)}2,
\qquad p_a(D)=1+\frac{D(D+K_X)}2.
$$

For a smooth minimal complex surface of general type, $K_X$ is nef and big. Vanishing applied to $mK_X=K_X+(m-1)K_X$, $m\ge2$, gives

$$
P_m=\chi(\mathcal O_X)+\frac{m(m-1)}2K_X^2,
\qquad p_a(mK_X)=1+\frac{m(m+1)}2K_X^2. \tag{VIII.1}
$$

The arithmetic-genus formula applies to the divisor class even when an individual member is singular. Identifying it with the geometric genus of a general member requires smoothness or a calculation of the singularity corrections. Standard foundations are Hartshorne (1977) and Beauville (1996); no unverified theorem numbering from those books is used here.

If a linear system is resolved by $\sigma:\widetilde X\to X$, write its pullback as a free moving divisor $M$ plus a fixed divisor. For the induced generically finite map $f$,

$$
M^2=\deg(f)\deg(f(\widetilde X)). \tag{VIII.2}
$$

A simple base point subtracts one from the moving square; in general the blow-up contributions are the squares of the successive base multiplicities. Replacing $M^2$ by $K_X^2$ without proving the absence of fixed parts and base points is a recurring source of trouble in this chapter.

For a smooth double cover $\pi:Z\to Y$, with smooth branch $B\sim2L$,

$$
\pi_*\mathcal O_Z=\mathcal O_Y\oplus L^{-1},\quad
K_Z=\pi^*(K_Y+L),\quad
\chi(\mathcal O_Z)=2\chi(\mathcal O_Y)+\tfrac12L(L+K_Y). \tag{VIII.3}
$$

For singular branch curves these formulas are applied **after canonical resolution**. Blowing up a branch point of multiplicity $m$, and writing $k=\lfloor m/2\rfloor$, changes the covering data to $L'=\beta^*L-kE$; the odd exceptional component is included in the new branch. This subtracts $k(k-1)/2$ from $\chi$ and $2(k-1)^2$ from the cover's $K^2$. Subsequent contractions of $(-1)$-curves add one each to $K^2$. Thus an ordinary quadruple point contributes $(\Delta p_g,\Delta K^2)=(1,2)$ under the usual independence assumptions, an ordinary sixfold point contributes $(3,8)$, and the standard $[3,3]$ configuration contributes $(1,1)$ **on the minimal model**, after its raw $K^2$-loss of two and one contraction. These distinctions are used explicitly below.

For an ordinary birational projection of a surface of degree $d$ to $\mathbb P^3$, with a general hyperplane section having normalization genus $g$, the degree of the ordinary double curve is

$$
\binom{d-1}{2}-g. \tag{VIII.4}
$$

This formula counts the nodes in a general plane section. It presupposes the stated generic projection and ordinary singularities; it is not a formula for arbitrary singular images.

### §1. Introduzione (pp.267–268)

The introduction distinguishes three phenomena: small geometric genus, canonical systems composed with a pencil, and canonical maps of degree greater than one. It correctly places $p_g>3$ canonical maps in $\mathbb P^{p_g-1}$, while saying that a canonical surface occurs “as a rule,” rather than claiming universal canonical birationality. The later exceptional cases show why this qualification matters. The $p^{(1)}=1$ elliptic-pencil discussion relies on the preceding classification and its hypotheses; the isolated equation $K^2=0$ would not identify the surface's Kodaira dimension.

The claim that sufficiently high pluricanonical systems give birational models is correct for surfaces of general type. In characteristic zero the modern uniform bound is $m\ge5$, with contraction of the curves on which $K$ has degree zero; this is not an assertion that the minimal smooth surface itself is embedded. Bombieri (1973) is the directly relevant primary theorem.

The Noether modifications mentioned on p.268 illustrate why $p_g$ and $K^2$ are not related by a single equality. An ordinary isolated triple point on a hypersurface surface has a blow-up exceptional plane cubic and lowers $p_g$ by one and $K^2$ by three relative to the smoothing. The quoted tacnode contribution $(1,2)$ requires the specific ordinary tacnodal type used in these constructions. Applying either rule to a singularity known only by its multiplicity would be unjustified. Independence of the imposed adjoint conditions must also be checked when several singularities are prescribed.

### §2. Quintic surfaces and their birational models (pp.268–271)

For a smooth quintic $S\subset\mathbb P^3$, adjunction gives $K_S=H$, so $p_g=4,q=0,K^2=5$. The chapter constructs three higher-degree images of this birational type: a septic with a triple conic and an external triple point; a septic with a double sextic of genus three; and a septic with a double rational quintic and a quadrisecant line. The indicated quadratic or cubic Cremona transformations explain the intended models. A modern verification must resolve their base schemes, calculate the transformed divisor class, and identify the contracted curves. Counting the degrees of equations alone does not prove birationality.

The cubic-surface plane classes in the second construction are concrete checks. On $Y=\operatorname{Bl}_6\mathbb P^2$, with $H=3h-\sum E_i$, the stated sextic class and residual twisted-cubic class are

$$
6h-3E_1-2E_2-2E_3-2E_4-2E_5-E_6,
\qquad 3h-E_2-E_3-E_4-E_5-2E_6.
$$

Their degrees and genera follow from intersection with $H$ and adjunction. Their effectiveness and lack of further fixed components depend on the prescribed point configuration. The chapter sketches the homaloidal maps rather than supplying this complete resolution calculation.

The attempted exhaustion on pp.269–270 is false. An irreducible moving canonical system with $p_g=4,K^2=5$ can have a base point and a double canonical map to a quadric. Horikawa (1973, pp.377–379) exhibits the type-II numerical quintics, in addition to the quintic type. His Theorem2 gives, locally at an ample type-IIb surface, a Kuranishi space with two forty-dimensional components meeting in dimension thirty-nine. That local statement by itself is not a proof that the global moduli space has exactly two irreducible components. The valid parameter count for smooth quintics,

$$
\dim\vert \mathcal O_{\mathbb P^3}(5)\vert -\dim\operatorname{PGL}_4=55-15=40,
$$

does not exhaust surfaces with those numerical invariants. The source's implicit divisibility argument $\deg\phi_K\mid K^2$ fails when $M^2\ne K^2$.

There is a separate local error on p.270. For $p_g=4,K^2=4$, the source says the double-quadric canonical system “therefore” has a base point. Take $Y=\mathbb P^1\times\mathbb P^1$, $L=(3,3)$, and a smooth branch curve in $\vert 2L\vert =\vert (6,6)\vert $. Then

$$
K_X=\pi^*(1,1),\quad K_X^2=4,\quad p_g(X)=h^0(Y,(1,1))=4,
$$

and $\vert K_X\vert $ is base-point-free. Its branch degree in the quadric embedding is twelve. The corresponding plane branch of degree twelve with two sixfold points has raw cover square two; the two split exceptional curves from the connecting line restore the minimal square four. This is an instructive example of why the plane and quadric computations must be compared only after minimalization.

### §3. $p_g=4, K^2=6$ (pp.271–273)

The simple sextic model has a double plane cubic. Its adjoint quadrics consist of that fixed plane plus a moving plane; the moving canonical system is therefore the hyperplane system. The alternative sextic with six ordinary triples has

$$
(p_g,K^2)=(10,24)-6(1,3)=(4,6).
$$

For the canonical double cubic, let $Y\subset\mathbb P^3$ be a smooth cubic and branch in $\vert 4H\vert $. Since $K_Y=-H$ and $L=2H$, formula (VIII.3) gives $K_X=\pi^*H$, $K_X^2=6$, $\chi=5$, and $p_g=4,q=0$. The plane branch is a degree-twelve curve with six ordinary quadruple points. Its invariants are $(10,18)-6(1,2)=(4,6)$.

The degeneration $F_3^2+\lambda F_6$ is flat as a family of hypersurfaces; the residual branch calculation $18-2\cdot3=12$ is consistent. Flatness of this embedded family does not itself prove that the smooth minimal resolutions lie in a single deformation family. A simultaneous normalization/canonical-model construction is needed for that stronger conclusion.

The double-quadric family from a decic with two $[3,3]$ points also has $(p_g,K^2)=(4,6)$, and its moving canonical square is reduced by the base points. The triple-quadric-cone example belongs to the later Pompilj discussion. Its discriminant degree eighteen is consistent with a cubic equation having coefficient degrees six and nine. The historical counts thirty-eight and thirty-nine describe construction loci; they are not by themselves proofs of component dimensions or separation.

The source's proposed three-family classification must be replaced by the modern result of Bauer, Catanese, and Pignatelli (2006): four irreducible components, eleven strata, and at most two connected components. “At most two connected components” must not be shortened to “two components”; irreducible and connected components are different notions here.

### §4. $p_g=4, K^2=7$ (pp.273–280)

The principal model is a septic whose double septic lies on a quadric cone, is hyperelliptic of geometric genus four, and passes triply through the vertex. In the cone's plane representation the initial half-class $C'_7(O^4O_1^3)$ has to be specialized to the $O^5O_1^2$ configuration. The source's reason is geometric: otherwise a ruling would meet the proposed double curve with too great a multiplicity for an irreducible septic surface. This is stronger than a bare parameter count. On the cone resolution one should express it as a fixed-component/proximity calculation.

The plane system is counted as dimension seventeen. Quotienting by the cone's seven-dimensional automorphism group gives ten parameters. The fixed-double-curve septic system is counted as dimension twenty-six, leading to thirty-six moduli. Enriques expressly calls this conclusion inductive and admits that the general moduli formula and the existence step are not rigorously established. That admission is part of the result and should not be hidden.

Franchetta's rational auxiliary septic gives a more concrete construction. In the total-transform basis of a blown-up plane put

$$
D=11h-5A-3\sum_{1}^{9}B_i-\sum_{1}^{8}D_i,
\quad T=7h-3A-2\sum_{1}^{9}B_i-\sum_{1}^{8}D_i.
$$

Direct computation gives

$$
D^2=7,\ K_YD=7,\ p_a(D)=8,\quad
T^2=-4,\ K_YT=8,\ p_a(T)=3,\quad DT=0,\quad D=2T+K_Y.
$$

The last relation explains the self-residual characteristic series; $T$ is the curve intended to contract to the quadruple point. What remains to prove is that the indicated system defines the asserted birational map, is free away from the prescribed locus, and has precisely the stated image singularities. These conclusions do not follow from intersection numbers alone.

The count $19-(6+3)=10$ is compatible with the ten-parameter curve family. It does not prove that **every** such curve occurs. A dominant parameter map would establish only a dense open family; extending to all members requires properness, control of limiting base schemes, and a flat construction. The later degeneration $3a+C_2+C'_2$ likewise needs its Hilbert polynomial and embedded structure. The source's nine-condition argument is a sketch of such a degeneration, not a complete proof of membership in the desired Hilbert-scheme component. The special septic system has the stated count $31+2=33$, and adding a cross ratio gives thirty-four, compatible with codimension two in the proposed principal family.

The exponent in the spatial hyperelliptic-curve count on p.276 appears as $28$ in the scan, whereas the TeX reads $26$. The latter is mathematically correct on the complete nonspecial $g^3_7$ locus: seven hyperelliptic moduli, four Picard parameters, and fifteen projective coordinates give $7+4+15=26$. The ledger distinguishes a diplomatic transcription from a mathematical emendation.

The one-base-point canonical case gives a sextic with a double conic and a specified tacnode. For its fixed rational line $a^2=-\nu$,

$$
(2a)^2=-4\nu,\quad p_a(2a)=-\nu-1,
\quad \bar p^{(2)}=10-4\nu,\quad \bar p^{(1)}=8-\nu.
$$

The canonical identity $\bar p^{(2)}=\bar p^{(1)}-1$ gives $10-4\nu=7-\nu$, hence $\nu=1$. This is a valid posterior calculation of the exceptional line once the preceding resolved intersection data are accepted. It explains the difference between relative and absolute linear genus, and the moving square $7-1=6$. The auxiliary quintics have the claimed thirty-seven parameters, the sextics thirty-eight, and the stabilizer subtraction gives thirty-five. These are not the forty moduli of canonical quintic surfaces from §2.

The double-cubic alternative is represented by a degree-twelve branch with five quadruple points and one $[3,3]$ point, giving $(4,7)$. Its canonical moving square six agrees with a double cubic and one simple base point. The further double-quadric construction has moving square four, hence total base contribution three, and the source counts thirty-three moduli. Its incidence expression $AA_1D$ conflicts with the stated placement of $B$ on the branch line; $AA_1B$ is a proposed emendation, not an alternative scan reading. The author's uncertainty about family inclusion and the unexamined fixed-component possibilities must remain explicit. No modern exhaustive classification of this entire range is claimed in this fragment.

### §5. $p_g=4, K^2=8$ (pp.281–283)

The octic model has a double $C_{12}$ of geometric genus ten on a four-nodal cubic, and four ordinary triple points. The plane half-class is represented by the stated nonic with three infinitely near pairs $P^4P_1,Q^4Q_1,R^4R_1$. Its degree and genus can be checked on the resolved cubic. The existence of a half divisor is a Picard-group condition, not a consequence of its even spatial degree.

The curve system is counted as dimension twenty-one and the fixed-curve octics as dimension thirteen, using a residual quintic count twelve. This yields thirty-four moduli only after dominance and the expected generic fiber have been justified. The print's $F_9$ at the relevant restriction step is impossible: a cubic meets it in degree twenty-seven, whereas twice $C_{12}$ has degree twenty-four. The required degree is eight.

The rational auxiliary construction uses

$$
D=11h-3\sum_{1}^{12}A_i-\sum_{1}^{5}B_i,
\quad T=7h-2\sum_{1}^{12}A_i-\sum_{1}^{5}B_i.
$$

It gives $D^2=8,p_a(D)=9,T^2=-4,p_a(T)=3,DT=0,D=2T+K_Y$. Again these establish the numerical self-residual geometry, not automatically the claimed image singularity. The seventeen-moduli construction and the assertion that a quadruple point imposes seventeen conditions are not fully demonstrated; the latter is presented tentatively in the text.

The double-quartic alternative, whose quotient has genus-two hyperplane sections, is represented by a branch of degree fourteen with one sixfold and eight quadruple points. The invariant calculation is

$$
(p_g,K^2)=(15,32)-(3,8)-8(1,2)=(4,8).
$$

The count $119-19-64-8=28$ assumes independent moving-singularity conditions. The inequality $28<30$ cannot prove inclusion in a particular other family. A double cubic with branch degree sixteen is represented by a degree-twelve curve with four quadruple and two $[3,3]$ points; its two canonical base points account for moving square six. Its stated thirty-two-moduli count and family relationship remain construction-level assertions.

### §§6–7 and the missing bridge (p.283; pp.284–285 absent)

The supplied beginning of §6 proposes a canonical nonic for $p_g=4,K^2=9$, involving a quartic with ten nodes and a half-class related to $9H-3\sum E_i$. The indispensable missing work is to verify divisibility in the Picard group, effectiveness, the required singularities, and the dimension/dominance statements. The expected expression $50-2n$ does not establish those facts. The text breaks off at “Questa cir-”. No wording, title, conclusion, or proof has been supplied for the missing continuation or §7.

What p.286 does establish, independently, is the start of a new case $p_g=5,K^2=9$, a sextic construction, and the $(3,3)$ complete-intersection family. It cannot be used to reconstruct the missing argument about the previous numerical case.

### §8. $p_g=5$, including $K^2=9,10$ (pp.286–289)

A sextic with five ordinary triple points has $(p_g,K^2)=(5,9)$. Quadrics through the five points give the classical map to a ten-nodal cubic threefold in $\mathbb P^4$, with the ten joining lines contracted. The transformed sextic belongs to the canonical $(3,3)$ family. For a smooth complete intersection, adjunction proves $K=H$; its parameter count is

$$
\dim\operatorname{Gr}(2,35)-\dim\operatorname{PGL}_5=66-24=42.
$$

The source's numerical argument uses $P_3=6+27=33$, while ambient cubics form a vector space of dimension thirty-five. Thus the restriction map has a kernel of dimension **at least two**, regardless of surjectivity. One equation is the known irreducible Segre cubic. A second independent cubic has no three-dimensional common component with it. Their complete intersection has degree nine and contains the irreducible degree-nine image, hence equals that image as the intended pure complete intersection. This repairs the argument without assuming projective normality. The conclusion is established for the constructed birational degree-nine image; it is not an exhaustion of every surface with these numerical invariants, whose canonical map may have different behavior.

The projected nonic has general-section genus ten and double-curve degree $28-10=18$. Its adjoint quartic has six nodes on a trope conic. On the K3 resolution,

$$
D_{16}=4H-\sum_1^6E_i,\quad D_{16}^2=52,\quad p_a(D_{16})=27.
$$

For the trope $C$, $C^2=-2,D_{16}C=2$, so $(D_{16}+C)^2=54$ and its arithmetic genus is twenty-eight. The equality of system dimension and arithmetic genus uses the nef and big condition and vanishing. It is false for arbitrary base-point-free K3 systems: a multiple of an elliptic pencil has arithmetic genus one and arbitrarily large system dimension. The half-class and trope relations are integral lattice data, which cannot be inferred merely from even degree.

The equation $x+14=42$ gives $x=28$ only after the construction dominates the claimed family and has that generic fiber. It cannot independently prove that every half curve admits a surface. The one-base-point octic and double-quartic cases with $p_g=5,K^2=9$ are consistent with moving square eight; the plane double model has four quadruple and one $[3,3]$ singularity in a degree-twelve branch. The stated forty-one-dimensional count is not a proof of its relation to the forty-two-dimensional family.

For $p_g=5,K^2=10$, the degree-twelve branch with three quadruple and two $[3,3]$ points gives the correct invariants. Its canonical moving square eight and degree-two map to a quartic leave total base contribution two. The printed branch degree eighteen on that quartic is wrong. A general canonical curve has genus eleven and covers a genus-two quotient curve twice, so Hurwitz gives

$$
20=2\cdot2+r,\qquad r=16.
$$

The scan securely reads $18$. The sextic with four triples and a tacnode also gives $(5,10)$. Equal forty-dimensional counts do not prove two separate components; the source itself speaks tentatively.

### §9. Threefold Jacobians, adjunction, and residual surfaces (pp.289–292)

For a smooth threefold $V$, a suitably free four-dimensional vector space of sections of $D$ gives a map to $\mathbb P^3$. Its differential determinant has divisor class $K_V+4D$. This yields the source's identities

$$
J(D)=K_V+4D,\quad J(D+E)=J(D)+4E,\quad D'=K_V+D.
$$

The determinant construction requires either a morphism or a resolution with all base contributions retained. For a smooth divisor $S$, the adjunction exact sequence gives $K_S=(K_V+S)\vert _S$. A converse assertion about a divisor on $V$ from its restriction to $S$ needs an injectivity theorem for Picard groups and, for complete systems, a cohomological surjectivity argument.

For a smooth hypersurface threefold $V_n\subset\mathbb P^4$, $K_V=(n-5)H$, and hyperplane adjoints have degree $n-4$. On singular varieties these are dualizing-sheaf formulas, not canonical-class formulas on a resolution without discrepancies. The listed multiplicities $i-1,i-2,i-3$ along ordinary surface, curve, and point loci encode the corresponding ordinary blow-up corrections. They must not be applied to arbitrary singularities having the same multiplicity.

If $S\in\vert K_V\vert $ and two canonical divisors meet smoothly in a curve $C$, put $y=K_V^3$ and $x=p_a(C)$. Then $K_C=3K_V\vert _C$, hence $x=1+3y/2$. Also $K_S=2K_V\vert _S$, so $K_S^2=4y$. Consequently

$$
2x+y-1=4y+1=p^{(1)}(S).
$$

These formulas are valid in their smooth/effective setting; the historical threefold “genera” listed here do not exhaust the modern Hodge and Chern invariants.

For a smooth complete-intersection surface of degrees $n_1,\dots,n_{r-2}$ in $\mathbb P^r$,

$$
K_X=\bigl(\sum n_i-r-1\bigr)H.
$$

The residual-surface versions require scheme-theoretic linkage and the appropriate Cohen–Macaulay/conductor duality, not just an equality of underlying sets. Both flagged residual indices on pp.291–292 read Greek $\alpha$.

### §10. Canonical complete intersections and threefold sections (pp.292–294)

For a nondegenerate canonical complete intersection with no linear equations,

$$
\sum n_i=r+2,\quad n_i\ge2,\quad 2(r-2)\le r+2,
$$

so $r\le6$. The list, with its smoothness assumptions, is:

| Type | Ambient space | $p_g$ | $K^2$ |
|---|---:|---:|---:|
| $5$ | $\mathbb P^3$ | 4 | 5 |
| $2,4$ | $\mathbb P^4$ | 5 | 8 |
| $3,3$ | $\mathbb P^4$ | 5 | 9 |
| $2,2,3$ | $\mathbb P^5$ | 6 | 12 |
| $2,2,2,2$ | $\mathbb P^6$ | 7 | 16 |

These are verified by adjunction and the product of degrees. They are not a classification of all canonical surfaces in those spaces.

The two more general constructions become precise when the ambient canonical class is specified. On an index-two threefold $V_n\subset\mathbb P^{n+1}$ with $K_V=-2H$, a smooth cubic section has $K_X=H$, $p_g=n+2$, and $K^2=3p_g-6$. The printed $n=p-1$ in the concluding first item must be $n=p-2$. On an index-one threefold of degree $2r-4$ in $\mathbb P^r$, $K_V=-H$, a quadric section gives $K^2=4p_g-12$. Completeness of the hyperplane restriction is required for the asserted $p_g$. The rationality claim for the first ambient family has the printed restriction $n>3$; it is not a claim about cubic threefolds. Cone examples require separate vertex/discrepancy treatment. The historical Fano, Godeaux, Bourniat and Maxwell citations are recorded as citations, without invented modern theorem attributions.

### §11. Noether and Castelnuovo bounds (pp.294–299)

#### A modern proof of the Noether inequality

Let $X$ be smooth, minimal, and of general type, with $q=0$. If the moving canonical system has two-dimensional image, resolve its base points and write $\sigma^*K_X=M+Z$, with $M$ free and $Z\ge0$. A general $C\in\vert M\vert $ is smooth and irreducible. Regularity and

$$
0\to\mathcal O_{\widetilde X}\to\mathcal O_{\widetilde X}(M)
\to\mathcal O_C(M)\to0
$$

give $h^0(\mathcal O_C(M))=p_g-1$. The series is special because its Serre-dual series is the restriction of $K_{\widetilde X}$, which has a nonzero effective representative not containing $C$. Clifford therefore gives $M^2\ge2(p_g-2)$. Since $\sigma^*K_X$ is nef, $M$ is nef and $Z\ge0$,

$$
K_X^2-M^2=Z\cdot\sigma^*K_X+Z\cdot M\ge0.
$$

Thus $K_X^2\ge2p_g-4$.

If the canonical system is composed with a pencil, its base curve is $\mathbb P^1$: a map to a positive-genus curve would contradict $q=0$. Write the moving part on $X$ as $aF$, $a=p_g-1$, and $K_X=aF+Z$. The moving pencil divisor $F$ is nef. If $F^2=0$, its general fiber has genus at least two, so

$$
K_X^2\ge aK_XF=2a(g(F)-1)\ge2p_g-2.
$$

If $F^2\ge1$, then $K_XF\ge aF^2$, hence $K_X^2\ge a^2F^2\ge(p_g-1)^2\ge2p_g-4$. The cases $p_g\le1$ are immediate from $K^2>0$. This treats the genus-two pencil omitted from the source's displayed $\pi\ge3$ argument. The source's reversed Clifford inequality and later $2p+1$ are slips. The positive base-point contribution is correct, but its displayed count is called $s$ after being introduced as $r$.

The equality case can also be justified under these regular, minimal, general-type hypotheses. If $p_g\ge3$ and $K_X^2=2p_g-4$, the pencil estimate above excludes a one-dimensional canonical image. In the two-dimensional case equality throughout gives $M^2=K_X^2$, $Z\cdot M=Z\cdot\sigma^*K_X=0$, and hence $Z^2=0$. The Hodge index theorem, since $M^2>0$, forces $Z$ numerically trivial; effectiveness then forces $Z=0$. Thus there are no canonical fixed parts or base points. For $p_g\ge4$, the Castelnuovo bound proved below excludes canonical birationality, since $3p_g-7>2p_g-4$; for $p_g=3$, a birational canonical map to $\mathbb P^2$ would make the surface rational. A nondegenerate surface in $\mathbb P^{p_g-1}$ has degree at least $p_g-2$. The degree formula $2(p_g-2)=\deg(\phi_K)\deg(\phi_K(X))$ now forces a double map onto a surface of minimal degree. Clifford equality on a smooth canonical member gives its hyperellipticity. This proves the stated canonical-map conclusion without claiming the detailed singular branch classification. The scan's ambient $S_{p-2}$ confuses degree and projective dimension; it must be $\mathbb P^{p_g-1}$.

The double-plane examples are numerically checkable. A smooth octic gives $(3,2)$, and a smooth decic gives $(6,8)$, not the printed $p_g=7$. For a branch of degree $2n+6$ with an ordinary $2n$-fold point, the invariants are $p_g=2n+1,K^2=4n-2,p^{(1)}=4n-1$. Adding a sixfold point gives raw $K^2=4n-10$, then two split $(-1)$-curve contractions give minimal $K^2=4n-8$, hence $p^{(1)}=4n-7$. Adding instead a quadruple point gives $p_g=2n,K^2=4n-4,p^{(1)}=4n-3$. The book repeatedly prints $K^2$ in place of $K^2+1$.

#### The birational canonical bound and its equality constructions

The Castelnuovo bound is $K^2\ge3p_g-7$ for a birational canonical map. It can be proved without assuming the canonical system free on the original surface. Use the same resolution $\sigma^*K_X=M+Z$ as in the Noether proof. A smooth general $C\in\vert M\vert $ has $n=M^2$ and a complete birational $g^r_n$ cut by $M$, with $r=p_g-2$. Completeness follows from $q=0$; birationality follows from that of the resolved canonical map on a general member. Write $K_{\widetilde X}=M+Z+E$, where the discrepancy divisor $E$ is effective. Since $M$ is nef,

$$
g(C)=1+\frac{M^2+K_{\widetilde X}M}{2}\ge n+1.
$$

Castelnuovo's genus bound for a nondegenerate birational degree-$n$ curve in $\mathbb P^r$ gives a maximal genus strictly less than $n+1$ when $n\le3r-2$. Thus $n\ge3r-1$, and $K_X^2\ge M^2$ yields $K_X^2\ge3p_g-7$. For $r=1$, a birational pencil forces a rational curve, contrary to $g(C)\ge n+1$; the relevant nondegenerate canonical cases have $r\ge2$. This supplies the fixed-part and base-point estimates as well as the curve argument.

The source's alternative proof chooses two divisors meeting in $r-1$ general points and estimates the canonical conditions imposed by their union as $2n-3r+1$. The elementary final inequality is correct; existence/general position of those divisors and the dependence count are the substantive steps. The modern curve genus bound avoids that informal incidence calculation.

The quintic and $(2,4)$ examples attain equality. For the scroll construction let $V=\mathbb P(E)\to\mathbb P^1$ be a suitable smooth rank-three scroll with $\deg E=p_g-3$, $H=\mathcal O_V(1)$, and ruling-plane class $F$. Then

$$
K_V=-3H+(p_g-5)F,\quad D=4H-(p_g-5)F,
\quad K_D=H\vert _D,
$$

and

$$
H^2D=4(p_g-3)-(p_g-5)=3p_g-7.
$$

Effectivity, smoothness of a general $D$, and complete hyperplane restrictions must be checked for the chosen splitting type. The ambient space is $\mathbb P^{p_g-1}$, not the printed $\mathbb P^{p_g-7}$. The spatial model's degree $2p-3$, $(p-4)$-fold line, triple generators, and residual adjoints of degree $p-3=(2p-7)-(p-4)$ are model-specific projection data, requiring ordinary projection hypotheses.

### §12. Upper bounds and moduli counts (p.299)

The Rosenblatt inequality $p^{(1)}\le16p_a+27$ is a historical citation to the 1912 paper, whose proof has not been independently checked here. The following Hodge-theoretic bound has a direct modern verification. Since

$$
c_2=12\chi-K^2,\quad b_2=c_2-2+4q,\quad h^{1,1}=b_2-2p_g,
$$

one gets $h^{1,1}=2p_g+8p_a+10-K^2$. The inequality $\rho\le h^{1,1}$ therefore gives exactly

$$
p^{(1)}\le2p_g+8p_a+11-\rho.
$$

The historical expression $M=10p-2p^{(1)}+12+\omega$ has the modern deformation-theoretic baseline $10\chi-2K^2$. Indeed Hirzebruch–Riemann–Roch gives $\chi(T_X)=2K^2-10\chi(\mathcal O_X)$, and a minimal general-type surface has no infinitesimal automorphisms, so the local Kuranishi dimension is at least $h^1(T_X)-h^2(T_X)=10\chi-2K^2$. The obstruction map, generic smoothness, and automorphism quotient cannot be replaced by a universal numerical “correction” $\omega$. A construction of smaller dimension may be a proper sublocus without being contained in the particular family named by the source.

### §13. Canonical multiple covers and trigonal systems (pp.300–303)

For a double cover of a rational surface, the splitting $\pi_*\omega_X=\omega_Y\oplus\omega_Y(L)$ proves that all canonical sections come from the second summand, because $p_g(Y)=0$. Their ratios are invariant under the deck involution. The canonical map factors through the quotient. This gives a clean sheaf-theoretic explanation of the chapter's double-plane examples.

The converse numerical criterion is false: $K^2<3p_g-7$ obstructs birationality, but the reverse inequality does not imply it. For a smooth double plane with branch degree $2n$, $p_g=(n-1)(n-2)/2$, $K^2=2(n-3)^2$, and their ratio tends to four, while the canonical map still factors through the involution.

The twenty-node quintic construction needs an even node set. On its resolution, require $2L=\sum_{1}^{20}E_i$. Then $L^2=-10,K_YL=0,K_Y^2=5,\chi(Y)=5$, so the double cover has $\chi=5$ and raw $K^2=2(5-10)=-10$. The twenty ramification $(-1)$-curves yield minimal $K^2=10$. The asserted $p_g=4$ additionally uses $q=0$. Neither twenty nodes alone nor a formal double degeneration establishes these hypotheses.

For the degree-eighteen double plane with eight sixfold points, the correct calculation is

$$
(p_g,K^2)=(28,72)-8(3,8)=(4,8),\quad p^{(1)}=9,
$$

not the printed eleven. The more specialized sextic and oscillating-node constructions depend on their local analytic types; they cannot be checked by multiplicity alone.

The triple-cover equations have the form $z^3+3p_{2d}z+q_{3d}=0$, with discriminant proportional to $4p_{2d}^3+q_{3d}^2$. For $d=2,3,4$ the discriminant degrees are twelve, eighteen, and twenty-four. The third displayed equation on p.303 omits the factor $z$ in its middle term; degree balance and the printed discriminant both require it. The infinitely near coefficient multiplicities are part of the construction and must satisfy proximity; an arbitrary discriminant of the correct degree does not define the desired cover.

The trigonal-theta argument constructs a plane curve of degree $m=n+3$, with an $n$-fold point and a triple point. Its intended contradiction is that removing two fixed lines from an adjoint leaves degree $m-5$ with multiplicity $m-4$ at the other point. This is impossible once the asserted fixed-line and birational plane-model conditions hold. Those geometric conditions are the unproved part of the sketch. The attribution to Pompilj is retained, but no independently verified theorem number or exhaustive statement beyond the printed hypotheses is invented.

### §14. $K^2=1, p_g=2$ (pp.303–305)

Formula (VIII.1) gives $P_2=4,P_3=6$. A canonical member has genus two, and the pencil has one simple base point in the standard canonical model. On a smooth canonical member $C$, adjunction gives $2K_X\vert _C=K_C$; the degree-one divisor at the base point is therefore a Weierstrass point. The bicanonical sections give a double quadric cone, with branch degree ten and special behavior at its vertex. Treating that vertex as an ordinary branch point on a smooth surface would be wrong. One may resolve the cone, or work directly with the following canonical ring.

#### Explicit modern model and proof

Take a general quasismooth hypersurface

$$
X=\{w^2=f_{10}(x,y,z)\}\subset\mathbb P(1,1,2,5).
$$

Choose nonzero $z^5,w^2$ coefficients and a sufficiently general $f_{10}$, so that the hypersurface is smooth in the ambient smooth locus and avoids the isolated quotient-singular points. Weighted adjunction gives $K_X=\mathcal O_X(1)$, and the intersection calculation gives

$$
K_X^2=\frac{10}{1\cdot1\cdot2\cdot5}=1,
\qquad p_g=2,\quad H^0(K_X)=\langle x,y\rangle.
$$

The hypersurface cohomology/graded-ring computation gives $q=0$. The bicanonical sections $x^2,xy,y^2,z$ satisfy the one quadric relation between their first three entries and define the double cover of the cone. The point $x=y=0$ on $X$ is one point after the weighted equivalence; in the chart $z\ne0$, the two choices of the nonzero square root $w$ are exchanged by the residual sign action. Since the stabilizer is trivial there, $x,y$ are local coordinates. Thus the canonical pencil has exactly one simple base point.

This model proves the asserted numerical/bicanonical geometry and will disprove the final tetracanonical claim. It is an explicit audit calculation, while the general exceptional-case theorem is Bombieri (1973, Main Theorem, p.173). The plane decic with a $[5,5]$ point is a birational plane description; its parity resolution is more complicated than subtracting two ordinary quintuple-point corrections. The end of §14 prints $p=1$ where its model and preceding discussion require $p=2$.

The fixed-component argument says that the moving genus-two pencil and its adjoint recover this same canonical model. That assertion should be made on the canonical model, or with a separate analysis of fixed $(-2)$-curves on a smooth resolution. Nefness only gives $K\theta\ge0$; it does not imply that every $K$-trivial curve is absent.

### §15. $K^2=1, p_g=1$ (pp.305–308)

Here $P_2=3,P_3=5$. The unique canonical divisor has arithmetic genus two; Enriques first assumes it irreducible. A bicanonical member has square four and arithmetic genus four. The complete characteristic series on such a member has projective dimension one, since regularity gives

$$
h^0(\mathcal O_C(C))=h^0(2K)-1=2.
$$

The source uses this completeness to exclude a particular hyperelliptic composite system. The restriction of $\vert 3K\vert $ to $C\in\vert 2K\vert $ is the canonical system of $C$. To infer global birationality one must also separate different bicanonical members and control fixed/base parts; the nonhyperellipticity of one curve alone is not a global separation theorem. The relevant result is included in Bombieri's pluricanonical analysis.

The tricanonical numerical data are projective dimension four, moving degree nine if free, and curve genus seven. The described image $F_9\subset\mathbb P^4$ has a triple line corresponding to the canonical curve; projection from a point of that line gives degree $9-3=6$. The resulting sextic has three coplanar cuspidal double lines, a special singularity at their intersection, general plane-section genus seven, and plane-through-the-point section genus four. The chapter's explicit cubic-surface contact construction is a real construction sketch, but its local analytic singularity type and normalization must be checked before all its adjoint counts become a proof. The historical “contact of order five / settipunto” terminology has not been silently translated into a modern local equation; that identification remains unverified.

The unique adjoint quadric, the adjoint-cubic dimension seven, and $P_2=3$ are intended to give $p_g=1,q=0,K^2=1$. The last implication is numerically sound once regularity is established: $P_2=\chi+K^2=2+K^2$. The source's $F_3+F'_2$ must read $F_3+F'_3$ in the cubic construction.

For $\vert 2K\vert =Z+\vert M\vert $, with $M^2=n,p_a(M)=\pi$, the displayed calculations are

$$
K M=2\pi-2-n\le2,
\qquad MZ=4\pi-4-3n\ge2.
$$

The final lower bound uses a two-connectedness input, stronger than simple connectedness, which is assumed from the earlier theory. Together with the separate $n>1$ premise these imply $n\le2$, hence $n=2,\pi\le3$. The remaining claimed double-octic identification and its $K^2=0$ contradiction require the omitted branch-resolution argument. The inequalities themselves are valid under the stated hypotheses; the classification step is not fully proved on the supplied page.

### §16. $K^2=1, p_g=0$: numerical Godeaux surfaces (pp.308–311)

The numerical formula gives $P_2=2,P_3=4$. The chapter's universal tricanonical nonic and its asserted absence of base points are false. When the tricanonical system is free and birational, the claimed degree nine, section genus seven, and double-curve degree $28-7=21$ are correct. They are conditional model data, not universal invariants of numerical Godeaux surfaces.

Miyaoka (1976) proves tricanonical birationality and describes the base points in terms of torsion. The primary indexed text of p.106, Theorem 2 and its reformulation, gives the number as half the number of torsion classes $t\ne-t$. Thus the cyclic torsion cases of orders one or two have zero base points, orders three or four have one, and order five has two. The resulting tricanonical degrees are nine, eight, and seven. Catanese's author-hosted exposition (1981, §V, especially the base-point propositions) gives a directly accessible treatment. Reid's canonical-ring paper (1978) is another primary source for the explicit models.

The precise defect in the source's base-point argument is a quantifier change. A **general** bicanonical member may be irreducible and smooth; the **special** member through a tricanonical base point need not be. Catanese's description uses a reducible member $D_t+D_{-t}$, with the base point at its transverse intersection for $t\ne-t$. Restricting the tricanonical system to that special member as though it were a smooth genus-four curve invalidates the argument. The claim does not become valid by citing the general member's irreducibility.

#### Audit example A: a complete degree-seven counterexample

Let

$$
Y=\{x_1^5+x_2^5+x_3^5+x_4^5=0\}\subset\mathbb P^3,
$$

and let $G=\mu_5$ act by weights $1,2,3,4$. Every nonidentity group element has four distinct eigenspaces, so its projective fixed points are the coordinate points. None lies on $Y$. The quotient $X=Y/G$ is therefore smooth and the cover is étale. Since $K_Y^2=5$, $K_X^2=1$. The canonical sections have the four nontrivial characters; hence $p_g(X)=0$, while $q(X)=0$ follows from $q(Y)=0$. Equivalently $\chi(Y)=5$ and étale multiplicativity gives $\chi(X)=1$.

The invariant quadrics are

$$
x_1x_4,\qquad x_2x_3.
$$

For a general nonzero parameter their linear combination is a smooth quadric. Its intersection with the quintic is smooth by Bertini off the fixed base locus, and at each base point the quadric differential has a nonzero component transverse to the coordinate line containing the point. On the quadric the curve has class $(5,5)$, hence is ample and connected; a smooth connected curve is irreducible. Its étale quotient is a smooth irreducible general bicanonical member of $X$. The counterexample therefore satisfies the source's hypothesis.

The invariant cubics are exactly

$$
s_0=x_1^2x_3,\quad s_1=x_1x_2^2,
\quad s_2=x_2x_4^2,\quad s_3=x_3^2x_4.
$$

Their common zeros on $Y$ are the intersections with the two coordinate lines $\langle x_1,x_4\rangle$ and $\langle x_2,x_3\rangle$. Each contains five points on the Fermat quintic, forming one free $G$-orbit. Thus $\vert 3K_X\vert $ has two base points. They are simple: on the first line two of the displayed sections have independent linear terms in $x_2,x_3$, and on the second they have independent linear terms in $x_1,x_4$.

Birationality of the quotient map can also be checked explicitly. On $x_1=1$, write $u=x_2,v=x_3,w=x_4$. The image ratios are

$$
r=\frac{u^2}{v},\quad s=\frac{uw^2}{v},\quad t=vw,
\qquad u^5=\frac{t^2r^3}{s},\quad v=\frac{u^2}{r},\quad w=\frac{tr}{u^2}.
$$

The five choices of $u$ are exactly one $G$-orbit. The map is therefore generically one-to-one on $X$. After blowing up the two simple base points its moving square is $9-2=7$, so the tricanonical image is a septic in $\mathbb P^3$. This computation is the audit's own derivation, not a result falsely attributed to Enriques or Reid.

The Campedelli double plane invoked on p.308 has branch degree ten, one ordinary quadruple point, and five $[3,3]$ points. The intended calculation $(6,8)-(1,2)-5(1,1)=(0,1)$ is conditional: canonical forms are adjoint conics through the six proper singular points, so $p_g=0$ requires that those points lie on no conic. This condition is absent from the supplied paragraph. Moreover, obtaining the stated smooth minimal model requires controlling further exceptional curves. The suitable quartic adjoint system being exactly a pencil is an explicit sufficient hypothesis in Werner (1994, §2, Proposition 1).

The historical existence input also needs correction. Bombieri (1973, §13, p.218) says that Campedelli's analogous $K^2=1,p_g=0$ construction is not correct. Dolgachev (1981, Chapter III, §2, Proposition 3 and the later Remark, author-PDF pp.62–63 and75–76) identifies the obstruction in the proposed three-conic-plus-quartic configuration: it would produce two independent order-two classes, forbidden on a numerical Godeaux surface. Enriques invokes the example without reproducing that configuration. This failure does not make the numerical branch type impossible.

A verified later existence repair is Werner's octic-plus-conic example (1994, §§2–4). Her construction satisfies the required branch and adjoint conditions and has free $\vert 3K\vert $. Combining that fact with Miyaoka's birationality theorem gives a tricanonical nonic: $(3K)^2=9$ and $P_3=4$. Thus a nonic of the desired kind does exist, but neither this example nor the numerical branch count proves Enriques's universal nonic assertion. The historical count $65-8-45-8=4$ remains an unverified parameter count, below the deformation baseline eight; Werner does not establish it. The historical terminology here concerns numerical Godeaux surfaces; modern “numerical Campedelli” means $K^2=2,p_g=q=0$.

The remainder of §§16's argument conditionally excludes a triple map to a cubic. On a smooth cubic it uses complementary twisted-cubic classes summing to $2H$, their genus-four pullbacks, self-residual $g^1_3$'s, and a doubled-system dimension comparison. The calculations make sense within the stated cover model, but the completeness and uniqueness steps need additional cohomological proof. The singular cubic case similarly requires resolving the target and its branch. These conditional arguments do not repair the false preliminary freeness assertion. Miyaoka's theorem supplies the true birationality conclusion. The final “bicanoniche” on p.311 is a local slip for “tricanoniche.”

### §17. $K^2=2, p_g=3$ (pp.311–312)

Noether's inequality gives $p_g\le3$ when $K^2=2$; the next sections divide the regular surfaces into $p_g=3,2,1,0$. For $p_g=3$ the standard model is a double plane branched in an octic. Formula (VIII.3) gives $K=\pi^*O(1)$, $K^2=2,p_g=3,q=0$, and $P_2=6$.

The fixed-part calculation writes $K=M+Z$, $M^2=n,p_a(M)=\pi$, and uses

$$
KM=2\pi-2-n,\quad MZ=2\pi-2-2n\ge0,\quad KZ\ge0.
$$

In the case analyzed, $n\ge2$ forces $n=2,\pi=3,KZ=0$. This does not on its own prove $Z=0$ on the smooth minimal surface: $K$-trivial $(-2)$-curves can exist. The canonical model contracts them. The global double-octic classification is part of Noether-line theory, rather than a consequence of these inequalities alone.

### §18. $K^2=2, p_g=2$ (pp.312–316)

Here $P_2=5$. Restricting $\vert 2K\vert $ to a smooth canonical member $C$ gives its complete canonical $g^2_4$: in

$$
0\to\mathcal O_X(K)\to\mathcal O_X(2K)\to\omega_C\to0,
$$

surjectivity follows from $H^1(K)=q=0$. Products of the two canonical sections separate different canonical-pencil parameters. Consequently the behavior on a general member distinguishes the nonhyperelliptic birational bicanonical case from the hyperelliptic double case, provided the fixed/base-part hypotheses have been established.

In the first case the bicanonical image is an octic in $\mathbb P^4$, with section genus seven. The plane canonical quartics lie in the ruling planes of a rank-three quadric threefold with vertex line. The projected octic in $\mathbb P^3$ has the stated infinitely near quadruple lines and double conic. Although the degree-eight image is cut by a quadric and a quartic, its normalization is not a smooth $(2,4)$ complete intersection: the latter would have $p_g=5,K^2=8$, and section genus nine. The conductor singularities account for the drop to seven. The polynomial ansatz and adjoint factors on p.313 must be interpreted on that normalization.

Two numerical examples are particularly transparent. A degree-twelve double plane with eight ordinary quadruple points has $(p_g,K^2)=(2,2)$; the canonical pencil is represented by cubics through the eight points. The pullback subsystem used for the bicanonical map has only four sections, whereas the full system has five. The double-cover splitting supplies the extra section. Confusing that incomplete subsystem with the complete bicanonical system would give the wrong degree.

For the K3 example, on the resolved quartic require

$$
2L=H+\sum_{1}^{6}E_i.
$$

Then $L^2=-2,\chi=3,K^2_{\rm raw}=-4$; contracting six ramification $(-1)$-curves gives $K^2=2$. The trope configuration gives the asserted $h^0(L)=1$, so $p_g=2,q=0$. The integrality and section count are genuine geometric hypotheses, not automatic for six arbitrary nodes.

In the hyperelliptic case the bicanonical image is the appropriate nodal degree-four del Pezzo surface, an intersection of two quadrics in $\mathbb P^4$. A general hyperplane section has genus one, and its double pullback genus seven; Hurwitz gives branch degree twelve **on this quartic**. Its plane representation instead has a decic branch with two quadruple and two $[3,3]$ points. These two degrees must not be confused, as happens in the summary on p.322.

The moduli assertion $24=9p-2p^{(1)}+12$ is untenable as a dimension of complete components. At $(p_g,K^2)=(2,2)$, the local lower bound is

$$
10\chi-2K^2=30-4=26.
$$

The source's own earlier formula used $10p$, not $9p$. Equal construction dimensions would not prove that the two loci are separate components in any event. The described common special locus needs a deformation argument. This audit does not substitute an unverified modern classification for that missing proof.

There is another original numerical error in the fixed-part exclusion on p.316. For $(\pi,n)=(2,1)$, adjunction gives $KM=1$. Therefore

$$
(K+M)^2=2+2+1=5,\qquad
p_a(K+M)=1+\frac{(K+M)(2K+M)}2=5,
$$

whereas the source states degree seven and genus four. The case has a short independent exclusion: with $Z=K-M$, one obtains $MZ=0,M^2=1,Z^2=1$, contradicting the Hodge index theorem. This is an audit repair. For the $(2,0)$ case the source uses a complete adjoint system of dimension three and degree six to obtain a double cubic scroll; the contradiction requires proving that pullback of the linearly normal scroll polarization would yield at least five sections. That completeness input must be supplied, not merely asserted. The conclusion should again distinguish the canonical model from a smooth resolution carrying $(-2)$-curves.

### §19. $K^2=2, p_g=1$ (pp.316–321)

The bicanonical system has four sections. If it is free and birational, its image is an octic in $\mathbb P^3$, with section genus seven and ordinary double-curve degree fourteen. The contact geometry involves an adjoint quartic and a seventh-degree surface, with an equation of the form

$$
F_8=\Phi_4^2+\alpha\Phi_7.
$$

The intersection of $F_8$ and $\Phi_7$ has degree fifty-six, so the “complete intersection” description of $C_{14}$ must be understood with multiplicity $4C_{14}$, not as a reduced complete intersection of degree fourteen. The claimed sixteen-moduli count is consistent with, but is not itself a proof of, the component constructed rigorously later.

#### A major omitted case: bicanonical degree four

Catanese and Debarre (1989, pp.1–3) explicitly identify Enriques's exclusion of degree four as an error. They list five cases which all occur: degree four to a quadric cone; degree four to a smooth quadric; degree two to a rational quartic; degree two to a K3 quartic; and birational degree eight. The torsion-$\mathbb Z/2$ case is an irreducible rational sixteen-dimensional family and has degree-four cone image. The degree-four smooth-quadric locus is an eleven-dimensional unirational family of simply connected surfaces. Thus even the possible degrees in the chapter are not exhaustive.

**Audit example B: an explicit degree-four map with irreducible canonical curve.** On $Y=\mathbb P^1\times\mathbb P^1$, choose smooth transverse branch divisors of types

$$
D_1=(1,1),\quad D_2=(3,1),\quad D_3=(1,3),
$$

with no triple intersection, and form the standard smooth bidouble cover with three distinct nonzero inertia characters. Its character line bundles are

$$
L_1=(2,2),\quad L_2=(1,2),\quad L_3=(2,1),
\qquad 2L_i=D_j+D_k.
$$

The cover algebra is $\mathcal O_Y\oplus L_1^{-1}\oplus L_2^{-1}\oplus L_3^{-1}$. Therefore

$$
p_g=\sum h^0(K_Y+L_i)=1,
\quad \chi=4+\tfrac12\sum L_i(L_i+K_Y)=2,
\quad q=0.
$$

The ramification formula gives $2K_X=\pi^*O_Y(1,1)$, so $K_X^2=2$. All four bicanonical sections come from $H^0(Y,O(1,1))$; the other three summands have no sections. The bicanonical map is consequently the degree-four cover followed by the Segre embedding. The unique canonical divisor is the reduced ramification divisor over $D_1$. It is a connected double cover of $D_1\cong\mathbb P^1$, branched at its eight transverse intersections with $D_2+D_3$, and has genus three. Thus it is smooth and irreducible for general branch curves. The counterexample satisfies the source's irreducible-canonical-curve assumption. This computation is our explicit verification of the branch types listed by Catanese and Debarre, not an attribution of the derivation to the 1949 text.

#### The degree-two loci and the limits of the old inclusion argument

For the K3 quartic case, require $2L=H+\sum_{1}^{10}E_i$. Then

$$
L^2=-4,\quad\chi=2,\quad K^2_{\rm raw}=-8,
\quad K^2_{\rm minimal}=-8+10=2.
$$

The printed “quartic of genus two” on p.318 is a slip for **surface geometric genus one**. Its smooth hyperplane section has genus three; these are different uses of “genus.” The square-root expression $\sqrt{\alpha\Phi_7}$, and its reduction to a degree-four radicand $\sqrt{\alpha F_3}$, require the actual contact-divisor identity in the K3 function field.

For

$$
D_{14}=\frac{7H-\sum_{1}^{10}E_i}{2},
$$

one has $D_{14}^2=44,p_a=23$; subtracting $H$ gives square twenty and genus eleven, and subtracting $2H$ gives square four and genus three. The restrictions of degrees fourteen and ten to a plane quartic of genus three have respectively twelve and eight sections by curve Riemann–Roch. Surjectivity of the surface restriction maps still requires vanishing or a direct proof; numerical genus alone does not imply it. The complementary contact sextics satisfy $C_6+C'_6=3H$, $C_6C'_6=14$. The source's residual four points and ten node conditions are compatible with these identities.

The parameter count $34-10+3-15=12$ is confirmed for the appropriate K3-quartic family by Catanese and Debarre, while the degree-two rational-quartic family has dimension thirteen and the plane branch decic with one quadruple and four $[3,3]$ points. Its invariants are $(6,8)-(1,2)-4(1,1)=(1,2)$. The source's inequalities $12<15$ and $13<15$ do not identify an ambient component. Catanese and Debarre prove that these loci, together with the degree-four smooth-quadric locus, belong to a sixteen-dimensional component $\mathcal M_E$. Their paper explicitly leaves **irreducibility of the entire torsion-zero moduli space as a conjecture**; it would be inaccurate to quote them as proving it. Enriques also explicitly leaves the reducible-canonical-divisor case unexamined.

### §20. $K^2=2, p_g=0$: numerical Campedelli surfaces (p.321)

Here $P_2=3,P_3=7$. Thus the bicanonical map, when free, has degree eight to $\mathbb P^2$, while the tricanonical map takes values in $\mathbb P^6$. The book prints $S_7$, confusing seven sections with projective dimension. The tricanonical curve genus is

$$
p_a(3K)=1+6K^2=13,
$$

not the printed $6p^{(1)}-2=16$. Accordingly a generic ordinary spatial projection of its degree-eighteen birational image has double-curve degree

$$
\binom{17}{2}-13=123,
$$

not 120. All three errors are present in the scan.

The proposed double decic with six $[3,3]$ points gives $(p_g,K^2)=(0,2)$ on the intended general locus. Its existence is cited rather than proved. The count $65-54-8=3$ is a construction count below the deformation lower bound $10-4=6$.

The curve argument also prints the wrong characteristic-series dimension. For $C\in\vert 2K\vert $, regularity gives $h^0(O_C(C))=P_2-1=2$, so the complete characteristic series is $g^1_8$, not $g^2_8$. The hyperelliptic contradiction is repairable **if this complete special series is also base-point-free**: on a hyperelliptic curve, such a series is a multiple of the hyperelliptic pencil; degree eight would make it $4g^1_2$, with five sections, contradicting two. Irreducibility of the general bicanonical member alone does not establish that freeness hypothesis. Catanese (1981, §IV, Theorem 2, pp.258–259; author-PDF pp.11–12) gives the actual theorem that the tricanonical map of a numerical Campedelli surface is birational; his argument includes the required base-point-free setting. This is a modern repair of the theorem, not a retrospective validation of the abbreviated source proof.

### §21. Exceptional tricanonical maps and the false tetracanonical conclusion (pp.321–324)

The summary recalls the double octic $(K^2,p_g)=(2,3)$, the decic $[5,5]$ case $(1,2)$, and the decic with two quadruple and two $[3,3]$ points $(2,2)$. In the last item the printed plane branch $C_{12}$ must be $C_{10}$, as both pp.314–315 and formula (VIII.3) show. This is distinct from the correct degree-twelve branch **on** the bicanonical quartic image.

The reduction to plane systems of lines, conics, and degree-$n$ curves with an $(n-1)$-point uses a classical classification of rational linear systems. The source's count $2n-s$ follows from subtracting the multiplicity and simple-point conditions from plane curves, provided the conditions are independent and the infinitely near cluster is admissible. The local formulas $2m=n+d+6$, multiplicity $2m-5$, and second-adjoint deficit lead to

$$
2(2m-5)\le2m,\quad m\le5.
$$

The connecting line must not already be a branch component, and the claimed infinitely near multiplicity requires a proximity argument. Positivity/general type excludes the smaller values in the stated case, leaving four and five. This is a useful outline of the special double-plane cases, not a complete substitute for Bombieri's global theorem with fixed and exceptional divisors.

For the double octic, $K=\pi^*O(1)$ and all tricanonical sections are pullbacks of plane cubics. Thus $P_3=10$ and the image is the degree-nine Veronese plane in $\mathbb P^9$, with elliptic hyperplane sections. This part is correct.

For $(K^2,p_g)=(1,2)$, however, the source's “sextic in $S_6$ with elliptic sections” is wrong in degree, ambient dimension, and sectional genus. In the weighted model of §14, the complete tricanonical basis is

$$
x^3,x^2y,xy^2,y^3,xz,yz.
$$

Hence the target is $\mathbb P^5$. There is one simple base point at $x=y=0$, so the moving square is eight. The map still has degree two, and its image is the rational normal scroll $S(1,3)$, of degree four, isomorphic to the Hirzebruch surface $\mathbb F_2$. A general hyperplane section is rational. A general tricanonical curve on $X$ is smooth at the simple base point and has genus seven, so it is hyperelliptic. Bombieri (1973, Main Theorem, p.173(iii)(a)) explicitly gives this exception.

#### The tetracanonical counterexample and the correct uniform bound

The canonical ring of the same $X_{10}\subset\mathbb P(1,1,2,5)$ is generated by $x,y,z,w$ in degrees $1,1,2,5$, with one relation in degree ten. For degree four its sections are exactly the five binary quartics in $x,y$, the three products of $z$ with binary quadratics, and $z^2$: nine sections in total. None involves $w$. The map therefore still factors through $w\mapsto-w$, has degree two, and has degree-eight image in $\mathbb P^8$. This is the cone described in Bombieri's exceptional-case statement, with the degree-four polarization of the weighted quotient. A statement that it is literally a degree-two quadric in $\mathbb P^8$ would confuse the underlying cone with its higher embedding.

At degree five the new generator $w$ appears. The sections $x^5,x^4y,x^3z,w$, on $x\ne0$, recover $y/x,z/x^2,w/x^5$, so $\vert 5K\vert $ is birational for this model. Thus the source's premise “tricanonical curves are never hyperelliptic” and its conclusion “$\vert 4K\vert $ is always simple for regular $p_g>0$” both fail. The separate $p_g=0$ assertion is explicitly conjectural in Enriques; its eventual proof requires a different argument.

The correct uniform statement is that $\vert mK_X\vert $ gives a birational map for all $m\ge5$ on smooth minimal complex surfaces of general type, with the appropriate contraction of $K$-trivial curves. Bombieri's theorem is the primary reference. A shorter modern proof of birationality uses Reider's adjoint criterion (Reider, 1988), in the formulation verified in Peters (n.d., Theorem 7.2, p.18; pluricanonical application, §8, p.19). Set $L=(m-1)K_X$, so $L$ is nef and $L^2\ge16$. For $L^2\ge10$, failure to separate points would produce an effective divisor $D$ with $LD=0$ and $D^2=-1$ or $-2$; $LD=1$ and $D^2=-1$ or $0$; or $LD=2$ and $D^2=0$. The values $LD=1,2$ are impossible because $LD$ is divisible by $m-1\ge4$. If $LD=0$, each component of $D$ is $K_X$-trivial and belongs to the exceptional locus of the canonical contraction. General pairs of points avoid this locus. The base-point version, valid for $L^2\ge5$, would require $LD=0,D^2=-1$ or $LD=1,D^2=0$. The former contradicts the evenness of $D(D+K_X)$, and the latter the same divisibility. Thus $\vert mK_X\vert $ is free and separates general points; it is birational. This proof uses smoothness, characteristic zero, nefness and bigness. It does not assert very ampleness on a minimal resolution containing $(-2)$-curves.

#### The $p_g=0$ conjecture is true in modern theory

For a smooth minimal complex surface of general type with $p_g=q=0$, the complete system $\vert 4K\vert $ is birational. Bombieri's Main Theorem deals with $K^2\ge2$; the remaining numerical Godeaux case $K^2=1$ is proved by Catanese (1981, §III, Theorem 1, p.254, proof pp.254–255; author-PDF pp.7–8). His statement gives injectivity on a nonempty Zariski open subset, which in characteristic zero yields birationality. This resolves the conjecture at the end of p.324 positively. It neither follows from, nor rescues, the preceding false assertion for $p_g>0$. The distinction is substantive: the weighted $(K^2,p_g)=(1,2)$ counterexample has a double tetracanonical map, while every regular surface of general type with $p_g=0$ has a birational one.

### Audit conclusions, extensions, and confidence

**High confidence, source and calculation agree:** the complete-intersection invariants; the explicit Noether inequality repair; the double-cover numerical checks; the p.286 kernel-and-Bézout argument; the Godeaux quotient and bidouble-cover counterexamples; and the weighted $(1,2)$ exceptional pluricanonical model. These are reproducible intersection, cohomology, and section-ring calculations.

**High confidence, directly verified primary repairs:** Horikawa's missing numerical quintics; the four-component $K^2=6,p_g=4$ analysis of Bauer et al.; Bombieri's exceptional tricanonical/tetracanonical case; Catanese and Debarre's five bicanonical cases and their stated moduli results; Catanese's numerical Campedelli tricanonical theorem; and his numerical Godeaux tetracanonical theorem. The historical Campedelli existence input is corrected using the distinct obstruction and later construction identified above. Miyaoka's base-point statement was checked through indexed primary text at p.106 when direct retrieval of the linked PDF failed; Catanese's accessible exposition provides an additional direct check. The original Bombieri–Catanese 1978 contribution is bibliographically verified, but its broken download link was not treated as a read of its proof.

**Explicitly unverified:** a complete modern local analytic verification of every projected sextic/septic singularity; dominance and all-special-member surjectivity of the Franchetta-type constructions; the full deformation classification of the $K^2=7,8,9,10$ ranges discussed; the paper-by-paper claims in the historical Fano/Godeaux/Bourniat/Maxwell/Pompilj bibliography; and the absent pp.284–285. Imperatives such as “compute the conductor” in the CSV identify the work needed for a complete repair; they do not assert that such a computation was completed. These are limits of this audit, not allegations that every classical assertion is false.

**Own extension C, high confidence:** the three examples A, B, and the weighted model form a useful sequence for testing historical linear-system arguments. They distinguish (i) irreducibility of a general member from freeness; (ii) completeness of a full system from a chosen subsystem; and (iii) the degree of a map from the self-intersection before resolving its base points. Their explicit section bases make the distinctions checkable without relying on classification terminology.

**Own research question, no claim of current open status:** for each half-curve construction on a nodal quartic, determine the exact lattice-polarized K3 locus where the half class is integral, nef, and effective, and then compute the incidence morphism to the canonical-surface moduli space. This would replace several “same dimension, therefore every curve” passages by precise statements about image, fibers, and boundary. The necessary lattice and degeneration analysis was not completed here; no claim is made that the corresponding questions remain open in current research.

### References used for Chapter VIII

Bauer, I., Catanese, F., & Pignatelli, R. (2006). The moduli space of surfaces with $K^2=6$ and $p_g=4$. *Mathematische Annalen, 336*(2), 421–438. [Author-hosted primary paper](https://pignatelli.maths.unitn.it/papers/k26pg4.pdf). The introduction and principal moduli statement were checked; four irreducible components and eleven strata are not inferred from a secondary summary.

Beauville, A. (1996). *Complex algebraic surfaces* (2nd ed.). Cambridge University Press. https://doi.org/10.1017/CBO9780511623936. [Official publisher record](https://www.cambridge.org/core/books/complex-algebraic-surfaces/E242F9DDB71DFB9B060ED6311400B5FA). Used for standard complex-surface foundations; publisher metadata verified, no unverified theorem numbers supplied.

Bombieri, E. (1973). Canonical models of surfaces of general type. *Publications Mathématiques de l'IHÉS, 42*, 171–219. https://doi.org/10.1007/BF02685880. [Official article](https://numdam.org/articles/10.1007/BF02685880/); [primary PDF](https://www.numdam.org/item/PMIHES_1973__42__171_0.pdf). Main Theorem, especially p.173(iii)(a), checked for the $(K^2,p_g)=(1,2)$ exception; §13, p.218 checked for the historical Campedelli construction caveat.

Bombieri, E., & Catanese, F. (1978). The tricanonical map of a surface with $K^2=2, p_g=0$. In *C. P. Ramanujam—A tribute* (Tata Institute of Fundamental Research Studies in Mathematics, Vol. 8, pp.279–290). Tata Institute of Fundamental Research. [Author's official publication list](https://www.mathe8.uni-bayreuth.de/en/team/prof-fabrizio-catanese/pdf/index.html). Bibliography verified; the original linked download was unavailable. The accessible Catanese exposition below is the proof source actually used.

Catanese, F. (1981). Pluricanonical mappings of surfaces with $K^2=1,2, q=p_g=0$. In G. Tomassini (Ed.), *Algebraic surfaces: C.I.M.E. 1977* (pp.247–266). Liguori. [Author-hosted primary scan](https://www.mathe8.uni-bayreuth.de/de/team/prof-fabrizio-catanese-old/pdf/006.pdf). Reprinted in *C.I.M.E. Summer Schools*, Vol.76, Springer; [official reprint contents](https://link.springer.com/book/10.1007/978-3-642-11087-0). Original publication details also verified in the author's [Lincei bibliography](https://www.lincei.it/sites/default/files/2024-08/459_bibl.pdf). §III, Theorem 1, pp.254–255 (author-PDF pp.7–8), §IV, Theorem 2, pp.258–259 (author-PDF pp.11–12), and §V's base-point analysis are the relevant passages; the reprint's catalog year differs across online and copyright records, so the original1981 date is used.

Catanese, F., & Debarre, O. (1989). Surfaces with $K^2=2, p_g=1, q=0$. *Journal für die reine und angewandte Mathematik, 395*, 1–55. [Author-hosted primary scan](https://www.mathe8.uni-bayreuth.de/de/team/prof-fabrizio-catanese-old/pdf/032.pdf). Title page and pp.1–3 inspected directly. Those pages explicitly discuss Enriques pp.316–321, list all five occurring bicanonical cases, give the quoted dimensions, identify the component $\mathcal M_E$, and retain full torsion-zero irreducibility as a conjecture.

Dolgachev, I. (1981). Algebraic surfaces with $q=p_g=0$. In *Algebraic surfaces: C.I.M.E., Cortona 1977*. Liguori. [Author's scan](https://sites.lsa.umich.edu/idolga-new/wp-content/uploads/sites/1467/2024/08/cortona81.pdf). Chapter III, §2, Proposition 3, author-PDF pp.62–63, and Remark, pp.75–76, verify the torsion obstruction used here. The author's publication list gives pp.97–217, whereas the [Springer reprint contents](https://link.springer.com/book/10.1007/978-3-642-11087-0) give pp.97–215; the discrepancy is retained rather than silently resolved.

Enriques, F. (1949). *Le superficie algebriche*. Zanichelli. Chapter VIII, pp.267–324, as supplied; pp.284–285 unavailable. The supplied scans, rather than the AI transcription or its editorial annotations, were the primary textual authority.

Hartshorne, R. (1977). *Algebraic geometry*. Springer. https://doi.org/10.1007/978-1-4757-3849-0. [Official publisher record](https://link.springer.com/book/10.1007/978-1-4757-3849-0). Used for standard adjunction, intersection, Riemann–Roch and cohomological foundations; no unsupported theorem numbering.

Horikawa, E. (1973). On deformations of quintic surfaces. *Proceedings of the Japan Academy, 49*(6), 377–379. https://doi.org/10.3792/pja/1195519286. [Primary PDF](https://www.jstage.jst.go.jp/article/pjab1945/49/6/49_6_377/_pdf). Direct comparison for the omitted numerical-quintic type and the local Kuranishi statement at ample typeIIb; global exact component counting is not inferred from this short paper.

Miyaoka, Y. (1976). Tricanonical maps of numerical Godeaux surfaces. *Inventiones Mathematicae, 34*, 99–111. https://doi.org/10.1007/BF01425477. [Indexed primary PDF endpoint](https://www.digizeitschriften.de/download/pdf/356556735_0034/log12.pdf). The endpoint failed direct retrieval in this audit, but indexed primary passages for Theorem3 and Theorem2/2′ on p.106 were verified. This access limitation is not concealed.

Reid, M. (1978). Surfaces with $p_g=0, K^2=1$. *Journal of the Faculty of Science, University of Tokyo, Section IA, 25*(1), 75–92. [Author's reprint](https://mreid.warwick.ac.uk/Reprint/pg0K21.pdf). §1 canonical-ring treatment checked in the coordinated audit. The explicit Fermat quotient calculation above is labeled as our derivation.

Peters, C. A. M. (n.d.). *Compact complex surfaces* [Author-hosted conference text; cover identifies the Canadian Mathematical Society Summer Meeting, June 1990]. https://cpeters1.win.tue.nl/ConfsAndSchools/Canada/surface.pdf. Theorem 7.2, p.18 gives the Reider criteria used above; §8, p.19 applies them to pluricanonical systems. The event date is verified, but it is not represented as a verified publication year.

Reider, I. (1988). Vector bundles of rank 2 and linear systems on algebraic surfaces. *Annals of Mathematics, 127*(2), 309–316. https://doi.org/10.2307/2007055. [Official journal record](https://annals.math.princeton.edu/1988/127-2/p04). Bibliographic metadata verified there; the exact criterion used in the proof is checked in Peters's authored formulation cited above.

Werner, C. (1994). A surface of general type with $p_g=q=0$, $K^2=1$. *Manuscripta Mathematica, 84*, 327–341. https://doi.org/10.1007/BF02567460. [Primary author preprint](https://arxiv.org/html/alg-geom/9408007v1). §2, Proposition 1, and §§3–4 were checked; the computer algebra calculations are reported by the paper, not independently rerun here.


## Chapter IX audit: irregular surfaces, continuous systems, and Picard varieties (pp. 325–369)

### IX.0. Scope, conventions, and the logical distinction that controls the chapter

The default modern setting of this audit is a smooth, connected, projective surface $X$ over $\mathbb C$. A singular projective model in Enriques's examples is replaced by a smooth model, and assigned multiple points are incorporated by blowing up when intersection numbers or characteristic systems require this. Neither the analytic arguments with periods nor the equality between the numerical irregularity and the dimension of the Picard variety are statements in arbitrary characteristic. Printed page references below are to the supplied scan, not to PDF page numbers. The separate corrections register distinguishes the printed reading, a transcription error, an original mathematical misprint, and an unverified reconstruction.

The chapter's principal valid conclusion is
$$
q=h^1(X,\mathcal O_X)=p_g-p_a=\dim\operatorname{Pic}^0(X).
$$
There is a complete algebraic family of sufficiently positive effective divisors whose linear-equivalence classes fill a $q$-dimensional Picard component. This theorem does **not** assert that every effective divisor belongs to such a dominant family with complete characteristic system. The chapter itself eventually exposes precisely that stronger assertion's failure, especially in §§7–8.

Three distinct smoothness/completeness questions must therefore be kept separate.

1. The Picard scheme parametrizes line bundles. Its tangent space at the identity is $H^1(\mathcal O_X)$; in characteristic zero its identity component is smooth.
2. The divisor scheme parametrizes effective Cartier divisors together with their sections up to scalar. At $C$, its tangent space is $H^0(C,\mathcal O_C(C))$, and it can be singular or nonreduced even when the Picard variety is smooth.
3. A chosen classical family has a characteristic linear series given by the image of its tangent space in $H^0(\mathcal O_C(C))$. Completeness requires surjectivity of this characteristic map. A tangent vector is not automatically the derivative of an actual curve in that chosen reduced family.

This is the modern formulation of the gap recognized on pp.331–333. The revisers' footnote on p.333 expressly says that the following argument was left incomplete and contains many lacunae. The audit does not retrospectively attribute a finished algebraic proof to that passage. Kleiman's historical and scheme-theoretic accounts distinguish the original theorem, overextended completeness assertions, and later rigorous approaches (Kleiman, 2005, §5, especially Remark 5.18; Kleiman, 2013).

#### Notation dictionary and exact sequence

For a smooth effective irreducible curve $C\subset X$, put $L=\mathcal O_X(C)$, $N=\mathcal O_C(C)$, $n=C^2$, and $\pi=p_a(C)$. Enriques's index of speciality is $i=h^2(X,L)=h^0(X,K_X-C)$, his superabundance is $\omega=h^1(X,L)$, and the complete linear-system dimension is $r=h^0(X,L)-1$. Surface Riemann–Roch and adjunction give
$$
\chi(L)=\chi(\mathcal O_X)+\frac{C(C-K_X)}2
       =p_a+n-\pi+2,\qquad
r=p_a+n-\pi+1-i+\omega.
$$
Here $p_a=\chi(\mathcal O_X)-1$, and is allowed to be negative. It is not the genus of a curve.

The sequence
$$
0\longrightarrow\mathcal O_X\longrightarrow L\longrightarrow N\longrightarrow0
\tag{IX.1}
$$
gives the exact tangent sequence
$$
0\longrightarrow H^0(L)/\mathbb C
\longrightarrow H^0(N)
\overset{\partial}{\longrightarrow}H^1(\mathcal O_X)
\overset{s}{\longrightarrow}H^1(L).
\tag{IX.2}
$$
Thus the deficiency of the characteristic series cut by the complete linear system is
$$
\delta=h^0(N)-r
       =\dim\ker s
       =q-\operatorname{rank}s,\qquad 0\leq\delta\leq q.
\tag{IX.3}
$$
The projective characteristic series cut by $\vert C\vert $ has dimension $r-1$, whereas the complete normal series has dimension $h^0(N)-1$. The subtraction of one is essential throughout the dimension counts. For a family $T$ of dimension $R$, an injective characteristic map at a general point gives a series of dimension $R-1$. In characteristic zero one may take a reduced, generically immersive parameter space; inseparability makes this automatic identification unavailable in characteristic $p$.

### IX.1. §§1–3, pp.325–328: the numerical bound, effectivity, and the Picard quotient

#### What is established from the earlier theory

On a regular surface $q=0$, (IX.2) says that the characteristic series of a complete linear system is complete. More generally, a family containing complete linear systems of general dimension $r$, with $d$ parameters of distinct linear-equivalence classes, has dimension $r+d$. Its characteristic series has dimension $r+d-1$, provided the tangent map has the expected rank. Castelnuovo's deficiency bound then gives $d\leq q$. The argument is sound for the stated general smooth members and separable families; it is not a proof that an arbitrary divisor scheme is smooth.

The passage from reducible curves to irreducible residual curves uses a sufficiently positive auxiliary system. Modernly, if the original divisors form a bounded algebraic family, one chooses a high tensor power of an ample line bundle uniformly over its parameter space. Relative Serre vanishing and relative generation provide residual systems, and Bertini gives smooth irreducible general residual members. This is the missing explicit quantifier behind “sufficiently high order.” It is a useful reduction, not a claim that all individual residual members are irreducible.

Enriques distinguishes the numerical quantity $p_g-p_a$ from a geometric maximum of the number of parameters of inequivalent complete systems. Over $\mathbb C$, the latter is $\dim\operatorname{Pic}^0$. The fundamental theorem identifies the two. The birational invariance used in changing projective models is correct for smooth surfaces: $h^1(\mathcal O)$, $h^2(\mathcal O)$, and hence $\chi(\mathcal O)$, are unchanged by point blowups.

#### The arithmetic effectivity criterion on p.327

The displayed inequality is
$$
p_a+n-\pi+1-i\geq0,
\quad\text{equivalently}\quad
\chi(L)-h^2(L)\geq1.
\tag{IX.4}
$$
It has a clean proof **at the level of effective line-bundle classes**. For $\alpha\in\operatorname{Pic}^0(X)$, the Euler characteristic $\chi(L\otimes\alpha)$ is constant. Upper semicontinuity gives $h^2(L\otimes\alpha)\leq h^2(L)$ in a neighborhood of the origin. Consequently
$$
h^0(L\otimes\alpha)
=\chi(L)+h^1(L\otimes\alpha)-h^2(L\otimes\alpha)
\geq\chi(L)-h^2(L)\geq1.
$$
Thus a neighborhood of the original class consists of effective classes. The image of the relevant proper divisor parameter space in the Picard component is closed; an image containing an open subset of the irreducible Picard variety contains the whole component. Equivalently, effective twists exist in every class after taking the closure of the dominant family.

There is no defect in interpreting the theorem as a series of complete linear systems or effective classes. A separate question is whether a prescribed section $s\in H^0(L)$, and hence its particular divisor, extends along such a family. If $h^0$ jumps at the original class, many sections need not extend. Section §8 recognizes this explicitly for canonical divisors. The audit does not insert this stronger conclusion into §2 merely to manufacture an error.

#### What a modern construction supplies

Choose an ample $H$ sufficiently positive that
$$
H^j(X,H\otimes\alpha)=0\quad(j>0,\ \alpha\in\operatorname{Pic}^0(X)).
$$
Uniformity follows by relative Serre vanishing for the Poincaré line bundle on $X\times\operatorname{Pic}^0(X)$. Its direct image $E$ after tensoring with $H$ is locally free, of rank $\chi(H)$. The projective bundle $\mathbb P(E)$ parametrizes all effective divisors in these classes and has dimension $\chi(H)-1+q$. Its characteristic map at a smooth divisor is the full tangent space $H^0(N)$. This constructs the desired complete continuous system and proves the numerical/geometric equality once the Picard scheme and characteristic-zero smoothness have been established. It does not use the unproved all-order construction of §5.

On p.328, the quotient by linear equivalence is a Picard component $\operatorname{Pic}^L$, a torsor under $\operatorname{Pic}^0$. Choosing $L$ as origin identifies the torsor with the group. Taking the residual with respect to a fixed large divisor corresponds to $M\mapsto H\otimes M^{-1}$, hence to inversion followed by translation. The operation is algebraic on the Picard scheme. The original discussion anticipates this structure, but existence, representability, and properness are substantive theorems, not consequences of set-theoretic quotienting alone.

Nor is the image of every continuous curve family an abelian variety. For example, on $X=B\times\mathbb P^1$ with $g(B)>1$, the fiber family is parametrized by $B$, whose image in $\operatorname{Pic}^1(B)$ is a curve rather than a group. Sums of independently varying members may generate a larger abelian subvariety. Merely multiplying every class by a fixed integer does not increase image dimension. This distinction clarifies the language about multiples on p.328. **This example and interpretation are audit extensions; confidence: high.**

### IX.2. §4, pp.329–330: the $p_g=0$ argument

For $p_g=0$, write $p_a=-p$. Take regular nonspecial systems $\vert C\vert $, $\vert D\vert $, with invariants $(n,\pi,r)$, $(\nu,\rho,r')$, and transverse intersection number $m$. Then
$$
r=-p+n-\pi+1,\qquad r'=-p+\nu-\rho+1.
$$
For the sum $E=C+D$,
$$
N=n+\nu+2m,\qquad
\Pi=\pi+\rho+m-1,
$$
and hence
$$
R=\dim\vert E\vert =-p+N-\Pi+1=r+r'+p+m.
\tag{IX.5}
$$
Near an ordinary transverse union, requiring $m$ unspecified nodes imposes at most $m$ conditions. The connectedness argument rules out an irreducible $m$-nodal curve specializing, with exactly those $m$ persistent nodes, to the disjoint normalization $C\sqcup D$. A modern proof simultaneously normalizes the persistent nodes after appropriate base change: proper connected fibers cannot acquire a disconnected special normalization in such an equinodal family. Thus the relevant equinodal component stays split. Its dimension is at least $R-m=r+r'+p$, giving at least $p$ parameters of linear-equivalence classes after allowing the linear motions of the two summands. Combined with the upper bound $d\leq p_g-p_a=p$, this gives equality.

The argument needs the transverse nodal setup, an actual flat family, and a normalization/connectedness theorem. It is a geometric sketch with a valid modern completion; it is not the unrestricted assertion that imposing nodes always gives independent conditions. On p.330 the scan prints $q\geq-p$, although $p=-p_a>0$. The argument proves $q\geq p$. This is an original sign misprint, not a questionable transcription.

There is an especially short independent modern proof in this case. If $C$ is sufficiently ample, $H^1(L)=H^2(L)=0$, and (IX.1) gives $H^1(N)=0$ because $H^2(\mathcal O_X)=0$. The divisor scheme is therefore smooth at $C$; (IX.2) gives tangent dimension $r+q$. In addition, $H^2(\mathcal O_X)=0$ kills the obstruction space for the Picard functor, so the Picard scheme is smooth even in positive characteristic. This special argument is stronger in characteristic than the general complex-period proof (Kleiman, 2005, Proposition 5.19).

The last paragraph's lower bound for arbitrary $p_g$ with $p_a<0$ is only $q_{\mathrm{geo}}\geq-p_a$. It is not the full equality $q_{\mathrm{geo}}=p_g-p_a$.

### IX.3. §5, pp.330–338: first-order splitting, integration, and the unfinished proof

#### The first-order calculation and its precise limitation

For general $p_g$, the sum-system count becomes
$$
R=r+r'+m-p_a.
$$
To produce $q=p_g-p_a$ additional class parameters by splitting, the desired codimension is $m-p_g$, rather than $m$. The curves through the intersection group $G=C_0\cap D_0$ supply infinitesimal splitting directions. In modern terms this is information in a tangent or normal space. Enriques correctly stops on p.331 to distinguish differential existence from integral existence.

A local calculation shows why. At a node $xy=0$, a first-order deformation
$$
xy+t(ax+by)
$$
is first-order equivalent to a split product. But
$$
(x+tb)(y+ta)=xy+t(ax+by)+t^2ab,
$$
so the original deformation has a second-order smoothing term unless an additional correction is made. First-order factorization does not imply persistence of a node to all orders. Likewise, the scheme $y^2=0$ has a larger tangent space than the dimension of its reduced support. Tangent excess is not evidence of a missing reduced family.

The desired tower $C_1,C_2,\ldots$ on p.332 must consist of **compatible** lifts through all infinitesimal thickenings. Constructing a second-order neighbor for some choice at each stage does not by itself establish compatibility, unobstructedness, convergence, or algebraization. A convergent analytic Lie flow does integrate a tangent vector on an already constructed smooth abelian variety. It cannot establish the smoothness and existence of that variety by assuming the group on which it is to flow.

#### The branched-cover construction, pp.333–335

Projecting a suitably embedded curve to a line gives the familiar branch count
$$
b=2N+2\Pi-2.
$$
For a nodal union $C+D$, the counts from $C$ and $D$, together with two branch points for each of the $m$ nodes after smoothing, add correctly:
$$
(2n+2\pi-2)+(2\nu+2\rho-2)+2m
=2(n+\nu)+2(\pi+\rho+m-1)-2.
$$
An ordinary branch point has transposition monodromy; the pair coalescing at an apparent node has product the identity. The existence theorem for branched covers allows one to separate such branch points and construct nearby abstract covers. With a sufficiently positive embedding and the necessary deformation theory, this also supplies an ambient spatial picture.

It does **not** show that the deformed curve remains on the fixed surface $X$. Nor does the branch count prove that every first-order section of its normal sheaf on $X$ integrates. The distinction between ambient deformations and deformations constrained to $X$ is the principal missing bridge. The claimed dimensions $R$ and $R-m$ require unobstructed ambient deformations and a surjective map to the chosen node-smoothing parameters, hypotheses that the Riemann-existence discussion alone does not establish. The printed $r=p+n-\pi+1$ on p.335 also drops the subscript $a$, an independent typographical error.

#### A concrete degree error in the auxiliary-curve construction

The difficulty on pp.335–337 is not only a vague complaint about rigor. Let the auxiliary curve $L$ have genus $P$, let $M=C\cdot L$, and let the restricted complete series $\vert C\vert _L$ have dimension $r>0$, as in the text. Choose an imposed divisor $A$ of degree $r$ that makes $C_0$ unique.

If one adds $S$ of degree $P-M$ to the **whole** divisor $C_0\cap L$, the result $G$ has degree $P$. However,
$$
h^0(L,\mathcal O_L(G))
\geq h^0(L,\mathcal O_L(C_0))=r+1>1.
$$
Riemann–Roch on $L$ says that a nonspecial degree-$P$ divisor has exactly one section. Therefore this $G$ cannot be nonspecial as claimed. If one first removes the $r$ imposed points $A$, the residual divisor has degree $M-r$, and a degree-$P$ completion requires
$$
\deg S=P-M+r,
$$
not $P-M$. The text alternates between referring to the removed group and counting the full intersection, and later changes the added group's letter. The scan confirms those readings. A corrected bookkeeping convention can remove this particular contradiction, but does not prove the subsequent transversality or integrability claims. **Confidence: high for the inconsistency; no claim is made to have reconstructed the author's intended full proof.**

#### Independence, nodal auxiliary curves, and descent

The assertion that speciality of $G$ and of its infinitesimally adjacent $G_1$ imposes two independent conditions requires a transversality statement. Two nearby equations may have the same differential; first-order adjacency is precisely a situation in which their dependence needs analysis. Dimension subtraction alone is insufficient. If the auxiliary curve degenerates to a nodal curve, one must work with its arithmetic genus and dualizing sheaf, or normalize and impose the appropriate gluing condition at the two preimages of the node. These requirements cannot be replaced by counting free points on the normalization.

The pencils $C_0+D_0+\lambda E$ appearing on p.337 usually have irreducible general members. Their infinitesimal splitting does not provide an actual factorization of the pencil. Finally, §5 acknowledges possible exchange of the two components under monodromy. To obtain a well-defined algebraic locus $G''$, one must establish descent through that monodromy, independence from the auxiliary $D$, constant degree, and compatibility with the proposed iteration. These are not supplied.

The displayed addition rule in the p.338 footnote is valid as **linear equivalence of divisors**. On a Picard torsor, the proposed parallelogram construction becomes $[G'']=2[G']-[G]$. This clarifies the geometric idea but does not establish the existence of every effective representative invoked in the argument.

#### Rigorous replacement and the role of semiregularity

For $H^1(L)=H^2(L)=0$, the projective-bundle construction in IX.1 supplies a full replacement of the chapter's fundamental theorem. More generally, the semiregularity homomorphism is
$$
\sigma:H^1(C,N)\longrightarrow H^2(X,\mathcal O_X).
$$
A divisor is semiregular when this map is injective. By (IX.1), this is equivalent to the surjectivity of $H^1(\mathcal O_X)\to H^1(L)$. The semiregularity theorem gives smoothness of the divisor space at the expected dimension
$$
R=h^0(L)-1+h^1(\mathcal O_X)-h^1(L)
  =r+q-\omega.
$$
It does not say that every divisor is semiregular, nor that semiregularity is necessary for every accidental smooth point. Kodaira and Spencer's 1959 completeness theorem and the later algebraic treatments belong here, with their hypotheses retained (Kodaira & Spencer, 1959; Kleiman, 2005, Remark 5.18). A different modern integration criterion is the transversality theorem of Mendes Lopes, Pardini, and Pirola (2013, Theorem 1.1), which states explicit cup-product exactness conditions; it is not an unconditional validation of first-order splitting.

One instructive classical counterexample can be expressed without any period calculation. Let $E$ be an elliptic curve and $V$ a nonsplit extension $0\to\mathcal O_E\to V\to\mathcal O_E\to0$. In the ruled surface $\mathbb P(V)$, the section $D$ defined by the quotient has normal bundle $\mathcal O_E$. Hence $h^0(N_D)=1$, but the section is isolated among the corresponding algebraically equivalent sections: a distinct such section would be disjoint from it and split the extension. The nonzero first-order motion does not integrate. Kleiman (2005, Remark 5.18) identifies this as the Severi–Zappa example and points to Mumford's treatment. It directly refutes any assertion that smoothness of $\operatorname{Pic}^0$ alone forces all complete characteristic systems.

### IX.4. §6, pp.339–347: historical claims and their mathematical content

The historical section should be read as Enriques's retrospective account, not as independent verification of every priority claim. Its references document a chain of ideas: rationally parametrized systems; the relation between inequivalent curves and irregularity; integrals of the first and second kind; the 1904 characteristic-system announcement; criticisms and attempted repairs; and Poincaré's analytic proof.

A rationally parametrized family of divisor classes is constant because every morphism $\mathbb P^1\to A$ to an abelian variety is constant. Thus such a family is contained in one complete linear system. This is the precise modern statement behind the opening observation. A family may be a proper subfamily of that linear system.

The trace construction of first-kind integrals from an incidence correspondence is a valid route to holomorphic one-forms. Over $\mathbb C$,
$$
h^0(X,\Omega_X^1)=h^1(X,\mathcal O_X)=q,
\qquad b_1(X)=2q.
$$
Second-kind integrals modulo exact ones describe the relevant de Rham cohomology; one must not count arbitrary meromorphic primitives without quotienting by exact differentials. The equality of the two Hodge summands and the period-lattice statement are characteristic-zero ingredients.

The genus-two example on p.341 has two distinct models. A theta divisor on the abelian surface $J(B)$, $g(B)=2$, has genus two and self-intersection two. Its translates provide a two-dimensional family with complete normal series $K_B=g^1_2$, although $\vert \Theta\vert $ has dimension zero. The symmetric square $B^{(2)}$, however, is the blowup of $J(B)$ at the canonical class; its coordinate curves $B+b$ have self-intersection one. The example must be placed on the abelian model when the characteristic degree is two.

The intrinsic construction $(C+D)\vert _C-D\vert _C=\mathcal O_C(C)$ correctly explains why the complete normal series is independent of the chosen residual divisor $D$. That independence does not imply its integrability. Pages 342–343 acknowledge that the original completeness argument exceeded what had been demonstrated. The later statement on p.347 that the construction completes the geometric proof cannot override the revisers' p.333 warning or the explicit missing steps audited above.

The sentence on p.344 that surfaces with $p_g=1,p_a=0$ always have a “pencil of elliptic curves” needs careful interpretation. Such a surface has $q=1$, hence has a pencil **over an elliptic base**, as §12 correctly says, with fibers of arbitrary genus. If the sentence means fibers of genus one, it is false without an additional classification hypothesis: general-type surfaces with $p_g=q=1$ and genus-two Albanese fibers exist. Lewis and Lyons (2018, §2 and Theorem 2.1) explicitly describe examples with $K_X^2=2$ as double covers of $E^{(2)}$ and identify their Albanese fibers as genus two. The source's two phrasings are not interchangeable. The claim that a surface with trivial canonical bundle and $p_g=1$ cannot have $q=1$ is valid and is examined separately on p.357.

The following attribution levels have been retained throughout the register:

- Enriques's account of his own and Castelnuovo's communications is recorded as a historical statement in this source.
- The existence and bibliographic identity of the modern Picard-scheme and completeness references listed below were checked independently.
- The audit does not claim to have read every nineteenth- or early-twentieth-century paper named in the footnotes, nor to adjudicate every priority dispute from those papers.

### IX.5. §7, pp.347–353: Segre's splitting argument, lost limits, and exorbitant systems

#### The dimension paradox and what it actually proves

Segre's attempted argument retains $m-p_g$ nodes while smoothing a union $C+D$. The normalization's characteristic series is assigned dimension
$$
2p_g+(n-\pi)+(\nu-\rho)+1.
$$
The naïve product of the two component characteristic series has dimension one less:
$$
2p_g+(n-\pi)+(\nu-\rho).
$$
That discrepancy is a contradiction only if the **entire** limiting linear series has been identified. It is not enough to compute the limits of a preferred set of cutting curves that remain proper intersections.

The plane-octic example is decisive. A degree-eight curve with fifteen nodes has normalization genus $21-15=6$; its canonical series is $g^5_{10}$, obtained from quintics through the nodes. Degenerate it to two smooth plane quartics meeting in sixteen points, retaining fifteen nodes and leaving one connecting point $O$. Each quartic has genus three, and the connected nodal normalization has genus six. A quintic through fifteen points of the $(4,4)$ complete intersection passes through the sixteenth as well, by Cayley–Bacharach. Restricting only proper quintic intersections therefore seems to lose a parameter.

The missing limits arise when the cutting quintic acquires one quartic as a component. In a modern limit-linear-series description, the aspects may be represented by $K_C+2O$ on one component and $K_D$ on the other, or the reverse, with the requisite gluing and scaling. The residual base point at $O$ is not present in every limiting aspect. The source's hyperbola example makes the same point in elementary form: for $xy=t$, a line tending an asymptote can produce residual points on that asymptote, which are absent if one substitutes $t=0$ before taking the closure of the intersections.

The supplied editorial apparatus proposes changing “curves $C_8$” to $C_5$ in the p.349 sentence about curves through fifteen points not being forced through $O$. That emendation is unsupported and would make the sentence false: quintics through fifteen of the sixteen points are forced through $O$, whereas degree-eight forms with those simple vanishing conditions are not. The printed $C_8$ naturally concerns degree-eight deformations of the quartic union, distinct from the quintic canonical cutters. The audit retains $C_8$ and rejects this attempted editorial correction. For example, restriction of degree-eight forms to $C_4$, after the fifteen imposed points, has degree $32-15=17$; it is not forced to vanish at the sixteenth point. This distinction is independent of the need to include all limiting canonical divisors.

On p.350, the disputed differential lemma is asked to force all $p_g$ connecting points to remain fixed in every limit, including limits with a common component. The passage does not prove that property. Enriques explicitly withdraws his own proposed solution using irreducible cutters. His criticism is a substantive warning about nonproper intersection and specialization, not a proof of a substitute lemma.

#### A verifiable modern splitting statement

Felisetti and Fontanari (2022, Theorem 1.1) give a precise version. The family is flat over a normal base, all curves are nodal, the general member is irreducible, and the special member is $C+D$ with irreducible components. Write $\Gamma=C\cap D=\Gamma_1\sqcup\Gamma_2$, with $\Gamma_1$ the persistent nodes. Assume the complete system $\vert \mathcal O_D(D)\vert $ is nonempty and the stated generality of $C$ relative to $D$, in particular that $\vert C(-\Gamma_1)\vert $ has no base point on $D$. Then either $\vert \Gamma_2\vert \geq p_g+1$, or $\Gamma_2$ imposes dependent conditions on $H^0(K_X)$.

The conclusion concerns the actual connecting nodes and canonical dependence. It does not identify every classical limiting characteristic series and does not validate every hypothesis-free version historically called the splitting principle. The article explicitly notes the missing nodality and generality assumptions in the original formulation.

#### Cohomological meaning of the three cases, pp.351–352

Set $\epsilon=\operatorname{rank}[H^1(\mathcal O_X)\to H^1(L)]$. Then
$$
\delta=q-\epsilon,\qquad 0\leq\epsilon\leq\min(q,\omega).
$$
Under the **express hypothesis** that the chosen complete continuous family has complete characteristic system, its dimension is $r+q-\epsilon$. The cases are:

1. $i>0,\omega=\epsilon=0$: the family dimension is $r+q$, with $q$ parameters of complete linear systems. Generic constancy of the fiber dimension gives the same speciality index.
2. $i=0,\omega>0,\epsilon=0$: the family dimension is again $r+q$. The image in the Picard variety has dimension at most $q$; semicontinuity gives generic fiber dimension at most $r$. Equality of total dimensions forces both bounds to be equalities, so the generic superabundance remains $\omega$.
3. $i=0,\omega=\epsilon>0$: the family dimension is $r+q-\epsilon$. Its image dimension can lie between $q-\epsilon$ and $q$, while generic linear-system dimension lies between $r-\epsilon$ and $r$. The extreme alternatives described by Enriques are compatible with this formula.

The family-completeness premise on p.351 is indispensable. This passage does not assert it for all families; it explicitly retreats from the earlier universal claim.

#### The ruled quintic and the two components

On the normalization of the ruled quintic $F_5$, the base has genus two, so $p_g=0,p_a=-2,q=2$. The hyperplane divisor $C$ has $C^2=5$, genus two, $K_XC=-3$, and $\chi(\mathcal O_X(C))=3$. The displayed $r=3$ gives $h^0=4$ and $\omega=1$. Its normal degree is five, so $h^1(N)=0$ and $h^0(N)=4$; thus $\delta=1$, exactly as stated. The divisor family has dimension four, although its general members lie in two-dimensional complete linear systems varying over a two-dimensional Picard component. A three-dimensional special linear system is a jumping fiber, not evidence for a one-dimensional class parameter.

Adding two ruling fibers produces the degree-nine model $F_9$ in $\mathbb P^6$. The special pair of incident generators produces the node used in the projection back to $F_5$. A second four-dimensional family arises from hyperplanes through this node and one ruling generator: it has one parameter of classes and three-dimensional linear systems. The pair of preimages $A,B$ of the node imposes only one condition on the special system and two on a general twist. This is the mechanism of “neutral” conditions and the meeting of distinct divisor components.

There is a visible omission in the p.353 residual formula. The prose says to subtract a ruling generator after imposing $A,B$, but the displayed expression $\vert C+\bar a+\bar b-A-B\vert $ omits that generator. On the blowup at $A,B$, its displayed square is $9-2=7$; subtraction of a ruling fiber is needed to get square five and the stated $g^3_5$. The correction register records the omission without pretending that an invisible symbol is present in the scan.

#### The cone examples and the precise meaning of exorbitance

Let $B\subset\mathbb P^2$ be a smooth plane curve of degree $n\geq3$, genus $(n-1)(n-2)/2$, and $L=\mathcal O_B(1)$. On the standard ruled resolution of its cone, let $E$ be the negative section with $E^2=-n$. The hyperplane class is $H=E+f^*L$, with $H^2=n$ and $h^0(H)=h^0(L)+h^0(\mathcal O_B)=4$. For a nontrivial degree-zero twist $\alpha$, the section contributed by $H^0(\alpha)$ disappears; effective divisors are the vertex section plus the fibers over a divisor in $\vert L\otimes\alpha\vert $.

For $n=3$, the generic fiber linear system has dimension two and the class locus dimension one. For $n=4$, these dimensions are one and three. For $n\geq5$, the effective class locus $W_n(B)$ has dimension $n$ and its general system is zero-dimensional. These are exactly the counts on p.353. “Contained” is correct for the class of $H$ in the closure of effective classes; it does not say that every hyperplane section belongs to the closure of the generic effective divisors. This is the geometric content of an exorbitant linear system.

### IX.6. §8, pp.354–357: paracanonical systems, correct dimensions, and counterexamples

#### The general formula and the invalid extension of a section

The paracanonical component is $\operatorname{Pic}^{K_X}(X)$. For $\alpha\ne\mathcal O_X$ in $\operatorname{Pic}^0(X)$,
$$
h^2(K_X\otimes\alpha)=h^0(\alpha^{-1})=0.
$$
Indeed, an effective nonzero divisor with numerically trivial class would have positive intersection with an ample divisor, a contradiction. Hence
$$
h^0(K_X\otimes\alpha)=\chi(\mathcal O_X)+h^1(K_X\otimes\alpha),\qquad
\dim\vert K_X\otimes\alpha\vert =p_a+h^1(K_X\otimes\alpha).
\tag{IX.6}
$$
If $p_a\geq0$, every nontrivial twist is effective. At the canonical class itself, $h^2(K_X)=1$, so one must not apply the §2 inequality with $i=0$ there. Formula (IX.6), rather than that substitution, establishes the p.354 effectivity assertion.

For the sufficiently positive auxiliary $C$, the adjoint system has dimension $p_a+\pi-1$, and its image on $C$ is a canonical subseries of dimension $\pi-1-q$. The group $G=C\cap K_X$ has degree $2\pi-2-n$. The flawed old proof assumes that every canonical divisor can be reached as a limit from any nearby paracanonical linear system, so that arbitrary normal directions are represented by nearby residual canonical curves. Pages 354–355 correctly reject this: a smaller nearby linear system can specialize to a proper subsystem of $\vert K_X\vert $. The predicted universal dimension $2p_g-p_a-1$ is therefore not established.

#### What generic vanishing proves, and what the source conjectures

The source calls the alternative dimension $p_g$ probable under $q>1,p_a\geq0$, and smooth irreducible canonical curves. It is not stated as a proved theorem. Under the additional hypothesis of **maximal Albanese dimension**, generic vanishing gives
$$
h^i(K_X\otimes\alpha)=0\quad(i>0)
$$
for general $\alpha$. The main paracanonical component then has dimension
$$
\chi(\mathcal O_X)-1+q=p_g.
$$
This is an appropriate modern theorem explaining the symmetric-square examples, with the Albanese hypothesis retained (Green & Lazarsfeld, 1987; Mendes Lopes et al., 2013). Generic vanishing is not a theorem for all irregular surfaces merely because their canonical system has a smooth irreducible member.

**Audit counterexample to the conjecture as literally phrased; independently derived, confidence high.** Let $B$ have genus $b>1$, put $Y=B\times\mathbb P^1$, and choose
$$
L=A\boxtimes\mathcal O_{\mathbb P^1}(d),\qquad
a=\deg A\gg0,\quad d\geq3.
$$
Let $\pi:X\to Y$ be the smooth double cover branched over a general member of $\vert 2L\vert $. The standard double-cover algebra is
$$
\pi_*\mathcal O_X=\mathcal O_Y\oplus L^{-1},\qquad
K_X=\pi^*(K_Y+L).
$$
Künneth gives $H^1(Y,L^{-1})=0$, hence $q(X)=b$. Also
$$
p_g(X)=h^0(Y,K_Y+L)=(a+b-1)(d-1).
$$
The bundle $K_Y+L=(K_B+A)\boxtimes\mathcal O(d-2)$ is ample and globally generated; a general member of its pullback canonical system is smooth, and connectedness of an ample divisor makes it irreducible. The pullback identifies $\operatorname{Pic}^0(B)$ with $\operatorname{Pic}^0(X)$: it is injective, and dimensions are equal. For every $\alpha\in\operatorname{Pic}^0(B)$,
$$
h^0(X,K_X\otimes f^*\alpha)=(a+b-1)(d-1)=p_g(X).
$$
The dimensions are constant because $\deg(K_B+A)$ is above the special range. Consequently the paracanonical family has dimension $p_g+b-1>p_g$. These examples have $p_a=p_g-b\geq0$ and the source's stated irreducibility properties. The missing maximal-Albanese-dimension hypothesis is therefore substantive, not cosmetic.

#### Symmetric squares: the cases $q=3,4,5$ are computable

Let $X=B^{(2)}$, where $B$ is a smooth curve of genus $g$. Then
$$
q=g,\quad p_g=\binom g2,\quad
p_a=\frac{g(g-3)}2,\quad
\chi(\mathcal O_X)=\binom{g-1}{2},\quad
K_X^2=(g-1)(4g-9).
$$
For a degree-zero line bundle $\alpha$ on $B$, the determinant-tautological description gives
$$
H^0(X,K_X\otimes\alpha^{(2)})
\cong\bigwedge\nolimits^2 H^0(B,K_B\otimes\alpha).
\tag{IX.7}
$$
For $\alpha\ne\mathcal O_B$, curve Riemann–Roch gives $h^0(K_B\otimes\alpha)=g-1$ and $h^1=0$. Thus the paracanonical linear systems have dimension $p_a$, and their total main component has dimension $p_g$. This directly answers the source's questions about completeness of the trace constructions. Sheridan (2022; author manuscript, §1 and Example 1.3) supplies the determinant construction and a modern description of these divisor components.

For $g=3$, the general paracanonical system consists of one divisor, with a three-dimensional family of classes; $\vert K_X\vert $ has dimension two. The source's $K_X^2=6$, canonical-curve genus seven, and Clifford obstruction to a nonhyperelliptic $g^3_6$ are consistent. For $g=4$, the general system is $\mathbb P^2$, with four parameters of classes, giving dimension six. The canonical $\mathbb P^5$ is an extra component; its intersection with the main component is the Plücker quadric $\operatorname{Gr}(2,4)$. Nondecomposable two-forms explain why a general canonical divisor does not deform out of $\vert K_X\vert $. For $g=5$, the general paracanonical system is $\mathbb P^5$, with five class parameters, giving dimension ten. Pencils in a four-dimensional space of sections form $\operatorname{Gr}(2,4)$, a quadric that spans $\mathbb P(\bigwedge^2\mathbb C^4)=\mathbb P^5$; the complete system is larger than just its decomposable trace divisors.

There is a separate slip in the explanation on p.356: the scan says that the chord surface belonging to a “special linear complex” cannot occur as a paracanonical limit. With the standard classical identification of a linear complex with an alternating form on the four-dimensional canonical section space, a special complex has rank two, hence is decomposable. These are exactly the points of $\operatorname{Gr}(2,4)$, the limit locus just described. It is the general **nonspecial**, rank-four complex that lies outside the main component. Thus the asserted exorbitance of the whole canonical system is correct, but the special/nonspecial description of the excluded members is reversed. The correction concerns that explanation, not the dimension six or the existence of the extra canonical component. **Confidence: high, with the classical rank-two meaning of “special complex” made explicit.**

One can also see the parity phenomenon directly. A canonical two-form $s$ induces, by cup product and duality, an alternating map $H^1(\mathcal O_X)\to H^1(K_X)$. Its kernel determines the normal-series deficiency. An odd-dimensional alternating matrix has nontrivial kernel; an even-dimensional one may be invertible. This explains why deficiency one is plausible in the odd-$q$ examples but cannot be asserted for every canonical divisor with even $q$.

#### Elliptic surfaces: two original numerical errors

The scan on p.356 really prints that a canonical curve is composed of $p_g-1$ elliptic fibers; this confuses projective dimension with degree on the base. A clean subclass already disproves the printed count. Let $f:X\to B$ be a relatively minimal elliptic surface with section, $\chi(\mathcal O_X)>0$, and fundamental line bundle $\mathcal L$ of degree $\chi(\mathcal O_X)$. Then
$$
K_X=f^*(K_B+\mathcal L),\qquad
q=g(B),\qquad
\deg(K_B+\mathcal L)=2q-2+\chi(\mathcal O_X)=p_g+q-1.
\tag{IX.8}
$$
For every $\eta\in\operatorname{Pic}^0(B)$, this base line bundle has degree greater than $2q-2$, so
$$
h^0(K_X\otimes f^*\eta)=p_g,\qquad
\dim\vert K_X\otimes f^*\eta\vert =p_g-1.
$$
The total dimension is therefore $p_g-1+q=2p_g-p_a-1$, including when $p_a=0$. Formula (IX.8) is the canonical-bundle formula, not an inference from the desired dimension (Schütt & Shioda, 2010, Theorems 6.8 and 6.12).

Page 357 instead puts $2q-2=2p_g-2$ fibers in the $p_a=0$ canonical divisor and lowers the generic linear-system dimension to $p_g-2$. That corresponds to forgetting the positive degree-one fundamental line bundle $\mathcal L$. For example, take an elliptic base $B$, $\deg\mathcal L=1$, and a general Weierstrass equation with coefficients in $\mathcal L^4,\mathcal L^6$. Its minimal smooth surface has $p_g=q=1,p_a=0$, canonical divisor one fiber, and a one-dimensional family of unique paracanonical divisors. The printed prediction gives total dimension zero. This counterexample requires no multiple-fiber subtleties. Multiple fibers in a more general elliptic fibration add canonical-bundle terms and must be treated separately; they cannot rescue a statement already false for elliptic surfaces with section. **Independent calculation; confidence high.**

The final observation on p.357, that $K_X\cong\mathcal O_X$ and $p_g=1$ cannot coexist with $q=1$, is correct. Choose an ample smooth $C$. Then $N_C=K_C$, and for a nontrivial $\alpha\in\operatorname{Pic}^0(X)$, vanishing gives $h^0(C+\alpha)=\pi$ if $q=1$. Restriction is injective because $h^0(\alpha)=0$. For sufficiently ample $C$, restriction of $\alpha$ remains nontrivial, so $K_C\otimes\alpha\vert _C$ is a noncanonical degree-$2\pi-2$ line bundle with only $\pi-1$ sections. This contradiction makes the source's short curve-theoretic proof rigorous.

### IX.7. §9, pp.357–361: abelian varieties, group actions, and unramified covers

A modern abelian variety is a connected projective algebraic group. Analytically it is a complex torus $\mathbb C^q/\Lambda$, with $\Lambda$ a lattice of rank $2q$, admitting a positive integral Riemann form. The polarization/algebraicity condition matters: a general complex torus is not projective. Enriques includes algebraicity and nondegeneracy in his definition, but the phrase “$2q$-periodic functions” alone would not be a sufficient modern definition.

Translations form a simply transitive group: exactly one translation sends a specified point to another. On a Picard torsor, residual involutions have the form $x\mapsto a-x$, and their even products are translations. The **mixed** group containing translations and these inversions is not simply transitive in the literal modern sense. Both a translation and an inversion send any given point to a prescribed target; inversions have fixed points satisfying $2x=a$. Thus “simply transitive” on p.357 is accurate for the connected translation subgroup, not for the whole mixed group.

The variety of effective degree-$g$ divisors $B^{(g)}$ is birational to $\operatorname{Pic}^g(B)$; it is not generally itself an abelian variety. The Abel map contracts special complete linear systems. Enriques's “exceptional variety” belongs to the symmetric-product model, whereas the nonsingular Jacobian has no such exceptional divisor and has a regular translation action. Keeping these models separate resolves much of the apparent tension between “without exception” and later contractions.

The reducible-period discussion expresses the existence of an abelian subvariety of a Jacobian and its complementary factor **up to isogeny**. For a polarized abelian variety $A$ and subvariety $B$, the connected kernel of the dual map associated to the polarization supplies a complementary $B'$ such that $B\times B'\to A$ is finite and surjective. It need not be a product isomorphism (Milne, 2008, I, Proposition 10.1).

Restriction from $X$ to a sufficiently ample smooth curve embeds $\operatorname{Pic}^0(X)$ in its Jacobian. Every complex abelian variety also arises as a Picard variety of a smooth projective surface: for dimension at least two take a smooth complete-intersection surface in its dual and apply weak Lefschetz; in dimension one take the dual elliptic curve times $\mathbb P^1$. Cutting further to a sufficiently ample curve and dualizing the resulting Jacobian quotient gives an embedding into a Jacobian. This supplies the content of the “Torelli theorem” named here; it is not the modern Torelli assertion that a polarized Jacobian determines its curve.

The proof on p.359 is a geometric precursor of the polarization map
$$
\phi_L:A\longrightarrow\widehat A,\qquad
a\longmapsto t_a^*L\otimes L^{-1}.
$$
For ample $L$, this is an isogeny. Thus the translation orbit of a sufficiently general divisor maps finitely to its linear-equivalence classes, and the number $s$ in the text is the order of the finite kernel. A positive-dimensional connected subgroup cannot act nontrivially through projective transformations on a fixed complete linear system: a homomorphism from a proper connected group to the affine group $\operatorname{PGL}$ is constant. The source's fixed-point argument gestures toward this fact but presupposes algebraicity and regularity of the action. As an audit extension, $\deg\phi_L=(L^q/q!)^2$; for an elliptic curve and a degree-$d$ line bundle it is $d^2$.

Pages 360–361 prove that a connected finite unramified cover of an abelian variety is again abelian. In the complex setting, this has a direct complete proof: if $A=\mathbb C^q/\Lambda$, a connected finite covering corresponds to a finite-index sublattice $\Lambda'\subset\Lambda$. Its total space is $\mathbb C^q/\Lambda'$; pullback of a polarization makes it projective. Choosing an origin makes the covering an isogeny. All translations lift, and the deck group is finite abelian.

The source's monodromy argument is sound in outline once this covering-space setup is supplied. Its final commutator calculation is also correct: if $T\Pi T^{-1}=\Pi\Omega$ and $\Omega$ lies in a finite deck group, then $\Omega$ is constant as $T$ varies in a connected group. At the identity it is $1$; therefore the lifted translations commute. This does not establish connectedness or a group law from a bare multivalued rational correspondence without the earlier covering assumptions.

### IX.8. §10, pp.361–364: canonical divisors on symmetric products and genus one of abelian varieties

Let $B$ be a smooth curve of genus $p$, and let $B^{(q)}$ denote its $q$-th symmetric product. The claim concerns $1\leq q\leq p$, and the notation $J_q$ in the source here denotes this symmetric product, not an abelian variety of dimension $q$.

For a $q$-dimensional subspace $W\subset H^0(B,K_B)$, evaluate sections on a divisor $\xi$ of degree $q$. The determinant of
$$
W\longrightarrow H^0(\xi,K_B\vert _\xi)
$$
vanishes exactly when $\xi$ lies in a member of the associated $g^{q-1}_{2p-2}$. Its divisor is the determinant-tautological divisor $N_{K_B}$, and
$$
N_{K_B}=K_{B^{(q)}},\qquad
H^0(B^{(q)},K_{B^{(q)}})\cong\bigwedge\nolimits^qH^0(B,K_B).
\tag{IX.9}
$$
One can verify the canonical identification locally off the diagonals by writing the determinant of the differentials at the $q$ points; the alternating determinant cancels the quotient ramification along the diagonals and extends across collisions. This provides a precise construction of the canonical divisor described in the text.

For $q=2$, the coordinate curve $M_A=A+B$ is isomorphic to $B$, has normal bundle $\mathcal O_B(A)$, and self-intersection one. Adjunction gives
$$
K_{B^{(2)}}\vert _{M_A}=K_B-A.
$$
The divisor cut by the chosen canonical pencil consists of the $2p-3$ points other than $A$ in its member through $A$. The missing point $(A,A)$ is the characteristic point of the moving coordinate curves. Thus the source's intersection calculation correctly identifies the adjunction residual.

For the induction, $M_{q-1}=A+B^{(q-1)}$ has normal divisor $M_{q-2}$, and
$$
K_{B^{(q)}}\vert _{M_{q-1}}=K_{M_{q-1}}-M_{q-2}.
$$
This is the clean line-bundle statement behind the generalization of the “third equivalence criterion.” The source gives a sketch of that generalization, not a proof of the criterion in every dimension. The scan has two index/letter slips: on p.362 the variety called the image of $g^{q-1}_{2p-2}$ should be $K_{q-1}$, although it prints $M_{q-1}$; on the first line of p.363 the restriction is to $M_{q-1}$, not the printed $M_{q-2}$.

For $q=p$, (IX.9) gives $h^0(K_{B^{(p)}})=1$. Its canonical divisor is the exceptional divisor of the Abel map $B^{(p)}\to J(B)$. The canonical bundle on the Jacobian itself is trivial. These are compatible statements on different birational models.

The extension to all abelian varieties has an immediate proof independent of the symmetric-product model. Translation identifies every tangent space with $T_0A$, so
$$
T_A\cong\mathcal O_A^{\oplus q},\qquad
\Omega_A^1\cong\mathcal O_A^{\oplus q},\qquad
K_A\cong\mathcal O_A.
$$
Because $A$ is connected and projective, $h^0(\mathcal O_A)=1$, hence its geometric genus $h^0(K_A)$ is one. An étale isogeny preserves this canonical triviality. This validates the conclusion on p.363 without treating contractions on a symmetric product as if they occurred on an abelian variety.

The alternative genus-two argument on p.364 is geometrically informative but abbreviated. A base-point-free degree-four pencil on a genus-two curve has ten simple branch points. Its unordered-pair trace curve is a degree-six cover of $\mathbb P^1$; a transposition of four letters acts on their six two-element subsets as two transpositions, so it gives two simple ramification points. Riemann–Hurwitz yields
$$
2g(L)-2=-12+20=8,\qquad g(L)=5.
$$
On the minimal abelian surface, its divisor class is a translate of $2\Theta$, with square eight. The net in the construction has two simple base points, leaving effective intersection degree six. The complete normal line bundle on a smooth $L$ is $K_L$. These statements justify the source's genus and degree counts. They should not be read as saying that a two-dimensional linear net by itself cuts the entire four-dimensional canonical series: its tangent image and the complete normal series are distinct. The auxiliary $g^2_6$ completed in $A+B+g^2_6\subset g^4_8$ likewise must be distinguished from the pencil cut by the net's other members. The source invokes Zeuthen's correspondence formula rather than writing this ramification calculation.

### IX.9. §§11–12, pp.365–369: $p_g=0$, Albanese pencils, and irregularity one

#### Surfaces in abelian varieties and the missing hypothesis in a generalization

If a smooth surface maps generically finitely onto a two-dimensional subvariety of an abelian variety, it has a nonzero holomorphic two-form. At a point where the differential has rank two, choose two invariant one-forms whose restrictions are independent. Their wedge pulls back nontrivially. After resolving a singular subvariety, the same argument applies. This proves the p.365 conclusion $p_g>0$ directly.

The translation orbit of a surface in a $q$-dimensional abelian variety has dimension at least $q-2$, since its stabilizer has dimension at most two. This dimension estimate is correct. The broader assertion that a family of surfaces of dimension at least $q-2$ in **any** $q$-fold of positive geometric genus must have members of positive geometric genus requires an additional coverage/characteristic-rank hypothesis.

**Audit counterexample, confidence high.** Let $V=S\times T$, where $S,T$ are projective K3 surfaces and $S$ contains a smooth rational curve $R$. Let $D$ vary in a sufficiently large complete linear system on $T$. The surfaces $R\times D$ form a family of dimension at least two, while $p_g(R\times D)=0$. Yet $h^0(K_V)=1$. The family fills only $R\times T$, not $V$. This violates the general statement as literally phrased.

A sufficient corrected hypothesis is that the evaluation map of a family of smooth surfaces dominates the ambient smooth $q$-fold and has normal characteristic rank $q-2$ at a general point. Contract a nonzero ambient $q$-form with $q-2$ independent characteristic sections. Adjunction gives a nonzero two-form on a general member. Translation families satisfy this condition; an arbitrary large family need not. The source's induction silently uses this rank when it assumes the one-parameter subfamilies sweep genuine threefolds and the successive families sweep the ambient variety.

#### A complete modern proof of the $p_g=0$ pencil theorem

Suppose $p_g(X)=0$ and $q>0$. Let $a:X\to A=\operatorname{Alb}(X)$. Its image cannot be two-dimensional, by the preceding wedge-of-one-forms argument. It cannot be a point, because pullback identifies invariant one-forms on $A$ with all holomorphic one-forms on $X$. Thus its image is a curve. Stein factorization gives a morphism
$$
f:X\longrightarrow B
$$
with connected fibers and smooth projective base $B$.

Pullback of one-forms gives $g(B)\leq q$. Conversely, the Albanese image generates $A$, so the induced $J(B)\to A$ is surjective, giving $q\leq g(B)$. Therefore
$$
g(B)=q=-p_a.
\tag{IX.10}
$$
This proves the required irrational pencil. The genus in the theorem is the genus of the base, not the genus of its moving curves. If there were two independent connected pencils over positive-genus curves, the product map would be generically finite onto the product of the bases. Pullback of the tensor products of their one-forms would give nonzero two-forms on $X$, contrary to $p_g=0$. Thus the Albanese pencil is unique up to an isomorphism of its base.

The converse sentence on p.366 prints $p_a=0$; it must read $p_g=0$. With $p_a=0$ and $p>0$, the stated conclusion $p_a=-p$ is self-contradictory. Under $p_g=0$, a connected irrational pencil is the Albanese pencil and has genus $q$, so the converse is correct.

#### The original incidence proof, pp.366–368

For a one-parameter family of curves of index $i>2$, let $C_i(x)$ be the sum of the $i$ members through $x$. The source distinguishes the dimension of the image of $x\mapsto[C_i(x)]$ in the appropriate Picard/Jacobian variety:

- Dimension zero: the sums are linearly equivalent. The cited Severi–Castelnuovo correspondence criterion implies that the original family has constant linear class, so it is contained in a linear system.
- Dimension one: fibers of the class map give an irrational pencil. Restrictions of the original curves to a general fiber have constant class; their differences are vertical, and the earlier equivalence criterion expresses them as differences of fibers.
- Dimension two: the map is generically finite onto a surface in an abelian variety, forcing $p_g>0$.

For $p_g=0$, an inequivalent family therefore yields the middle case. The rank-zero and vertical-equivalence steps are applications of the earlier chapter's equivalence criteria, not proved afresh here. In particular, reducible singular fibers require care: their components form a discrete lattice of divisor classes. A connected algebraic family cannot vary its discrete component class, but this does not by itself make two named effective components literally identical. The $K_1=\bar K_1$ line on p.367 abbreviates this cancellation in a class calculation.

The displayed equalities in this argument are statements of linear equivalence, even where the scan uses an ordinary equals sign. Modern notation $C+\sum K\sim C_0+\sum K'$ prevents confusion with equality of effective divisors.

The first two paragraphs of p.368 are physically obscured by overlapping leaves. The supplied transcription says it restored them from an exposed scan called s197L, which is **not included** among the available source images. Their mathematical content is consistent with (IX.10) and the independent-two-pencil argument, but that does not verify their hidden wording. All obscured restorations remain explicitly unresolved in the corrections register. The exposed historical notice and footnotes were read directly. Its transcendental argument is the same wedge obstruction: functionally independent first-kind integrals would produce a nonzero two-form; otherwise their level sets yield the Albanese pencil.

#### Irregularity one, p.369

For every smooth projective complex surface with $q=1$, the Albanese variety is an elliptic curve and its image is the whole curve. The Albanese morphism has connected fibers. To see this, factor through a smooth curve $B$. Since $g(B)\leq q=1$ and $B\to\operatorname{Alb}(X)$ is nonconstant, $B$ has genus one. The universal property yields a reverse homomorphism from $\operatorname{Alb}(X)$ to $B$ splitting the finite map; this forces that finite map to be an isomorphism. Thus the pencil is over an elliptic base, with fiber genus $\pi\geq0$ unrestricted.

Moreover $f^*:\operatorname{Pic}^0(B)\to\operatorname{Pic}^0(X)$ is an isomorphism. If $C,C_0$ are algebraically equivalent divisors, their difference is
$$
\mathcal O_X(C-C_0)=f^*\mathcal O_B(b-b_0),
\qquad C\sim C_0+F_b-F_{b_0}.
\tag{IX.11}
$$
Fibers here mean the full scheme-theoretic fibers, including multiplicities. This is the exact content of the final assertion about continuous systems. It does not say that every twist is effective or that all effective representatives belong to one irreducible divisor component. The formula concerns line-bundle classes and is compatible with exorbitance.

Printed p.370 is blank apart from marks and a handwritten folio. It contributes no mathematical claim.

### IX.10. Characteristic and hypothesis boundary

The identities from Riemann–Roch, adjunction, and the cohomology of (IX.1) remain valid over an algebraically closed field for a smooth projective surface. The identification
$$
\dim\operatorname{Pic}^0_{\mathrm{red}}=h^1(\mathcal O_X)
$$
does not hold in arbitrary positive characteristic: the Picard scheme may be nonreduced. Its tangent dimension is still $h^1(\mathcal O_X)$, while its reduced dimension measures actual class parameters. Characteristic-zero smoothness, Hodge symmetry, $b_1=2q$, and integration of complex periods must not be transported unchanged to characteristic $p$. Kleiman (2005, Corollaries 5.13–5.14 and Remark 5.15) explicitly separates these facts and examples.

Even in characteristic zero, smoothness of the Picard variety does not imply smoothness of the divisor scheme, and semiregularity of one divisor does not establish completeness for every family on the surface. Nor does generic vanishing apply to Albanese dimension one without additional hypotheses. These are different limits of applicability, and the audit keeps them separate.

### IX.11. References and verification status

The supplied Enriques pages are the primary evidence for what the chapter states, proves, sketches, retracts, and cites. The following references were independently verified through author/institutional manuscripts, journal metadata, or the primary texts indicated. Modern proofs explicitly labeled as audit extensions are our own derivations from their stated hypotheses; citing a standard theorem does not attribute the particular example or analysis to its author.

- Felisetti, C., & Fontanari, C. (2022). On the splitting principle of Beniamino Segre. *Annali di Matematica Pura ed Applicata, 201*(4), 1577–1581. https://doi.org/10.1007/s10231-021-01171-w . Primary manuscript: https://arxiv.org/pdf/2105.00892 . Theorem 1.1 and its hypotheses were read; publication details were checked against the University of Modena and Reggio Emilia record, https://iris.unimore.it/handle/11380/1286089 .
- Green, M., & Lazarsfeld, R. (1987). Deformation theory, generic vanishing theorems, and some conjectures of Enriques, Catanese and Beauville. *Inventiones Mathematicae, 90*(2), 389–407. https://doi.org/10.1007/BF01388711 . Bibliographic identity was checked against institutional metadata; the application here is the standard generic-vanishing theorem for maximal Albanese dimension, also explicitly used in Mendes Lopes et al. The audit does not claim an independently checked page-specific proof in the original article.
- Kleiman, S. L. (2005). *The Picard scheme*. arXiv. https://arxiv.org/abs/math/0504020 . Full author text: https://arxiv.org/html/math/0504020v1 . Relevant verified locators: Theorem 5.4 (projectivity under normality), Theorem 5.11 (tangent space), Corollaries 5.13–5.14 (dimension and characteristic-zero smoothness), Remark 5.15 (positive-characteristic behavior), Remark 5.18 (divisors, semiregularity, historical counterexamples), and Proposition 5.19 ($H^2(\mathcal O)=0$).
- Kleiman, S. L. (2013). The Picard scheme. In *Alexandre Grothendieck: A mathematical portrait* (pp. 35–74). International Press. Verified author manuscript: https://dspace.mit.edu/server/api/core/bitstreams/7c844b02-9b45-42e9-82cb-a7b41c86ab8b/content . Institutional metadata: https://dspace.mit.edu/entities/publication/b19e8bf7-8b44-404b-b54c-ddceddc1a5d9 . Used for historical orientation, not as evidence that the unfinished proof in the supplied scan is complete.
- Kodaira, K., & Spencer, D. C. (1959). A theorem of completeness of characteristic systems of complete continuous systems. *American Journal of Mathematics, 81*(2), 477–500. https://doi.org/10.2307/2372752 . Title and publication details verified through the Mathematical Society of Japan's Kodaira bibliography and journal records; the specific modern semiregularity formulation used above was checked in Kleiman (2005), rather than attributed to an unexamined page of this paper.
- Lewis, P. D., & Lyons, C. (2018). Some results on surfaces with $p_g=q=1$ and $K^2=2$. *International Mathematics Research Notices, 2018*(6), 1878–1919. https://doi.org/10.1093/imrn/rnw294 . Primary manuscript: https://arxiv.org/pdf/1508.01863 . The opening of §2 and Theorem 2.1 explicitly give genus-two Albanese fibers and double-cover constructions over $E^{(2)}$; these supply a directly checkable counterexample to interpreting p.344 as a claim about elliptic fibers.
- Mendes Lopes, M., Pardini, R., & Pirola, G. P. (2013). Continuous families of divisors, paracanonical systems and a new inequality for varieties of maximal Albanese dimension. *Geometry & Topology, 17*(2), 1205–1223. https://doi.org/10.2140/gt.2013.17.1205 . Primary manuscript: https://arxiv.org/abs/1207.4516 ; author-hosted text: https://arpi.unipi.it/retrieve/e0d6c92b-ee0e-fcf8-e053-d805fe0aa794/PARAfinal.pdf . Theorem 1.1 supplies an explicit transversality/integration criterion; the introductory definitions distinguish the main component from exorbitant systems.
- Milne, J. S. (2008). *Abelian varieties* (Version 2.00). https://www.jmilne.org/math/CourseNotes/AV.pdf . Verified locators: I §§1–3 (definition, complex tori, maps), I §§7–9 (isogenies and duality), I Proposition 10.1 (complementary subvarieties), III §§3–5 (symmetric powers and Abel maps), III Theorem 10.1 (Jacobian quotients). The canonical trivialization and finite-cover proof in this audit are written out directly.
- Schütt, M., & Shioda, T. (2010). Elliptic surfaces. *Advanced Studies in Pure Mathematics, 60*, 51–160. https://arxiv.org/abs/0907.0298 . Primary text: https://arxiv.org/pdf/0907.0298 . Theorems 6.8 and 6.12, and the hypotheses of surfaces with section and positive Euler characteristic, were checked. Their auxiliary line bundle has degree $-\chi$; our $\mathcal L$ is its inverse.
- Sheridan, J. (2022). Divisor varieties of symmetric products. *International Mathematics Research Notices, 2022*(13), 9830–9863. https://doi.org/10.1093/imrn/rnaa313 . Primary manuscript: https://arxiv.org/pdf/1906.05465 . The determinant-tautological construction and Example 1.3 were checked; general component-count theorems in §3 have additional curve-generality hypotheses and are not invoked here indiscriminately.

The following older works are cited **as references appearing in Enriques's text**, unless separately covered above: Humbert's 1893/1894 work on integrals; Enriques's 1904 characteristic-property note and 1906 linear-genus-one note; Castelnuovo's 1905 papers on simple integrals; Castelnuovo–Enriques (1906), *Sur les intégrales simples*; Severi's 1903 work on symmetric squares, 1905 integral papers, 1911 irregular-variety paper, 1916 contributions, and 1941/1942 continuous-system papers; Poincaré's 1910 work; Beniamino Segre's 1932 covariant-groups paper, 1938 splitting paper, and 1939 note; and the cited volumes of Enriques–Chisini. Their occurrence, dates as printed, and role in the chapter were checked against the supplied pages. That is narrower than independent bibliographic or priority verification.


## Supplement: page 186

### The physical witness and the recoverable mathematics

The first PDF image is assigned p. 186 in the supplied edition. Its upper-left area is covered by overlapping paper: “184” is visible on an overlapping portion, as are displaced fragments including “185.” This does **not** independently verify the underlying page number. The heading *Capitolo quinto* and the complete lower passage beginning “Si designi dunque” are legible. The missing beginnings of the three preceding paragraphs cannot be supplied from this image. In particular, the formula relating the **linear** genera, referred to in the first visible fragment, is not visible in full. The visible convention $\varrho=1,\ s=0$ when branching is absent is retained as a convention, not interpreted as the existence of an actual branch curve of genus one.

The page is important because its lower half supplies the correspondence calculation requested in the prompt. All six displayed formulas there agree with the scan, including the minus sign before the cusp count and the final constant $-4$. There is no justification for blaming the transcription for either sign. The statement about the number of singular pencil members must, however, be read as a **weighted count of nodes**, since a lifted member can have $n$ nodes at once.

### Exact modern statement of the calculation

Let $f:X\to Y$ be a finite degree-$n$ cover of smooth connected projective complex surfaces in the generic simple-branching situation intended here. For the single-genus formula, assume that the nonempty reduced branch curve $B\subset Y$ is irreducible and has ordinary nodes and cusps, that its normalization has genus $\rho$, and that the local monodromy is a transposition along a smooth branch point, two disjoint transpositions at a node, and the ordinary three-sheet cusp model at a cusp. The normalization of the ramification curve is the normalization of $B$. The empty-branch convention and the extension to several components are specified below. Write $c$ for the number of cusps: the book uses $\chi$ for this number, **not** for holomorphic Euler characteristic.

Choose a sufficiently general Lefschetz pencil $\vert c_Y\vert $ in a sufficiently high very ample system on $Y$, with $m$ simple base points disjoint from the branch curve, smooth general member of genus $\pi$, and $\delta$ nodal singularities in its singular members. Choose it transverse to the branch stratification and with generic tangency to the smooth branch locus. Its general pullback is smooth and connected: the pulled-back line bundle is ample, so its effective divisors are connected, and Bertini applies to the generated pullback system. The pullback pencil has $M$ base points, smooth general member of genus $\Pi$, and total nodal contribution $\Delta$. Let $t=c_Y\cdot B$. The printed formulas are

$$
i=\delta-m-4\pi,\qquad M=mn,\qquad
\Pi=n(\pi-1)+1+\frac t2,
$$

$$
\Delta=n\delta+2t+2\rho-2-c,
$$

and

$$
I=\Delta-M-4\Pi
 =n\delta+2\rho-2-c-nm-4n(\pi-1)-4.
$$

Here $i=e(Y)-4$ and $I=e(X)-4$, with $e$ the topological Euler characteristic. Combining the printed equations yields the correspondence relation

$$
\boxed{I=ni+4(n-1)+2\rho-2-c,}
\qquad
\boxed{e(X)=n\,e(Y)+2\rho-2-c.}
$$

These boxed formulas are **audit derivations from the visible equations**. They are not represented as additional recovered text beneath the occlusion. In particular, they establish the sign of the cusp term without reconstructing the hidden preceding formula. The intended convention for empty branch is $2\rho-2=0,\ c=0$, which gives the expected multiplicativity $e(X)=ne(Y)$.

### Checking each step

**1. Pencil topology and the normalization of the invariant.** Blow up the $m$ base points on $Y$. The resulting surface $\widehat Y$ is fibred over $\mathbb P^1$. A smooth fibre has Euler characteristic $2-2\pi$, and an ordinary node contributes one above the smooth-fibre Euler number. Additivity over the base therefore gives

$$
e(\widehat Y)=2(2-2\pi)+\delta.
$$

Blowing up adds one to $e$ per point, so $e(Y)=4-4\pi+\delta-m$. Thus the printed $i$ is indeed $e(Y)-4$. This also shows precisely why singular fibres must be counted by local contributions rather than simply by their number. The argument for $I$ is the same. The needed generic-pencil hypotheses are standard; the complete proof is the calculation just given, not a claim that the displayed page states all those hypotheses.

**2. Base points.** Each simple base point lies in the étale locus, so it has exactly $n$ preimages; hence $M=nm$. If a base point is placed on the branch or at a singularity, this count needs correction. The page tacitly works with a general pencil avoiding that situation.

**3. Genus of the inverse-image curve.** A general member meets $B$ transversely at $t$ smooth points, each contributing one simple ramification point to the curve cover. Riemann–Hurwitz is

$$
2\Pi-2=n(2\pi-2)+t,
$$

which gives exactly the printed formula. This is a valid application of the curve theorem; it is not a new unsupported surface theorem.

**4. Counting tangencies and the cusp subtraction.** The restriction of the pencil parameter to the normalization $\widetilde B$ is a degree-$t$ map to $\mathbb P^1$. Riemann–Hurwitz gives total ramification $2t+2\rho-2$. A general simple tangency at a smooth point of $B$ produces one ordinary node on the corresponding inverse-image pencil member. At an ordinary cusp the normalization parameter can be written $u\mapsto(u^2,u^3)$; a general linear pencil function has a simple ramification point there. It contributes to the ramification count on $\widetilde B$, but is not a smooth-branch tangency producing the extra node being counted. The absence of an extra node at a cusp can be checked directly in the ordinary three-sheet local model

$$
f(x,z)=(x,z^3+xz),\qquad B:\ (x,y)=(-3z^2,-2z^3).
$$

For a general pencil parameter $h(x,y)=\alpha x+\beta y+\cdots$, with $\alpha\ne0$, one has $d(h\circ f)_0=\alpha\,dx\ne0$, so its inverse-image member is smooth at the three-sheet point. On the normalized branch, however, $h=-3\alpha z^2-2\beta z^3+\cdots$ has one simple ramification point. A simple smooth-branch tangency has local pullback equation $a w^2+b v^2+\cdots=0$, with $ab\ne0$, and gives an ordinary node. At a branch node, the two disjoint simple-ramification charts each have a transverse pencil derivative and give no extra singularity. Thus subtract exactly one for each cusp. Each original Lefschetz node away from $B$ lifts to $n$ nodes. This proves $\Delta=n\delta+2t+2\rho-2-c$ and explains, rather than merely checks, its minus sign.

**5. Substitution.** The $2t$ in $\Delta$ cancels the $4(t/2)$ in $4\Pi$. Expanding the remaining terms gives exactly the final line of the page. The cancellation is an especially useful transcription check: a mistaken sign or factor in the genus term would leave a spurious dependence on the chosen pencil. The result is an invariant of the cover.

### Independent modern proof by stratification

There is also a short proof that does not choose a pencil. Let $b$ be the number of branch nodes. For an irreducible nodal-cuspidal branch curve,

$$
e(B)=2-2\rho-b.
$$

The cardinality of the geometric fibre of $f$ is $n$ off $B$, $n-1$ on the smooth branch locus, and $n-2$ at a node or cusp in the stated generic local models. Additivity of Euler characteristic gives

$$
\begin{aligned}
e(X)&=n(e(Y)-e(B))+(n-1)(e(B)-b-c)+(n-2)(b+c)\\
&=ne(Y)-e(B)-b-c\\
&=ne(Y)+2\rho-2-c.
\end{aligned}
$$

The branch-node contribution cancels; the cusp contribution remains. This independent calculation verifies the page's answer and identifies the assumptions under which it is true. For a disconnected normalization, replace $2-2\rho$ by the sum of the Euler characteristics of its components. Merely calling $\rho$ “the geometric genus” without specifying components would otherwise lose a constant.

The modern generic-plane-cover special case appears explicitly as equation (24), p. 138, in Kulikov and Kulikov (2010): $e(X)=3n+2(g-1)-c$. This is corroboration of the formula, not an attribution of a previously missing proof to those authors. Their equation specializes $e(Y)=3$; the proof above handles the more general base used in the supplied page.

Combining the verified Euler formula with Noether's formula gives the precise relation between the holomorphic Euler characteristics:

$$
12\bigl(\chi(\mathcal O_X)-n\chi(\mathcal O_Y)\bigr)
=K_X^2-nK_Y^2+2\rho-2-c.
$$

This is a modern consequence, not a reconstruction of the hidden paragraph about numerical genera. To express it in the book's notation one substitutes $\chi(\mathcal O_X)=P_a+1$, $\chi(\mathcal O_Y)=p_a+1$. If one also substitutes linear genera, they must refer to the same smooth models; minimalizing either side introduces the corresponding exceptional-curve corrections.

### What Enriques proves, assumes, and cites here

The visible passage **proves by a pencil calculation** the displayed expression for $I$, assuming the earlier definition and invariance of the Zeuthen–Segre number, curve Riemann–Hurwitz, genericity of the pencil, and the local meaning of cusps of the branch curve. The explanation of cusp subtraction is compressed but mathematically sound in this generic setting. No substantive sign or numerical error was found in the visible formulas. The main repair is to make the generic-cover hypotheses and the weighted singularity count explicit.

The visible footnotes cite Enriques, *Ricerche ecc.*, 1893, and Severi, *Sulle relazioni che legano i caratteri invarianti di due superficie algebriche*, 1903. The first is identifiable in the national edition catalogue as the 1893 monograph *Ricerche di geometria sulle superficie algebriche*, also published in the Turin academy memoirs in 1894. The second title is abbreviated in the book: Severi's bibliographic entry gives *Sulle relazioni che legano i caratteri invarianti di due superficie in corrispondenza algebrica*, *Rendiconti del Reale Istituto Lombardo*, series 2, volume 36, pp. 495–511. The original 1903 paper was not independently read in full for this audit; the expanded title and pagination are bibliographic verification only. Nothing in the invisible part of p. 186 is asserted on that basis.

### Audit examples and extensions

**Example A: the smooth sextic double plane (high confidence).** For the degree-two cover of $\mathbb P^2$ branched over a smooth sextic, $\rho=(6-1)(6-2)/2=10$ and $c=0$. The page's formula gives $e(X)=2\cdot3+20-2=24$. The double-cover formula gives $K_X\sim0$, $\chi(\mathcal O_X)=2$; Noether's formula gives the same 24. This checks the constant as well as the sign.

**Example B: the smooth quartic double plane (high confidence).** Here $\rho=3$, so $e(X)=6+6-2=10$. The cover has $K_X^2=2$ and $\chi(\mathcal O_X)=1$, again giving 10. Thus the relation is not confined to surfaces with numerically trivial canonical class.

**Example C: why “generic simple cover” cannot be dropped (high confidence).** A smooth cyclic triple cover branched over a smooth sextic has fibre cardinalities three off the branch and one on it. Therefore $e(X)=3e(\mathbb P^2)-2e(B)=9+36=45$. The simple-branch formula would incorrectly give 27. Independently, the cyclic-cover algebra is $\mathcal O\oplus\mathcal O(-2)\oplus\mathcal O(-4)$, giving $\chi=4$, and $K_X=\pi^*\mathcal O(1)$ gives $K_X^2=3$, hence $e=48-3=45$. This is an audit counterexample to an overgeneralization, **not** a counterexample to the page interpreted with its generic branching convention.

**Extension (high confidence, not claimed novel).** For a finite map stratified so that fibre cardinalities are constant on each stratum, the general relation is $e(X)=\sum_S \#f^{-1}(s)\,e(S)$. Ordinary nodes and cusps are the particular strata that reduce this expression to the printed formula. Higher branch singularities require their actual local fibre deficits; assigning all of them the cusp correction would be wrong. A useful further exercise is to calculate those deficits for specified local monodromy rather than guessing them from the singularity name alone.

### References for the supplement

Enriques, F. (1893). *Ricerche di geometria sulle superficie algebriche*. Clausen. National-edition bibliographic record, entries 1893_6 and 1894_6: https://www.federigoenriques.org/indice-cronologico-delle-opere/ . The 1894 academy version is listed as *Memorie della Reale Accademia delle Scienze di Torino*, series 2, 44, 171–232.

Kulikov, V. S., & Kulikov, Vik. S. (2010). On complete degenerations of surfaces with ordinary singularities in $\mathbb P^3$. *Sbornik: Mathematics, 201*(1), 129–158. https://doi.org/10.1070/SM2010v201n01ABEH004068 . Equation (24), p. 138. Author-hosted text: https://webhomes.maths.ed.ac.uk/cheltsov/kulikov/pdf/2010.pdf . The authors' abbreviated first names are retained to distinguish the two authors accurately.

Severi, F. (1903). Sulle relazioni che legano i caratteri invarianti di due superficie in corrispondenza algebrica. *Rendiconti del Reale Istituto Lombardo di Scienze e Lettere*, series 2, *36*, 495–511. Bibliographic identification: https://www.mat.uniroma3.it/users/sernesi/BIBLIOGRAFIA/severi.htm , entry 17. The original full text was not checked; the citation is not used to fill the occlusion.
