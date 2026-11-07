# Mathematical commentary and check: Enriques, Chapter IV

**Source:** Federigo Enriques, *Le superficie algebriche* (Zanichelli, 1949), Chapter IV, “Il genere numerico e il teorema di Riemann–Roch per le superficie,” supplied scan positions corresponding to pp. 101–166. The mathematical text occupies pp. 101–165; the final supplied page, position 66, is blank. The chapter contains 21 numbered sections, including its own §1, *Introduzione*. No separate introductory chapter or other chapter is present in these attachments.

This commentary follows those 21 sections. The accompanying `claims.csv` is the more granular register of definitions, assertions, displayed computations, examples, historical assertions, and proof steps. The correction register distinguishes what the scan actually prints from the mathematical reading that should replace it. A mathematical repair does not silently become a transcription correction.

## Conventions essential to reading this chapter

Unless a passage explicitly concerns a reducible degeneration, let $X$ be a smooth, connected, projective surface over $\mathbb C$, obtained when necessary by resolving the surface model in ordinary projective space. Intersections and coherent cohomology are computed on this smooth model. The distinction between this $X$ and Enriques’s possibly nonnormal projected image $F\subset\mathbb P^3$ is indispensable.

| Enriques’s terminology | Modern interpretation and qualification |
|---|---|
| *Singolarità normali* of a projected surface | Ordinary projection singularities, involving a double curve and ordinary special points. This does **not** mean a normal scheme. |
| Complete system $\lvert D\rvert$, dimension $r$ | $\mathbb P H^0(X,\mathcal O_X(D))$, with $r=h^0(D)-1$; the empty system has dimension $-1$. A formula for a complete system is not a lower bound for an arbitrary proper vector subspace. |
| Degree $n$ of a system | $D^2$, after resolving its assigned base points in the convention being used; it is not generally the degree of an ambient embedding. |
| Genus $\pi$ of a system | For a smooth general member, its geometric genus. In the virtual calculus, $p_a(D)=1+\frac12D(D+K_X)$, including reducible and nonreduced divisors. These meanings coincide only under the corresponding smoothness assumptions. |
| Geometric genus $p_g$ | $h^0(X,K_X)=h^2(X,\mathcal O_X)$. |
| Numerical or arithmetic genus $p_a$ of the surface | $\chi(X,\mathcal O_X)-1=p_g-q$, where $q=h^1(X,\mathcal O_X)$. It can be negative. It must not be confused with $p_a(D)$. |
| Regular surface | $q=0$. This has no connection with the local-ring use of “regular.” |
| Adjoint $D'$ | $K_X+D$, with the exceptional corrections required when moving between surface models or imposing multiple base points. |
| Speciality index $i$ of a surface system | $h^0(K_X-D)=h^2(D)$. It is not $h^1(D)$. |
| Superabundance $\omega$ | $h^1(X,\mathcal O_X(D))$. Thus regularity of a complete system means $h^1(D)=0$, not Castelnuovo–Mumford regularity. |
| Characteristic series of $\lvert D\rvert$ | The image of $H^0(X,D)\to H^0(D,\mathcal O_D(D))$, after removing its one-dimensional kernel. Its projective dimension is $r-1$. |
| Deficiency of a series | Codimension of the image in the complete space of sections of the restricted line bundle. An incomplete series is not thereby a special line bundle. |
| *Normale* in the projective discussion on p. 136 | Linearly normal: embedded by a complete hyperplane system. This must not be substituted by normality of the local rings or by projective normality of the whole homogeneous coordinate ring. |
| Fundamental curve of a system | A curve contracted by the associated map; for a free system, its intersection with the system is zero. Ample divisors have no such curves. |
| “Normally large” relative to $D$ | For the repaired restriction theorem, a precise sufficient condition is a family $sH+E_0$, with $H$ ample and $E_0$ fixed, or the specified cohomological vanishing. The literal effective-domination condition in §10 is weaker and does not by itself guarantee the conclusion. |
| Linear genus $p^{(1)}$ | $K_X^2+1$ for the model relevant to the passage. The relative value changes under blowup; the “absolute” or “pure” value in §§18–20 is associated with the minimal model. |
| Pure versus impure canonical system | The exceptional fixed contributions caused by blowing up have been removed, or retained, respectively. The distinction changes superabundance even though plurigenera remain birational invariants. |
| Arithmetic connectedness in §17 | Numerical 1-connectedness: every decomposition $D=A+B$, with $A,B>0$, satisfies $A\cdot B>0$. For nonreduced divisors it is stronger than connectedness of the underlying topological support. |
| The symbol $\equiv$ in §§14 and elsewhere | In the source it often denotes equivalence of linear systems, hence linear equivalence. Modern numerical equivalence is explicitly written $\equiv_{\mathrm{num}}$ here; algebraic equivalence is also named explicitly. |

These identifications make the main formula of the chapter transparent:

$$
\boxed{\quad r=p_a(X)+D^2-p_a(D)+1-h^0(K_X-D)+h^1(D).\quad}
$$

It is exactly surface Riemann–Roch together with Serre duality, not an approximation. Enriques’s inequality is obtained by dropping the nonnegative final term. Precise modern starting points are Beauville (1996, Theorems I.11–I.12 and Remarks I.13) and the independent proofs and exact sequences given below.

## How the proof diagnoses are used

“Proved” in the register means that the excerpt supplies an argument, judged in the stated classical framework. It does not mean that every prerequisite is reproved in these pages. “Sketched” records a compressed argument or an explicit omission of details. “Assumed from earlier work” preserves Enriques’s own attribution or cross-reference; it does not certify that an unavailable earlier source has been inspected. A row can therefore be classified “proved” and still identify an invalid step. The classification describes what the author does; the error field evaluates it.

The commentary distinguishes three kinds of mathematical intervention. First, some printed formulas contain local sign, index, or constant errors and can be repaired by direct calculation. Second, some statements need a hypothesis made explicit, such as completeness, positive ample degree, or passage to a minimal model. Third, several assertions fail when read with the scope actually printed; the worked counterexamples below explain their precise scope. The results depending on those assertions are checked again with valid positivity hypotheses or exact sequences.

The central gap in the supplied proof is explicit: on p. 155 Enriques assumes that a numerically 1-connected nonreduced divisor detaches with its full multiplicities in the indicated pencil. The modern cohomological replacement proves the required adjoint regularity, without asserting that the exact historical pencil formulation has thereby been verified. The replacement theorem says that a numerically 1-connected effective divisor has only constant global functions; the divisor exact sequence then proves adjoint regularity on a surface with $q=0$. A specific subsequent repair is Ramanujam (1972, Lemma 3; reprint p. 127), whose introduction expressly discusses the missing lemma in Franchetta's approach. Reid (1996, Lemma 3.11) gives an accessible proof. For the later bicanonical argument, Catanese et al. (1999, Theorem 3.3) prove global generation of the dualizing sheaf of a numerically 2-connected Gorenstein curve, apart from the rational exception. These verified sources establish the replacement theorems; no unsupported claim of absolute historical priority is intended.

References to Zariski, Kodaira, Mumford, or later classifications are made only where the stated theorem requires them. The chapter’s core dimension computations do not need the full classification of surfaces. In particular, one must not cite a positive-characteristic classification as though it automatically repaired a complex-geometric vanishing argument.

## Chapter IV, including its Introduzione

### §1. The curve model for the argument (pp. 101–102; A001–A010)

Enriques starts from results already established in Enriques–Chisini, Book V, volume III: complete linear series on a curve, the birational invariance of the canonical series, completeness of plane adjoints, and curve Riemann–Roch. The excerpt does not prove these foundational theorems. It explains why their method suggests a surface analogue.

Let $C_0\subset\mathbb P^2$ be an integral plane curve of degree $m$ with only ordinary nodes, let $\nu:C\to C_0$ be its normalization, and let $g=g(C)$. If $Z$ is the node scheme, its length is

$$
 d=\frac{(m-1)(m-2)}2-g.
$$

Each node has normalization delta-invariant one. With $H=\nu^*\mathcal O_{C_0}(1)$ and $G$ the sum of the two branches over every node, adjunction gives

$$
 K_C\sim(m-3)H-G.
$$

Thus degree-$m-3+s$ plane adjoints, after the conductor contribution is removed, cut $|K_C+sH|$. “Complete” concerns the resulting series on the normalization; it does not mean that arbitrary ambient forms have no kernel. For large $s$, curve Riemann–Roch and $H^1(K_C+sH)=0$ give

$$
 \deg(K_C+sH)=2g-2+sm,
 \qquad \dim|K_C+sH|=g-2+sm.
$$

The argument in the introductory paragraph then imposes independent points on a nonspecial complete series. Independence is essential: a special configuration can impose fewer conditions, and that is precisely what the later surface argument is designed to measure. At $s=0$, the complete series is canonical, of dimension $g-1$. The nodes impose independent conditions on forms of degree $m-3$. When $g=0$, this says the adjoint space is zero-dimensional as a vector space and the projective system is empty; it is not an exception to the formula.

For any divisor $D$ of degree $n$, the “index of speciality” is the **vector** dimension

$$
 i(D)=h^0(K_C-D)=h^1(D),
$$

and the precise theorem is

$$
 \dim|D|=n-g+i(D).
$$

This resolves the otherwise easy confusion between “number of independent canonical groups” and projective dimension. Vakil’s *Complex algebraic surfaces, Class 5* gives a concise modern statement of curve Riemann–Roch, Serre duality, and adjunction on its first page. No new mathematical gap appears in §1 once the cited curve theory and the ordinary-node model are acknowledged. The pronoun errors `contenerle` on pp. 101–102 are printed grammatical slips; the punctuation after the node formula is best read as a semicolon.

### §2. Spatial curve postulation, including reducible curves (pp. 102–106; A011–A029)

#### The invariant being counted

For $C\subset\mathbb P^3$, the number of independent conditions imposed by containing $C$ is

$$
 \operatorname{post}_C(N)
 =\operatorname{rank}\bigl[H^0(\mathbb P^3,\mathcal O(N))
 \longrightarrow H^0(C,\mathcal O_C(N))\bigr].
$$

For a smooth degree-$m$, genus-$g$ curve, let $e_N$ be the cokernel dimension of this restriction. Riemann–Roch gives the exact diagnostic identity

$$
 \operatorname{post}_C(N)=mN+1-g+h^1(C,\mathcal O_C(N))-e_N.
$$

Speciality and incompleteness have opposite signs. The excerpt correctly distinguishes them. Once $mN>2g-2$, speciality vanishes and the postulation is at most $mN+1-g$. Equivalently,

$$
 h^0(\mathcal I_C(N))\geq\binom{N+3}{3}-mN+g-1.
$$

The sentence on p. 103 calling $C$ a degree-$n$ curve is printed that way; the curve degree should be $m$, while $n$ there denotes the degree of the containing surfaces.

#### Why $N\geq m-2$ suffices

The argument is attributed to Castelnuovo’s 1893 paper *Sui multipli di una serie lineare di gruppi di punti appartenente ad una curva algebrica*, reprinted at the cited place in *Memorie scelte*. Its structure is a genuine proof, not merely an invocation of “general position.” Work over characteristic zero and take a generic projection of the smooth nondegenerate spatial curve to a plane. The projection has

$$
 d=\binom{m-1}{2}-g
$$

ordinary nodes, whose inverse images give a divisor $G$ of degree $2d$ on $C$. Cones over plane adjoints of degree $N\geq m-2$ give the complete residual series

$$
 |NH-G|=|K_C+(N-m+3)H|.
$$

This is nonspecial because $N-m+3\geq1$. It remains to show that the $2d$ points of $G$ impose independent conditions on spatial forms of degree $N$. For $N=m-2$, fix one selected branch point $P$. By the independence of the $d$ plane nodes for adjoints of degree $m-3$, choose a cone of degree $m-3$ containing the $d-1$ other secant lines but not the secant containing $P$. Multiply its equation by that of a plane passing through the other endpoint of this secant but avoiding $P$. The product vanishes at every point of $G$ except $P$. Repeating for each point gives a basis of separators. For larger $N$, multiply by a form avoiding all of $G$.

The restriction series therefore contains the complete residual series and acquires exactly $2d$ independent values along $G$. It is all of $H^0(C,NH)$. Consequently

$$
 \operatorname{post}_C(N)=mN-g+1\qquad(N\geq m-2).
$$

This proof assumes the generic nodal-projection theorem and plane-adjoint completeness, already part of the cited curve theory. Those are prerequisites, not newly discovered omissions. The doubtful subscript at TeX line 70 is actually $\Phi_n$ in the scan, correcting the transcription’s $\Phi_h$. Repeated equality signs across a printed line break on p. 104 are a typographic continuation convention, not an algebraic equation with an extra equality operator.

#### Nodes, noncoplanar triple points, and component genera

For singular curves the geometric genus of the normalization is insufficient by itself. Enriques’s coefficient $2t$ is correct because his triple points have three **noncoplanar** branches. Their completed local ring is modeled by

$$
 k[[x,y,z]]/(xy,xz,yz).
$$

Its normalization is the direct sum of three branch rings. The local functions are triples with one common constant, so the normalization quotient has length two. An ordinary plane triple point, by contrast, has delta-invariant three. Substituting the plane value here would falsely indict the printed formula.

A containing surface must vanish to order at least two at such a triple point: a nonzero linear term cannot vanish on three independent tangent directions. This entails four ambient jet conditions. On the three normalization branches, the forced double-point vanishing removes six intersection conditions. Hence one triple point changes the smooth residual count by $4-6=-2$. At an ordinary node, the corresponding change is $1-2=-1$. For an irreducible curve of degree $m$, normalization genus $g$, $t$ such triple points, and $\tau$ nodes, the eventual result is

$$
 \operatorname{post}_C(N)=mN-2t-\tau-g+1.
$$

Enriques first explains this through residual intersections, then treats several components. The clean modern proof packages all cases into

$$
 0\longrightarrow\mathcal O_C\longrightarrow
 \nu_*\mathcal O_{\widetilde C}\longrightarrow Q\longrightarrow0,
 \qquad\ell(Q)=2t+\tau.
$$

If $\widetilde C=\coprod_{i=1}^h C_i$, define

$$
 \rho=\sum_{i=1}^h g(C_i)-h+1.
$$

Then $\chi(\mathcal O_{\widetilde C}(N))=mN+1-\rho$, and

$$
 \chi(\mathcal O_C(N))=mN+1-\rho-2t-\tau.
$$

Serre vanishing makes this the actual restriction rank for $N\gg0$. Thus the final formula includes all configurations where the stated singularities are ordinary and no other singularities intervene:

$$
 p_a(C)=\rho+2t+\tau,
 \qquad\operatorname{post}_C(N)=mN-2t-\tau-\rho+1.
$$

The integer $\rho$ is the arithmetic genus of the **disjoint normalization**, not the sum of its component genera and not the arithmetic genus of the singular curve. It may be negative. This point is what makes the component calculation on pp. 105–106 coherent. The source’s repeated minus sign in the broken display $x=mn-6t-2\tau$ is again a continuation convention.

### §3. The virtual genus and its cohomological meaning (pp. 107–110; A030–A047)

Let $F\subset\mathbb P^3$ be a degree-$n$ projected surface with ordinary singularities, and let its double curve $\Gamma$ have degree $d$, normalization-disjoint genus $\rho$, $t$ noncoplanar triple points, and $\tau$ ordinary nodes. The eventual vector dimension of degree-$m$ adjoint forms is

$$
 N_m=\binom{m+3}{3}-dm+2t+\tau+\rho-1.
$$

Its finite difference is

$$
 N_m-N_{m-1}=\binom{m+2}{2}-d.
$$

Here “normal singularities” is the classical term for the prescribed ordinary projection singularities; it does not mean that $F$ is normal in the modern scheme-theoretic sense. A surface with a double curve is nonnormal.

The transcription’s $N_{w-1}$ at line 165 is a misread $N_{m-1}$. The right side is the vector dimension of the plane adjoints to a general plane section, whenever the $d$ nodes impose independent conditions. Their **projective** dimension is $m(m+3)/2-d$, one less. Enriques keeps those two counts consistent.

The argument descends from high degrees: the kernel of restriction to a plane consists of adjoints divisible by that plane’s equation. If the restriction image loses $\delta$ dimensions, the previous-degree adjoint space gains $\delta$ relative to the virtual polynomial. Independence of planar nodes in degree at least $n-3$ lets this continue down to ambient adjoint degree $n-4$. It gives actual count at least virtual count, and therefore $p_g\geq p_a$. Below that degree the planar independence guarantee ends. The sentence saying the degree-$n-4$ plane system *is* superabundant is too categorical; it may be superabundant, and that weaker statement is all the proof needs. A smooth plane curve has no node conditions at all, so cannot exhibit their superabundance.

#### Why the virtual value is $\chi(\mathcal O_X)-1$, not a convention without content

Let $\nu:X\to F$ be the smooth normalization of the ordinary projected model, and write $H=\nu^*\mathcal O_F(1)$. Finite duality identifies the conductor ideal on $F$ with

$$
 \mathcal Hom_F(\nu_*\mathcal O_X,\mathcal O_F)
 \simeq\nu_*\omega_X\otimes\omega_F^{-1}.
$$

Since $\omega_F\simeq\mathcal O_F(n-4)$, its preimage in $\mathcal O_{\mathbb P^3}$ gives the exact sequence

$$
 0\longrightarrow\mathcal O_{\mathbb P^3}(m-n)
 \longrightarrow\mathcal I_\Gamma(m)
 \longrightarrow\nu_*\omega_X(m-n+4)
 \longrightarrow0. \tag{3.1}
$$

For ordinary double curves, including the standard triple/pinch-point local models, this is the classical adjoint ideal. For an arbitrary singular model one must use the actual canonical/resolution adjoint ideal, not assume that vanishing on the reduced singular set alone suffices.

Taking Euler characteristics in (3.1) at $m=n-4$ gives

$$
 N_{n-4}=\chi(\omega_X)+\chi(\mathcal O_{\mathbb P^3}(-4))
 =\chi(\mathcal O_X)-1=p_a(X).
$$

The contribution $\chi(\mathcal O_{\mathbb P^3}(-4))=-1$ is essential. The actual canonical forms have dimension $p_g$, and their excess over $N_{n-4}$ is precisely $q$. This modern derivation verifies the intended invariant, while also explaining why the arithmetic genus of the singular hypersurface $F$, computed directly from its degree, is generally **not** Enriques’s birational numerical genus.

Substituting into the postulation polynomial gives the printed expression

$$
 p_a=\binom{n-1}{3}-(n-4)d+2t+\tau+\rho-1.
$$

For $m=n-4+s$, the adjoint divisor is $K_X+sH$. Let $\pi=p_a(H)$ and $\pi_s=p_a(sH)$. Adjunction gives

$$
 \pi_s=1+s(\pi-1)+\frac{s(s-1)}2n,
 \qquad\pi=\binom{n-1}{2}-d.
$$

The dimension of the induced system is obtained by subtracting the scalar dimension and the kernel of restriction to $F$: for $s\gg0$,

$$
 \dim|K_X+sH|=N_{n-4+s}-1-h^0(\mathbb P^3,\mathcal O(s-4))
 =p_a+\pi_s-1.
$$

For $s=1,2,3$, the kernel is zero. One must not extend the polynomial $\binom{s-1}{3}$ to $s=0$ and treat its value $-1$ as a vector-space dimension. At that endpoint, (3.1) and the actual canonical space must be used. On p. 109 the middle binomial identity has a printed minus in front of $s(s-1)n/2$; it must be plus. The preceding genus formula, the succeeding binomial expression, and direct expansion all agree on the correction.

### §4. Deficiency, comparison of adjoints, and numerical Riemann–Roch (pp. 110–114; A048–A074)

#### A single exact sequence organizes the whole section

For a smooth connected effective divisor $C\subset X$, adjunction gives

$$
 0\longrightarrow\omega_X\longrightarrow\omega_X(C)
 \longrightarrow\omega_C\longrightarrow0. \tag{4.1}
$$

Define $\delta(C)$ as the codimension of the image on global sections in $H^0(C,\omega_C)$. Then

$$
 \dim|K_X+C|=p_g+g(C)-1-\delta(C). \tag{4.2}
$$

This includes empty systems without changing conventions. Over a fixed nonzero projective canonical section, the adjoints restricting to it have an affine fibre of dimension $p_g$, whose projective closure has the same dimension; the kernel itself is $\mathbb P H^0(K_X)$, dimension $p_g-1$. This clarifies the source’s elementary counting language.

Because $C$ is connected, $H^1(K_C)\to H^2(K_X)$ is an isomorphism: its dual is $H^0(\mathcal O_X)\to H^0(\mathcal O_C)$, the isomorphism on constants. Also $H^2(K_X+C)=H^0(-C)^*=0$. Therefore the long exact sequence yields

$$
 \delta(C)=q-h^1(K_X+C),\qquad 0\leq\delta(C)\leq q, \tag{4.3}
$$

and hence

$$
 \dim|K_X+C|=p_a+g(C)-1+h^1(K_X+C). \tag{4.4}
$$

Equivalently, by dualizing the relevant restriction sequence,

$$
 \delta(C)=\operatorname{rank}\bigl[H^1(X,\mathcal O_X)
 \longrightarrow H^1(C,\mathcal O_C)\bigr].
$$

The deficiency is thus a rank, not an unexplained geometric defect. Completeness is exactly $\delta(C)=0$.

#### The comparison argument is valid under its stated hypotheses

Enriques compares $C$ with $C+L$. He assumes moving irreducible systems and an irreducible sum; two pencils must be distinct, so that the relevant intersection $i=C\cdot L$ is positive. For a smooth $L$, the restriction

$$
 (K_X+C+L)|_L=K_L+C|_L
$$

has degree $2g(L)-2+i$, hence is nonspecial and has projective dimension $g(L)+i-2$. The genus addition formula is

$$
 p_a(C+L)=p_a(C)+p_a(L)+C\cdot L-1.
$$

Subtracting the two instances of (4.2), or using the long exact sequence of restriction to $L$, gives

