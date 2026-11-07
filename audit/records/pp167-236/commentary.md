# Mathematical commentary and verification: Enriques, *Le superficie algebriche* (1949)

## Introduzione: scope, conventions, and the modern mathematical dictionary

### What this commentary covers

The authority for the historical text is the supplied scanned PDF, checked against the supplied first-pass TeX transcription. The supplied PDF contains **71 image pages, of which 68 contain mathematical text and three are blank**. Its actual contents are Chapter V, §§1–14, nominal pp. 167–215 **with printed p. 186 absent**; Chapter VI, §§1–4, pp. 217–235; and the first page of Chapter VII, §1, inferred p. 237. The blank leaves occur before Chapter V, between Chapters V and VI, and between Chapters VI and VII. The chapter-opening pages have no printed page number: 167, 217, and 237 are positional identifications, with 167 also written by hand in the scan. Consequently, the filename “pp167–236” is not an exact description of the supplied content. Neither a scan nor a transcription of the book's historical *Introduzione* is included. The present section is the reviewer's introduction and mathematical dictionary; it does not pretend to audit an absent introductory chapter. A public online partial transcription of the book was located, but it covers earlier chapters and does not supply the missing p. 186. No wording or proof has been invented for that missing page.

The accompanying claim register records substantive definitions, conclusions, intermediate formulas, examples, and assumptions, including statements later qualified or corrected by Enriques himself. Its proof-status column describes what the **1949 excerpt** supplies, not whether the result has a modern proof. A claim marked “sketched” may be entirely correct. Conversely, “proved” records the presence of an argument and must be read together with the gap/error column. Historical attributions reproduced from Enriques's footnotes are distinguished from independently verified later literature. A source misprint means that the questionable reading is actually printed; the scan cannot establish whether author, editor, or compositor caused it.

### Ambient category and notation

Unless a paragraph explicitly says otherwise, modern statements concern a smooth, connected, projective surface \(S\) over \(\mathbb C\). Singular projective models are replaced by their normalization and, when necessary, a resolution. A finite map and a rational correspondence are not interchangeable: the latter may require blowups before a ramification formula applies. Generic projection formulas require the indicated ordinary singularities and transversality. Counts are intersection-theoretic, with multiplicities; they are literal counts of distinct objects only in the generic case.

| Enriques's expression | Modern meaning used here | Caution |
|---|---|---|
| Genere geometrico \(p_g\) | \(h^0(S,\omega_S)=h^2(S,\mathcal O_S)\) | Equality uses Serre duality. |
| Genere numerico / aritmetico \(p_a\) | \(\chi(\mathcal O_S)-1=p_g-q\) | This is not the arithmetic genus of an individual curve. It may be negative. |
| Irregolarità | \(q=h^1(S,\mathcal O_S)\) | Over \(\mathbb C\), \(q=h^0(S,\Omega_S^1)\) and \(b_1=2q\). |
| Superficie regolare | \(q=0\), hence \(p_a=p_g\) | It does not mean “nonsingular.” |
| \(P=P_2\), \(P_i\) | \(h^0(S,\omega_S^{\otimes2})\), \(h^0(S,\omega_S^{\otimes i})\) | A plurigenus is a vector-space dimension. |
| Dimension \(r\) of \(\vert D\vert \) | \(h^0(S,\mathcal O_S(D))-1\) | Distinguish projective dimension from number of sections. |
| Grado of a curve/system | Usually \(D^2\), or its moving self-intersection after resolving base points | “Ordine” in a fixed projective model usually means intersection with a hyperplane. These are different numbers. |
| Genere virtuale \(\pi\) of \(D\) | \(p_a(D)=1+(D^2+K_SD)/2\) | For a singular integral curve, geometric genus is smaller by the total \(\delta\)-invariant. For disconnected divisors, arithmetic genus may be negative. |
| Genere lineare relativo \(p^{(1)}\) | \(K_S^2+1\) | This quantity changes under blowup. |
| Genere lineare assoluto | \(K_{S_{\min}}^2+1\) for the nonruled minimal model in the applications here | Do not insert a minimal-model value into formulas on an uncontracted resolution. Rational/ruled models need separate specification. |
| \(p^{(2)}\) in VI §1 | \(K_S^2=p^{(1)}-1\) | This is **not** the bigenus \(P_2\). |
| Aggiunto / \(C^{(i)}\) | \(\vert C+K_S\vert \) / \(\vert C+iK_S\vert \), with careful treatment of fixed parts | Restriction to \(C\) and completeness require the relevant cohomology statement. |
| Curva eccezionale di prima specie | A smooth rational curve \(E\) with \(E^2=-1\) | A \((-2)\)-curve has a different contraction and discrepancy. |
| Curva canonica d'ordine zero | The zero effective divisor in \(\vert K\vert \), hence \(K\sim0\) | Numerical triviality alone does not imply linear triviality. |
| Curva bicanonica d'ordine zero, \(p_g=0\) | \(2K\sim0\) and \(K\not\sim0\) | This is exactly where cancelling a factor 2 in linear equivalence is dangerous. |
| Piano \(n\)-plo / involuzione d'ordine \(n\) | A degree-\(n\) finite cover of a plane, or its birational model | “Involuzione” need not mean a group action of order two. |
| Curva di coincidenza / diramazione | Ramification upstairs / branch divisor downstairs | The source occasionally changes letters; these must not be confused. |

The definitions and intersection identities are standard in Beauville (1978, Chapter I, Theorems I.11–I.12 and §§I.14–I.17, and Chapter II) and Reid (1996, §§A.10–A.12, B.9). We use their terminology, while deriving the particular comparisons below directly. The distinction between numerical and linear equivalence is indispensable: a nontrivial torsion line bundle is numerically trivial, and \(2D\sim2E\) does not generally imply \(D\sim E\).

### A common proof framework for the chapter-by-chapter audit

**Adjunction and arithmetic genus.** If \(D\) is an effective Cartier divisor on a smooth surface, the adjunction isomorphism is \(\omega_D\simeq(\omega_S\otimes\mathcal O_S(D))|_D\). The dualizing sheaf, rather than ordinary differentials on a singular curve, is the correct object. It yields

\[
2p_a(D)-2=D(D+K_S).
\]

For \(D=A+B\), bilinearity gives

\[
p_a(A+B)=p_a(A)+p_a(B)+A B-1.
\]

Thus a union of \(n\) disjoint genus-\(g\) fibres has arithmetic genus \(ng-n+1\), precisely the convention required on p. 173. For a reduced integral curve with normalization \(\nu:\widetilde D\to D\), the exact sequence \(0\to\mathcal O_D\to\nu_*\mathcal O_{\widetilde D}\to Q\to0\) gives \(p_a(D)=g(\widetilde D)+\operatorname{length}Q\). Nodes and ordinary cusps each contribute one; an ordinary \(r\)-fold point contributes \(r(r-1)/2\). These local corrections to genus should not be confused with their contributions to the discriminant of a pencil.

**Surface Riemann–Roch and duality.** For any divisor \(D\),

\[
\chi(\mathcal O_S(D))=\chi(\mathcal O_S)+\tfrac12D(D-K_S),\qquad
h^2(D)=h^0(K_S-D).
\]

A proof of the numerical formula can be reduced to Riemann–Roch on curves: the exact sequence \(0\to\mathcal O_S(D-C)\to\mathcal O_S(D)\to\mathcal O_C(D)\to0\), for a smooth very ample \(C\), gives the difference \(DC+1-g(C)\); adjunction makes this equal to the difference of the proposed quadratic polynomials. Write an arbitrary \(D\) as the difference of two sufficiently positive smooth divisors and apply the same calculation twice. This also explains why an inequality for \(h^0\) is automatic but equality requires control of \(h^1\) and \(h^2\). A verified modern presentation is Brosnan's Theorem 3.4, which identifies Hartshorne's corresponding result as Theorem V.1.6. The proof here uses the exact sequences with consistent notation, not the minor letter inconsistencies in that online transcription.

**Noether's formula.** The degree-two part of the Todd class is \((c_1(T_S)^2+c_2(T_S))/12\). Hirzebruch–Riemann–Roch for \(\mathcal O_S\), together with complex Gauss–Bonnet, gives

\[
12\chi(\mathcal O_S)=K_S^2+c_2(S)=K_S^2+e(S).
\]

This is a derivation from explicitly named general theorems, not a proof of those theorems from first principles. It is exactly the modern identity behind Enriques's \(I+p^{(1)}=12p_a+9\), because \(I=e(S)-4\). The constant shifts are checked rather than suppressed.

**Blowing up and resolving a pencil.** For \(\sigma:\widetilde S\to S\), the blowup of a smooth point with exceptional curve \(E\),

\[
K_{\widetilde S}=\sigma^*K_S+E,\quad E^2=-1,\quad
K_{\widetilde S}^2=K_S^2-1,\quad e(\widetilde S)=e(S)+1.
\]

The canonical formula follows in local coordinates from \(dx\wedge d(xv)=x\,dx\wedge dv\). The topological formula replaces a point by \(\mathbb P^1\). The direct-image identities \(\sigma_*\mathcal O_{\widetilde S}=\mathcal O_S\), \(R^1\sigma_*\mathcal O_{\widetilde S}=0\), and extension of pluricanonical forms across a point give birational invariance of \(p_g,q,\chi\), and all \(P_m\). For a curve of multiplicity \(a\) at the centre, \(\widetilde D=\sigma^*D-aE\), \(\widetilde D^2=D^2-a^2\), and \(p_a(\widetilde D)=p_a(D)-a(a-1)/2\). Infinitely near points are treated successively, using total transforms as the diagonal intersection basis. The linear, rather than quadratic, correction to \(K_SD\) derived from these formulas is relevant to p. 205.

**Two different completeness questions.** On a fixed regular smooth surface, \(0\to\mathcal O_S\to\mathcal O_S(C)\to\mathcal O_C(C)\to0\) and \(H^1(\mathcal O_S)=0\) prove that the characteristic series of a complete linear system restricts completely to a smooth member. Likewise, \(0\to\omega_S\to\omega_S(C)\to\omega_C\to0\) and \(H^1(\omega_S)=H^1(\mathcal O_S)^*=0\) prove completeness of the adjoint series. These facts justify several steps in Chapter VI. They do **not** prove that every first-order deformation preserving nodes and cusps integrates to a family. The latter is Enriques's distinct working hypothesis in V §12; modern obstruction theory and counterexamples are discussed there. Conflating the two questions would incorrectly condemn valid arguments in Chapter VI and incorrectly validate a conjecture in Chapter V.

### Reading the corrections and the historical record

The correction register keeps the original reading and the observed scan reading separate from any mathematical emendation. For a printed mathematical error the “scan reading” remains the erroneous printed formula; the evidence field supplies the derivation of the proposed correction. The doubtful markers are accounted for individually, including punctuation and typeface uncertainties with no mathematical effect. Where damaged print prevents a unique palaeographic decision, the entry records a preferred reading and its limit rather than treating mathematical plausibility as visual proof.

The modern proofs are replacements or clarifications unless a verified source explicitly attributes a historical repair. For example, the text itself attributes the criticism of its earlier moduli argument to Zariski (1935); Catanese (2013, §1.3) expressly connects the modern moduli lower bound with Kuranishi. Neither statement justifies crediting Zariski or Kuranishi with correcting a particular typographic error on p. 175. The same discipline applies to Kodaira, Mumford, and Bombieri–Mumford: their theories provide modern foundations or positive-characteristic extensions, not a license to assign unverified historical priority.

The subsequent commentary follows the complete supplied chapter sequence. Formula repairs, hypotheses, and examples are included at their relevant pages; the CSV supplies a more granular index. The method file gives the exact page map, validation procedures, and unresolved limits.

## Chapter V. Numerical invariants and multiple planes (pp. 167–215)

### Conventions and the scope of this chapter

The ground field in the statements below is **the complex numbers**. Let $S$ be a smooth projective model of Enriques's surface, $K=K_S$, $q=h^1(S,\mathcal O_S)$, $p_g=h^0(S,K)$, $p_a=\chi(\mathcal O_S)-1=p_g-q$, and $\lambda=p^{(1)}=K^2+1$. The last equality concerns the chosen model; it is not a birational invariant before exceptional curves have been contracted. The Euler characteristic $e$ is the topological Euler characteristic. A general member $H$ of the linear systems being considered has $H^2=n$ and genus $\pi$, so that $KH=2\pi-2-n$. Enriques reuses $n,d,k,P,\chi$ for different objects; each subsection below restates their meaning. In particular his $\chi$ sometimes counts cusps and is **not** $\chi(\mathcal O_S)$.

The supplied text jumps from p. 185 to p. 187. No assertion is attributed here to the missing p. 186. Identities needed to bridge that break are explicitly derived as modern reconstructions. The historical Introduction is not present in this chapter's source.

The register supplies individual rows for the definitions, formulas, intermediate identities, and qualitative claims. The discussion below supplies the proofs and qualifications behind those rows. “Proved” describes what Enriques supplies in the available text; it does not by itself certify that every unstated general-position assumption has been supplied.

### V.1. The Zeuthen–Segre invariant (pp. 167–172)

**Exact modern statement.** Resolve the base scheme of a pencil on $S$ by $b$ point blowups, producing $f:\widetilde S\to\mathbf P^1$ with smooth connected generic fiber $F$ of genus $g$. For every singular fiber define

\[
\Delta_t=e((F_t)_{\mathrm{red}})-(2-2g).
\]

Then

\[
I(S):=e(S)-4=\sum_t\Delta_t-b-4g. \tag{V.1.1}
\]

For a Lefschetz pencil with distinct simple base points and one node in each singular fiber, $b=n$ and every $\Delta_t=1$; this is precisely $I=\delta-n-4\pi$ on p. 167. “Relative invariant” means that $I$ belongs to a smooth model and changes under blowup. It does not mean a new birational invariant. The introductory claim that it is expressible using $p_a,p^{(1)}$ is proved later, not here.

**Enriques's argument.** On pp. 168–169 he reproduces Segre's comparison of two pencils. Put $s=C_1C_2$, let $L$ be their tangency locus, and use the normalizations whenever needed. A general $C_i$ meets $L$, outside its own base points, in the ramification divisor of the map to the other pencil; Riemann–Hurwitz gives degree $2s+2\pi_i-2$. The two induced maps $L\to\mathbf P^1$ therefore have total ramification

\[
4s+4(\pi_1-1)+2g(L)-2=\delta_1+\tau+n_2,
\]
\[
4s+4(\pi_2-1)+2g(L)-2=\delta_2+\tau+n_1.
\]

Here $\tau$ counts the common third-order tangencies. The terms are justified individually: nodal members of the first pencil, the common third-order contacts, and the base points of the other pencil. Subtraction cancels both $g(L)$ and $\tau$. This is a genuine proof for general pencils, not a bare appeal to birational intuition. Enriques cites Zeuthen (1871) for the original character and C. Segre (1896) for this comparison.

The argument needs the stated generic relative position, simple ramification in the auxiliary maps, and correct multiplicities at nongeneric contacts. It is not a proof that an unweighted count of singular members is invariant for every pencil. The “continuity” passage concerning infinitely near bases on p. 169 is a sketch; resolving the pencil and using (V.1.1) makes its content precise. The number of blowups is not the scheme length $\sum m_i^2$ of a multiple base scheme. Enriques's convention for “effective” and infinitely near bases must be followed together with his corrections to $\delta$, rather than extracting $n$ alone and treating it as $H^2$.

**Modern proof.** Outside finitely many critical values the map is a differentiable fiber bundle. Additivity of Euler characteristic gives

\[
e(\widetilde S)=2(2-2g)+\sum_t\Delta_t.
\]

Every point blowup increases $e$ by one; substitution proves (V.1.1). For an isolated reduced plane-curve singularity the local contribution is its Milnor number. An ordinary $r$-fold point has $r$ smooth transverse branches and

\[
\mu=2\delta_{\rm loc}-r+1=r(r-1)-r+1=(r-1)^2.
\]

This proves the multiplicity asserted on p. 169. The adjective “ordinary,” or equivalently the generic transversal-branch assumption expressed by Enriques's “in generale,” matters: a cusp and a node are both double points but have different Milnor numbers. An arbitrary multiplicity-$r$ point need not have contribution $(r-1)^2$.

**Nonreduced and reducible fibers.** For a fiber $F_0=\sum_i m_iD_i$ whose reduced components are smooth and meet transversely, with no triple intersections, write $g_i=g(D_i)$, $a_{ij}=D_iD_j$, and sum over unordered pairs $i<j$. Enriques's Godeaux formula is

\[
\Delta_0=\sum_i(m_i-1)(2g_i-2)
 +\sum_{i<j}a_{ij}(m_i+m_j-1). \tag{V.1.2}
\]

It includes $2\chi+\psi$, for which the contribution is $2g(\chi)-2+2i$, and $h\chi+\psi$, for which it is $(h-1)(2g(\chi)-2)+hi$, provided the residual intersections and components satisfy the same assumptions. These are weighted Euler defects, not literal counts of distinct singular fibers.

Here is a proof not requiring a deformation to nodal fibers. The fiber equations $F_0D_i=0$, adjunction, and $KF_0=2g-2$ give

\[
2g-2=\sum_i m_i(2g_i-2)+\sum_{i<j}(m_i+m_j)a_{ij}.
\]

On the other hand $e((F_0)_{\rm red})=\sum_i(2-2g_i)-\sum_{i<j}a_{ij}$. Subtracting $2-2g$ gives (V.1.2). Enriques provides the two-pencil calculation for a double component on pp. 170–171, sketches the extension to multiplicity $h$, and cites Godeaux (1920; 1934) and Campedelli (1934) for the general formula. His residual-intersection count on p. 170 must be $C_2L_1$, not $C_2L$; the scan preserves the latter, which is a source slip.