$$
 \delta(C)\leq\delta(C+L).
$$

In fact the codimension of the restriction of $|K_X+C+L|$ inside the complete series on $L$ is $\delta(C+L)-\delta(C)$. Thus equality of the deficiencies is equivalent to completeness of this restriction. These are proved claims, not unjustified monotonicity assumptions. For a reducible added divisor, the source carefully asks that its components not be fundamental for the original system and that successive additions retain irreducibility; that positivity is needed for the nonspeciality used in the calculation.

The discussion of base points is most cleanly expressed on a common blowup. If $\sigma:\widetilde X\to X$ blows up one point of multiplicity $i$ on $C$, then

$$
 K_{\widetilde X}=\sigma^*K_X+E,
 \qquad\widetilde C=\sigma^*C-iE,
 \qquad K_{\widetilde X}+\widetilde C
 =\sigma^*(K_X+C)-(i-1)E.
$$

The corresponding adjoint condition has length $i(i-1)/2$, the number of monomials in two variables of total degree below $i-1$. For a sufficiently positive system the jets are independent. The source’s infinitesimal exceptional curve is the geometric form of this calculation.

For $L_s=sH$, the large-degree formula of §3 and (4.2) imply $\delta(L_s)=p_g-p_a=q$. Given a fixed moving $C$, the difference $sH-C$ is very ample for $s\gg0$; comparison then yields $\delta(C)\leq q$. The p. 112 opening sentence inadvertently calls the adjoint system itself $|L_s|$, whereas the following formulas require $L_s=sH$ and $L'_s=K_X+sH$. This is an antecedent/notation slip, not a change of genus convention.

The maximum-deficiency characterization implies birational invariance of $p_a$, once canonical forms and moving systems are transferred to smooth models. Modernly, blowing up a smooth point preserves $H^i(\mathcal O_X)$; birational maps of smooth surfaces factor into such modifications. Thus $p_g,q,p_a$ are birational invariants. The source defines regularity as $p_a=p_g$, i.e. $q=0$.

There is no contradiction between these preliminary inequalities and the later stronger regularity criterion. In characteristic zero, if $|C|$ is a moving irreducible system of dimension at least two, resolve its base points. The resulting free class is nef and big: its morphism has two-dimensional image, since a free system composed with a curve would have a general member that is a sum of fibres unless it were a pencil. Ramanujam’s vanishing theorem then gives $H^1(K_X+C)=0$, hence $\delta(C)=q$. The nef-and-big proof does not address square-zero pencils; moving linear pencils require a separate fibration argument. Isolated or nonmoving divisors can have $\delta(C)<q$. No strict-deficiency example among complete moving irreducible linear pencils is being claimed. Enriques’s earlier estimate is weaker; it is not false merely because later machinery gives equality under stronger hypotheses.

#### The numerical formulas at the end of §4

Let $n=C^2$, $\pi=p_a(C)$, $C'=K_X+C$, and $p^{(1)}=K_X^2+1$ on the chosen smooth model. Then $K_XC=2\pi-2-n$, so

$$
 \begin{aligned}
 \pi'&=p_a(C')=3\pi-3-n+p^{(1)},\\
 n'&=(C')^2=4\pi-5-n+p^{(1)},\\
 \pi-1&=n'-\pi'+1.
 \end{aligned}
$$

The apparent prime after the **last** $n$ in the second formula on p. 113 cannot be retained mathematically. The scan has a small high stroke; it is best treated as a printed misprint with moderate visual confidence. The required $n$, without prime, follows unambiguously from the intersection calculation. The parameter $p^{(1)}$ is called “relative” for good reason: $K^2$ decreases by one under blowup. It is not a birational invariant unless an appropriate minimal-model convention is introduced.

Equation (4.4) gives

$$
 \dim|C'|\geq p_a+\pi-1=p_a+n'-\pi'+1.
$$

Relabelling an adjoint divisor yields the numerical Riemann–Roch inequality printed on p. 114. In full modern form,

$$
 h^0(D)-1=p_a+\frac{D(D-K_X)}2+h^1(D)-h^2(D).
$$

For an adjoint to a nonzero effective divisor, $h^2(D)=0$; its excess over the numerical value is $h^1(D)\geq0$. This is the modern content of the regular/superabundant distinction made here. The excerpt does not yet state the full theorem for all divisors; that is developed later in the chapter.

### §5. Multiple curves, Hilbert polynomials, and propagation (pp. 114–117; A075–A096)

#### A direct proof of the multiple-curve formula

Let $C\subset\mathbb P^3$ be smooth of degree $m$ and genus $g$, with ideal $\mathcal I$. The $s$-fold thickening used here is defined by $\mathcal I^s$. Since $C$ is a regular embedding of codimension two,
$$
 \mathcal I^j/\mathcal I^{j+1}\simeq\operatorname{Sym}^j N_{C/\mathbb P^3}^{\vee}.
$$
The normal bundle has rank two and degree $4m+2g-2$, by adjunction. Its $j$th symmetric conormal power has rank $j+1$ and degree
$$
 -\frac{j(j+1)}2(4m+2g-2).
$$
Riemann–Roch for vector bundles on a curve therefore gives
$$
 \chi\!\left(\operatorname{Sym}^jN^\vee\otimes\mathcal O_C(N)\right)
 =(j+1)(Nm+1-g)-\frac{j(j+1)}2(4m+2g-2).
$$
Summing from $j=0$ to $s-1$, using
$$
 \sum(j+1)=\frac{s(s+1)}2,\qquad
 \sum j(j+1)=\frac{s(s-1)(s+1)}3,
$$
produces exactly
$$
 \operatorname{post}_{sC}(N)
 =\frac{s(s+1)}6
 \left[(3N-4s+4)m-(2s+1)(g-1)\right]
 \qquad(N\gg0).
$$
Thus the displayed Noether–Campedelli formula is correct. The source credits Noether and cites Campedelli’s 1931 article; it does not provide this derivation. The footnote saying that singular points of $C$ require modification is substantive: the conormal filtration need not remain a rank-two vector-bundle calculation, and no correction depending only on degree and normalization genus is supplied. For an isolated assigned $s$-fold point in $\mathbb P^3$, the independent conditions number
$$
 \ell\bigl(k[x,y,z]/(x,y,z)^s\bigr)=\binom{s+2}{3}.
$$

#### The indexing errors and the correct telescoping invariant

Set $H$ equal to a plane section. On p. 115, degree-$n-3+s$ adjoints correspond to
$$
 K_X+(s+1)H,
$$
not to $K_X+sH$. Since the same paragraph defines $\pi_s=p_a(sH)$, its printed dimension $p_a+\pi_s-1$ is an off-by-one error; it must be $p_a+\pi_{s+1}-1$. The restriction degree $2\pi-2+sn$ printed immediately afterward is correct, because the restriction to $H$ is $K_H+sH_H$.

The eventual finite difference in the number of adjoint forms is
$$
 \binom{n+s-1}{2}-d
 =\pi+sn+\frac{s(s-3)}2.
$$
This validates the “arithmetic progression of third order”: it is an eventual cubic Hilbert polynomial whose first difference is this quadratic. Its extrapolated values are virtual counts. The footnote’s extension to arbitrary fixed schemes of points and curves is the Hilbert-polynomial theorem; it does not require those base schemes to arise as the singularities of a surface.

Let $\delta_s$ denote the failure of restriction
$$
 H^0(K_X+(s+1)H)\longrightarrow H^0(K_H+sH_H)
$$
to be surjective, for $s\geq0$. The source fixes a threshold $h$ beyond which all deficiencies vanish. The descent gives
$$
 q=\delta_0+\delta_1+\cdots+\delta_{h-1}.
 \tag{5.1}
$$
For $s\geq1$, the curve bundle $K_H+sH_H$ is nonspecial. The long exact sequence gives
$$
 \delta_s=h^1(K_X+sH)-h^1(K_X+(s+1)H).
$$
At $s=0$, the trace isomorphism used in §4 gives
$$
 \delta_0=q-h^1(K_X+H).
$$
These formulas telescope to (5.1). They explain exactly why the canonical endpoint differs from an ordinary positive-twist step.

The first displayed descending dimension on p. 116 must use $\pi_{h-1}$, not $\pi_{h-2}$. The next must use $\pi_{h-2}$, not $\pi_{h-3}$, and must include the missing constant $-1$. When a descent reaches $K_X$ itself, one uses the separately printed formula $p_g-1$, rather than forcing the positive-twist notation beyond its range. The final prose formula erroneously begins its sum at $s=1$; the correct lower bound is $s=0$. These are errors in the scan, not OCR.

Under the smooth finite-normalization hypothesis and in characteristic zero, $H$ is ample. Kodaira vanishing gives $H^1(K_X+sH)=0$ for every $s\geq1$. Consequently all $\delta_s$ with $s\geq1$ vanish and $\delta_0=q$. Enriques is working toward that stronger picture through classical geometric arguments. His provisional sequence of possible defects is a valid formal estimate, not evidence of actually existing higher defects under these positivity assumptions. If one changes to an arbitrary resolution with exceptional curves, positivity must be checked anew.

#### The multiplication lemma and its special boundary case

Write $M,L$ for line bundles on a smooth curve, and assume $L$ has a basepoint-free pencil $V\subset H^0(L)$. The exact sequence
$$
 0\longrightarrow L^{-1}\longrightarrow V\otimes\mathcal O_C
 \longrightarrow L\longrightarrow0
$$
tensored with $M$ shows that
$$
 H^1(M-L)=0
 \quad\Longrightarrow\quad
 V\otimes H^0(M)\twoheadrightarrow H^0(M+L).
 \tag{5.2}
$$
This is the modern basepoint-free pencil trick. Enriques’s argument with two disjoint divisors is the same proof in projective dimensions. If $\deg M=m$, $\deg L=n$, and $M,M-L$ are nonspecial, the two copies of $H^0(M)$ meet in $H^0(M-L)$; their vector-space span has dimension $m+n-g+1$. The source’s “minimum sum” means this linear span of products, not the set of pairwise sums of divisors alone. A modern explicit reference is Voight and Zureick-Brown, *The canonical ring of a stacky curve*, §2.4, Lemma 2.4.1.

For $M=K_C+sL$ with $s>1$, the residual $M-L$ has positive twist and (5.2) applies. At $s=1$, $M-L=K_C$ has $h^1=1$. The two-pencil-section image is therefore one dimension short. Its projective dimension is
$$
 2(g+n-1)-g-1=g+2n-3,
$$
while the complete target $|K_C+2L|$ has dimension $g+2n-2$. The scan on p. 117 prints $g+n-3$ and $g+n-2$: each occurrence is missing a second $n$ contribution.

For the plane-line series, a pencil corresponds to lines through a point $P$ off the curve. The deficient plane adjoints are precisely those through $P$. Two generic distinct centres give distinct evaluation hyperplanes, whose span is the entire adjoint space. This repairs the boundary case without pretending that $H^1(K_C)$ vanishes. The argument does not yet prove the $s=0$ assertion; §6 deals with that case.

### §6. Castelnuovo’s regularity criterion (pp. 117–120; A097–A113)

For a smooth surface and a smooth ample hyperplane section $C$, the decisive exact sequence is (4.1). Kodaira vanishing gives $H^1(K_X+C)=0$, and hence
$$
 \operatorname{coker}\!\left[H^0(K_X+C)\to H^0(K_C)\right]
 \simeq H^1(K_X),\qquad
 \dim\operatorname{coker}=q.
 \tag{6.1}
$$
Therefore the adjoints restrict to the **complete canonical series if and only if $q=0$**. In that case
$$
 \dim|K_X+C|=p_g+g(C)-1.
$$
Kodaira’s 1952 paper supplies the later vanishing machinery; this is a modern proof, not a claim that he was the first person to repair the precise 1897 argument reproduced here.

Enriques explicitly calls the ensuing classical demonstration a “rapid sketch,” and cites Castelnuovo’s *Alcune proprietà fondamentali dei sistemi lineari di curve tracciati sopra una superficie algebrica* (1897). Its first lemma is sound. A divisor $G$ of degree $m$ moving in a $g_m^h$ imposes $m-h$ canonical conditions, by Riemann–Roch. Under canonical completeness those are the same fixed linear conditions on the global adjoints. Therefore their rank is independent of the smooth plane section through the fixed axis. “Every plane” must be read within the smooth/generic-section framework or reformulated using dualizing sheaves at singular members.

The longer construction on pp. 118–119 seeks an adjoint of degree $n-2$ by sweeping plane adjoints through a pencil of planes. In each plane it imposes: the canonical group cut by $C'$, $s-1$ selected axis intersections, and a tangent-plane condition at one selected point. The text asserts a unique curve after these conditions; the swept surface initially has degree $n-2+h$ and contains the axis with multiplicity $h$. A tangent-plane argument at one further intersection point is used to force $h=0$ via the preceding special-series lemma. Varying the data is then said to produce $s+1$ dimensions of adjoints and $s$ dimensions of characteristic series.

This is an authentic outline of a geometric proof, but it does not supply the full incidence calculation: independence of the chosen point and tangency conditions, algebraicity of the swept family, control of its degree and fixed components, the limiting tangent-plane argument, and the final dimension variation are compressed. The correct diagnosis is **sketched, with these details omitted**, rather than “false.” Formula (6.1) proves the desired criterion without those auxiliary choices.

Once $q=0$, characteristic completeness follows directly from
$$
 0\longrightarrow\mathcal O_X\longrightarrow\mathcal O_X(C)
 \longrightarrow\mathcal O_C(C)\longrightarrow0.
$$
The cokernel of restriction injects into $H^1(\mathcal O_X)=0$. This proof works for every effective Cartier divisor for which the characteristic-series interpretation is appropriate, and does not need Kodaira vanishing in this direction.

#### The curve multiplication result used at the end

The additional curve theorem on p. 120 says: if $L$ is a complete basepoint-free linear series on a positive-genus smooth curve and its map is birational onto its image, then
$$
 H^0(K_C)\otimes H^0(L)\twoheadrightarrow H^0(K_C+L).
 \tag{6.2}
$$
The phrase “not composed with an involution” is the birationality hypothesis. It must not be discarded. For a concrete failure, let $A$ be the hyperelliptic pencil on a curve of genus $g\geq2$ and put $L=2A$. Then $h^0(L)=3$, while the canonical products have dimension $g+2$ and $h^0(K_C+2A)=g+3$. The deficiency is one. This does not describe arbitrarily high multiples, which eventually become very ample.

The source gives a dimension argument using a product-series lemma from Castelnuovo (1893). If $G\in|L|$ is general, of degree $n$, and $h^0(L)=s+1$, the two evaluated spaces have dimensions $s$ and $n-s$. The cited lemma gives at least $n-1$ conditions on their product. Adding the canonical subspace gives $n+g-2$, exactly the Riemann–Roch dimension of the target. The $n-1$ lower bound is a substantive lemma about these series; it is not a valid dimension inequality for arbitrary coordinate subspaces.

A modern version of the same proof can use the usual secant lemma for a birational curve series: choose $s-1$ general points $D$ so that $L(-D)$ is a complete basepoint-free pencil. This is the geometric ingredient in the classical multiplication theorem. For $M=L(-D)$, the pencil trick tensored with $K_C$ gives a surjective product map, because the dual of
$$
 H^1(K_C-M)\longrightarrow H^0(M)\otimes H^1(K_C)
$$
is the isomorphism from the dual pencil to $H^0(M)$. Thus the products already contain $H^0(K_C+L-D)$. Evaluation of $H^0(L)$ at $D$ is surjective. For each point of $D$, choose a section of $L$ vanishing at the other points but not there, and a canonical section nonzero there; the products fill every missing coordinate at $D$. Since $H^1(K_C+L-D)=H^0(D-L)^*=0$, this fills the entire target. This isolates precisely the secant/general-position input rather than hiding it in a dimension count.

Finally, the note extends the surface criterion to irreducible systems of dimension at least two that need not define birational maps. After resolving base points the moving class is free, nef, and big. Ramanujam’s characteristic-zero vanishing gives $H^1(K_X+C)=0$, so (6.1) remains valid. This proves the extension in the stated dimension range. The source excludes pencils from this formulation, and the nef-and-big proof does not cover square-zero classes. Complete moving irreducible linear pencils can be treated separately by fibration methods in characteristic zero; they are not being offered as counterexamples. Arbitrary isolated effective divisors cannot replace the moving-system hypothesis.

### §7. Examples and a reconstruction of the Campedelli paragraph (pp. 120–123; A114–A144)

#### Smooth hypersurfaces, rational surfaces, and ruled surfaces

For a smooth degree-$n$ hypersurface in $\mathbb P^3$,
$$
 K_X=\mathcal O_X(n-4),\qquad
 p_g=p_a=\binom{n-1}{3},\qquad q=0.
$$
The canonical form count follows from the hypersurface sequence and the cohomology of projective space. Smoothness suffices; the surface need not be general in its degree. Planes, smooth quadrics, and smooth cubics give zero. Birational invariance then yields $p_g=p_a=0$ for every smooth rational surface. The p. 120 footnote formally assigns the empty double curve genus $\rho=1$, so that its Euler characteristic is zero. That is a useful convention, not the genus of a connected empty curve. Its degree should be denoted $d=0$, not the printed $n=0$.

For a ruled surface with base $B$ of genus $g$, pass to a smooth $\mathbb P^1$-bundle $f:X\to B$. Then
$$
 f_*\mathcal O_X=\mathcal O_B,\qquad R^1f_*\mathcal O_X=0,
$$
and Leray gives $q=g$ and $p_g=0$, hence $p_a=-g$. The cone proof in the source is a geometrical counterpart. The first adjoint is empty, yielding a deficiency equal to the plane-section genus; the next adjoint restricts completely, eliminating further deficiencies. Its conclusion is correct. The alternative direct statement about ruled surfaces is only sketched, but the bundle calculation supplies a full proof.

The sentence saying that surfaces with simple double curves are “usually” regular is a qualitative observation, not a theorem with specified numerical hypotheses. The historical credits to Cayley, Noether, and Castelnuovo are reported as Enriques’s credits. In particular, “first example” is not independently certified by this audit.

#### Why the elementary sextic dimension count needs a generality argument

A sextic surface has 84 coefficients, hence projective dimension83. An assigned triple point imposes ten jet conditions. The subtraction $83-8\cdot10=3$ is only an expected dimension: independence at eight points needs proof. Moreover “arbitrarily assigned” cannot mean every configuration, since the next paragraph deliberately supplies a special configuration where independence fails.

Here is an explicit modern repair for eight sufficiently general points. Let $Y=\operatorname{Bl}_{P_1,\ldots,P_8}\mathbb P^3$, let $H$ be the pullback of a plane, and put
$$
 L=2H-\sum E_i.
$$
The quadrics through the points form a pencil. On a smooth member $Q$, blow up the eight points to obtain $S$ and let $D=L|_S=-K_S$. The pencil base curve is a smooth elliptic quartic $E$. The degree-zero bundle $N=\mathcal O_E(D)$ is not torsion of order1,2, or3 for a sufficiently general configuration. From
$$
 0\longrightarrow\mathcal O_S((k-1)D)
 \longrightarrow\mathcal O_S(kD)\longrightarrow N^k\longrightarrow0
$$
one obtains $h^0(S,kD)=1$ for $k=1,2,3$. Restriction to $S\in|L|$ on $Y$ then gives $h^0(Y,kL)\leq h^0(Y,(k-1)L)+1$. Binary degree-$k$ polynomials in the two pencil quadrics already give $k+1$ independent sections. Hence equality holds and $h^0(Y,3L)=4$. Every binary cubic factors over $\mathbb C$, so every such sextic is a union of three quadrics from the pencil. This is the missing independence argument, with its generality hypothesis explicit.

#### The Cayley-octad net: a complete calculation

Now let the eight points be the reduced transverse base scheme of a general net of quadrics. On the same blowup $Y$, $L$ is generated by three sections and defines
$$
 f:Y\longrightarrow\mathbb P^2.
$$
The general fibre is the strict transform of a complete intersection of two quadrics, hence an elliptic quartic. For a general net the morphism is equidimensional with connected fibres; the smooth target and Stein factorization give $f_*\mathcal O_Y=\mathcal O_{\mathbb P^2}$. Consequently
$$
 h^0(Y,kL)=\binom{k+2}{2}.
$$
In particular the sextics triple at the octad form projective dimension9. This supplies both the lower bound by cubic expressions in the net and the upper bound relegated to the source’s footnote.

Let $B\subset\mathbb P^2$ be a general smooth plane curve of degree $n\geq3$ and let $X=f^{-1}(B)\in|nL|$. Generality ensures $X$ is smooth on the blowup; its image in $\mathbb P^3$ is a degree-$2n$ surface with eight ordinary $n$-fold points. Since
$$
 K_Y=-4H+2\sum E_i=-2L,
$$
adjunction gives $K_X=(n-2)L|_X$. With $f_X:X\to B$ and connected fibres,
$$
 p_g(X)=h^0(B,\mathcal O_B(n-2))=\frac{n(n-1)}2.
$$
The relative dualizing bundle is
$$
 \omega_{X/B}=f_X^*\mathcal O_B(1),
$$
because $\omega_B=\mathcal O_B(n-3)$. Relative duality for this flat genus-one fibration gives
$$
 R^1(f_X)_*\mathcal O_X=\mathcal O_B(-1).
$$
Leray and $H^0(B,\mathcal O_B(-1))=0$ now show
$$
 q(X)=g(B)=\frac{(n-1)(n-2)}2,\qquad
 \chi(\mathcal O_X)=n,\qquad p_a=n-1.
$$
For $n=3$ these are $p_g=3,p_a=2,q=1$, exactly as printed. This is a full proof of the general family formulas stated without calculation on p. 122.

Each exceptional $E_i\simeq\mathbb P^2$ maps isomorphically to the parameter plane of the net, because the three local linear parts of the quadrics are independent at a transverse base point. Therefore $E_i\cap X\simeq B$. This verifies the source’s statement that the tangent-cone section at an ordinary $n$-fold point has the same genus as the irrational pencil’s base. The exceptional curve also supplies a section of the resolved elliptic fibration. The equality $q=g(B)$ is a computed fact of this family, not a consequence of having an arbitrary irrational pencil.

#### Campedelli’s degree notation: what is printed and what follows mathematically

The p. 123 paragraph cites Campedelli (1936), without title or pages, and says that the construction depends on a genus-one pencil on a quadric “of degree $m$,” with $m\mid n$, $n=ms$, and eight “$s$-fold” base points. It then says that projection gives a Halphen pencil of plane curves of degree $3m$ with nine $m$-fold base points. These data cannot all be correct. They are present in the scan; they are not a transcription error.

The following is an **independent mathematical reconstruction by this audit**, not a claim to have recovered the exact wording or complete proof of Campedelli’s original article. It has high confidence as geometry, but lower confidence as an identification of which of Enriques’s letters the author intended to change.

On $Q\simeq\mathbb P^1\times\mathbb P^1$, let $E\in|\mathcal O_Q(2,2)|$ be a smooth elliptic quartic through the eight points, and let $Z=P_1+\cdots+P_8$. Set
$$
 N=\mathcal O_E(2,2)(-Z).
$$
Its degree is zero. If $N$ has exact finite order $m$, then on $S=\operatorname{Bl}_8Q$ the anticanonical class $D=-K_S$ has $D^2=0$ and normal bundle $N$ along its unique member for $m>1$. The exact sequences above show $h^0(kD)=1$ for $1\leq k<m$ and $h^1(kD)=0$ in that range, since $\chi(kD)=1$ and $h^2(kD)=0$. At $k=m$, the restriction to $N^m\simeq\mathcal O_E$ lifts and gives $h^0(mD)=2$. A new member is disjoint from $E$, so this pencil is basepoint-free. Its fibres are connected: writing $S\to B\to\mathbb P^1$ for the Stein factorization, $H^1(B,\mathcal O_B)$ injects into $H^1(S,\mathcal O_S)=0$ because $S$ is rational, so $B\simeq\mathbb P^1$. If its finite map to the pencil parameter line had degree $d$, connected-fibre pushforward would give $h^0(S,mD)=h^0(\mathbb P^1,\mathcal O(d))=d+1$. Thus $d=1$. Bertini and adjunction then make a general member a smooth connected genus-one curve. This is the quadric form of a Halphen pencil of index $m$.

Its image on $Q$ has **bidegree $(2m,2m)$, spatial degree $4m$, and eight base points of multiplicity $m$**. Projection from one of the base points has plane degree $4m-m=3m$. The two ruling lines through the projection point contract to two plane base points of multiplicity $m$; the other seven points give the remaining seven. Thus there are nine $m$-fold plane base points, exactly as the final clause says. Neither spatial degree $m$ nor spatial degree $2m$ can give that clause.

The other printed condition, that the eight-point group comes by “division by $n$” from the series cut on $E$ by degree-$2n$ surfaces, is coherent:
$$
 nZ\sim\mathcal O_E(2n)
 \quad\Longleftrightarrow\quad N^n\simeq\mathcal O_E.
$$
It means that the minimal index $m$ divides $n$. The degrees are $8n$ on both sides. Thus the torsion condition itself should be retained while the degree/base-multiplicity wording is corrected or explicitly flagged.

#### Further reconstruction: parameter range and irregularity

One can push this reconstruction far enough to explain the irregularity and expose a boundary qualification omitted from the short paragraph. This derivation is supplied here, not attributed to an unread historical proof.

On $Y=\operatorname{Bl}_8\mathbb P^3$, again put $L=2H-\sum E_i$. Suppose the quadric pencil is general subject to the torsion condition of exact index $m$. For $k<m$, restriction to $S$ gives $h^0(Y,kL)=k+1$. The fat-point ideal description gives
$$
 \chi(Y,kL)=\binom{2k+3}{3}-8\binom{k+2}{3}=k+1,\qquad
 H^2(Y,kL)=H^3(Y,kL)=0 \quad(k\geq0).
$$
Hence $H^1(Y,(m-1)L)=0$, and the new section of $mD$ lifts to a section $\theta\in H^0(Y,mL)$. If $u,v$ are the pencil quadrics, their common zero scheme on $Y$ is the strict transform of $E$. The restriction $\theta|_E$ is a nonzero constant in $N^m\simeq\mathcal O_E$. Consequently $u^m,v^m,\theta$ have no common zero, and $|mL|$ is generated. This supplies the morphism used below and makes Bertini applicable to $|nL|$ when $m\mid n$. Moreover, $u,v,\theta$ are algebraically independent in the graded section ring: $\theta$ varies along a general quadric, where its restriction supplies the nonconstant Halphen-pencil parameter.

The complete section ring is consequently
$$
 \bigoplus_{k\geq0}H^0(Y,kL)\simeq\mathbb C[u,v,\theta],
 \qquad\deg u=\deg v=1,\quad\deg\theta=m.
 \tag{7.1}
$$
For completeness, the dimension check is not assumed: $h^0(S,kD)=\lfloor k/m\rfloor+1$ follows from the genus-one pencil, and restriction gives an upper bound whose successive increments are these numbers. The weighted monomials in $u,v,\theta$ attain precisely that upper bound. They therefore span each graded piece, proving (7.1).

For $n=ms$, a general $X\in|nL|$ is the inverse image of a weighted-plane curve $B$ of degree $n$ in $\mathbb P(1,1,m)$. The coefficient of $\theta^s$ can be chosen nonzero, so $B$ avoids the weighted-plane singular vertex. The ratio $[u:v]$ gives a degree-$s$ map $B\to\mathbb P^1$; the discriminant has degree $ms(s-1)$ and is simply branched for a general equation. Riemann–Hurwitz yields
$$
 g(B)=\frac{(s-1)(ms-2)}2=\frac{(s-1)(n-2)}2.
 \tag{7.2}
$$
Adjunction still gives $K_X=(n-2)L|_X$. Since $Y$ is rational and $K_Y=-2L$, the restriction sequence gives
$$
 p_g(X)=h^0(Y,(n-2)L),\qquad
 \chi(\mathcal O_X)=n,\qquad p_a(X)=n-1.
$$
Using the monomial count in (7.1),
$$
 p_g(X)-(n-1)
 =\sum_{j=1}^{\lfloor(n-2)/m\rfloor}(n-jm-1)
 =\frac{(s-1)(n-2)}2.
$$
Thus $q(X)=g(B)$, agreeing with the type of equality asserted by Enriques. The generic fibres of $X\to B$ are the genus-one members of the quadric Halphen pencil. This supplies a coherent modern explanation for the generalized family under explicit ordinary/genericity hypotheses.

It also makes the parameter qualification visible: with $n\geq3$, these surfaces are irregular precisely when $s>1$. The boundary $s=1$, namely $n=m\geq3$, has $q=0$. The source’s phrase “one obtains irregular surfaces” is safe as an existence assertion after choosing the parameters to make (7.2) positive. Read as an assertion about every divisor $m\mid n$, it requires this omitted restriction. Because the printed symbols are already inconsistent and the original Campedelli article was not inspected, this audit does not insist that Campedelli himself made this error; it localizes the issue to the compressed account on p. 123.

#### The general irrational-pencil inequality

Finally, if $f:X\to B$ is a proper morphism with connected fibres and $B$ smooth, so $f_*\mathcal O_X=\mathcal O_B$, the low-degree Leray sequence begins
$$
 0\longrightarrow H^1(B,\mathcal O_B)
 \longrightarrow H^1(X,\mathcal O_X)
 \longrightarrow H^0(B,R^1f_*\mathcal O_X)\longrightarrow0.
$$
Therefore $q(X)\geq g(B)$, and a positive-genus base forces irregularity. The source states the inequality and postpones its proof. This proof only needs the connected-fibre direct-image hypothesis; no assertion about injectivity of differentials under an arbitrary inseparable map is being substituted for it.

#### Additional observations for §§1–7 and confidence

The following are deductions of this audit rather than historical claims.

1. **A practical consistency test for adjoint notation — high confidence.** For a degree-$n$ projected model, an adjoint form of degree $n-4+t$ must represent $K_X+tH$. Checking this one relation detects all three subscript shifts on pp. 115–116 without guessing from the desired final formula.
2. **A single cohomological meaning for two kinds of “defect” — high confidence.** The §4 defect is the rank of restriction on $H^1(\mathcal O)$; the §5 defects telescope differences of $h^1(K_X+sH)$. They are not the same symbols with interchangeable meanings. Their relation explains why the canonical endpoint contributes all irregularity for ample hyperplanes in characteristic zero.
3. **A test family for degree conventions — high confidence in the reconstruction.** The Halphen index-$m$ quadric pencil has degree $4m$, not $2m$. Projection subtracts the multiplicity at the projection centre, leaving $3m$. This provides an independent diagnostic even before computing cohomology.
4. **A weighted-parameter description of the generalized examples — high confidence under the stated generality and ordinary-singularity hypotheses.** Equations (7.1)–(7.2) give an explicit section-ring model and exhibit the regular boundary $s=1$. This is not asserted to be novel research; it is an independently supplied reconstruction. Identifying the exact correspondence with every case in Campedelli’s 1936 article remains a historical/source-verification question.
5. **Positive-characteristic extension — limited claim, not a blanket generalization.** The Hilbert-polynomial identities, normalization delta calculations, blowup formulas, and Leray inequality remain meaningful over much wider fields. The uses of generic nodal projection, the birational curve-series secant lemma, and Kodaira/Ramanujam vanishing have been stated in characteristic zero. No positive-characteristic version of the regularity equivalences is asserted without additional hypotheses.

### §8. Systems larger than the canonical system (pp. 123–127)

#### Formula organizing §§8–14

The underlying object in the modern statements below is a smooth projective connected surface $X$ over $\mathbf C$. Singular projective models in the source are replaced by a smooth model with the actual canonical divisor $K_X$. Write

$$
p_a(X)=\chi(\mathcal O_X)-1,\qquad
p_g=h^0(K_X),\qquad q=h^1(\mathcal O_X)=p_g-p_a(X).
$$

For a divisor $C$, including an ineffective divisor class, put

$$
n=C^2,\quad \pi=p_a(C)=1+\frac{C^2+K_XC}{2},\quad
r=h^0(C)-1,\quad i(C)=h^0(K_X-C),\quad \omega(C)=h^1(C).
$$

The convention $r=-1$ for an empty system is indispensable. The modern identity organizing these pages is

$$
\boxed{r=p_a(X)+n-\pi+1-i(C)+\omega(C).}
\tag{8.1}
$$

It follows from surface Riemann–Roch and Serre duality (Beauville, 1996, Theorems I.11–I.12 and Remarks I.13). The calculations below are applications and derivations, not assertions that Enriques used sheaf cohomology. A *regular system* means $\omega(C)=0$; a *regular surface* means $q=0$. They are different conditions. The dimension estimates concern **complete** systems, including complete systems with assigned base conditions after passing to a blowup. An arbitrary smaller vector subspace need not satisfy them.

The genus in the numerical identities is arithmetic genus, including for reducible divisors. The earlier notation $p^{(1)}$, when applied to the full canonical divisor on the chosen smooth model, means $1+K_X^2$. It must not be indiscriminately identified with an invariant defined using only a moving or “pure” canonical part. The notation $p^{(2)}$ on p. 144 denotes canonical degree, not the plurigenus $P_2$.


#### The main proof and the distinction between containment and positivity

Enriques recalls the inequality for adjoints $C=K+L$ with $L$ irreducible. He defines a system “more ample than the canonical system” by effective nonzero containment $C-K>0$. This is an order relation among divisor classes, not the modern definition of an ample line bundle. He correctly observes that the residual can have fixed components and need not be irreducible. The subtraction argument removes that restriction.

The proof on pp. 124–125 becomes precise as follows. Fix an ample $H$, take $s$ sufficiently large, and set $A=K+sH$, $D=A-C$. The complete systems can be chosen with the regularity, global generation, and irreducibility required in the argument. These facts follow from Serre vanishing and eventual very ampleness for a fixed line bundle twisted by $sH$ (Stacks Project, Lemma 30.17.1, Tag 01XO). Choose $D$ smooth. Since $C-K$ is effective and nonzero, $(K-C)D<0$, so adjunction and curve duality give

$$
h^1(D,\mathcal O_D(A))=h^0(D,\mathcal O_D(K-C))=0.
$$

Write $D^2=\nu$, $p_a(D)=\rho$, and $CD=t$. The complete restricted line bundle has $h^0=\nu+t-\rho+1$, and the image of surface sections has no larger dimension. Consequently

$$
r(C)\ge r(A)-(\nu+t-\rho+1).
$$

Together with

$$
A^2=n+\nu+2t,\qquad p_a(A)=\pi+\rho+t-1,
$$

this gives $r(C)\ge p_a+n-\pi+1$, including reducible $C$. In (8.1), the reason is $i(C)=0$ and $\omega(C)\ge0$. The source supplies the subtraction calculation; the high-degree existence assertions are sketches dependent on earlier postulation results.

#### The singular-point illustration on p. 124

Two displayed errors are in the print. If $\bar C=C-\theta$, $C\theta=0$, and $\theta^2=-\nu$, then

$$
\bar n=n-\nu,\qquad \pi=\bar\pi+\rho+\nu-1.
$$

The source instead prints $n=\bar n-\nu$ and $\bar\pi=\bar\pi+\rho+\nu-1$. The scan confirms both the minus sign and the extraneous left overbar. The missing left system bars in $\bar C=|C-\theta|$ are also printed.

There is a further hypothesis issue. The formulas $\theta^2=-\nu$ and $g(\theta)=(\nu-1)(\nu-2)/2$ describe an **ordinary** isolated hypersurface point with smooth plane tangent cone, not an arbitrary isolated point of multiplicity $\nu$. Moreover, subtracting one $\theta$ from $L=C-K$ need not leave an irreducible residual. On the resolution of an ordinary $\nu$-fold point of a degree-$d$ surface,

$$
K=(d-4)H-(\nu-2)\theta.
$$

For large $C=sH$, $L$ contains fixed contribution $(\nu-2)\theta$, and $L-\theta$ retains $(\nu-3)\theta$ when $\nu>3$. The assertion needs a restriction or a different subtraction. This affects an illustration, not the subsequent general proof.

Under the illustration's intended extra assumptions, the corrected calculation does give strict superabundance. Basepoint freedom gives $h^0(C)-h^0(C-\theta)=1$, while $\bar n-\bar\pi=n-\pi+\rho-1$. The adjoint lower bound therefore gives $r(C)\ge p_a+n-\pi+1+\rho$. These corrections belong in commentary, not invisibly in the diplomatic source.

#### The addition assertion on p. 126 is too strong

For regular nonspecial $C$, and irreducible smooth $D$ with genus $\rho$, square $\nu$, and $m=CD>0$, the source correctly obtains

$$
(C+D)^2=n+\nu+2m,\qquad p_a(C+D)=\pi+\rho+m-1.
$$

The condition $m\ge\rho-\nu$ makes the virtual dimension of $C+D$ strictly exceed $r(C)$. With the moving-system and Bertini hypotheses, the intended irreducibility conclusion follows. This does **not** imply the next assertion that $C+D$ is regular and its restriction to $D$ nonspecial. The obstruction is explicit in

$$
0\longrightarrow\mathcal O_X(C)\longrightarrow\mathcal O_X(C+D)
\longrightarrow\mathcal O_D(C+D)\longrightarrow0.
$$

Since $h^1(C)=h^2(C)=0$, it gives

$$
h^1(C+D)=h^1(D,\mathcal O_D(C+D))
=h^0(D,\mathcal O_D(K-C)).
\tag{8.2}
$$

Restriction is complete because $h^1(C)=0$, but it can be special. A sufficient extra condition is $(C-K)D>0$. The source's weaker inequality does not force this.

**Worked counterexample, derived for this audit; confidence high.** Let $X\subset\mathbf P^1\times\mathbf P^2$ be a smooth hypersurface of bidegree $(2,4)$. Put $F=\mathcal O_X(1,0)$, $H=\mathcal O_X(0,1)$. Adjunction and intersections give

$$
K_X=H,\quad F^2=0,\quad FH=4,\quad H^2=2,\quad
q=0,\quad p_g=p_a=3.
$$

Take very ample $C=H+F$ and a smooth fibre $D\in|F|$, a plane quartic. Then $\rho=3,\nu=0,m=4\ge3$. Ambient restriction sequences and projective-space cohomology yield:

| Divisor | $h^0$ | $h^1$ | Square | Arithmetic genus | Actual $r$ | RR value with $i=0$ |
|---|---:|---:|---:|---:|---:|---:|
| $H+F$ | 6 | 0 | 10 | 9 | 5 | 5 |
| $H+2F$ | 9 | 1 | 18 | 15 | 8 | 7 |

The ambient exact sequences use $\mathcal O(-1,-3)$ for the first divisor and $\mathcal O(0,-3)$ for the second. The latter has one-dimensional second cohomology, producing $h^1_X(H+2F)=1$; the former has none. Moreover $(H+2F)|_D=\mathcal O_D(1)=K_D$, with speciality one. Every numerical hypothesis in the printed assertion holds, while regularity fails. This is an explicit verification, not a claim of historical novelty.

The asymptotic conclusion on pp. 126–127 survives: for a fixed $C$, choose $D=sH_0$ with $H_0$ ample and $s\gg0$. Both $D$ and $C+D$ are regular and very ample. The false assertion for arbitrary $D$ is unnecessary. Finally, strict negativity of a fundamental curve's square requires a big moving system. From $CD=0$ alone one cannot infer $D^2<0$: fibres of a pencil have square zero. In the big case, the Hodge index theorem supplies the required negativity.

### §9. Eliminating exceptional curves (pp. 127–128)

The source distinguishes a rational curve $E$ with $E^2=-1$, an exceptional curve of the first kind, from a rational curve with nonnegative square, called the second kind. The latter terminology is not modern exceptional-curve terminology.

Here the addition argument is valid despite the false general predecessor. If $m=CE>0$ and $E^2=\nu\ge-1$, then $\mathcal O_E(C+E)$ on $\mathbf P^1$ has degree $m+\nu\ge0$, so $H^1$ vanishes. The exact sequence proves regularity at every allowed step. Intersections evolve as

$$
(C+kE)E=m+k\nu.
$$

For $\nu=-1$, the process ends at $k=m$, when $E$ has degree zero for $C+mE$. For $\nu\ge0$, it continues indefinitely. The additive character is

$$
a(C)=2p_a(C)-2-C^2=K_XC,
$$

and $a(E)=-2-\nu\le-1$. Indefinite addition therefore produces moving classes with negative canonical intersection. These numerical steps are explicitly proved.

The geometric steps are sketches. Degree zero on $E$ alone does not establish a birational morphism or a smooth image point. The precise input is Castelnuovo contraction: a smooth rational $(-1)$-curve contracts to a smooth point. The construction with sufficiently ample $C$ and $C+mE$ has a modern proof in Stacks Project, Lemma 54.16.8, Tag 0C2M. This is a modern justification, not a claim that this source was the first historical repair.

Enriques asserts finiteness and excludes intersecting exceptional curves under his nonruled hypothesis; global finiteness is not proved here. If another $(-1)$-curve $E'$ meets $E$ in $a>0$, its image has square $-1+a^2\ge0$; for $a>1$, that image can be singular, so a smooth-rational-curve argument alone does not finish the reasoning. Modern nonruled minimal-model theory supplies the full interpretation. Successive contractions terminate because each lowers Picard number. The reducible configurations discussed are those arising from successive point blowups, contracted in reverse order, not arbitrary negative reducible divisors. Infinitely near points mean centres on successive models.

The closing statement that the transformation “fails” for ruled surfaces concerns eliminating both of the source's kinds. Ruled surfaces also have minimal models, meaning models without $(-1)$-curves, but can retain fibres of square zero. Every positive plurigenus of a ruled surface vanishes because $K$ restricts as $\mathcal O_{\mathbf P^1}(-2)$ on a general fibre. The classification of the negative-canonical moving-system alternative as ruled is deferred, not proved here.

### §10. Restriction of a small system to a large curve (pp. 128–131)

#### A precise statement and complete modern proof

For fixed divisors $C,E_0$, an ample $H$, and a smooth general $D_s\in|sH+E_0|$ with $s\gg0$, the restriction

$$
H^0(X,\mathcal O_X(C))\longrightarrow H^0(D_s,\mathcal O_{D_s}(C))
$$

is surjective, and eventually an isomorphism. In

$$
0\to\mathcal O_X(C-D_s)\to\mathcal O_X(C)
\to\mathcal O_{D_s}(C)\to0,
$$

duality identifies $H^1(C-D_s)^*$ with $H^1(K-C+D_s)$, which vanishes by Serre vanishing. Negative ample intersection gives $H^0(C-D_s)=0$. This works for any fixed line bundle $C$, effective or not, and identifies the required positivity precisely.

#### The geometric proof, its valid dimension step, and its gaps

Enriques starts from arbitrary $G\in|\mathcal O_D(C)|$. He seeks $G'$ such that $G+G'$ is characteristic and $G'$ is cut by an irreducible $B\in|D-C|$. Once available, the pencil through $G+G'$ has a member containing $B$; its residual $C$ cuts $G$. Resolve the basepoints: the induced pencil has residual degree zero on $B$, hence is constant there, which gives the claimed reducible member.

The linear-algebra step is sound. Two projective subseries of $\mathbf P^N$, of dimensions $a,b$, whose deficiencies are less than their own dimensions satisfy $N-a<a$ and $N-b<b$. Thus $a+b>N$, and they intersect. This is stronger than necessary but valid. No gap should be invented in this criterion.

The subsequent growth calculation has two mistakes and an omitted condition:

1. $n_s=s^2n$ and $\pi_s=s\pi+s(s-1)n/2-s+1$ are correct. Substitution gives
   $$
   r_s\ge p_a+\frac{s^2n}{2}+\frac{sn}{2}-s\pi+s.
   $$
   The print instead has $-sn/2$ and constant $-1$. Its quadratic leading term still supplies the intended asymptotic growth.