For a node on $D_i$, use either its geometric genus and add $2m_i-1$, or its arithmetic genus and add one. These two rules agree because a node lowers geometric genus by one. For more general singularities one must use the local delta invariant and the number of branches; one must not extend the “add one” rule to all double points. A convenient generalization, derived here, is the correction $2m_i\delta_p-(r_p-1)$ when the component's geometric genus is used. Blowups first reduce more complicated intersections and base clusters to a configuration where the same Euler-characteristic calculation applies.

### V.2. Irrational pencils (pp. 172–173)

For a fibration $f:S\to B$ over a smooth curve of genus $b$, with connected generic fiber genus $g$, the exact formula is

\[
e(S)=4(b-1)(g-1)+\sum_t\Delta_t,
\qquad
I(S)=\sum_t\Delta_t+4(b-1)(g-1)-4. \tag{V.2.1}
\]

This follows from the same Euler-characteristic proof. Enriques alternatively composes $f$ with a simply branched degree-$a$ map $B\to\mathbf P^1$. Such a map can be obtained from a sufficiently ample pencil; his suggested degree $b+1$ follows from the existence of suitable divisors on a curve. The generic fiber of the composite is a disjoint union of $a$ fibers of $f$, and its **arithmetic** genus is

\[
\Pi=ag-a+1.
\]

It may be disconnected, so this expression must not be called the genus of a connected Riemann surface. The $2a+2b-2$ simple ramification points of $B\to\mathbf P^1$ produce fibers containing a double component; each has defect $2g-2$. Thus

\[
I=\Delta+(2g-2)(2a+2b-2)-4(ag-a+1),
\]

which simplifies to (V.2.1). On p. 173 the printed first factor is $\pi-2$, whereas both the preceding sentence and the simplification require $2\pi-2$. This is a genuine source misprint, not a failure of the theorem.

### V.3. Noether's formula and ordinary projections (pp. 173–177)

**Blowup and intrinsic formula.** A blowup changes $I$ by $+1$ and $\lambda=K^2+1$ by $-1$. Hence $I+\lambda$ is birationally invariant. Noether's formula is

\[
K^2+c_2(S)=12\chi(\mathcal O_S),
\qquad I+\lambda=12p_a+9. \tag{V.3.1}
\]

The modern proof is Hirzebruch–Riemann–Roch applied to $\mathcal O_S$: the degree-two Todd term is $(c_1^2+c_2)/12$; $c_1(T_S)^2=K^2$, and Chern–Gauss–Bonnet identifies $c_2$ with $e(S)$. The same expansion applied to $\mathcal O_S(D)$ yields

\[
\chi(\mathcal O_S(D))=\chi(\mathcal O_S)+\tfrac12D(D-K).
\]

This explains exactly what the historical arithmetic genus measures. It does not replace $p_a$ by $p_g$ on irregular surfaces.

**What the text proves.** Enriques gives a classical elimination argument attributed to Bonnesen (1906), after assuming an ordinary projection to a degree-$n$ surface in $\mathbf P^3$, with an irreducible ordinary double curve of degree $d$, normalization genus $\rho$, ordinary triple points $t$, and pinch points $\tau$. Let $\Delta\subset S$ be the conductor curve, $\Pi$ its normalization genus, $H$ a hyperplane section of genus $\pi$, and $J=3H+K$ the ramification curve of a general projection to the plane. The seven relations being used are

\[
\begin{aligned}
I&=\delta-n-4\pi,\\
\delta+\tau&=3n+12(\pi-1)+\lambda-1,\\
d&=\tfrac12(n-1)(n-2)-\pi,\\
2(\Pi+3t)-2&=2(n-4)d,\\
2\Pi-2&=2(2\rho-2)+\tau,\\
2n^2-7n+15+2\pi(n-7)-\lambda-\tau&=(n-2)d-3t,\\
p_a&=\binom{n-1}{3}-(n-4)d+2t+\rho-1.
\end{aligned} \tag{V.3.2}
\]

The first is the pencil formula. The second is $J^2-\tau=\delta$. The third is the plane-section genus formula. The fourth uses $\Delta+K\sim(n-4)H$, $H\Delta=2d$, and adjunction, since $p_a(\Delta)=\Pi+3t$. The fifth is Riemann–Hurwitz for the double covering of the normalized double curve. For the sixth, $J\Delta=(n-2)d-3t+\tau$, obtained by the second polar, while direct intersection gives

\[
J\Delta=(3H+K)((n-4)H-K)
=2n^2-7n+15+2\pi(n-7)-\lambda.
\]

The seventh can be made precise through the conductor exact sequence. Locally at an ordinary triple point the double curve has three spatial branches and delta invariant two; its arithmetic genus is $\rho+2t$. The conductor curve has three ordinary nodes over each such point, so its arithmetic genus is $\Pi+3t$. The conductor sequence gives $\chi(\mathcal O_S)=\chi(\mathcal O_F)+\chi(\mathcal O_\Delta)-\chi(\mathcal O_D)$. Inserting these genera and the fourth equation yields exactly the final equation of (V.3.2). Thus the triple-point corrections have a specific algebraic explanation.

The scan on p. 175 genuinely omits $-\lambda$ from the displayed expansion of $J\Delta$. Its subsequent equation (6) genuinely prints $2n^2+n+14+2\pi(n-7)-\lambda=(n-2)d-3t$. That expression is inconsistent with the immediately preceding calculations. The sixth line of (V.3.2) is the correction; these are source errors, not transcription errors. The cross-reference for $d$ should be equation (3), not (2). The “seven characters” list on p. 176 omits $d$.

Solving the corrected equations gives

\[
\begin{aligned}
\delta&=n+4\pi-\lambda+12p_a+9,\\
\rho&=\tfrac12(n^2-7n+48)+(n-12)\pi+9p_a-2\lambda,\\
\Pi&=n^2-6n+2(n-10)\pi+12p_a-3\lambda+36,\\
t&=\tfrac16(n^3-9n^2+26n-78)-(n-8)\pi-4p_a+\lambda,\\
\tau&=2n+8\pi-12p_a+2\lambda-22.
\end{aligned} \tag{V.3.3}
\]

These are the five formulas printed on p. 176; they agree with the corrected system, not with the erroneous equation (6). Consequently $I=12p_a-\lambda+9$, $2n+8\pi-\tau=12p_a-2\lambda+22$, and $2\delta-\tau=36p_a-4\lambda+40$. The last two are relative invariants of the surface expressed using a generic three-dimensional system. Their geometric counting interpretations require the ordinary-projection assumptions. They are not additional independent Chern numbers.

**Examples on p. 177.** A general conic pencil on $\mathbf P^2$ has four base points, genus zero, and three nodal reducible members; hence $I=-1$, $p_a=0$, and $\lambda=10$, consistently with $K^2=9$. A relatively minimal ruled surface over a genus-$b$ curve has $e=4-4b$, $I=-4b$, $p_a=-b$, and $\lambda=9-8b$. “Absolute linear genus” for rational surfaces requires particular care: different minimal rational models need not have the same $K^2$. The numerical calculations here are for the specified plane or ruled model.

### V.4. Cuspidal members of a net (pp. 177–179)

For a sufficiently general net in a sufficiently ample linear system $H$, whose singular members have the expected stable singularities, the number of cuspidal members is

\[
i=24(p_a+\pi)=24\chi(\mathcal O_S)+12H(H+K). \tag{V.4.1}
\]

Enriques works on the ordinary projected surface. Its parabolic curve has class $P=8H+4K$, and the cusp count is $JP-2\tau$, because each pinch point contributes two to that intersection. Expanding,

\[
JP=24n+20(2\pi-2-n)+4\lambda-4,
\]

and substituting the last formula in (V.3.3) proves (V.4.1). The Hessian has degree $4n-8$, and subtracting its fourfold double-curve contribution gives $P\sim4K+8H$. The footnote gives a second route: the Jacobian of the polar net is $J_2=P+H$, whereas its class is $3J+K=9H+4K$.

The intermediate sentence on p. 178 is too broad if read as a statement about an arbitrary isolated biplanar double point: its Hessian need not have order four. For example, the homogeneous cubic $F=uxy+z^3$ has Hessian determinant $12uxyz$, of local order three at $[0:0:0:1]$. The calculation must retain the surrounding assumption that the point lies on an ordinary double **curve**. This is a missing local hypothesis, not a counterexample to (V.4.1). The prime attached to one $F$ in the first-pass Hessian transcription is not a different function; the matrix is the symmetric matrix of second derivatives of one polynomial.

Enriques proves the formula for nets embedded in a three-dimensional system, and only sketches extension by adjoining an auxiliary fixed component. A modern intrinsic formulation is the universal $A_2$-locus calculation for the first jets of sections: its degree is $12H^2+12HK+2K^2+2c_2$, which equals (V.4.1) by Noether. Here is the intrinsic calculation explicitly. On $S\times\mathbf P^2$, the universal first jet of $H$ cuts the incidence curve $Z$ of singular members. With $h=c_1(\mathcal O_{\mathbf P^2}(1))$,
\[
[Z]=c_3(J^1H\otimes\mathcal O(1))
=c_1(J^1H)h^2+c_2(J^1H)h,
\]
where $c_1(J^1H)=K+3H$ and $c_2(J^1H)=c_2(S)+2KH+3H^2$. On $Z$, degeneracy of the Hessian is a section of the line bundle of class $2K+2H+2h$. Its degree is
\[
2(K+3H)(K+H)+2(c_2+2KH+3H^2)
=2K^2+12KH+12H^2+2c_2.
\]
For a generic transverse incidence problem, these are precisely the ordinary cuspidal members; Noether gives (V.4.1). This supplies the calculation rather than merely naming a universal formula.

The general-position condition is essential. A deliberately special net, a net composed with a pencil, or a non-simple cover does not have this literal unweighted cusp count.

### V.5. Historical note (p. 180)

This section supplies historical attributions, not a new proof. Enriques credits Zeuthen (1871) with $i-24\pi=24p_a$, notes that the early birational-invariance argument had restrictions on surface singularities, and credits Severi (1902) with a direct comparison of nets. Bonnesen (1906), Pannelli (1905), and Caporali are cited for forms of the proof used here. The discussion of Painlevé–Castelnuovo concerns the curve correspondence formula, and the discussion of Severi's equivalence systems concerns an attempted higher-dimensional analogue of divisor linear series. It should not be silently translated into a proved equivalence between every such historical construction and modern Chow groups. The source's bibliographic entries are reproduced in the historical-reference ledger; where originals were not consulted, that fact is retained.

### V.6. Numerical characters of a net and its branch curve (pp. 180–182)

Let $f:S\to\mathbf P^2$ be the finite morphism defined by a generic base-point-free net in $H$, of degree $n=H^2$, and suppose it is simply ramified along a smooth ramification curve $R\sim K+3H$. Assume the branch curve $B$ has only ordinary nodes and cusps and $R\to B$ is its normalization. Write $N=\deg B$, $P=g(R)$, $\delta=\deg B^\vee$, $k=\#\text{cusps}(B)$, $d=\#\text{nodes}(B)$, $i=\#\text{ordinary flexes}(B)$, and $t=\#\text{ordinary bitangents}(B)$. Then the seven formulas are

\[
\begin{aligned}
N&=2n+2\pi-2,\\
P&=\lambda+9\pi-9,\\
\delta&=n+4\pi+12p_a-\lambda+9,\\
k&=3(n+6\pi+\lambda-4p_a-11),\\
i&=24(\pi+p_a),\\
d&=2[(n+\pi)^2-5n-17\pi-2\lambda+6p_a+24],\\
t&=\tfrac12[(n+4\pi+12p_a-\lambda)^2+15n-6\pi+132p_a-17\lambda+74].
\end{aligned} \tag{V.6.1}
\]

These have all been checked algebraically. The first is $HR$. The second is adjunction for $R$. The third is the pencil invariant. The fourth and sixth follow by eliminating $d,k$ from

\[
P=\tfrac12(N-1)(N-2)-d-k,
\qquad \delta=N(N-1)-2d-3k.
\]

The fifth is (V.4.1), equivalently the Plücker flex formula $i=3N(N-2)-6d-8k$. The last is the genus formula for the dual curve, $t=\tfrac12(\delta-1)(\delta-2)-P-i$. Enriques states these eliminations without writing each line. No numerical inconsistency was found in (V.6.1).

The geometric dictionary is substantive: a triple contact in the net is a cusp of $B$; a cuspidal member is a flex tangent to $B$; a two-point tangency in the net gives a node of $B$; and a two-nodal member gives a bitangent of $B$. These identifications use stable local models and do not extend unchanged to more singular projections.

Conversely,

\[
\lambda=P-9\pi+9,\quad
p_a=i/24-\pi,\quad
4p_a=n+P-3\pi-k/3-2,\quad
\pi=N/2-n+1.
\]

In the concluding observation the printed $3(n+6\pi-k)$ must be $3(n+6\pi)-k$. Its constancy follows from the fourth equation, whereas the printed expression does not. The second invariant $24\pi-i=-24p_a$ is correctly printed. These branch-curve formulas describe a general net, not every base-point-free net solely on the strength of its being base-point-free; the repeated “in generale” is mathematically necessary.


### V.7. Finite correspondences and double planes (pp. 183–185)

**Canonical divisor formula.** For a finite generically separable map $f:X\to Y$ of smooth surfaces,

\[
K_X=f^*K_Y+R_f, \tag{V.7.1}
\]

where $R_f$ is the divisor of the determinant of $df$. At a simple ramification point the local model $(u,v)\mapsto(u,v^2)$ gives coefficient one. More generally, a tame ramification index $e$ gives coefficient $e-1$. In (V.7.1), $R_f$ is the ramification divisor, not the whole pullback of the branch divisor: for a general cover $f^*B$ also contains unramified components. Enriques proves the formula by comparing Jacobians of corresponding nets. That is a valid divisor calculation in the finite, separable situation he assumes.

For a generically finite map with exceptional curves, his instruction to add a “fundamental curve” needs the correct discrepancy multiplicities. A single blowup adds its exceptional divisor with coefficient one; a succession of infinitely near blowups can give larger coefficients when expressed on the final model. Thus the one-curve phrase on p. 183 is not a general coefficient-free formula for arbitrary birational correspondences. Resolve the map and apply (V.7.1) and the blowup formula at each stage.

**Double-cover reconstruction.** A flat double cover is specified by a line bundle $L$ on $Y$ and a branch section of $L^{\otimes2}$. Its algebra is

\[
f_*\mathcal O_X=\mathcal O_Y\oplus L^{-1},\qquad
K_X=f^*(K_Y+L).
\]

Projection formula therefore gives the complete plurigenus decomposition

\[
H^0(X,mK_X)=
H^0(Y,mK_Y+mL)\oplus H^0(Y,mK_Y+(m-1)L). \tag{V.7.2}
\]

This is the precise modern explanation of the two projective fixed eigenspaces of the involution described on p. 184. For a smooth branch curve of degree $2n$ on $\mathbf P^2$, put $L=\mathcal O_{\mathbf P^2}(n)$. Then

\[
H^0(X,mK_X)=H^0(\mathbf P^2,\mathcal O(m(n-3)))
\oplus H^0(\mathbf P^2,\mathcal O(m(n-3)-n)).
\]

For $m=1$ the second summand vanishes, so canonical forms correspond to plane curves of degree $n-3$. For $m=2$, the eigenspaces are the degree-$2n-6$ and degree-$n-6$ systems. A section in the second summand is multiplied by the square-root coordinate; its zero divisor contains the ramification curve. This explains why the whole bicanonical system is invariant under the involution while its general member need not descend to the plane. If the two projective eigenspaces have dimensions $r$ and $t$, then $P_2=r+t+2$, not $r+t+1$; Enriques correctly writes $P_2-1=r+t+1$. His $\pi=t+1$ gives $P_2=r+\pi+1$. Empty eigenspaces are allowed and have projective dimension $-1$.

The text permits singular branch curves, importing their multiplicity conventions from Chapter III §7. Those conventions are outside this excerpt. One cannot apply the smooth degree formulas without resolving the branch singularities. A canonical-resolution step at a point of branch multiplicity $m$ replaces

\[
L\ \text{by}\ L'=\sigma^*L-\lfloor m/2\rfloor E,\qquad
B\ \text{by}\ B'=\sigma^*B-2\lfloor m/2\rfloor E.
\]