2. For characteristic defect $d$ and speciality $i=h^1(D,\mathcal O_D(D))$, the general identity is
   $$
   i=d+p_a+\omega(sL).
   $$
   The printed $i=d+p_a$ assumes regularity not established at that stage. The weaker $d\le i-p_a$ is sufficient.
3. The strict bound $i<\deg(K|_D)$ is false. Use
   $$
   h^0(M)\le\max(\deg M+1,0)
   $$
   on a smooth connected curve. On a K3 surface, $K|_D$ has degree zero and one section. The corrected bound still gives $i=O(s)$, since $KD=s(2\pi-2-n)$.

Imposing $G$ of length $sn$ costs at most $sn$ conditions, so the relevant series retain leading dimension $s^2n/2$, and the common subseries exists for large $s$. The print does not separately ensure that a suitable common divisor comes from an **irreducible** $B$, and only sketches passage from the worked special case to general fixed $C,E_0$. These are missing justifications, not counterexamples to the precise restriction theorem. The cohomological argument above supplies a complete replacement.

#### The literal effective-domination reading is too broad

The phrase “more ample than $sL$” on p. 129 cannot safely mean mere effective domination with an arbitrary residual varying with $s$.

**Diagnostic example derived for this audit; confidence high.** On $X=\operatorname{Bl}_p\mathbf P^2$, let $\ell$ be the pulled-back line and $E$ the exceptional curve. The divisor $H=C=2\ell-E$ is very ample. Put $D_s=2s\ell$, choosing a smooth member avoiding $E$, for $s\ge2$. Then

$$
D_s-C-(s-2)H=2\ell+(s-1)E
$$

is effective, so $D_s-C$ contains arbitrarily high multiples of an ample system in the literal order sense. Yet $D_s$ contracts $E$, and $D_s-C=(2s-2)\ell+E$ has fixed $E$. On $D_s$, $C|_{D_s}\simeq\mathcal O_{D_s}(2)$, which has six sections; $H^0(X,C)$, conics through $p$, has dimension five. Restriction is incomplete for every $s\ge2$.

This identifies a needed precision in terminology. It does not refute the ample-twist interpretation or the source's own warning about fundamental curves. A sufficient modern formulation is $D_s=sH+E_0$ with $E_0$ fixed, or directly $H^1(K-C+D_s)=0$. The footnote's printed $L_1$ is also an index slip: surrounding notation requires $L_s$.

### §11. Riemann–Roch for arbitrary complete systems (pp. 131–134)

Adjunction gives $K_D-D|_D=K_X|_D$. For large $D$, restriction identifies $H^0(K_X|_D)$ with $H^0(K_X)$, so the complete characteristic line bundle has speciality $p_g$, including $p_g=0$. Enriques treats the zero case separately: hypothetical speciality forces a sufficiently small $C$ to lie in its adjoint $C'$, contradicting absence of canonical divisors. The componentwise intersection comparison works once $D$ is sufficiently large against every component involved.

For any fixed effective $C$, the same reasoning gives

$$
h^1(D,\mathcal O_D(C+D))
=h^0(D,(K_X-C)|_D)=h^0(K_X-C)=i(C).
$$

Subtract $D$ from regular sufficiently positive $C+D$ to obtain $r\ge p_a+n-\pi+1-i$. This is the source's general inequality. Equation (8.1) identifies the omitted nonnegative quantity as $h^1(C)$. The proof is complete once the previous restriction lemma and positivity construction are made precise.

A multiplicity-$m$ basepoint condition has length $m(m+1)/2$, and imposes at most that many independent conditions. On the blowup,

$$
\widetilde C=f^*C-mE,\quad
\widetilde C^2=C^2-m^2,\quad
p_a(\widetilde C)=p_a(C)-m(m-1)/2.
$$

Use the complete prescribed-basepoint system on the blowup, not an arbitrary incomplete subsystem. Speciality is compatible because

$$
K_{\widetilde X}-\widetilde C=f^*(K_X-C)+(m+1)E
$$

has the same sections as $K_X-C$. The calculation iterates for infinitely near conditions.

The residual formulas on pp. 133–134 are correct. For $C_1+C_2=K$, $n_j=C_j^2$, $\pi_j=p_a(C_j)$, and $m=C_1C_2$,

$$
p^{(1)}=\pi_1+\pi_2+m-1,\quad
p^{(1)}-1=n_1+n_2+2m,\quad
m=2\pi_1-2-2n_1.
$$

Hence

$$
\pi_2=p^{(1)}-3\pi_1+2n_1+3,\qquad
n_2=p^{(1)}+3n_1-4\pi_1+3.
$$

The prose once reverses “genus and degree” for $n_1,\pi_1$; the equations consistently use degree and genus. Since $i(C_1)=r_2+1$, the paired equalities

$$
r_1=p_a+n_1-\pi_1-r_2+\omega_1,\qquad
r_2=p_a+n_2-\pi_2-r_1+\omega_2
$$

give $\omega_1=\omega_2$. Modern duality is exactly this symmetry, $h^1(C)=h^1(K-C)$. No residual formula needs a sign correction.

### §12. Deficiency of the characteristic series (pp. 134–137)

#### Exact meaning and proof of the bound

For a smooth connected member $C$ of a complete moving system,

$$
0\to\mathcal O_X\to\mathcal O_X(C)\to\mathcal O_C(C)\to0
$$

identifies the characteristic vector space with the image of $H^0(C)$ modulo the defining section. Therefore

$$
\boxed{d=\dim\ker[H^1(\mathcal O_X)\to H^1(\mathcal O_X(C))]\le q.}
\tag{12.1}
$$

If $h^1(C)=0$, equality holds, so sufficiently ample systems attain the maximum $q$.

The source first assumes $i(C)=0$ and uses defects $d,d'$ of the characteristic and canonical restriction series. Curve RR gives

$$
r=n-\pi+p_g+d'-d+1,\qquad
\omega(C)=q+d'-d.
$$

For a regular sufficiently large system, $d'=0$, hence $d=q$. The comparison lemma then proves the general bound. Its rank calculation is sound: for $A=C_1+C_2$, dimensions $r=\dim|A|$, $r_j=\dim|C_j|$, and intersection scheme $G$ imposing $s-\varepsilon$ conditions, completeness on $C_1$ gives

$$
d_1=r-r_1-r_2-(s-\varepsilon).
$$

The corresponding image on $C_2$ has relative defect equal to this expression, which is at most $d_2$. Thus $d_1\le d_2$. Scheme lengths replace point counts for nontransverse intersections.

Choose $D$ sufficiently ample. Then $C+D$ is regular and restricts completely to $C$ because $H^1(D)=0$. The printed condition $(CD)>n-\pi$ reverses the threshold in §8, and the cited arbitrary-addition regularity statement was too strong. Neither defeats this asymptotic proof: the available ample $D$ supplies all required vanishings.

When $q=0$, every complete smooth moving system has complete characteristic series. In the projective reformulation, “normal” means **linearly normal**, not normality of local rings or projective normality in all degrees. A linearly normal embedding of a regular surface has linearly normal smooth hyperplane sections. Failure of section linear normality implies irregularity.

#### The scroll illustration needs a correction

For a ruled surface over a genus-$g$ curve, $p_g=0,q=g,p_a=-g$. If $H$ embeds it as a scroll, then $H$ has fibre degree one and a smooth general member has genus $g$. The correct formulas are

$$
r=n-2g+1+h^1(X,H),\qquad
d=g+h^1(C,H|_C)-h^1(X,H).
\tag{12.2}
$$

The source describes the extra term in $r$ as the speciality of the hyperplane section and concludes that $d=g$ in every nonconical normal case. This identifies different cohomology groups and is false without another condition.

**Worked counterexample derived here; confidence high.** Let $B\subset\mathbf P^2$ be a smooth plane quartic, $X=B\times\mathbf P^1$, and

$$
H=K_B\boxtimes\mathcal O_{\mathbf P^1}(1).
$$

The Segre embedding in $\mathbf P^5$ is a smooth nonconical linearly normal scroll. One has $H^2=8$, $p_a(H)=3$, $h^0(H)=6$, and $h^1(H)=2$ by Künneth. A general section is the graph of a degree-four map $B\to\mathbf P^1$ from a basepoint-free pencil in $H^0(K_B)$. Hence $C\simeq B$, $H|_C\simeq2K_B$, $h^0(H|_C)=6$, and $h^1(H|_C)=0$. The characteristic vector image has dimension $6-1=5$, so $d=1$, whereas $q=g=3$. This does not rely on an incomplete embedding or a cone.

The Segre footnote also has a date mismatch. Institutional author and BDIM catalogues identify the relevant *Recherches générales…*, part II on ruled surfaces, as *Mathematische Annalen*, 34 (1889), 1–25; the abbreviated printed reference says 1892. This verifies the matching work's date, not the exact theorem or priority of every assertion attributed to it. The original article has not been audited in full here.

#### Irrational pencils and algebraic families

For a morphism $f:X\to B$ with connected fibres, Leray injects $H^1(B,\mathcal O_B)$ into $H^1(X,\mathcal O_X)$, so $q(X)\ge g(B)$. Resolve a rational pencil and use Stein factorization before applying this. The source attributes the result to Castelnuovo and relates it to the inequality for families of inequivalent divisors.

Precisely, a family whose image in $\operatorname{Pic}(X)$ has dimension $d$ satisfies $d\le q$. In characteristic zero the Picard scheme is smooth of dimension $h^1(\mathcal O_X)$, and its tangent space at the identity is $H^1(\mathcal O_X)$ (Kleiman, 2005, Theorem 5.11 and Corollary 5.14). The source's infinitesimal argument requires a smooth parameter point and the expected tangent rank. It is not a proof that every infinitesimal normal deformation integrates, nor a general completeness theorem for continuous characteristic systems. No stronger assertion is needed. The construction using groups of $g$ fibres corresponds to the dominant Abel map $\operatorname{Sym}^gB\to\operatorname{Pic}^gB$.

### §13. Historical note (pp. 137–142)

#### Evidentiary status

These pages are Enriques's retrospective account as a participant. The following are **claims made by Enriques**, not independently certified priority findings:

| Pages | Enriques's report | Audit conclusion |
|---|---|---|
| 137–138 | Cayley's negative arithmetic count for ruled surfaces; Zeuthen's invariance with singularity restrictions; Noether's early comparison of the genera | The modern invariants are checked. Exact original restrictions and Noether's reported presumptions have not been reconstructed from all original papers. |
| 138 | Castelnuovo 1891 and Picard/Humbert irregular examples; “hyperelliptic” surfaces with $p_g=1,p_a=-1$ | These invariants fit abelian-type examples. The old term is not today's bielliptic surface, whose $p_g=0,q=1$. Priority remains attributed. |
| 138–139 | Enriques 1893/1896; Picard 1905 adjoint regularity; Severi 1908 algebraic route | The modern mathematical content is supplied. Original proof scope has not been exhaustively verified. |
| 139 | Noether 1886 implicitly assumed completeness of two restricted series | This is Enriques's explicit criticism. The defect identity verifies its mathematical importance; the audit has not invented it. |
| 139–140 | Castelnuovo 1896/1897 maximum defect and Severi 1903/1905 simplifications | The resulting theorem and proof route are checked; chronology is not independently adjudicated. |
| 141–142 | The 1940 proof is simpler; reducible cases were known early “at least implicitly,” and explicit in joint work around 1900 | Simplicity and implicit knowledge are authorial judgments. The subtraction proof does cover reducible classes. The joint paper's 1900/1901 dating needs care. |

The Noether paragraph has a source misprint: the restricted canonical series should have projective dimension $p_g-i-1$, since $p_g-i$ is its vector dimension. The printed exponent is $p-i$. With defects $d,d'$, the correct equality is

$$
r=p_g+n-\pi+1-i+d'-d.
$$

Completeness of the surface systems alone does not establish completeness of either restriction. Both restriction defects zero suffice for the displayed Noether equality; the defects could also cancel, so the equality alone does not prove individual completeness.

The next historical paragraph displays $r\ge p_g+n-\pi+1$ without specifying nonspeciality. This cannot apply to every system: on a regular surface with $p_g>1$, taking $C=K$ gives $r=p_g-1$, whereas that right side is $p_g$. The summary therefore needs the restriction $i(C)=0$, or the missing speciality term. This is a scope qualification of the retrospective paragraph, not a finding about the exact wording of Enriques's 1893 original paper.

Picard's theorem is discussed for simple systems with at least three parameters. A modern translation must retain the actual positivity/birational hypotheses. Fixed ample twists are handled by Serre vanishing; broader big-nef adjoint vanishing is a characteristic-zero theorem. This audit does not identify an unspecified modern result as the first historical repair by a named author.

#### The $Af+B\varphi$ route

Let $G$ be the plane complete-intersection scheme defined by $f_n,f_s$ on $z=0$. If $f_m$ vanishes on $G$, then modulo $z$ its class lies in the ideal generated by $f_n|_{z=0}$ and $f_s|_{z=0}$. Choose homogeneous coefficients of degrees $m-n,m-s$, lift them, and divide the remaining polynomial by $z$:

$$
f_m=Af_n+Bf_s+zf_{m-1}.
$$

Negative coefficient degree means that coefficient is zero. For general transverse sections, pointwise and scheme-theoretic vanishing coincide. For nonreduced intersections, scheme-theoretic vanishing is required; merely passing through the support is insufficient.

Enriques summarizes Severi's descent from degree $m$ to $m-1$ for adjoints through the double points of $D_s=F_n\cap F_s$. The descent and exact adjoint/conductor conditions are not developed here; they are assumed input, not proved by the polynomial identity alone. For $s>n-4$, a degree-$(n-4)$ surface through all intersections of $F_s$ with each double-curve component must contain that component by Bézout, provided the intersections are general and transverse. It is therefore an adjoint of $F_n$, giving the stated completeness in this setting.

The remaining deductions repeat the audited route: restriction completeness gives RR; sufficiently high regularity gives characteristic defect $q$; the comparison lemma gives the universal bound. Eventual regularity is explicitly deferred to §15. The unclosed quotation mark on p. 141 is printed. By contrast, the transcription's $D'_s$ at line 1321 is an actual transcription error: the 300-dpi scan reads $D_s$, without a prime.

### §14. Virtual curves and effectivity (pp. 142–147)

#### Numerical tests and the positive-square criterion

A virtual curve $C=A-B$ is a divisor class whose complete system may be empty. Adding a common sufficiently ample divisor makes $A,B$ regular, smooth in general, basepoint free, and without contracted curves while preserving $C$. This reduction is crucial; arbitrary nonample representatives cannot be substituted.

If $C$ is effective,

$$
C(A+B)=A^2-B^2\ge0,\quad
CB=AB-B^2\ge0,\quad CA=A^2-AB\ge0.
$$

Thus $A^2\ge B^2$ and $B^2\le AB\le A^2$, also necessary if any positive multiple of $C$ is effective. For nonzero effective $C$ and ample $A,B$, the latter inequalities are strict. The possible zero divisor explains the weak form.

The sufficient criterion is correct: if $C^2>0$ and $A^2>AB>B^2$, every sufficiently large $mC$ is effective. Indeed $BC>0$, so $B(K-mC)<0$ for $m\gg0$, and $h^0(K-mC)=0$. Meanwhile

$$
\chi(mC)=\chi(\mathcal O_X)+\frac{m^2C^2-mKC}{2}
$$

has positive quadratic leading term. Hence $h^0(mC)=\chi(mC)+h^1(mC)>0$.

Enriques instead subtracts $B$ repeatedly from $mA$. At the last step the restriction degree is

$$
(mA-(m-1)B)B=AB+(m-1)(AB-B^2),
$$

eventually greater than $2g(B)-2$. All earlier restriction degrees are at least as large, so they too are nonspecial. This supplies the uniform induction needed to justify the apparently assumed existence of the penultimate residual. The source does address that issue; it should not be called simply circular. The formulas

$$
n_m=m^2n,\qquad \pi_m=m\pi+\frac{m(m-1)}2n-m+1
$$

are correct, including the final sign and constant.

#### The missing hypothesis in the plurigenus bound

The simplified inequality printed on pp. 142–144 is

$$
P_m\ge p_a+1+\frac{m(m-1)}2K^2\qquad(m>1).
$$

The exact modern equality is

$$
\boxed{P_m=\chi(\mathcal O_X)+\frac{m(m-1)}2K^2+
h^1(mK)-h^0((1-m)K).}
\tag{14.1}
$$

The simplified bound follows if $h^0((1-m)K)=0$. A sufficient hypothesis is positive $KH$ for an ample $H$, as in the intended nontrivial positive canonical class of the nonruled setting. The condition $K^2>0$ alone does not choose the positive component: $\mathbf P^2$ has $K^2=9$ but every $P_m=0$. The unrestricted formula also fails on a K3 surface: $K=0,p_a=1,P_m=1$, whereas the claimed lower bound is two. There $(B+mK)|_B=\mathcal O_B(B)=K_B$, so the asserted nonspeciality on p. 143 fails by one. These are qualifications of a printed mathematical assertion, not OCR corrections. Retain canonical positivity or the full term in (14.1).

#### Boundary square and torsion

The source correctly says the positive-square argument is inconclusive for $C^2=0$ and $C^2<0$. An explicit square-zero example clarifies why. On $X=B\times E$, with $E$ elliptic, take $b\in B$ and a nontorsion degree-zero $P\in\operatorname{Pic}^0(E)$. Put

$$
L=\operatorname{pr}_B^*\mathcal O_B(b)\otimes\operatorname{pr}_E^*P.
$$

Then $L^2=0$ and $L$ meets an ample divisor positively, yet $h^0(mL)=0$ for all $m>0$, because $P^m$ has no sections. Removing the twist yields a numerically equivalent class with effective multiples. **This example is supplied by the audit; confidence high.** It shows that numerical data do not settle boundary effectivity. For negative square, an effective negative curve and its negative already illustrate opposite effectivity behavior at the same square.

Now assume $A^2=AB=B^2$, retaining positive representatives. Then $C^2=0$, $C(A+B)=0$, and $C$ is numerically trivial. An effective numerically trivial divisor must be zero because every nonzero effective divisor meets an ample divisor positively. Hence

$$
|mC|\ne\varnothing\quad\Longleftrightarrow\quad mC\sim0.
$$

Enriques's $\equiv$ in this passage means linear equivalence; reading it as today's numerical-equivalence symbol would erase the substantive issue.

On a regular complex surface, numerical triviality implies torsion: some multiple is algebraically trivial, the torsion components of the Picard scheme form a finite group, and $q=0$ makes $\operatorname{Pic}^0$ trivial. Therefore some $mA\sim mB$. Without regularity, some multiples are still algebraically equivalent, but need not be linearly equivalent (Kleiman, 2005, Definition 6.1, Theorem 6.3, Theorem 6.16, Corollary 6.17). Equal zero intersections for arbitrary nonample isotropic divisors do not suffice for this conclusion.

The source's bounded-degree-family argument sketches the existence and boundedness of infinitely many twists; the Picard proof supplies the missing precision. References to Severi, Todd, Hodge, B. Segre, and Bronowski remain Enriques's citations, without an invented claim of historical priority.

#### General virtual RR and speciality

For $C=A-B$, define $i=h^0(K-C)$ even when $|C|$ is empty. Equation (8.1) remains valid. Thus

$$
p_a+n-\pi+1-i\ge0
$$

implies $h^0(C)\ge1$. This ensures effectivity, not irreducibility or a moving system. The source takes large $D=sB$, restricts $K-C$ completely to it, and obtains speciality $i$ for $\mathcal O_D(C+D)$. Subtraction then gives the inequality. Although written for $i>0$, the same exact-sequence proof treats $i=0$.

For effective $C$, multiplication by its defining section injects $H^0(K-C)$ into $H^0(K)$, giving $i\le p_g$. For virtual $C=-mH$, $i=h^0(K+mH)$ grows quadratically and is unbounded. The final assertion that the residual lies inside the canonical system is correct when this means translation by a fixed effective divisor representing $C$, not literal inclusion of unrelated vector spaces without specifying the multiplier.

#### Additional contributions for §§8–14 and confidence

The $(2,4)$-hypersurface counterexample, plane-quartic scroll counterexample, blowup diagnostic for literal effective domination, and nontorsion-twist boundary example are calculations supplied by this audit. Their line-bundle and cohomology calculations are displayed above; confidence is high. No claim of novelty or historical priority is attached. The cohomological reconstructions use standard results and are not newly attributed historical repairs.

Specific limits remain. The isolated-point wording does not state all singularity assumptions. “Normally large” admits an overly literal reading, which has been tested separately from a precise sufficient statement. Not all original historical papers were read, so their history is attributed rather than certified. Faint punctuation/ink distinctions remain optically uncertain; conservative readings and confidence are explicitly recorded in the corrections ledger. None affects a mathematical formula.

### §15, pp. 147–150: regularity, complete restrictions, and contracted curves

#### Model and cohomological conventions

Throughout the modern reconstructions, $X$ is a smooth connected projective surface over $\mathbf C$. An effective divisor is a nonzero integral combination $D=\sum m_i\Gamma_i$ of irreducible curves, with $m_i>0$; it is allowed to be reducible or nonreduced. We write

$$
p_g=h^0(K_X),\qquad q=h^1(\mathcal O_X),\qquad
p_a(X)=\chi(\mathcal O_X)-1=p_g-q,
$$

$$
n=D^2,\quad \pi=p_a(D)=1+\tfrac12(D^2+K_XD),\quad
r=h^0(D)-1,\quad i=h^0(K_X-D).
$$

The surface Riemann–Roch formula becomes

$$
r=p_a(X)+n-\pi+1-i+h^1(D).
\tag{15.1}
$$

Consequently Enriques's superabundance is precisely $\omega=h^1(D)$. Empty complete systems have projective dimension $-1$. Arithmetic genus, rather than the sum of the genera of the reduced components or the genus of a normalization, is required in all addition formulas. Where the classical system has prescribed multiple base points, one must first specify the smooth model and strict-transform system on which its degree and genus are calculated; an adjoint on that model need not be the naive divisor $K_X+D$ on a model before resolving those base points.

The “pure” canonical system in §§18–20 is interpreted on a minimal smooth model. For a surface of general type this gives $K_X$ nef and $K_X^2>0$, and the historical absolute linear genus is $p^{(1)}=K_X^2+1$. On a nonminimal model the actual canonical square is smaller. Purity does **not** mean that every canonical member is irreducible, reduced, or free of fixed components: §18 exists precisely to disprove that interpretation. An elliptic curve of square $-1$ is not an exceptional curve of the first kind; that term refers to a smooth rational curve of square $-1$.

The nefness used below can be justified directly in the situation of the source. Since $p_g>0$, choose an effective canonical divisor. If an integral curve $\Gamma$ satisfied $K_X\Gamma<0$, it would occur in that divisor and would have $\Gamma^2<0$. Adjunction then gives $2p_a(\Gamma)-2=K_X\Gamma+\Gamma^2\le-2$. Both negative intersection numbers must equal $-1$, and $p_a(\Gamma)=0$, so $\Gamma$ is a smooth rational $(-1)$-curve. Removing such curves therefore makes $K_X$ nef. With $K_X^2>0$, Riemann–Roch gives quadratic pluricanonical growth, hence bigness and general type. Thus the modern positivity assumptions follow from the stated effective canonical class, absolute linear genus greater than one, and passage to the pure/minimal model; they are not additional unexplained conclusions.

The source-status labels in the accompanying claims file describe what these pages do, not whether a modern theorem is true. In particular, the theorem at p. 156 is printed after an explicit admission that its proof depends on an unproved working hypothesis. Modern repairs below are not retrospectively credited to Enriques. No assertion of historical priority beyond the verified references is intended.


#### Riemann–Roch and the Picard argument

The definitions at p. 147 follow directly from (15.1). The main adjoint assertion is

$$
h^1(K_X+C)=0,\qquad \dim|K_X+C|=p_a(X)+p_a(C)-1.
\tag{15.2}
$$

For effective $C>0$, $h^2(K_X+C)=h^0(-C)=0$, so the dimension follows from the vanishing. The general cohomological diagnostic, valid for every effective divisor, is

$$
h^1(K_X+C)
=h^0(\mathcal O_C)-1+
\dim\ker\bigl[H^1(\mathcal O_X)\longrightarrow H^1(\mathcal O_C)\bigr].
\tag{15.3}
$$

Indeed, take cohomology of $0\to\mathcal O_X(-C)\to\mathcal O_X\to\mathcal O_C\to0$, use $H^0(-C)=0$, and apply Serre duality. This is recorded explicitly as Fact 1 in Mendes Lopes (1996, p. 2 of the author manuscript). Formula (15.3) isolates two logically different issues: global functions on a possibly nonreduced curve, and injectivity of the irregularity restriction map.

Enriques states his version with $\dim|C|\ge q$, but his proof on p. 148 starts with $\dim|C|>q$. His auxiliary lemma is introduced, “for simplicity,” for both systems of dimension greater than one. Thus the displayed proof does not itself cover the equality case or all pencil cases of its statement. This is a difference between theorem and proof scope, not evidence that the theorem is false.

The lemma says that $|C|$ restricts completely to a general $L\in|C+D|$ when $\dim|D|>q$. Its characteristic-series proof uses the earlier bound $\delta\le q$, a projective dimension count to find a residual group $G'$, and a pencil from which $D$ can be detached. It suppresses the exact restriction maps and the assumptions excluding extra fixed intersections. The modern sequence is

$$
0\longrightarrow\mathcal O_X(-D)
\longrightarrow\mathcal O_X(C)
\longrightarrow\mathcal O_L(C)\longrightarrow0.
\tag{15.4}
$$

Thus $H^1(-D)=0$ is a transparent sufficient condition for complete restriction. When the moving system has a surface as image, its divisor is nef and big on the relevant smooth model; Ramanujam vanishing supplies this condition in characteristic zero. Reid (1996, Theorem 3.13) gives the precise effective nef-and-big statement $H^1(-D)=0$.

For completeness, the exceptional numerical case of a moving irreducible system with $C^2=0$ can be treated separately in the complex setting. Its complete irreducible pencil has rational base, since a moving degree-one linear system on its Stein-factor base curve forces that curve to be $\mathbf P^1$. A holomorphic one-form restricting to zero on a general fiber descends to the base: on the smooth locus of the fibration it has no vertical part, and closedness forces its horizontal coefficient to be constant along fibers; extension across the finitely many exceptional fibers gives a form on the base. Since $H^0(\mathbf P^1,\Omega^1)=0$, restriction of holomorphic one-forms is injective. Hodge conjugation then gives the required injection on $H^1(\mathcal O)$. This supplies a modern proof route for the pencil boundary, rather than pretending that the strict inequality in the printed proof covers it. This argument is an audit reconstruction using standard complex Hodge theory, not an identification of Picard's original proof.

The numerical residual calculation on p. 148 is correct. Put $L=C+D+K_X$, $\rho=p_a(D+K_X)$, $m=(D+K_X)^2$, and $s=C(D+K_X)$. Then

$$
p_a(L)=\pi+\rho+s-1,\qquad
\deg((D+K_X)|_L)=m+s.
$$

The two restricted systems are residual because

$$
(K_X+C)+(K_X+D)=K_X+L.
$$

When their restrictions are complete, curve Riemann–Roch gives

$$
\dim|(K_X+C)|_L|
=p_a+m-\rho+1-\{m+s-p_a(L)\}-1
=p_a+\pi-1.
$$

The kernels $H^0(-C)$ and $H^0(-D)$ vanish, so the restricted and surface projective dimensions agree. These are the missing cohomological justifications for the dimension identifications.

#### High multiples and the exact positivity needed

At pp. 148–149 Enriques proves that high multiples of an irreducible system of dimension at least two are regular when there are no fundamental, that is contracted, curves. On a base point free model, such a divisor $C$ is nef, has $C^2>0$, and satisfies $C\Gamma>0$ for every irreducible curve. Nakai–Moishezon makes it ample; Serre vanishing then gives $H^1(sC)=0$ for $s\gg0$. Mere bigness does not give this conclusion.

The source chooses $D=hC-K_X\ge0$, starts from the regular $K_X+sC$, and adds the finitely many irreducible components of $D$, counting repetitions. If $L^2=\nu$, $p_a(L)=\rho$, and $C L=t>0$, the correct identity is

$$
(K_X+sC)L=st+2\rho-2-\nu.
\tag{15.5}
$$

The scan at p. 149 prints $r$ in place of $\nu$; this is a source misprint, not OCR. If $L$ is added again, its self-intersection contributes once more. In the printed negative case $L^2=-\nu'$, the next intersection is $st+2\rho-2$, as stated.

This argument invokes the earlier addition criterion of §8. A defective weak numerical criterion in that earlier discussion must not be silently reused here. Fortunately $s\gg0$ supplies more than the displayed weak inequality: at every one of the finitely many additions, the restriction to the integral component $L$ has arbitrarily large degree, so its residual to $\omega_L$ has negative degree and its $H^1$ vanishes. Explicitly, for any fixed partial sum $E\le D$,

$$
\deg\bigl((K_X+sC+E+L)|_L\bigr)
=st+(K_X+E+L)L\longrightarrow+\infty.
$$

The finitely many thresholds can be met simultaneously. The restriction exact sequence then preserves $H^1=0$ at each addition. Thus this conclusion survives independently of the insufficient general addition criterion; it is the unbounded $st$ term that repairs the proof.

#### Positive-genus contracted curves and a sign slip

Let a base point free $C$ contract an integral curve $\theta$ of genus $\rho>0$, with $\theta^2=-\nu<0$. Because the associated morphism contracts $\theta$, $\mathcal O_X(sC)|_\theta\simeq\mathcal O_\theta$, and a section not vanishing at the image point shows that restriction has rank one. Consequently

$$
r(sC-\theta)=r(sC)-1.
$$

The weaker numerical assertion $sC\cdot\theta=0$ alone would not establish triviality or rank one. Adjunction gives

$$
(sC-\theta)^2=(sC)^2-\nu,
\qquad
p_a(sC-\theta)=p_a(sC)-\nu-\rho+1.
$$

For large $s$, the speciality indices vanish, and the virtual dimension therefore **increases** by $\rho-1$ upon removing $\theta$. The printed p. 150 says that it decreases. The final formula is nevertheless correct:

$$
\omega(sC)=\omega(sC-\theta)+\rho\ge\rho.
\tag{15.6}
$$

The extra term can come from the infinitesimal neighborhoods of the exceptional curve; its reduced genus need not exhaust the defect.

#### Completing the omitted ordinary-multiple-point calculation

The final example is uniform only with an ordinary isolated hypersurface point. For the displayed total global defect, assume that this point is the only singularity contributing higher direct-image cohomology of the resolution (for example, the projective hypersurface is otherwise smooth). Contributions from other nonrational singularities would have to be added. Assume the degree-$i$ tangent cone is a smooth plane curve, $i>3$, and the blowup resolves the point. Its exceptional curve $E$ then satisfies

$$
g(E)=\frac{(i-1)(i-2)}2,\qquad
\mathcal O_E(-E)=\mathcal O_E(1),\qquad E^2=-i.
$$

Let $H$ be the pullback of a hyperplane section and $D_j=sH-jE$. The exact sequences

$$
0\to\mathcal O_X(D_{j+1})\to\mathcal O_X(D_j)
\to\mathcal O_E(j)\to0
$$

have surjective maps on $H^0$ for $s\gg0$ and fixed $j\le i-3$: ambient homogeneous degree-$j$ initial forms supply every section of $\mathcal O_E(j)$, and high-degree global sections interpolate the finitely many required jets. Curve duality gives

$$
h^1(\mathcal O_E(j))
=h^0(\mathcal O_E(i-3-j))
=\binom{i-1-j}{2}.
$$

For $j\ge i-2$, all the subsequent exceptional-neighborhood graded pieces have $H^1=0$; formal functions and high-degree Serre vanishing give $h^1(D_{i-2})=0$. The recurrence therefore yields the omitted answer

$$
\boxed{h^1(D_j)=\binom{i-j}{3}\quad(0\le j\le i-2),\qquad
\omega(sH)=\binom i3.}
\tag{15.7}
$$

This is an original worked calculation for the audit, with high confidence under the stated ordinary-point and global-positivity hypotheses. It is not asserted for arbitrary isolated singularities of multiplicity $i$. For $i=4$, the exceptional genus is 3 while the defect is 4, concretely explaining the strict inequality in (15.6).

### §16, pp. 150–152: regular adjoints of reduced connected divisors

#### The reduced argument is sound

In §16, $q=0$ and $p_g=p_a=p>0$. Every system containing the canonical system has an effective residual $L$, hence is $|K_X+L|$. For integral $L$, the adjunction sequence

$$
0\to\mathcal O_X(K_X)\to\mathcal O_X(K_X+L)
\to\omega_L\to0
$$

is surjective on global sections because $h^1(K_X)=q=0$. Since $h^0(\mathcal O_L)=1$, duality on the Gorenstein curve $L$ gives $h^0(\omega_L)=p_a(L)$, and $\dim|K_X+L|=p+p_a(L)-1$. Smoothness of the integral curve is unnecessary if dualizing sheaves and arithmetic genus are used.

For a reduced connected divisor, the intersection graph admits an ordering with every initial union connected. Grow a connected set of vertices one vertex at a time; a proper connected set has an edge to its complement. This proves the lemma and corollary at p. 151 without relying on any self-intersection sign.

At each step write $L=A+B$, where $B$ is the newly added **integral** component, $A$ is the previous connected union, and $j=AB\ge1$. Then

$$
p_a(L)=p_a(A)+p_a(B)+j-1,
$$

$$
(K_X+L)|_B=\omega_B(A),\quad
\deg\omega_B(A)=2p_a(B)-2+j.
$$

The dual $H^0(\mathcal O_B(-A))$ vanishes because it has negative degree on the integral curve. This proves nonspeciality and the upper bound $r_B\le p_a(B)-2+j$ for the image series. Comparing with the surface Riemann–Roch lower bound forces equality, proves regularity, and completes the induction. One must not replace integral $B$ by an arbitrary connected reducible curve and infer nonspeciality from its total degree alone: degree can be distributed unevenly among its components.

For a reduced curve with $s$ connected components, (15.3) gives exactly

$$
h^1(K_X+L)=s-1.
\tag{16.1}
$$

The two-disjoint-components calculation at p. 152 is correct: $p_a(L)=\pi_1+\pi_2-1$, $\dim|K_X+L|=p+p_a(L)$, and $\omega=1$. The last sentence of §16 says that analogous exceptional-multiple calculations are easy, but gives no formula. For nonreduced cycles the answer is controlled by $h^0(\mathcal O_L)$, not merely the count of connected supports.

### §17, pp. 152–156: numerical connectedness, multiplicities, and the admitted hypothesis

#### Numerical 1-connectedness is the correct nonreduced definition

Enriques's “arithmetically connected” means

$$
D=A+B,\quad A,B>0\quad\Longrightarrow\quad AB>0.
\tag{17.1}
$$

Every effective integral subcycle counts; the two pieces may share underlying components. This is modern numerical 1-connectedness. For reduced divisors it agrees with ordinary connectedness, because distinct effective components have nonnegative intersection. For nonreduced divisors, negative self-intersections change the condition.

A simple diagnostic shows why connected support is inadequate. If $E\simeq\mathbf P^1$ is an exceptional curve with $E^2=-1$, then $2E$ has connected support, but

$$
0\to\mathcal O_E(1)\to\mathcal O_{2E}\to\mathcal O_E\to0
$$

gives $h^0(\mathcal O_{2E})=3$. It is not 1-connected because the split $E+E$ has intersection $-1$. These extra sections are nilpotents; no topological path argument can exclude them.

The source cites Franchetta for failures of the naive component-addition rule, without displaying his examples. Here is an independent, fully checkable illustration, **constructed for this audit; not claimed to be Franchetta's example**. In $\mathbf P^2$, choose a smooth conic $A_0$ and a transverse line $B_0$. Blow up five points of $A_0\setminus B_0$ and four points of $B_0\setminus A_0$. Their strict transforms satisfy

$$
A^2=-1,\quad B^2=-3,\quad AB=2.
$$

The cycle $L=2A+B$ is 1-connected: up to exchanging the two sides, its nontrivial splits have intersections $A(A+B)=1$ and $2AB=4$. Moreover $LB=1>0$. Nevertheless $L+B=2(A+B)$ is not 1-connected, since the split $(A+B)+(A+B)$ has intersection 0. This directly verifies the phenomenon described at p. 153. Confidence is high; all subcycles of $L$ have been checked.

#### Franchetta's two lemmas, as actually proved in the text

Theorem I is a useful finite descent. If $D=A+B$ with $AB\le0$, and $A$ is not 1-connected, write $A=A_1+A_2$ with $A_1A_2\le0$. At least one $A_iB\le0$, since their sum is $AB\le0$. For that $A_i$, its intersection with the entire residual remains nonpositive. Repeating decreases the sum of the coefficients, so the process terminates with a 1-connected subcycle having nonpositive boundary. This proves the contrapositive of the stated criterion. The missing verb on p. 154 is a grammatical source misprint, not a mathematical obstruction.

Theorem II requires $D$ to have a nontrivial decomposition. Choose a proper 1-connected subcycle $B$ minimizing its positive boundary $B(D-B)$. If $A=D-B$ is not 1-connected, Theorem I provides a 1-connected $A_1\le A$ with $A=A_1+A_2$, $A_1A_2\le0$. Connectedness of $D$ implies $BA_1,BA_2>0$. Hence

$$
A_1(B+A_2)\le A_1B<AB,
$$

contradicting minimality. Thus both pieces are 1-connected. The wording must exclude an irreducible reduced divisor, which admits no proper nonzero effective split; this is a harmless scope qualification, not a counterexample to the intended statement.

#### The p. 155 working hypothesis must remain visible

The geometric proof on pp. 154–155 takes a very positive regular $C$, sets $D=C+L$, and aims to prove that $|C|$ cuts a complete series on $D$. Restrictions of the fixed $L$ and $K_X+L$ to a sufficiently positive $D$ can be justified by Serre vanishing and duality. The remaining obstruction is specifically $H^1(-L)$, which does not disappear merely because $C$ is large.

Enriques constructs a pencil with a prescribed characteristic group and asserts that imposing an additional point on $L$ forces the entire $L$, with every multiplicity, to detach. He then explicitly says that he lacks an exhaustive proof and introduces this as a working hypothesis, to which the following result and its consequences are subordinate. This is an unusually clear admission; the audit must preserve it. Support containment of a nonreduced divisor is insufficient to prove containment of its full scheme structure.

Conditional on complete restriction, the calculation itself is correct. With $n=C^2$, $\rho=p_a(C)$, $m=CL$, and $\pi=p_a(L)$, the series $C|_D$ has degree $n+m$, projective dimension $p+n-\rho+1$, and ambient curve genus $\pi+\rho+m-1$. Its speciality index is $p+\pi$, so its canonical residual has dimension $p+\pi-1$. The scan prints $(CL')$ for this residual; it should be $(DL')$, since it lies on $D$.

#### A complete modern proof replacing the hypothesis

The exact needed theorem is that numerical 1-connectedness implies $H^0(\mathcal O_L)=\mathbf C$. Ramanujam (1972, Lemma 3, reprinted at p. 127 of *C. P. Ramanujam—A tribute*) proves this for effective divisors; Reid (1996, Lemma 3.11(ii)) gives a particularly transparent induction. These are concrete repair references, without an unverified claim about the earliest historical repair.

Here is the short induction in the present notation. Start with a reduced integral component $A\le L$, so $h^0(\mathcal O_A)=1$. If $A<L$, numerical connectedness of the **whole** $L$ gives $A(L-A)>0$, so some integral component $\Gamma\le L-A$ satisfies $A\Gamma>0$. The divisor restriction sequence

$$
0\to\mathcal O_\Gamma(-A)\to\mathcal O_{A+\Gamma}
\to\mathcal O_A\to0
$$

has $H^0(\mathcal O_\Gamma(-A))=0$. Therefore $h^0(\mathcal O_{A+\Gamma})\le1$, while constants supply a nonzero section. Induct until $A=L$, counting repeated components. Crucially, the induction preserves $h^0=1$; it does **not** claim that every partial sum is 1-connected. This is precisely why Franchetta's obstruction to the naive geometric composition lemma does not invalidate it.

Now $q=0$, and

$$
0\to\mathcal O_X(-L)\to\mathcal O_X\to\mathcal O_L\to0
$$

gives $H^1(-L)=0$, because the map on constants is an isomorphism. Duality yields $H^1(K_X+L)=0$. The assumption $p_g>0$ is not needed for this adjoint-vanishing argument; $q=0$ and numerical connectedness suffice. This proves the theorem at p. 156 for all effective 1-connected divisors, including arbitrary negative multiple components, and fills the exact restriction obstruction in the preceding proof. It does not assert that every informal pencil formulation of the detachment principle is valid without its additional base-locus hypotheses.

### §18, pp. 156–158: reducible pure canonical systems and verified double-plane constructions

#### What the counterexamples refute

The two alternatives attributed to Noether—exceptional rational $(-1)$-components, or a pure canonical system of square zero composed with elliptic curves—are not an exhaustive classification. A minimal general-type surface can have fixed rational $(-2)$-curves or fixed positive-genus curves. The three examples in the text establish this once their branch curves, resolutions, and minimal models are constructed. The source abbreviates all three constructions and gives only a partial constant-count argument for the second.

The following explicit constructions are **original worked reconstructions for this audit**. They are not claimed to be historically new surfaces or the original constructions intended by Enriques. Their purpose is to verify existence, exact singularity type, and every stated invariant. Confidence is high under the generic choices described below.

#### A common interpolation lemma, including the infinitely near points

Fix $r=3$ or 4 distinct points $p_1,\ldots,p_r$ on the line $a=(z=0)\subset\mathbf P^2$, with a prescribed tangent direction at each point transverse to $a$. Blow up each point and then the prescribed point on its first exceptional curve. In the orthogonal total-transform basis write $H,E_i,E_i'$, with each exceptional basis vector of square $-1$. Put

$$
A=rH-\sum_{i=1}^r(E_i+E_i').
\tag{18.1}
$$

The system $|A|$ is base point free. To see every base point explicitly, use an affine coordinate $x$ on $a$, write $p_i=(t_i,0)$, and let the prescribed tangent be $x-t_i=\alpha_i z$. Choose a homogeneous degree-$r$ form $F_0$ whose restriction to $a$ is $\prod_i(x-t_i y)$. Its coefficient of $z$, a degree-$(r-1)$ binary form, can be chosen to have the $r$ values required to impose the prescribed tangents. These values determine it by interpolation. The system contains

$$
cF_0+z^2R_{r-2}(x,y,z).
\tag{18.2}
$$

Away from $a$, $z^r$ is an available nonvanishing section. On $a\setminus\{p_i\}$, $F_0\ne 0$. Near $p_i$, set $u=x-t_i-\alpha_i z$. The two kinds of sections have leading terms $u+O(2)$ and $z^2 R(p_i)+O(3)$, and $R(p_i)$ can be nonzero. Their common local ideal is the curvilinear length-two ideal $(u+O(2),z^2)$. After the first blowup, using $u=zt$, and dividing by the prescribed exceptional factor, the leading sections are $t+O(z)$ and $z R(p_i)+O(z^2)$. They have exactly one simple base point, the prescribed infinitely near point, and their differentials span its cotangent space. Blowing it up resolves the base ideal; the restrictions to the new exceptional $E_i'$ span $H^0(\mathbf P^1,\mathcal O(1))$. There are no other base points on either exceptional curve. This proves the claimed global generation, not merely an expected dimension count.

Also $A^2=r^2-2 r>0$, so $A$ is nef and big. The classes $3 A+H$ for $r=3$, and $3A$ for $r=4$, are therefore free and big. Their general members are smooth irreducible curves on the blown-up surface by Bertini. They avoid the strict transforms $E_i-E_i'$, on which they have degree zero, and meet each $E_i'$ transversely in three distinct points. The degree-three restriction is general: products of the full degree-one restrictions of $|A|$ span all binary cubics on $E_i'$; multiplying by a section of $H$ nonzero at $p_i$ does not change this in the degree-ten case.

Choose these three intersection points away from $E_i'\cap(E_i-E_i')$. Blowing down the second exceptional curve gives three smooth branches with distinct tangent directions at the first infinitely near point, none tangent to the old exceptional curve. Blowing down the first exceptional curve gives three smooth branches with one common tangent and distinct quadratic terms