The exceptional divisor belongs to $B'$ when $m$ is odd. Then
$K_{Y'}+L'=\sigma^*(K_Y+L)+(1-\lfloor m/2\rfloor)E$.
Iterating this construction gives the adjoint vanishing conditions and the actual plurigenera. This is a modern repair of the *missing imported machinery*, not a claim that Enriques invented an incorrect double-cover formula.

The tricanonical and further “adjoint plus branch” constructions are instances of (V.7.2); they do not say that every pluricanonical curve belongs to the invariant eigenspace. The final rational/ruled assertion on p. 185 imports the Castelnuovo–Enriques classification of plane curves with vanishing successive adjoints (1900), cited through Enriques–Conforto §27, p. 489. Enriques does not prove that classification here. The three normal forms he explicitly lists are a degree-$2n$ curve with a $(2n-2)$-fold point, a quartic, and a sextic with two infinitely near triple points, together with specializations of these. These are imported Cremona/adjoint classification statements, not three cases derived in the present pages. Over $\mathbf C$, a surface whose plurigenera all vanish has Kodaira dimension $-\infty$ and is birationally ruled. In the double-plane case the nonrational base must admit a degree-two map to $\mathbf P^1$, explaining “hyperelliptic ruled” in the historical statement. This implication belongs to surface classification; it does not follow merely by setting a few polynomial degree counts equal to zero.

### V.8. Numerical formulas for finite maps; Kummer and Enriques covers (pp. 185, 187–192)

Let $f:X\to Y$ have degree $n$, simple branch curve $B$, smooth ramification curve $R$ mapping birationally to $B$, and no contracted curves. Let $\rho=g(R)$, $s=K_YB$, $\nu=B^2$, $\varepsilon$ be the number of nodes of $B$, and $c$ its number of ordinary cusps. Write $(p_a,\lambda)$ for $Y$ and $(P_a,\Lambda)$ for $X$. Pullback of holomorphic two-forms gives $p_g(X)\ge p_g(Y)$, since the map is dominant and separable. Riemann–Hurwitz on the pullback of a canonical divisor, followed by the genus-addition formula, yields

\[
\Lambda=n(\lambda-1)+\rho+\frac32s. \tag{V.8.1}
\]

The term $s$ can be negative because a canonical divisor may be virtual; the polynomial identity remains an intersection-theoretic statement. The source switches between $D$ and $d$ for the branch curve on p. 185; the notation $B$ downstairs and $R$ upstairs used here removes that local ambiguity.

**Reconstruction across the missing page.** Stratify $Y$ by the complement of $B$, its smooth locus, nodes, and cusps. The respective fiber cardinalities are $n,n-1,n-2,n-2$. Since the normalization of $B$ has Euler characteristic $2-2\rho$ and every node identifies two preimages,

\[
e(X)=ne(Y)+2\rho-2-c. \tag{V.8.2}
\]

This is supplied here as an independent derivation, not a quotation from the absent p. 186. Combining (V.8.1), (V.8.2), and Noether gives the displayed p. 187 formula

\[
24(P_a+1)=24n(p_a+1)+6\rho-6+3s-2c. \tag{V.8.3}
\]

Adjunction on the singular branch curve gives
$s=2(\rho+\varepsilon+c)-2-\nu$. Therefore

\[
\begin{aligned}
\Lambda&=n(\lambda-1)+4\rho+3(\varepsilon+c)-\tfrac32\nu-3,\\
24(P_a+1)&=24n(p_a+1)+12\rho-12+6\varepsilon+4c-3\nu.
\end{aligned} \tag{V.8.4}
\]

The printed second formula on p. 187 ends in $-3$; it must end in $-3\nu$. This is confirmed by the substitution, by the next page's $-3N^2$, and by the double-cover examples. If $R^2=x$, comparison of $K_X^2=(f^*K_Y+R)^2$ with (V.8.1) gives

\[
x=\nu/2-(\varepsilon+c).
\]

For a smooth branch component in a double cover, this reduces to $R^2=B^2/2$, also directly from $f^*B=2R$ and $(f^*B)^2=2B^2$. With no branch divisor, the conventional $\rho=1$ makes the terms $2\rho-2$ vanish; it does not mean that an actual elliptic branch curve exists. For disconnected branch divisors, $\rho$ must similarly be interpreted by $2-2\rho=e(\widetilde B)$, not as a positive genus.

Putting $Y=\mathbf P^2$, $\lambda=10$, $p_a=0$, $\nu=N^2$, $\rho=P$, $\varepsilon=d$, and $c=k$ recovers the two inverse formulas in V.6. Enriques performs these substitutions explicitly on p. 188. This is a useful consistency check on the conventions and the factor $24$.

**The Kummer example (pp. 188–190).** Enriques assumes the classical $16_6$ configuration of nodes and trope planes of a Kummer quartic; its proof is referred to Enriques–Chisini, Book VI §40, vol. IV, p. 246. He chooses a tetrahedron whose four vertices and remaining twelve nodes give odd vanishing orders for its defining product. On the smooth Kummer resolution $Y$, its double cover is branched along the sixteen disjoint exceptional $(-2)$-curves $E_i$. Thus

\[
B=\sum_{i=1}^{16}E_i,\quad B^2=-32,\quad
\rho=1-16=-15,\quad \varepsilon=c=0.
\]

A generic quartic hyperplane section has genus three; its unramified degree-two inverse image has genus five and self-intersection eight, exactly the $8=2\cdot5-2$ calculation on p. 189. The cover $\widetilde X$ consequently has $K_{\widetilde X}^2=-16$ and $\Lambda=-15$. This is not a contradiction with the asserted minimal value $\Lambda=1$: above each $E_i$ lies a $(-1)$-curve, and contracting all sixteen increases $K^2$ by sixteen. Equation (V.8.3) gives $\chi(\mathcal O_X)=0$, hence $P_a=-1$. The constructed minimal surface has trivial canonical bundle, $p_g=1$, $q=2$, and every $P_m=1$. In modern terminology it is an abelian surface (the Jacobian in the genus-two construction), whereas Enriques's “hyperelliptic surface” here uses an older, broader vocabulary.

One can verify the holomorphic Euler characteristic independently from the double-cover formula

\[
\chi(\mathcal O_{\widetilde X})
=2\chi(\mathcal O_Y)+\tfrac12 L(L+K_Y)
=4+\tfrac12(-8)=0,\qquad 2L\sim B.
\]

Since $K_Y=0$, $K_{\widetilde X}=f^*L$ is supported on the sixteen exceptional curves, and it disappears after contraction. The symmetric square of a genus-two curve is **birational** to its Jacobian, not isomorphic to it: the Abel map contracts the curve coming from the hyperelliptic pencil. Enriques says “equivale,” so the source should not be accused of asserting an isomorphism. More specifically, for a degree-four class $L$ with complete series $g^2_4$, the involution on degree-two divisor classes is $D\mapsto L-D$. Its fixed classes satisfy $2D=L$; multiplication by two on the genus-two Jacobian has sixteen solutions. For general $L$, these give the sixteen fixed points of the stated quotient construction.

**The Enriques sextic and its K3 cover (pp. 190–192).** Let $Y$ be the smooth model of the sextic double along the six edges of a tetrahedron. The constructed degree-two cover is unramified on the smooth model. The source imports $p_a=p_g=0$, $\lambda=1$, and nontrivial bicanonical triviality from Chapter II §8. Equations (V.8.1)–(V.8.3) give $K_X^2=0$ and $\chi(\mathcal O_X)=2$.

There is, however, a real gap in the p. 191 implication

\[
|2C'|=|2C|\quad\Longrightarrow\quad |C'|=|C|.
\]

Cancellation by two in $\operatorname{Pic}$ is not valid: the nontrivial canonical two-torsion of an Enriques surface is precisely the counterexample. The conclusion for this *particular* cover is right, but requires identifying the cover as the canonical cover. A direct repair uses the conductor divisor $\Delta$ on $Y$. Normalization adjunction gives $K_Y\sim2H-\Delta$. The tetrahedron product $T$, as a section of $\mathcal O_Y(4H)$, has divisor $2\Delta$. Consequently adjoining $\sqrt T$ defines the étale cover associated to the two-torsion line bundle $\mathcal O_Y(2H-\Delta)=\omega_Y$. Its pullback becomes trivial; therefore $K_X\sim0$. Together with $\chi=2$, this gives $p_g(X)=1$, $q(X)=0$, all $P_m=1$, and the modern K3 identification. This repair is supplied by the present audit, using the standard cyclic-cover construction, not attributed to an unverified historical author.

The Comessatti splitting criterion in the p. 189 footnote has the following precise content: restricting a double cover to a curve tangent to its branch divisor gives a split cover exactly when the half-contact divisor is linearly equivalent to the restriction of the branch square-root line bundle. Even contact multiplicities alone do not suffice; the square-root class is essential.

### V.9. Existence of a cover with prescribed branch curve (pp. 192–198)

**The problem and the discriminant.** A polynomial equation $z^n=f(x,y)$ defines a cyclic cover of the affine plane when its function field has degree $n$, but its *discriminant divisor* includes $(n-1)(f=0)$ and may branch at infinity. If $\deg f=m$, the monodromy around infinity is the inverse of an $m$th power of an $n$-cycle, so it is trivial exactly when $n\mid m$. More precisely, the coefficient of the infinity component in the discriminant is $n-\gcd(n,m)$ when it occurs. The latter numerical refinement is derived here from the ramification indices; Enriques only says “one or more times.” Irreducibility is automatic for a reduced irreducible branch polynomial over $\mathbf C$, but not for an arbitrary perfect power.

For a general projected singular model, the polynomial discriminant separates as $\Delta=\Delta_1\Delta_2^2$: $\Delta_1$ is genuine simple branch, while $\Delta_2$ comes from the apparent double curve of the chosen equation. This factorization is not a universal factorization for every non-generic polynomial; it describes the ordinary projection under discussion. The finite normalization, not merely the raw polynomial resultant, is the geometric cover.

Choose a line pencil through $O\notin B$ and a generic fiber meeting a degree-$2m$ branch curve in $2m$ points. A connected degree-$n$ cover of that line is determined by a transitive tuple of $2m$ transpositions with product one, modulo simultaneous relabelling. Its genus is

\[
g=m-n+1.
\]

The scan on p. 194 really prints $m/2-n+1$; that is a source error. The statement that there are finitely many possibilities refers to covers with fixed branch locations and fixed degree, not to a finite set of curves independent of those locations. Enriques cites Riemann's existence theorem through Enriques–Chisini and mentions Hurwitz's enumeration without using its number.

**The three local conditions.** Moving the line gives braid monodromy. After transporting the vanishing arcs so the colliding punctures are adjacent, the required transpositions are:

| Critical line | Local braid relation | Transpositions for a smooth generic covering surface |
|---|---|---|
| Simple tangency to smooth $B$ | Equality of the two meridians | The same transposition |
| Line through a node of $B$ | Commutation | Disjoint transpositions |
| Line through a cusp of $B$ | $aba=bab$ | Distinct transpositions with one letter in common |

Equal transpositions also commute at a node but produce a singular double-cover local model; Enriques calls that a “virtually nonexistent” node for the generic smooth-cover enumeration. At a cusp, equal transpositions similarly give a singular local covering surface rather than the required generic triple-sheet model. This is why the smoothness/local-model conditions are stronger than an arbitrary representation into $S_n$.

The reduction to adjacent arcs is the Hurwitz action, not a permission to move arcs through branch points while leaving their transpositions unchanged. In one convention the elementary move is $(a,b)\mapsto(b,b^{-1}ab)$; changing the convention reverses this formula but not the existence condition. Enriques explicitly notes the necessary change of substitutions on p. 197. The three classes of critical values generate the pencil monodromy, together with the projective product relation. Thus checking them is a finite topological formulation of a global condition, not merely three numerical tests on the numbers of nodes and cusps.

**Precise existence theorem and modern proof.** A connected degree-$n$ finite cover of $\mathbf P^2$ with prescribed simple branch $B$ and the stated local models exists exactly when there is a transitive monodromy representation

\[
\pi_1(\mathbf P^2\setminus B)\longrightarrow S_n
\]

whose local meridians and local singularity representations have the preceding types. The representation first produces a finite topological cover of the complement. The complex Riemann existence theorem algebraizes it. Normalizing $\mathbf P^2$ in its function field extends it to a finite normal projective cover, and the prescribed local models show that its total space is smooth. Conversely, any such cover supplies the representation. SGA 1, Exposé XII, Theorem 5.1, is a precise modern reference for the algebraization step; the normalization and local checks are separate steps.

**What Enriques supplies and what needs completion.** The necessity is developed carefully on pp. 194–197. The sufficiency on p. 198 is a short construction: realize the varying line cover by finitely many sufficiently high-degree plane models, sum the corresponding functions, and vary the line. It assumes that the resulting family is algebraic and descends, and that the sum still generates the intended degree-$n$ function field. A sum of primitive functions need not itself be primitive. The prescribed distinct points $O_1,\dots,O_n$ can repair this last issue if they are consistently labelled in every summand: the sum then takes distinct values on that fiber. Nevertheless the algebraization and global gluing remain compressed; the preceding modern proof supplies them without claiming that every trace is automatically primitive. His exclusion of additional branch lines relies on the same distinct-fiber normalization.

**The deformation corollary.** The existence property is constant along a connected, topologically locally trivial equisingular family, with the local covering types transported along the family. The assertion must not be read as saying that degree, number of nodes, and number of cusps determine the complement's fundamental group. Equisingular strata may have different connected components, and passage through worse singularities can change the answer. Zariski's examples and the modern deformation literature make this distinction indispensable. Likewise existence is different from **uniqueness**. Enriques's p. 193 appeal to Chisini's 1944 work is a qualified anticipation of a uniqueness problem; it is not a proved general uniqueness theorem in these pages. Modern results for generic linear projections and conjectures for more general generic covers must be distinguished. Kulikov (2008, Theorem, p. 902) proves uniqueness for generic linear projections, with the Veronese exception stated explicitly. That theorem is not a blanket theorem for every generically branched cover of a fixed degree.

### V.10. Chisini's degenerations and the K3 examples (pp. 199–204)

Enriques credits the existence theorem to his 1923 paper and Zariski's topological reformulation to papers of 1929 and 1931. The statement that a cusp-free branch curve cannot give a connected simply branched cover of degree $>2$ uses the standing irreducibility and nodal hypotheses. For an irreducible nodal plane branch curve, the complement group is cyclic; transitive monodromy generated by its one meridian is then cyclic, and a transposition permits only degree two. If multiplicities in the discriminant are allowed, cyclic covers explain the stated exception. With reducible branch divisors and more general ramification there are other abelian covers; the sentence should not be generalized to them. The history of the needed fundamental-group theorem matters: Deligne (1981), Introduction and Theorem 1, explains that Zariski's 1929 argument relied on Severi's then-unproved irreducibility result. Fulton (1980) proved the tame algebraic fundamental-group assertion; Deligne supplied the topological theorem. Thus the rigorous modern nodal-complement justification must not simply be attributed to the 1929 proof.

**Degeneration identity.** If a surface equation degenerates into $F_1F_2=0$, the discriminant acquires the square of the resultant:

\[
\operatorname{disc}(F_1F_2)
=\operatorname{disc}(F_1)\operatorname{disc}(F_2)
 \operatorname{Res}(F_1,F_2)^2
\]

up to a nonzero normalization factor. Thus the limiting branch divisor is $B_1+B_2+2C$, where $C$ is the image of the common curve. This algebraic identity explains the construction. Its converse requires a smoothing with the correct monodromy; an arbitrary sum with a doubled curve is not enough.

For a smooth quartic projected from outside, $n=4,\pi=3,p_a=\lambda=1$ in (V.6.1), so $B=C_{12}$ has $24$ cusps and $12$ nodes. Letting the center move onto a smooth point produces $C_{10}+2L$, where $C_{10}$ is a triple-plane branch curve with $18$ cusps and no nodes, and $L$ is bitangent. Making the center an ordinary double point produces $C_6+2Q+2L$, with $Q$ a six-tangent conic. A triple center gives the further limit $2C_3+2Q+2L$. The sextic in the second degeneration is **special enough to possess the six-tangent conic**; the phrase “affatto generale” cannot mean a general point of the full space of smooth sextics simultaneously with that condition.

The local counts are consistent: each tangency to an added double component absorbs three cusps; each simple crossing absorbs two nodes. Thus the two tangencies and six further intersections in $C_{10}+2L$ account for six additional cusps and twelve nodes. The six conic contacts in $C_6+2Q$ account for eighteen cusps. Enriques explains these through the first and second polars and the bitangents through the moving center, but refers the global smoothing construction to Chisini's papers of 1934, 1938, and 1939.

For the proposed K3 family, put $n=2\pi-2$, $p_a=\lambda=1$. The branch data become

\[
\deg B=3n=6\pi-6,\qquad
k(\pi)=24(\pi-2),\qquad
d(\pi)=18\pi^2-78\pi+84.
\]

If such a **smooth finite generic cover** exists, its pullback $H$ is ample, $K^2=0$, $\chi=2$, and $KH=0$. Riemann–Roch gives $p_g=q+1>0$; a nonzero canonical section has an effective zero divisor of intersection zero with $H$, hence no zero divisor. Therefore $K\sim0$, $p_g=1$, and $q=0$. Kodaira vanishing then gives $h^0(H)=\pi+1$. This supplies the content of Enriques's inference that these are surfaces with trivial canonical curve and a $\pi$-dimensional hyperplane system. It is stronger than merely saying that their two numerical invariants happen to be one.

The step $\pi=3\to4$ adds eighteen cusps and twenty-four nodes at the conic stage, then six cusps and twenty-four nodes at the line stage, giving $48$ cusps and $60$ nodes for the sextuple plane. In general the conic stage adds eighteen cusps and $12n-24$ nodes; the line stage adds six cusps and $6n$ nodes. Their total node increment is $18n-24=36\pi-60$, exactly $d(\pi+1)-d(\pi)$.

The final p. 203 assertion about selecting the line has a more concrete reconstruction than the preceding conic step. The successful intermediate $(n+1)$-plane has $p_a=1$, $K^2=-1$, $H^2=n+1$, and $KH=1$. Since $\chi=2$, there is an effective canonical divisor. Its ample degree one forces it to be a single reduced irreducible curve $E$; adjunction gives $p_a(E)=0$ and $E^2=-1$. Contracting it produces a K3 surface with a polarization of square $n+2$. The curve $E$ maps to a line because $HE=1$, and its intersection with the ramification divisor is $(3H+E)E=2$, explaining the required two tangencies in the generic model. This fills the source's contraction argument, subject to its ordinary-projection and embedding assumptions. It does not remove the earlier conic-stage obstruction.

**What is not proved.** Having at least nineteen moduli does not alone establish the existence of a specialization with a prescribed six-tangent conic. Nor does the existence of such a conic ensure that its double can be smoothed with the desired branch monodromy. Enriques explicitly acknowledges the latter obstruction on p. 203 and does not claim to have carried out the induction for all $\pi$. The low-degree construction is an illustration of Chisini's method; the general K3 existence/classification is deferred to Chapter VII §3, outside the supplied substantive chapter range. The last page's citations to Campedelli, Libois, B. Segre, and Pompilj are bibliographic pointers rather than proofs reproduced in this excerpt.

### V.11. The first count of moduli (pp. 204–207)

Enriques restricts first to a minimal regular nonruled surface, $q=0$, $p=p_a=p_g$, with some nonzero plurigenus. Choose $H$ sufficiently positive that the complete linear system is base-point-free, simple, and regular and nonspecial in the cohomological sense $H^1(H)=H^2(H)=0$. Surface Riemann–Roch gives

\[
r=\dim|H|=p+n-\pi+1.
\]

The inequality $n\le2\pi-2$ is $KH\ge0$, valid because $K$ is nef on the minimal nonruled complex surface. For branch degree $N=2n+2\pi-2$, a node imposes at most one condition and an ordinary cusp at most two on the space of degree-$N$ plane curves when their locations may move. Consequently the equisingular component has dimension at least

\[
s_0=\frac{N(N+3)}2-d-2k
=(n+\pi-1)(2n+2\pi+1)-d-2k.
\]

This dimension lower bound does **not** assume that the equisingular scheme is smooth or reduced. Write its actual component dimension as $s_0+\omega$, $\omega\ge0$. Changing plane coordinates accounts for eight parameters, and choosing a net in the $(r+1)$-dimensional space of sections accounts for
$\dim\operatorname{Gr}(3,r+1)=3r-6$.
The generic degree of the map from covers to branch curves is finite for fixed branch curve and degree, by finite generation of the complement group; uniqueness is unnecessary for this dimension calculation.

For $q=0$, a continuously varying line-bundle class on a fixed surface is constant, since $\operatorname{Pic}^0(S)$ is zero-dimensional. The identity component of the automorphism group does not contribute for the regular nonruled surfaces under consideration; its polarized stabilizer is finite. Infinite **discrete** automorphism groups, such as those of many K3 surfaces, are not ruled out and do not invalidate a dimension calculation. This is the content behind the source's Picard-system argument and its appeal to Enriques–Fano on continuous projective automorphisms.

Subtracting the two redundant dimensions and inserting (V.6.1) gives

\[
M\ge9p-2\lambda+12,\qquad
M=9p-2\lambda+12+\omega. \tag{V.11.1}
\]

The equality expresses $\omega$ as the actual excess of the relevant branch component, with the preceding fiber-dimension assumptions. It does not identify that excess with a tangent-space dimension.

**The multiple-base calculation on p. 205.** The text addresses a possible degeneration from systems with base points to the chosen free system. If multiplicities are $i_j$, moving self-intersection is $n$, and the resolved generic member has geometric genus $\pi$, then

\[
L^2=n+\sum i_j^2,\qquad
p_a(L)=\pi+\frac12\sum i_j(i_j-1),
\]

so adjunction gives

\[
KL=2\pi-2-n-\sum i_j,
\]

not the printed $2\pi-2-n-\sum i_j^2$. Equivalently, on the resolved surface,
$K_{\widetilde S}\widetilde L=KL+\sum i_j$.
The printed square is valid if one holds the *unresolved arithmetic genus* fixed, but that conflicts with the phrase “genere effettivo” in this argument. If $L$ specializes to $H+\theta$, the corrected formula still gives $K\theta=-\sum i_j<0$. This contradicts nefness. Thus the intended exclusion survives, although the quantitative formula and the corresponding formula for $\theta^2$ require correction.

For an irregular surface, line bundles in $\operatorname{Pic}^0$ add $q=p_g-p_a$ parameters to the redundant family. The resulting expression is

\[
M=10p_a-p_g-2\lambda+12+\omega.
\]

If a continuous automorphism group acts, its dimension must be included in the fiber calculation; Enriques's footnote explicitly allows a changed meaning of $\omega$. One must not identify that redefined $\omega$ with the original branch excess without an automorphism correction.

The examples $M=19$ for K3 surfaces and $M=10$ for Enriques surfaces are asserted here and promised later proof. The first is the dimension of a family with a fixed polarization type. The local analytic deformation space of an unpolarized complex K3 surface has dimension twenty; projectivity with a specified polarization cuts out one condition. Thus nineteen is not an error, but the moduli problem needs to be specified.

### V.12. The completeness hypothesis and its actual status (pp. 207–209)

Let $D$ be an irreducible plane curve of degree $n$ with $d$ nodes and $k$ ordinary cusps, and let $\nu:C\to D$ be its normalization. The line bundle controlling its equisingular first-order deformations is

\[
A=\nu^*\mathcal O_D(n)
 \Bigl(-\sum_{\rm nodes}(P_i+Q_i)-3\sum_{\rm cusps}R_j\Bigr).
\]

At a node, the equisingular Jacobian ideal pulls back to order one on both branches; at a cusp $x=t^2,y=t^3$, the ideal $(x^2,y)$ pulls back to order three. Hence

\[
m=\deg A=n^2-2d-3k,\qquad
g(C)=\frac{(n-1)(n-2)}2-d-k.
\]

The printed $m=n-2d-3k$ on p. 208 omits the square. Put
$r=n(n+3)/2-d-2k$; then $m-g+1=r$, and Riemann–Roch says

\[
h^0(A)=r+h^1(A).
\]

If the actual family dimension is $r+\omega$, its characteristic **projective** series has dimension $r+\omega-1$, whereas the complete projective series has dimension $h^0(A)-1$. Therefore $\omega\le h^1(A)$. The source's displayed phrase
“$\ge r+\omega=m-\pi+\omega$” has a further off-by-one: with the corrected $m$, $r=m-\pi+1$. The intended characteristic dimension is $r+\omega-1=m-\pi+\omega$.

Enriques correctly distinguishes a first-order deformation from an actual integrable deformation. He describes the possibility that local equations have dependent differentials while still cutting out the expected smaller-dimensional reduced locus. On p. 209 he explicitly labels the equality $\omega=h^1(A)$ an **“Ipotesi di lavoro”** and says he has not proved it. It would be historically wrong to report that he silently assumed the disputed step in this 1949 presentation.

The unrestricted hypothesis is not a theorem that was later proved in full. Nodal/cuspidal equisingular strata can be nonreduced and can have incomplete characteristic series. Wahl (1974), *Deformations of plane curves with nodes and cusps*, is the classical deformation-theoretic treatment; Guffroy (2003), *Sur l'incomplétude de la série linéaire caractéristique d'une famille de courbes planes à nœuds et à cusps*, supplies explicit further examples. Vakil's Murphy's law, Main Theorem 1.1, parts M5a–M5b, shows the severity of possible singularities for simple covers and nodal/cuspidal plane-curve strata. Consequently a universal replacement must retain an obstruction space; one cannot repair the argument merely by declaring every first-order direction integrable. Singular points of a reduced stratum and generically nonreduced components are logically different phenomena, and the latter are particularly relevant to a hypothesis made at a generic member.

For a precise sheaf-theoretic formulation, Tannenbaum (1984, §1, Definition 1.1 and Remarks 1.2) identifies the equisingular normal sheaf, its tangent sections, and its obstruction cohomology. His Introduction also records the failure of the unrestricted characteristic-series assertion. In the nodal/cuspidal situation above that sheaf is $\nu_*A$, as the displayed local ideals show.

A precise sufficient condition is $H^1(C,A)=0$: then the equisingular deformation is unobstructed and of the expected dimension. In the nodal case,
$K_C-A=\nu^*\mathcal O_D(-3)$, so this group vanishes. With cusps,
$K_C-A=\nu^*\mathcal O_D(-3)+\sum R_j$, of degree $k-3n$; thus $k<3n$ is an elementary sufficient vanishing condition. This last bound is an explicit deduction in this audit, not claimed as an optimal theorem from the literature. It also shows why elementary examples can support the hypothesis while more complicated ones invalidate it.

### V.13. The stronger moduli inequality and the canonical calculation (pp. 209–213)

This section is conditional throughout on V.12's completeness assumption. Enriques says so on p. 209, again on p. 210, and in his “probabilmente” conclusion on p. 213. His branch characteristic series pulls back to the ramification curve $J=3H+K$ as the series cut by $L=4H+K$, with the pinch-point divisor $G$ removed. The geometric explanation on p. 210 is that polars through another point cut the first-polar series of the branch curve. One must distinguish the line bundle of the full infinitesimal series from the potentially smaller series of actual deformations.

For sufficiently positive $H$, the restriction and vanishing hypotheses allow

\[
\dim|4H+K|=p+4\pi+6n-4.
\]

If $\tau=\deg G$ and the relevant speciality is $\omega$, the characteristic family dimension is

\[
R=13p+4n-4\pi-2\lambda+19+\omega.
\]

Choosing a four-dimensional vector subspace of $H^0(H)$ and spatial coordinates accounts for
$S=4r-12+15=4r+3=4p+4n-4\pi+7$.
Thus $R-S$ reproduces (V.11.1). The vanishing and restriction statements are permissible after choosing a sufficiently high positive system; they are not automatic for every divisor merely because a net exists.

**Canonical system and notation repair.** Assume the canonical map has the generic birational properties required by the source, with $p>3$. Put $H=K$, so $n=\lambda-1$, $\pi=\lambda$, $J=4K$, and by adjunction $K_J=5K|_J$. Let

\[
\theta=\dim|G|_J=h^0(J,\mathcal O_J(G))-1.
\]

Serre duality gives
$h^1(J,K_J-G)=\theta+1$,
and $G$ imposes $\tau-\theta$ independent conditions on the canonical series. Since $q=0$, the restriction $H^0(5K)\to H^0(K_J)$ is surjective with kernel $H^0(K)$ of dimension $p$. Using $h^0(5K)=p+1+10K^2$ gives

\[
M=9p-2\lambda+16+\theta. \tag{V.13.1}
\]

This is the coherent meaning of the displayed formula on p. 212. The accompanying symbols are not coherent as printed: the original moduli excess in V.11 equals $\theta+4$, so $\theta=\omega_{\rm mod}-4$, whereas the speciality on the canonical ramification curve equals $\theta+1$, so it cannot be that same $\omega$. The printed sentence calls $\theta$ the speciality and then calls it the projective dimension of $|G|$; these differ by one. In particular, the first displayed characteristic-dimension formula on p. 212 must read

\[
R-1=p+4\pi+6n-4-\tau+\theta,
\qquad
R=13p-2\lambda+15+\theta,\quad S=4p-1.
\]

If canonical speciality is denoted by $\omega_{\rm can}=\theta+1$, the last term in the first equation is $\omega_{\rm can}-1$, not $\omega_{\rm can}$. Subtracting the displayed $S$ gives (V.13.1). This audit keeps three quantities distinct: branch-component excess $\omega_{\rm mod}$, canonical speciality $\theta+1$, and projective divisor-series dimension $\theta$.

A fixed canonical net lies in a $(p-4)$-dimensional family of three-dimensional canonical systems. Enriques argues that their pinch-point divisors on the fixed Jacobian curve move in $|G|$, giving $\theta\ge p-4$. The independence and genericity of this family are sketched, not developed as a deformation-theoretic proof. Inserting the inequality in (V.13.1) gives

\[
M\ge10p-2\lambda+12=10\chi(\mathcal O_S)-2K^2.
\]

**The correct modern replacement.** The inequality survives without the false universal completeness hypothesis. The Kuranishi deformation space of a smooth surface has tangent space $H^1(S,T_S)$ and an obstruction map into $H^2(S,T_S)$; hence

\[
\dim\operatorname{Def}(S)
\ge h^1(T_S)-h^2(T_S)
=10\chi(\mathcal O_S)-2K^2+h^0(T_S).
\]

Here Hirzebruch–Riemann–Roch gives
$\chi(T_S)=2K^2-10\chi(\mathcal O_S)$.
For a surface of general type the automorphism group is finite, so $h^0(T_S)=0$, and the local moduli dimension has the stated lower bound. No claim that the obstruction map vanishes is needed. Catanese (2013), §1.3, arXiv version p. 13, explicitly identifies this as Enriques's inequality proved by Kuranishi. This repairs the numerical conclusion by a different theorem; it does not retroactively prove Enriques's completeness hypothesis.

### V.14. Historical assessment and irregular formulas (pp. 213–215)

Enriques reports that Noether (1888) anticipated equality
$M=10p-2\lambda+12$ by a negative-postulation parameter count. The count “number of parameters minus number of conditions” is a heuristic unless actual local equations, their codimension, and the relevant fibers have been controlled. Equality is stronger than the modern lower bound and is not universal.

The historical admission on p. 214 is unusually explicit. Enriques says his papers of 1908 and 1912 had overlooked the distinction between the differential property and completeness, and that Zariski's *Algebraic surfaces* (1935), V §8, exposed the gap. He compares this with Severi's 1921 criticism of an earlier irregularity argument, to be discussed in Chapter IX §6. The last paragraph of p. 214 and the beginning of p. 215 distinguish the revised *first* moduli bound, which uses actual branch-family dimensions and existence, from the *second* bound still tied to the working hypothesis. Those distinctions must be preserved. The sentence on p. 214 that calls Noether's equality the case $\omega=0$ needs the prime: it is $\omega'=0$, the vanishing of the stronger excess in the immediately preceding formula. The scan confirms the missing prime; the transcription preserves the printed reading.

The further displayed expressions are conditional historical proposals:

\[
M=12p_a-2p_g-2\lambda+12+\omega,\qquad \omega\ge0,
\]
\[
M\ge10p-2\lambda+11,
\]
\[
M=9p_a+p_g-2\lambda+11+\theta.
\]

The last two come from B. Segre's claimed estimates $\omega\ge p-1$ and
$\omega\ge2p_g-p_a-1$ for the excess in the first formula of V.11. Enriques explicitly says that Segre's approach retained the disputed completeness assumption. These are not independent proofs supplied here, and their individual excess symbols should not be identified across formulas without checking their definitions. In particular, the general modern Kuranishi bound does not automatically establish every sharper irregular estimate simply by renaming an excess term.

The closing Castelnuovo communication asserts
$\omega\ge2p_a+p_g+\lambda-I-3$.
If $I$ retains its chapter-wide meaning as the Zeuthen–Segre invariant, Noether gives

\[
2p_a+p_g+\lambda-I-3=p_g-10p_a+2\lambda-12.
\]

Inserted in $M=10p_a-p_g-2\lambda+12+\omega$, this yields only $M\ge0$. Thus, with that symbol identification, the displayed bound is numerically consistent but adds no positive lower bound beyond nonnegativity. The text gives no derivation and no published locator for the private communication. This audit does not invent one.

### V.E. Further deductions and proposed work, explicitly by this audit

1. **A uniform exact replacement for singular-member counting (high confidence).** Use the Euler defect $e(F_{\rm red})-e(F_{\rm gen})$ throughout V.1–V.2. This handles reducible and nonreduced fibers without pretending each contributes a positive number of actual nodal members. For example, a smooth multiple elliptic fiber contributes zero, while a nodal elliptic fiber contributes one. A generic elliptic K3 pencil therefore has total defect twenty-four. This follows directly from the formulas already proved.

2. **A computational consistency suite (high confidence).** For a generic degree-$d$ plane pencil, $b=d^2$, $g=(d-1)(d-2)/2$, and $\delta=3(d-1)^2$, so $I=-1$ independently of $d$. For a generic quartic projection, the branch data $(N,P,\delta,k,i,d,t)=(12,19,36,24,96,12,480)$ follow from (V.6.1). These are exact examples for testing notation and constants; the value $t=480$ follows from the genus of the dual curve, not from counting apparent crossings in a drawing.

3. **Separate excess, speciality, and obstructions (high confidence).** The right conceptual diagram behind pp. 207–213 is: actual equisingular family dimension $\le$ tangent dimension; tangent dimension is computed by a line-bundle cohomology group; actual dimension is cut out by higher-order obstructions. The three numbers coincide only under additional hypotheses. This separation resolves both the acknowledged logical gap and the printed $\omega/\theta$ inconsistencies.

4. **A concrete unobstructed example with nonzero obstruction space (high confidence).** A smooth sextic surface in $\mathbf P^3$ has $p_g=10$, $K^2=24$, and embedded moduli dimension $\binom93-16=68$. The Enriques–Kuranishi lower bound is $110-48=62$. This can be verified from the normal sequence
$0\to T_S\to T_{\mathbf P^3}|_S\to\mathcal O_S(6)\to0$
and the restricted Euler sequence. They give
$h^0(\mathcal O_S(6))=83$, $h^0(T_{\mathbf P^3}|_S)=15$,
$H^1(T_{\mathbf P^3}|_S)=0$, and $h^2(T_{\mathbf P^3}|_S)=6$.
The last number is the dimension of the cokernel of
$H^2(\mathcal O_S)\to H^2(\mathcal O_S(1))^{\oplus4}$; its dual is the kernel of the multiplication map
$H^0(\mathcal O_S(1))^{\oplus4}\to H^0(\mathcal O_S(2))$,
which is surjective from dimension sixteen to ten.
The normal sequence then gives $h^1(T_S)=68$ and $h^2(T_S)=6$.
Every first-order abstract deformation is induced by a degree-six equation, and the smooth open space of such equations modulo coordinate changes supplies the smooth local deformation family (a finite stabilizer can give a finite quotient in coarse moduli). Thus the obstruction *space* has dimension six while the Kuranishi family is smooth. A nonzero $H^2(T_S)$ does not imply that obstructions occur, and Noether's equality is not universal. In V.11's notation the branch excess is sixteen, and the stronger excess is six.

5. **A sharply scoped research question (not claimed open in full generality).** For a specified nodal/cuspidal branch component admitting a fixed monodromy representation, determine when the branch deformation functor and the cover deformation functor induce a smooth map, and identify the exact obstruction classes when they do not. The local calculations above and the cited deformation literature provide a framework. This is a proposed computation for individual families, not a claim that the general question has no known answers. Similarly, Chisini's proposed K3 induction should be investigated with explicit braid data; numerical cusp and node counts alone cannot certify its smoothing step.

### V.R. Verified modern references used in the chapter

- Catanese, F. (2013). A superficial working guide to deformations and moduli. In *Handbook of moduli* (Vol. I, pp. 161–215). International Press. Author's full preprint: https://arxiv.org/abs/1106.1368 ; PDF https://arxiv.org/pdf/1106.1368 . Verified locator: §1.3, preprint p. 13, the Enriques–Kuranishi inequality and its attribution. The author's publication list independently confirms the final bibliographic data.
- Grothendieck, A. (Ed.). (2003). *Revêtements étales et groupe fondamental (SGA 1)* (Documents Mathématiques, Vol. 3; revised reissue of the 1971 Lecture Notes in Mathematics, Vol. 224; including two exposés by Michèle Raynaud). Société Mathématique de France. https://arxiv.org/abs/math/0206203 . Publisher record: https://smf.emath.fr/node/43215 . Verified locator: Exposé XII, Theorem 5.1, original pp. 332–333, retained in the reissue's margin. Used for complex Riemann existence, not for uniqueness of branched covers.
- Deligne, P. (1981). Le groupe fondamental du complément d’une courbe plane n’ayant que des points doubles ordinaires est abélien (d’après W. Fulton). *Séminaire Bourbaki, 1979–1980*, Exposé 543, 1–10. https://www.numdam.org/item/SB_1979-1980__22__1_0/ . Verified locator: Introduction and Theorem 1; the independent reference audit consulted the original PDF.
- Fulton, W. (1980). On the fundamental group of the complement of a node curve. *Annals of Mathematics, 111*(2), 407–409. https://doi.org/10.2307/1971204 . Publisher metadata verified by the independent reference audit.
- Guffroy, S. (2003). Sur l'incomplétude de la série linéaire caractéristique d'une famille de courbes planes à nœuds et à cusps. *Nagoya Mathematical Journal, 171*, 51–83. https://doi.org/10.1017/S0027763000025514 . Publisher abstract and bibliographic data verified; the abstract explicitly distinguishes Wahl's nonreduced example from the author's examples with singular reduction.
- Kulikov, V. S. (2008). On Chisini's conjecture. II. *Izvestiya: Mathematics, 72*(5), 901–913. https://doi.org/10.1070/IM2008v072n05ABEH002423 . Full text: https://webhomes.maths.ed.ac.uk/cheltsov/kulikov/pdf/2008.pdf . Verified locator: Theorem, p. 902, including the Veronese exception and the restriction to generic linear projections.
- Tannenbaum, A. (1984). On the classical characteristic linear series of plane curves with nodes and cuspidal points: Two examples of Beniamino Segre. *Compositio Mathematica, 51*(2), 169–183. https://www.numdam.org/item/CM_1984__51_2_169_0/ . Full text: https://www.numdam.org/item/CM_1984__51_2_169_0.pdf . Verified locators: Introduction, pp. 169–170; §1, Definition 1.1 and Remarks 1.2, for the tangent and obstruction sheaves.
- Vakil, R. (2006). Murphy's law in algebraic geometry: Badly-behaved deformation spaces. *Inventiones Mathematicae, 164*, 569–590. https://arxiv.org/abs/math/0411469 . Verified locator supplied by the independent reference audit: Main Theorem 1.1, M5a–M5b, for simple branched covers and nodal/cuspidal curves. This is a limitation on universal smoothness assertions.
- Wahl, J. M. (1974). Deformations of plane curves with nodes and cusps. *American Journal of Mathematics, 96*(4), 529–577. https://doi.org/10.2307/2373706 . Journal contents verify title, author, year, and page range. The full article was not accessible through the retrieval used in this sub-audit; detailed claims about its examples are corroborated by Guffroy's primary abstract and the later primary deformation literature, rather than an invented theorem number.

The common modern surface references for Riemann–Roch, adjunction, double covers, resolution, and classification are supplied in the cross-chapter reference guide and the verified references accompanying Chapter VI. Proofs in this chapter explicitly labelled as reconstructions or deductions are this audit's calculations. Historical references below remain citations **as given by Enriques**, unless independently marked verified.

### V.H. Historical dependency ledger

| Source location | Historical dependency cited there | Treatment in these pages |
|---|---|---|
| 167 | H. G. Zeuthen, *Études géométriques etc.*, Math. Ann. IV (1871); C. Segre, *Intorno ad un carattere delle superficie ecc.*, Turin (1896) | Invariant credited; Segre's comparison reproduced |
| 170, 172 | Castelnuovo–Enriques, *Sopra alcune questioni fondamentali ecc.*, Ann. di Mat. (1901) | Double-component case worked out; irrational-pencil formula derived |
| 172 | Godeaux, Hainaut vol. 66 (1920), and Belgian Academy communication (13 October 1934); Campedelli, Lincei ser. 6 vol. XIX (1934) | General fiber-equivalence formula quoted |
| 173–180 | Noether, Math. Ann. VIII; Bonnesen (1906); Pannelli (1905); Caporali | Ordinary-projection elimination and cusp formula explained; existence of ordinary models imported |
| 180 | Severi (1902), *Il genere aritmetico ed il genere lineare...*; Severi's 1942 book on equivalence systems | Direct invariance proof credited, not reproduced; broader program described |
| 183–185 | Enriques, *Ricerche ecc.*; Chapter III §7; Castelnuovo–Enriques (1900), via Enriques–Conforto §27 p. 489 | Canonical transformation proved; singular double-plane conventions and adjoint classification imported |
| 188–190 | Enriques–Chisini, Book VI §40, vol. IV p. 246; Klein; Enriques–Severi, *Mémoire sur les surfaces hyperelliptiques*, Acta Math. (1909) | Kummer configuration and genus-two representation imported; cover invariants calculated |
| 191–192 | Chapter II §8; Enriques, *Un'osservazione relativa alle superficie di bigenere uno*, Bologna (1908) | Enriques sextic invariants imported; its double cover analyzed |
| 193–198 | Enriques–Chisini, Book V §33, vol. III p. 355, and §3 p. 18; Hurwitz; Chisini (1944) | Riemann existence and braid changes imported; necessity explained; sufficiency compressed; uniqueness only qualified |
| 199 | Enriques (1923), *Sulla costruzione delle funzioni algebriche...*; Zariski (1929, 1931), and *Algebraic surfaces* (1935) | Existence and group reformulation credited |
| 199–204 | Chisini (1934, 1938, 1939); Enriques (1896, 1898); Campedelli (1932, 1940); Libois (1934); B. Segre (1930); Pompilj (1939, 1941) | Degeneration method illustrated; broader developments only referenced |
| 206 | Enriques–Fano, through Enriques–Conforto, ch. VI §37 p. 496 | Continuous-projective-automorphism restriction imported |
| 207 | De Jonquières and Beck, Math. Ann. 14 (1878), through Enriques–Chisini | Infinitesimal intersection multiplicities credited |
| 213–215 | Noether (1888); Enriques (1908, 1912, 1923–1924); Zariski (1935), V §8; Severi (1921); B. Segre (1934); private communication from Castelnuovo | Historical gap openly acknowledged; stronger formulas remain conditional |

The abbreviated “etc.” and “op. cit.” entries are not silently expanded to guessed full titles or page ranges. They record exactly which earlier work the source relies on. Independent consultation of every original nineteenth- and early-twentieth-century paper has not been completed.

#### Historical titles and locators preserved from the excerpt

The following entries expand the ledger using the titles and locators actually supplied in the excerpt. They are **source-recorded citations**, not a claim that each original publication was independently inspected. Missing dates, pages, or abbreviated titles are deliberately not guessed.

- Zeuthen, H. G. (1871). *Études géométriques etc.* *Mathematische Annalen, IV*. Cited on pp. 167 and 180.
- Segre, C. (1896). *Intorno ad un carattere delle superficie ecc.* *Atti dell'Accademia delle Scienze di Torino*. Cited on p. 167.
- Castelnuovo, G., & Enriques, F. (1901). *Sopra alcune questioni fondamentali ecc.* *Annali di Matematica*. Cited on pp. 170 and 172.
- Godeaux, L. (1920). *Sur le calcul de l'invariant de Zeuthen-Segre.* *Mémoires de la Société des Sciences du Hainaut, 66*. Also cited: *Bulletin de l'Académie Royale de Belgique*, 13 October 1934. Source p. 172.
- Campedelli, L. (1934). *Sul computo dell'invariante di Zeuthen-Segre per una superficie algebrica*; *Ancora sul computo ecc.* *Rendiconti dell'Accademia dei Lincei*, ser. 6, XIX. Source p. 172.
- Noether, M. *Op. cit.*, *Mathematische Annalen, VIII*. The excerpt's p. 173 does not give the title or year; its earlier full citation is unavailable here.
- Bonnesen, T. (1906). *Sur les séries linéaires triplement infinies de courbes algébriques sur une surface algébrique.* *Bulletin de l'Académie Royale des Sciences et des Lettres de Danemark*, no. 4. Source p. 173; its footnote mistakenly has initial “P.” despite “T.” in the main text.
- Severi, F. (1902). *Il genere aritmetico ed il genere lineare in relazione alle reti di curve tracciati sopra una superficie algebrica.* *Atti dell'Accademia di Torino, XXXVII*. Source p. 180. The title is retained in the source's grammatical form.
- Pannelli, M. (1905). *Sui sistemi lineari triplamente infiniti di curve tracciati sopra una superficie algebrica.* *Rendiconti del Circolo Matematico di Palermo, XX*. Source p. 180.
- Severi, F. (1942). *Serie, sistemi di equivalenza e corrispondenze algebriche sulle varietà algebriche.* Cremonese. Source p. 180.
- Enriques, F. *Ricerche ecc.* Source p. 183 supplies no full title, year, or locator; these have not been reconstructed by guesswork.
- Enriques, F., & Conforto, F. *Le superficie razionali*, §27, p. 489, and chapter VI §37, p. 496. Cited on pp. 185 and 206; the edition is not specified in these pages.
- Enriques, F., & Chisini, O. *Lezioni*, Book V §3, vol. III, p. 18; Book V chapter III §33, vol. III, p. 355; Book VI §40, vol. IV, p. 246. These are the source's locators for braid changes, curve-cover existence, and the Kummer configuration respectively.
- Enriques, F., & Severi, F. (1909, as cited). *Mémoire sur les surfaces hyperelliptiques.* *Acta Mathematica*. Source p. 190; no article-page range is provided.
- Enriques, F. (1908). *Un'osservazione relativa alle superficie di bigenere uno.* *Rendiconti dell'Accademia di Bologna*. Source p. 192.
- Chisini, O. (1944). *Sulla identità birazionale delle funzioni algebriche di due variabili dotate di una medesima curva di diramazione.* *Rendiconti dell'Istituto Lombardo di Scienze e Lettere*. Source p. 193.
- Enriques, F. (1923). *Sulla costruzione delle funzioni algebriche di due variabili possedenti una data curva di diramazione.* *Annali di Matematica*, ser. IV, I. Source p. 199; p. 214 also refers to Annali 1923–1924.
- Zariski, O. (1929). *On the problem of existence of algebraic functions of two variables possessing a given branch curve.* *American Journal of Mathematics, 51*. Source p. 199.
- Zariski, O. (1929). *On the linear connection index of the algebraic surfaces z^n=f(xy).* *Proceedings of the National Academy of Sciences of the U.S.A., 15*. Source p. 199; the first-pass transcription's journal abbreviation required scan checking.
- Zariski, O. (1931). *On the irregularity of cyclic multiple planes.* *Annals of Mathematics*, ser. II, 32. Source p. 199.
- Zariski, O. (1935). *Algebraic surfaces.* Springer. Source pp. 199 and 214; the latter gives V §8 for the completeness criticism.
- Chisini, O. (1934). *Un teorema di esistenza dei piani multipli*, Notes I and II. *Atti dell'Accademia dei Lincei*, ser. VI, 19. Chisini, O. (1938). *Un più generale teorema di esistenza dei piani multipli.* Same journal, ser. VI, 27. Chisini, O. (1939). *Altre curve di diramazione dei piani n-pli.* Same journal, ser. VI, 29. Source p. 199.
- Enriques, F. (1896). *Sui piani doppi di genere 1.* *Memorie della Società Italiana delle Scienze, detta dei XL*. Enriques, F. (1898). *Sui piani doppi di genere lineare p^(1)=1.* *Reale Accademia dei Lincei*. Source p. 203.
- Campedelli, L. (1940). *Sopra i piani doppi con tutti i generi uguali all'unità.* *Rendiconti del Seminario Matematico di Padova, XI*. Campedelli, L. (1940). *Le superficie con i generi uguali all'unità, rappresentabili in infiniti modi sul piano doppio.* *Rendiconti del Seminario Matematico della Reale Università di Roma*, ser. V, I. Campedelli, L. (1940). *La classificazione dei piani doppi con tutti i generi uguali all'unità.* *Atti del 2° Congresso dell'Unione Matematica Italiana*, Bologna. Source p. 204.
- Campedelli, L. (1932). *Sui piani doppi con curva di diramazione dell'ottavo ordine*; *Sui piani doppi con curva di diramazione del 10° ordine*; *Sopra alcuni piani doppi notevoli con curva di diramazione del 10° ordine*. *Reale Accademia dei Lincei*. Source p. 204.
- Libois, P. (1934). *Rendiconti dell'Accademia dei Lincei*. No title is supplied in the excerpt; the topic is biquadratic degree-four covers.
- Segre, B. (1930). *Sulla caratterizzazione delle curve di diramazione dei piani multipli generali.* *Reale Accademia d'Italia, I*. Source p. 204.
- Pompilj, G. (1939). *Sulla rappresentazione algebrica dei piani tripli*; *Sui piani multipli diedrici*. *Rendiconti del Seminario Matematico della Reale Università di Roma*. Pompilj, G. (1941). *Osservazioni sui piani tripli.* *Reale Istituto Lombardo*. Source p. 204.
- De Jonquières and Beck (1878, as cited). *Mathematische Annalen, 14*. The source p. 207 gives no article title and refers additionally to Enriques–Chisini, Book II chapter II, vol. I p. 331 and vol. II p. 286.
- Noether, M. (1888). *Anzahl der Moduln einer Classe algebraischer Flächen.* *Sitzungsberichte der Akademie*, Berlin. Source p. 213.
- Enriques, F. (1908, June). *Sui moduli delle superficie algebriche.* *Rendiconti dei Lincei*. Enriques, F. (1912). *Sui moduli di una classe di superficie algebriche e sul teorema d'esistenza per le funzioni algebriche di due variabili.* *Atti della Reale Accademia di Torino*. Source p. 214.
- Segre, B. (1934). *Sui moduli delle superficie algebriche irregolari.* *Rendiconti dell'Accademia dei Lincei, XIX*. Source p. 215.

## Chapter VI. Regular surfaces: lower bounds and rationality (pp. 217–235)

### Reading conventions and the chapter's actual hypotheses

The opening leaf is unnumbered in the scan; its position before printed p. 218 identifies it as p. 217. The chapter normally works over the complex numbers with a smooth projective model \(S\). Its initial hypothesis \(p_g=p_a=p\) means \(q=h^1(S,\mathcal O_S)=0\), since \(p_a=\chi(\mathcal O_S)-1=p_g-q\). Enriques's \(P\) is \(P_2=h^0(S,2K_S)\), and \(P_i=h^0(S,iK_S)\). For a Cartier divisor \(C\), “degree” means the self-intersection \(n=C^2\), not its degree in a fixed projective embedding, and “virtual genus” means \(p_a(C)=1+(C^2+K_SC)/2\). When the member is smooth and irreducible this is its geometric genus. Thus \(p^{(2)}=K_S^2\) and \(p^{(1)}=K_S^2+1\). The latter is the **absolute** linear genus only after passage to the minimal model in the nonruled setting under discussion. A blow-up lowers \(K^2\) by one without changing any \(P_i,p_g,q\). The plane's relative value \(p^{(1)}=10\), calculated on p. 223, is consequently not an assertion that every rational model has that value.

An effective canonical divisor “of order zero” means the zero divisor: \(K_S\sim0\). A *virtual* canonical divisor of order zero is different: \(K_SH=0\) for the chosen ample class \(H\), and, under the nefness conditions used here, \(K_S\equiv0\). Numerical triviality alone does not give linear triviality. That distinction is the entire mechanism separating K3 from Enriques surfaces in §2. Standard modern formulations of these notions and the surface Riemann–Roch identity appear in Dolgachev (2016, §2); the particular deductions below are worked out directly from the excerpt.

### VI.1. Positivity of the absolute linear genus (pp. 217–220)

**Statement.** If \(S\) is a smooth minimal projective surface and \(P_m(S)>0\) for some \(m\geq1\), then \(K_S^2\geq0\), hence \(p^{(1)}\geq1\). Regularity is unnecessary. Enriques explicitly removes that hypothesis on p. 219. He does not assert the converse: for example, the plane has \(K^2=9\) and every positive plurigenus vanishes.

**The component proof is valid.** First let \(D=K_S=\sum s_iC_i>0\). Put \(\nu_i=C_i^2\), \(\rho_i=p_a(C_i)\), and \(n_{ij}=C_iC_j\geq0\) for \(i\ne j\). Adjunction gives

\[
K_SC_i=2\rho_i-2-\nu_i.
\]

If this were negative, integrality and \(\rho_i\geq0\) would give \(\nu_i\geq-1\). The case \(\nu_i=-1\) forces \(\rho_i=0\); an integral curve of arithmetic genus zero on a smooth surface is a smooth rational curve, so this is precisely an excluded \((-1)\)-curve. Otherwise \(\nu_i\geq0\), and

\[
K_SC_i=s_i\nu_i+\sum_{j\ne i}s_jn_{ij}\geq0,
\]

a contradiction. Hence \(K_SC_i\geq0\) for every component and \(K_S^2=\sum s_iK_SC_i\geq0\). The displayed quadratic expression on p. 218 is

\[
K_S^2=\sum_i s_i^2\nu_i+2\sum_{i<j}s_is_jn_{ij},
\quad
\frac{\partial K_S^2}{\partial s_i}=2K_SC_i.
\]

Euler's homogeneous-function identity gives the same conclusion. It does **not** show that the intersection matrix is positive semidefinite for arbitrary coefficients; it only evaluates this form at the positive coefficients of the effective canonical divisor. Reading it that way removes an apparent, but nonexistent, gap.

For \(D\in|mK_S|\), the identical argument works: if \(K_SC_i<0\), adjunction and minimality give \(C_i^2\geq0\), whereas \(mK_SC_i=D C_i\geq0\). Curves outside the support of \(D\) also have \(K_SC\geq0\). Thus the argument actually proves that \(K_S\) is nef whenever an effective positive multiple exists on a minimal model. If \(D=0\), then \(mK_S\sim0\), so \(K_S^2=0\). This deals with the separately discussed “order-zero” case without regarding the empty divisor as an ordinary curve.

Enriques's calculation with \(C'=C+K\) is another correct expression of the latter case. If \(K\sim0\), then \(C'=C\), \(n=2\pi-2\), and

\[
p_a(C+K)=p_a(C)+p_a(K)+C K-1
\]

reduces to \(\pi=\pi+p^{(1)}-1\), giving \(p^{(1)}=1\). This is an identity of *virtual arithmetic genera*: \(p_a(0)=1\).

**The second argument is a sketch, with movable parts requiring care.** On pp. 219–220, Enriques follows the adjoint sequence \(C,C+K,C+2K,\ldots\). Its intersections with \(K\) are

\[
K(C+jK)=KC+jK^2.
\]

If \(K^2<0\), these strictly decrease. Once a movable divisor \(L\) has \(KL<0\), the degrees \((L+jK)H\) eventually become negative for a suitable positive test class, so effective adjoints terminate. An effective \(mK\), conversely, would give injections \(H^0(C+jK)\hookrightarrow H^0(C+(j+m)K)\) and prevent termination. These are the mechanisms behind the argument. The prose suppresses the control of fixed components, the choice of a positive test curve, and the construction of an irreducible system after adding sufficiently positive divisors. Those points are not proved in this subsection.

The first observation on p. 220 must consequently not be read as a general assertion that the mere presence of an exceptional curve produces a **moving** system with negative canonical intersection and a terminating adjoint process. On the blow-up of a K3 surface, \(K=E\): every moving irreducible curve \(C\ne E\) has \(KC=EC\geq0\), while the isolated system \(|E|\) has \(E^2=-1>2p_a(E)-2=-2\) but its adjoints \(|(j+1)E|\) never terminate. The distinction between an isolated divisor and the movable systems needed in the proof matters. This is a limitation of the compressed second argument, not a counterexample to the theorem, already proved correctly by components. A modern minimal-model formulation supplies the missing framework; Hassett (2009, Corollary 2.20 and Theorem 2.26) is a verified reference.

### VI.2. Bigenus and plurigenera (pp. 220–224)

#### The lower bound and the boundary \(d=0\)

Let \(H=C\) be a sufficiently positive smooth irreducible member, \(n=C^2\), \(\pi=g(C)\), and \(d=KC=2\pi-2-n\). The second adjoint is \(C''=C+2K\), and its restriction to \(C\) has degree \(2\pi-2+d\). If \(d>0\), it is nonspecial and has \(\pi-1+d\) independent sections. The exact sequence

\[
0\longrightarrow\mathcal O_S(2K)\longrightarrow
\mathcal O_S(C+2K)\longrightarrow
\mathcal O_C(C+2K)\longrightarrow0
\]

is the precise modern meaning of “detaching \(C\).” It bounds the number of conditions by \(h^0(C,\mathcal O_C(C+2K))\), without assuming that the restriction map is surjective.

A shorter computation makes the exceptional case visible. Surface Riemann–Roch and Serre duality give

\[
P_2=\chi(\mathcal O_S)+K^2+h^1(2K)-h^0(-K).
\tag{VI-RR2}
\]

When \(KH>0\), \(h^0(-K)=0\), so

\[
P_2\geq\chi(\mathcal O_S)+K^2=p_a+p^{(1)}.
\]

For a regular surface this is \(P\geq p+p^{(1)}\), the formulas on pp. 220–221. The argument on p. 220 initially says that the restricted series is certainly nonspecial even for \(d=0\); degree \(2\pi-2\) alone does not justify that assertion. The printed theorem on p. 221 also retains \(d\geq0\), exactly as transcribed. Enriques then explicitly separates the exceptional \(K\sim0\) case on the same page and treats nontrivial degree-zero canonical class on p. 222. The correct final reading is the qualified statement, not an unqualified theorem contradicted by his next paragraph. There is no transcription error in the sign \(\geq\).

#### Equality and elliptic pencils

If \(q=0\) and \(C_0\in|K|\) is an integral canonical divisor, adjunction and

\[
0\to\mathcal O_S(K)\to\mathcal O_S(2K)
\to\omega_{C_0}\to0
\]

show that restriction is surjective because \(H^1(K)\simeq H^1(\mathcal O_S)^*=0\). Since \(h^0(\omega_{C_0})=p_a(C_0)=p^{(1)}\), one obtains \(P=p+p^{(1)}\), as on p. 221. Smoothness is convenient but unnecessary if the divisor is integral and its dualizing sheaf is used.

For \(K^2=0\) and a nonzero moving pluricanonical system, the associated fibration has genus-one fibres. Its base is \(\mathbf P^1\) when \(q=0\): pullback injects \(H^1(B,\mathcal O_B)\) into \(H^1(S,\mathcal O_S)\). Enriques's assertion that the canonical system decomposes into elliptic members is a structural description, not a proof of semiampleness in all cases; when \(p_g=0\) there is no effective canonical system at all. The statement must concern the effective pluricanonical systems. The modern abundance and genus-one-fibration results cover that distinction (Reid, 1996, §§E.4–E.7).

If \(K\sim(p-1)F\) with \(F\) a fibre and no extra fixed part, then

\[
P_2=h^0(\mathbf P^1,\mathcal O(2p-2))=2p-1,
\]

giving Enriques's \(P-1=2p-2\). Multiple fibres can make a fixed component become movable after doubling; then \(P-1>2p-2\). These are genuine effects of linear equivalence, not failures of the numerical bound.

For later verification, the precise characteristic-zero formula is useful. If \(f:S\to B\) is a relatively minimal genus-one fibration, \(F_j=m_jE_j\) its multiple fibres, and \(\mathcal L=(R^1f_*\mathcal O_S)^\vee\), then

\[
K_S\sim f^*(K_B+\mathcal L)+\sum_j(m_j-1)E_j,
\qquad \deg\mathcal L=\chi(\mathcal O_S).
\tag{VI-CBF}
\]

Thus, for \(B=\mathbf P^1\),

\[
P_m=\max\left\{0,\;1+m(\chi-2)+
\sum_j\left\lfloor\frac{m(m_j-1)}{m_j}\right\rfloor\right\}.
\tag{VI-F}
\]

The floor functions express the fact that only a whole multiple fibre moves. Reid (1996, §E.7.3) states the canonical-bundle formula and explains this divisor calculation; the applications to Enriques's particular examples below are independent computations. In positive characteristic, wild fibres require different coefficients; the characteristic-zero formula must not be transported unchanged.

#### The two numerically trivial cases

If \(q=0\) and \(K\sim0\), then \(p=1\), every \(mK\sim0\), and all \(P_m=1\). In (VI-RR2), the term \(h^0(-K)=1\) is precisely what defeats the preliminary bound \(P_2\geq p+p^{(1)}=2\). The adjoint identities \(|C|=|C'|=|C''|\), \(n=2\pi-2\), \(p^{(1)}=1\), and \(p-1=P-1=0\) on pp. 221–222 are all correct.

If \(q=p_g=0\) and \(K\equiv0\), then \(K\not\sim0\) and \(h^0(-K)=0\): a nonzero effective divisor has positive intersection with an ample divisor. Riemann–Roch for \(2K\) now gives \(h^0(2K)\geq1\). But an effective numerically trivial divisor must be zero. Hence \(2K\sim0\), \(P_2=1\), and \(K^2=0\). Therefore

\[
P_{2i}=1,\qquad P_{2i+1}=0.
\]

This is the clean cohomological repair of the compressed restriction argument on p. 222: it does not assume, without proof, that two distinct systems have different restrictions to \(C\). Kumar (2008, Lecture 17, Proposition 1) gives this order-two argument in modern notation. Such a complex surface is an Enriques surface; the \(K\sim0,q=0\) case is a K3 surface. These conclusions concern a minimal smooth model, not the branch-plane model before resolving and contracting exceptional curves.

#### The plane calculation and its printed sign error

On pp. 222–223, take \(C=7H\subset\mathbf P^2\). Then \(g(C)=15\), \(C^2=49\), \(K=-3H\), \(C'=4H\), and \(C''=H\). The line series on a septic is \(g^2_7\), with speciality

\[
h^1(C,\mathcal O_C(1))=h^0(C,\mathcal O_C(3))=10.
\]

Thus the nonspecial-series bound cannot be used. Enriques's genus addition calculation is \(0=p^{(1)}+3-12-1\), hence \(p^{(1)}=10=K^2+1\), while \(P_2=h^0(\mathbf P^2,-6H)=0\). All those numbers check.

There is, however, a genuine source sign misprint on p. 222: the scan prints \(-d=n-(2\pi-2)\) while calling this the negative canonical degree. With \(d>0\) as the following restriction calculation requires, the consistent formulas are

\[
d=n-(2\pi-2)>0,
\qquad KC=-d=2\pi-2-n.
\]

The transcription accurately preserves the printed error. The later \(-d=-3\) for a line on p. 223 independently confirms the intended convention.

#### Higher plurigenera and the \(P_6\) test

For \(m\geq2\) and \(KH>0\), the same calculation gives

\[
P_m=\chi(\mathcal O_S)+\binom m2K^2+h^1(mK)
\geq p_a+1+\binom m2(p^{(1)}-1).
\tag{VI-RRm}
\]

The restriction \(m\geq2\) is essential: setting \(m=1\) in the displayed lower bound on p. 223 would give \(p_g\geq p_g+1\) for a regular surface. It is implicit in the word “plurigenera” and in the extension from the bigenus. If \(q=0\) and \(C_0\in|(m-1)K|\) is integral, the exact sequence \(0\to\mathcal O_S(K)\to\mathcal O_S(mK)\to\omega_{C_0}\to0\) gives equality, since \(p_a(C_0)=1+\binom m2K^2\). This proves the particular equality Enriques states without needing a modern vanishing theorem. On a smooth minimal surface of general type in characteristic zero, nef-and-big vanishing gives the same equality for all \(m\geq2\), without the existence of an integral member at that particular level; this is an extension, not an extra hypothesis silently inserted into the old proof. Apply Esnault and Viehweg (1992, Corollary 5.12(c), pp. 48–49) with zero boundary and then Serre duality to \((m-1)K\), which is nef and big.

For \(q=p_g=0,P_2=1\) with the bicanonical divisor of positive order, (VI-RRm) gives \(P_m\geq1\) for every \(m\geq2\), in particular \(P_3\geq1\). Let \(D_2\in|2K|\) and \(D_3\in|3K|\). The two effective divisors \(3D_2,2D_3\in|6K|\) are distinct: equality would imply \(D_2=2E,D_3=3E\), and \(2(E-K)\sim3(E-K)\sim0\) would imply \(E\sim K\), contradicting \(p_g=0\). Thus \(P_6\geq2\), justifying the step only briefly indicated on p. 224. The statement that all plurigenera are positive refers to indices at least two; \(P_1=p_g\) remains zero.

Consequently, within the stated \(q=p_g=0,P_2=1\) class, \(P_3=0\) or \(P_6=1\) detects the order-two, numerically trivial canonical class, whereas positive-order bicanonical divisors give \(P_3\geq1,P_6\geq2\). This is the precise distinction used again on the supplied opening page of Chapter VII.

### VI.3. Double-plane examples, including the numerical defects (pp. 224–230)

#### The imported classification and its scope (pp. 224–225)

Enriques cites his *Sui piani doppi di genere lineare \(p^{(1)}=1\)*, *Rendiconti della R. Accademia dei Lincei*, April and May 1898. That is his reference, not a classification proved in these pages. The precise issue pagination and the completeness of that earlier classification have not been independently verified here. The present excerpt supplies examples and calculations.

A double plane branched over a smooth sextic has \(K\sim0\), \(q=0,p_g=1\), and all \(P_m=1\). If \(K^2=0\) and some \(P_m>1\), the pluricanonical genus-one fibration is preserved by the covering involution. On an invariant smooth genus-one fibre, the involution either has quotient \(\mathbf P^1\), with four branch points, or has a genus-one quotient, in which case the degree-two map is étale. Alternatively it interchanges fibres, inducing a degree-two map on the base. These are the geometric alternatives behind Enriques's two categories.

In category I, the fibres map to lines through \(O\). A branch curve of degree \(2n\) with an ordinary point of multiplicity \(2n-4\) leaves four branch points on a general such line. With multiplicity \(2n-3\), three residual branch points and one odd contribution over \(O\) again give four. Riemann–Hurwitz gives genus one. The asserted normal forms and allowed additional quadruple or \([3,3]\) singularities are imported from the 1898 analysis; the four-point calculation by itself does not prove their exhaustiveness.

In category II, the quotient pencil is a Halphen pencil: after nine blow-ups, it is \(|-sK_Y|\) on a rational surface \(Y\), with plane members of degree \(3s\) and nine points of multiplicity \(s\). Horizontal branch components would ramify a general fibre and change its genus, so the relevant branch components are fibres and possibly the distinguished anticanonical cubic. Cantat and Dolgachev (2012, Proposition 2.2 and §2.2) verify the modern Halphen description, including infinitely near base points and the unique multiple fibre of multiplicity \(s\) when \(s>1\). Enriques cites Enriques–Conforto, *Le superficie razionali*, for this earlier material. The \(\kappa=0\) Enriques examples below also carry chosen genus-one pencils, although such a pencil is not supplied by their constant pluricanonical ring.

#### The calculation that replaces “impure” and “infinitesimal” curves

For a smooth double cover \(\pi:X\to Y\) determined by \(B\in|2L|\),

\[
\pi_*\mathcal O_X=\mathcal O_Y\oplus\mathcal O_Y(-L),\quad
K_X=\pi^*(K_Y+L),
\]
\[
\chi(\mathcal O_X)=2\chi(\mathcal O_Y)+\tfrac12L(L+K_Y),\quad
K_X^2=2(K_Y+L)^2.
\tag{VI-DC}
\]

These formulas follow directly from the local algebra \(\mathcal O_Y\oplus L^{-1}\), the ramification formula, projection formula, and Riemann–Roch on \(Y\). They also give

\[
H^0(X,mK_X)=H^0(Y,m(K_Y+L))
\oplus H^0(Y,m(K_Y+L)-L).
\]

For singular branch curves one first uses the **canonical resolution**: blowing up a point of branch multiplicity \(b\) replaces \(L\) by \(\sigma^*L-\lfloor b/2\rfloor E\), and adds the exceptional curve to the new reduced branch divisor precisely when \(b\) is odd. This rule follows by removing the largest even power of a local exceptional equation from \(z^2=f\). On a smooth double-cover model, a branch \((-2)\)-curve pulls back to twice a \((-1)\)-curve; the latter must be contracted before computing the absolute \(p^{(1)}\). Enriques's “impure” canonical divisors comprise these exceptional contributions. His “infinitesimal” elliptic curves are actual exceptional curves on the resolved double cover, not formal infinitesimals in the modern scheme-theoretic sense.

Assume that the stated branch singularities are ordinary in the specified successive blow-ups and that no additional singularity changes the invariants. Write \(H,E_0,E_i,E_i'\) for the line class and the total-transform exceptional classes over \(O,A_i,A_i'\). For branch degree \(2n\), multiplicity \(2n-4\) at \(O\), and \(t\) aligned \([3,3]\) clusters, one obtains

\[
L=nH-(n-2)E_0-\sum_{i=1}^t(E_i+2E_i'),\qquad
K_Y+L=(n-3)(H-E_0)-\sum_{i=1}^tE_i'.
\]

Here the coefficient \(2E_i'\) is important: after the first odd triple blow-up the new branch also includes \(E_i\), making the second branch multiplicity four. Consequently

\[
K_X^2=-2t,\qquad \chi(\mathcal O_X)=n-1-t.
\]

The strict transform \(H-E_0-E_i-E_i'\) of each branch line and the strict transform \(E_i-E_i'\) are disjoint branch \((-2)\)-curves. Their \(2t\) lifts are \((-1)\)-curves. Contracting them gives \(K_S^2=0\). The resulting pencil has \(t\) multiple fibres of multiplicity two. For the examples in the text, the canonical adjoint calculation gives \(q=0\), hence \(p_g=n-2-t\). Formula (VI-F) becomes

\[
P_m=\max\{0,\ 1+m(n-3-t)+t\lfloor m/2\rfloor\}.
\tag{VI-I}
\]

This computation both verifies the numerical examples and makes their genericity assumptions explicit.

| Branch data in the excerpt | \(p_g=q+ p_a\), with \(q=0\) | Multiple fibres | \(P_2\) | \(P_3\) | \(P_6\) |
|---|---:|---|---:|---:|---:|
| \(D_8\), \(O^4\), one \([3,3]\) cluster (pp. 225–226) | \(1\) | one double fibre | 2 | 2 | 4 |
| \(D_8\), \(O^4\), two \([3,3]\) clusters (p. 226) | \(0\) | two double fibres | 1 | 0 | 1 |
| \(D_{10}\), \(O^6\), two \([3,3]\) clusters (pp. 226–227) | \(1\) | two double fibres | 3 | 3 | 7 |
| \(D_{10}\), \(O^6\), three \([3,3]\) clusters (p. 227) | \(0\) | three double fibres | 2 | 1 | 4 |

Entries not explicitly computed by Enriques are consequences of (VI-I), included as our extension of his checks.

**The first octic (pp. 225–226).** Bézout forces the line \(r=OA\) into the branch curve: its required intersection multiplicities exceed eight. The residual septic has \(O^3A^2A_1^2\). The canonical adjoint is the unique line \(r\) through \(O,A\), so \(p_g=1\), and (VI-DC) gives \(\chi=2\), hence \(q=0\). After the two exceptional curves are contracted, the canonical divisor is the reduced half-fibre \(E\), with \(2E\sim F\). Thus \(|2K|=|F|\), \(P_2=2\), and \(p^{(1)}=1\). The apparent disconnected rational canonical image on the singular plane model is not the canonical divisor on the smooth minimal model.

For completeness, the conics through \(A,A_1\) have class \(\Gamma=2H-E_A-E_{A_1}\), \(\Gamma^2=2\), and \(\Gamma B=10\). Their double covers have genus \(4\) by Riemann–Hurwitz, self-intersection \(4\), and canonical intersection \(2\); bicanonical intersection is \(4\). They form the stated \(\infty^3\), mapping to a double quadric cone with branch degree ten. These numerical claims check. The further projection description of \(D_{10}\), with triple point \(P\), infinitely near triple point \(P_1\), and the tangent-plane direction \(PP_1\), is a geometric construction sketched on p. 226; it is not independently developed there into a full resolution diagram.

**The second octic and an actual numerical error (p. 226).** With two clusters, Bézout gives

\[
B=r+s+D_6(O^2A^2A_1^2B^2B_1^2).
\]

There is no canonical adjoint line through \(O,A,B\) when these are not collinear, so \(p_g=0\); \(\chi=1\), \(q=0\), and \(2K_S\sim0\) with \(K_S\not\sim0\). Thus \(P_2=1,P_3=0\), exactly as Enriques says. His bicanonical “impure” divisor consists of twice the four exceptional curves before contraction; afterwards it is zero.

The four exceptional curves in the canonical resolution used here include two extra resolution \((-1)\)-curves over the clusters. Contracting these first leaves the two exceptional branch-line curves counted in Enriques's description; the difference in the number of curves is a difference of intermediate models, not a further numerical error.

The next sentence is internally inconsistent. The scan really says that the \(\infty^4\) of cubics through \(O,A,A_1,B,B_1\) gives genus \(4\), degree \(6\), and a **double cubic** surface, normal in \(S_4\), with branch degree \(10\). The indicated full cubic system has instead

\[
\Gamma=3H-E_0-E_A-E_{A_1}-E_B-E_{B_1}=-K_Y,
\quad \Gamma^2=4,\quad p_a(\Gamma)=1,\quad \Gamma B=8.
\]

Its pullback descends after contracting the four exceptional curves and has square \(8\) and genus \(5\). It has five sections, so its projective dimension is indeed four. The image of \(Y\) is a four-nodal **quartic** del Pezzo surface in \(\mathbf P^4\), and the one-dimensional branch curve has degree \(8\), with the nodes also involved in the double-cover construction. Thus, for the construction actually named, the consistent tuple is

\[
(\text{genus},\text{degree},\text{image degree},\text{branch degree})
=(5,8,4,8),
\]

not \((4,6,3,10)\). This repair is independently confirmed by Dolgachev (2016, §4, p. 13 in the author PDF): he describes exactly the anticanonical map from the blow-up of the five singular points of an Enriques octic, the four-nodal quartic, and branching in \(|\mathcal O_D(2)|\). The scan is not being silently emended; the old reading is retained in the correction register. Which different construction, if any, Enriques had in mind for the erroneous tuple is not established.

The promised sextic model with double tetrahedral edges is a forward reference, not proved on p. 226. It is announced again on the final supplied page.

**Two decic examples (pp. 226–227).** For \(D_{10}\) with \(O^6\) and two clusters, the forced lines \(r,s\) leave \(D_8(O^4A^2A_1^2B^2B_1^2)\). The canonical adjoint is the conic \(r+s\); after removing exceptional contributions the canonical divisor consists of the two reduced double fibres. With \(2E_A\sim2E_B\sim F\),

\[
K_S\sim E_A+E_B,\qquad 2K_S\sim2F.
\]

Hence \(p_g=1\), \(P_2=3>p+p^{(1)}=2\), and the bicanonical net corresponds to pairs of lines through \(O\). Linear equivalence must be retained: although \(K_S\equiv F\), it does not follow that \(K_S\sim F\); the latter would wrongly give \(p_g=2\).

Adding a third cluster forces the third branch line. There is no conic with a double point at \(O\) passing through three distinct directions \(A,B,E\): such a conic is a union of two lines through \(O\). Thus \(p_g=0\) and, by \(\chi=1\), \(q=0\). With three double fibres, the canonical formula is

\[
K_S\sim-F+E_A+E_B+E_E.
\]

It follows that \(2K_S\sim F\), \(3K_S\sim E_A+E_B+E_E\), and \(6K_S\sim3F\). These identities establish \(P_2=2,P_3=1,P_6=4\), and explain the three double members of the bicanonical pencil and the image by triples of lines. They verify every plurigenus asserted in this paragraph.

#### Halphen covers and an endpoint missed in the text (pp. 227–229)

Let \(Y\) be a Halphen surface of index \(h\), with \(J=-K_Y\) represented by its distinguished cubic. Then \(J^2=0\), the pencil is \(|hJ|\), and for \(a\geq0\),

\[
h^0(Y,aJ)=\lfloor a/h\rfloor+1;
\qquad h^0(Y,aJ)=0\quad(a<0).
\tag{VI-H}
\]

One proof is to use the unique multiple fibre \(hJ\), strip off the fixed remainder of \(aJ\), and identify the movable part with the pullback of \(\mathcal O_{\mathbf P^1}(\lfloor a/h\rfloor)\). This is exactly the feature recorded by the normal bundle of \(J\), of order \(h\) in \(\operatorname{Pic}^0(J)\); merely knowing the branch degree and nine multiplicities without the irreducibility and pencil information is not enough to fix all plurigenera. In the source's examples, however, the stated irreducibility actually forces the required index, so this is not an extra missing hypothesis. Indeed, write $a=qh+r$ with $0\leq r<h$. Every member of $|aJ|$ is the sum of $q$ fibres and the fixed divisor $rJ$. An irreducible reduced member with $a>1$ therefore forces $q=1,r=0$, hence $a=h$. Applied to the irreducible $D_{6n}$ and $D_{6n-3}$, this gives $h=2n$ and $h=2n-1$, respectively.

**First family: an irreducible \(D_{6n}\), \(n>1\).** Here \(h=2n\), \(B\sim2nJ\), and the covering line bundle is \(nJ\). Therefore

\[
K_X=(n-1)\pi^*J,\qquad \chi(\mathcal O_X)=2,
\]
\[
P_m=h^0(Y,m(n-1)J)+h^0(Y,(m(n-1)-n)J)
=\left\lfloor\frac{m(n-1)}n\right\rfloor+1.
\tag{VI-H1}
\]

In particular \(p_g=1,q=0,K^2=0,P_2=2\). The inverse image \(E=\pi^*J\) is the connected étale double cover of the distinguished cubic: the restriction of \(nJ\) to \(J\) is its nontrivial order-two line bundle. A general fibre of the genus-one pencil on \(X\) has class \(F=nE\). General fibres on \(Y\) split into pairs on \(X\), which is the geometric point of the Comessatti remarks in the footnotes. This splitting follows from the degree-two Stein factor on the base, or equivalently from the square criterion for the restricted cover; parity of intersection multiplicities alone is insufficient.

Thus \(2K_X\sim F+(n-2)E\), exactly explaining the moving elliptic component and fixed part of multiplicity \(n-2\) described on p. 228. But the printed statement that the fixed component is a \(1/(n-1)\)-part of \(L\) is wrong: it is a \(1/n\)-part. The source prints \((n-1)\)-ma, as does the transcription. Moreover,

\[
P_3=\begin{cases}2,&n=2,\\3,&n\geq3.\end{cases}
\]

The displayed \(P_3=3\) on p. 228 overlooks the allowed endpoint \(n=2\). More precisely, \(3K_X=2F+(n-3)E\) only when \(n\geq3\); at \(n=2\) one has \(3K_X=F+E\). Even for \(n>3\), “pairs of curves \(L\)” describes the movable part and leaves a fixed \((n-3)E\) unmentioned. These corrections are our explicit double-cover computation, not a claim that a named later author published an erratum to this page.

**Second family: \(D_{6n-3}+D_3\).** Now the Halphen index is \(2n-1\), the branch divisor is \(G+J\sim2nJ\), and \(J\) itself is branched. If \(E\) is its reduced inverse image, then \(\pi^*J=2E\), a general fibre is \(F=(2n-1)E\), and

\[
K_X=2(n-1)E,\qquad
P_m=\left\lfloor\frac{m(2n-2)}{2n-1}\right\rfloor+1.
\tag{VI-H2}
\]

For \(n>1\), this gives \(p_g=q+p_a=1\) with \(q=0\), \(K^2=0\), and \(P_2=2\), verifying the claims actually printed at the bottom of p. 228. Here \(2K_X=F+(2n-3)E\). The final sentence of the printed paragraph describes only the moving fibre and the doubled image \(D_3^{n-2}\), accounting for \(F+2(n-2)E\); it omits one reduced ramification cubic \(E\). This is visible already in the preceding construction: the ramification divisor is \(C_G+E\), and adding \(\pi^*((n-2)J)\) gives \(C_G+(2n-3)E\). At \(n=2\), the fixed part is still \(E\), whereas the final printed exponent would leave no fixed part. This is a source omission in the conclusion, not a transcription error; the preceding ramification construction and the asserted \(P_2=2\) are correct.

**The irregular extensions.** The sentence on p. 229 allows branch divisors composed of several Halphen fibres and says that in general \(p_a=1,p_g>1,p^{(1)}=1\). Under the stated vertical-cover assumptions, (VI-DC) still gives \(\chi=2\), and the Stein base of the lifted pencil can have genus \(b>0\). Then \(q=b\), \(p_g=1+b\), and \(K^2=0\). The source makes a broad structural remark, not a classification of every possible singular fibre configuration. Its first subscript is \(a\); it must not be changed to \(i\) or to \(g\).

#### The decic \(D_9+r\) (pp. 229–230)

Enriques cites two papers of L. Campedelli in the *R. Accademia dei Lincei* (1932), with titles transcribed in the bibliography below. The earlier existence and classification are assumed. The stated branch is a Halphen nonic with nine triple points, three pairs infinitely near and the other three on \(r\), together with \(r\). The points \(A,B,E\) are not collinear. Any candidate canonical conic through the six specified proper points would contain \(r\), leaving an impossible line through \(A,B,E\); hence \(p_g=0\). The branch line has self-intersection \(-2\) on the resolved base and lifts to an exceptional \((-1)\)-curve. Removing it is necessary for the absolute genus calculation. A direct invariant calculation supplies the other needed information: a smooth decic double plane starts with \(\chi=7,K^2=8\). The three proper triple points of the nonic on \(r\) are quadruple points of the total branch, and the second point in each of the three \([3,3]\) clusters also has total branch multiplicity four after the first odd blow-up. These six multiplicity-four steps each lower \(\chi\) by one and \(K^2\) by two. The intervening multiplicity-three steps change neither. Hence the smooth canonical resolution has \(\chi=1,K_X^2=-4\). The branch line and the three first exceptional branch \((-2)\)-curves lift to four \((-1)\)-curves; contracting them gives \(K_S^2=0\). With \(p_g=0\), this also proves \(q=0\).

On the minimal surface, let \(C_2\) be the irreducible bicanonical elliptic curve represented by the cubic \(D_3\), and \(C_3\) the tricanonical elliptic curve represented by \(D_9\). The geometric description yields

\[
2K_S\sim C_2,\qquad3K_S\sim C_3,\qquad
6K_S\sim3C_2\sim2C_3=F.
\]

Thus the fibration has a triple fibre \(3C_2\) and a double fibre \(2C_3\), with \(\chi=1\). Formula (VI-F) gives

\[
P_m=\max\{0,\;1-m+\lfloor m/2\rfloor+\lfloor2m/3\rfloor\},
\]

so \(P_2=P_3=1,P_6=2\), in agreement with the stated invariants. These numbers provide a concrete example of the positive-order case distinguished in §2. The isolation of \(C_3\) can also be justified without invoking the whole formula: if \(|3K|\) moved and a member passed through a point of \(C_2\), the zero intersection \(C_2(3K)=0\) would force containment of \(C_2\), leaving an effective canonical divisor, a contradiction.

The sentence near the end of p. 230 nevertheless calls the unique tricanonical image \(D_3\). The scan confirms that subscript. It is a source slip: \(D_3\) has just been identified as bicanonical, while \(D_9\) is tricanonical. The claimed \(P_3=1,P_6=2\) is unaffected. The statements about irreducibility of the lifted cubic and nonics rely on Comessatti's criterion, cited through Enriques–Chisini, Book V, Chapter IV, §38, vol. III, p. 445. This audit checks their compatibility with the divisor and fibration calculation; it does not supply new equations for the branch curve or independently re-prove the existence of the required nine-point configuration.

### VI.4. Castelnuovo's rationality criterion (pp. 230–235)

#### Exact statement and what the excerpt establishes

For a smooth projective surface over an algebraically closed field of characteristic zero,

\[
S\text{ is rational}\quad\Longleftrightarrow\quad q(S)=0,\ P_2(S)=0.
\]

Equivalently, in Enriques's notation, \(p_a=P_2=0\). Indeed a nonzero canonical section has a nonzero square, so \(P_2=0\) implies \(p_g=0\); hence \(p_a=p_g-q=0\) then implies \(q=0\). Rationality gives the converse vanishing by birational invariance and the direct calculation on \(\mathbf P^2\). Vanishing of \(p_g,q\) alone is insufficient, as the preceding Enriques examples show.

The source credits Castelnuovo's *Sulle superficie di genere zero* (1896), citing *Memorie scelte*, p. 307. It explicitly uses earlier rationality theorems of Noether and Clebsch–Noether, referring to Enriques–Conforto. The present argument is substantial: it divides into two cases, analyses the last adjoints, and treats a fixed-component case. It is not merely an assertion of the criterion. Nevertheless some residual-system and irreducibility steps are compressed into assertions, so the historical proof should not be labelled fully expanded in modern foundations.

#### Case I: a system of negative canonical intersection (pp. 231–234)

Take an irreducible moving system \(C\) with \(n=C^2>2\pi-2\); equivalently \(KC<0\). After making it a suitable hyperplane system, put \(d=n-(2\pi-2)>0\). The adjoints \(C+jK\) have degrees against \(C\)

\[
2\pi-2,\quad2\pi-2-d,\quad2\pi-2-2d,\ldots.
\]

A positive ample degree cannot become negative for an effective divisor, so this process terminates. The proof assumes that the last system of positive dimension can be tracked through removing fixed components and, if necessary, replacing a system by its moving part.

If the last irreducible system has no positive-dimensional adjoint, its genus is zero or one. The relevant cohomological fact is

\[
0\longrightarrow\mathcal O_S(K)\longrightarrow
\mathcal O_S(K+D)\longrightarrow\omega_D\longrightarrow0.
\]

For \(p_g=q=0\) and a smooth irreducible \(D\), it yields \(h^0(K+D)=g(D)\). Thus an adjoint of projective dimension at most zero means \(g(D)\leq1\). This fills in the numerical step on p. 231.

If the genus is zero, a pencil of rational curves makes the surface rational. On resolving its base points, the generic fibre is a genus-zero curve over \(\mathbf C(t)\); the Noether–Enriques theorem, or the existence of a rational section over this field, gives a birational ruled surface over \(\mathbf P^1\). Enriques assumes that result from earlier work.

For an elliptic complete system of dimension \(r\geq2\), the sequence \(0\to\mathcal O_S\to\mathcal O_S(D)\to\mathcal O_D(D)\to0\) and \(q=0\) show that its characteristic series is complete. Since \(D^2>0\), curve Riemann–Roch gives \(r=D^2\). Imposing \(r-2\) general simple base points leaves a net of degree two on the blown-up surface. Its general member has genus one, so the resulting double-plane branch has degree four. This is the classical Clebsch case, whose rationality is imported. “Containing a net of degree two” includes the imposed base points; merely taking an arbitrary three-dimensional subspace would not lower \(D^2\).

If the final elliptic system is a pencil, Enriques passes to the preceding genus-two system, of dimension at least two. He argues that the hyperelliptic conjugate of a point remains fixed as the curve varies through that point; otherwise it traces a rational component of the elliptic pencil. This is a geometric sketch of the existence of a surface involution. For an adjoint \(D=K+C\), \(p_g=q=0\) and smooth connected \(C\), the same cohomology sequence gives \(H^1(S,D)=0\): the map \(H^1(\omega_C)\to H^2(K)\) is the trace isomorphism. Hence its characteristic series is not only complete but nonspecial.

On a hyperelliptic curve of genus \(g\), a complete series composed with the hyperelliptic \(g^1_2\) is a multiple \(a g^1_2\) only while no extra anti-invariant sections appear. If it is also nonspecial, the borderline value is \(a=g\), giving degree \(2g\) and projective dimension \(g\). For a surface system of dimension \(r\), the characteristic projective dimension is \(r-1\), so

\[
g=r-1,\qquad D^2=2(r-1).
\]

For \(g=2\), this gives \(r=3,D^2=4\), exactly the \(\infty^3\) printed on p. 232. The map has degree two onto a quadric. In the branch configuration retained after excluding rational pencils, the quadric is a cone; its ruling has three moving branch points and the vertex supplies the fourth. A smooth quadric would have branch bidegree \((a,b)\) with even entries and \(a+b=6\); one ruling then has at most two branch points, returning to a rational pencil already disposed of. This gives the missing qualification behind the short parity argument in the text: degree six alone does not force bidegree \((3,3)\). The double-cone model is birational to Noether's double plane with a sextic having an infinitely near pair of triple points. Its rationality is again assumed, not established anew in this subsection.

#### Fixed parts and composite adjoints (pp. 232–234)

If an adjoint has fixed part \(\theta\) and an irreducible moving part of dimension at least two, Enriques says that one can continue after stripping \(\theta\). This requires control of the cohomology and arithmetic genus of the new system; a fixed-part removal does not automatically preserve all the vanishing statements just proved for an actual adjoint. The excerpt does not supply that control in full generality.

For a moving part composed with a pencil \(|L|\), regularity makes the base rational. Rational members settle rationality immediately. Otherwise, let their genus be \(\rho>0\). The fixed part is fundamental for the preceding irreducible system: the restricted canonical series has no base points, so \(\theta\) cannot meet a general preceding member. Restriction of the complete canonical series to that member is composed with the pencil. Its degree \(\nu>1\) is necessarily two, since a canonical map of a nonhyperelliptic curve is birational. The preceding curves are therefore hyperelliptic, and the pencil consists of their bisecants.

Using completeness and nonspeciality again, the text obtains

\[
n_{h-1}=2(r_{h-1}-1),\qquad
\pi_{h-1}=r_{h-1}-1.
\]

Subtracting \(L\) is said to impose two conditions and to lower the genus by one. If the residual curve has the required connectedness and arithmetic genus, the addition formula

\[
\pi_{h-1}=(\pi_{h-1}-1)+\rho+i-1
\]

with \(i=L\cdot(\text{residual})\geq1\) gives \(\rho+i=2\), hence \(\rho=i=1\). These numerical deductions are correct. The omitted issue is establishing those residual hypotheses and the asserted behaviour after all fixed parts have been removed. Connectedness of the original member alone should not be substituted for an argument about every residual system.

On an elliptic curve a degree-one complete linear series is fixed. Enriques uses this to conclude that residual curves split into members of the pencil and that the degree-two image is a cone of degree \(m=r_{h-1}-1\). The hyperelliptic branch degree on a general hyperplane section is \(2+2\pi_{h-1}=2m+2\). Each ruling must contain at least three moving branch points if its double cover has positive genus. Therefore

\[
3m\leq2m+2,
\]

so \(m\leq2\). The excluded plane/rational cases leave \(m=2\), the quadric-cone case already treated. This verifies the arithmetic of pp. 233–234 while identifying the geometric assertions that remain sketched.

#### Case II and a modern complete replacement (pp. 234–235)

If every relevant irreducible moving system satisfies \(KC\geq0\), Enriques uses §2 to deduce \(P_2\geq p^{(1)}\). Since \(P_2=0\), \(p^{(1)}\leq0\), so \(K^2\leq-1\). Successive adjoints decrease intersection with \(K\) by \(K^2\); either an adjoint violates the assumed nonnegativity, or the process terminates and returns to Case I. His final assertion that an appropriate multiple of a reducible system can be combined with a regular system to produce an irreducible system is another indicated construction rather than a proof in the excerpt.

A modern proof avoids these residual-system choices. Contract \((-1)\)-curves. The surface minimal-model theorem gives a minimal model with \(K\) nef, or a geometrically ruled/rational model. Suppose \(K\) were nef. Because \(P_2=0\), \(p_g=0\); together with \(q=0\), this gives \(\chi=1\). Riemann–Roch for \(-K\) and Serre duality yield

\[
h^0(-K)+h^0(2K)=1+K^2+h^1(-K)\geq1.
\]

Thus \(-K\) is effective. A nef \(K\) has nonnegative intersection with an ample class, whereas a nonzero effective \(-K\) has positive ample degree, a contradiction. If the divisor is zero instead, then \(K\sim0\), contradicting \(P_2=0\). Hence the minimal model is ruled or rational. For a ruled model over \(B\), \(q=g(B)\); therefore \(B\simeq\mathbf P^1\), and the surface is rational.

This is a complete proof **relative to the surface minimal-model theorem**, not a claim to re-prove that theorem in a paragraph. Hassett (2009, Theorem 2.26, p. 178, with Corollary 2.20) supplies this modern formulation; Kumar (2008, Lecture 9, Theorem 1 and its reductions) supplies an alternative proof closer to the classical adjunction method. Zariski's *On Castelnuovo's criterion of rationality \(p_a=P_2=0\) of an algebraic surface* (1958) is the precise later reference for the characteristic-\(p\) rationality theorem, as explicitly recorded by Hassett (2009, Remark 2.29). It is an extension and foundational treatment, not evidence that the characteristic-zero theorem was false. The accompanying *The problem of minimal models in the theory of algebraic surfaces* (1958) addresses the minimal-model foundations. These references are not being used to attribute the local misprints on pp. 222, 226, or 228 to a documented historical erratum.

The algebraically closed hypothesis matters. A smooth anisotropic quadric over \(\mathbf R\) can have \(q=P_2=0\) and no real point, hence cannot be \(\mathbf R\)-rational. The classical criterion concerns geometric rationality, not arbitrary-field rationality. In positive characteristic the cohomological \(q=h^1(\mathcal O)\) must also be distinguished from the dimension of a possibly nonreduced Picard scheme; none of the complex-analytic identifications should be silently transferred.

### VI.5. Further deductions and research questions from this audit

The following are our deductions or proposed exercises, not claims attributed to Enriques.

1. **All plurigenera of the displayed examples can be recovered, not just \(P_2,P_3,P_6\).** Equations (VI-I), (VI-H1), (VI-H2), and the \((2,3)\)-fibre formula give periodic corrections to linear growth. Confidence: high under the explicitly stated ordinary-singularity and irreducible-Halphen-member hypotheses, because both the double-cover eigensheaf computation and the canonical-bundle formula give the same values. This also pinpoints the \(n=2\) defect in the first Halphen family.
2. **An explicit resolution graph would be a useful next artifact.** Start with the four category-I branch configurations, record parity at every blow-up, then contract the lift of each branch \((-2)\)-curve. This would make “impure” canonical divisors and the different counts of exceptional curves fully visible. Confidence: high for the numerical procedure; existence and generic smoothness of the prescribed branch curves must still be checked in any chosen equation.
3. **A textual-history question remains.** Was the inconsistent p. 226 tuple copied from a different projection construction, or is it a cluster of printing mistakes? The quartic reconstruction is mathematically determined by the named cubic system and confirmed in the modern literature, but the author's intended editorial correction is not recoverable from these leaves alone. This is an unresolved historical question in this audit, not an asserted open problem in surface theory.
4. **The original proofs can be compared without erasing their strengths.** The component proof of \(K^2\geq0\) and the \(P_6\) product argument require little modernization; the adjoint-system proof of rationality needs more infrastructure. Confidence: high. The precise lesson is to track arithmetic genus, fixed components, and linear rather than numerical equivalence, rather than to assign a blanket “Italian-school gap” to the chapter.

## Supplied opening of Chapter VII (unnumbered leaf, inferred p. 237)

The PDF includes the blank p. 236 and the opening leaf of Chapter VII. The latter is outside the filename's stated endpoint and ends after item 2 of a continuing list. It must be recorded rather than silently discarded or completed from memory.

For regular \(p_g=0,P_2=1\) surfaces, the opening repeats that \(P_3=0\), equivalently \(P_6=1\), distinguishes the zero bicanonical divisor on the minimal model. In modern terms this is \(K\not\sim0,2K\sim0\), hence an Enriques surface in characteristic zero. Those claims were established in VI.2, so their status here is “assumed from earlier work” within this book.

The announced double-plane model has branch \(D_8=D_6+p+q\), where the sextic has tacnodes at \(M,N\), tangent lines \(p,q\), and a node at \(p\cap q\). The sextic-with-double-tetrahedral-edges model is announced next. Neither birational construction is proved on this leaf. They cannot be counted as completed proofs in the supplied excerpt. Dolgachev (2016, §2, pp. 3–5) confirms the Enriques octic and tetrahedral sextic models, including appropriate degenerations. He identifies modern proofs with Artin's Harvard dissertation (1960) and work of Averbuch (1965). These exact historical attributions are verified through that source; the dissertations themselves were not consulted here.

The two numbered assertions actually present are:

\[
C^2=2p_a(C)-2,
\qquad
\dim|C|\geq p_a(C)-1
\]

for the indicated effective curve systems on a minimal Enriques surface. The first is adjunction with \(K\equiv0\). For nonzero effective \(C\), \(h^0(K-C)=0\), because \((K-C)H<0\); Riemann–Roch then gives \(h^0(C)\geq1+C^2/2=p_a(C)\), proving the second. “Genus” must mean arithmetic/virtual genus when \(C\) is singular. The proviso concerning base points concerns how the older system's degree is measured; the cohomological inequality itself holds for every nonzero effective Cartier divisor. The next item and the promised classification are absent from the supplied files.

### Verified modern references used in this chapter

- Cantat, S., & Dolgachev, I. (2012). Rational surfaces with a large group of automorphisms. *Journal of the American Mathematical Society, 25*(3), 863–905. https://doi.org/10.1090/S0894-0347-2012-00732-2. Author copy: https://sites.lsa.umich.edu/idolga-new/wp-content/uploads/sites/1467/2024/08/jams12.pdf. Proposition 2.2 and §2.2 were checked for the Halphen index, infinitely near points, and multiple fibre.
- Dolgachev, I. V. (2016). A brief introduction to Enriques surfaces. In *Development of moduli theory—Kyoto 2013* (*Advanced Studies in Pure Mathematics*, Vol. 69, pp. 1–32). Mathematical Society of Japan. Author copy: https://sites.lsa.umich.edu/idolga-new/wp-content/uploads/sites/1467/2024/08/Kyoto13.pdf; arXiv record https://arxiv.org/abs/1412.7744. Sections 2 and 4 were checked, especially the octic/sextic models, the Artin/Averbuch attribution, and the degree-eight polarization giving a double quartic del Pezzo.
- Esnault, H., & Viehweg, E. (1992). *Lectures on vanishing theorems* (DMV Seminar, Vol. 20). Birkhäuser. https://page.mi.fu-berlin.de/esnault/books/esvibuch.pdf. Corollary 5.12(c), printed pp. 48–49, supplies the nef-and-big vanishing used in the general-type extension.
- Hassett, B. (2009). Rational surfaces over nonclosed fields. In H. Darmon, D. A. Ellwood, B. Hassett, & Y. Tschinkel (Eds.), *Arithmetic geometry* (*Clay Mathematics Proceedings*, Vol. 8, pp. 155–209). American Mathematical Society. https://www.claymath.org/wp-content/uploads/2022/03/cmip08c.pdf. Corollary 2.20, Theorem 2.26 (printed p. 178), Remark 2.29, and the Zariski bibliography were checked.
- Kumar, A. (2008). *Algebraic surfaces, Lecture 9: Castelnuovo's criterion for rationality*. MIT OpenCourseWare, 18.727. Notes prepared by Kartik Venkatram in collaboration with Abhinav Kumar. https://ocw.mit.edu/courses/18-727-topics-in-algebraic-geometry-algebraic-surfaces-spring-2008/01d543f81d0b743f06deed68d9eec77d_lect9.pdf. Theorem 1 and reductions 1–2 were checked.
- Kumar, A. (2008). *Algebraic surfaces, Lecture 17: Enriques surfaces*. MIT OpenCourseWare, 18.727. Notes prepared by Kartik Venkatram in collaboration with Abhinav Kumar. https://ocw.mit.edu/courses/18-727-topics-in-algebraic-geometry-algebraic-surfaces-spring-2008/9fa718160b9c9c0ecc0dceeaa339e644_lect17.pdf. Proposition 1 was checked for the order of the canonical bundle.
- Reid, M. (1996). *Chapters on algebraic surfaces*. arXiv:alg-geom/9602006. https://arxiv.org/pdf/alg-geom/9602006. This is the consulted preprint version; §E.7.3 gives the tame canonical-bundle formula, §E.7.7 explains the wild-fibre qualification, and §§E.4–E.7 give the relevant abundance framework. No unverified pagination from the later printed version is substituted.
- Zariski, O. (1958). On Castelnuovo's criterion of rationality \(p_a=P_2=0\) of an algebraic surface. *Illinois Journal of Mathematics, 2*(3), 303–315. https://doi.org/10.1215/ijm/1255454536. Bibliographic details and its role in the positive-characteristic extension were verified through Hassett's reference list and Remark 2.29; the full original proof was not retrieved.
- Zariski, O. (1958). The problem of minimal models in the theory of algebraic surfaces. *American Journal of Mathematics, 80*, 146–184. Bibliographic details and its role were verified through Hassett's reference list and Remark 2.29; no theorem number from the original is claimed.

### Earlier work cited by Enriques in these pages

The following records reproduce the excerpt's attributions and distinguish them from independently read modern sources: Enriques (1898), *Sui piani doppi di genere lineare \(p^{(1)}=1\)*, Lincei, April and May; Enriques–Conforto, *Le superficie razionali*, Zanichelli, Bologna; Enriques–Chisini, Book V, Chapter IV, §38, vol. III, p. 445, for the Comessatti criterion; Campedelli (1932), *Sui piani doppi con curva di diramazione del 10° ordine* and *Sopra alcuni piani doppi notevoli con curva di diramazione del 10° ordine*, Lincei; Castelnuovo (1896), *Sulle superficie di genere zero*, Società Italiana delle Scienze (dei XL), reprinted in *Memorie scelte*, p. 307. Missing issue or page details have not been invented.


## Cross-chapter reference guide

The chapter bibliographies above contain the verified modern sources and distinguish them from Enriques's own historical footnotes. The following entries supply the common background cited in the Introduzione and connect the principal modern replacements to precise consulted locations. Dates and theorem numbers refer to the identified editions.

- Beauville, A. (1978). *Surfaces algébriques complexes* (Astérisque, No. 54). Société Mathématique de France. Bibliographic record: https://www.numdam.org/item/AST_1978__54__R1_0/ . Consulted full text: https://smf.emath.fr/system/files/filepdf/AST_1978__54__R1_0.pdf . Verified locators: Theorems I.11 (duality) and I.12 (Riemann–Roch), I.14 (Noether's formula), I.15 (arithmetic genus), I.16 (normalization correction), and I.17 (adjunction); Chapter II gives the birational framework.
- Brosnan, P. (n.d.). *UMD 808J: Algebraic surfaces—Riemann–Roch for surfaces*. University of Maryland. https://www.math.umd.edu/~pbrosnan/notes/Surfaces/sect0017.html . Theorem 3.4 states surface Riemann–Roch and identifies Hartshorne's corresponding locator as V.1.6. The online proof contains minor letter inconsistencies; this audit writes the exact-sequence proof independently with consistent notation.
- Enriques, F. (1949). *Le superficie algebriche*. Zanichelli. Primary audit source: the supplied scan excerpt and its separately identified first-pass TeX. Publication identity was checked against the Federigo Enriques chronological bibliography: https://www.federigoenriques.org/indice-cronologico-delle-opere/ . The absence of p. 186 and the true terminal leaf are documented in the method file.

| Modern input or repair | Verified source and locator | Precise role |
|---|---|---|
| Canonical divisors and adjunction | Reid (1996), §§A.10–A.12 | Arithmetic/dualizing-sheaf formulation; not a claim that singular geometric genus equals arithmetic genus |
| Duality, arithmetic genus, and Noether's formula | Beauville (1978), Theorem I.11 and §§I.14–I.17 | Separates cohomological, arithmetic, geometric, and topological invariants |
| Surface Riemann–Roch | Reid (1996), §B.9(ix); Brosnan, Theorem 3.4 | Euler characteristic and the cohomological correction terms in plurigenus estimates |
| Hodge index and nef divisors | Reid (1996), §§D.2.2–D.2.3 | Numerical positivity and the distinction between numerical and linear equivalence |
| Complex Riemann existence | Grothendieck (Ed., 2003), SGA 1, Exposé XII, Theorem 5.1, original pp. 332–333 | Algebraization of the unramified cover; normalization and branch-local smoothness are checked separately |
| Nodal plane-curve complements | Deligne (1981), Introduction and Theorem 1; Fulton (1980) | Correctly scoped topological and tame algebraic results and the limitation of the older historical proof |
| Equisingular tangent and obstruction spaces | Tannenbaum (1984), §1; Wahl (1974), as corroborated there and by Guffroy (2003); Vakil (2006), Main Theorem 1.1, M5a–M5b | Replaces a universal characteristic-completeness assertion by a deformation problem with possible obstructions |
| Moduli lower bound | Catanese (2013), §1.3, preprint p. 13 | Explicit Enriques–Kuranishi attribution and the inequality from tangent minus obstruction dimension |
| Minimal models and rationality | Hassett (2009), Corollary 2.20, Theorem 2.26, published p. 178; Kumar (2008), Lecture 9, Theorem 1 | Complete replacement for the compressed residual-system proof, relative to the surface minimal-model theorem |
| Genus-one canonical-bundle formula | Reid (1996), §E.7.3, with the qualification in §E.7.7 | The characteristic-zero multiple-fibre terms used in all plurigenus calculations |
| Nef-and-big vanishing | Esnault and Viehweg (1992), Corollary 5.12(c), pp. 48–49 | The stated extension of the general-type plurigenus equality |
| Halphen pencils | Cantat and Dolgachev (2012), Proposition 2.2 and §2.2 | Exact index, distinguished anticanonical cubic, and multiple fibre |
| Enriques models | Dolgachev (2016), §§2 and 4, especially author-PDF p. 13 | Independently confirms the corrected quartic del Pezzo model on p. 226 and the octic/sextic descriptions |

The double-cover eigensheaf and canonical-resolution calculations, the conductor identification of the p. 191 cover, the corrected intersection expansions, and the Halphen endpoint/fixed-part repairs are derived explicitly in this commentary. A modern reference supplying the general method is not represented as a published erratum to Enriques. No historical priority is claimed for these audit calculations.