$$
u=\lambda_jz^2+O(z^3),\qquad \lambda_1,\lambda_2,\lambda_3\ \text{distinct}.
$$

Thus the downstairs singularity is exactly the ordinary $[3,3]$ cluster intended here: multiplicity 3, followed by an ordinary triple point after one blowup, with no further infinitely near singularity. Smoothness of the strict transform and transversality to the exceptional curves exclude any additional singularities. This is stronger than merely obtaining a nonempty linear system with virtual assigned multiplicities.

#### The double-cover calculation and the exceptional contractions

For a smooth double cover $\pi:S\to Y$ with branch $2L$,

$$
\pi_*\mathcal O_S=\mathcal O_Y\oplus L^{-1},\qquad
K_S=\pi^*(K_Y+L),
$$

$$
\chi(\mathcal O_S)=2\chi(\mathcal O_Y)+\tfrac12L(L+K_Y),\qquad
K_S^2=2(K_Y+L)^2.
\tag{18.3}
$$

The decomposition and Hurwitz formula are the double-cover specialization of the abelian-cover framework described by Pardini (2010, PDF pages 4 and 10); the Euler-characteristic identity follows immediately by applying surface Riemann–Roch to $L^{-1}$.

At a branch point of multiplicity $m$, blow up and put $b=\lfloor m/2\rfloor$. The new half-branch class is $L'=f^*L-b E$. Direct substitution in (18.3) gives

$$
\Delta\chi=-\tfrac12b(b-1),\qquad
\Delta K^2=-2(b-1)^2.
\tag{18.4}
$$

An ordinary $[3,3]$ point has canonical-resolution branch multiplicities 3 and 4, not 3 and 3: the first odd exceptional curve belongs to the branch and passes through the second triple point. Thus $b=1,2$, and the resolution decreases $\chi$ by 1 and $K^2$ by 2. After the second blowup the first exceptional curve has square $-2$, belongs to the branch, and has smooth rational ramified preimage $R$ with $R^2=-1$. Contracting $R$ raises $K^2$ by 1. Therefore each such cluster contributes a net decrease of 1 to $K^2$ on the minimal model. Failing to make this final contraction gives the wrong numbers in all three examples.

The second exceptional curve is not a branch component and meets the branch in four distinct points. Its preimage is elliptic of square $-2$ before contracting $R$, and square $-1$ afterwards. This accounts for the elliptic negative curves in the complete inverse images of the line, while distinguishing them from the rational exceptional curves that were contracted.

#### Example 1: degree $2n$, one ordinary $(2n-6)$-fold point, and two $[3,3]$ points

Take distinct collinear $O,p_1,p_2$, blow up $O$ once and the two prescribed transverse length-two clusters at $p_1,p_2$. Set

$$
A=3H-E_O-\sum_{i=1}^2(E_i+E_i'),\qquad F=H-E_O.
$$

Here $A^2=4$ and $|F|$ is the pencil of lines through $O$. The interpolation proof above works with two tangent conditions and one ordinary point condition. On $a$, a cubic restricts to the product of the three point factors; the coefficient of $z$ has two prescribed values at $p_1,p_2$ and a free value at $O$. Consequently the two independent first-order directions at $O$ are both available, so a single blowup resolves its base point. The local argument at each $p_i$ is unchanged. Thus $A$ is free, as is $F$.

For $n\ge 5$, take a general member of

$$
D_n=3A+(2n-9)F
=2nH-(2n-6)E_O-3\sum_{i=1}^2(E_i+E_i').
\tag{18.5}
$$

This system is free and big. Its restriction to $E_O$ includes the full space of binary forms of degree $2n-6$, because the restrictions of both $A$ and $F$ span degree-one forms and their products span all the required degree. A general member meets $E_O$ transversely in $2n-6$ distinct points. It therefore has an ordinary $(2n-6)$-fold point downstairs, together with exactly the two ordinary $[3,3]$ points already analyzed and no other singularities. The strict transform of $a$ has intersection zero with $D_n$, so a general branch does not contain $a$.

For a smooth degree-$2n$ double plane, $\chi=1+\binom{n-1}{2}$ and $K^2=2(n-3)^2$. The ordinary point has $b=n-3$; the two clusters have the corrections just computed. Hence

$$
\chi=1+\binom{n-1}{2}-\binom{n-3}{2}-2=2n-6,
$$

$$
K_{\min}^2=2(n-3)^2-2(n-4)^2-2=4n-16.
$$

Canonical plane forms have degree $n-3$, vanish to order $n-4$ at $O$, and pass through $p_1,p_2$. Their assigned intersection with $a$ exceeds their degree, so they contain $a$. The residual forms have degree $n-4$ and multiplicity $n-5$ at $O$, and their vector-space dimension is $2n-7$. Therefore

$$
p_g=p_a=2n-7,\qquad q=0,\qquad p^{(1)}=4n-15.
$$

The strict line on the cluster surface has square $-2$; its connected double cover is branched only at the two first exceptional branch curves, so it is rational. Its square on the resolved cover is $-4$, which becomes $-2$ after the two rational contractions. Thus the fixed canonical curve $\theta$ has genus 0, square $-2$, and

$$
\theta(K-\theta)=2p_a(\theta)-2-2\theta^2=2.
$$

The residual moving class is the pullback of $(n-4)H-(n-5)E_O$, which is free and nef. It has intersection 2 with $\theta$. Consequently $K\theta=0$, and $K\Gamma\ge 0$ for every other irreducible curve $\Gamma$, since it is a sum of that nef moving class and the effective $\theta$. This verifies minimality rather than presuming that the contracted rational curves were the only possible $(-1)$-curves.

#### Example 2: degree 10 and three collinear $[3,3]$ points

Use $D=3 A+H$ with $r=3$. This is the promised free and big system giving an irreducible branch curve with precisely the required singularities. The constant count can also be completed. On this cluster surface $K_Y=-A$, so $D-K_Y=4 A+H$ is nef and big, and characteristic-zero vanishing gives $H^1(D)=0$. Since $D^2=46$ and $DK_Y=-12$, Riemann–Roch gives $h^0(D)=30$, hence projective dimension 29, as printed.

For the subsystem consisting of twice $a$ and an octic with three assigned tacnodes, the octic class is

$$
T=8H-2\sum(E_i+E_i')=2A+2H.
$$

Now $T-K_Y=3 A+2 H$ is nef and big, $T^2=40$, and $TK_Y=-12$, so $h^0(T)=27$, giving projective dimension 26. In subtracting $2a$ from the degree-ten cluster class one must unload the old exceptional curves: if $\widetilde a=H-\sum E_i$, then

$$
D-2\widetilde a=T+\sum(E_i-E_i').
$$

These fixed old exceptional components explain why twice $a$ plus a tacnodal octic satisfies the virtual $[3,3]$ conditions. Comparing 29 with 26 alone does not rule out all branches containing $a$ once; the free-system construction resolves that logical omission.

The cover has $\chi=7-3=4$, $K^2=8-3=5$, and canonical images equal to conics through the three collinear points, namely $a$ plus arbitrary lines. Thus $p_g=3$, $q=0$, and $p^{(1)}=6$. The line cover has four branch points—three from the first exceptional branch curves and one residual branch intersection—so its fixed component $\theta$ is elliptic. Its resolved square is $2(1-3)=-4$, increasing by 3 to $-1$. Therefore $\theta(K-\theta)=2$, exactly as stated.

The complete inverse image of $a$ consists of $\theta$ and three elliptic curves $E_i^*$, each of square $-1$, each meeting $\theta$ once, and pairwise disjoint. Hence

$$
p_a(\theta+\sum E_i^*)=4,\qquad
(\theta+\sum E_i^*)^2=-1-3+6=2.
$$

The residual canonical system is the pullback of lines, so it is nef; $K\theta=-1+2=1>0$, and $K$ is nonnegative on all other curves. This proves that the resulting surface is minimal.

#### Example 3: degree 12 and four collinear $[3,3]$ points

Take $D=3 A$ with $r=4$. The construction and local verification are identical. Canonical cubics through four collinear points contain $a$; the residual conics have vector-space dimension 6. The source does not state the surface invariants here, but the same verified computation gives

$$
\chi=11-4=7,\quad p_g=p_a=6,\quad q=0,\quad
K^2=18-4=14,\quad p^{(1)}=15.
\tag{18.6}
$$

The line cover is elliptic with four branch points. Its square is initially $2(1-4)=-6$, and becomes $-2$ after four contractions. The residual canonical conic system meets it in 4, giving $\theta(K-\theta)=4$. The complete preimage of $a$ is a star of five elliptic curves, with four edges; its arithmetic genus is 5 and its square is $-2-4+8=2$. Nefness and minimality follow as in Example 2, now with $K\theta=-2+4=2$.

#### The irregular example in the footnote is also verifiable

Choose a smooth conic $Q=0$ and a quartic $F=0$ transverse to it at eight distinct points, and take three distinct general parameters $\lambda_j$. The degree-twelve branch

$$
B=\prod_{j=1}^3(F-\lambda_jQ^2)=0
\tag{18.7}
$$

is the union of three smooth quartics in the pencil generated by $F$ and $Q^2$. They meet only at the eight base points, with common tangent and pairwise contact order 2. Thus the total branch has eight ordinary $[3,3]$ clusters and no further singularities. Canonical-resolution corrections give $\chi=11-8=3$ and $K^2=18-8=10$. Canonical cubics through the eight points contain $Q$, since $3\cdot 2<8$, and are $Q$ times arbitrary linear forms. Therefore $p_g=3$, $q=1$, $p_a=2$, and $p^{(1)}=11$, all as printed.

The conic cover branches at eight points and has genus 3. Its square changes from $-8$ on the resolved cover to 0 after the eight rational contractions. If $H$ is the moving pullback of a line, $K=\theta+H$, $\theta H=4$, $H^2=2$, and $K^2=10$, confirming both the fixed curve and minimality.

The irrational base can be seen without invoking an unidentified theorem. In the function field of the double plane $w^2=\prod(F-\lambda_j Q^2)$, put

$$
t=F/Q^2,\qquad u=w/Q^3.
$$

Then $u^2=\prod(t-\lambda_j)$ defines a genus-one double cover of $\mathbf P^1$, branched at the three $\lambda_j$ and infinity. The generic quartic $F-tQ^2$ is geometrically integral: general members of this pencil are smooth irreducible plane quartics. It remains geometrically integral after the extension of $\mathbf C(t)$ by $u^2=\prod(t-\lambda_j)$. Consequently the displayed elliptic function field is algebraically closed in the surface function field, so this is the full Stein-factor base, not merely a curve to which the surface maps. The text's reference to de Franchis is compatible with this calculation, but the exact historical theorem and original citation are not supplied in the excerpt and have not been independently identified here.

#### Canonical pencils and the outdated open-problem sentence

The main-text “not known whether examples exist” at p. 158 is superseded by its own footnote naming Pompilj's 1948 examples. Burniat (1952, p. 1030) explicitly describes those regular double planes with canonical genus-two pencils and expands the range of examples. The audit therefore does not report this as a present open problem or even an unresolved question in the final version of the book.

The numerical pencil bounds are correct on a minimal model. Write $K=Z+sk$, where $Z$ is fixed, $p_a(k)=\pi$, and $k^2=n\ge 0$. Intersecting with $K$ gives

$$
K^2=s(2\pi-2-n)+\sum m_i(2p_a(\theta_i)-2-\theta_i^2).
$$

The fixed contributions are $m_i K\theta_i\ge 0$. Moreover $k(K-k)=2\pi-2-2 n\ge 0$. Thus $n\le\pi-1$ and $\pi\le K^2+1=p^{(1)}$, so $n\le K^2$. The notation $p^{(2)}=p^{(1)}-1$ on this page denotes canonical degree; it must not be confused with the bigenus $P_2$.

### §19, pp. 158–162: canonical connectedness, bicanonical regularity, and the incorrect plurigenus formula

#### The exact modern theorem and a noncircular proof

Let $X$ be a smooth minimal complex surface of general type with $q=0$ and $p_g=p>0$. Then every effective canonical divisor is numerically 2-connected, every effective positive multiple of $K_X$ is numerically 1-connected, and

$$
H^1(mK_X)=H^2(mK_X)=0\qquad(m\ge2).
\tag{19.1}
$$

Therefore

$$
\boxed{P_m=h^0(mK_X)=1+p+\binom m2K_X^2
=1+p+\binom m2\bigl(p^{(1)}-1\bigr)\quad(m\ge2).}
\tag{19.2}
$$

The separate first plurigenus is $P_1=p$. In particular $P_2=p+p^{(1)}$, as the source correctly states.

Here is an intersection-theoretic proof of the connectedness step, which avoids first having to prove irreducibility of the bicanonical moving system. An effective nef divisor $D$ with $D^2>0$ is 1-connected; this is Reid's Lemma 3.11(i), also Mendes Lopes's Lemma 2.6. Suppose $D=A+B$ and $AB\le 0$. Put $x=DA\ge 0$, $y=DB\ge 0$, so $x+y=D^2>0$. If $x=0$, Hodge index implies $A^2<0$, because a nonzero effective $A$ cannot be numerically zero; but $A^2=x-AB\ge 0$, a contradiction. Similarly $y>0$. Hodge index now gives

$$
x^2\ge D^2A^2=(x+y)(x-AB)\ge(x+y)x,
$$

contradicting $xy>0$. Thus $AB>0$.

Apply this to $D=m K_X$. For a canonical split $K_X=A+B$, adjunction additionally gives

$$
AB=A(K_X-A)=2p_a(A)-2-2A^2,
$$

an even positive integer, hence at least 2. This argument is valid for nonreduced subcycles as well as reduced components. The 1-connectedness theorem from §17 gives $H^0(\mathcal O_{(m-1)K_X})=\mathbf C$, and $q=0$ then gives $H^1(m K_X)=0$. Finally $H^2(m K_X)=H^0((1-m)K_X)=0$, since a negative multiple of a nef big canonical class cannot be effective. Surface Riemann–Roch proves (19.2).

In the complex setting the more general plurigenus identity is $P_m=\chi(\mathcal O_X)+\binom m 2 K_X^2$ on every smooth minimal general-type surface for $m\ge 2$, without the restriction $q=0$: apply nef-and-big vanishing to $(m-1)K_X$. The elementary effective-divisor proof above uses $q=0$ and $p_g>0$; it must not be advertised as a proof of the unrestricted statement. Conversely, its cohomological connectedness part is algebraic and does not intrinsically require characteristic zero once those hypotheses hold. No blanket claim about arbitrary positive-characteristic surfaces is being made.

#### The p. 159 formula is a source error, not an OCR error

The printed general formula is

$$
P_i=p+\frac{i(i-1)}2p^{(1)}.
$$

The scan confirms every term. It is not corrected by reinterpreting $p^{(1)}$, because the immediately preceding bigenus formula and the chapter's canonical-degree convention fix $p^{(1)}=K_X^2+1$. For $m\ge 3$, the printed expression exceeds the correct answer by $\binom m 2-1$. For example, the verified degree-ten double plane of §18 has $p=3$, $K^2=5$, and $p^{(1)}=6$. Its $P_2=9$ agrees with the book, whereas $P_3=19$; the printed general formula gives 21. This independent internal example makes the error concrete.

#### Diagnosing the two bicanonical-pencil arguments

The source first treats $p\ge 2$. If a canonical moving pencil has general member $C$ of genus $\pi>1$, the adjunction restriction is complete because $q=0$, and the system $|K_X+C|$ has variable canonical intersections with $C$ of degree $2\pi-2>0$. This is the right geometric idea for ruling out composition of the bicanonical system with that pencil. The passage compresses the standard argument excluding every possible pencil; the independent proof of §20 below avoids this compression. The exclusion of an elliptic pencil is deferred in the source to later classification. On a minimal general-type model it follows immediately: an elliptic fiber $F$ has $F^2=K_XF=0$, incompatible with Hodge index and $K_X^2>0$.

For $p=1$, the assertion that the unique $K$ decomposes into a fixed part and $s$ half-fibers is not established. The next dimension estimate also uses the full-fiber genus for a half-fiber. If a resolved fiber is $F=2 A$, $F^2=0$, and $p_a(F)=\pi$, then

$$
A^2=0,\qquad K_XA=\pi-1,\qquad
p_a(A)=\frac{\pi+1}{2},
$$

which is not $\pi$. This arithmetic diagnosis does not, by itself, validate the earlier half-fiber decomposition. The general theorem is true, but this printed proof is incomplete.

The long footnote supplies a second approach. Its intersection identity

$$
2K_X^2=\sum m_i(2\rho_i-2-\nu_i)
+s(2\pi-2-n)
$$

is correct; nefness makes the fixed terms nonnegative. For a nonspecial complete pencil $C$, Riemann–Roch gives $p+n-\pi+1\le 1$, so $n\le\pi-p\le\pi-1$. The scan prints $n<\pi-1$, an unjustified strict inequality. Replacing it by $\le$ preserves the intended contradiction for $\pi>2$: one gets $s(\pi-1)\le 2 K_X^2$, hence $s\le K_X^2$, while $\dim|2 K_X|\ge p+K_X^2>s$.

The remaining genus-two case imports a double-plane normal form with specified elementary singularities. That classification is not established in these pages. More seriously, the existence of one doubled canonical member does not by itself show that the fixed plane part of the whole bicanonical system has even multiplicities: multiple-fiber and vertical contributions require separate control. The subsequent deduction $s=2 h$, $h\ge 1\Rightarrow p_g>1$, is conditional on that unproved bookkeeping. These are precise limits of the excerpt, not counterexamples to the bicanonical theorem.

#### Repairing the fixed-subcycle proof of connectedness

Given an irreducible general moving bicanonical member, any nonpositive split of $2 K=L+C$ has one side supported in the fixed part $L$. The descent of §17 permits a 1-connected such subcycle $D$. Let $\rho=p_a(D)\ge 0$, $\nu=D^2$. The displayed calculation is correct:

$$
D(2K-D)=4\rho-4-3\nu\le0,
\qquad \nu\ge\frac43(\rho-1).
\tag{19.3}
$$

The nonnegativity of $\rho$ follows from the source's valid induction using Franchetta's Theorem II; alternatively $h^0(\mathcal O_D)=1$ makes $\rho=h^1(\mathcal O_D)\ge 0$.

The two low-genus cases admit short rigorous replacements. If $\rho=0$, integrality gives $\nu\ge-1$, while nefness gives $0\le KD=-2-\nu$, hence $\nu\le-2$, contradiction. This avoids calling a reducible or nonreduced genus-zero cycle an irreducible exceptional curve. If $\rho=1$, nefness and (19.3) force $\nu=KD=0$; Hodge index excludes a nonzero effective cycle of square zero orthogonal to a nef big $K$. The source instead infers an elliptic pencil, but does not establish movement of $D$, so its inference needs this repair.

For $\rho>1$, (19.3) gives $\nu>\rho-1$. The source assigns speciality index $i(D)=p$. That equality is unnecessary and is not justified for a subcycle of the fixed divisor of $|2 K|$, especially with multiplicities. The always-valid injection $H^0(K-D)\hookrightarrow H^0(K)$ gives $i(D)\le p$. Hence

$$
\dim|D|\ge p+\nu-\rho+1-i(D)
\ge\nu-\rho+1>0.
$$

Replacing $D$ by a different linearly equivalent effective divisor inside a complete bicanonical member contradicts its being fixed. Thus this part of Enriques's approach can be repaired economically. The direct nef-and-big proof above is shorter and avoids relying on the preceding pencil argument.

#### Why purity and minimality are mathematically essential

Let $f:\widetilde X\to X$ blow up $t\ge 1$ points of a smooth minimal regular general-type surface. Then

$$
K_{\widetilde X}^2=K_X^2-t,\qquad
P_m(\widetilde X)=P_m(X),\qquad
\chi(\mathcal O_{\widetilde X})=\chi(\mathcal O_X).
$$

Pluricanonical forms acquire the prescribed exceptional factors, so the dimensions of their spaces remain birationally invariant. But the Riemann–Roch polynomial on the new surface decreases by $\binom m 2 t$. Since $H^2(m K_{\widetilde X})=0$ for $m\ge 2$, comparison gives the exact defect

$$
\boxed{h^1(mK_{\widetilde X})=\binom m2t\qquad(m\ge2).}
\tag{19.4}
$$

Thus even though the plurigenera are unchanged, the full canonical multiples on the blowup are superabundant. Statements about the pure system cannot be extended to arbitrary blowups by treating minimality as a cosmetic choice. Formula (19.4) is an original audit cross-check, with high confidence, derived directly from birational invariance and Riemann–Roch.

### §20, pp. 162–163: irreducibility and a complete nonreduced repair

The author explicitly limits the argument to a reduced canonical divisor. This limitation must be retained. Its first dimension calculation is sound whenever $K=K_1+K_2$, $K_1$ is integral, $K_2$ is connected, and $n=K_1 K_2\ge 2$:

$$
p_a(K)=\pi_1+\pi_2+n-1,\qquad
\dim|2K|-\dim|K+K_2|=\pi_1+n-1>0.
$$

Thus $K_1$ is not fixed. The restriction to $K_1$ has degree $2\pi_1-2+n\ge 2\pi_1$, so its completeness does imply base point freeness on this integral curve; completeness alone, without the degree bound, would not suffice.

Two combinatorial steps are not justified in the excerpt. First, it chooses an irreducible component of minimum boundary and says the residual remains connected. Theorem II in §17 minimizes over connected subcurves, which need not be irreducible. A general weighted graph can be 2-connected in the numerical edge-cut sense and still have its minimum-degree vertex be a cut vertex: take two copies of a complete four-vertex graph, all edge weights 2, joined to a new central vertex by one weight 2 edge to each copy. The center has degree 4, all other vertices have degree at least 6, and its removal disconnects the graph. **This is only a diagnostic of the general graph inference; it is not asserted to occur as an effective canonical divisor with nef big $K$, and no canonical counterexample is claimed.** Additional canonical intersection theory might rule out such a configuration, but that argument is absent here. A noncut component does exist by the reduced graph lemma, so minimum boundary is not needed for the first step.

Second, removing rational one-point “handles” from a general connected curve need not leave a 2-connected core: separating positive-genus subcurves are possible. The propagation of a fixed handle to a base point on the previously removed component also needs more geometric detail. Again these observations identify missing justification in the excerpt, not an established counterexample to the special canonical assertion. Mendes Lopes (1996) gives a later systematic treatment of adjoints and rational-chain obstructions; it is not necessary to reconstruct Enriques's peeling procedure to settle the theorem.

A complete modern proof covers nonreduced canonical divisors as well. Catanese, Franciosi, Hulek, and Reid (1999, Theorem 3.3, pp. 194–195) prove that the dualizing sheaf of a numerically 2-connected Gorenstein curve is globally generated unless the curve is $\mathbf P^1$. Their proof uses duality and factorization through a subcurve: a hypothetical base-point obstruction factors through a generically injective map on a subcurve $B$; for a proper subcurve, numerical 2-connectedness gives a degree gap at least 2, which cannot be consumed by a length-one base point. The remaining whole-curve case forces the exceptional rational curve. This is exactly the nonreduced case for which the classical argument lacks a proof.

Choose any effective $D\in|K_X|$. It is a Cartier divisor on a smooth surface, hence Gorenstein; the previous section proves it numerically 2-connected. Its arithmetic genus is $K_X^2+1\ge 2$, so the rational exception is impossible. Adjunction identifies

$$
\omega_D\simeq\mathcal O_D(2K_X).
$$

Moreover

$$
0\to\mathcal O_X(K_X)\to\mathcal O_X(2K_X)
\to\omega_D\to0
$$

is surjective on global sections because $H^1(K_X)=q=0$. Thus $|2 K_X|$ has no base point on $D$. Outside $D$, the square of the canonical section defining $D$ is nonzero, so it has no base point there either. This proves global generation, stronger than absence of fixed components. The same restriction argument appears at the beginning of §6 in Catanese et al. (1999, p. 206); their later embedding conclusions have stronger hypotheses, which are not being imported into this elementary base-point argument.

Finally $(2 K_X)^2>0$, so the associated morphism has two-dimensional image. Bertini gives a smooth general member, and numerical 1-connectedness makes it connected; a smooth connected curve is irreducible. Thus the general pure bicanonical member is irreducible under the hypotheses of §§19–20, without the source's reducedness restriction and without circularly assuming bicanonical irreducibility to prove canonical connectedness. This conclusion does not assert that the bicanonical map is an embedding or even birational.

### §21, pp. 163–165: reducible surfaces, arithmetic genus, and canonical square

#### The model must be specified before invariants are compared

The source discusses a projected surface with historical “normal singularities,” its limiting apparent double curve, and two components $F_1,F_2$ glued through a further curve $C$. The degree-$\delta$ common part of the projected double locus is not automatically the same as the intrinsic gluing/conductor curve. On an arbitrary reducible or nonnormal surface these data can carry multiplicities and embedded structure; numerical formulas cannot be inferred from the reduced supports alone.

A clean modern setting is a projective reduced surface $X_0=X_1\cup_CX_2$, with $X_i$ smooth and $C$ a smooth connected curve embedded as a Cartier divisor in both, locally a double normal crossing. Write $\pi=g(C)$, $n_i=C^2_{X_i}$, and $p_i=\chi(\mathcal O_{X_i})-1$. This is an intrinsic gluing statement. To identify these numbers with those of a smooth nearby fiber, additionally assume a proper flat family. To identify canonical squares, require a compatible relative Gorenstein structure, or more generally an integer $r>0$ for which $\omega_{\mathcal X/T}^{[r]}$ is invertible and restricts to $\omega_{X_t}^{[r]}$ on every fiber; flatness of the underlying schemes alone does not supply an arbitrary canonical-divisor comparison. The Stacks Project, Tag 0CBN, supplies the precise normal-crossing definition, and Tag 0B9T gives local constancy of Euler characteristic for proper flat families.

#### Arithmetic genus: the formula and the virtual-dimension argument

The exact sequence

$$
0\to\mathcal O_{X_0}\to
\mathcal O_{X_1}\oplus\mathcal O_{X_2}
\to\mathcal O_C\to0
\tag{21.1}
$$

gives

$$
\chi(\mathcal O_{X_0})=\chi(\mathcal O_{X_1})+
\chi(\mathcal O_{X_2})-\chi(\mathcal O_C).
$$

Substituting $\chi(\mathcal O_C)=1-\pi$ and $p_a=\chi-1$ yields exactly

$$
\boxed{p_a(X_0)=p_1+p_2+\pi.}
\tag{21.2}
$$

No regularity assumption on $X_i$ occurs. In particular $p_i$ cannot be replaced by $p_g(X_i)$ when the components are irregular. The same Euler-characteristic inclusion-exclusion principle extends to higher dimensions; for unions with more components, higher intersections contribute alternating terms, and the sign convention for arithmetic genus must be respected.

Enriques's virtual count is consistent with this intrinsic proof. Adjoint hypersurfaces of degree $m_1+m_2-4$ restrict to $K_{X_1}+C$, with virtual projective dimension $p_1+\pi-1$. The kernel containing $F_1$ consists of residual adjoints to $F_2$, with virtual projective dimension $p_2-1$. Adding image and kernel vector-space dimensions introduces the extra 1 for projective dimensions, giving $p-1=p_1+p_2+\pi-1$. At p. 165 the author explicitly acknowledges possible failure of actual restriction surjectivity and says that virtual dimensions, or high-degree adjoints, are intended. The Euler-characteristic formulation validates this distinction without presuming surjectivity. A general deformation claim would still need the flatness and conductor hypotheses just stated.

#### Canonical square and the linear-genus formula

For a double normal crossing, the dualizing sheaf restricts as

$$
\omega_{X_0}|_{X_i}\simeq\omega_{X_i}(C).
\tag{21.3}
$$

Locally this is the residue description on $xy=0$; the logarithmic poles on the two branches have opposite residues along the common curve. Equivalently it follows from Cartier-divisor adjunction, whose duality formulation is given in the Stacks Project, Tag 0B4A. The canonical square is therefore the sum of the two component squares:

$$
\begin{aligned}
K_{X_0}^2
&=(K_1+C)^2+(K_2+C)^2\\
&=K_1^2+K_2^2+2(K_1C+K_2C)+n_1+n_2\\
&=K_1^2+K_2^2+8\pi-8-n_1-n_2,
\end{aligned}
\tag{21.4}
$$

because $K_i C=2\pi-2-n_i$. Consequently, if $p_i^{(1)}=K_i^2+1$ refers to the actual component models being glued,

$$
\boxed{p^{(1)}(X_0)=p_1^{(1)}+p_2^{(1)}+
8\pi-n_1-n_2-9.}
\tag{21.5}
$$

The arithmetic checks in the text agree. On $X_i$,

$$
p_a(K_i+C)=p_i^{(1)}+3\pi-3-n_i.
$$

Adding these two genera and the common canonical degree $2\pi-2$, then subtracting 1, yields (21.5). If $\pi=0$, however, $2\pi-2=-2$ is not an actual count of points in a canonical group. That part of the geometric language must be read virtually, or replaced by the canonical-square computation, which remains valid. The scan's $m_1+m_2+ +4$ on p. 165 is a genuine source sign error; the adjoint order is $m_1+m_2-4$.

The phrase “linear genus” must not cause the actual $K_i^2+1$ in (21.5) to be replaced silently by a birationally invariant minimal-model value: blowing down curves in a component changes both its canonical class and the embedding/normal bundle of the gluing curve. Those adjustments have to be tracked explicitly. Likewise a normalization formula for an arbitrary nonnormal surface needs its complete conductor, not just the reduced intersection curve.

#### A smoothing constraint and an independent numerical test

If the total space of a semistable smoothing is smooth along $C$, then

$$
N_{C/X_1}\otimes N_{C/X_2}\simeq\mathcal O_C,
\qquad n_1+n_2=0.
\tag{21.6}
$$

Indeed $X_1+X_2$ is the principal central fiber, and restricting its line bundle to $C$ gives the tensor-product relation. This is an additional smooth-total-space condition, not a requirement for the abstract gluing identity (21.4), and not a consequence of flatness alone.

As an explicit audit test, degenerate a smooth quadric in $\mathbf P^3$ to two planes meeting in a line. Each plane has $p_i=0$, $K_i^2=9$, and $p_i^{(1)}=10$; the line has $\pi=0$ and $n_1=n_2=1$. Formula (21.2) gives 0, and (21.5) gives

$$
10+10-1-1-9=9,
$$

so $K^2=8$, the correct square for a smooth quadric. The family can be written $xy=tq(z,w)$, with a square-free binary quadratic $q$. Its total space is singular at the two zeros of $q$ on the common line, which explains why $n_1+n_2=2$ does not contradict (21.6). It is nevertheless a flat Gorenstein hypersurface family, so the invariant comparison is legitimate. This is an original consistency check, not an example from the source.

## Independent modern verification of the chapter’s main mechanisms

The following derivations organize the repairs by mathematical mechanism. They are supplied as modern arguments, not attributed to Enriques’s original proof. They also explain why several local mistakes do not invalidate the principal theorems.

### M1. Surface Riemann–Roch from curve Riemann–Roch

Let $X$ be smooth and projective and put

$$
Q(D)=\chi(\mathcal O_X(D))-\chi(\mathcal O_X)-\tfrac12D(D-K_X).
$$

For a smooth effective curve $C\subset X$, the exact sequence

$$
0\longrightarrow\mathcal O_X(D-C)\longrightarrow\mathcal O_X(D)
\longrightarrow\mathcal O_C(D)\longrightarrow0
$$

and curve Riemann–Roch give

$$
\chi(D)-\chi(D-C)=D\cdot C+1-g(C).
$$

Adjunction gives $2g(C)-2=C(C+K_X)$. Substituting shows $Q(D)=Q(D-C)$. Choose a very ample $H$ and a sufficiently large $m$. Choose smooth divisors $E\in|D+mH|$ and $T\in|mH|$. Applying the preceding equality to $E$, with the subtracted curve also $E$, gives $Q(E)=Q(0)=0$. Applying it again with the subtracted curve $T$ gives $Q(D)=Q(E-T)=Q(E)=0$. This proves

$$
\chi(D)=\chi(\mathcal O_X)+\tfrac12D(D-K_X)
$$

for every divisor class, including classes with no effective representative. Serre duality identifies $h^2(D)=h^0(K_X-D)$, giving the chapter’s exact dimension formula and inequality. This proof makes the extension to “virtual curves” automatic; it is not necessary to assume existence of an intermediate effective difference. For the standard theorem and duality statement, see Beauville (1996, I.11–I.12). Curve Riemann–Roch, including the Gorenstein case, is stated in The Stacks Project (n.d., Tag 0BS6).

### M2. Two deficiencies, two exact sequences

For a nonzero effective divisor $D$, the sequence

$$
0\to\mathcal O_X\to\mathcal O_X(D)\to\mathcal O_D(D)\to0
$$

identifies the characteristic deficiency with

$$
d(D)=\dim\ker\bigl[H^1(\mathcal O_X)\to H^1(\mathcal O_X(D))\bigr].
$$

Consequently $0\le d(D)\le q$, and $d(D)=q$ whenever $h^1(D)=0$. This conclusion needs no assumption that the restricted series is nonspecial. It also shows directly why every complete system on a regular surface has complete characteristic series, even when that system itself is superabundant.

For a smooth connected curve $C$, adjunction instead gives

$$
0\to\omega_X\to\omega_X(C)\to\omega_C\to0.
$$

The deficiency of the adjoint restriction is

$$
\delta(C)=\dim\ker[H^1(K_X)\to H^1(K_X+C)]\le q.
$$

The final trace map $H^1(\omega_C)\to H^2(\omega_X)$ is an isomorphism, so

$$
h^1(K_X+C)=q-\delta(C),\qquad
\dim|K_X+C|=p_g+g(C)-1-\delta(C).
$$

These are the exact counterparts of §§4–6. If $d'$ denotes the deficiency of the canonical restriction $H^0(K_X)\to H^0(C,K_X|_C)$, then curve and surface Riemann–Roch together yield

$$
d-d'=q-h^1\!\left(X,\mathcal O_X(C)\right).
$$

Thus the three quantities “characteristic deficiency,” “canonical restriction deficiency,” and “superabundance” cannot be identified indiscriminately. The special-scroll issue on p. 136 is an explicit instance of that distinction.

### M3. What “sufficiently large” actually supplies

Fix a divisor $A$ and an ample divisor $H$. For $D\in|mH|$,

$$
0\to\mathcal O_X(A-mH)\to\mathcal O_X(A)\to\mathcal O_D(A)\to0
$$

shows that restriction is surjective if $H^1(A-mH)=0$. By duality this group is dual to $H^1(K_X-A+mH)$, which vanishes for $m\gg0$ by Serre vanishing. The kernel $H^0(A-mH)$ also vanishes, since its intersection with $H$ would be negative. Hence restriction is an **isomorphism** for sufficiently large $m$, not merely surjective. This proves the “small system on a normally large curve” lemma with a definite, modern meaning for the positivity involved.

The same vanishing theorem proves eventual regularity of $mH+A$. It also gives independence of finitely many prescribed point or jet conditions after sufficiently ample twisting and the eventual Hilbert-polynomial postulation formulas. A primary foundation is Serre (1955); the precise ampleness/vanishing equivalence used here is The Stacks Project (n.d., Lemma 30.17.1, Tag 01XO). The argument does not apply unchanged to a nef divisor contracting a positive-genus curve. That limitation is mathematical, not merely terminological.

### M4. A point of multiplicity and the blowup bookkeeping

Let $f:Y\to X$ blow up a smooth point, with exceptional curve $E$. For $D_m=f^*D-mE$,

$$
D_m^2=D^2-m^2,\qquad K_Y=f^*K_X+E,
$$

and therefore

$$
p_a(D_m)=p_a(D)-\binom m2,\qquad
\chi(D_m)=\chi(D)-\binom{m+1}{2}.
$$

The number $\binom{m+1}{2}$ is the length of $\mathcal O_{X,p}/\mathfrak m_p^m$, hence the maximum number of independent linear conditions at that point. Equality is an independence assertion, not a formal consequence of assigning the multiplicity. Iterated blowups give the corresponding computation for infinitely near points, provided the actual cluster is used.

The surface invariants $p_g,q,p_a(X)$ are unchanged by point blowups. In contrast, $K_Y^2=K_X^2-1$. This explains why the chapter’s relative linear genus changes but its arithmetic genus does not. A $(−1)$-curve can be contracted to a smooth point; an exact modern existence statement is The Stacks Project (n.d., Lemma 54.16.8, Tag 0C2M).

### M5. Nonreduced connectedness and adjoint regularity

For any nonzero effective divisor $D$ on a surface with $q=0$,

$$
0\to\mathcal O_X(-D)\to\mathcal O_X\to\mathcal O_D\to0
$$

and duality imply the exact formula

$$
\boxed{h^1(K_X+D)=h^0(\mathcal O_D)-1.}
$$

For a reduced divisor, $h^0(\mathcal O_D)$ counts connected components. This immediately proves §16, including its superabundance $s-1$ for $s$ disconnected components. For a nonreduced divisor, nilpotent functions can increase $h^0$; support connectedness alone does not suffice.

Numerical 1-connectedness eliminates that difficulty. The exact theorem is Ramanujam (1972, Lemma 3; reprint p. 127). Start with an irreducible reduced component $D_1$ of $D$, so $h^0(\mathcal O_{D_1})=1$. If $D_1<D$, 1-connectedness gives $D_1(D-D_1)>0$; some irreducible component $\Gamma$ of the residual divisor satisfies $D_1\Gamma>0$. The sequence

$$
0\to\mathcal O_\Gamma(-D_1)\to\mathcal O_{D_1+\Gamma}
\to\mathcal O_{D_1}\to0
$$

has zero global sections in its first term because its degree is negative. Thus $h^0(\mathcal O_{D_1+\Gamma})=1$. Iterating, counting multiplicities, proves $h^0(\mathcal O_D)=1$. Crucially, the intermediate divisors need not themselves be numerically 1-connected. The induction uses 1-connectedness of the original $D$ to find each next component. This is precisely why it bypasses the compositional difficulty that Enriques explains in §17. See Reid (1996, Lemmas 3.10–3.11).

### M6. Minimality, canonical connectedness, and plurigenera

Let $X$ be a smooth minimal complex surface of general type. Its canonical divisor is nef and big. An effective nef divisor $D$ with $D^2>0$ is numerically 1-connected by the Hodge index theorem. If $D=K_X=A+B$, adjunction gives

$$
A\cdot B=A(K_X-A)=2p_a(A)-2-2A^2,
$$

an even integer. Since it is positive, it is at least two. This proves the numerical 2-connectedness of an effective canonical divisor without the circuit through a bicanonical pencil used in §§19–20.

When $q=0$ and $p_g>0$, apply M5 successively to effective multiples of $K_X$. It gives $h^1(mK_X)=0$ for $m\ge2$; also $h^2(mK_X)=h^0((1-m)K_X)=0$, because $K_X$ has positive intersection with an ample divisor. Riemann–Roch therefore gives

$$
\boxed{P_m=1+p_g+\binom m2K_X^2
=1+p+\binom m2\bigl(p^{(1)}-1\bigr),\qquad m\ge2.}
$$

For $m=2$, this is $P_2=p+p^{(1)}$, as printed. The general formula printed on p. 159 does not specialize correctly to the modern expression except at $m=2$; its missing terms are genuine printed errors.

More generally, over characteristic zero, nef-and-big vanishing gives $h^1(mK_X)=0$ also when $q>0$, and the formula becomes $P_m=\chi(\mathcal O_X)+\binom m2K_X^2$. With $p_g>0$, the effective-divisor version in Reid (1996, Theorem 3.13) suffices. The version for any nef line bundle of positive square is stated in Ramanujam (1974, supplement, reprint p. 160). This states the characteristic and minimality hypotheses explicitly.

To see why “pure” matters, blow up $t$ points of such a minimal surface. Plurigenera remain unchanged, while $K^2$ decreases by $t$. For $m\ge2$, Riemann–Roch on the blowup consequently gives

$$
h^1(mK_{\mathrm{blowup}})=\binom m2t.
$$

Thus pluricanonical regularity is not a birational invariant, although plurigenus is. Removing exceptional fixed contributions is essential to Enriques’s assertion.

### M7. Gluing two components and keeping virtual invariants separate

For a union $Y=X_1\cup_C X_2$ with scheme-theoretic intersection $C$, the exact sequence

$$
0\to\mathcal O_Y\to\mathcal O_{X_1}\oplus\mathcal O_{X_2}
\to\mathcal O_C\to0
$$

gives

$$
p_a(Y)=p_a(X_1)+p_a(X_2)+p_a(C).
$$

In the smooth double-curve, normal-crossing Gorenstein situation, dualizing adjunction gives $\omega_Y|_{X_j}=\omega_{X_j}(C)$. Write $n_j=C^2_{X_j}$ and $\pi=g(C)$. Then

$$
\begin{aligned}
K_Y^2
&=(K_{X_1}+C)^2+(K_{X_2}+C)^2\\
&=K_{X_1}^2+K_{X_2}^2+8\pi-8-n_1-n_2.
\end{aligned}
$$

Adding one and substituting $p_j^{(1)}=K_{X_j}^2+1$ produces exactly Enriques’s final formula. The computation is an Euler-characteristic and dualizing-class calculation. It does not assert that geometric genus is simply additive, or that every such glued surface is smoothable. Constancy in a degeneration requires the relevant flatness and relative dualizing hypotheses.

As an independent numerical check, a quadric can degenerate to two planes meeting in a line. Here $p_1=p_2=\pi=0$, $p_1^{(1)}=p_2^{(1)}=10$, and $n_1=n_2=1$. The formula gives $p^{(1)}=9$, hence $K^2=8$, the correct invariant of a smooth quadric. This also shows why one should not impose $n_1+n_2=0$ on every flat spatial degeneration: that extra condition belongs to a more restrictive semistable situation with smooth total space.

## Additional worked examples and proposed investigations

The following are this commentary’s own choices of examples and research exercises. No claim of historical novelty is made.

1. **A nonreduced divisor with connected support and extra global functions (high confidence; fully computed).** Blow up a K3 surface at one point and let $E\simeq\mathbb P^1$ be the exceptional curve. For $D=2E$, the support is connected, but $E\cdot E=-1$, so $D$ is not numerically 1-connected. The sequence $0\to\mathcal O_E(1)\to\mathcal O_{2E}\to\mathcal O_E\to0$ gives $h^0(\mathcal O_{2E})=3$. Since $K_X=E$ and $q=0$, $h^1(K_X+2E)=2$. This isolates the precise obstruction that support-only language would miss in §17.

2. **Orientation of a positive-square virtual class (high confidence; fully computed).** On $\mathbb P^2$, both $H$ and $-H$ have square one; only positive multiples of $H$ are effective. Their intersections with the ample $H$ distinguish them. The existence argument in §14 therefore requires an orientation such as $D\cdot H>0$, not merely $D^2>0$. Applied to $K_{\mathbb P^2}=-3H$, this also explains why a pluricanonical lower bound with its speciality term omitted cannot be universal.

3. **A controlled comparison of linear and numerical equivalence (high confidence).** On a product containing an elliptic factor, take a non-torsion degree-zero line bundle $M$ from that factor and an ample $A$. Then $A$ and $A\otimes M$ have the same intersection numbers, while no nonzero tensor power of their difference is trivial. They remain algebraically equivalent. This provides a concrete test of the regularity assumption in the torsion conclusion of §14.

4. **Extend the explicit double-plane reconstruction (proposed finite verification project; high confidence in the method).** The commentary supplies branch constructions and canonical-resolution calculations for the ordinary cluster configurations in §18. A useful extension is to vary the infinitely near tangent directions and record the boundary cases where two directions coalesce, a line becomes a branch component, or extra singularities appear. Record each branch multiplicity, discrepancy, and contraction rather than extrapolating the generic dimension count. This is a proposed computation about the boundary of the verified constructions, not an assertion of a new open problem.

5. **Track the passage from ordinary projection singularities to a smooth model (proposed documentation project; high confidence in its usefulness).** The conductor exact sequence in §3 already compares the ordinary-projection Hilbert polynomial with intrinsic Riemann–Roch and checks its boundary value at adjoint degree $n-4$. Extend that comparison to explicitly chosen nonordinary singularities. This would identify exactly which extra conductor or local geometric-genus terms enter outside the ordinary class assumed in §§2–5.

None of these proposed investigations is presented as a newly established open problem in algebraic geometry. The unresolved matters in this audit are identified in `method_and_limits.md`.

## References and source-verification notes

Entries follow author–date citation practice. A checked theorem, a bibliographic identification, and a historical attribution are different kinds of evidence; the notes below make that distinction explicit. The calculations labeled as this audit's reconstructions are proved in the commentary itself. They are not attributed to a reference merely because that reference supplies some of the underlying machinery. URLs identify the inspected edition or primary repository. Online sources were checked during this audit on November 7, 2026.

### Primary text

Enriques, F. (1949). *Le superficie algebriche*. Zanichelli. Chapter IV, §§1–21, printed pp. 101–165, with the final supplied scan position blank. The supplied scans are the authoritative text for the present audit. The publication information follows the task specification; the excerpt does not include the title page.

### Sources consulted for modern statements and proofs

Beauville, A. (1996). *Complex algebraic surfaces* (2nd ed.). Cambridge University Press. [Publisher's excerpt](https://assets.cambridge.org/97805214/95103/excerpt/9780521495103_excerpt.pdf). **Checked locations:** Theorems I.11–I.12 and Remarks I.13, giving duality, surface Riemann–Roch, and its dimension consequences. The excerpt, rather than an unavailable full edition, is the directly inspected source.

Catanese, F., Franciosi, M., Hulek, K., & Reid, M. (1999). Embeddings of curves and surfaces. *Nagoya Mathematical Journal, 154*, 185–220. [https://doi.org/10.1017/S0027763000025381](https://doi.org/10.1017/S0027763000025381). [Published article](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/7FEAD216C2F054EFB04C655991150B60/S0027763000025381a.pdf/embeddings_of_curves_and_surfaces.pdf). **Checked locations:** Theorem 3.3, pp. 194–195, and the bicanonical restriction argument in §6, p. 206. The [author preprint](https://people.dm.unipi.it/franciosi/lavori/embeddings.pdf) has different pagination: Theorem 3.3 on p. 9 and §6 on p. 19. The theorem used here concerns the dualizing sheaf of a numerically 2-connected Gorenstein curve; it is distinct from the 1-connected global-functions lemma.

Kleiman, S. L. (2005). *The Picard scheme* [Expanded lecture notes]. arXiv. [https://doi.org/10.48550/arXiv.math/0504020](https://doi.org/10.48550/arXiv.math/0504020). [Checked full text](https://arxiv.org/pdf/math/0504020). **Checked locations:** Theorem 5.11, p. 42; Corollary 5.14, p. 44; Definition 6.1 and Theorem 6.3, pp. 52–53; Theorem 6.16, p. 58; Corollary 6.17, p. 59. These establish the tangent-space interpretation, characteristic-zero smoothness, and the relationship between numerical triviality, the identity component, and torsion components. Pagination refers to this preprint, not to a guessed book edition.

Mendes Lopes, M. (1996). Adjoint systems on surfaces. *Bollettino dell'Unione Matematica Italiana, Serie 7, 10-A*, 169–179. [Author manuscript](https://www.math.tecnico.ulisboa.pt/~mmlopes/ADJOINT.pdf). **Checked locations:** Fact 1, manuscript p. 2; Lemma 2.6; and Theorem 4.1, characterizing smooth base points of the dualizing system on a 1-connected curve. Publication metadata was checked against the [author's publication list](https://fenix.tecnico.ulisboa.pt/homepage/ist14340/publications). The nine-page manuscript and journal version have different pagination.

Pardini, R. (2010, October 21–24). *Abelian covers and complete moduli of varieties of general type* [Lecture slides; joint work with V. Alexeev]. University of Georgia. [Primary slides](https://pagine.dm.unipi.it/pardini/files/UGA10B.pdf). **Checked locations:** PDF page 4, eigensheaf decomposition; PDF page 10, Hurwitz formula. The double-cover Euler-characteristic identity follows by Riemann–Roch. The branch interpolation, blowup corrections, and examples in §18 are direct calculations in this audit, not claims that these examples appear in the slides.

Ramanujam, C. P. (1972). Remarks on the Kodaira vanishing theorem. *Journal of the Indian Mathematical Society, 36*, 41–51. Reprinted in *C. P. Ramanujam—A tribute* (1978), pp. 123–134. Tata Institute of Fundamental Research/Springer. [Institutional reprint](https://mathweb.tifr.res.in/Documents/Publications/Studies/CP-Ramanujam-A-Tribute.pdf). **Checked location:** Lemma 3, reprint p. 127, on constant global functions of a numerically 1-connected divisor. The introduction explicitly discusses the missing lemma in Franchetta's approach. This is a verified subsequent repair, not an unsupported assertion of absolute historical priority. [Alternate institutional copy](https://www.math.tifr.res.in/~publ/studies/CP-Ramanujam-A-Tribute.pdf).

Ramanujam, C. P. (1974). Supplement to the article “Remarks on the Kodaira vanishing theorem.” *Journal of the Indian Mathematical Society, 38*, 121–124. Reprinted in *C. P. Ramanujam—A tribute* (1978), beginning at p. 159. Tata Institute of Fundamental Research/Springer. [Institutional reprint](https://mathweb.tifr.res.in/Documents/Publications/Studies/CP-Ramanujam-A-Tribute.pdf). **Checked location:** The theorem on reprint p. 160 gives the characteristic-zero vanishing for the inverse of a nef line bundle of positive square. This is the version used when an effective representative is not assumed.

Reid, M. (1996). *Chapters on algebraic surfaces* [Preprint]. arXiv. [Record](https://arxiv.org/abs/alg-geom/9602006); [full text](https://arxiv.org/pdf/alg-geom/9602006). **Checked locations:** Lemmas 3.10–3.11, pp. 72–73, and Theorem 3.13, p. 74. These supply the divisor exact sequence, numerical 1-connectedness, the constant-functions lemma, and the effective nef-and-big vanishing theorem. The effectivity and characteristic assumptions are retained when that particular theorem is invoked.

Serre, J.-P. (1955). Faisceaux algébriques cohérents. *Annals of Mathematics, 61*(2), 197–278. [https://doi.org/10.2307/1969915](https://doi.org/10.2307/1969915). [Institution-hosted original](https://www.college-de-france.fr/media/jean-pierre-serre/UPL5435398796951750634_Serre_FAC.pdf). The primary paper was consulted as the foundation for coherent sheaf cohomology and sufficiently ample twisting. For the exact ampleness/vanishing formulation used in the repairs, the directly verified Stacks lemma below provides a stable pinpoint reference.

The Stacks Project Authors. (n.d.). *The Stacks Project*. Retrieved November 7, 2026. The following individual statements were opened and checked:

| Tag and locator | Mathematical use | Link |
|---|---|---|
| 0BY6, “The genus of a curve” | Arithmetic-genus convention and connectedness qualifications | [0BY6](https://stacks.math.columbia.edu/tag/0BY6) |
| 0BS6, Lemma 53.5.2 | Riemann–Roch and duality for a Gorenstein curve | [0BS6](https://stacks.math.columbia.edu/tag/0BS6) |
| 01XO, Lemma 30.17.1 | Ampleness and eventual coherent-cohomology vanishing | [01XO](https://stacks.math.columbia.edu/tag/01XO) |
| 0C2M, Lemma 54.16.8 | Contraction of an exceptional curve of the first kind | [0C2M](https://stacks.math.columbia.edu/tag/0C2M) |
| 0B9T, Lemma 36.32.2 | Local constancy of Euler characteristic in a proper flat family | [0B9T](https://stacks.math.columbia.edu/tag/0B9T) |
| 0B4A, §48.14 | Dualizing adjunction for effective Cartier divisors | [0B4A](https://stacks.math.columbia.edu/tag/0B4A) |
| 0CBN, §41.21 | Normal-crossing local geometry | [0CBN](https://stacks.math.columbia.edu/tag/0CBN) |

Vakil, R. (2002). *Complex algebraic surfaces, Class 5* [Lecture notes]. Stanford University. [Author-hosted notes](https://math.stanford.edu/~vakil/02-245/sclass5A.pdf). **Checked location:** PDF page 1 explicitly states curve Riemann–Roch, Serre duality, and adjunction. The year is supplied by the course directory and the note's Wednesday, October 16 date.

Voight, J., & Zureick-Brown, D. (n.d.). *The canonical ring of a stacky curve* [Author manuscript with errata incorporated]. [Author-hosted manuscript](https://jvoight.github.io/articles/stacky-canonical-rings-final-fixederrata.pdf). **Checked location:** §2.4, Lemma 2.4.1, the basepoint-free pencil trick. The inspected online version is cited without assigning an unverified publication year or journal pagination.

### Historical corroboration and metadata verification

Burniat, P. (1952). Surfaces algébriques à système canonique pur dégénéré. *Bulletin de la Classe des sciences, Académie Royale de Belgique, 38*, 1030–1043. [https://doi.org/10.3406/barb.1952.69760](https://doi.org/10.3406/barb.1952.69760). [Primary article archive](https://www.persee.fr/doc/barb_0001-4141_1952_num_38_1_69760). The opening page, p. 1030, was read, including its discussion and citation of Pompilj's 1948 examples. The entire article was not audited. It corroborates the later examples, rather than supplying an uninspected proof for them.

Castelnuovo, G. (1893). Sui multipli di una serie lineare di gruppi di punti appartenente ad una curva algebrica. *Rendiconti del Circolo Matematico di Palermo, 7*. [https://doi.org/10.1007/BF03012436](https://doi.org/10.1007/BF03012436). [Article archive record](https://zenodo.org/records/1786689). Title, author, date, and DOI were verified; the archive's article-PDF retrieval was unsuccessful. The original argument was therefore not independently audited. Enriques supplies the additional *Memorie scelte* locator, p. 95, and later the item number VIII.

Castelnuovo, G. (1896). Alcuni risultati sui sistemi lineari di curve appartenenti ad una superficie algebrica. *Memorie della Società Italiana delle Scienze (detta dei XL), Serie 3, 10*, 82–123. [Academy-hosted original](https://media.accademiaxl.it/memorie/S3-VX-1896/Castelnuovo82-123.pdf). Title and bibliographic location were checked in the primary scan. The paper was not read end to end, and its exact original scope is not inferred from Enriques's retrospective summary.

Hartshorne, R. (1977). *Algebraic geometry* (Graduate Texts in Mathematics, Vol. 52). Springer. [https://doi.org/10.1007/978-1-4757-3849-0](https://doi.org/10.1007/978-1-4757-3849-0). Publisher metadata and the Chapters III–V locations were checked; the complete text was not retrieved. It is a general reference for the modern framework, not an invented pinpoint authority for a historical repair. The actual calculations are supplied here or anchored to the verified statements above.

Kodaira, K. (1952). On the theorem of Riemann-Roch for adjoint systems on Kählerian varieties. *Proceedings of the National Academy of Sciences, 38*(6), 522–527. [https://doi.org/10.1073/pnas.38.6.522](https://doi.org/10.1073/pnas.38.6.522). [Primary archive](https://pmc.ncbi.nlm.nih.gov/articles/PMC1063603/). Author, title, year, pages, and DOI were verified. The paper identifies a foundational modern vanishing source; the exact nef-and-big statements used in this commentary are instead located in the verified Ramanujam/Reid texts.

Segre, C. (1889). Recherches générales sur les courbes et les surfaces réglées algébriques (II partie, Surfaces réglées algébriques). *Mathematische Annalen, 34*, 1–25. [Institutional record](https://bdim.dma.unina.it/item?id=GM_Segre_1889_1); [institutional bibliography](https://www.corradosegre.unito.it/articoli.php). These records verify the date of the matching work cited on p. 136, where the source prints 1892. The original theorem text was not audited; the scroll counterexample in §12 is independently computed.

For the remaining historical references, the following register preserves what Enriques actually supplies. Franchetta's 1941 article and Pompilj's 1948 article were not independently read in full. Pompilj's citation is corroborated by Burniat as *Atti dell'Accademia Nazionale dei Lincei, Rendiconti*, Serie 8, volume 4, pp. 539–544. The Campedelli reference on p. 123 remains abbreviated; its exact intended notation and the full scope of the original 1936 construction are not certified. No unavailable historical paper is treated as if its proof had been inspected.

## Register of historical citations printed in the excerpt

The following register preserves the bibliographic information that Enriques actually gives, including abbreviated titles, cross-references, and dates. It is separate from the verified modern bibliography. Inclusion here means that the supplied scan/text cites the work; it does **not** mean that the original paper's full proof was independently inspected. Incomplete references remain incomplete rather than acquiring invented pagination. The p. 136 Segre date is retained in this record and corrected in §12 and the bibliography. Bracketed contextual attributions identify authors named in the adjacent main text; these brackets are editorial additions, not quoted words from the footnote. The register also includes the two indicated main-text attributions. The mathematical footnotes, including the long bicanonical-pencil alternative on pp. 159–160, are audited in the corresponding commentary and claim rows.

| Printed page | Original TeX line | Citation or cross-reference as supplied |
|---|---:|---|
| 101 | 13 | Cfr. p. es. Enriques-Chisini, Op. cit. Libro V, vol. III. |
| 102 | 39 | [Main-text attribution.] “formule di postulazione di Cayley (1870) e di Noether (1871).” No titles or publication details are supplied; this is not silently identified with the later Cayley deficiency article. |
| 103 | 68 | La dimostrazione che segue è di G. Castelnuovo, *Sui multipli di una serie lineare di gruppi di punti appartenente ad una curva algebrica.* Rend. Circolo Mat. di Palermo, t. VII, 1893. Riprodotto in “ Memorie Scelte „ pag. 95. |
| 107 | 160 | A priori si può supporre che la data superficie $F$ possegga una curva doppia irriducibile priva d’incroci: $\tau=0$ (Cfr. *Introduzione, ecc.*, § 5). Tuttavia può essere utile sviluppare le formule anche nel caso $\tau>0$. |
| 114 | 430 | Cfr. anche L. Campedelli, *Sulla postulazione di una curva $i$-pla.* (Rend. Circolo Matematico di Palermo, to. 55, 1931). |
| 115 | 464 | Cfr. G. Castelnuovo, *Alcuni risultati sui sistemi lineari di curve appartenenti ad una superficie algebrica.* Mem. Soc. It. delle scienze (detta dei XL), serie III, t. 10, 1896. Riportato nelle “Memorie scelte„ pag. 335. |
| 118 | 551 | [Context: Castelnuovo.] *Alcune proprietà fondamentali dei sistemi lineari di curve tracciati sopra una superficie algebrica.* Annali di Mat., serie II, t. 25 (1897). Cfr. *Memorie scelte.* XXIII. |
| 120 | 599 | Cfr. Castelnuovo, *Sui multipli di una serie lineare di gruppi di punti appartenente ad una curva algebrica.* Rendic. Circolo di Palermo, 1893. *Memorie scelte*, VIII. |
| 121 | 662 | [Context: A. Cayley; the continuation supplies 1871.] . *On the deficiency of certain surfaces.* Math. Annalen, Bd. III. |
| 122 | 671 | Cfr. G. Castelnuovo, *Osservazioni intorno alla geometria sopra una superficie.* Rend. Ist. Lombardo, 1891. Nota I. “ Memorie scelte „ n. XVII. |
| 123 | 700 | L. Campedelli, in Atti R. Accademia di Torino, 1936. |
| 136 | 1211 | C. Segre, *Courbes et surfaces réglées.* Math. Annalen, 1892. |
| 137 | 1223 | [Context: F. Enriques.] *Una proprietà delle serie continue di curve appartenenti ad una superficie algebrica regolare.* Rendic. Circolo Mat. Palermo, t. XIII, 1899. |
| 137 | 1228 | [Context: F. Severi.] *Osservazioni sui sistemi continui di curve appartenenti ad una superficie algebrica.* Atti R. Accad. Scienze di Torino, 1904. |
| 137 | 1234 | A. Cayley, *On the deficiency of certain Surfaces.* Math. Annalen, Bd. III (1871). |
| 138 | 1243 | [Context: Noether.] *Mathematische Annalen.* Bd. VIII (1875). |
| 139 | 1258 | E. Picard, *Sur quelques questions se rattachant à la connexion linéaire dans la théorie des fonctions algébriques de deux variables indépendantes.* v. Crelle, Bd. 129, 1905. Cfr. Picard et Simart, *Traité*, t. II, pag. 437. Una dimostrazione algebrico-geometrica (ed anche un’estensione delle condizioni di sussistenza) del teorema, è stata data dal Severi, nella Nota *Sulla regolarità del sistema aggiunto* (Lincei, 8 nov. 1908), fondandosi però sul teorema della completezza della serie caratteristica di un sistema continuo |
| 139 | 1260 | [Context: M. Noether; the body supplies 1886.] *Extension du théorème de Riemann-Roch aux surfaces algébriques.* Comptes Rendus de l’Académie des Sciences, Paris, t. 103. |
| 140 | 1282 | [Context: G. Castelnuovo; the body supplies 1896 and 1897.] *Alcuni risultati sui sistemi lineari di curve appartenenti ad una superficie algebrica.* Memorie della Società Italiana delle Scienze, detta dei XL (1896, vol. X). *Alcune proprietà fondamentali dei sistemi lineari di curve tracciati sopra una superficie algebrica.* Annali di Matematica, serie II, vol. XXV. Riprodotte in “ Memorie scelte „, XXII e XXIII. |
| 140 | 1286 | [Context: F. Severi.] *Sulla serie caratteristica di un sistema lineare di curve appartenente ad una superficie algebrica.* Rendiconti R. Accademia dei Lincei, serie V, vol. XII (1903). *Sul teorema di Riemann-Roch e sulle serie continue di curve appartenenti ad una superficie algebrica.* Atti Accademia delle Scienze di Torino, vol. XL (1905). |
| 141 | 1321 | Cfr. F. Enriques, *Sur l’extension du théorème de Riemann-Roch aux systèmes linéaires de courbes appartenant à une surface algébrique.* Bull. des Sciences Mathématiques, 1940 (Cfr. in particolare il n. 5). |
| 142 | 1334 | [Context: Enriques's Ricerche of 1893, named immediately before the marker.] L. c., IV, 4. |
| 142 | 1334 | Castelnuovo-Enriques, *Sopra alcune questioni fondamentali nella teoria delle superficie algebriche.* Annali di Mat., t. VI, serie III, n. 4. |
| 142 | 1351 | [Context: Castelnuovo.] *Sul genere lineare di una superficie ecc.* Rend. R. Acc. dei Lincei, 1897; riprodotta in « Memorie scelte », XXIV. |
| 142 | 1351 | [Context: Castelnuovo–Enriques.] *Sopra alcune questioni fondamentali della teoria delle superficie.* Ann. di Matematica, 1900. |
| 146 | 1502 | Cfr. F. Severi, Math. Annalen, 62 (1906), pag. 194. A. Todd, Proc. of the Cambridge Phil. Soc. 23 marzo, 1939. Per le relazioni con un teorema sulla base di W. V. D. Hodge, J. London Math. Soc. 12, 1937, cfr. B. Segre, Ann. di Mat., 1937 e J. Bronowski, J. London Math. Soc., 1938. |
| 146 | 1504 | [Context: Severi.] *Sulle curve algebriche virtuali appartenenti ad una superficie algebrica.* Rendic. Ist. Lombardo II, 38 (1905). |
| 147 | 1562 | Cfr. Enriques, Bull. de Sc. Math., l. c. 1940. |
| 150 | 1651 | Cfr. Enriques, *Ricerche ecc.*, 1893. |
| 153 | 1768 | [Context: A. Franchetta.] *Sulla caratterizzazione delle curve eccezionali riducibili di prima specie*, in Boll. dell’Unione Mat., Bologna, 1941. |
| 153 | 1776 | [Context: the preceding Franchetta 1941 item.] l. c. |
| 157 | 1924 | [Mathematical footnote.] M. De Franchis: “un teorema generale sui piani doppi irregolari.” No title, date, or publication is supplied. The attribution concerns the irregular double plane with $p_a=2$, $p_g=3$, and $p^{(1)}=11$. |
| 158 | 1937 | Esempi effettivi sono stati costruiti recentemente da G. Pompilj: *Alcuni esempi di superficie algebriche a sistema canonico puro degenere*, Rend. Acc. Lincei, s. 8, v. IV, 1948. |
| 164 | 2205 | Cfr. Enriques-Chisini, Op. cit. |
| 164 | 2213 | In generale, per le varietà di qualunque dimensione: cfr. F. Severi, *Fondamenti per la geometria sulle varietà algebriche.* Rendic. Circolo Mat. di Palermo, 1909. |
