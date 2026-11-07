# Mathematical commentary and audit

Federigo Enriques, *Le superficie algebriche* (1949): front matter and printed pages 1–100

The supplied scan is the textual authority; the supplied LaTeX is a working transcription. Page references below are printed page numbers; physical PDF page numbers are fifteen greater for pages 1–100. The scope ends with Chapter III, §13. Later chapters are dependencies, not material contained in the packet. The companion registers separate source assertions from textual discrepancies, including mistaken suggestions already marked as errors in the transcription.

The labels “proved,” “sketched,” “stated without proof,” and “assumed from earlier work” describe what Enriques does **at the cited place**. A true proposition may have an incomplete local argument. A modern proof does not automatically document who historically repaired a particular passage. Audit-only auxiliary claims are expressly identified in the register; their proof-status labels refer to the modern proof supplied here. Reconstructions are labeled accordingly. Definitions, formulas, exercises, and subsidiary assertions are indexed separately in the claims register.


## Reading guide

The chapter sections follow the printed order. The claim register supplies the granular inventory; the correction register supplies the original TeX line locators and scan decisions. Each chapter ends with annotated references that distinguish inspected mathematics from bibliographic or historical reports.

- [Modern framework and conventions](#0-modern-framework-and-conventions)
- [Front matter](#front-matter)
- [Introduzione](#introduzione)
- [Chapter I: Linear systems of curves](#chapter-i-linear-systems-of-curves)
- [Chapter II: Covariant systems and invariants](#chapter-ii-covariant-systems-and-invariants)
- [Chapter III: Adjoint surfaces](#chapter-iii-adjoint-surfaces)

## 0. Modern framework and conventions

### 0.1 Models and notation

Unless a singular local model is explicitly under discussion, \(X\) is a smooth connected projective surface over \(\mathbb C\). The surface \(F\subset\mathbb P^3\) may be singular; \(\mu:X\to F\) denotes a chosen resolution. Normalization is finite and birational; resolution need not be finite. The word *normale* in the Introduzione describes ordinary projected singularities, not integral closedness: a surface with a double curve is usually nonnormal.

Characteristic zero matters to generic smoothness, separability of incidence maps, Picard smoothness, and Kodaira vanishing. The resolution theorem for excellent surfaces is broader, but that does not extend all the other arguments to positive characteristic (The Stacks Project Authors, n.d., Theorem 54.14.5, Tag 0BGP; Liedtke, 2008, Introduction).

| Classical term | Modern interpretation |
|---|---|
| \(\infty^r\) | Projective parameter dimension \(r\), from \(r+1\) independent sections. |
| Complete system \(\lvert D\rvert\) | \(\mathbb P H^0(X,\mathcal O_X(D))\); empty if \(h^0(D)=0\). |
| Equivalent, often \(\equiv\) | Linear equivalence \(D\sim E\), stronger than numerical equivalence. |
| Continuous system | An algebraic family; its members need not be linearly equivalent. |
| Degree of a system | Usually moving self-intersection after assigned base multiplicities are removed, not the degree of the curve in its ambient space. |
| Virtual curve | A divisor class that need not have an effective representative. |
| Virtual genus | \(p_a(D)=1+(D^2+K_XD)/2\); arithmetic genus, not necessarily normalization genus. |
| Characteristic series | Restrictions of the system to a member, contained in \(\lvert\mathcal O_D(D)\rvert\), possibly incomplete. |
| Fundamental curve | A curve contracted by the map of the specified system. |
| Exceptional curve of first kind | A smooth rational \((-1)\)-curve, or an explicitly specified total exceptional divisor on a succession of blowups. |
| Pure canonical system | Canonical system of the nonruled smooth minimal model, pulled back when appropriate; one does not simply discard all fixed components. |
| Surface genus \(p\) | Ordinarily \(p_g=h^0(\omega_X)\); the numerical surface genus is \(p_a(X)=\chi(\mathcal O_X)-1=p_g-q\). |
| Bigenus \(P\); plurigenus \(P_i\) | \(P_2=h^0(2K_X)\); \(P_m=h^0(mK_X)\). |
| Linear genus \(p^{(1)}\) | On the pure/minimal model, \(p_a(K_X)=K_X^2+1\); the model convention is essential. |

### 0.2 Adjunction and genus

For an effective Cartier divisor \(D\) on \(X\), adjunction states

\[
\omega_D=(\omega_X\otimes\mathcal O_X(D))|_D,\qquad
2p_a(D)-2=D(D+K_X).
\tag{0.1}
\]

For smooth \(D\), the first identity follows by taking determinants in

\[
0\to\mathcal O_D(-D)\to\Omega_X^1|_D\to\Omega_D^1\to0.
\]

For singular or nonreduced \(D\), apply duality to its length-one locally free resolution; \(\omega_D\) is the dualizing sheaf, not the ordinary cotangent bundle. Bilinearity then gives

\[
p_a(A+B)=p_a(A)+p_a(B)+AB-1,\qquad
p_a(mD)=1+\frac{m^2D^2+mK_XD}{2}.
\tag{0.2}
\]

For arbitrary divisor classes the right side defines virtual genus. For a reduced integral curve, comparison with its normalization shows \(p_a(D)-g(\widetilde D)=\sum\delta_p\); a reducible curve requires the component correction. An ordinary plane \(r\)-fold point has \(\delta=r(r-1)/2\). This prevents confusion between a rational singular plane curve and a divisor of arithmetic genus zero. Standard locators are Hartshorne (1977, II, Proposition 8.20; V, Proposition 1.5), and Brosnan (n.d., §3.1, Proposition 3.1).

### 0.3 Riemann–Roch and irregularity

Set \(q=h^1(\mathcal O_X)\), \(p_g=h^0(\omega_X)\). Surface Riemann–Roch and Serre duality give

\[
\chi(\mathcal O_X(D))=1-q+p_g+\frac{D(D-K_X)}2,
\]
\[
h^0(D)-h^1(D)+h^0(K_X-D)
=1-q+p_g+\frac{D(D-K_X)}2.
\tag{0.3}
\]

Consequently a count of coefficients minus nominal conditions does not prove completeness unless the evaluation map or the relevant cohomology is controlled.

Here is a proof of Riemann–Roch relative to curve Riemann–Roch and adjunction. For a smooth effective divisor \(A\), the restriction sequence gives

\[
\chi(D)-\chi(D-A)=\chi(\mathcal O_A(D))
=DA+1-g(A)=DA-\frac{A(A+K_X)}2.
\]

This equals the difference between the two quadratic Riemann–Roch expressions. Choose \(A\) sufficiently positive that both \(A\) and \(D+A\) have smooth effective representatives. Apply the formula first to \(D+A\), relative to zero, and then subtract \(A\). This proves (0.3) for arbitrary \(D\), without assuming \(h^1(D)=0\). See Hartshorne (1977, V, Theorem 1.6) and Brosnan (n.d., §3.2, Theorem 3.4). Enriques's dedicated Riemann–Roch chapter begins on page 101; this is a modern bridge for the present excerpt.

For smooth \(C\), the sequence

\[
0\to\mathcal O_X\to\mathcal O_X(C)\to N_{C/X}\to0
\tag{0.4}
\]

locates the failure of completeness of the characteristic series. The image of global sections has dimension \(h^0(C)-1\), and its cokernel is
\(\ker[H^1(\mathcal O_X)\to H^1(\mathcal O_X(C))]\).
The ambient \(H^0(N_{C/X})\) is the Hilbert-scheme tangent space. This explains the role of irregularity without assuming every completeness statement for arbitrary continuous systems.

### 0.4 Blowups and birational invariants

For the blowup \(\pi:Y\to X\) of a smooth point, exceptional curve \(E\), and divisor \(D\) with assigned multiplicity \(m\),

\[
E\simeq\mathbb P^1,\quad E^2=-1,\quad
K_Y=\pi^*K_X+E,\quad
\widetilde D=\pi^*D-mE,
\]
\[
\widetilde D^2=D^2-m^2,\qquad
p_a(\widetilde D)=p_a(D)-\frac{m(m-1)}2.
\tag{0.5}
\]

Indeed \(x=u,y=uv\) gives \(dx\wedge dy=u\,du\wedge dv\), proving the canonical coefficient. The other formulas follow from \(\pi^*D\,E=0\) and adjunction. On iterated blowups distinguish total transforms \(E_i^*\), with matrix \((E_i^*E_j^*)=-\delta_{ij}\), from irreducible strict transforms, whose intersection matrix changes under infinitely near blowups.

For \(m\ge0\), \(\pi_*\mathcal O_Y(mE)=\mathcal O_X\): a rational function with possible poles only over one smooth point extends across that codimension-two point. Projection formula proves invariance of \(P_m\). Moreover \(R^1\pi_*\mathcal O_Y=0\), so \(q,p_g,\chi(\mathcal O)\) are invariant, whereas \(K_Y^2=K_X^2-1\). Factorization of birational maps of smooth projective surfaces into point blowups and blowdowns proves birational invariance in general. See Hartshorne (1977, V, §3), Brosnan (n.d., §4.2), and the contraction construction in The Stacks Project Authors (n.d., Lemma 54.16.8, Tag 0C2M).

## Front matter

### F.1 Editorial status (title; V–X)

The title page identifies Bologna, Nicola Zanichelli, 1949. Castelnuovo's foreword reports that Enriques had not completed the final revision, that Pompilj and Franchetta assisted, and that a short editorial intervention could not rework every difficult argument. The warning about continuous systems and completeness of characteristic series is specific; it is not evidence against an unrelated proof merely because it belongs to the Italian school.

Enriques describes the relation to his lectures with Campedelli, completion of the main exposition in April 1942, and limitations of the wartime bibliography. His preface is dated September 1945, and Castelnuovo's January 1949. These are source-witness statements, not an independently reconstructed biography.

The modern context for the warning is \(\operatorname{Pic}^0(X)\), smooth of dimension \(q\) over \(\mathbb C\). Transition functions \(1+\varepsilon a_{ij}\) identify its tangent space with \(H^1(\mathcal O_X)\). Smoothness follows from the characteristic-zero theorem on group schemes; positive-characteristic Picard schemes can be nonreduced (Liedtke, 2008, Introduction and §2). For sufficiently positive \(D\), sections of \(D\otimes\alpha\) form, locally over \(\operatorname{Pic}^0(X)\), a projective bundle. Its tangent calculation is (0.4). This supplies a favorable precise setting for complete characteristic systems; it is not a proof that every family or Hilbert component is smooth. Chapter IX is outside the packet.

### F.2 Contents (XI–XV)

The contents are a map of the book, not proofs of the later statements named there. They locate the Introduzione at 1, Chapter I at 15, Chapter II at 41, Chapter III at 67, and Chapter IV at 101. Printed pages 14 and 66 are blank. All contents pages were read. Numerical entries such as \(p^{(1)}=6,5\) enumerate two integers, not a decimal number. Minor doubtful punctuation is registered separately, distinguishing the presence of a visible mark from certainty about its typographical intention. The physical origin of every tiny dot cannot be settled from the scan.


## Introduzione

### Int.1 Singular points and infinitely near points (§1, pp. 1–2)

**Definitions and their scope.** An irreducible equation \(f(x,y,z)=0\) gives an affine surface; its homogenization gives the projective closure. Its degree is the number of intersections, with multiplicity, with a general line. At a point of multiplicity \(r\), a general line through the point contributes \(r\) local intersections and \(n-r\) residual intersections. The word “general” excludes a tangent direction and a line contained in the surface. The first nonzero homogeneous term of the local equation is the tangent cone. At a smooth point the gradient is nonzero; the implicit-function theorem gives an analytic local graph and its successive Taylor approximations. It does not give a rational parametrization of an open subset of the algebraic surface.

Enriques distinguishes an ordinary multiple curve, with generically distinct smooth local sheets and tangent planes, from an isolated ordinary multiple point. At the latter the projectivized tangent cone is a smooth plane curve in the ordinary case. A general tangent cone can instead be reducible or nonreduced. The cuspidal double curve and the uniplanar double point are examples in which the tangent-cone data degenerate. The definition of infinitely near points refers to points on successive blowups; an “infinitesimal curve” is properly interpreted on these successive models. The earlier Enriques–Chisini treatment is assumed, not reproduced.

**Qualification of the three-neighbor assertion.** Page 2 says that a uniplanar double point has three infinitely near double points in distinct directions. This is the *ordinary uniplanar* case, as Chapter III later makes explicit on pages 83–84; rank one of the quadratic tangent cone alone does not imply it. A direct check is useful. Write a local equation as

\[
z^2+g_3(x,y)+\text{terms of degree at least four}=0,
\]

where the binary cubic \(g_3\) has three distinct roots in \(\mathbb P^1\). In the blowup chart \(y=xt,\ z=xw\), the strict transform is

\[
w^2+xg_3(1,t)+\text{terms divisible by }x^2=0.
\]

Along the reduced exceptional line \(x=w=0\), singularities occur precisely at the roots of \(g_3\). At a simple root, the quadratic part is \(w^2+c\,x(t-t_0)+d x^2\), with \(c\ne0\), and is nondegenerate. Thus there are three ordinary nodes. Repeated roots or vanishing \(g_3\) change the configuration. This is a completed local calculation, not evidence that the later, explicitly ordinary, statement is false.

The tacnode is specified here by the singularities of general plane sections: two consecutive double points. A convenient generic local model is \(z^2+g_4(x,y)+\cdots=0\), with \(g_4\) having four distinct directions. A general plane section through the point has a plane tacnode. One should not identify every surface singularity with double tangent plane with this model, or import the plane-curve label \(A_3\) as a complete classification of the surface germ. The excerpt postpones the needed refinements to Chapter III.

### Int.2 Rational transformations, contractions, and branch separation (§2, pp. 2–5)

**Rational maps.** Enriques's expressions \(x'=\varphi_1/\varphi_0\), \(y'=\varphi_2/\varphi_0\), \(z'=\varphi_3/\varphi_0\) are homogeneous coordinates for a rational map after clearing denominators. Common fixed factors must first be removed. The base scheme, not just its set of points, determines the resolution of the map. His “involution \(I_n\)” means the degree-\(n\) grouping of points in the fibers of a generically finite correspondence; it does not necessarily mean an automorphism of order two. A birational correspondence of surfaces is an isomorphism of their function fields. It need not extend to a Cremona transformation of the ambient three-space.

The restriction of an ambient map to a surface is birational onto its image when its general fiber contains exactly one point of that surface. This is the content of the general-position discussion; it is not a theorem about *every* invariant hypersurface. The exceptional possibility of a surface meeting the generic fiber in several points is acknowledged in the text.

**What point expansion actually requires.** The blowup of a smooth point replaces it by \(\mathbb P(T_pX)\simeq\mathbb P^1\); a system with a prescribed base point can realize that blowup when it separates the needed tangent directions. For a complicated base ideal, several blowups or a normalized blowup may be needed. Conversely, a curve contracted to a point is not automatically an exceptional curve of the first kind: the image point may be singular. This distinction is developed in Chapter I.

For an ordinary \(r\)-fold curve, normalization separates its \(r\) local sheets at a general point. For an ordinary isolated multiple point, blowing it up produces its projectivized tangent cone as exceptional curve. These observations are correct local descriptions. They do not prove termination for arbitrary singularities. The phrase about reducing a neighborhood from order \(r\) to order \(r-1\) must not be converted into a universal assertion that the multiplicity drops by one at each blowup. For example, the strict transform of \(z^2+x^5+y^5=0\) still has multiplicity two in an appropriate chart after the first blowup. The existence of a terminating procedure is a separate theorem assumed in §3.

**The five-equations count on pp. 4–5.** The equations describing two points with the same image form an off-diagonal fiber-product problem. Six point coordinates minus the two surface equations and the three image-equality equations suggest a one-dimensional double locus. This is an expected-dimension calculation, not by itself a proof. The diagonal component must be removed, the equations must impose the claimed independent conditions, and tangential coincidences require separate analysis. A map that is an embedding has no off-diagonal double locus at all. For a general projection these missing assertions are supplied by generic-projection theory; for a special rational map they can fail.

The capital \(F\) in the phrase on p. 3 that describes the transformed surface as a transform of \(F\), where the initial surface is \(f\), is visible in the scan. It is a printed notation slip, not an OCR correction.

### Int.3 Smooth models, the graph construction, and embedding in \(\mathbb P^5\) (§3, pp. 5–6)

**Maps to higher-dimensional projective space.** A list of \(r+1\) homogeneous functions gives a rational map to \(\mathbb P^r\). The image may be described as a component of an intersection of equations. Enriques uses this freedom to separate singular branches while retaining birational equivalence. General projection of a smooth surface in sufficiently high projective space embeds it in \(\mathbb P^5\): the union of secant and tangent lines has dimension at most five, and a general projection center of dimension \(N-6\) in \(\mathbb P^N\) avoids it, since \(5+(N-6)<N\). Avoiding these length-two secants separates points and tangent vectors; properness then gives a closed immersion. Projecting further to \(\mathbb P^4\) generally produces only finitely many ordinary improper double points, with two distinct preimages and transverse tangent planes. The exceptional secant-defective situation, including the Veronese surface, must be allowed; “finitely many” includes zero.

**A genuine defect in the unqualified graph sentence.** Enriques describes placing the corresponding coordinates of two models in a common higher-dimensional space and says that only singularities common to the two models remain. Formation of a graph does not, by itself, justify this assertion. Here is an explicit counterexample, calculated for this audit. Consider the birational map between smooth affine planes

\[
(x,y)\dashrightarrow(u,v)=\left(\frac{x^2}{y},\frac{x^3}{y}\right),
\quad
(u,v)\dashrightarrow(x,y)=\left(\frac vu,\frac{v^2}{u^3}\right).
\]

Its graph closure is

\[
v=xu,\qquad uy=x^2.
\tag{Int.1}
\]

It is irreducible and contains the graph over \(xy\ne0\) as a dense open subset. Its remaining equation \(uy-x^2=0\) has all first partial derivatives zero at the origin. Thus the graph is a normal quadric-cone singularity although both target points lie on smooth surfaces. Normalizing the graph would not remove this singularity. The repair is to resolve the graph, obtaining a **common smooth resolution**, or to use an independently proved resolution theorem. This counterexample concerns the general sentence on p. 6; it does not claim to refute the theorem of resolution, or to audit Beppo Levi's original paper, which has not been read in full here.

**The asserted resolution theorem and a modern justification.** Every integral projective complex surface has a smooth projective surface birational to it; composing a projective embedding with the projection just discussed places a smooth model in \(\mathbb P^5\). The excerpt cites Levi, Chisini, Albanese, Walker, and Zariski and gives an explanatory sketch, not a terminating local resolution algorithm. A precise modern source is Lipman's surface-resolution theorem as presented in The Stacks Project Authors (n.d., Theorem 54.14.5, Tag 0BGP). Normalize first; finite-type schemes over \(\mathbb C\) satisfy the finiteness and excellence conditions there, and a normal surface has only finitely many singular closed points. The local normalized-blowup resolution theorem, combined with the gluing and descent statements cited in that proof, yields the resolution. Projective blowups and finite normalization preserve projectivity in this situation. This is a proof of the claimed consequence **relative to that explicitly identified local theorem**, not a new proof of the local termination theorem.

The scan reads *qualsiansi* in the displayed theorem on p. 6; the transcription's *qualsiasi* is a harmless lexical substitution. The distinction between a harmless word correction and a substantive mathematical defect is preserved in the register.

### Int.4 General projection and ordinary singularities (§4, pp. 6–8)

**Precise statement.** A sufficiently general projection of a smooth projective surface embedded in sufficiently high projective space to \(\mathbb P^3\) is birational onto a surface whose singularities are ordinary double-curve points, ordinary triple points, and pinch points. Locally in analytic coordinates these have equations

\[
xy=0,\qquad xyz=0,\qquad x^2-y^2z=0,
\tag{Int.2}
\]

respectively. The normalization is smooth. Enriques's statement on p. 8 includes discussion of pinch points; it would be inaccurate to criticize him for omitting them just because the preceding italicized sentence emphasizes the nodal double curve and triple points. Ordinary singularities and the projection theorem are stated in a modern form in Ciliberto and Flamini (2011, Definition 2.1 and Theorem 2.5), which also gives precise earlier references to Mezzetti and Portelli (1997).

**Audit of the dimension argument.** Secant lines to a surface are parametrized by at most four parameters; their incidence with a point on the line has dimension at most five. In \(\mathbb P^5\), a nondefective secant incidence has finite generic fibers. In \(\mathbb P^4\), the corresponding incidence through a general center has dimension one. The trisecant discussion and the exclusion of quadruple coincidences are used to obtain the claimed types of multiple points. These counts identify the expected strata, but do not establish transversality, smoothness of the double curve, or the absence of higher infinitesimal coincidences. Those are exactly the genericity conclusions supplied by the modern projection theorem. They should be stated as additional theorem input, rather than concealed inside a count of dimensions.

**Pinch-point calculation and the polar base point.** Normalize the third equation in (Int.2) by

\[
(u,v)\longmapsto(x,y,z)=(uv,u,v^2).
\]

The conductor on the normalization is \(u=0\). The polar derivatives pull back to

\[
f_x=2uv,\qquad f_y=-2uv^2,\qquad f_z=-u^2.
\]

After their common conductor factor \(u\) is removed, the residual system is generated by \(2v,-2v^2,-u\). It has one simple base point at \((0,0)\): its base ideal is \((u,v)\). This directly verifies the assertion on p. 8 about the residual polar system, and anticipates the same issue in Chapter II. It also makes clear why counting intersections only on the singular image loses information.

The source attributes the ordinary-model result to a theorem announced by Noether in 1888. That attribution is recorded as Enriques's statement. A complete independent priority study of the nineteenth-century papers is outside the evidence obtained for this audit.

Page 8 provisionally allows crossings of two branches of the double curve. Pages 10–11 subsequently analyze and exclude the associated tacnodal configurations for the general projections needed in §5. Such a crossing is therefore not to be inserted as an additional local equation in the modern list (Int.2).

### Int.5 Franchetta's irreducibility theorem (§5, pp. 8–13)

**Statement.** For a smooth, irreducible, nondegenerate surface \(X\subset\mathbb P^5\), the double curve of a general projection to \(\mathbb P^3\) is irreducible, except when \(X\) is the Veronese surface. The text also states the version for a surface in \(\mathbb P^4\) with only finitely many ordinary improper double points. The exceptional projection is the Steiner quartic with three double lines meeting at a triple point. Nondegeneracy and a genuinely general center are indispensable qualifications. Ciliberto and Flamini (2011, Theorems 2.4 and 2.6) give modern formulations and the Franchetta references. The dates in their bibliography and Enriques's footnote differ; this audit records the discrepancy without silently repairing the edition's date from a secondary citation.

The birational existence claim made at the start of §5 has no exception: an arbitrary surface can be resolved and reembedded by a sufficiently high power of an ample bundle, so that the resulting \(\mathbb P^5\) model is not the degree-four Veronese embedding. Its projected double curve is then irreducible. A special embedding being exceptional does not make its birational class exceptional.

#### Int.5.1 The tangent-plane lemma on p. 9

The lemma asserts that a three-dimensional family of pairs of tangent planes meeting along a line cannot have its joining secants fill \(\mathbb P^4\). The printed proof introduces a curve of contacts and then reasons with neighboring tangent planes and developable families. The common-three-space step has a standard infinitesimal explanation on the ordinary locus. Fix \(\pi=T_PX=\mathbb P(\Pi)\); for \(Q\notin\pi\), consider the map \(Q\mapsto\langle\pi,Q\rangle\) to \(\mathbb P(V/\Pi)\simeq\mathbb P^1\). The condition \(\dim\langle\pi,T_QX\rangle=3\) makes its derivative along the contact curve zero. In characteristic zero it is constant, proving the asserted fixed three-space on that locus. A contact component contained in \(\pi\), and the subsequent developable classification, need separate attention. Thus the usual infinitesimal step should be explained rather than itself declared false.

Here is a shorter modern proof, reconstructed for this audit. Let \(T\) be the family of pairs \((P,Q)\) at smooth points such that the tangent planes meet along a line. On the associated line incidence, consider

\[
e(P,Q,[a:b])=[aP+bQ].
\]

The image of the differential of \(e\) is contained in the linear span of the two projective tangent planes. Because these planes meet in a line, that span has projective dimension at most three. Thus the generic differential rank is at most three. In characteristic zero, the dimension of the image equals the generic rank, so the image cannot be all of \(\mathbb P^4\). This proof addresses the lemma directly and avoids the auxiliary classification of the developable possibilities. Distinct points and the appropriate dense smooth locus are understood; a limiting pair requires a jet calculation instead.

#### Int.5.2 Connectedness and the alternatives on pp. 9–10

Enriques first argues that the apparent double divisors, parametrized by projection centers, belong to one linear system because their parameter space is rational or unirational. A modern explanation is that the resulting map to \(\operatorname{Pic}^0(X)\) is constant: a rational map from a unirational variety to an abelian variety is constant (Milne, 2008, I, Propositions 3.9–3.10). One works on the smooth normalization and on an open set with a flat family; the divisor classes then extend appropriately. This is an imported theorem in the text, with its Enriques–Chisini citation, not something proved in the paragraph.

If the containing linear system has irreducible general member, connectedness of members follows after resolution of base points from the morphism/Stein-factorization argument, or from the standard connectedness theorem for the associated effective divisors. If it is everywhere reducible, the version of Bertini's second theorem used in Chapter I says that its movable part is composed with a pencil. The incidence of apparent double components through \(A,A_1,A_2\) is then used to contradict that pencil structure. The text gives a geometric sketch: a full proof must organize components in a family and distinguish a moving intersection at \(A\) from a fixed base locus. These are genuine family-theoretic details, not a counterexample to the conclusion.

The resulting possibilities for a connection of components are a crossing of two branches of the double curve, or a triple point. In the first case with distinct preimages, their tangent planes lie in the same three-space, and the preceding lemma rules out the required dominance of centers. This implication is correct once the incidence dimensions are justified.

#### Int.5.3 Infinitely near branches on pp. 10–11

The remaining crossing case has infinitely near preimages and forces abnormal tangent contact. The text argues through hyperplane sections with two consecutive double points, then separates the possibilities of a triple point plus a simple infinitely near point and a quadruple point. The passage from the center/contact incidence to an assertion about osculating behavior at general points is a **sketch**: general and exceptional osculating spaces must be distinguished.

The final curve-theoretic implication itself is standard in characteristic zero. If a space curve's osculating plane has contact at least four at a general point, a local homogeneous lift satisfies \(q'''\in\langle q,q',q''\rangle\). The derivative of its osculating-plane map vanishes, so the plane is constant and the curve is planar; lower osculating rank already gives a line. The audit's qualification concerns the preceding inference that the general sections have this property, not this valid final implication. Generic-projection theory excludes the abnormal centers in the situation required. The brevity of the source is not evidence that all its osculating deductions are false.

#### Int.5.4 Triple points and the omitted specialization justification (pp. 12–13)

The triple-point alternatives are (a) three distinct components of the double curve and (b) one simple component together with a component having two branches there. The corresponding apparent-double components upstairs are labeled \(K_i\). If one component remains fixed as the center moves along the trisecant, the argument places it in a plane and identifies it as a conic; identifying the resulting surface as a projection of the Veronese surface uses a classification theorem about the relevant secant-defective geometry. The mere existence of some two-parameter family of conics, without the nondegeneracy and incidence hypotheses, is not a sufficient general substitute for that theorem.

If \(K_1\) moves, the text says that for a suitable center it passes through \(P_1\). This is a substantive missing step: movement in a family alone does not imply incidence with an arbitrarily specified point. One must compactify the incidence family, prove the necessary nonconstant map has the required value, and control degenerations and inadmissible centers. No such proof is given here. The later tangency contradiction is reasonable conditional on that step. The same omission occurs in both alternatives. The bare \(C\) and the misplaced bars over \(K_1\) visible in the print are separately recorded as notation slips; they do not supply the missing specialization argument.

#### Int.5.5 A modern replacement for the principal \(\mathbb P^5\) conclusion

The following is a reconstruction using the secant-incidence/Bertini argument recorded by Lopez and Ran (2001, §1, pp. 1–2), who attribute the idea to Mumford and point to Moishezon (1977, p. 115). It repairs the conclusion needed for the ordinary birational model, without pretending to fill every sentence of the historical proof.

Blow up the diagonal in \(X\times X\). The line spanned by two points extends across the exceptional divisor as the tangent line in the indicated direction. The corresponding \(\mathbb P^1\)-bundle \(I\) is irreducible of dimension five, and has a proper secant-evaluation map \(e:I\to\mathbb P^5\). If \(X\) is not secant defective, \(e\) is dominant and generically finite. The inverse image of a general line \(\ell\subset\mathbb P^5\) is irreducible: apply the irreducibility form of Bertini successively to four general hyperplanes, noting that the image has dimension at least two until the final cut. Map this curve by the first endpoint \(I\to\operatorname{Bl}_{\Delta}(X\times X)\to X\), and then project that endpoint from \(\ell\) to \(\mathbb P^3\). Its image is the double curve, so it is irreducible. Projection of \(e(I)\cap\ell\) itself would be undefined; it is the endpoint map that is used. The classification of smooth nondegenerate secant-defective surfaces in \(\mathbb P^5\) leaves the Veronese surface. That classification is an explicit external input, not proved anew by the incidence argument.

For the Veronese exception one can check everything directly. Project the quadratic Veronese map by using the four forms

\[
[u:v:w]\longmapsto[uv:uw:vw:u^2+v^2+w^2]=[X:Y:Z:T].
\]

Its image satisfies

\[
X^2Y^2+Y^2Z^2+Z^2X^2-XYZT=0.
\tag{Int.3}
\]

Each of the three coordinate lines \(X=Y=0\), \(Y=Z=0\), and \(Z=X=0\) is a double line. They meet at \([0:0:0:1]\), the image of the three coordinate points of the source plane. Substitution verifies the quartic equation, and the leading local term at that image point is \(-XYZ\). Thus this calculation confirms the three double lines and the triple point asserted on p. 13.

### Int.6 Ideas and extensions arising from the audit

**Own calculation; high confidence.** Equation (Int.1) is a compact test case for the difference between a graph, a normalization, and a common resolution. It would be useful in an annotated edition beside p. 6 because all three distinctions are visible in one quadratic equation.

**Own reformulation; high confidence over \(\mathbb C\).** The differential proof of the tangent-plane lemma isolates the actual dimension obstruction. It also identifies exactly why the same one-line argument cannot simply be transferred to an inseparable setting: the generic differential rank need not equal the image dimension.

**Own worked example; high confidence.** The normalization and conductor calculation at a pinch point should accompany any account of polar curves and adjoints. It predicts the simple residual polar base point without relying on a drawing or on a convention about “virtual” intersections.

**A question for historical verification, not an open mathematical conjecture.** Which hypotheses are present in Franchetta's original incidence specialization, and exactly how do they enter the version for an arbitrary \(\mathbb P^4\) model with improper nodes? The modern principal theorem is verified, but the original paper was not obtained in full. This audit therefore does not attribute a particular corrected proof to Franchetta beyond the verified published references.


### References and verification: front matter and Introduzione

These references use author–date citation. “Verified” means that the indicated item, statement, or locator was inspected in the accessible source named here; it does not mean every page of every cited book was read. Historical works cited only by Enriques are distinguished from works consulted for a modern proof.

- Brosnan, P. (n.d.). *UMD 808J: Algebraic surfaces* [Course notes]. University of Maryland. [https://math.umd.edu/~pbrosnan/notes/Surfaces/index.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/index.html)  
  Directly consulted: §3.1, Proposition 3.1 (adjunction), [https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0016.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0016.html); §3.2, Theorem 3.4 (surface Riemann–Roch), [https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0017.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0017.html); §4.2 (blowups), [https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0028.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0028.html). These also verify several Hartshorne theorem locators.

- Ciliberto, C., & Flamini, F. (2011). On the branch curve of a general projection of a surface to a plane. *Transactions of the American Mathematical Society, 363*(7), 3457–3471. [https://doi.org/10.1090/S0002-9947-2011-05401-2](https://doi.org/10.1090/S0002-9947-2011-05401-2)  
  Author preprint inspected: [https://arxiv.org/pdf/0811.0467](https://arxiv.org/pdf/0811.0467) (version 2, 2010). Relevant locators: Definition 2.1, Remark 2.2, Theorems 2.4–2.6; Remark 3.3 on polars and pinch points. Journal metadata was cross-checked through the authors' institutional record, [https://art.torvergata.it/handle/2108/73827](https://art.torvergata.it/handle/2108/73827). The Franchetta, Mezzetti–Portelli, and Severi references below are verified as bibliography entries here, not as fully read original papers.

- Enriques, F. (1949). *Le superficie algebriche*. Nicola Zanichelli.  
  Primary source: the user-supplied facsimile, front matter and printed pp. 1–100. The supplied LaTeX is a secondary transcription of this witness.

- Hartshorne, R. (1977). *Algebraic geometry* (Graduate Texts in Mathematics, Vol. 52). Springer. [https://doi.org/10.1007/978-1-4757-3849-0](https://doi.org/10.1007/978-1-4757-3849-0)  
  Relevant standard locators: II, Proposition 8.20 (adjunction); V, §1 (intersection, genus, Riemann–Roch), especially Proposition 1.5 and Theorem 1.6; V, §3 (blowups and birational transformations). Publisher metadata was inspected. The full book was not downloaded; the explicitly quoted theorem numbers for adjunction, Riemann–Roch, and blowups were checked against Brosnan's notes rather than invented from a search snippet.

- Liedtke, C. (2008). *A note on non-reduced Picard schemes* [Preprint, version 2]. arXiv. [https://arxiv.org/pdf/0805.0848](https://arxiv.org/pdf/0805.0848)  
  Directly consulted: Introduction and §2, especially the tangent-space interpretation of \(H^1(\mathcal O_X)\). Published version: Liedtke, C. (2009). A note on non-reduced Picard schemes. *Journal of Pure and Applied Algebra, 213*(5), 737–741. [https://doi.org/10.1016/j.jpaa.2008.09.001](https://doi.org/10.1016/j.jpaa.2008.09.001). The commentary's 2008 citations identify the inspected preprint.

- Lipman, J. (1978). Desingularization of two-dimensional schemes. *Annals of Mathematics, 107*, 151–207. [https://doi.org/10.2307/1971141](https://doi.org/10.2307/1971141)  
  The theorem on p. 151 is the attribution given by Stacks Tag 0BGP. Bibliographic data were checked against the journal and the author's publication list, [https://www.math.purdue.edu/~jlipman/Vita/publications.html](https://www.math.purdue.edu/~jlipman/Vita/publications.html). The commentary follows the Stacks proof and its cited dependencies; it does not claim an independent line-by-line audit of Lipman's 57-page paper.

- Lopez, A., & Ran, Z. (2001). *On the irreducibility of secant cones, and an application to linear normality* [Preprint]. arXiv. [https://arxiv.org/pdf/math/0111147](https://arxiv.org/pdf/math/0111147)  
  Directly consulted: §1, pp. 1–2, especially the secant incidence over the normalized blowup of the diagonal, and the Bertini argument for a positive-dimensional center. The authors explicitly attribute the surface theorem to Franchetta and this argument to Mumford, as recorded by Moishezon. The citation deliberately identifies the accessible 2001 version; later publication metadata are not needed for the proof locator.

- Milne, J. S. (2008). *Abelian varieties* (Version 2.00) [Course notes]. [https://www.jmilne.org/math/CourseNotes/AV.pdf](https://www.jmilne.org/math/CourseNotes/AV.pdf)  
  Directly consulted: I, Propositions 3.9–3.10 (rational maps from rational curves and unirational varieties to abelian varieties are constant). This is the explicit source for the Picard-map argument.

- The Stacks Project Authors. (n.d.). *The Stacks Project*. Retrieved November 6, 2026, from [https://stacks.math.columbia.edu/](https://stacks.math.columbia.edu/)  
  Directly consulted: Theorem 54.14.5 (Lipman), Tag 0BGP, [https://stacks.math.columbia.edu/tag/0BGP](https://stacks.math.columbia.edu/tag/0BGP); §54.16, especially Lemma 54.16.8, Tag 0C2M, [https://stacks.math.columbia.edu/tag/0C2M](https://stacks.math.columbia.edu/tag/0C2M); §18.34 (finite-order differential operators and principal parts), Tag 09CQ, [https://stacks.math.columbia.edu/tag/09CQ](https://stacks.math.columbia.edu/tag/09CQ). Stable tags, rather than potentially changing section numbers alone, identify the statements.

##### Historical references retained with qualified verification

- Franchetta's paper is printed by Enriques on p. 8 as *Sulla curva doppia della proiezione di una superficie generale dello S₄ da un punto generico su uno S₃*, *Rendiconti della R. Accademia d'Italia* (1941), with a further 1947 Lincei reference. Ciliberto and Flamini's reference 13 gives the first as 1940, series VII, volume 2, pp. 282–288, and the second as volume 2 (1947), pp. 276–279. This discrepancy is registered; the original first paper was not obtained in full.

- Mezzetti, E., & Portelli, D. (1997). A tour through some classical theorems on algebraic surfaces. *Analele Ştiinţifice ale Universităţii Ovidius Constanţa, Seria Matematică, 5*(2), 51–78.  
  Metadata and the theorem references are confirmed through Ciliberto and Flamini; direct access through the institutional record was blocked. It is not presented as a paper read in full for this audit.

- Moishezon, B. (1977). *Complex surfaces and connected sums of complex projective planes* (Lecture Notes in Mathematics, Vol. 603). Springer.  
  Page 115 is the locator supplied by Lopez and Ran for Mumford's argument. The present reconstruction was checked against Lopez and Ran, not against the full Moishezon volume.

- Enriques's p. 6 references to Levi (1897), Chisini (1921), Albanese (1924), Walker (1935), and Zariski (1939, with a further “1941”) were read in the scan. No unverified article title, theorem number, or priority claim has been added to the abbreviated references. They document what Enriques assumes; the proof used here is identified separately.


## Chapter I: Linear systems of curves

### Scope, notation, and the standard of comparison

This commentary covers every numbered section (§§1–13), the displayed calculations, examples, footnotes, and historical notes in Chapter I. The scan, not the first-pass transcription, controls the text. All twenty-six scan pages were inspected. Exact line references and the twelve flagged readings are recorded separately in `transcription_corrections.csv`; the granular claim register is `claims.csv`.

The modern comparison is over **the complex numbers**. Write \(X\) for a smooth projective model of Enriques's surface \(F\), \(K_X\) for its canonical divisor, \(D\cdot E\) for intersection, and \(p_a(D)=1+(D^2+D\cdot K_X)/2\) for the arithmetic genus attached to a divisor class. In the chapter the letter \(K\) ordinarily denotes an **arbitrary curve or auxiliary linear system**, not the canonical divisor. Enriques's \(C\equiv K\) denotes **linear equivalence**. It must not be silently translated as numerical equivalence.

Three distinctions are indispensable throughout. First, the geometric genus of a normalization differs from arithmetic genus when a curve is singular. Second, the degree of a moving system after its assigned base points have been removed differs from the square of its divisor class on the original surface. Third, a total transform differs from a strict transform. Several apparent contradictions disappear once these conventions are kept explicit; other printed formulae really are wrong. Statements about an ordinary-singular projective model are interpreted on its smooth model unless the ambient projective singularities themselves are being discussed. The foundational references are Hartshorne (1977, Chapters II–III and V), the Stacks Project references listed below, and Kleiman's historically documented treatment of Bertini's two theorems (1998).

The labels **source proof**, **source sketch**, **source assertion**, and **modern reconstruction** describe what is actually supplied. A contemporary proof given here is not attributed to a named historical repairer unless documentary evidence establishes that attribution.

### §1. Linear pencils (pp. 15–17)

#### Functions, fibres, and the parameter

The starting datum is a nonconstant rational function \(t=\varphi/\psi\in\mathbf C(X)\). Its level curves \(C_t\), including the pole curve \(C_\infty\), form a pencil. In modern terms, choose a line bundle \(L\) and independent sections \(s_0,s_1\in H^0(X,L)\); their span \(V\) defines 
\[
\phi_V:X\dashrightarrow\mathbf P^1,\qquad x\longmapsto[s_0(x):s_1(x)].
\]
The members are the divisors of \(a s_0+b s_1\), indexed by \([a:b]\in\mathbf P^1\). A common divisorial factor is the fixed part; cancelling it leaves the same rational map. Enriques explicitly allows the fixed curve to remain in every member, which is why a pencil of divisors and its moving fibre pencil must be distinguished.

Replacing \(t\) by \(\tau=(\alpha t+\beta)/(\gamma t+\delta)\), with \(\alpha\delta-\beta\gamma\ne0\), changes only its projective coordinate. Three distinct members determine that coordinate after prescribing their three values. The source proves the relevant uniqueness by comparing functions with the same zero and pole curves. On a smooth complete integral surface, if \(\operatorname{div}(f)=\operatorname{div}(g)\), then \(f/g\) is a global invertible function and is constant. This is the precise hypothesis behind the elementary argument; on a nonnormal model it is safest to work on the smooth model.

The calculation on p. 16,
\[
\varphi\psi_1-\psi\varphi_1\equiv0\pmod F,
\]
expresses equality in the function field of an irreducible hypersurface. Thus the polynomial difference is a multiple of its defining equation. This is a **source proof**, not an unproved appeal to birational invariance. The punctuation at the preceding displayed equality is a printed semicolon, as the enlarged scan confirms.

#### Projective degree, ambient pencils, and base points

After homogenization, every divisor in the pencil has the same projective degree. An affine leading coefficient can vanish for a special parameter; the lost affine degree then lies at infinity. Enriques's explanation correctly prevents an apparent degree jump from being mistaken for a geometric one. The same pencil on \(F\) can be cut out by different ambient pencils because ambient equations are considered modulo the equation of \(F\), and because common components can be retained or cancelled.

The ambient base locus is \(\{\varphi=\psi=0\}\cap F\), but a point on a common fixed curve is not automatically a genuine indeterminacy of the reduced rational map. The essential base locus is the zero-dimensional locus remaining after removing the fixed divisor. At a smooth point \(P\), the common order of a general section is the multiplicity assigned to \(P\). Its tangent cone may contain fixed directions; those are detected as base points on the exceptional line after blowing up \(P\). In modern language, principalizing the two-generated base ideal resolves the rational map. This supplies standard background to the source rather than repairing a false statement.

### §2. Irrational pencils (pp. 17–18)

Enriques enlarges the word pencil to an algebraic one-parameter family of curves of **index one**: through a general point of the surface passes exactly one member. Modernly this is a rational map \(f:X\dashrightarrow B\) to a smooth projective curve, with the member parameter normalized and with connected general fibres when the pencil is treated as primitive. It is rational or linear when \(B\simeq\mathbf P^1\); it is irrational when \(g(B)>0\). The ruled-surface example has the ruling curve as parameter. The construction involving a cone in four-space likewise produces a fibration over its base curve. The genus \(p\) in this construction is the genus of the **parameter curve**; without further hypotheses it is not the genus of every fibre cut out by an additional hypersurface.

#### A pencil with a genuine smooth base point is rational

The source first varies tangent directions at a base point and applies Lüroth's theorem; it then repeats the argument after passing to higher-order neighbourhoods if the tangents are fixed. This is a **sketch**, with finite resolution of the base ideal understood.

Here is a modern proof. Resolve \(f\) by point blowups \(\pi:\widetilde X\to X\), obtaining \(\widetilde f:\widetilde X\to B\). A genuine base point forces at least one exceptional component \(E\simeq\mathbf P^1\) to dominate \(B\). Indeed, if the exceptional fibre were mapped to one point, the morphism would descend across that point of the normal surface \(X\); there would be no indeterminacy there. A nonconstant map \(\mathbf P^1\to B\) in characteristic zero forces \(g(B)=0\), by Riemann–Hurwitz (or the function-field form of Lüroth). Thus an irrational pencil has no genuine base point on a smooth model. The word **genuine** excludes an artificially retained fixed divisor. The source's passage to infinitely near points is exactly the geometric content of finding a dicritical exceptional component in this proof.

### §3. Linear systems (pp. 18–19)

A linear system is \(\mathbf P(V)\), for a nonzero finite-dimensional vector space \(V\subset H^0(X,L)\). Its dimension is \(r=\dim V-1\). If an ambient projective system has dimension \(R\), and its restriction kernel has projective dimension \(h\), the induced system has
\[
r=R-h-1.
\]
The empty projective kernel is assigned \(h=-1\). This convention is needed to cover injective restriction. Enriques's alternative description by independent rational functions \(1,t_1,\ldots,t_r\), given a common pole divisor, is the same construction. Linear independence is in the function field of \(F\), equivalently modulo its equation in a polynomial presentation.

Successive **general** points impose independent conditions until the system is exhausted; hence \(r\) general points determine one member. Generality is essential: a fixed base point imposes no new condition, and special configurations can give dependent conditions. The familiar hyperplane description proves the assertion directly: evaluation at a nonbase point is a nonzero linear functional on \(V\).

The source calls the system irreducible when a general member is integral. Resolve its assigned base cluster and remove its fixed part, obtaining a moving divisor \(D'\). Its effective degree is \(n=(D')^2\), the number of residual intersections of two general members. Its effective genus is the geometric genus of the general strict transform. On a smooth general member \(C\), the characteristic series is induced by
\[
V/\langle s_C\rangle\longrightarrow H^0(C,\mathcal O_C(D')).
\]
It has projective dimension \(r-1\) and degree \(n\). Since a nonzero line bundle of degree \(n\ge0\) on an integral smooth curve has \(h^0\le n+1\),
\[
r\le n+1.
\]
For the inequality, repeatedly subtract a point and use that the space of sections drops by at most one; a degree-zero bundle has at most one section. This is a modern completion of the source's brief appeal to curve theory. The source is working with the irreducible system here; the inequality is not a blanket statement about arbitrary composite systems.

A moving system of degree zero is a pencil or is composite with a pencil. After resolution, a base-point-free system whose image is two-dimensional has positive square, since two general hyperplanes on its image meet in a positive number of points. Thus square zero forces one-dimensional image. Stein factorization gives its pencil. This argument also explains why “dimension \(>1\)” does not itself imply two-dimensional image.

### §4. The characteristic property of linear systems (pp. 19–20)

#### The exact scope of the theorem

The source states that an algebraic system of dimension \(r\ge2\), with exactly one curve through \(r\) general points, is linear. It subsequently says that its curves may be assumed irreducible “for simplicity.” **That qualification is essential.** Without integral general members, the initially unrestricted wording is false.

For an explicit counterexample, let \(f:X\to B\) be a fibration with connected integral fibres over a curve \(B\) of positive genus. The family
\[
F_{b_1}+\cdots+F_{b_r},\qquad (b_1+\cdots+b_r)\in\operatorname{Sym}^r B,
\]
has dimension \(r\). Through \(r\) general points of \(X\), lying on distinct fibres, passes exactly one such member. Yet the divisor class varies with the Abel map of \(\operatorname{Sym}^rB\), so it is not a linear system. For example, take \(r=2\) and an elliptic base: its divisors have different classes as the sum of their two parameters varies. This is an **independent counterexample supplied here**, not a historical attribution.

#### What the source's proof accomplishes

For a two-dimensional system, Enriques groups the \(n\) common intersections of two members into points of a new surface, reconstructs an incidence plane, and uses pencils through two points to identify that surface birationally with a projective plane. He then extends from nets to higher-dimensional systems using overlapping nets. The geometric idea is sound under the irreducibility hypothesis, but the construction of the quotient surface and the necessary incidence and generic uniqueness assertions are not proved in the text. It is therefore a **source sketch**, not a scheme-theoretically complete construction.

#### Modern reconstruction of the result

A precise formulation takes an irreducible reduced parameter variety \(T\) of distinct effective divisors on a smooth projective complex surface, with integral general member and \(\dim T=r\ge2\), and assumes that the incidence variety of a member together with \(r\) points on it maps birationally to \(X^r\). Replace the family by its proper closure in the relevant Hilbert/Chow component, keeping the general locus of integral members.

1. Fix \(r-1\) general points on a general member. The remaining one-parameter family has index one on \(X\), by the uniqueness assumption. It has genuine base points at the fixed points. Its normalized parameter is therefore \(\mathbf P^1\), by §2.
2. The family defines a divisor-class map \(T\to\operatorname{Pic}(X)\). Every rational curve in \(T\) just obtained maps constantly to the abelian variety component of \(\operatorname{Pic}(X)\). At a general member, choose \(r\) general points so that the incidence projection is unramified. Leaving each point condition free in turn gives \(r\) tangent directions spanning the tangent space of \(T\). The differential of the class map vanishes on all of them. In characteristic zero the class map is constant.
3. Consequently the family lies in one complete system \(|L|\). A point condition is a hyperplane in \(|L|\). Intersecting the closure of \(T\) with \(r\) general such hyperplanes is proper and transverse and consists of one point. Its degree is therefore one. A projective variety of degree one in its linear span is a linear subspace. Thus \(T=\mathbf P^r\subset|L|\).

This proof makes explicit the flat-family, generic-smoothness, and Picard-variety background suppressed by the incidence sketch. It is an **authorial reconstruction of this audit**; no claim is made that a particular later mathematician repaired this exact passage. It also shows exactly where the counterexample fails: the residual one-parameter families have reducible members and retain a fixed sum of \(r-1\) fibres, so their fixed points are not genuine base points of the moving pencil.

### §5. Bertini's theorems (pp. 20–21)

The first statement is that a general member of a linear system has no variable singularity outside its base locus. On a singular projective surface, its own singular locus must also be excluded; on the smooth model this extra qualification disappears. Enriques's differentiation argument is a legitimate characteristic-zero sketch, but the characteristic and ambient smoothness hypotheses matter. It is not a valid positive-characteristic argument without separability assumptions.

For a modern proof, remove the base locus and consider the universal incidence variety
\[
\mathcal U=\{(x,[s]):s(x)=0\}\subset X\times\mathbf P(V).
\]
Over the open set where evaluation \(V\otimes\mathcal O_X\to L\) is surjective, this is a projective bundle and is smooth. Generic smoothness in characteristic zero applied to \(\mathcal U\to\mathbf P(V)\) makes a general member smooth there. This proves precisely the claimed exclusion of variable singularities. Kleiman (1998, Theorem 4.1) gives the classical statement and its historical development.

The second statement says that if a general member is reducible, then, after removing the fixed part, the system is composite with a pencil. The pencil may be irrational. The three alternatives listed on p. 21 are: a fixed component plus a variable integral component; a system composite with a pencil; or their combination. Modernly resolve the rational map of the system. If its image has dimension at least two, Bertini's irreducibility theorem makes a general hyperplane pullback integral. If its image is a curve, Stein factorization gives a morphism \(f:X'\to B\) with connected general fibre, and the system is pulled back from a linear series on \(B\); general divisors are sums of fibres. This is the precise meaning of being composite with a pencil. It requires removal of fixed components, and it says neither that \(B\) is rational nor that its complete series is a pencil of projective dimension one.

Here a genuinely documented historical gap can be named. Kleiman's examination of Bertini's second proof identifies the unproved algebraicity of the family of variable components and records that **van der Waerden (1937, p. 709)** supplied it; he also discusses Zariski's independent proof through pencils (1941). Zariski (1944) provided the intrinsic approach to the first theorem. These specific attributions are verified through Kleiman's primary mathematical-historical paper and its bibliography; they should not be generalized into an unsupported assertion that all the chapter's omissions were “repaired by Zariski.” See Kleiman (1998, Theorem 5.3 and the discussion following it), van der Waerden (1937), and Zariski (1941, 1944).

### §6. Projective images of linear systems (pp. 22–24)

#### Degree and generic multiplicity

The map of a system \(V=\langle\varphi_0,\ldots,\varphi_r\rangle\) is
\[
\phi_V:X\dashrightarrow\mathbf P^r,\qquad x\mapsto[\varphi_0(x):\cdots:\varphi_r(x)].
\]
After resolving the base cluster, let \(D'=\pi^*D-\sum m_iE_i^*\) be the base-point-free moving divisor, where \(E_i^*\) denotes total exceptional transform. If the map is generically finite of degree \(m\) onto a surface \(Y\), the projection formula gives
\[
(D')^2=m\deg Y.
\]
Thus the effective degree \(n\) of the system is \(m\) times the degree of its image. For a net the image is \(\mathbf P^2\), hence the generic degree is \(n\). A “simple” system means that the map is birational to its image. The source's suggestion that systems in sufficiently large dimension generally are simple is a generic geometric observation, not a theorem following just from \(r\ge3\): pull a very ample system back along any finite cover to obtain arbitrarily large nonsimple systems.

The discussion of a plane representing \(n\) sheets is the language of a generically finite map. Its branch curve is modernly obtained from the discriminant/ramification of the finite map on an appropriate open set or from the normalization. Simple branching is a further general-position property, not an automatic property of every net. Exceptional and nonfinite fibres need their own treatment.

#### A verified printed error on p. 22

For a surface of degree \(m\) in \(\mathbf P^3\), cones of degree \(q\) with a common vertex outside the surface are pullbacks of plane curves of degree \(q\) under projection from that vertex. Their divisor class is \(qH\), so their system degree is
\[
(qH)^2=mq^2.
\]
Enriques uses the letter \(n\) for this cone degree and the scan actually prints \(mn\). The mathematically correct expression is \(mn^2\). It is **a source misprint, not a transcription error**. The associated map factors through a degree-\(m\) projection and the degree-\(n^2\) Veronese image of the plane, which independently verifies the square.

#### Subsystems, projections, and infinitely near base points

A subsystem \(W\subset V\) corresponds to projection from the annihilator of \(W\). If its sections share a fixed divisor, that divisor lies in the intersection with the projection centre. Birational geometry of a pair consisting of a surface and a simple system is thus translated into projective geometry of its image. This is an equivalence of descriptions with the usual qualifications about resolving indeterminacy; the underlying smooth surface need not equal the generally singular image as a scheme.

Blow up a base point of multiplicity \(i\). If there is no further base point on its exceptional line \(E\), the transformed bundle restricts to \(\mathcal O_E(i)\). Consequently the image cycle of \(E\) has degree \(i\), counted with the degree of the map on \(E\). To say that the reduced image curve itself has degree \(i\), as in the source's generic picture, additionally requires that the restriction be birational. If a simple infinitely near base point occurs, a second blowup gives a first exceptional strict transform of system-degree \(i-1\) and a new exceptional line of degree one. When \(i=1\), the first component is contracted, has square \(-2\), and the appropriate normal image has an ordinary quadratic singularity; a neighbouring exceptional line remains visible. This is the ordinary two-step configuration illustrated by the quadric-cone example, not a classification of every possible image singularity without normality and generation hypotheses.

The note on p. 24 says that the exceptional curve has as many parts as the branches making up the singularity. Read literally as a statement about analytic branches of an arbitrary curve singularity and an arbitrary resolution, this is too strong: one smooth branch followed through several infinitely near base points already produces several exceptional components. The robust invariant is the **cluster of blowup centres and its proximity relations**, not merely the number of local irreducible branches. Enriques may be using “rami” in the broader historical sense of branches of the infinitely near configuration, or selecting a particular transformed model; the wording does not justify replacing the statement by a universal branch-count theorem. Section 12 gives the reliable intersection-theoretic account.

The footnote's Barber–Zariski reference is identifiable: **S. F. Barber and O. Zariski (1935), “Reducible exceptional curves of the first kind,” American Journal of Mathematics, 57(1), 119–141**, DOI 10.2307/2372025. The scan prints “E. Barber” and “Mathematik”; these are source bibliographic slips. The abbreviated Du Val citation can also be identified from the journal record: Du Val (1936), “Reducible exceptional curves,” American Journal of Mathematics, 58(2), 285–289, DOI 10.2307/2371038. Its metadata have been verified; no uninspected theorem number or full-text proof is claimed.

### §7. Equivalent curves and complete systems (pp. 24–26)

Two effective divisors are linearly equivalent when their difference is principal. Enriques expresses this by belonging to one pencil (or to the dimension-zero system when they coincide). Their reflexivity, symmetry, and transitivity follow respectively from the constant function, inversion, and multiplication of rational functions. These are **source proofs**. If \(C\) and \(K\) have common components, the statement that they are exactly the zero and pole curves of a function must be read after cancelling those common components: intrinsically it is always the identity \(\operatorname{div}(f)=C-K\).

The complete system is
\[
|D|=\mathbf P H^0(X,\mathcal O_X(D)).
\]
Every effective divisor linearly equivalent to \(D\) occurs as a section divisor, unique up to scalar. Finite-dimensionality on a proper variety supplies the existence of a unique maximal linear system. The source constructs this maximum geometrically by successively adjoining curves and bounding the dimension. That construction is an adequate classical sketch in its moving irreducible setting; coherent cohomology proves the statement uniformly, including systems of dimension zero and reducible systems.

**Completeness does not mean freedom from base points.** A complete system can have either fixed components or genuine base points. With assigned proper and infinitely near base points, the appropriate complete system is on the blown-up surface, for the divisor \(\pi^*D-\sum m_iE_i^*\). This is a relative completeness convention. It must not be conflated with the unrestricted complete system \(|D|\) on \(X\), in which some previously imposed point conditions may disappear. The text's qualifications “in general” and “virtually” need this interpretation.

The projective “normal” surface on pp. 25–26 is **linearly normal**: its hyperplane sections form a complete linear system. It is not the modern scheme-theoretic assertion of integrally closed local rings, nor does it assert normal generation of the homogeneous coordinate ring. For a fixed polarized smooth model \((X,L)\), completion replaces a chosen \(V\subset H^0(X,L)\) by the whole space. The final image is unique up to projective change of coordinates, regardless of the intermediate chain of projections. This is the exact modern meaning of the maximal projective model.

#### The quintic example

Blow up four points in general position in \(\mathbf P^2\), with exceptional divisors \(E_1,\ldots,E_4\). The cubic system has class
\[
D=3H-E_1-E_2-E_3-E_4=-K_X,
\]
so \(D^2=9-4=5\), \(p_a(D)=1\), and \(h^0(D)=10-4=6\). It embeds the degree-five del Pezzo surface in \(\mathbf P^5\). A four-dimensional vector subspace gives the source's three-dimensional system and its projection to \(\mathbf P^3\). Five-dimensional subspaces containing it form \(\mathbf P^1\), producing intermediate projections to \(\mathbf P^4\). Their general members are not all projectively equivalent: the automorphism group of the polarized degree-five del Pezzo surface is finite, so a one-dimensional family of subspaces cannot be one orbit. “Birationally distinct” in the source means inequivalent as the specified systems under a birational transformation preserving their polarizing data, not that the underlying rational surfaces have different birational types.

For a **general ordinary projection** \(\nu:X\to Y\subset\mathbf P^3\), the entire singularity description can be reconstructed. Let \(B\) be the reduced double curve downstairs and \(A\) its conductor divisor upstairs. A general plane section of \(Y\) is a quintic with normalization of genus one, so \(\deg B=6-1=5\). General projection has ordinary double, triple, and pinch points; its double curve is irreducible here because the degree-five del Pezzo is not the exceptional Veronese surface. These general-projection facts, with the local equations, are recorded in Friedman, Lehman, Leyenson, and Teicher (2012, §2). They are hypotheses/theorems about a general centre of projection, not properties of every four-dimensional subspace.

Finite duality gives the conductor adjunction identity
\[
K_X=\nu^*K_Y-A.
\]
Indeed, \(\operatorname{Hom}_{\mathcal O_Y}(\nu_*\mathcal O_X,\mathcal O_Y)\) is the conductor, and tensoring with the invertible dualizing sheaf of the hypersurface gives \(\nu_*\omega_X\). Since \(K_Y=(5-4)H\) and \(K_X=-H\), we obtain \(A\sim2H\), hence \(p_a(A)=6\). The conductor-square exact sequence
\[
0\to\mathcal O_Y\to\nu_*\mathcal O_X\oplus\mathcal O_B
 \to\nu_*\mathcal O_A\to0
\]
gives \(\chi(\mathcal O_Y)=\chi(\mathcal O_X)+\chi(\mathcal O_B)-\chi(\mathcal O_A)\). Here \(\chi(\mathcal O_Y)=5\), \(\chi(\mathcal O_X)=1\), and \(\chi(\mathcal O_A)=-5\), so \(p_a(B)=2\).

Write \(t\) for the number of ordinary triple points and \(b\) for the pinch points. The differential \(T_X\to\nu^*T_{\mathbf P^3}\) drops rank at the pinch points. Thom–Porteous, with its expected codimension two satisfied by a general projection, gives
\[
b=\int_X c_2(\nu^*T_{\mathbf P^3}-T_X)
 =6H^2-4Hc_1(T_X)+c_1(T_X)^2-c_2(X)
 =30-20+5-7=8.
\]
Here \(c_2(X)=3+4=7\) for the blowup of four points. This use of the degeneracy formula is covered by Fulton (1998, Chapter 14, §14.4).

At each ordinary triple point, \(B\) has a spatial ordinary triple with delta invariant two, while \(A\) has three ordinary nodes. The normalizations therefore have genera \(g(\widetilde B)=2-2t\) and \(g(\widetilde A)=6-3t\). The degree-two map \(\widetilde A\to\widetilde B\) branches precisely at the eight pinch points; locally the conductor map at a pinch is \(u\mapsto u^2\). Riemann–Hurwitz gives
\[
10-6t=2(2-4t)+8,
\]
so \(t=1\), \(g(\widetilde B)=0\), and \(g(\widetilde A)=3\). This also checks that the normalized conductor cover is connected: a disconnected degree-two cover of a connected smooth curve would be a union of two degree-one covers and could not have these branch points.

Finally \(\deg\mathcal O_B(2)=10>2p_a(B)-2=2\), so \(H^1(B,\mathcal O_B(2))=0\) and Riemann–Roch gives \(h^0(B,\mathcal O_B(2))=9\). Since quadrics in \(\mathbf P^3\) form a ten-dimensional vector space, \(B\) lies on a quadric. The quadric cannot be reducible: irreducibility would put \(B\) in one plane, but an integral plane quintic has arithmetic genus six, not two. It cannot be smooth at the triple point, because a multiplicity-three curve on a smooth surface has delta at least three, whereas this spatial triple has delta two. Hence the quadric is a cone with vertex at that point. The surface \(Y\) itself has an ordinary triple point there. This completes the source's projected-quintic example under its general-projection convention.

This is a **modern reconstruction supplied by the audit**, not an attribution of a historical repair. The local singularities are supplied by the generic-projection theorem, the conductor identities by finite duality and the conductor square, and the numerical conclusions by the calculations just displayed.

### §8. Sums, differences, and the residual theorem (pp. 26–30)

#### Divisor addition and two meanings of “sum system”

The equality \(\operatorname{div}(fg)=\operatorname{div}(f)+\operatorname{div}(g)\) proves that sums of equivalent curves are equivalent. Thus the complete sum is the unambiguously defined system \(|L\otimes M|\). For chosen systems \(V\subset H^0(L)\) and \(W\subset H^0(M)\), the **minimum sum system** is
\[
\mathbf P\operatorname{im}\bigl(V\otimes W\longrightarrow H^0(L\otimes M)\bigr).
\]
The union of divisors \(C+K\) is the image of the product \(\mathbf P(V)\times\mathbf P(W)\); its linear span is this minimum sum. It need not fill the complete sum. This distinction is fundamental, and no defect in the multiplication map should be called a failure of linear equivalence.

If the two positive-dimensional irreducible moving systems are not composite with the same pencil, their joint map has two-dimensional image. The sum has a two-dimensional image as well, and Bertini makes its general member integral. In particular, multiples \(|sD|\) are generically integral when \(|D|\) has two-dimensional image. The exception for a pencil requires precision: the minimum multiple of a pencil is always composite; the full complete multiple is composite in the fixed-free connected-fibre situation used later, but can be larger if additional sections exist. For example, after resolving a primitive base-point-free pencil \(f:X\to\mathbf P^1\), \(f_*\mathcal O_X=\mathcal O_{\mathbf P^1}\) implies \(H^0(X,f^*\mathcal O(s))=H^0(\mathbf P^1,\mathcal O(s))\), so the complete multiple is indeed a sum of fibres.

The sentence that assigned base points remain base points of the complete sum is valid for **completion relative to those assigned conditions**, equivalently on the chosen blowup. It is false if interpreted as unrestricted completion on the original surface. For instance, the pencil of lines through a point of \(\mathbf P^2\) has an assigned base point, while the unrestricted complete system \(|2H|\) has none. This is a convention-sensitive qualification, not a newly discovered failure of the tensor-product construction.

#### The quadric example and its missing low-degree exception

Planes through a smooth point \(O\) of a surface in \(\mathbf P^3\) give a net. Products of their equations span the six-dimensional vector space of quadrics singular at \(O\), hence a projective system of dimension five. Quadrics whose restrictions to the surface vanish to order at least two at \(O\) satisfy only three independent linear conditions: their value and their two tangential first derivatives vanish. They form a seven-dimensional vector space, hence a projective system of dimension six. This is the larger system of quadrics tangent to the surface at \(O\).

These dimension counts as systems on the surface require its degree to be **at least three**, so that restriction has no nonzero quadratic equation in its kernel. For a smooth quadric surface its own equation reduces the latter dimension to five; the asserted strict inclusion disappears. For a plane, even the initial restriction count is different. Enriques states the example for a surface of degree \(n\) without this low-degree exclusion. The missing hypothesis is a real qualification of the example, not an OCR problem.

#### Residuation: the intrinsic result and the projective supplement

Fix an effective divisor \(K\), with defining section \(s_K\). The members of a complete \(|C|\) containing \(K\) are exactly the section divisors obtained from
\[
H^0(X,\mathcal O_X(C-K))\xrightarrow{\cdot s_K}H^0(X,\mathcal O_X(C)).
\]
Removing \(K\) gives the complete residual system \(|C-K|\). If \(K'\sim K\), the line bundles \(\mathcal O(C-K')\) and \(\mathcal O(C-K)\) are isomorphic; the complete residual system is independent of the representative. This is the **intrinsic residual theorem**, proved in the source through rational functions. For an incomplete original system, only its corresponding subspace of residual sections is obtained; completeness cannot be omitted from the independence claim.

The source carefully distinguishes a second, projective assertion: adjoint hypersurfaces through the double curve of an ordinary-singular model cut a complete residual system. That theorem is **announced here and deferred** to the adjoint theory, not proved by the multiplication-of-functions argument. It must not be treated as a second consequence of linear equivalence alone.

The smooth-hypersurface special case follows immediately from
\[
0\longrightarrow\mathcal O_{\mathbf P^3}(q-n)\longrightarrow\mathcal O_{\mathbf P^3}(q)\longrightarrow\mathcal O_X(q)\longrightarrow0
\]
and \(H^1(\mathbf P^3,\mathcal O(k))=0\) for every integer \(k\). Thus all sections of \(\mathcal O_X(q)\) are induced by degree-\(q\) forms. This proves the asserted completeness in the nonsingular case; the ordinary-singular adjoint case requires the conductor/adjunction analysis appearing later in the book. Enriques's footnote to Noether is too abbreviated to verify an exact article here, so it is recorded as a source citation, not expanded by guesswork.

Subtraction can introduce reducibility, fixed components, and new base points. The example \(|K+2L|-|K|=|2L|\) gives a composite system when \(|L|\) is a fixed-free primitive pencil. A new residual base point becomes a fixed exceptional component after blowing it up; this is the correct geometric relationship, and it is stronger than merely observing an accidental intersection in one member.

#### Virtual curves and the historical note

A virtual curve is a formal divisor difference modulo linear equivalence. Equality
\[
C-K\sim L-M\quad\Longleftrightarrow\quad C+M\sim K+L
\]
is the group-completion relation. Adding a sufficiently positive ample divisor makes any such class effective by Serre vanishing and Riemann–Roch. Effectivity of the class itself is not required. These are integral divisor classes, not fractional divisors merely because the word “virtual” occurs.

The more restrictive notion mentioned on p. 29—a noneffective class with an effective multiple—is only a subclass. A nontrivial torsion line bundle gives a clean example: it has no nonzero section on a projective integral variety, whereas a suitable power is trivial and has the zero divisor as an effective representative. The canonical class of a classical complex Enriques surface is a familiar later instance. No assertion is made that every virtual class has an effective positive multiple.

The historical note assigns the early idea to Enriques's 1893 and 1896 works, terminology and further use to Severi, and an interpretation to Lefschetz. These attributions are reported as the source's history; the cited original papers were not all independently inspected. Modernly the first Chern class maps linear equivalence classes to cohomology, but it forgets \(\operatorname{Pic}^0\), and rational cohomology also forgets torsion. Thus the homological viewpoint does not identify all distinct virtual divisor classes.

### §9. Geometric representation of a sum (pp. 30–31)

The minimum sum map is the Segre composition of the two original maps, followed by passage to its linear span. The source's estimate \(R>r+s\) is a generic statement under independence of the two systems, not a universal numerical consequence of their dimensions: relations in the multiplication map and composition with a common pencil must be excluded.

There are two printed mistakes in the subsequent projective description. On p. 30 the scan reads \(S_r\) for the ambient space where \(S_R\) is required. In the next paragraph the curves \(C\) and \(K\) are interchanged: the \(S_{R-r-1}\) centre corresponds to a fixed \(K\), and the \(S_{R-s-1}\) centre to a fixed \(C\). The preceding paragraph already establishes the correct pairing. Both are source slips; changing only the first subscript leaves the second error in place.

A coordinate-free reconstruction makes the geometry transparent. Choose nonzero sections \(s_C\in V\), \(s_K\in W\), and form
\[
U=s_KV+s_CW\subset H^0(L\otimes M).
\]
If the two summands intersect only in the line spanned by \(s_Cs_K\), then \(\dim U=r+s+1\). The new image lies in \(\mathbf P^{r+s}\). Along \(K_0=(s_K=0)\), only \(s_CW\) remains, giving an image in \(\mathbf P^{s-1}\); along \(C_0\), only \(s_KV\) remains, giving an image in \(\mathbf P^{r-1}\). This proves the stated projection construction and fixes the swapped labels without conjecturing a different theorem.

For \(r=2,s=1\), the target is \(\mathbf P^3\). The fibre \(K_0\) goes to a point \(O\), and \(C_0\) to a line \(a\) not through \(O\). Suppose the joint map is birational, the pencil has no base points, the chosen intersections are simple, and set
\[
C^2=n,\qquad K^2=0,\qquad C\cdot K=i.
\]
The base locus of \(U\) is the \(i\) points of \(C_0\cap K_0\). Blowing these up gives the transforming divisor
\[
D=\pi^*(C+K)-\sum_{j=1}^{i}E_j,
\qquad D^2=n+2i-i=n+i.
\]
Consequently the image surface has degree \(n+i\). Its point \(O\) has multiplicity \(i\), and the line \(a\) has multiplicity \(n\) in the ordinary general configuration; the latter reflects the degree-\(n\) characteristic map of \(C_0\) to that line. The plane through \(O\) and \(a\) contains the remaining \(i\) exceptional lines. These multiplicity statements require the generic local model implicit in the source, while the divisor-square calculation is exact.

Finally, the products of equations of planes through \(O\) and planes through \(a\) span the quadrics through \(O\cup a\). This is the minimum sum system in the model. Birationality is not guaranteed by \(r=2,s=1\) alone: it is the asserted absence of a common nontrivial involution, translated as degree one for the joint function-field map, that provides it.

### §10. Virtual degree and genus (pp. 31–33)

For two divisor classes \(D,E\), bilinearity and adjunction give
\[
(D+E)^2=D^2+E^2+2D\cdot E,
\]
\[
p_a(D+E)=p_a(D)+p_a(E)+D\cdot E-1.
\]
For reduced curves meeting transversely these follow from counting intersections and from
\[
0\to\mathcal O_{D+E}\to\mathcal O_D\oplus\mathcal O_E\to\mathcal O_{D\cap E}\to0.
\]
The Euler-characteristic proof automatically includes scheme-theoretic intersection multiplicities. The surface Riemann–Roch formula extends the genus identity to arbitrary integral divisor classes, including virtual and nonreduced classes. The source proves the addition formula geometrically and then uses it to define the invariants of an isolated curve through an auxiliary moving system.

If \(C\) is isolated, choose sufficiently positive \(K\) so that \(K\) and \(C+K\) admit general integral members. Then
\[
C^2=(C+K)^2-K^2-2C\cdot K,
\]
\[
p_a(C)=p_a(C+K)-p_a(K)-C\cdot K+1.
\]
The text compares two auxiliaries and their sum to establish independence. Modern intersection theory and adjunction establish this directly. There is no gap merely because the source develops intersection theory using moving curves before naming its bilinear extension.

#### Blowups and the role of assigned singularities

For the blowup \(\pi:X'\to X\) of a smooth point where \(C\) has multiplicity \(m\),
\[
\pi^*C=C'+mE,\quad E^2=-1,\quad C'\cdot E=m,
\]
\[
(C')^2=C^2-m^2,\qquad p_a(C')=p_a(C)-\frac{m(m-1)}2,
\]
and \(K_{X'}=\pi^*K_X+E\). Total transform preserves the square and arithmetic-genus expression. The source's example \(C'+E\) concerns a simple point on \(C\); it must not be extrapolated with coefficient one to a multiple point. Likewise, the loss \(m(m-1)/2\) is the change under **one blowup**, not in general the whole delta invariant of an arbitrary singularity. For an ordinary \(m\)-fold point it is the full delta; for a cusp or more complicated singularity, further infinitely near multiplicities contribute.

If the system assigns multiplicity \(a\) at a point where a particular member actually has multiplicity \(m>a\), the transformed member includes \((m-a)E\) as an exceptional component relative to the assigned class. This explains why fixed exceptional components occur in special members and why assigned conditions must be maintained consistently through addition and subtraction.

The source's “virtual” degree and genus obtained by ignoring a designated base point are the invariants of the unsubtracted divisor class. They are not a statement that the actual ideal of a base point ceases to exist. For a singular integral curve, the geometric genus is \(p_a-\sum\delta_P\); all occurrences of genus must be checked against which singularities have already been assigned and removed. This qualification becomes crucial in §11.

### §11. Irreducible exceptional curves (pp. 33–37)

#### The two historical species and their examples

An irreducible curve of the first species is contracted to a smooth point by a birational transformation whose defining system has no base point on it. In modern language, near that curve the transformation is a morphism and is the inverse of a point blowup. A curve of the second species can be contracted by a birational map whose resolution requires base points on the curve. This is a distinction relative to the chosen model, not a birational invariant of the abstract normalization of the curve. Here “curve” means the entire exceptional divisor over the point. An individual strict component of a longer exceptional fibre can also map to a smooth point while having square less than −1; §12 expressly separates such components from whole exceptional curves.

The twenty-seven lines on a smooth cubic surface are first-species curves: each is smooth rational and has square \(-1\), by adjunction with \(K_X=-H\). There are no first-species curves on \(\mathbf P^2\), since every nonzero effective curve has positive self-intersection. A line can nevertheless be contracted by a quadratic plane transformation with two of its base points on that line. A smooth conic can be contracted by a cubic homaloidal system of type \((3;2,1,1,1,1)\), with the double point and four simple points on the conic: the intersection with its strict transform is \(6-(2+4)=0\). General-position conditions are needed for these homaloidal systems to define birational maps.

Resolving the base points of a second-species contraction makes it a morphism. Appropriate factorization then exhibits the relevant first-species curve on an intermediate smooth model. Enriques proposes adding an auxiliary system and comparing transforms; this is a geometric sketch of resolution and factorization. His count \(\sum i_j\) of intersections consumed by base points presumes that the curve is simple at those assigned centres. In general the local contribution is \(\sum i_jm_j\), where \(m_j\) is the multiplicity of the curve at the centre.

#### Numerical characterization and an important genus qualification

A first-species curve \(E\) satisfies
\[
E\simeq\mathbf P^1,\quad E^2=-1,\quad K_X\cdot E=-1,\quad p_a(E)=0.
\]
The source computes genus zero and degree \(-1\) by comparing a moving curve before and after adding the exceptional curve. The modern local computation of the exceptional divisor of \(\operatorname{Bl}_P X\) gives \(\mathcal O_E(E)=\mathcal O_{\mathbf P^1}(-1)\); adjunction then gives the same values.

The converse is Castelnuovo's contraction criterion: an **integral** divisor with arithmetic genus zero and square \(-1\) is a smooth rational \((-1)\)-curve and contracts to a smooth point. Arithmetic genus zero implies that its normalization has genus zero and every delta invariant is zero, so it is smooth. This implication does not extend to arbitrary reducible connected divisors solely from the two numerical equalities.

The text also assigns genus zero and nonnegative degree to second-species curves. It is essential to specify which genus and which assigned singularities are intended. A nodal plane cubic is rational and can be transformed to a conic by a quadratic map based at the node and two smooth points; its degree becomes \(2\cdot3-2-1-1=2\). The conic can then be contracted. But the original plane cubic has arithmetic genus one and square nine. Thus the source's statement is correct for geometric genus, or for the genus of a smooth representative after its singularities have been assigned and resolved; it is false if uncritically read as \(p_a=0\) for every original singular representative. This is a convention-sensitive limitation of the wording, not a claim that Enriques did not know the difference between geometric and virtual genus. The distinction was developed immediately beforehand.

#### A modern proof of the contraction criterion

Choose a sufficiently ample divisor \(H\) with \(H^1(X,\mathcal O_X(H))=0\), and let \(d=H\cdot E>0\). For \(1\le k\le d\), the exact sequence
\[
0\to\mathcal O_X(H+(k-1)E)\to\mathcal O_X(H+kE)\to\mathcal O_E(d-k)\to0
\]
has a quotient with no \(H^1\). Induction gives vanishing of the preceding \(H^1\), surjectivity of restriction, and the appropriate increase in sections. Set \(M=H+dE\). Then \(M\cdot E=0\), \(M|_E\simeq\mathcal O_E\), and a lifted nonzero constant section generates along \(E\). Away from \(E\), the sections inherited from \(H\) provide generation and separation. A suitable power of \(M\) therefore defines a morphism which contracts exactly \(E\) and is an isomorphism away from it; take its Stein factorization to obtain a normal target.

The remaining local assertion is that the contracted point is smooth and the morphism is its blowup. It follows from \(E\simeq\mathbf P^1\), \(\mathcal O_E(-E)\simeq\mathcal O_{\mathbf P^1}(1)\), and the vanishings \(H^1(\mathbf P^1,\mathcal O(m))=0\) for \(m\ge0\), which identify the completed local algebra with that of a regular two-dimensional point. The Stacks Project, Section 54.16, especially Lemmas 54.16.4 and 54.16.8 (Tags 0C2L and 0C2M), provides this exact contraction-and-blowup argument. This is the missing modern background to Enriques's proposed construction. In the chapter the decisive abundance and freedom of the constructed system are announced for later justification, so his argument is a **sketch/deferred proof**, not a completed proof on p. 36.

#### The numerical defect and ruledness

Write
\[
\Delta(D)=D^2-2p_a(D)+2=-K_X\cdot D.
\]
Adding a first-species curve increases this quantity by one, since \(-K_X\cdot E=1\). For disjoint such curves, adding \(\sum i_jE_j\) increases it by \(\sum i_j\). When the exceptional curves are infinitely near, the correct classes are their total transforms or the calculation must be made successively; the disjoint-formula proof cannot simply be applied to intersecting strict components.

The criterion announced on p. 37 is that a moving irreducible system with \(n>2\pi-2\), equivalently \(K_X\cdot D<0\), forces the surface to be birationally ruled. Over \(\mathbf C\), this follows from the classification of surfaces: a nonruled smooth surface has pseudo-effective canonical class on its minimal model, and a moving class is nef; pullback and exceptional contributions preserve the needed nonnegativity. Conversely, on a ruled surface one can choose a sufficiently positive moving divisor with negative canonical intersection. The source explicitly defers its proof, and this modern explanation should not be represented as an argument already present in the chapter.

A smooth rational curve with square at least zero also forces ruledness. Its normal bundle has nonnegative degree and vanishing \(H^1\), so it moves in a positive-dimensional family covering an open subset; the surface is uniruled and hence ruled over \(\mathbf C\). This explains the exclusion of genuine second-species curves from the relevant nonruled setting once the genus/assigned-point convention is fixed. Contracting \((-1)\)-curves terminates because each contraction decreases the Picard number. Thus a smooth minimal model exists; uniqueness for nonruled surfaces is a further theorem, not proved by termination alone.

### §12. Reducible exceptional curves (pp. 37–39)

#### Total transforms, connected support, and the free chain

The source starts with blowups of distinct points, whose exceptional curves are disjoint, and lets points become infinitely near. The resulting exceptional divisors can have several components and multiplicities. The correct modern object is the **total transform of one point-exceptional divisor through later blowups**. Its numerical invariants remain square \(-1\) and arithmetic genus zero even when its individual strict components have smaller squares.

For successive free points \(P_0,\ldots,P_s\) following one smooth branch, write \(E_j\) for the final strict exceptional components. Then
\[
E_j^2=-2\ (j<s),\quad E_s^2=-1,\quad E_j\cdot E_{j+1}=1,
\]
with all other distinct intersections zero, and
\[
\Omega_j=E_j+E_{j+1}+\cdots+E_s.
\]
There are \(s+1\) vertices and \(s\) edges. Therefore
\[
p_a(\Omega_0)=\sum_{j=0}^{s}p_a(E_j)+s-s=0,
\qquad
\Omega_0^2=-2s-1+2s=-1.
\]
The scan on p. 38 instead prints \((s-1)-(s-1)\) in the genus calculation and \(2(s-1)\) in the square calculation. The first pair happens to cancel, concealing the index shift; the second gives the wrong result with the displayed \(s+1\) components. These are **source indexing slips**. The intended invariants are correct after replacing the edge count by \(s\).

In this passage *connessa* means that successive components meet, explicitly in one point. **Chapter I does not define numerical 1-connectedness** (the condition \(A\cdot B\ge1\) for every decomposition \(D=A+B\) into nonzero effective divisors). It also does not prove a converse for arbitrary connected divisors with \(p_a=0,D^2=-1\). Its reducible divisors have the much stronger blowup/proximity structure just described. This observation is essential when evaluating later uses of “connected.”

#### A satellite point and the doubled component

Blow up \(P_0\), then a point \(P_1\) on the first exceptional line, then their intersection \(P_2\). On the final surface,
\[
\Omega_0=E_0+E_1+2E_2,\quad
\Omega_1=E_1+E_2,\quad
\Omega_2=E_2.
\]
The strict squares are \(-3,-2,-1\); \(E_0E_1=0\), while \(E_0E_2=E_1E_2=1\). Thus
\[
\Omega_0^2=-3-2-4+4+4=-1.
\]
Adjunction on the three rational components gives \(K\cdot E_0=1\), \(K\cdot E_1=0\), \(K\cdot E_2=-1\); hence \(K\cdot\Omega_0=-1\) and \(p_a(\Omega_0)=0\). This proves the source's cuspidal/satellite example without relying on a pictorial continuity argument.

On p. 39 the text correctly names the new curve \(\omega_2\), then says that the transformed \(\omega_1\) must be counted twice. The scan really has \(\omega_1\). It should be \(\omega_2\): another **source subscript slip**, already visible from the preceding displayed sum.

#### General proximity computation

Let \(E_i^*\) denote the total transform of the \(i\)-th exceptional divisor to the final surface. These classes satisfy
\[
E_i^*\cdot E_j^*=-\delta_{ij}.
\]
If \(P_j\) is proximate to \(P_i\), the strict transform is
\[
E_i=E_i^*-\sum_{j\text{ proximate to }i}E_j^*.
\]
The triangular proximity matrix is invertible over the integers. Inverting it expresses each \(\Omega_i=E_i^*\) as an effective weighted sum of strict components. It immediately gives
\[
E_i^2=-1-\#\{j:P_j\text{ is proximate to }P_i\}.
\]
The coefficients can also be read as orders of appropriately chosen curvettes through the cluster; this is the modern formulation of the source's minimum branch-order rule for \(h_i\). One must retain the entire proximity structure: merely ordering the centres does not determine the graph if satellite points occur. The source's “last proximate successor” description concerns the specified sequence following a branch, not an arbitrary combinatorial tree without a realizability condition.

The rules on pp. 38–39 are therefore **correct sketches in substance**, apart from the identified slips. Pullback itself proves that every \(\Omega_i\) has square \(-1\) and arithmetic genus zero; no general contraction criterion for arbitrary connected curves follows from those equalities.

Finally,
\[
K_{X_s}-\pi^*K_X=\sum_{i=0}^{s}E_i^*=\sum_i\Omega_i.
\]
Expanding the right-hand side in strict components adds their multiplicities exactly as the last paragraph describes. Thus the observation anticipates the relative canonical divisor and the later canonical-system calculation. This is a useful modern identification, not a claim that the source proves canonical adjunction at this point.

The verifiable cited paper is Barber and Zariski (1935), pp. 119–141. The printed initial “E.” is incorrect; the paper's author is Sherburne F. Barber. The footnote abbreviation “Ann. Journ.” is also inconsistent with the verified *American Journal of Mathematics*. The doubtful superscript on \(\omega_i\) is \(h_i\), and the odd “con-le” is actually printed with a hyphen. The footnote marker after Enriques is printed **(2)**, not the transcription's [3]; preserving the scan leaves a numbering anomaly which is recorded rather than silently regularized.

### §13. The virtual characteristic series (p. 40)

For an effective Cartier divisor \(C\) on a smooth surface, the intrinsic characteristic object is its normal line bundle
\[
N_{C/X}=\mathcal O_C(C),\qquad\deg N_{C/X}=C^2.
\]
The complete virtual characteristic series is \(|\mathcal O_C(C)|\), even when \(C\) is isolated. The line bundle and its divisor class are always defined; its space of effective sections may be zero. Positive degree alone does not guarantee a section on a curve of positive genus.

The auxiliary construction in the text gives a rigorous proof. Choose a sufficiently ample \(K\), so that \(H^1(X,\mathcal O_X(K))=0\). Then
\[
0\to\mathcal O_X(K)\to\mathcal O_X(C+K)\to\mathcal O_C(C+K)\to0
\]
shows that restriction to \(C\) is surjective. Restrict those sections whose intersection divisor contains the fixed \(K\cap C\), and divide on \(C\) by the section defining that intersection. The result is all of \(H^0(C,\mathcal O_C(C))\). This proves independence of the sufficiently ample auxiliary choice and completeness of the resulting series. The source sketches the comparison of two auxiliary systems and explicitly postpones the sufficiency assertion; Serre vanishing supplies it.

For the ordinary characteristic series of a complete linear system, the exact sequence is instead
\[
0\to\mathcal O_X\to\mathcal O_X(C)\to N_{C/X}\to0.
\]
Thus its sections form the image of \(H^0(X,\mathcal O_X(C))/\mathbf C\) in \(H^0(C,N_{C/X})\). Its deficiency embeds in \(H^1(X,\mathcal O_X)\), so it is bounded by the irregularity \(q\). The virtual series can therefore be larger than the characteristic series of the linear system, precisely the phenomenon motivating continuous systems in the source. The exact sequences and the identity of the normal sheaf are verified in Stacks Project Section 31.15 (Tag 0C4S; Lemma 31.15.2, Tag 0B3P).

Infinitesimal deformations of \(C\) in the surface give sections of \(N_{C/X}\); the Hilbert-scheme tangent space is \(H^0(C,N_{C/X})\). Locally a deformation over \(\mathbf C[\epsilon]/(\epsilon^2)\) is the graph of an \(\mathcal O_X\)-linear map from the ideal \(\mathcal I_C\) to \(\mathcal O_C\); it factors through \(\mathcal I_C/\mathcal I_C^2\). Gluing identifies these maps with \(H^0(\mathcal Hom(\mathcal I_C/\mathcal I_C^2,\mathcal O_C))=H^0(N_{C/X})\). The corresponding gluing obstruction is the source of the first-cohomology obstruction group (Hartshorne, 2010, Chapters 1–2). Obstructions can lie in \(H^1(C,N_{C/X})\). Therefore an actual continuous family supplies some, and in favourable cases all, of the virtual characteristic series. Neither the text nor this statement establishes that every first-order section integrates, or that every continuous family has complete characteristic series. Those are substantially stronger claims and should not be imported into this paragraph.

The historical note credits a Castelnuovo letter and Severi's later definition, with the surface of unordered pairs of points of a genus-two curve as an example. Modernly \(\operatorname{Sym}^2 C\) is birational to \(\operatorname{Jac}(C)\), through the degree-two Abel map. The historical word “hyperelliptic surface” here is not automatically the current classification term for bielliptic surfaces. The exact letter and Severi footnote were not independently inspected; their history is reported as Enriques's, with that limitation.

### Independent deductions and useful checks supplied by this audit

1. **Incidence criterion counterexample (high confidence).** The \(\operatorname{Sym}^r B\) family of sums of fibres over a positive-genus base isolates the essential irreducibility hypothesis in §4. The Picard-map proof above explains why integral members eliminate the counterexample.
2. **A computational check on exceptional configurations (high confidence).** Encode the proximity matrix, invert it, and compute the strict intersection matrix. Every legitimate total transform must have square \(-1\), canonical intersection \(-1\), and arithmetic genus zero. The free-chain and satellite calculations above test both the signs and the nonreduced coefficients. This is a finite verification method, not a proposed new classification theorem.
3. **Positive degree with empty virtual characteristic series (high confidence).** Choose a curve \(B\) of genus \(g\ge2\) and a line bundle \(N\) of degree \(1\le d<g\) with \(H^0(B,N)=0\). On the ruled surface \(\mathbf P(\mathcal O_B\oplus N)\), the section corresponding to the quotient onto \(N\) has normal bundle \(N\), square \(d>0\), and no infinitesimal normal section. This separates the virtual characteristic class from an effective characteristic series.
4. **Singular rational representatives (high confidence).** The nodal-cubic calculation in §11 prevents geometric genus zero from being confused with arithmetic genus zero before assigned singularities are resolved. It provides a concrete test for every later invocation of a rational exceptional curve.
5. **No fabricated open problem.** The remaining limits concern damaged typography and original historical papers not inspected in full. They are not presented as unsolved mathematical problems.


### References and verification: Chapter I

The following references support the modern formulations in the chapter commentary. “Verified” distinguishes an inspected mathematical text from bibliographic metadata. Access was checked on 6 November 2026. 

#### Primary text under audit

Enriques, F. (1949). *Le superficie algebriche*. Zanichelli. Chapter I, printed pp. 15–40.

The supplied PDF has 115 scan pages. The audited pages are PDF pp. 30–55, inclusive; printed p. 15 is an unnumbered chapter-opening page. The supplied transcription lines 672–1380 were compared with the scan. This local primary source controls all quotations, formula readings, and author-versus-transcriber decisions.

#### Modern foundations

**Hartshorne, R. (1977). *Algebraic geometry*. Springer.** [https://doi.org/10.1007/978-1-4757-3849-0](https://doi.org/10.1007/978-1-4757-3849-0)

Publisher record: [https://link.springer.com/book/10.1007/978-1-4757-3849-0](https://link.springer.com/book/10.1007/978-1-4757-3849-0)

Relevant locations: II.6, divisors; II.7, projective morphisms and linear systems; III.5, projective-space cohomology and Serre vanishing; V.1, intersection theory, Riemann–Roch and adjunction; V.3, blowups; V.5, birational transformations and exceptional curves; V.6, classification of surfaces. These are chapter/section references, not invented theorem numbers. Publisher metadata was checked (author, 1977 date, GTM 52, DOI). The commentary supplies the elementary proofs it uses; it does not claim to have reread the entire textbook during this audit.

**Hartshorne, R. (2010). *Deformation theory*. Springer.** [https://doi.org/10.1007/978-1-4419-1596-2](https://doi.org/10.1007/978-1-4419-1596-2)

Publisher record: [https://link.springer.com/book/10.1007/978-1-4419-1596-2](https://link.springer.com/book/10.1007/978-1-4419-1596-2)

Relevant locations: Chapters 1–2, first-order embedded deformations and their obstruction theory. The publisher explicitly describes its normal-bundle treatment of the Hilbert tangent space and obstructions.  The commentary also gives the ideal-map argument identifying first-order deformations with Hom(I/I²,O_C), so the identification is not merely asserted on the authority of an uninspected theorem number.

**The Stacks Project Authors. (n.d.). *Contracting exceptional curves* (Section 54.16, Tag 0C2I).** [https://stacks.math.columbia.edu/tag/0C2I](https://stacks.math.columbia.edu/tag/0C2I)

- Lemma 54.16.8, Tag **0C2M**: [https://stacks.math.columbia.edu/tag/0C2M](https://stacks.math.columbia.edu/tag/0C2M) — existence of contraction in the proper/ample setting, constructed by twisting an ample line bundle by a suitable multiple of the exceptional curve. The statement and proof were read. 
- Lemma 54.16.4, Tag **0C2L**: [https://stacks.math.columbia.edu/tag/0C2L](https://stacks.math.columbia.edu/tag/0C2L) — the contraction is the Stein factorization of a proper map contracting the exceptional curve and quasi-finite off it; the proof supplies the regular local target and blowup description. The statement and proof were read. 
- The commentary works over C on smooth projective surfaces, a special case of these statements. No positive-characteristic extension of every other chapter argument is inferred from this more general contraction theorem.

**The Stacks Project Authors. (n.d.). *Effective Cartier divisors and invertible sheaves* (Section 31.15, Tag 0C4S).** [https://stacks.math.columbia.edu/tag/0C4S](https://stacks.math.columbia.edu/tag/0C4S)

- Lemma 31.15.2, Tag **0B3P**: [https://stacks.math.columbia.edu/tag/0B3P](https://stacks.math.columbia.edu/tag/0B3P) — normal bundle N_(C/X)=O_X(C)|C.
- Lemma 31.15.4 — O(D+E)=O(D)⊗O(E).
- Lemma 31.15.10 — regular section/effective Cartier divisor correspondence.
- Remark 31.15.11 — 0→O_X→O_X(C)→i_*N_(C/X)→0.
- The mathematical text was inspected, not just the title. 

#### Bertini: statements, proofs, and the documented historical repair

**Kleiman, S. L. (1998). Bertini and his two fundamental theorems. *Rendiconti del Circolo Matematico di Palermo, Serie II, Supplemento, 55*, 9–37.**

Author preprint (1997): [https://arxiv.org/abs/alg-geom/9704018](https://arxiv.org/abs/alg-geom/9704018)

Verified full-text PDF: [https://www.sba.unipi.it/sites/default/files/persona_archivio/steven_l._kleiman_bertini_and_his_two_fundamental_theorems.pdf](https://www.sba.unipi.it/sites/default/files/persona_archivio/steven_l._kleiman_bertini_and_his_two_fundamental_theorems.pdf)

Publisher/bibliography metadata were cross-checked with [https://stacks.math.columbia.edu/bibliography/Kleiman-Bertini](https://stacks.math.columbia.edu/bibliography/Kleiman-Bertini) (search result accessible; direct opening returned an access error).

Specific locations actually checked: Theorem 4.1 for smoothness off the fixed base locus and ambient singularities; Theorem 5.3 for the reducible/general-member characterization; the ensuing discussion of algebraicity of the family of components; the bibliography for van der Waerden and Zariski. The text expressly identifies the missing algebraicity step in Bertini's historical proof and records van der Waerden's 1937 repair, p. 709. This is the basis for naming an actual historical repairer. It is not used to assign unrelated omissions of Enriques to Zariski or van der Waerden.

**van der Waerden, B. L. (1937). Zur algebraischen Geometrie. X. Über lineare Scharen von reduziblen Mannigfaltigkeiten. *Mathematische Annalen, 113*, 705–712.**

Primary-volume digital record: [https://gdz.sub.uni-goettingen.de/id/PPN235181684_0113](https://gdz.sub.uni-goettingen.de/id/PPN235181684_0113)

The Göttingen volume record verifies the exact title, eight-page extent, volume, and 1937 volume date. Kleiman supplies the precise relevance of p. 709. A secondary author bibliography at [https://www.math.rug.nl/~top/vdwbib.pdf](https://www.math.rug.nl/~top/vdwbib.pdf) groups this work under “1936c”; the commentary uses the journal volume date 1937, as does Kleiman. The original eight-page article was not independently read line by line. 

**Zariski, O. (1941). Pencils on an algebraic variety and a new proof of a theorem of Bertini. *Transactions of the American Mathematical Society, 50*, 48–70.** [https://doi.org/10.1090/S0002-9947-1941-0004241-4](https://doi.org/10.1090/S0002-9947-1941-0004241-4)

Journal/JSTOR record: [https://www.jstor.org/stable/1989911](https://www.jstor.org/stable/1989911)

Issue record: [https://www.jstor.org/stable/i308246](https://www.jstor.org/stable/i308246)

Exact title, author, pages, and article identifier were verified in the journal issue record; the AMS DOI is also confirmed in an AMS bibliography. Direct opening of the DOI failed in the web tool, so full-text inspection of this paper is not claimed. Its historical role is checked in Kleiman. 

**Zariski, O. (1944). The theorem of Bertini on the variable singular points of a linear system of varieties. *Transactions of the American Mathematical Society, 56*, 130–140.** [https://doi.org/10.2307/1990280](https://doi.org/10.2307/1990280)

Metadata/DOI were verified in the MaRDI bibliographic record and an author-hosted AMS review; the title and pagination were cross-checked in Kleiman's bibliography. Direct DOI opening failed. Its original proof was not independently read in full.  The commentary attributes the specific historical role through the verified Kleiman discussion.

Bertini's original “Sui sistemi lineari” was published in *Rendiconti dell'Istituto Lombardo*, series II, 15 (1882), 24–28, although associated with a December 1880 date. This publication/date distinction is recorded in Kleiman. Enriques's 1880 dating should therefore not automatically be called a mathematical or transcription error.

#### Reducible exceptional curves

**Barber, S. F., & Zariski, O. (1935). Reducible exceptional curves of the first kind. *American Journal of Mathematics, 57*(1), 119–141.** [https://doi.org/10.2307/2372025](https://doi.org/10.2307/2372025)

Primary journal record: [https://www.jstor.org/stable/2372025](https://www.jstor.org/stable/2372025)

Issue record: [https://www.jstor.org/stable/i316347](https://www.jstor.org/stable/i316347)

An IAS author bibliography also identifies **Sherburne F. Barber**: [https://www.ias.edu/sites/default/files/library/pdfs/ar/publicationsofme00inst.pdf](https://www.ias.edu/sites/default/files/library/pdfs/ar/publicationsofme00inst.pdf)

The exact paper, author initials, journal, volume, pages, and DOI were verified. The journal record is the authority for correcting the source's “E. Barber,” “Mathematik,” and “Ann. Journ.” Full-paper inspection was not obtained; the mathematical rules needed here were instead proved directly with blowup intersection theory in the commentary. Therefore the audit does not invent a theorem number in Barber–Zariski. 

**Du Val, P. (1936). Reducible exceptional curves. *American Journal of Mathematics, 58*(2), 285–289.** [https://doi.org/10.2307/2371038](https://doi.org/10.2307/2371038)

Primary journal record: [https://www.jstor.org/stable/2371038](https://www.jstor.org/stable/2371038)

Issue record: [https://www.jstor.org/stable/i316344](https://www.jstor.org/stable/i316344)

The primary issue contents identify Patrick Du Val, the exact title, pages285–289, April1936, and article DOI. This resolves the abbreviated source citation on p.24. The mathematical text was not read in full; the direct proximity calculation in the commentary supplies the needed proof independently.  Opening the primary article returned its exact title but no readable body; DOI opening failed.

**Zariski, O. (1971). *Algebraic surfaces* (2nd supplemented ed.). Springer.** [https://doi.org/10.1007/978-3-642-92450-7](https://doi.org/10.1007/978-3-642-92450-7)

Publisher record: [https://link.springer.com/book/10.1007/978-3-642-92450-7](https://link.springer.com/book/10.1007/978-3-642-92450-7)

Useful modern/classical supplementary reference for exceptional curves and ruled surfaces. Publisher metadata was verified; the entire text was not newly read. The commentary's actual proof reference for contraction is the inspected Stacks section.

#### Completing the projected-quintic example

**Friedman, M., Lehman, R., Leyenson, M., & Teicher, M. (2012). On ramified covers of the projective plane II: Generalizing Segre's theory. *Journal of the European Mathematical Society, 14*, 971–996.** [https://doi.org/10.4171/JEMS/324](https://doi.org/10.4171/JEMS/324)

Primary published full text: [https://ems.press/content/serial-article-files/31835](https://ems.press/content/serial-article-files/31835)

Section 2 explicitly records the ordinary double, triple, and pinch local equations for a generic projection to P³ and the irreducibility of its reduced double curve unless the source is the Veronese surface. Those statements and the first-page bibliographic information were inspected. This is the verified general-position input for the new reconstruction of Enriques's quintic. The calculations of conductor class, Euler characteristics, eight pinch points, one triple point, and the quadric cone are supplied in the commentary and are not represented as a specific quintic theorem quoted from this article. 

The article cites Moishezon's *Complex surfaces and connected sums of complex projective planes*, Lecture Notes in Mathematics 603 (1977), Theorem 3, for irreducibility, and Ragni Piene's “Some formulas for a surface in P³,” LNM 687 (1978), 196–235, for classical projection formulas. These additional citations were seen in its bibliography but were not independently inspected; they are not needed as stand-alone verified proof references here.

**Fulton, W. (1998). *Intersection theory* (2nd ed.). Springer.**

Chapter 14, “Degeneracy loci and Grassmannians,” especially §14.4 (Thom–Porteous):
[https://doi.org/10.1007/978-1-4612-1700-8_15](https://doi.org/10.1007/978-1-4612-1700-8_15)

Primary publisher chapter record and mathematical preview:
[https://link.springer.com/chapter/10.1007/978-1-4612-1700-8_15](https://link.springer.com/chapter/10.1007/978-1-4612-1700-8_15)

The preview verifies the vector-bundle degeneracy setting, expected-codimension condition, and Chern-class determinant formula; bibliographic metadata establish the 1998 edition. The chapter's §14.4 title and page 254 were independently visible in the contents record, but the commentary avoids asserting an unverified theorem number. For ranks 2→3 and rank ≤1, the determinant reduces to c₂(F−E), precisely the formula used for the pinch points. 

#### Source citations that remain historical reports, not independently verified articles

- Enriques–Chisini, the books/volumes/pages cited on pp. 24 and 39.
- Enriques–Conforto, *Le superficie razionali*, Bologna, 1939 (1945), cited on p. 26. The illustrative quintic has now been independently reconstructed, but this particular historical derivation was not inspected.
- Du Val’s full proof was not inspected, although the precise article was identified and is listed above.
- The Noether and Brill–Noether *Mathematische Annalen* volume references in §8. The intrinsic residual theorem is proved independently; the exact historical entries are not guessed.
- The Enriques 1893/1896 history, Severi's 1905 “Sulle curve algebriche virtuali appartenenti ad una superficie algebrica,” and Lefschetz attribution on pp. 29–30.
- Castelnuovo's letter and the Severi 1904 note on p. 40.
- Segre and Castelnuovo's introduction/naming of the characteristic series in the p. 19 footnote.

These are not mathematical gaps in the modern proofs supplied. They are limits on bibliographic and historiographical verification. The audit identifies no fictitious historical “repair” for them.


## Chapter II: Covariant systems and invariants

### Scope, notation, and principal findings

This chapter develops the Jacobian class, adjunction, the canonical class, geometric genus, canonical self-intersection, exceptional curves, and plurigenera. Every printed page 41–65 was read against its scan; page 66 was inspected and is blank. Original transcription lines 1381–2230 are the reference frame for the correction register. The claim register separates the status of Enriques's argument from the modern justification supplied below.

Unless a singular projective model is discussed explicitly, let \(X\) be a smooth projective connected surface over \(\mathbb C\). Write \(K_X\) for its canonical divisor class, \(D\sim D'\) for linear equivalence, \(D^2\) for self-intersection, and
\[
p_a(D)=1+\frac{D^2+K_XD}{2}
\]
for the arithmetic, or Enriques's virtual, genus of a divisor. This polynomial definition extends to arbitrary divisor classes, including classes without effective representatives. Enriques's “degree” of a curve on a surface normally means its self-intersection, with prescribed base conditions accounted for; projective order is a different number. His “equivalence” here is linear equivalence, not merely numerical equivalence. His \(p^{(1)}\) is \(K_X^2+1\), his \(p^{(2)}\) is \(K_X^2\), and his surface genus \(p\) or \(p_g\) is \(h^0(X,\omega_X)\). A bare \(p\) for a ruled surface's base curve in §6 means that curve's genus instead.

The central calculation is
\[
J(D)\sim K_X+3D,\qquad D'=K_X+D.
\]
It proves the independence assertions and explains prescribed-base-point corrections. Enriques gives genuine arguments for these assertions. The qualifications concern degenerating nets, complete systems on a surface versus complete series on a member, and virtual intersections of nonreduced exceptional divisors. Results explicitly deferred—completeness of adjoint surface sections and existence of minimal models—must not be represented as proved in this chapter.

There is a printed minus-sign error in the five-by-five determinant on p. 45. The prose ordering of exceptional-point corrections on pp. 48–49 conflicts with the correct displayed formula. The overline over the last \(K\) on p. 46 is a transcription error: enlargement shows ordinary \(K\). Several other flags concern punctuation or historical spelling. The p. 43 reference visibly reads “Libro XV, cap. IV, §39, vol. II, pag. 634 e seg.”; the volume must not be changed to III. The unusual book number requires checking against the cited volume, not silent conjectural emendation.

### §1. Jacobian curves (pp. 41–42)

#### Definition and Enriques's argument

A net is a projective two-dimensional linear system. Its Jacobian is the locus where a member has a double point, equivalently where two members are tangent. At a point where the evaluation and first-derivative conditions have their expected rank, a linear combination of two tangent local equations has zero value and zero differential, proving the equivalence. This is a determinantal construction: its multiplicities, not just its reduced support, are essential.

For plane curves of degree \(n>1\), Enriques states that the Jacobian has degree \(3n-3\). At an ordinary assigned base point of multiplicity \(i\), its multiplicity is generically \(3i-1\). A simple base point gives a double point of the Jacobian; a common tangent there gives generically a triple point with that tangent. “In general” is essential: further infinitesimal conditions can raise multiplicity. The reference is Enriques–Chisini, volume II, Book III, chapter I, §5. Transfer to a smooth surface is justified by finite-order osculation and rational local models. An exact local-coordinate calculation makes the required finite-order argument precise.

Enriques proves linear equivalence of Jacobians of nets in one irreducible system. Two nets sharing a pencil span a projective three-dimensional subsystem. Nets through that pencil form a \(\mathbb P^1\); their Jacobians form a rational pencil of curves. Two nets sharing only one curve are compared through an auxiliary net sharing a pencil with each. Nets with no common member are linked through a third sharing one member with each. Transitivity finishes the proof. It uses the earlier result that a rational pencil is linear.

An implicit hypothesis must be retained in “arbitrary nets”: each Jacobian under comparison must be a divisor, not an identically zero determinant. An irreducible net over \(\mathbb C\) gives a generically finite map, but a special subnet of a larger irreducible system may be composed with a pencil. For example \(\langle x^2,xy,y^2\rangle\subset H^0(\mathbb P^2,\mathcal O(2))\) has identically zero Jacobian. This identifies a genericity convention; it does not disprove equivalence of the defined Jacobian divisors.

#### Modern proof by principal parts

For \(L=\mathcal O_X(D)\), the first-principal-parts sequence is
\[
0\longrightarrow\Omega_X^1\otimes L\longrightarrow P_X^1(L)
\longrightarrow L\longrightarrow0.
\]
The middle bundle has rank three and determinant \(\omega_X\otimes L^3\). The sequence is verified in the Stacks Project, §18.34, Lemma 18.34.6. Three sections \(V\subset H^0(X,L)\) give
\[
V\otimes\mathcal O_X\longrightarrow P_X^1(L).
\]
Its determinant, when nonzero, defines a divisor in \(|K_X+3D|\). In local coordinates and a trivialization of \(L\), its equation is
\[
\det\begin{pmatrix}
f_0&f_1&f_2\\
\partial_x f_0&\partial_x f_1&\partial_x f_2\\
\partial_y f_0&\partial_y f_1&\partial_y f_2
\end{pmatrix}=0.
\]
Thus the result concerns a line-bundle class, not merely a numerical class. On \(\mathbb P^2\), \(K=-3H\), giving degree \(3n-3\).

At an \(i\)-fold assigned point, the naïve lowest determinant order is \(3i-2\). Euler's relation on the initial homogeneous degree-\(i\) terms makes that leading determinant vanish, so the generic order becomes \(3i-1\). Equivalently, on the blowup,
\[
\widetilde D=\pi^*D-iE,\quad
K_{\widetilde X}=\pi^*K_X+E,\quad
K_{\widetilde X}+3\widetilde D=\pi^*(K_X+3D)-(3i-1)E.
\]
Excess actual multiplicity does not change this virtual prescribed coefficient.

### §2. The complete Jacobian system and fixed components (pp. 42–48)

#### Completion and infinitely near conditions

The complete Jacobian system contains the Jacobians already constructed, imposing multiplicity \(3i-1\) at each assigned \(i\)-fold base point. Without assigned base conditions, completion adds none. This does not imply that the completed system has no actual base points.

For successive simple points \(O,O_1\), with \(O_1\) specifying the common tangent, Enriques distinguishes an actual triple point at \(O\) plus a simple point at \(O_1\) from the virtual pair of double points. On the twice-blown-up surface, let \(E_1^*\) be the total transform of the first exceptional divisor and \(E_2\) the second. The intrinsic Jacobian class is
\[
\pi^*(K_X+3D)-2E_1^*-2E_2.
\]
An actual strict Jacobian with multiplicities \(3,1\) has class
\[
\pi^*(K_X+3D)-3E_1^*-E_2.
\]
Their difference is \(E_1^*-E_2\), the strict first exceptional curve. This exactly explains the virtual adjustment. It does not guarantee an actual enlargement with precisely two ordinary double points; Enriques explicitly allows the enlargement to fail.

Adding a fixed curve \(A\) to a net yields
\[
J(A+D)=3A+J(D).
\]
Enriques calls this fixed curve \(K\) temporarily, before introducing the canonical notation. The coefficient is exactly three unless the residual Jacobian already contains \(A\). Locally replace every \(f_i\) by \(af_i\) in the jet determinant. Row subtraction on \(a\ne0\) gives \(a^3J(f_0,f_1,f_2)\), an identity of regular expressions extending everywhere. This proves the statement without osculating surfaces.

#### Analytic verification and the printed determinant error

Let \(F=(f=0)\subset\mathbb P^3\) be smooth of degree \(n\); let \(\varphi_i\) have degree \(m\) and \(\varphi\) degree \(s\). Enriques chooses an auxiliary curve \(L\), not containing the fixed component, such that \(C+L\) is cut by degree-\(m\) hypersurfaces. The net is represented by
\[
\varphi(\lambda_1\varphi_1+\lambda_2\varphi_2+\lambda_3\varphi_3)=0.
\]
The availability of the complete residual systems is assumed from the adjoint-completeness result, expressly referred forward to Chapter III.

Write \([g_1,g_2,g_3,g_4]\) for the determinant with their four gradients as columns. The first determinant on p. 44 is
\[
D=[\varphi\varphi_1,\varphi\varphi_2,\varphi\varphi_3,f].
\]
Its last-row third-column entry has misplaced printed parentheses, \((\partial\varphi\varphi_3)/\partial x_4\); mathematically it is \(\partial(\varphi\varphi_3)/\partial x_4\). Multilinearity gives
\[
D=\varphi^3 A+\varphi^2\Phi,\qquad A=[\varphi_1,\varphi_2,\varphi_3,f],
\]
\[
\begin{aligned}
\Phi={}&\varphi_1[\varphi,\varphi_2,\varphi_3,f]\\
&+\varphi_2[\varphi_1,\varphi,\varphi_3,f]\\
&+\varphi_3[\varphi_1,\varphi_2,\varphi,f].
\end{aligned}
\]
Terms with two columns proportional to \(d\varphi\) vanish. After the stated column exchanges, these three terms are the first-row expansion of
\[
\Phi=\det\begin{pmatrix}
\varphi_1&\varphi_2&\varphi_3&0&0\\
\partial_1\varphi_1&\partial_1\varphi_2&\partial_1\varphi_3&\partial_1\varphi&\partial_1f\\
\partial_2\varphi_1&\partial_2\varphi_2&\partial_2\varphi_3&\partial_2\varphi&\partial_2f\\
\partial_3\varphi_1&\partial_3\varphi_2&\partial_3\varphi_3&\partial_3\varphi&\partial_3f\\
\partial_4\varphi_1&\partial_4\varphi_2&\partial_4\varphi_3&\partial_4\varphi&\partial_4f
\end{pmatrix}.
\]
The scan genuinely prints a minus before the last-column \(\partial_3f\). This is a source misprint, faithfully transcribed. It destroys the preceding expansion and following Euler calculation. The plus above is a mathematical correction, not the claimed scan reading.

Multiply the first row by \(m\), then subtract \(x_1,\ldots,x_4\) times the derivative rows. Euler's identity gives
\[
(0,0,0,-s\varphi,-nf).
\]
The resulting determinant is \(m\Phi\), vanishing when \(f=\varphi=0\). More precisely, with \(B=[\varphi_1,\varphi_2,\varphi_3,\varphi]\), expansion gives
\[
m\Phi=s\varphi A-nfB,
\]
\[
D=\frac{m+s}{m}\varphi^3A-\frac nm f\varphi^2B,\qquad
D|_F=\frac{m+s}{m}\varphi^3A|_F.
\]
This exact factorization is our streamlined derivation. It shows why a fourth copy occurs only when \(A|_F\) already contains the fixed component. Division by \(m\) and the nonvanishing of \(m+s\) use characteristic zero.

On pp. 46–47 Enriques instead differentiates at \(P\) with \(f(P)=\varphi(P)=0\). The first three differentiated-column determinants vanish because the first row is zero; the other two give
\[
m(\partial_i\Phi)_P=s(\partial_i\varphi)_P A(P)-n(\partial_i f)_P B(P).
\]
If the tangent planes coincide, write
\[
(\partial_i\Phi)_P=\rho(\partial_i f)_P,\quad i=1,\ldots,4.
\]
Then
\[
(m\rho+nB(P))df_P=sA(P)d\varphi_P.
\]
If \(A(P)\ne0\), \(df_P,d\varphi_P\) are proportional, contradicting the generic transversality of the simple fixed component. Otherwise \(A(P)=0\), precisely the residual-Jacobian alternative. Multiplicity is tested at its generic smooth point; special singular or tangency points do not invalidate that argument.

#### The projective verification

The last proof uses four degree-\(m\) forms:
\[
\lambda_1\varphi_1+\lambda_2\varphi_2+\lambda_3\varphi_3+\lambda_4f\psi=0,
\qquad\deg\psi=m-n.
\]
Their ambient Jacobian has degree \(4m-4\). Its restriction to \(F\) contains \(\psi\cap F\), of order \(n(m-n)\), besides the net Jacobian. Hence the latter has order
\[
n(4m-4)-n(m-n)=n(3m+n-4).
\]
This particular construction requires \(m\ge n\), achievable by enlarging the auxiliary residual choice. Multiplying by the fixed degree-\(s\) form gives four copies in the ambient Jacobian and removes one in the extraneous intersection, leaving three. The resulting order is
\[
n\{3(m+s)+n-4\}.
\]
Intrinsically \(K_F=(n-4)H\), \(H^2=n\), and \((K_F+3mH)H=n(3m+n-4)\), confirming the count.

### §3. The fundamental theorem (pp. 48–49)

For systems without assigned base conditions, the fixed-component calculation in both orders gives
\[
J(C+L)\sim J(C)+3L\sim3C+J(L),\qquad
J(C)-3C\sim J(L)-3L.
\]
Enriques extends to a pencil or isolated curve by defining
\[
J(C):=3C+J(L)-3L
\]
using a sufficiently ample auxiliary \(L\). This may have no effective representative; independence of \(L\) follows from the proved relation.

If \(C\) has an assigned \(i\)-fold point \(O\) and \(L\) an assigned \(s\)-fold point \(O'\), distinct, let \(E,E'\) be their exceptional divisors on a common blowup. Then
\[
\widetilde C=\pi^*C-iE,\quad \widetilde L=\pi^*L-sE',
\]
\[
\widetilde J_C=\pi^*(K_X+3C)-(3i-1)E,\quad
\widetilde J_L=\pi^*(K_X+3L)-(3s-1)E'.
\]
The equality is
\[
3\widetilde C+\widetilde J_L+E
\sim3\widetilde L+\widetilde J_C+E'.
\]
Here the symbols \(\widetilde J_C,\widetilde J_L\) mean transforms of the Jacobian classes built with each system's own assigned conditions. They are not the intrinsic Jacobian classes of the two transformed systems on the common blowup \(Y\): those are respectively \(K_Y+3\widetilde C=\widetilde J_C+E'\) and \(K_Y+3\widetilde L=\widetilde J_L+E\). This distinction explains the exceptional terms and avoids treating two different constructions as identical.

This is the correct displayed \(|3C+L_j+O|=|3L+C_j+O'|\). A point symbol records the exceptional correction. The surrounding prose assigns the points to the two systems in reversed order under “respectively”; the scan confirms this source wording slip. Swapping the displayed points would introduce an error.

Define
\[
K=J(C)-3C,\qquad C'=J(C)-2C=C+K.
\]
For plane degree-\(m\) curves with prescribed \(i\)-fold points, adjoints have degree \(m-3\) and prescribed multiplicities \(i-1\), because
\[
K+\widetilde C=(m-3)H-\sum(i-1)E_i.
\]
The fundamental adjunction identity is
\[
C'+L=L'+C.
\]
It holds in the Picard group even when some systems are empty. Enriques also says that adjoints will generally be effective for sufficiently positive systems and leaves the relevant bounds to later theory. A precise modern sufficient condition is \(C=mH\) with \(H\) ample and \(m\gg0\): Serre vanishing and surface Riemann–Roch give \(h^0(K_X+mH)>0\). The passage should not be converted into a theorem about every divisor of large arithmetic genus without positivity hypotheses. Absence of assigned base conditions does not erase the actual common points of a complete system.


### §4. Canonical curves and adjoint hypersurfaces (pp. 50–52)

#### Birational covariance and the hypersurface description

Enriques compares canonical classes constructed from systems on birational surface models. Without fundamental points or exceptional curves they transform to the same system. Under a blowup, the transformed canonical system acquires the exceptional divisor once. This is covariance of divisor classes: an individual canonical divisor's strict transform need not be canonical on the blowup.

For \(F_n\subset\mathbb P^3\) with ordinary singularities, the Jacobian of a plane-section net is cut by a polar of degree \(n-1\), removing the double curve. Subtracting three hyperplane sections suggests adjoints of degree \(n-4\). Enriques discusses forced cusp or pinch points of the polar construction: these belong to that subsystem, not to the prescribed conditions of its completion. Degree-\(n-4\) adjoints through the double curve cut canonical curves outside it.

That these hypersurfaces cut the *complete* canonical system is expressly anticipated from Chapter III, as is completeness in other degrees. Polar counting alone does not prove it. It would be inaccurate to present this declared dependency as a concealed gap.

#### Modern proof for ordinary singular models

Let \(\nu:X\to F\subset\mathbb P^3\) be the smooth normalization of a hypersurface with ordinary double-curve, triple-point, and pinch-point singularities. Let \(\mathfrak c\subset\mathcal O_F\) be the conductor and \(\Delta\) its divisor upstairs. Finite duality gives
\[
\nu_*\omega_X\simeq
\mathcal Hom_F(\nu_*\mathcal O_X,\omega_F)
\simeq\mathfrak c\otimes\mathcal O_F(n-4),
\]
equivalently
\[
K_X\sim(n-4)H-\Delta.
\]
For these ordinary singularities \(\mathfrak c\) is the ideal of the double curve with its proper scheme structure. Dolgachev (2016, §2, pp. 3–4) explicitly verifies this conductor formulation and the ordinary local models. This is a verified modern justification, not a claim that Dolgachev first repaired the theorem.

If \(\Gamma\subset\mathbb P^3\) denotes the conductor subscheme on \(F\), then
\[
0\to\mathcal O_{\mathbb P^3}(d-n)\to\mathcal I_\Gamma(d)
\to\mathfrak c(d)\to0.
\]
Since \(H^1(\mathbb P^3,\mathcal O(k))=0\) for every \(k\), degree-\(d\) adjoints cut the complete system
\[
\bigl|K_X+(d-n+4)H\bigr|.
\]
Local duality identifies the correct ideal; projective-space cohomology proves completeness. At \(d=n-4\) this is \(|K_X|\).

Enriques also states the orders \(i-1\) along an ordinary \(i\)-fold curve and \(s-2\) at an ordinary isolated \(s\)-fold conical point, without their full local proofs. The isolated-point rule follows by blowing up the ambient smooth threefold: its canonical divisor gains \(2E\), while the strict surface subtracts \(sE\). Adjunction gives discrepancy \((2-s)E\), requiring the adjoint numerator to vanish \(s-2\) times. This assumes an ordinary point with smooth projectivized tangent cone. Multiplicity alone does not determine the adjoint ideal at an arbitrary singularity.

For a sequence of blowups \(f:X\to Y\),
\[
K_X=f^*K_Y+K_{X/Y}.
\]
Enriques's “impure” system includes the discrepancy divisor. His later precise “pure” system is the pullback of the canonical system on the contracted model. It is **not** obtained by removing every fixed component: base points of \(|K_Y|\) may force further exceptional components in \(f^*|K_Y|\), which he retains as pure.

### §5. Restriction of canonical and adjoint systems (pp. 52–53)

#### The characteristic-series proof

Let \(C\) be a smooth general member of a mobile system, of genus \(\pi\) and self-intersection \(n\). Its characteristic pencil has degree \(n\). Curve Riemann–Hurwitz gives ramification degree \(2n+2\pi-2\) and class \(K_C+2C|_C\). Enriques identifies this ramification divisor with the cut of the net Jacobian. Subtracting two characteristic divisors shows that adjoints cut canonical groups; subtracting three gives the characteristic residual:
\[
(K_X+C)|_C\simeq K_C,\qquad K_X|_C\simeq K_C-C|_C.
\]
Consequently
\[
C\cdot C'=2\pi-2,\qquad C\cdot K_X=2\pi-2-n.
\]
This is a genuine argument using the curve-theoretic ramification theorem.

For arbitrary curves Enriques adds a sufficiently positive auxiliary \(L\), so that \(C+L\) has a mobile irreducible representative, and subtracts the formulas for \(L\). If \(p_a(C)=\pi\), \(p_a(L)=\rho\), and \(CL=s\), then
\[
p_a(C+L)=\pi+\rho+s-1,\qquad(C+L)^2=C^2+2s+L^2.
\]
Cancellation yields the same formula for \(C\). For singular or reducible curves \(\pi\) is the arithmetic/virtual genus, not normalization genus.

#### Modern adjunction and its limits

For smooth \(C\), determinants in
\[
0\to\mathcal O_C(-C)\to\Omega_X^1|_C\to\Omega_C^1\to0
\]
give \(\omega_C\simeq(\omega_X(C))|_C\). The same identity using the dualizing sheaf holds for any effective Cartier divisor on a smooth surface. Riemann–Roch supplies the virtual version:
\[
\chi(\mathcal O_X(D))=\chi(\mathcal O_X)+\frac{D(D-K_X)}2.
\]
From \(0\to\mathcal O_X(-D)\to\mathcal O_X\to\mathcal O_D\to0\),
\[
\chi(\mathcal O_D)=-\frac{D(D+K_X)}2,\qquad
p_a(D)=1+\frac{D(D+K_X)}2.
\]
References are Hartshorne (1977), II, Proposition 8.20, and V, Theorem 1.6; the exact numbering and statements were checked through Brosnan's author-hosted notes, §§3.1–3.2.

The line-bundle identity does **not** imply that every canonical section on \(C\) lifts to an adjoint on \(X\). In
\[
0\to\omega_X\to\omega_X(C)\to\omega_C\to0,
\]
the restriction on global sections can have cokernel in \(H^1(X,\omega_X)\). Completeness of adjoint hypersurfaces on \(X\) and completeness of the canonical series they induce on \(C\) are different questions. Enriques says the cuts are canonical groups; §5 does not assert surjectivity. Attributing that stronger assertion to him would invent a mistake.

An example supplied here makes the distinction concrete. On an abelian surface, take a smooth sufficiently ample \(C\) with \(H^1(\mathcal O_X(C))=0\). Then \(K_X=0\), \(g(C)=1+C^2/2\), and \(h^0(\mathcal O_X(C))=g(C)-1\). Restriction to \(\omega_C\) has a one-dimensional kernel, hence image of dimension \(g(C)-2\), versus \(h^0(\omega_C)=g(C)\). The defect is two, the irregularity. This illustrates the exact-sequence obstruction without contradicting adjunction.

### §6. Absolute and relative invariants (pp. 53–56)

#### Definitions and geometric genus

An absolute invariant survives every birational map of smooth models. A relative invariant survives transformations without fundamental points or exceptional curves but may change under blowups. Enriques defines
\[
p_g(X)=h^0(X,\omega_X)=\dim|K_X|+1,
\]
with \(p_g=0\) if the system is empty. The “number of linearly independent curves” is the dimension of a section space.

For a smooth degree-\(n\) hypersurface,
\[
p_g=\binom{n-1}{3}=\frac{(n-1)(n-2)(n-3)}6,
\]
obtained by counting degree-\(n-4\) forms. It vanishes for \(n=1,2,3\). This concerns a general, thus smooth, hypersurface, not every singular surface of that degree. Rational surfaces have \(p_g=0\), by birational invariance and \(K_{\mathbb P^2}=-3H\). Enriques qualifies his cubic rationality assertion to exclude cones.

For a ruled surface, a general fibre \(f\simeq\mathbb P^1\) has \(f^2=0\) and \(Kf=-2\). An effective canonical divisor cannot have negative intersection with a general moving fibre. Hence \(p_g=0\); likewise \(P_m=0\) for every \(m>0\). Enriques states this in adjoint language: a curve cutting a fibre in \(n\) points has adjoint cutting it in \(n-2\).

#### Linear genus, canonical degree, and blowups

The relative linear genus and degree are
\[
p^{(1)}=p_a(K_X),\qquad p^{(2)}=K_X^2.
\]
As \(|K'|=|2K|\), adjunction gives
\[
K_X(2K_X)=2p^{(1)}-2,\qquad
p^{(2)}=p^{(1)}-1,\qquad p^{(1)}=K_X^2+1.
\]
These use the entire virtual class; the genus of its moving part need not obey the identity.

For a blowup at a smooth point,
\[
K_{\widetilde X}=\pi^*K_X+E,\quad E^2=-1,\quad
\pi^*D\cdot E=0,\quad K_{\widetilde X}^2=K_X^2-1.
\]
In a local chart \(x=u,y=uv\), the identity \(\pi^*(dx\wedge dy)=u\,du\wedge dv\) gives the single exceptional zero. Projection and the normal bundle \(\mathcal O_{\mathbb P^1}(-1)\) give the intersection formulas. Both relative invariants decrease by one. Hartshorne V, Propositions 3.1–3.3, verified through Brosnan §4.2, is the modern reference.

For \(f:X\to X_{\min}\) comprising \(\sigma\) blowups over a nonruled minimal model,
\[
\bar p^{(1)}=p^{(1)}+\sigma,\quad
\bar p^{(2)}=p^{(2)}+\sigma,\quad
\bar p^{(2)}=\bar p^{(1)}-1.
\]
Here \(\sigma\) counts blowup steps, including infinitely near points, or the rank of the exceptional lattice. It is not the number of currently visible irreducible \((-1)\)-curves: after two infinitely near blowups their strict exceptional curves have squares \(-2,-1\), although \(\sigma=2\).

The assertion that ruled surfaces lack a model free of exceptional curves uses the classical notion including second-kind exceptions. It must not become the false modern assertion that ruled surfaces have no models without \((-1)\)-curves. Minimal ruled surfaces exist. Enriques separately defines a maximal relative linear genus across a ruled birational class.

#### The numerical examples

Plane quartics have \(\pi=3\), \(C^2=n=16\), and adjoint lines have \(\pi'=0\). The genus-sum identity
\[
\pi'=\pi+p^{(1)}+(2\pi-2-n)-1
\]
gives \(p^{(1)}=10\), agreeing with \(K_{\mathbb P^2}^2=9\). The 16 and the final subtraction of one are correct.

For a ruled surface with base genus \(g>0\) and hyperplane class \(H\), \(H^2=m\), Enriques obtains
\[
p_a(2H)=2g+m-1,\quad (2H)^2=4m.
\]
The adjoint \(K+2H\) is pulled back from a degree-\(m+2g-2\) divisor on the base, represented by that many fibres when effective. Thus
\[
p_a(K+2H)=1-(m+2g-2)=-m-2g+3,
\]
and substitution yields
\[
p^{(1)}=9-8g=-8(g-1)+1,\qquad K^2=8(1-g).
\]
Negative arithmetic genus of a disconnected fibre sum is legitimate.

For a direct check in the quotient convention \(X=\mathbb P_B(\mathcal E)\), put \(\xi=c_1(\mathcal O_X(1))\). Then
\[
K_X=-2\xi+\pi^*(K_B+\det\mathcal E).
\]
For \(H=\xi+\pi^*A\), the base degree of \(K+2H\) is \(2g-2+\deg\mathcal E+2\deg A=2g-2+H^2\), proving the asserted fibre count.

Maximality of 10 in the rational class and \(9-8g\) in an irrational ruled class requires classification of minimal rational and ruled models. The arithmetic does not prove maximality. Enriques attributes the invariant to Castelnuovo (1897) and refers forward. Modern minimal rational models have \(K^2=9\) on \(\mathbb P^2\) or \(8\) on Hirzebruch surfaces; minimal irrational ruled models have \(K^2=8(1-g)\). Blowups only lower it.

### §7. Exceptional curves in canonical systems (pp. 56–60)

#### Fixed components and disjointness

Assume \(p_g>0\), so an effective canonical divisor exists. For a \((-1)\)-curve \(E\simeq\mathbb P^1\), adjunction gives \(KE=-1\); thus every effective canonical divisor contains \(E\).

Enriques correctly proves that two such curves cannot meet. If \(EF=i\ge1\), remove their full multiplicities \(r,s\) from an effective \(K\), leaving \(R\) containing neither. Then
\[
RE=-1+r-si,\qquad RF=-1+s-ri.
\]
Both must be nonnegative, whereas their sum is \(-2+(r+s)(1-i)<0\). Finiteness follows because all such curves are components of any one effective canonical divisor. This concerns irreducible \((-1)\)-curves on the current model, not every prime component of an exceptional configuration.

A classical second-kind exceptional curve can, by the earlier argument, be represented on a birational model by a rational curve \(E\) with square \(\nu\ge0\). There
\[
KE=-2-\nu,\qquad (K-sE)E=-2-(s+1)\nu<0
\]
for every \(s\ge0\). No finite fixed multiplicity can suffice. Birational invariance of \(p_g\) preserves the effective canonical divisor on that model, giving the contradiction.

After removing one \(E\), the residual class has intersection zero with it, but may still contain it. If the blowdown point has canonical base multiplicity \(a\), then
\[
|K_X|=f^*|K_Y|+E
\]
has \(a+1\) copies of \(E\), of which \(a\) still belong to the pure pullback system. Enriques explicitly recognizes this on p. 57. “Virtually absent” describes an unassigned point, not an empty actual base scheme.

#### Infinitely near points and discrepancy

The text invokes continuity and cites Franchetta (1940) for composite exceptional multiplicities. Blowup induction gives an exact modern proof. If \(E_j^*\) is the total transform on \(X\) of the exceptional divisor born at step \(j\), then
\[
K_X=f^*K_Y+\sum_{j=1}^{\sigma}E_j^*.
\]
Each prime component's discrepancy coefficient is the sum of its multiplicities in these total transforms. This proves the stated rule without specialization. Additional fixed multiplicity inherited from \(|K_Y|\) is still possible.

For three points following a smooth branch the total exceptional curves are
\[
\omega+\omega_1+\omega_2,\qquad\omega_1+\omega_2,\qquad\omega_2,
\]
giving coefficients \(1,2,3\). For a satellite third point at the intersection of the first two prime components they are
\[
\omega+\omega_1+2\omega_2,\qquad\omega_1+\omega_2,\qquad\omega_2,
\]
giving \(1,2,4\). These are different proximity configurations.

The rigorous existence of a model free of exceptional curves is expressly deferred to surface Riemann–Roch and Castelnuovo–Enriques (1901). The modern completion uses Castelnuovo contraction: a smooth rational curve of square \(-1\) contracts to a smooth point on a projective surface. Each contraction lowers the Picard number, so the process terminates. The Stacks Project, Lemma 54.16.8 (Tag 0C2M), provides the algebraic construction: twist a sufficiently positive line bundle \(L\) by \((L\cdot E)E\), use the resulting system trivial on \(E\), and take its Stein factorization; the local contraction criterion ensures smoothness. This is a verified modern proof source, not a first-repair attribution.

For \(p_g>0\), the minimal model is nonruled and unique. Given a common resolution of two minimal models, remove any \((-1)\)-curve exceptional for both morphisms. A remaining first curve to be contracted for one side is a \((-1)\)-curve not exceptional for the other. Every \((-1)\)-curve contracted on the other side is disjoint from it by the proved disjointness theorem. It therefore remains a \((-1)\)-curve throughout those contractions, contradicting minimality on the other side. This uses standard elimination of indeterminacy and factorization into point blowups.

#### Additivity and the irreducible criterion

The function
\[
D\longmapsto2p_a(D)-2-D^2=KD
\]
is additive. This also follows by cancelling the cross term in the genus-sum formula, as the text notes. If integral \(C\) satisfies
\[
C^2>2p_a(C)-2,
\]
then \(KC<0\), so \(C\) occurs in every effective canonical divisor. After removing its full multiplicity \(s\), the residual intersection is
\[
2p_a(C)-2-(s+1)C^2.
\]
If \(C^2\ge0\), it is still negative, impossible. Thus \(C^2<0\). Since \(p_a(C)\ge0\), the original strict inequality forces \(p_a(C)=0,C^2=-1\). Arithmetic genus zero of an integral curve implies that its normalization genus and all singularity \(\delta\)-invariants are zero. Hence \(C\) is smooth rational, exactly a \((-1)\)-curve. This proof is substantially present in Enriques.

#### A qualification of the general composite assertion on p. 59

For effective divisors, define numerical 1-connectedness by \(A\cdot B\ge1\) for every expression \(D=A+B\) with \(A,B>0\), including shared prime components. For reduced curves this agrees with connected support; for nonreduced divisors it does not. Enriques explicitly explains “sconnessa” in these paragraphs by zero virtual intersection, and the exercise on p. 60 requires attention to decompositions with shared components. However, neither the reviewed Chapter I nor this passage states the fully quantified definition of numerical 1-connectedness. We add it as a precise sufficient hypothesis and a repaired reading of the criterion. The exercise disproves a support-connected reading but does not uniquely identify the author’s intended definition.

The preceding broader assertion on p. 59 deserves a separate qualification. Read literally as an assertion about effective summands, it says that every \(D\) with \(KD<0\) is obtained by adding exceptional curves orthogonal to an effective remainder \(A\) with \(KA\ge0\). This orthogonal-decomposition claim is too strong for arbitrary nonreduced effective divisors. The scan confirms “un numero virtuale nullo,” so the issue is not a transcription substitution of zero for a negative number.

Here is an explicit counterexample supplied in this audit. Blow up a smooth quartic at a point and then at a point on the first exceptional curve. On the final surface let \(F\) be the first strict exceptional curve and \(E\) the second. Then
\[
F^2=-2,\quad E^2=-1,\quad FE=1,\quad K=F+2E.
\]
For \(D=2F+E\),
\[
D^2=-5,\qquad KD=-1,\qquad p_a(D)=-2,
\]
so \(D^2>2p_a(D)-2\). An effective remainder \(A\le D\) with \(KA\ge0\) must be \(aF\), where \(a=0,1,2\). The only first-kind exceptional cycles supported there are \(E\) and \(F+E\): a cycle \(uF+vE\) with genus zero and square \(-1\) has \(K(uF+vE)=-v=-1\), hence \(v=1\), and the square then forces \(u=0\) or 1. If \(A=0\), \(D\) is not a positive sum of these cycles, because two copies of \(F\) require at least two of \(E\). If \(A=F\), the exceptional remainder \(F+E\) meets \(A\) in \(-1\), not zero. If \(A=2F\), the remainder \(E\) meets \(A\) in 2.

Thus the orthogonal decomposition fails **if its remainder is required effective**. Chapter I permits virtual divisor classes, so this is not a categorical refutation of every classical reading. Indeed the very same example has
\[
D=-E+2(F+E),\qquad K(-E)=1,\qquad(-E)(F+E)=0.
\]
The virtual remainder \(-E\) salvages the statement.

There is a precise general modern formulation. Contract to a minimal model \(f:X\to Y\) and use the orthogonal total-transform basis \(E_i^*\). Write
\[
D=f^*D_0+\sum a_iE_i^*,\qquad
K_XD=K_YD_0-\sum a_i.
\]
Here \(D_0=f_*D\) is effective or zero and \(K_Y\) is nef: the irreducible criterion proves nefness on a minimal surface with \(p_g>0\). Put
\[
B=\sum_{a_i>0}a_iE_i^*,\qquad
A=f^*D_0+\sum_{a_i\le0}a_iE_i^*.
\]
Then \(B\) is a positive sum of total exceptional divisors, \(A\cdot E_i^*=0\) for every positive coefficient in \(B\), and
\[
K_XA=K_YD_0-\sum_{a_i\le0}a_i\ge0.
\]
Moreover \(K_XD<0\) forces at least one positive \(a_i\). This proves the text's orthogonal-addition statement with a **possibly virtual remainder**, and explains why the coefficients cannot all be presumed nonnegative. The issue is an essential interpretive qualification of the sketched argument, not an invented historical failure. No first-repair attribution is made. The example is not 1-connected and does not invalidate p. 60, whose effective criterion is proved next.

#### Complete modern proof of the composite exceptional criterion

**Statement.** If \(p_g(X)>0\), an effective 1-connected divisor \(D\) with \(p_a(D)=0,D^2=-1\) is a total exceptional divisor of a contraction to a smooth point. Conversely a total pullback of a \((-1)\)-curve under successive point blowups is 1-connected with these invariants.

For the forward implication, \(KD=-1\). Some prime component has negative canonical intersection, hence is a \((-1)\)-curve \(E\). If \(D\ne E\), 1-connectedness applied to \(E+(D-E)\) gives \(t=DE\ge0\). Contract \(E\), put \(D'=\pi_*D\), and obtain
\[
D=\pi^*D'-tE,\qquad (D')^2=D^2+t^2,\qquad
K_YD'=K_XD-t<0.
\]
The pushforward \(D'\) is again 1-connected. For \(D'=A'+B'\), let \(m_A,m_B\) be the \(E\)-coefficients of the total pullbacks. Since \(D\) contains \(E\), \(m_A+m_B-t\ge1\). Choose integers \(a,b\ge0\), \(a\le m_A,b\le m_B,a+b=t\). Then
\[
D=(\pi^*A'-aE)+(\pi^*B'-bE)
\]
is an effective decomposition. Its product is \(A'B'-ab\ge1\), so \(A'B'\ge1\).

Again \(K_YD'<0\) supplies a \((-1)\)-component. Picard number decreases at each step, so eventually the entire divisor is one \((-1)\)-curve; a multiple \(rE\), \(r>1\), is excluded by 1-connectedness. Initial and final squares are both \(-1\), while each step increases square by \(t^2\). Every \(t\) is therefore zero. The original \(D\) is the total pullback of that last exceptional curve.

Conversely total pullback preserves square and arithmetic genus and preserves 1-connectedness. Indeed, decompose \(\pi^*D=A+B\), write \(A=\pi^*A'+aE,B=\pi^*B'-aE\), and compute \(AB=A'B'+a^2\). If both pushforwards are nonzero this is at least one; if one is zero, its summand is a positive multiple of \(E\), giving \(a^2\ge1\). Induction from a reduced \((-1)\)-curve finishes the proof. This proof is supplied here, not attributed to the unread original Franchetta article.

#### The quartic exercise

Let \(S\subset\mathbb P^3\) be smooth quartic containing a line \(a\). With hyperplane class \(H\), \(K_S=0,H^2=4,Ha=1,a^2=-2\). The residual plane cubics through \(a\) have class \(F=H-a\), so
\[
F^2=0,\qquad p_a(F)=1.
\]
Blow up a smooth point of a smooth such cubic; let \(E\) be exceptional and \(C=\pi^*F-E\). Then
\[
C^2=-1,\quad CE=1,\quad E^2=-1,\quad K_X=E.
\]
The exercise divisor is
\[
D=C+2E=\pi^*F+E,\qquad D^2=-1,\quad KD=-1,\quad p_a(D)=0.
\]
It is not exceptional. Its support contains an elliptic curve, and the intersection matrix
\[
\begin{pmatrix}-1&1\\1&-1\end{pmatrix}
\]
is not negative definite. Most directly \(D=(C+E)+E\) with \((C+E)E=0\). Thus it is not 1-connected although its support is connected. This resolves Enriques's paradox and shows why merely topological connectedness would make the criterion false. Numerical 1-connectedness is the explicit sufficient replacement adopted here, not a definition quoted from Chapter I.

The footnote extends the criterion to \(p_g=0\), with a rational-pencil/fixed-component exception, citing Franchetta (1941). This is assumed earlier work here. Its full original formulation and proof were not verified in that paper. The proof above retains \(p_g>0\), where all inputs have been established.

### §8. Bicanonical and pluricanonical systems (pp. 60–62)

#### Definitions and identities

A class may lack effective representatives while a multiple has them. Since \(C'=C+K\),
\[
|2K|=|2C'-2C|,\qquad |iK|=|iC'-iC|,
\qquad |iC'-iC|=|iL'-iL|.
\]
If \(C''=(C')'=C+2K\), then
\[
|(C+C')'|=|C+C''|=|2C'|,\qquad |2K|=|C''-C|.
\]
These Picard-group identities do not presume that any lower multiple is effective.

The \(i\)-th plurigenus is \(P_i=h^0(X,\mathcal O_X(iK_X))\), with bigenus \(P_2\). Enriques defines these and states absolute birational invariance. The virtual genera and degrees are relative:
\[
p_a(2K)=2p^{(1)}+p^{(2)}-1=3p^{(1)}-2,\qquad
(2K)^2=4p^{(2)}=4(p^{(1)}-1),
\]
\[
p_a(iK)=1+\frac{i(i+1)}2(p^{(1)}-1),\qquad
(iK)^2=i^2(p^{(1)}-1).
\]
Substitution in arithmetic adjunction proves all these. They concern entire divisor classes, not the genus of a moving part or the smoothness of a general representative.

#### The tetrahedral sextic

For a sufficiently general sextic with the six tetrahedron edges as double curves, the smooth normalization \(X\) has \(p_g=0\) and \(2K_X\sim0\). The unique effective bicanonical divisor is the zero divisor. Its plane-section class \(H\) has \(H^2=6,p_a(H)=4\); \(H'=H+K_X\) is cut by cubics through the edges. Although \(H'\not\sim H\), \(2H'\sim2H\). Smooth normalization with the expected ordinary singularities is required; this does not apply to every degenerate sextic containing the doubled edges.

A direct conductor computation verifies the statements. For conductor divisor \(\Delta\),
\[
K_X=2H-\Delta.
\]
The four tetrahedron faces cut \(2\Delta\): generically on each branch over an edge the two incident face equations each vanish once. Thus \(4H\sim2\Delta\), giving \(2K_X\sim0\). No quadric contains all six coordinate edges, because restriction to each coordinate line kills every square and cross-monomial coefficient. The adjoint description gives \(H^0(K_X)=0\), so \(K_X\) is nontrivial two-torsion. Therefore \(K_XH=0\), and adjunction yields \(p_a(H)=1+6/2=4\). All remaining equivalences follow. Dolgachev (2016, §2, pp. 3–4) independently verifies the conductor description and this example.

Torsion excludes \((-1)\)-curves because their canonical intersection would be \(-1\). The general exceptional-curve extension below also excludes second-kind exceptions. After one blowup \(K_{\widetilde X}=\pi^*K_X+E\), so the unique bicanonical divisor becomes \(2E\), exactly as on p. 61.

#### Birational invariance and positive plurigenera

For one blowup,
\[
iK_{\widetilde X}=\pi^*(iK_X)+iE.
\]
Every effective divisor in this class contains \(E\) at least \(i\) times: its intersection with \(E\) is \(-i\), and remains negative after removing \(r<i\) copies. Removing \(iE\), then using \(\pi_*\mathcal O_{\widetilde X}=\mathcal O_X\), gives
\[
H^0(\widetilde X,iK_{\widetilde X})\simeq H^0(X,iK_X).
\]
A common resolution proves invariance for arbitrary smooth birational models. Hartshorne V, Propositions 3.3–3.4, verified through Brosnan §4.2, supplies the blowup and pushforward facts.

If some \(P_i>0\), replace the effective canonical divisor in §7 by an effective \(iK\). For two meeting \((-1)\)-curves the residual intersection equations begin with \(-i\), and their sum is again negative. For a rational curve with nonnegative square, subtraction again never terminates. Thus irreducible exceptional curves are finite, pairwise disjoint, and first-kind. Their forced multiplicity is \(i\) times the canonical discrepancy; more copies may come from pluricanonical base points downstairs. This is Enriques's “in general \(i\) times,” including composite cycles through the total-transform rule.

The same contraction theory supplies a nonruled minimal model even if \(p_g=0\) but \(P_i>0\), and the absolute linear genus is \(K_{X_{\min}}^2+1=p^{(1)}+\sigma\). This does not assert positive plurigenus for ruled surfaces: all their positive plurigenera vanish.

### §9. Historical note (pp. 62–65)

This section offers historical attributions and restates earlier mathematics. Its claims are registered as such, without converting priority assertions into newly proved theorems.

Enriques attributes geometric genus to Clebsch's 1868 number of everywhere finite double integrals. Their integrands are holomorphic two-forms, a space of dimension \(h^0(\omega_X)\). In hypersurface language, adjoint numerators of degree \(n-4\) multiply residue two-forms, parallel to degree-\(n-3\) adjoints for plane curves. This explains the canonical divisors' birational covariance.

Noether is credited with an algebraic invariance proof and the linear genus. Enriques emphasizes that \(p^{(2)}=p^{(1)}-1\) holds for virtual canonical characters, not necessarily the genus and degree of a moving effective part. The footnote gives Mathematische Annalen volumes 2 and 8, dated 1869 and 1874. Bibliographic references usually date publication 1870 and 1875; earlier dates can reflect writing or submission. Original journal pages were not successfully verified here, so these dates are not silently emended or called a demonstrated mathematical error.

The Ricerche and Introduzione are said to characterize canonical restrictions, subject to an explicit exception and exclusions for proper fundamental curves, then prove birational invariance by special transformations. The exception is not completely specified in this passage, which refers forward to Chapter III. This cannot be replaced by the unrestricted assertion that restriction to one moving curve determines a line bundle on the surface.

The Ricerche date 1893 is defensible: the official collected-works archive lists a Clausen offprint of 1893 and the journal publication in volume 44 in 1894. Its 1896 Introduzione entry is also verified. A blanket “1893 to 1894” correction would erase a real distinction.

The conceptual extension is the canonical class when \(p_g=0\):
\[
C+D'=C'+D,\qquad K=C'-C=D'-D.
\]
Its virtual numerical characters remain defined, and \(sK\) may be effective although \(K\) is not. Plurigenera supply additional *dimensions*; their numerical genus and degree are already polynomials in \(K^2\).

The account locates the Jacobian presentation in the Bologna course of 1897–98, the 1899 published programme, and the 1901 Intorno ai fondamenti della geometria sopra le superficie algebriche. The official archive confirms the programme's 1897–98 title and the paper in Atti of Turin, 37, 19–40. The paper's opening recollection uses a different lecture-year wording; exact chronology should be checked against both originals before settling priority.

Enriques compares Segre's and Bertini's 1894 expositions, citing Segre §75 and Bertini §21(b),(g), and says their proof uses uniqueness of the canonical \(g_{2g-2}^{g-1}\) via curve Riemann–Roch. The mathematical uniqueness is immediate: if \(\deg L=2g-2,h^0(L)=g\), Riemann–Roch yields
\[
h^0(K_C\otimes L^{-1})=1.
\]
A degree-zero line bundle with a nonzero section is trivial; hence \(L\simeq K_C\). The effective-series formulation has \(g\ge1\); on \(\mathbb P^1\) the canonical class is the ineffective \(\mathcal O(-2)\). This proves the comparison's mathematics, but not the universal historical assertion that no other proof was known. The entire Segre and Bertini papers were not independently reread for that priority claim.

The closing references to Enriques–Chisini volume III and Enriques's Bologna memoir of 1914 point to variants of the method. The preference for simplicity is an expository judgment, not an additional theorem.

### Additional deductions and questions supplied in this audit

**Higher-dimensional exponent.** On a smooth \(d\)-fold, the first-jet bundle has rank \(d+1\) and determinant \(\omega_X\otimes L^{d+1}\). A nonzero determinant from \(d+1\) sections has class \(K_X+(d+1)D\), and multiplying all sections by one equation gives that fixed divisor \(d+1\) times. This derives the dimension generalization mentioned on p. 64. Confidence: high, by the exact-sequence calculation.

**The exceptional lattice organizes the formulas.** Total exceptional transforms satisfy \(E_i^*E_j^*=-\delta_{ij}\), while \(K_{X/Y}=\sum E_i^*\). Changing to prime components introduces proximity coefficients such as \(1,2,4\). This unifies genus, degree, and fixed multiplicity and prevents confusing blowup count with visible \((-1)\)-curves. Confidence: high, by blowup induction.

**Canonical self-intersection loses torsion.** A quartic has \(K\sim0\); the tetrahedral sextic normalization has \(K\not\sim0,2K\sim0\). Both have \(K^2=0,p^{(1)}=1\), but different geometric genera and plurigenera. The Picard-group class must be retained before numerical passage. Confidence: high, from the explicit examples.

**The composite assertion requires care.** The double-blowup divisor \(2F+E\) above gives a concrete test for the distinction between “orthogonal” and “nonpositively intersecting” decompositions. It is a counterexample to the literal effective orthogonal formulation, not a counterexample to the numerically 1-connected exceptional criterion. The latter has a complete proof here. Confidence: high under the explicitly stated effective-divisor reading.

**Positive characteristic is a separate extension.** The jet sequence persists, but inseparable maps can have identically zero determinants; the homogeneous calculation also divides by degrees. A direct transfer requires separability and degree qualifications. This limits a proposed extension, not the complex-algebraic original; no unsolved classification problem is asserted.

**Documentary limits.** Direct checks of the printed Enriques–Chisini Book XV location, Franchetta's original 1940–1941 articles, and the complete historical priority comparison remain useful. Unverified bibliographic details do not replace the modern mathematical proofs supplied above, and no unsupported first-repair attribution has been made.


### References and verification: Chapter II

#### Modern references actually checked

Brosnan, P. (n.d.). *UMD 808J: Algebraic surfaces*. University of Maryland. The following author-hosted sections were opened and checked:

- §3.1, “Adjunction,” Proposition 3.1 and Corollary 3.2: [https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0016.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0016.html)
- §3.2, “Riemann–Roch for surfaces,” Theorem 3.4: [https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0017.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0017.html)
- §4.2, “Monoidal transformations on surfaces,” Propositions 4.7, 4.8, 4.10, and 4.11: [https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0028.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0028.html)
- §4.6, “Elimination of indeterminacy”: [https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0035.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0035.html)
- §4.10, “Castelnuovo's contractibility criterion”: [https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0039.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0039.html)
- Bibliography, confirming the Hartshorne and Beauville editions used: [https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0040.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0040.html)

The first three sections were read in detail for the formulas and exact textbook pointers. The last two were checked as the relevant author-hosted theorem sections; the contraction proof used in the commentary was also read in the Stacks Project. The notes contain minor typographic slips in their displayed Riemann–Roch proof, so the commentary derives its formulas independently rather than copying that proof. No date is invented for these notes.

Dolgachev, I. V. (2016). A brief introduction to Enriques surfaces. In *Development of moduli theory—Kyoto 2013* (Advanced Studies in Pure Mathematics, Vol. 69, pp. 1–32). Mathematical Society of Japan. Author preprint, version 2: [https://arxiv.org/abs/1412.7744](https://arxiv.org/abs/1412.7744) ; full text: [https://arxiv.org/pdf/1412.7744](https://arxiv.org/pdf/1412.7744)

Verification: arXiv identifies version 2 as April 11, 2016; the Mathematical Society of Japan contents independently confirms publication in volume 69 (2016), starting at p. 1, with the next article at p. 33: [https://www.mathsoc.jp/assets/pdf/publications/aspm/CFM69.pdf](https://www.mathsoc.jp/assets/pdf/publications/aspm/CFM69.pdf) . Preprint §2, pp. 3–4, was checked for the ordinary double/triple/pinch local models, finite-duality conductor formula, tetrahedral sextic, and nontrivial two-torsion canonical class. The preprint pagination is distinguished from the published page range. This is a mathematical source and a modern exposition, not evidence for historical first-repair attribution. Its old Michigan URL redirected unsuccessfully, so the accessible author-posted arXiv version was used.

Hartshorne, R. (1977). *Algebraic geometry* (Graduate Texts in Mathematics, Vol. 52). Springer.

Exact pointers checked through Brosnan's explicit references: II, Proposition 8.20 (adjunction); V, Theorem 1.6 (surface Riemann–Roch); V, Propositions 3.1–3.4 (point blowup, Picard/intersection decomposition, canonical divisor, and direct images of the structure sheaf). The whole book was not accessed during this audit, and the notation “verified” here means that these statements and numbered cross-references were checked in the author-hosted course notes, not that every original textbook page was inspected.

The Stacks Project Authors. (n.d.). *The Stacks Project*, §18.34, “Finite order differential operators,” Lemma 18.34.6. [https://stacks.math.columbia.edu/tag/09CQ](https://stacks.math.columbia.edu/tag/09CQ)

Verification: the canonical exact sequence of first principal parts is explicitly displayed in Lemma 18.34.6. Applying it to a line bundle on a smooth surface and taking determinants is the commentary's own derivation of the Jacobian class. The section does not itself assert every Enriques-specific geometric interpretation.

The Stacks Project Authors. (n.d.). *The Stacks Project*, §54.16, “Contracting exceptional curves,” especially Lemma 54.16.8 (Tag 0C2M). [https://stacks.math.columbia.edu/tag/0C2I](https://stacks.math.columbia.edu/tag/0C2I) ; [https://stacks.math.columbia.edu/tag/0C2M](https://stacks.math.columbia.edu/tag/0C2M)

Verification: the statement and proof of Lemma 54.16.8 were read. They construct a contraction in the proper/ample setting, retain properness and ampleness downstairs, and invoke the local criterion in Lemma 54.16.4. This supplies an algebraic Castelnuovo contraction theorem for the smooth projective application. No priority claim is attached to this modern presentation.

#### Standard context whose exact theorem numbering was not asserted

Beauville, A. (1996). *Complex algebraic surfaces* (2nd ed.; London Mathematical Society Student Texts, Vol. 34). Cambridge University Press. [https://www.cambridge.org/core/books/complex-algebraic-surfaces/E242F9DDB71DFB9B060ED6311400B5FA](https://www.cambridge.org/core/books/complex-algebraic-surfaces/E242F9DDB71DFB9B060ED6311400B5FA)

Publisher metadata and the edition in Brosnan's bibliography were checked. It is a standard reference for minimal rational/ruled models and the birational classification context. No unverified proposition number is assigned to it. The commentary gives the elementary ruled \(K^2\) computation and distinguishes it from the separate classification input needed for maximality.

Alzati, A., & Tortora, A. (2002). On connected divisors. *Advances in Geometry, 2*(3), 243–258. [https://doi.org/10.1515/advg.2002.012](https://doi.org/10.1515/advg.2002.012)

Author-institution metadata: [https://air.unimi.it/handle/2434/6534](https://air.unimi.it/handle/2434/6534) . The record verifies title, authors, venue, year, page range, and abstract on numerical connectedness. A nonprimary mirror of the full paper was encountered but not used as the proof authority. The fully quantified 1-connectedness definition and blowdown proof in the commentary are supplied explicitly; they are not claimed to be a definition appearing in Enriques's Chapter I. This bibliographic entry is optional background, not a premise for that proof.

#### Historical works cited in Chapter II

The chapter's citations are preserved separately from modern technical references. A title and date copied from Enriques's footnote are not represented as a full independent reading of that work.

Enriques, F. (1893). *Ricerche di geometria sulle superficie algebriche*. Clausen. The official archive lists the 1893 offprint and the journal version separately:

Enriques, F. (1894). Ricerche di geometria sulle superficie algebriche. *Memorie della Reale Accademia delle Scienze di Torino*, series II, *44*, 171–232.

Enriques, F. (1896). Introduzione alla geometria sopra le superficie algebriche. *Memorie della Società Italiana delle Scienze*, series III, *10*, 1–81.

Enriques, F. (1899). Università di Bologna. Programma del corso di Geometria superiore per l'anno 1897–98. *Bollettino di Bibliografia e Storia delle Scienze Matematiche, 2*, 76–78.

Enriques, F. (1901). Intorno ai fondamenti della geometria sopra le superficie algebriche. *Atti della Reale Accademia delle Scienze di Torino, 37*, 19–40.

These records were checked in the official chronological archive: [https://www.federigoenriques.org/indice-cronologico-delle-opere/](https://www.federigoenriques.org/indice-cronologico-delle-opere/) . The 1901 paper is also contained in the collected volume at [https://www.federigoenriques.org/wp-content/uploads/opere/pdf/GM_Enriques_1959_1.pdf](https://www.federigoenriques.org/wp-content/uploads/opere/pdf/GM_Enriques_1959_1.pdf) . The opening lecture-year wording of that paper differs from the book's 1897–98 recollection; this is reported as a documentary issue, not a settled correction of the course date. The archive's 1899 programme title specifically supports 1897–98.

Enriques, F., & Chisini, O. (1915–1934). *Lezioni sulla teoria geometrica delle equazioni e delle funzioni algebriche* (Vols. 1–4). Zanichelli.

Chapter II specifically cites: volume II, Book III, chapter I, §5 for plane and spatial Jacobians (p. 41; p. 47 adds p. 31); “Libro XV, cap. IV, §39, vol. II, pag. 634 e seg.” for osculating rational surfaces (p. 43); and volume III for the curve-theoretic presentation (p. 65). The official archive verifies the four-volume publication series and volume-II date 1918, but the p. 634 passage and the unusual printed Book XV were not checked in the original volume. The scan decisively reads volume II; changing it to III would be an unsupported transcription alteration.

Franchetta, A. (1940). Sulle curve eccezionali riducibili di prima specie. *Bollettino dell'Unione Matematica Italiana*.

Franchetta, A. (1941). Sulla caratterizzazione delle curve eccezionali riducibili di prima specie. *Bollettino dell'Unione Matematica Italiana*.

These are the papers cited on pp. 58 and 60. Original articles were not obtained. Secondary bibliographies conflict on the series-II volume numbers: 2/3 versus 4/5, although they consistently give page ranges 332–341 and 372–375. Accordingly this audit does not manufacture a definitive volume number, theorem number, or attribution of a repaired proof. The canonical-discrepancy rule is proved by blowup induction here; the \(p_g>0\) composite criterion receives an independent modern proof. The broader \(p_g=0\) exclusion is retained as source-cited earlier work.

Castelnuovo, G. (1897). Sul genere lineare di una superficie e sulla classificazione a cui esso dà luogo. *Rendiconti della Reale Accademia dei Lincei*, Vol. VI. Enriques additionally refers to *Memorie scelte*, p. 443.

This citation is copied from the p. 55 footnote; exact original pagination and a complete original reading were not verified. It supports an attribution in the text, not an independent assertion of priority.

Clebsch's 1868 *Comptes rendus* note and Noether's *Mathematische Annalen* papers in volumes 2 and 8 are cited on p. 62. The book prints 1869 and 1874 for Noether; modern bibliographic records commonly give 1870 and 1875. Direct retrieval of the original Noether pages failed. Dates of composition and publication were not conflated, and the footnote was not silently changed.

Segre, C. (1894). Introduzione alla geometria sopra un ente algebrico semplicemente infinito. *Annali di Matematica Pura ed Applicata*, series II, *22*. Chapter II points to §75.

Bertini, E. (1894). La geometria delle serie lineari sopra una curva piana secondo il metodo algebrico. *Annali di Matematica Pura ed Applicata*, series II, *22*. Chapter II points to §21(b),(g).

The book's comparison of these expositions is reported as Enriques's historical claim. Their complete texts were not independently inspected, so no universal priority conclusion is endorsed. The curve Riemann–Roch uniqueness calculation is proved independently in the commentary.

Enriques's 1914 Bologna memoir on invariance of the canonical series is cited on p. 65. The printed abbreviated title is preserved in the source discussion; an exact full bibliographic item was not fabricated.


## Chapter III: Adjoint surfaces

### Scope, notation, and principal findings

The endpoint is the end of §13 on p. 100. This chapter contains thirteen sections, not the beginning of §14. All its pages, including both parts of the footnote running from p. 91 to p. 92, have been compared with the scans. The numbered records III001 onward in the accompanying register distinguish the author's arguments from the modern reconstructions below.

Work over the complex numbers. Let \(X\) be a smooth projective model of the surface \(F\subset\mathbf P^3\), and let \(H\) denote the pullback of a plane section. The source's \(p\) is \(p_g(X)=h^0(X,K_X)\); its bigenus \(P\) is \(P_2(X)=h^0(X,2K_X)\), a vector-space dimension, whereas a system written \(\infty^r\) has projective dimension \(r=h^0-1\). The adjoint of a divisor \(C\) is \(C'=K_X+C\). Thus \(C''=2K_X+C\), while \((2C)'=K_X+2C\): these expressions must not be confused. The characteristic series is the image of the moving system on its general member, with underlying line bundle \(\mathcal O_C(C)\); it need not be a complete series. The “linear genus” of the canonical class on the stated model is
\[
p^{(1)}=p_a(K_X)=1+K_X^2.
\]
Its use requires the model convention: blowing up a smooth point lowers \(K^2\) by one, whereas \(p_g,q\), and all plurigenera remain unchanged. “Equivalent” in the equivalence criteria means linearly equivalent, not merely numerically or algebraically equivalent. The modern identities used throughout are surface Riemann–Roch, Serre duality, and adjunction (Beauville, 1978, I.12–I.16 and III.20).

Three distinctions govern the audit. First, the completeness of a system on \(X\) does not say that its restriction gives every section on a curve. Second, the local number of adjunction conditions need not equal the actual loss of global sections in low degree; Enriques explicitly makes this distinction on p. 74. Third, a reduced exceptional curve, a fundamental cycle, and the divisorial part of the pullback of a maximal ideal are different objects. Confusing them makes the calculations on pp. 83–87 appear more contradictory than they are.

Several important findings concern the printed text rather than its transcription. On pp. 70–71 the characteristic multiple should be \(r-1\), not \(r\), in the discussion of \(K_X+rH\). The two \(C_4\)'s on p. 77 should be \(C_7\). The degree label in the p. 92 footnote should be \(4n-8\) when the surface has degree \(2n\). At the flex in Exercise 2, p. 89, the complete imposed subsystem has dimension four, not three. The trace normalization in §13 does not justify the asserted description of its extra poles. Conversely, the supposed error in the adjunction calculation on p. 80 is entirely generated by the transcription: the scan's two unprimed \(C_1\)'s are correct. The scan also has \(r>1\), not the transcription's \(r\geq1\), in the theorem on p. 72.

### III.1. Adjoint surfaces in ordinary projective space (§1, pp. 67–69)

#### Singular curves, neutral groups, and proper singular points

Enriques begins with a generic \(i\)-fold curve of \(F\). On a model separating its \(i\) local sheets, a point on that curve is represented by a group of \(i\) points. A hyperplane containing the original point contains the entire group and imposes one linear condition, not \(i\) independent conditions. This is the meaning of a neutral group relative to \(|H|\). It is a statement about the image of the chosen linear system, not a claim that distinct points never impose independent conditions on a complete linear system.

A multiple point is called improper when a general plane section constrained to pass through it has the same geometric genus as an unconstrained general section. It is proper when that genus decreases. Ordinary intersections of sheets, such as a triple point of both the surface and its double curve, are the first sort. The words “ordinary” and “general” matter: additional tangencies or singularities of the sheets can create proper singularity data that are invisible in the multiplicity alone.

If an improper point has been replaced by exceptional curves, each connected component of the appropriate exceptional cycle has arithmetic genus zero and meets the residual plane-section system once. The genus-of-a-sum identity
\[
p_a(A+B)=p_a(A)+p_a(B)+A\cdot B-1
\]
explains the absence of a genus loss. Enriques refers back to the theory of exceptional curves from the earlier chapters for contractibility. This is not an assertion that every reduced configuration of rational curves is a single \((-1)\)-curve. A connected configuration can be contracted by a succession of blowdowns, with the relevant multiplicities retained.

#### The sweeping argument

Assume \(F\) is not ruled and its general plane section \(C\) has genus \(\pi>1\). Suppose a curve \(L\) on \(F\) cuts a canonical divisor on every general \(C\). The plane adjunction theorem supplies a curve of degree \(n-3\) through the singularities of the plane curve \(C\), with multiplicity \(i-1\) at an ordinary \(i\)-fold point. That point absorbs \(i(i-1)\) intersections. The remaining intersection divisor has degree \(2\pi-2\). The plane adjoint is unique for the specified residual divisor because its degree is smaller than \(n\).

Enriques fixes a general line \(a\), takes this plane adjoint in each plane through \(a\), and sweeps out a surface of degree \(n-3+h\) having multiplicity \(h\) along \(a\). If \(h>0\), take \(A\in a\cap F\) outside \(L\) and the multiple curve. A suitable plane through \(a\), tangent to the swept surface at \(A\), makes its residual degree-\(n-3\) curve pass through \(A\). The prescribed canonical and singularity intersections already account for the full Bézout number with the section of \(F\); the additional point forces a common component. Since the residual adjoint has smaller degree, that section of \(F\) must be reducible. Varying the generic axis gives a two-dimensional family of such reducible sections. The exclusion of the ruled and Steiner alternatives uses the Kronecker–Castelnuovo classification cited by Enriques through Enriques–Conforto, Book II, Chapter II, §7, p. 273. That classification is assumed, not proved in these pages. The assertion that the plane curves vary algebraically also uses the algebraic dependence of the solutions of their linear equations on the plane; uniqueness on a dense open set supplies a rational family. With these inputs, the sweeping argument identifies an adjoint surface of degree \(n-3\).

The local condition along an ordinary \(i\)-fold curve is multiplicity \(i-1\). The elementary translational model in the footnote explains that condition at a general point of the multiple curve. It does not by itself settle the extra conditions at exceptional points of that curve or at isolated singularities; precisely those questions occupy the subsequent sections.

#### A modern completeness theorem

Here is a modern replacement for the construction, valid without the ruled-surface exclusion. Let \(F\) be a reduced degree-\(n\) hypersurface in \(\mathbf P^3\), and let \(\pi:X\to F\) be a resolution. The adjoint ideal \(\operatorname{adj}(F)\) is defined on an embedded resolution \(\mu:W\to\mathbf P^3\), with smooth strict transform \(\widetilde F\), by
\[
\operatorname{adj}(F)
=\mu_*\mathcal O_W(K_{W/\mathbf P^3}-\mu^*F+\widetilde F).
\]
Ein and Lazarsfeld (1997, Proposition 3.1, p. 254) prove the exact sequence
\[
0\longrightarrow\mathcal O_{\mathbf P^3}(-4)
\longrightarrow\operatorname{adj}(F)(n-4)
\longrightarrow\pi_*\omega_X\longrightarrow0.
\]
Twisting by \(r\), and using \(H^1(\mathbf P^3,\mathcal O(r-4))=0\), gives a surjection
\[
H^0(\mathbf P^3,\operatorname{adj}(F)(n-4+r))
\twoheadrightarrow H^0(X,K_X+rH).
\tag{III.1}
\]
Thus adjoint forms cut the complete system \(|K_X+rH|\); forms differing by the equation of \(F\) times a form of degree \(r-4\) have the same section on \(F\). The proof pushes forward the ordinary adjunction sequence on \(W\); the vanishing of \(R^1\mu_*\omega_W\) is the vanishing input. This is a verified modern theorem and reference, not an assertion that Ein–Lazarsfeld historically corrected this particular paragraph.

If the normalization of \(F\) is smooth, finite-morphism duality describes its canonical sheaf through the conductor. If that normalization still has proper singularities, one must pass on to its resolution: the conductor alone need not impose all adjunction conditions. This is exactly why the first sweeping construction has to be modified at proper multiple points.

The surjectivity in (III.1) concerns sections on \(X\). Restriction to \(C\) is governed by
\[
0\to\omega_X\to\omega_X(C)\to\omega_C\to0,
\]
and its cokernel can involve \(H^1(X,\omega_X)\). No claim that every canonical section on \(C\) extends to \(X\) should be read into Enriques's completeness statement.

### III.2. Arbitrary multiples and canonical surfaces (§2, pp. 69–70)

On a plane section, an adjoint of degree \(n-3+r\) cuts
\[
K_C+rH|_C.
\]
For \(r\geq3\), adding the equation of \(C\) times a form of degree \(r-3\) leaves the residual divisor unchanged. The vector space of these additions has dimension
\[
\binom{r-1}{2}=\frac{(r-1)(r-2)}2.
\]
This explains the loss of uniqueness noted in the text; it is an affine family of representatives of a fixed section. For negative \(r\), Enriques adds an auxiliary surface to reduce to a positive degree and then uses the forced common factor to subtract it. Modern twisting of the adjoint sequence gives the same conclusion directly, with an empty linear system permitted when there are no sections.

For the adjoint of \(rH\), however, the formula is
\[
(rH)'=K_X+rH=H'+(r-1)H.
\]
Consequently its restriction to a general \(H\) is
\[
(K_X+rH)|_H=K_H+(r-1)H|_H.
\tag{III.2}
\]
The printed statement on p. 70 that uses the \(r\)-fold characteristic series alongside \(|(rC)'|\) is off by one. The same mismatch recurs in §3. It is not the earlier plane-curve formula that is wrong: that earlier formula uses degree \(n-3+r\), one higher than the degree \(n-4+r\) of adjoints representing \(K_X+rH\).

At \(r=0\), degree-\(n-4\) adjoint forms represent canonical sections. At \(r=1\), degree-\(n-3\) adjoints represent \(|K_X+H|\). For a smooth hypersurface this is the familiar identity \(K_F=(n-4)H\). The remainder of the chapter explains how singularities change the ideal of admissible numerators.

### III.3. Ruled surfaces (§3, pp. 70–71)

Let \(X=\mathbf P_B(\mathcal E)\) be a smooth ruled model over a curve of genus \(g\), let \(f\) be a ruling fiber, and suppose the chosen hyperplane class \(H\) is a unisection: \(Hf=1\). Then \(K_Xf=-2\). Hence
\[
(K_X+H)f=-1,
\]
so \(|K_X+H|\) is empty: an effective divisor cannot have negative intersection with a general moving fiber.

Nevertheless, a canonical divisor on \(B\), pulled back to \(X\), cuts a canonical divisor on every unisection \(C\simeq B\). For \(g>1\), this consists of \(2g-2\) generators; for \(g=1\) it is the zero divisor. Thus the property of cutting canonical groups on the plane sections does not characterize \(|K_X+H|\) for scrolls. This is a genuine exception to the characterization, not a failure of the completeness theorem (III.1).

Enriques's projective obstruction agrees with the intersection argument. Let \(\Delta\) be the conductor divisor on the smooth normalization of the ordinary scroll. Conductor adjunction gives \(K_X=(n-4)H-\Delta\); intersecting with a general ruling fiber gives \(-2=n-4-\Delta f\), hence \(\Delta f=n-2\). These are the \(n-2\) intersections of a generator with the double curve counted in the source. This is an added proof of a fact Enriques assumes (Dolgachev, 2016, §2, equation (1), gives the conductor formula). A degree-\(n-3\) surface cannot meet the generator at that many points without containing it. Requiring this for every generator forces the whole scroll as a component, which is impossible in the stated degree.

In the convention \(H=\mathcal O_{\mathbf P(\mathcal E)}(1)\), \(H^2=\deg\mathcal E=n\),
\[
K_X=-2H+f^*(K_B+\det\mathcal E),
\qquad K_X+2H=f^*(K_B+\det\mathcal E).
\]
This vertical system cuts the series \(K_C+H|_C\), of degree \(2g-2+n\). More generally, \((K_X+rH)f=r-2\). Therefore the vertical system that merely reproduces the restricted divisors agrees with an adjoint of \(rH\) only for \(r=2\). The printed \(r\)-fold characteristic series must again be replaced by \((r-1)\)-fold in this comparison. For higher \(r\), genuine adjoints have a horizontal part. The chapter states their completeness and postpones its justification; (III.1) supplies it.

### III.4. An invariant characterization of adjoints (§4, pp. 71–72)

The projective construction can be applied to a net represented by planes through a point \(O\) of multiplicity \(s\) on a surface of degree \(m=n+s\). In the scan, \(m>n\) is clear. The adjoint has degree \(m-3\), multiplicity \(i-1\) along an \(i\)-fold curve, and multiplicity \(s-1\) at \(O\); the latter includes the one additional order imposed by taking plane sections through \(O\). These are conditions for the adjoint to the chosen net, not the \(s-2\) condition for canonical adjoints of unrestricted hyperplanes in §6.

Two hypotheses are stated: the relevant net contains no one-dimensional family of reducible curves, and a general member is not itself composite. The theorem then applies to a system of dimension \(r>1\) whose reducible locus has dimension at most \(r-2\). The transcription's \(r\geq1\) is wrong; the strict inequality is visible in the scan. A pencil by itself would be a false extension, since one can add fiber divisors without changing restriction to a general fiber.

Here is a modern justification of the characterization under the stated base-locus and completeness conventions. Choose a general pencil in the parameter space that misses the reducible locus. If \(L\) cuts \(K_C\), the line bundle
\[
M=\mathcal O_X(L-K_X-C)
\]
is trivial on the generic member of that pencil. Resolve the pencil to \(f:\widetilde X\to\mathbf P^1\). A trivialization on its generic fiber gives a rational section of the pullback of \(M\), whose divisor is vertical. Push down to \(X\). Exceptional curves of the resolution disappear; since all the original pencil members are integral, the remaining divisor is an integral sum of pencil members. They are linearly equivalent, so \(M\simeq\mathcal O_X(sC)\). Restriction to \(C\) gives \(sC^2=0\). A noncomposite system of dimension \(>1\) has \(C^2>0\), and therefore \(s=0\).

This proves \(L\sim K_X+C\). Replacing the cut canonical series by its residual to the characteristic series proves the corresponding characterization of canonical divisors. If the chosen system contracts proper curves, vertical correction terms can survive on \(X\); those are precisely the exceptions that subsequent sections analyze. The argument is our modern reconstruction of the logic, not a claim that the text contains this generic-fiber proof.

### III.5. Isolated multiple points (§5, pp. 72–73)

With a proper multiple point present, a curve \(L\) cutting canonical groups on general hyperplane sections still comes from an ambient form satisfying the multiple-curve conditions. Its system can exceed \(|K_X+H|\) by an exceptional divisor \(\theta\), because those general sections do not meet the isolated singular point. The additional point conditions must be determined on a smooth model, rather than inferred from their restrictions alone.

A polar of \(F\) has degree \(n-1\). At an ordinary \(i\)-fold curve its multiplicity is \(i-1\); at an ordinary isolated \(s\)-fold point it has multiplicity \(s-1\). The polar cut omits one exceptional copy from the complete Jacobian divisor at an isolated point. Adding that copy relaxes the numerator condition from \(s-1\) to \(s-2\), the canonical adjunction order. The text explains this geometrically through the Jacobian and later examples; a blowup calculation below verifies it without relying on the picture.

The same order \(s-2\) is a lower bound at a proper \(s\)-fold point lying on the multiple curve, under the genericity stated by Enriques. The multiple-curve conditions and infinitely near singularities may force additional orders. The point multiplicity alone is not a complete classification.

### III.6. Adjoints, subadjoints, and examples (§6, pp. 73–75)

Enriques separates two ideals of conditions. A subadjoint satisfies the generic conditions along multiple curves and cuts the intended groups on general plane sections. An adjoint additionally satisfies the conditions at proper multiple points that are necessary for the resulting differential to extend over a smooth model. This distinction is essential: a general plane misses an isolated point and cannot detect those extra extension conditions.

The number of local linear conditions eventually stabilizes as the ambient degree grows. In modern language, an adjunction ideal of finite colength defines a zero-dimensional quotient, and Serre vanishing makes the global restriction map onto that quotient surjective after a sufficiently positive twist. In small degree the image can be smaller. Enriques explicitly warns of dependence between point conditions and conditions already imposed by the multiple curve or other singularities. The “diminution of genus” is therefore virtual unless independence is checked. It is not an error that later numerical losses are called virtual.

The numerical genus that he anticipates is \(p_a(X)=\chi(\mathcal O_X)-1=p_g-q\) on a smooth surface. For a singular projective hypersurface one must distinguish its arithmetic genus from that of its resolution; the resolution defect is what the local conditions measure in the examples. Surface Riemann–Roch packages these virtual counts, while \(H^1\) records the possible global dependence (Beauville, 1978, I.12–I.13).

#### The order \(s-2\) and its condition count

Suppose the tangent cone of an isolated \(s\)-fold point is smooth. Blow up the point in the ambient smooth threefold. If \(E\) is the exceptional divisor, then
\[
K_W=\mu^*K_{\mathbf P^3}+2E,\qquad
\widetilde F=\mu^*F-sE.
\]
Adjunction on \(\widetilde F\) gives
\[
K_{\widetilde F}=\pi^*K_F+(2-s)E|_{\widetilde F}.
\]
Thus an ambient canonical numerator must vanish to order at least \(s-2\). The number of coefficients of degree \(<s-2\) in three local variables is
\[
\ell\bigl(\mathcal O_{\mathbf A^3,O}/\mathfrak m_O^{s-2}\bigr)
=\binom{s}{3}=\frac{s(s-1)(s-2)}6.
\tag{III.3}
\]
This proves the local count in the ordinary case. A singular tangent cone can require further infinitely near conditions, which are not determined by \(s\) alone.

An ordinary double point imposes no canonical condition. An ordinary triple point imposes one; a quadruple point imposes four. A smooth quartic has \(p_g=1\). A quartic with an ordinary triple point has \(p_g=0\), and is rational by projection from that point: a general line through a point of multiplicity \(n-1\) has one residual intersection. The same argument makes a quintic with an ordinary quadruple point rational. A nodal quartic retains \(p_g=1\).

#### A double line and a triple point on a quintic

For a general quintic with a double line \(a\), canonical adjoints are planes containing \(a\). Their vector dimension is two, so \(p_g=2\), and the residual canonical curves are plane cubics. An additional ordinary triple point \(O\notin a\) imposes the extra condition that the plane contain \(O\), leaving one canonical divisor and \(p_g=1\). The unique plane \(Oa\) has residual intersection three lines; these are exceptional curves on the smooth model.

Enriques verifies the geometry by using quadrics through \(a\) and \(O\), obtaining a degree-eight genus-five surface in \(\mathbf P^5\), and reversing the projection from a line through three points of a plane cubic. The following intersection calculation makes the construction transparent. Let \(S\) be a smooth K3 surface with a very ample divisor \(A\), \(A^2=8\), and an elliptic plane cubic \(E\), \(AE=3\), \(E^2=0\). Blow up three distinct collinear points \(P_i\) of \(E\), with exceptional curves \(e_i\), and set
\[
H=A-e_1-e_2-e_3.
\]
Then \(H^2=5\), \(K_X=e_1+e_2+e_3\), \(H K_X=3\), and \(p_a(H)=5\). The strict transform \(E'=E-\sum e_i\) has \(H E'=0\), \(E'^2=-3\), and genus one. Each \(e_i\) has image degree one. Because the three points are collinear in the degree-eight embedding, hyperplanes through them impose only two independent conditions on \(H^0(A)\), leaving four sections. Under the genericity assumptions in the construction this gives the quintic model, contracts \(E'\) to the triple point, and realizes the canonical divisor as the three exceptional lines.

The genus-five K3 surface containing this plane elliptic cubic is a special, trigonal model; one must not automatically describe it as a complete intersection of three quadrics. Beauville (1978, VIII, Exercise 11) explicitly distinguishes this situation. The genus and intersection computations above verify the claimed birational model numerically; the particular ordinary-singularity presentation still uses the generic projection assumptions of Enriques's construction.

### III.7. First-species singularities, tacnodes, and oscnodes (§7, pp. 76–77)

A proper singular point is of first species when, after removing its first exceptional cycle from the hyperplane system, no further proper fundamental curve remains. The plane-section test is then sufficient: an adjoint numerator, together with one line through the point in the section plane, must be a plane adjoint to the constrained section. Enriques proves this by §4 under the no-pencil-of-reducibles hypothesis. Where that hypothesis fails for plane sections, he directs the reader to use intersections with sufficiently high-degree surfaces instead.

A tacnode has general plane sections with two consecutive double points; an oscnode has three. The text obtains:

| Singularity | Canonical numerator condition | Virtual loss of \(p_g\) |
|---|---|---:|
| First-species tacnode | Pass through the point | 1 |
| First-species oscnode | Pass through the point and have the prescribed tangent plane | 3 |

Here “have the prescribed tangent plane” means that the linear term is a multiple of the linear equation of that plane. It gives three conditions in the local three-variable ring: one constant coefficient and two tangential linear coefficients.

For explicit modern checks, take \(z^2+f_4(x,y)+\cdots=0\), with \(f_4\) a product of four distinct linear factors. The weighted blowup of weights \((1,1,2)\) has discrepancy \(-1\); its exceptional curve is the genus-one double cover of \(\mathbf P^1\) branched at four points and has square \(-2\). The canonical ideal is \((x,y,z)\). For \(z^2+f_6(x,y)+\cdots=0\), weights \((1,1,3)\) give discrepancy \(-2\), an exceptional curve of genus two and square \(-2\), and ideal \((x^2,xy,y^2,z)\). These calculations prove the stated local counts for these ordinary models. They do not equate all singularities sharing a coarse plane-section description.

#### The tacnodal quintic and its quartic model

For the quintic with a double line and a tacnode off the line, the unique canonical plane through both contains, residually, a conic and a line tangent at the tacnode. The conic and line are exceptional in the map to a smooth quartic K3 surface containing a line \(a'\).

On that quartic let \(H\) be a hyperplane section and \(E=H-a'\) the elliptic cubic pencil. Then
\[
H^2=4,\quad E^2=0,\quad HE=3,\quad
D=2H-a'=H+E,\quad D^2=10,\quad p_a(D)=6.
\]
The system \(|D|\) has seven sections. At a general \(P\in E\), imposing a double point removes three independent first-jet conditions, leaving four sections. On \(E\), the remaining divisor has degree \(3-2=1\), so there is an automatic residual base point \(B\) with \(2P+B\sim H|_E\). For general \(P\), \(B\ne P\). Blowing up \(P,B\) gives
\[
\widetilde D=D-2e_P-e_B,\quad
\widetilde D^2=5,\quad
K_X=e_P+e_B,\quad K_X\widetilde D=3.
\]
The strict transform \(E'=E-e_P-e_B\) has square \(-2\), genus one, and zero intersection with \(\widetilde D\). The two exceptional curves have image degrees two and one. This checks the quintic, the tacnode, and the canonical conic-plus-line description.

The two printed references to \(C_4\) in the inverse construction are wrong: these are the degree-seven curves \(C_7\) cut residually by quadrics through \(a'\). The scan confirms \(C_4\); this is an author's misprint, not an OCR error. The dimension calculation and the automatic base point are correct. The more special case \(B=P\), namely a flex, is relevant to the correction in Exercise 2 below.

### III.8. Double planes and infinitely near branch points (§8, pp. 77–79)

A double plane has function field \(\mathbf C(x,y)(\sqrt f)\). Replacing \(f\) by \(f g^2\) does not change that field. A branch curve of odd affine degree must be completed by the line at infinity; in projective language the branch divisor has even degree \(2n\).

Enriques uses the ordinary projective closure of \(z^2=f_{2n}(x,y)\), of degree \(2n\). Its point at infinity on the \(z\)-axis has multiplicity \(2n-2\). A general plane through the axis gives a hyperelliptic curve of genus \(n-1\). The plane-curve arithmetic genus is \((2n-1)(n-1)\), so the total delta contribution at infinity is \(2(n-1)^2\). The initial multiplicity contributes \((n-1)(2n-3)\), leaving \(n-1\) double-point contributions infinitely near. This is the source's count. Its ambient canonical numerator factors as the infinity-plane equation to power \(n-1\), times a degree-\(n-3\) form; the factor accounts for exceptional intersections at infinity.

#### Intrinsic double-cover formulas

Let \(f:S\to Y\) be a smooth double cover with branch \(B\in|2L|\). Directly from the algebra \(\mathcal O_Y\oplus L^{-1}\) and the ramification formula,
\[
f_*\mathcal O_S=\mathcal O_Y\oplus L^{-1},\qquad
K_S=f^*(K_Y+L).
\]
The projection formula then gives
\[
H^0(S,mK_S)=H^0(Y,mK_Y+mL)
\oplus H^0(Y,mK_Y+(m-1)L).
\tag{III.4}
\]
These basic identities are stated in Calabri and Ferraro (2002, §3, equations (3.2)–(3.3)); their §14 applies the same decomposition to pluricanonical conditions. For a smooth branch curve of degree \(2n\) in \(\mathbf P^2\), they yield, by direct substitution,
\[
p_g=\binom{n-1}{2},\quad q=0,\quad K_S^2=2(n-3)^2,
\]
with \(h^0(\mathcal O(d))=0\) for \(d<0\). Canonical divisors are represented by degree-\(n-3\) plane curves because the second canonical summand is \(H^0(K_{\mathbf P^2})=0\). For bicanonical divisors the second summand can be nonzero; this is the point of the footnote on pp. 91–92.

#### The branch blowup rule and unloading

Blow up a point of multiplicity \(m\) in the current branch divisor, put \(r=\lfloor m/2\rfloor\), and let \(E\) be the new exceptional curve. Normalize the pulled-back double cover. Its branch divisor and half-branch class are
\[
B'=\widetilde B+(m\bmod2)E,\qquad
L'=\sigma^*L-rE.
\]
Thus
\[
K_{Y'}+L'=\sigma^*(K_Y+L)-(r-1)E.
\tag{III.5}
\]
An even point of multiplicity \(2i\) imposes multiplicity \(i-1\) on the canonical plane numerator. An odd point of multiplicity \(2i+1\) has the same first correction, but the exceptional curve is itself branch; consequently a following point must be tested against the transformed branch divisor including that exceptional component. This is why replacing an odd cluster by a list of independent ordinary multiplicities would be wrong.

For two successive odd points \([2i+1,2i+1]\), the initial formal multiplicities \((i-1,i)\) violate proximity. Subtracting the forced exceptional component, or “unloading,” replaces them by \((i,i-1)\). In particular a \([3,3]\) branch point imposes one ordinary base point on the degree-\(n-3\) canonical curves. A branch point of multiplicity \(2i\), or \(2i+1\) without further nonnegligible infinitely near data, contributes \(i(i-1)/2\) to the virtual genus loss.

For completeness, the Euler-characteristic calculation underlying the count is short. From \(f_*\mathcal O_S\) and Riemann–Roch,
\[
\chi(\mathcal O_S)=2\chi(\mathcal O_Y)+\tfrac12 L(L+K_Y).
\]
Substitute \(L'=\sigma^*L-rE\), \(K_{Y'}=\sigma^*K_Y+E\), \(E^2=-1\). The loss is \(r(r-1)/2\). Similarly \(K^2\) drops by \(2(r-1)^2\) before any exceptional \((-1)\)-curves of the covering surface are contracted. This is a local virtual calculation; global dependencies remain as in §5.

Enriques mentions Clebsch, Noether, De Paolis, Bertini, and his own 1896 memoir for the historical double-plane theory. The Clebsch date printed as 1861 is erroneous: the identified paper is in volume 3, pp. 45–75; the publisher dates the issue to 1870, while bound-volume citations commonly give 1871. The other historical references are recorded as citations used by Enriques, not as papers whose full proofs have all been independently inspected in this audit.

### III.9. The numerical bound for an irreducible fundamental curve (§9, pp. 80–82)

Let \(E=\theta\) be an irreducible first-species fundamental curve with \(p_a(E)=\rho\), \(E^2=-s<0\), and \(H E=0\). Write \(H=C_1+E\). Then \(C_1E=s\). Since \(C'=K_X+H\) and \(E'=K_X+E\),
\[
C'=C_1+E',\qquad
E C'=E C_1+E E'=s+2\rho-2.
\]
Both \(C_1\)'s are unprimed in the scan. The transcription inserts a prime into the second line and then proposes an incorrect correction to the first. No correction to Enriques's adjunction identity is needed.

If the subadjoint system extends \(|C'|\) by \(xE\), and \(E\) is not to remain a forced fixed component in the enlarged system, a necessary condition is
\[
(C'+xE)E=2\rho-2-(x-1)s\geq0,
\qquad
x\leq1+\frac{2\rho-2}{s}.
\tag{III.6}
\]
The preceding prose says the extension stops when intersection becomes “zero or negative,” whereas the displayed inequality correctly permits zero. Degree zero is the boundary case: a nontrivial degree-zero line bundle has no sections; the trivial one has one. Read the prose as a warning about that boundary, not as a strict inequality.

The exact sequence for adding the \(x\)-th copy is
\[
0\to\mathcal O_X(C'+(x-1)E)
\to\mathcal O_X(C'+xE)
\to\mathcal O_E(K_E+(x-1)E)\to0.
\tag{III.7}
\]
This gives two possible obstructions beyond the degree bound: the line bundle on \(E\) may have no section, and a section may fail to lift because of \(H^1\) on \(X\). Sufficient positivity in the external hyperplane twist removes the latter obstruction, not the former. Enriques explicitly demonstrates that the numerical bound need not be attained; there is no missing assertion of universal sufficiency.

For \(\rho=0\), a proper first-species exceptional curve has \(s\geq2\), so (III.6) forces \(x=0\). Such rational singularities impose no canonical correction. For \(\rho=1\), the first boundary bundle is \(K_E\simeq\mathcal O_E\), giving the familiar one-condition correction. The tacnode has \((\rho,s)=(1,2)\). The oscnode has \((2,2)\), permits \(x=2\), and contributes three canonical conditions, as already computed.

Enriques's counterexample to attaining the upper bound is particularly instructive. An ordinary sextuple tangent cone with six nodes has normalization of genus \(10-6=4\). The six nodes correspond to six branches of the surface's double curve. Here \(s=6\), so (III.6) permits \(x=2\). Let \(h\) be the plane-section divisor on the normalized sextic, and let \(\Delta\) be the twelve preimages of its six nodes. Then
\[
K_E=3h-\Delta,\qquad
\mathcal O_E(E)=\mathcal O_E(-h),\qquad
K_E+E=2h-\Delta.
\]
This last bundle has degree zero. It is trivial exactly when a conic passes through the six nodes. For general six nodes there is no such conic. Hence the last possible numerical enlargement does not occur: the subadjoint has order three at the point, whereas the adjoint has order four, so only one copy is added. This supplies a precise line-bundle explanation of the source's geometric example.

### III.10. Higher-species singularities and the exercises (§10, pp. 82–89)

#### Successive fundamental cycles

Enriques defines higher species inductively: after the first fundamental part is removed, a further fundamental part remains for the residual system. His descriptions of connectedness and monovalence concern the successive systems, not just the unweighted support of an exceptional divisor. The conditions on sections must therefore be computed with the actual multiplicities and proximity relations.

On a modern resolution there are at least three relevant objects: the reduced exceptional divisor, the smallest positive exceptional cycle with nonpositive intersection with every exceptional component, and the fiber cycle defined by the divisorial part of the pulled-back maximal ideal. They can differ. Calabri and Ferraro (2002, Theorem 9.7 and §§10–11) explicitly compute the fiber and fundamental cycles for double points. Their distinction provides a precise framework for the source's successive-removal procedure; it does not make the historical word “fundamental curve” automatically synonymous with one modern cycle.

#### A uniplanar double point and the cubic-surface calculation

An ordinary uniplanar double point has a double tangent plane and three exceptional tangent directions. A local model is
\[
z^2+xy(x+y)=0,
\]
a rational double point of type \(D_4\). Its minimal resolution has a central rational curve \(E_0\) and three arms \(E_1,E_2,E_3\), all of square \(-2\), with \(E_0E_i=1\) and pairwise disjoint arms. The maximal-ideal cycle is
\[
Z=2E_0+E_1+E_2+E_3,\qquad Z^2=-2,\qquad p_a(Z)=0.
\]
The exceptional intersection matrix is negative definite, and \(K_XE_i=0\) for all four components by adjunction. The resolution is crepant, so the point imposes no canonical adjunction condition.

Enriques checks the configuration using a rational cubic surface represented by plane cubics through six points, three collinear and three infinitely near. A quartic de Jonquières transformation of type \((4;3,1^6)\) changes the hyperplane system to
\[
D=9h-6p-3(a_1+a_2+a_3)-2(b_1+b_2+b_3)-(o_1+o_2+o_3).
\]
All the letters on the right denote total-transform classes on the blown-up plane. Direct calculation gives
\[
D^2=81-36-27-12-3=3,\qquad K_XD=-27+6+9+6+3=-3,
\]
so \(p_a(D)=1\), as required for a cubic surface.

The central line has class \(E_0=h-a_1-a_2-a_3\); the arms have \(E_i=h-p-b_i-o_i\). Their weighted sum is
\[
Z=5h-3p-2\sum a_i-\sum b_i-\sum o_i.
\]
Hence
\[
D-Z=4h-3p-\sum a_i-\sum b_i.
\]
This residual system has square one and arithmetic genus zero. It meets \(E_0\) once and is orthogonal to the three arms. This verifies both the stated quartic residual system and the continued fundamentality of the arms. In the source \(\theta_0\) already denotes the central line counted twice in the relevant cycle; omitting that weight would produce a false degree calculation.

#### The Noether double point with an infinitely near tacnode

For the next singularity, a convenient local model is
\[
z^2+x^3+y^6=0.
\tag{III.8}
\]
Its plane branch curve has three smooth branches with common tangent and distinct second-order terms, hence a \([3,3]\) cluster. The weights \((2,1,3)\) give weighted degree six and discrepancy \(-1\). Its minimal resolution has one elliptic exceptional curve \(E\) of square \(-1\). A canonical numerator must lie in the maximal ideal, so the local canonical loss is one.

The arithmetic of pp. 85–87 is most clearly checked on two explicitly different models. On the minimal resolution, a hyperplane pullback \(H\) has \(HE=0\), while \((H-E)E=1\). A degree-one line bundle on an elliptic curve has one section, so this intersection is a fixed point of the residual system. Thus
\[
(H-E)^2=H^2-1,
\]
but after removing that remaining simple base point the effective moving degree is \(H^2-2\). This is the distinction between virtual and effective degree that Enriques explicitly makes on p. 86.

Blow up that fixed point. Let \(E_0\) be the new rational exceptional curve and \(E_1\) the strict transform of \(E\). Then
\[
E_0^2=-1,\quad E_1^2=-2,\quad E_0E_1=1.
\]
The reduced total transform \(E_0+E_1\) has genus one and square \(-1\). The maximal-ideal cycle of the original double point is instead
\[
Z=2E_0+E_1,\qquad Z^2=-2,\qquad p_a(Z)=0.
\]
Removing this cycle accounts for the first genus drop of one; a subsequent removal associated with \(E_1\) accounts for the tacnodal drop of two. Contracting \(E_0\) restores the elliptic curve of square \(-1\).

This bookkeeping explains the intended conclusion without endorsing every intermediate use of \(\theta\) as literally the same divisor on the same surface. The source passes between a model with a remaining base point and one where it is separated, and between reduced and weighted neighborhoods. Those changes are not made explicit enough for a modern proof. There is also a genuine sign inconsistency: \(\nu\) is introduced as the signed square \(-1\), but p. 87 occasionally writes “degree \(-\nu\)” and \(-\nu=-\nu_0-\nu_1+2=-1\). Retain \(\nu=E^2=-1\), and take \(\nu_i=-E_i^2>0\); then the left side of the latter identity is \(\nu\), not \(-\nu\). The prime after \((\pi-1)\) in the scan has no mathematical role and should be treated as a stray printed mark.

The two rational quartic models cited from Noether are numerically consistent:
\[
(7;3,2^9),\qquad (9;3^8,2,1).
\]
In either case \(D^2=4\), \(K_XD=0\), and \(p_a(D)=3\). The cubic through the ten specified base points has genus one, square \(-1\), and zero intersection with \(D\). Its intersection with \(D-E\) is one, but that one point is fixed. Thus the statement that it is still fundamental for the residual system means there are no variable intersections; it does not assert that the intersection number remains zero. In the second model, the source itself explains that the tacnodal plane contains the original point and forces splitting of certain plane sections; using a more positive system removes that projective complication.

The reference to Pedoe (1937) is bibliographically verified, including its abstract concerning accidental base points in canonical systems. The full article was not available in the inspected publisher record, so the particular local assertion attributed to it is not presented as independently checked from that paper.

#### The double-plane verification

For a double plane branched in degree \(2n\), the pullback of a general conic has genus \(2n-1\), by Riemann–Hurwitz with \(4n\) branch points. A conic through the first point of a \([3,3]\) cluster removes two branch contributions modulo parity, lowering the genus by one; imposing the prescribed infinitely near condition produces a further loss of two. This matches the double point followed by a tacnode. The canonical cluster condition is a single base point, so the virtual canonical loss is one.

The two quartic rational examples project to sextic double planes with, respectively, an ordinary quadruple branch point and a \([3,3]\) branch point. Each imposes one condition on canonical plane constants, leaving no canonical section. These are consistency checks of the already constructed rational models; \(p_g=0\) alone would not prove rationality.

#### Exercise 1: two infinitely near triple points

Each ordinary triple point gives one canonical condition. For two successive triple points, these are a simple point and the prescribed infinitely near simple point; their local cluster has length two. For a quintic with a double line \(a\), the space of canonical planes through \(a\) has vector dimension two. Assuming the specified cluster is in the stated general position off \(a\), the two conditions remove both sections, giving \(p_g=0\).

Let \(\ell=OO_1\) denote the line in the prescribed tangent direction. If it were not contained in the quintic, its intersection multiplicity at the two successive triple points would be at least six, exceeding five. Hence \(\ell\subset F_5\). Planes through \(\ell\) have residual quartics. Their plane arithmetic genus is three; the double-line intersection contributes one node and the cluster contributes the other two double-point losses. The general residual quartic is rational. For a complete modern proof of rationality from this pencil, resolve its base points. The smooth generic fiber over \(\mathbf C(t)\) has genus zero, hence is a conic via its anticanonical system. Tsen’s theorem gives it a \(\mathbf C(t)\)-point, so it is \(\mathbf P^1_{\mathbf C(t)}\) and the surface function field is \(\mathbf C(t,u)\). This proves rationality independently of the unspecified spatial transformation (Stacks Project, Theorem59.67.10, Tag03RD).

The quadratic spatial transformation cited in the exercise has base the double line and three points of the surface, including \(O,O_1\). Under the genericity assumptions of that transformation, the image is a quartic with a double line, which is a standard rational model. The text does not write coordinates for the transformation; the genus calculation, line containment, and rational pencil above give the requested substantive verification without pretending that its full base scheme was displayed.

#### Exercise 2: a flex imposes one dependent triple-point condition

This exercise contains a substantive dimension issue. Let \(S\subset\mathbf P^3\) be a smooth quartic containing a line \(a\), let \(H\) be its hyperplane class, and let \(E=H-a\) be the elliptic cubic pencil. Set \(D=H+2E\). Then
\[
D^2=16,\qquad p_a(D)=9,\qquad h^0(S,D)=10.
\]
These agree with the source. Let \(P\in E\) be a flex of the plane cubic \(E\), and blow it up, with exceptional curve \(e\). Put
\[
A=\pi^*D-3e,\qquad E'=\pi^*E-e,\qquad
B=A-E'=\pi^*(H+E)-2e.
\]
The numerical assertions also agree:
\[
A^2=7,\quad K_XA=3,\quad p_a(A)=6,\quad
E'^2=-1,\quad AE'=0.
\tag{III.9}
\]

But the dimension of the complete imposed subsystem is four, not three. Here is a proof that also explains the dependence. The pencil \(|E|\) is globally generated and \(H\) is very ample, so \(H+E\) is very ample. It has \(h^0=7\), and its first-jet evaluation at \(P\) is surjective. Therefore
\[
h^0(X,B)=7-3=4.
\]
Riemann–Roch on \(X\) gives \(\chi(B)=4\), while \(h^2(B)=0\), so \(h^1(B)=0\). Since \(P\) is a flex,
\[
A|_{E'}\simeq H|_E(-3P)\simeq\mathcal O_E.
\]
The exact sequence
\[
0\to B\to A\to\mathcal O_{E'}\to0
\]
then gives
\[
h^0(X,A)=5,\qquad \dim|A|=4.
\tag{III.10}
\]
Equivalently, \(\chi(A)=4\) and \(h^1(A)=1\). The flex is exactly the reason that the six nominal triple-point conditions have rank five. If \(P\) is not a flex, \(A|_{E'}\) is a nontrivial degree-zero bundle, all four remaining sections contain \(E'\), and it is a fixed component rather than the intended contracted curve.

The source does not literally say “complete” in its last sentence. Nevertheless, “the system obtained by imposing a triple point” on the previously specified complete \(\infty^9\) naturally denotes the full imposed subsystem, and that reading requires \(\infty^4\). A specified projective three-dimensional subsystem does recover the claimed projective model. The following construction is our reconstruction; the projection choice and additional generic hypotheses are not written in the exercise.

##### A complete construction of the special subsystem

Assume \(E_0\) is a smooth fiber, \(P\in E_0\setminus a\) is its flex, the tangent plane has contact exactly two with \(S\) at \(P\), and \(S\) contains no line other than \(a\). The condition \(P\notin a\) is printed in the source. The last two are additional general-position hypotheses used for this construction. They hold for general input: imposing another line on a quartic containing \(a\) gives incidence dimensions at most \(24+4=28\) for a disjoint line or \(25+3=28\) for an intersecting one, inside the projective space of dimension 29 of quartics through \(a\). Exact tangent contact two is also available. In the equation \(gC+hT\) used below, keep \(C\) fixed and vary the coefficient \(\beta\) of \(-g^2l\) in \(T\). This changes the quadratic term \(\beta Ux\), while preserving \(a\), \(E_0\), and its flex; choose a smooth general quartic with \(\beta\ne0\). Global generation and the local elliptic calculation below do not require these last two hypotheses.

Choose hyperplane forms \(g,h,l,t\), with \(a=(g=h=0)\), \(h=0\) cutting \(a+E_0\), \(g(P)\ne0\), \(t=0\) the tangent plane, and \(l(P)=0\) a local parameter along \(E_0\). If \(s_a\) cuts out \(a\), put \(u=h/s_a\), \(v=g/s_a\); these generate \(H^0(E)\). Near \(P\) use
\[
U=u/v=h/g,\qquad x=l/g,\qquad w=t/g.
\]
The flex condition gives
\[
w=\alpha U^2+\beta Ux+O(3),\qquad
\operatorname{ord}_x w(0,x)=3.
\]
The seven sections of \(H+E\), in this local trivialization, are
\[
1,\ U,\ x,\ U^2,\ Ux,\ w,\ Uw.
\]
Thus \(B=H+E-2e\) has basis \(U^2,Ux,w,Uw\), represented globally by \(hu,lu,tv,tu\). Away from \(P\), their common vanishing is impossible: if \(u\ne0\), it forces \(h=l=t=0\), whose only ambient point is \(P\); if \(u=0\), it forces \(t=0\) on \(E_0\), whose intersection with the tangent plane is \(3P\). On \(e\), the initial quadrics span \(U^2,Ux\), with the single common zero \(E'\cap e=[0:1]\). Hence \(|B|\) has just that base point. The established surjection \(H^0(A)\to H^0(\mathcal O_{E'})\), together with \(E'+|B|\subset|A|\), removes it and proves that \(|A|\) is globally generated.

Set \(M=A-E=H+E-3e\). The unique tangent-plane section gives \(h^0(H-2e)=1\); Riemann–Roch gives \(h^1(H-2e)=0\). Since \(M=(H-2e)+E'\) and \(M|_{E'}=\mathcal O_{E'}\), one obtains \(h^0(M)=2\). The pencil trick identifies the kernel of
\[
H^0(M)\otimes H^0(E)\longrightarrow H^0(A)
\]
with \(H^0(H-3e)\). Exact tangent contact two makes this kernel zero. Choose bases \(m_0,m_1\) of \(H^0(M)\) and \(u,v\) of \(H^0(E)\), and a fifth section \(r\). The complete map has image
\[
Y\subset Q:\ z_{00}z_{11}-z_{01}z_{10}=0\subset\mathbf P^4,
\]
where
\[
(z_{00},z_{01},z_{10},z_{11},z_4)
=(m_0u,m_0v,m_1u,m_1v,r).
\]
The quadric has rank four. Since \(A^2=7\) and the image is nondegenerate, the map is birational and \(\deg Y=7\).

The pencil \(|M|\) has no fixed curve. Its local generators are \(Uw\) and \(w-\alpha U^2-\beta Ux\). The restriction to \(E'\) excludes \(E'\) as a fixed component, and the exact order three of \(Uw\) excludes \(e\). Any other possible fixed curve would be the line \(t=\alpha h+\beta l=0\), excluded by the hypothesis on lines. Because \(M^2=1\), its base scheme consists of one reduced point, disjoint from \(E'\). Blow up that point. The exceptional curve is a section of the resulting pencil, so the general fiber is connected; Bertini gives a smooth irreducible member of genus three. Its image is a plane quartic, since \(AM=4\); birationality on a general member and the equality of its genus with the plane-quartic arithmetic genus three show that this plane image is smooth. A general \(E\)-fiber maps to a smooth plane cubic: \(AE=3\), and \(h^0(A)-h^0(M)=3\) supplies the complete degree-three series.

Choose general members \(M_1=(m_1=0)\), \(E_1=(v=0)\) whose ruling planes avoid \(q=\varphi_A(E')\). Those planes are
\[
\Pi_4=(z_{10}=z_{11}=0),\qquad
\Pi_3=(z_{01}=z_{11}=0).
\]
Choose \(R=(1,0,0,0,\lambda)\) on their common generator, outside \(Y\) and outside the quadric vertex. The required subsystem is now explicit:
\[
V_R=\langle m_0v,\ m_1u,\ m_1v,\ r-\lambda m_0u\rangle.
\]
It has vector dimension four and is base-point-free because \(R\notin Y\). In target coordinates \([X:Y:Z:W]\), after shifting the fifth coordinate by \(\lambda z_{00}\), the inverse of projection on \(Q\) is
\[
[X:Y:Z:W]\dashmapsto[XY:XZ:YZ:Z^2:WZ].
\]
Projection is therefore birational. It contracts \(\Pi_4\) to \(L_4=(Y=Z=0)\) and \(\Pi_3\) to \(L_3=(X=Z=0)\). Their curves map onto these lines with degrees four and three.

These are the actual generic sheet multiplicities. Near a general point of \(L_4\), use \(X=1\) and coordinates \((\tau,\rho,w)\) on \(Q\) with
\[
z_{00}=\tau,\quad z_{01}=1,\quad z_{11}=\rho,\quad
z_{10}=\tau\rho.
\]
Projection is \((\tau,\rho,w)\mapsto(y=\tau\rho,z=\rho,w)\). The plane quartic meets a general projection fiber in four distinct points \(\tau_i\); each local sheet becomes \(y=z\tau_i(z,w)\). Their tangent planes are distinct. Thus \(L_4\) is an ordinary quadruple line at its general point; the same calculation gives the ordinary triple line \(L_3\).

A general plane section has normalization of genus six and already has delta contribution \(6+3=9\) from those two lines, accounting for the whole difference \(15-6\). Hence no further singular curve occurs. Nor does \(A\) contract another curve: for an irreducible \(C\ne E_0\), with \(m=\operatorname{mult}_P C\), one has \(EC\ge m\) and \(HC\ge m\); equality \(AC=0\) forces \(HC=m\), which makes \(C\) a line through \(P\), excluded by hypothesis. Also \(Ae=3\). Away from the two multiple lines and the image of \(E'\), the proper birational map is finite onto a normal hypersurface and hence an isomorphism. The remaining isolated singularity is checked directly next.

##### The double point and its infinitely near tacnode

Write the original quartic equation as
\[
gC(g,l,t)+hT(g,h,l,t)=0,
\]
where the smooth cubic \(E_0\) and its flex allow
\[
C=g^2t+c_1glt+c_2gt^2+\kappa l^3+c_3l^2t+c_4lt^2+c_5t^3,
\quad\kappa\ne0,
\]
and
\[
T=-\alpha g^2h-\beta g^2l+\gamma g^2t+gQ_2(h,l,t)+Q_3(h,l,t).
\]
Here \(Q_2,Q_3\) are homogeneous forms of degrees two and three. A convenient basis for the five sections of \(A\), expressed as local ratios, is
\[
[a_0:b_0:c_0:d_0:f_0]
=[U^3:U^2x:Uw:U^2w:w-\alpha U^2-\beta Ux].
\]
These coordinates satisfy
\[
d_0f_0=c_0(c_0-\alpha a_0-\beta b_0),\qquad
q=[0:0:0:0:1].
\]
On \(f_0=1\), write \(a,b,c\) for the first three coordinates and \(s=c-\alpha a-\beta b\). Then \(d=cs\), and the inverse coordinates on the quartic are
\[
[g:h:l:t]=[a:as:bs:cs^2].
\]
Substituting into the quartic and dividing out the factor \(as^3\) gives the image equation
\[
\begin{aligned}
\Phi={}&a^2+c_1abc+c_2ac^2s+\kappa b^3+c_3b^2cs
+c_4bc^2s^2+c_5c^3s^3\\
&+\gamma a^2c+aQ_2(a,b,cs)+sQ_3(a,b,cs)=0.
\end{aligned}
\]
For weights \((a,b,c)=(3,2,1)\), its initial form is
\[
\Phi_6=a^2+c_1abc+c_2ac^3+\kappa b^3
+c_3b^2c^2+c_4bc^4+c_5c^6.
\]
Every omitted term has weight at least seven. The weighted projective curve \(\Phi_6=0\) is the smooth \(E_0\), via \([g:l:t]=[a:bc:c^3]\). Its cone has an isolated critical point. Consequently \(\Phi=0\) is an isolated normal double hypersurface germ. The first four sections vanish precisely along \(E'\), so its exceptional fiber is the single elliptic curve \(E'\), with square \(-1\).

Blow up this double point in the \(c\)-chart, \(a=cz,b=cy\). Analytic completion of the square gives
\[
\begin{aligned}
Z^2+c\bigl[\kappa y^3
+(c_3-c_1^2/4)cy^2
+(c_4-c_1c_2/2)c^2y
+(c_5-c_2^2/4)c^3\bigr]
+\text{terms of degree at least five}=0.
\end{aligned}
\]
Terms of original weight at least seven contribute order at least five to this branch equation: the critical value of \(z\) has order at least two, so an original monomial of weight \(w\) contributes order at least \(w-2\) after division by \(c^2\). The displayed binary quartic has four distinct linear factors: its cubic factor has distinct roots because \(E_0\) is smooth, and \(\kappa\ne0\) separates the factor \(c\). This is the ordinary tacnode of the source. It is the unique singular point on the first exceptional line; the other charts are smooth there. The chosen projection is an isomorphism near \(q\), because \(q\) belongs to neither contracted ruling plane. Thus the septimic has exactly the stated double point with an infinitely near tacnode, under the explicit generic hypotheses.

##### The adjoint cubic

Let \(\Pi_0=(Z=0)\), the plane containing both multiple lines, and let \(\Pi_q\) be the plane through \(L_4\) and \(q\). On \(X\) their pullbacks are \(M_1+E_1\) and \(M_1+E'+e\). Hence
\[
\operatorname{div}(\Pi_0^2\Pi_q)=3M_1+2E_1+E'+e.
\]
Removing conductor orders three and two along the ordinary multiple lines and the elliptic adjoint correction \(E'\) leaves \(K_X=e\). This proves the asserted adjoint cubic. Equivalently, the cubic forms in \((Y,Z)^3\cap(X,Z)^2\) are \(Z^2(aY+bZ)\), and passing through \(q\) fixes their ratio. Its residual curve is the plane cubic image of \(e\), whose degree is \(Ae=3\). It is rational, with a cusp at \(q\), as the exceptional-curve parametrization \([U^3:U^2x:f_3(U,x)]\) shows.

If tangent contact at \(P\) is at least three, \(\alpha=\beta=0\) and the quadric drops to rank three. The dimension correction remains valid, but this proof does not assert the same two-line presentation in that special case.

The inverse requested by the exercise has a clean intrinsic answer on the common smooth model:
\[
\pi^*H=A+K_X-2E'.
\tag{III.11}
\]
Indeed \(K_X=e\), so the right side is
\[
(H+2E-3e)+e-2(E-e)=H.
\]
Thus the complete system \(|A+K_X-2E'|\) contracts \(e\) and recovers the original quartic embedding. There is also an explicit ambient inverse. In the complete-image coordinates above, put \(s=c_0-\alpha a_0-\beta b_0\). The four quadrics
\[
[g:h:l:t]=[a_0f_0:a_0s:b_0s:d_0s]
\tag{III.11a}
\]
recover the original quartic coordinates on the common dense open set; this follows immediately from \(d_0f_0=c_0s\). Compose them with the quadratic inverse \([XY:XZ:YZ:Z^2:WZ]\) of the chosen projection, and the intervening linear change from the product basis to \((a_0,b_0,c_0,d_0,f_0)\). This gives four explicit degree-four forms defining the rational inverse from the septimic to \(S\). Their common zero set is the base locus of this chosen presentation; common factors can be cancelled. On the smooth common model the resolved inverse is exactly (III.11). No minimal-degree assertion is made for these quartic representatives. For a fully expanded prescription when \(\beta\ne0\), choose the global sections \(m_0=tu\), \(m_1=tv-\alpha hu-\beta lu+\mu tu\) with general \(\mu\), and complementary section \(r=hu^2=a_0\). Given \([X:Y:Z:W]\), form the quadrics
\[
d=XY,\quad c=XZ,\quad s=Y(Z-\mu X),\quad f=Z(Z-\mu X),
\]
\[
a=WZ+\lambda XY,\qquad b=(c-s-\alpha a)/\beta.
\]
Then the quartic representatives are simply \([af:as:bs:ds]\). In this basis they share the factor \(Z-\mu X\). Cancelling it gives the cubic representatives \([aZ:aY:bY:XY^2]\), without asserting minimality. This illustrates why a chosen presentation degree must be distinguished from the rational map itself.

#### The chapter's explicit limit

The note on p. 89 expressly says that the preceding examples do not exhaust the singularities or fundamental curves. It asks the reader to examine chains of quadruple points, longer chains of triple points, and mixed clusters. This is not an unproved assertion of a complete classification. The modern branch blowup algorithm (III.5), together with proximity and the actual fiber cycle, is the appropriate extension. Franchetta's Notes I–II are cited in the source as 1945; the verified modern bibliography locates them in series VIII, volume 1 (1946), pp. 49–57 and 162–168. Their original scans were not inspected here.

### III.11. Bicanonical curves and biadjoints (§11, pp. 89–92)

For a degree-\(n\) projective surface, biadjoint forms have degree \(2n-8\), and forms representing \(2K_X+rH\) have degree \(2n-8+r\). The bicanonical space is \(H^0(2K_X)\), not the image of \(\operatorname{Sym}^2H^0(K_X)\). The latter can be zero while the former is nonzero, as the next section shows.

Along an ordinary double curve, a biadjoint vanishes to order two. Along an \(i\)-fold curve for \(i>2\), the intrinsic condition is twice the canonical vanishing on each separated sheet. It need not be represented by ambient order \(2i-2\): in the local ring of \(F\), forms differing by a multiple of its equation agree. In transverse local coordinates, a useful expression is
\[
g\in I^{\,2i-2}+(F),
\]
where \(I\) is the ideal of the multiple curve. A representative can have ambient order \(i\), with the leading and subsequent jets chosen to agree with multiples of the equation of \(F\). For a triple curve, a third-order numerator with the appropriate tangent-cone contact represents the same intrinsic condition as a fourth-order one.

The source's phrase “a linear combination of \(\psi\) and \(F\)” must be understood locally, or after multiplying by forms to equalize their degrees. When \(2n-8<n\), there is no nonzero global degree-\((n-8)\) multiplier available. It would be incorrect to add two homogeneous equations of unequal degree literally. This is a clarification of representatives; it does not invalidate the intrinsic contact condition or the complete biadjoint system.

At an ordinary isolated \(s\)-fold point, the intrinsic numerator condition is
\[
g\bmod F\in\mathfrak m^{\,2s-4}\mathcal O_F.
\tag{III.12}
\]
For \(s=3\), the ambient numerator has a double point. For \(s=4\), it has a quadruple point. For \(s\geq5\), it may have order \(s\) together with the extra contact making its class satisfy (III.12). Thus the source's general multiplicity-\(s\) phrase is to be read together with its explicit \(s=3\) exception. In particular, at a quintuple point, matching the tangent cone supplies the next necessary order. The local count, if the tangent cone is ordinary, can be checked from
\[
\ell\frac{\mathbf C[[x,y,z]]}{(F,\mathfrak m^{2s-4})}
=\binom{2s-2}{3}-\binom{s-2}{3},
\]
with the second binomial taken as zero when appropriate. This is our optional numerical refinement, obtained by subtracting the multiples of the degree-\(s\) initial equation; as elsewhere, it is a local condition count, not automatically a global loss.

#### Why the bicanonical condition is not simply the square of the canonical ideal

For the tacnode \(z^2+f_4(x,y)=0\), the relevant weighted valuation has \(v(x)=v(y)=1\), \(v(z)=2\). A canonical numerator has valuation at least one, but a bicanonical numerator needs valuation at least two. Hence
\[
J_1=(x,y,z),\qquad J_2=(x^2,xy,y^2,z).
\]
The second ideal has colength three. It is larger than \(J_1^2\), which would impose the unnecessary vanishing of the linear \(z\)-term. This is exactly Enriques's condition: pass through the tacnode and have the prescribed tangent plane. His plane-section “unloading” is an elementary way to obtain the same result.

For the Noether point (III.8), \(v(x)=2,v(y)=1,v(z)=3\). The analogous ideals are
\[
J_1=(x,y,z),\qquad J_2=(x,z,y^2),
\]
of colength one and two respectively. The two bicanonical conditions are the first point and its prescribed infinitely near point. In a double-plane calculation, the formal cluster \((0,2)\) unloads to \((1,1)\). This verifies the stated bigenus loss of two for a \([3,3]\) branch point.

The degree-\(n-4\) plane adjoint named on p. 91 is a printed index slip: the section of a degree-\(n-4\) surface plus a line has degree \(n-3\). The correction is \(\varphi_{n-3}\).

#### The complete footnote on pp. 91–92

The footnote begins on p. 91 and continues at the bottom of p. 92. Both transcription comments saying that the continuation or its reference mark lies outside the packet are wrong.

The footnote correctly warns that a complete system downstairs need not pull back to a complete system upstairs. For a smooth double plane branched in degree \(2n\), (III.4) gives
\[
P_2=h^0(\mathbf P^2,\mathcal O(2n-6))
+h^0(\mathbf P^2,\mathcal O(n-6)).
\tag{III.13}
\]
The second summand first appears at \(n=6\). For example, a smooth branch curve of degree twelve gives \(28+1=29\) bicanonical sections, whereas pulling back only sextics gives 28. This is a direct computation from the cover algebra, not a failure of completeness of the plane system itself.

The quartic-branch illustration in the footnote concerns pullbacks of conics, not an effective bicanonical system of that rational double plane. Here \(L=\mathcal O(2)\), and
\[
h^0(f^*\mathcal O(2))=h^0(\mathcal O(2))+h^0(\mathcal O)=6+1=7.
\]
Thus the pulled-back conics form a projective five-dimensional subsystem of a complete projective six-dimensional system. The extra generator is the covering coordinate.

Finally, the footnote uses \(F\) of degree \(2n\), yet labels its biadjoints \(\psi_{2n-8}\). They must have degree \(2(2n)-8=4n-8\). The printed multiplicity \(2n-2\) at the point at infinity is not the quantity to replace. It is compatible with the corrected degree and the necessary contact. For instance, an invariant representative can be written, in homogeneous coordinates with infinity equation \(w\),
\[
w^{2n-2}h_{2n-6}(x,y,w),
\]
of degree \(4n-8\). The anti-invariant summand, when present, has representatives of the form
\[
z\,w^{3n-3}h_{n-6}(x,y,w).
\]
Both degrees check. Multiples of the defining equation can change the ambient multiplicity while preserving the section on \(F\). The scan really prints the smaller subscript, so this is an author's notational carryover, not a transcription error.

### III.12. Surfaces with \(p_g=0\) and \(P_2>0\) (§12, pp. 92–96)

#### The tetrahedral sextic

The displayed equation means
\[
F_6=\varphi(x_2x_3x_4,x_3x_4x_1,x_4x_1x_2,x_1x_2x_3)
+x_1x_2x_3x_4 f(x_1,x_2,x_3,x_4)=0,
\]
where both \(f\) and \(\varphi\) are quadratic forms in their respective four arguments. The absence of commas in the last argument list is nineteenth-century notation, not a degree-ten term \(f(x_1x_2x_3x_4)\) in one variable. A general member has double curves along the six edges and the stated ordinary triple and pinch-point behavior.

The source's “double system” must be distinguished from the smallest span of products of the four cubics \(t_i=\prod_{j\ne i}x_j\) through the edges. The ten products \(t_it_j\), \(i\leq j\), are distinct monomials, with exponent patterns \((2,2,2,0)\) or \((2,2,1,1)\). The entire degree-six space satisfying the double-edge conditions has dimension fourteen: there are also the four monomials \(x_1x_2x_3x_4x_i^2\), with pattern \((3,1,1,1)\). Indeed an exponent vector \((a_1,\ldots,a_4)\) of sum six must have \(a_i+a_j\geq2\) for every pair corresponding to a coordinate edge ideal; these three patterns exhaust the possibilities. The displayed \(\varphi(t)+x_1x_2x_3x_4f(x)\) spans this full space: its two ten-dimensional summands have a six-dimensional intersection. This is the distinction between the prescribed double-edge system and the minimum product system, not a source transcription error. On a model resolving the entire base ideal, one must additionally track the tetrahedron vertices: each cubic vanishes to order two at a vertex, while the four extra sextics have order three at the corresponding vertex. One should therefore not identify this fourteen-dimensional ambient space with the product span or with a doubled resolved divisor class without specifying those vertex conditions.

No quadric vanishes on all six edges. Indeed a quadratic monomial involves at most two coordinates, so it restricts nontrivially to at least one coordinate edge unless its coefficient is zero. Thus \(p_g=0\). The only quartic vanishing doubly along all six edges is, up to scalar, the product of the four coordinates: the required pairwise exponent inequalities force every exponent to be one. Its divisor on the normalization is twice the conductor divisor. Consequently
\[
2K_X\sim0,\qquad K_X\not\sim0,\qquad P_2=1.
\tag{III.14}
\]
The normalization is a complex Enriques surface. Dolgachev (2016, §2, pp. 3–4, equation (1)) gives the conductor calculation and verifies \(p_g=q=0\) for this model. The genericity qualification is essential: special equations may acquire further singularities or split.

For the hyperplane class,
\[
H^2=6,\quad K_XH=0,\quad p_a(H)=4.
\]
Because \(q=0\), the characteristic series is complete. It has degree six and projective dimension two and is nonspecial. To see the last assertion directly, Kodaira vanishing gives \(h^0(H)=4\), and the restriction sequence gives \(h^0(H|_C)=3\). A canonical series on a genus-four curve has four sections, so \(H|_C\) is not canonical. Nevertheless,
\[
2H|_C\sim2K_C,
\]
because \(K_C=(K_X+H)|_C\) and \(2K_X=0\). Thus the example exhibits a nontrivial two-torsion difference between the characteristic and canonical line bundles.

The adjoint system is \(|H+K_X|\), again degree six and genus four. Its double equals \(|2H|\), and applying adjunction twice returns \(|H|\). The source's formulas involving \((2C)''\), \(2C'\), and \(C+C''\) are correct once prime placement is respected. Finally \(K_X^2=0\), so \(p^{(1)}=1\). None of this says that \(K_X\) itself is effective: \(p_g=0\) says the opposite.

#### Castelnuovo's septimic

The second model is a degree-seven surface with a triple line \(r\), a double conic \(\Gamma\) disjoint from \(r\), and three tacnodes \(A_i\), whose tangent planes \(\alpha_i\) contain \(r\). Enriques constructs a pencil from two reducible surfaces: a quartic double along \(\Gamma\), tangent to the prescribed planes at \(A_i\), multiplied by \(\alpha_1\alpha_2\alpha_3\); and the square of a cubic through \(r,\Gamma\), multiplied by a plane through \(r\). The assertion that a general member is irreducible uses general position and the absence of a forced common component. “Take a pencil” alone would not establish irreducibility for arbitrary choices, so this part is an existence sketch rather than a complete parameter-space verification.

A canonical cubic must contain \(\Gamma\) and be double along \(r\). Its restriction to the plane of \(\Gamma\) is forced to contain that plane; the residual quadric is two planes through \(r\). The three tacnodes require three distinct planes through \(r\), which two planes cannot supply. Hence \(p_g=0\).

The exhibited biadjoints are sextics
\[
(\text{plane of }\Gamma)^2\alpha_1\alpha_2\alpha_3\beta,
\]
where \(\beta\) varies among planes through \(r\). They cut a pencil of plane quartics. The two intersections with the double conic account for two nodes, so the quartics have genus \(3-2=1\). The pencil has square zero and no base points.

The completeness argument needs more than square zero: the general residual quartic is irreducible, so the induced morphism \(f:X\to\mathbf P^1\) has connected fibers. Its fiber divisor \(F\) is the exhibited bicanonical divisor. Therefore
\[
H^0(X,\mathcal O_X(F))
=H^0(\mathbf P^1,f_*\mathcal O_X\otimes\mathcal O(1))
=H^0(\mathbf P^1,\mathcal O(1)),
\]
and \(P_2=2\). This supplies the missing justification for the source's short completeness sentence. In this model the contact conditions along the triple line force the stronger ambient quadruple vanishing; the intrinsic criterion was not simply ambient fourth order in every situation.

Since \((2K_X)^2=0\) and \(p_a(2K_X)=1\), the source's identities
\[
4p^{(1)}-4=0,\qquad 3p^{(1)}-2=1
\]
both give \(p^{(1)}=1\). On its minimal model this is a properly elliptic surface, rather than an Enriques surface: \(P_2=2\) and an elliptic bicanonical pencil distinguish it from (III.14). This conclusion uses the actual bicanonical fibration; no unverified list of multiple fibers is inferred.

#### Godeaux and Campedelli: what the historical sentence establishes

The source refers to the examples of Godeaux (1931) and Campedelli (1932), with respectively \(p_g=0,P_2=2\) and \(p_g=0,P_2=3\). These distinguish \(K^2=1\) and \(K^2=2\) general-type examples from the preceding \(K^2=0\) models. The broad preceding question asks also for a bicanonical system of dimension greater than one. Godeaux's \(P_2=2\) gives only a pencil; Campedelli's \(P_2=3\) supplies the net that meets that additional requirement. One should not turn the combined historical sentence into a claim that both examples have bicanonical projective dimension greater than one.

#### An explicit verification of Campedelli's construction

Choose nonzero \(a,b\) with \(a^2\ne b^2\), and put
\[
q_1=x^2+y^2-a^2z^2,\quad
q_2=x^2+y^2-b^2z^2,\quad
q_3=x^2/a^2+y^2/b^2-z^2.
\]
The first two conics are concentric circles in the affine real picture; the third ellipse touches them at the ends of perpendicular axes. Over \(\mathbf C\), their six pairwise contacts are
\[
I=(1:i:0),\ J=(1:-i:0),\
P_\pm=(\pm a:0:1),\
Q_\pm=(0:\pm b:1).
\]
They are distinct. A conic through \(I,J\) has equation
\[
\lambda(x^2+y^2)+\ell xz+myz+cz^2=0.
\]
The two \(P\)'s force \(\ell=0,c=-\lambda a^2\), and the two \(Q\)'s force \(m=0,c=-\lambda b^2\). Hence all coefficients vanish. There is no conic through the six points. This proves the canonical vanishing without a generic-position slogan.

The quartics having the six prescribed tangent contacts form exactly the vector space
\[
\langle q_1q_2,\ q_1q_3,\ q_2q_3\rangle.
\tag{III.15}
\]
To prove completeness, restrict any such quartic \(G\) to \(q_1\). Its eight intersections are the four contacts counted twice, precisely the divisor of \(q_2q_3|_{q_1}\). Subtract a scalar multiple of \(q_2q_3\); the remainder is \(q_1R\) for a conic \(R\). At the two contacts of \(q_2,q_3\), the residual conditions force \(R\) into their pencil. This gives (III.15). The three displayed forms are independent. Thus the twelve point-and-tangent conditions on the fifteen-dimensional quartic space are independent.

For a general
\[
G=\alpha q_1q_2+\beta q_1q_3+\gamma q_2q_3,
\]
the quartic is smooth and its curvature at each contact differs from those of the two conics there. Bertini applies away from the finite base scheme; nonvanishing of the relevant linear terms and distinct second-order terms are open conditions at the six base points. The branch curve
\[
B=q_1q_2q_3G=0
\]
has degree ten and exactly the six intended \([3,3]\) clusters under these generality assumptions.

Canonical plane numerators would be conics through all six first points. None exists, so \(p_g=0\). The smooth degree-ten double plane has \(\chi=7\); each \([3,3]\) cluster lowers it by one, giving \(\chi=1\), hence \(q=0\). Bicanonical invariant numerators are the quartics in (III.15), with the six \((1,1)\) clusters. The other summand in (III.4) has negative plane degree \(n-6=-1\) and no sections; after resolution it cannot acquire sections, since pushing down to the plane would give an effective divisor of negative degree. Therefore
\[
P_2=3.
\tag{III.16}
\]

The intersection check gives the claimed linear genus. On the blown-up plane the quartic system has square \(16-12=4\), and its pullback has square eight. Thus
\[
(2K_{\min})^2=8,\qquad K_{\min}^2=2,\qquad p^{(1)}=3.
\]
The canonical-resolution calculation provides the same result: start with \(K^2=8\), lose two at the second blowup of each of the six clusters, reaching \(-4\), then contract the six disjoint rational \((-1)\)-curves above the first exceptional branch curves, reaching \(2\). Omitting these six contractions would give the wrong answer.

Enriques also proves completeness directly by restricting to the quartic branch component \(G\), of genus three. The residual series has degree four. If it were canonical, the twelve imposed cluster points would lie on a cubic. Such a cubic would meet each \(q_i\) at four prescribed tangencies, at least eight intersections, exceeding its Bézout number six unless it contained \(q_i\). Containing all three conics is impossible for a cubic. The degree-four series is therefore nonspecial and has two sections. There is only one bicanonical divisor containing the ramification curve over \(G\), namely its double. Restriction bounds the total space by \(1+2=3\), matching (III.15). This is a complete argument once the stated intersection interpretation of the cluster is made explicit.

**Own extension, with high confidence.** The ideal of the quartic net at each contact is locally \((u,v^2)\), so the two successive base-point blowups resolve it. It has no other base points and defines a degree-four map of the blown-up plane to \(\mathbf P^2\). After lifting to the double cover and contracting the six extraneous \((-1)\)-curves, the complete bicanonical map has degree eight onto \(\mathbf P^2\). This follows directly from the explicit base ideal and \((2K)^2=8\); it is not needed for Enriques's calculation of \(P_2\).

### III.13. Equivalence criteria (§13, pp. 96–100)

#### From adjoints to equivalent restrictions

The opening observation says that if \(L,M\) cut equivalent divisors on every general member of a sufficiently ample, nonruled system without proper fundamental curves, they are equivalent on the surface. To reduce to the special adjoint form, Enriques chooses a sufficiently high-degree adjoint containing \(L\), with residual curve \(D\), and compares \(L+D\) with \(M+D\). The existence of that adjoint is supplied in modern terms by Serre vanishing for the ideal of \(L\). Proper fundamental divisors remain a possible kernel of restriction; excluding them is necessary.

This is a statement about equivalent line bundles on curves, not equality of numerical degrees. Equal degrees alone are much weaker. Nor does the argument imply that restriction to one arbitrary ample curve is injective on all of \(\operatorname{Pic}(X)\): on \(\mathbf P^1\times\mathbf P^1\), for example, \(\mathcal O(1,-1)\) restricts trivially to a smooth \((1,1)\)-curve.

#### First criterion: a pencil with a simple base point

The source assumes a linear pencil of integral curves, no reducible members, and a simple base point \(O\) avoided by \(K_0,K_\infty\). If the restrictions of \(K_0,K_\infty\) are equivalent, a rational function on each member can be normalized to take value one at \(O\). Enriques correctly recognizes that the zero and pole divisors of the resulting function might acquire extra pencil members, and tries to exclude them by the normalization.

A rigorous modern proof can avoid delicate pointwise assertions about a rational function at an indeterminacy point. Resolve the pencil and work over the function field of its parameter line. The line bundle \(M=\mathcal O_X(K_0-K_\infty)\) is trivial on its generic fiber, so choose a rational section trivializing it there. Its divisor is vertical. Push down from the resolved pencil to \(X\): exceptional components disappear, and each remaining vertical prime is a pencil member, because all those members are integral. Consequently
\[
K_0-K_\infty\sim sC.
\]
The assumed equivalence on \(C\) gives \((K_0-K_\infty)C=0\). A simple base point makes \(C^2>0\), so \(s=0\). This proves the criterion. It also shows why the base-point hypothesis matters and why restrictions must count any intersections at base points rather than silently discarding them.

The transition from fiberwise triviality to generic-fiber triviality uses algebraicity. On a proper flat family of integral curves, a degree-zero line bundle having a section on general fibers has a section on the generic fiber by semicontinuity and base change; a nonzero section of degree zero on an integral proper curve trivializes it. Merely choosing unrelated analytic functions on each complex fiber would not establish rational dependence.

#### Second criterion: equivalence up to vertical divisors

For a proper pencil \(f:X\to B\) with integral fibers, the same generic-fiber argument yields
\[
K_0+\sum a_i C_i\sim K_\infty+\sum b_j C_j,
\tag{III.17}
\]
where the sums are effective vertical divisors after separating positive and negative coefficients. This is the criterion on p. 97. If \(B\simeq\mathbf P^1\), all fibers are equivalent, so the difference is \(sC\). If the pencil has base points on the original model and those intersections are included, the degree calculation above forces \(s=0\).

The integral-fiber qualification is substantive. With reducible fibers, individual components occur in the vertical divisor; with multiple fibers, primitive components and their multiplicities must be retained. The loose phrase “a sum of members” should not erase that information.

#### The trace normalization fails to control the extra poles

The printed proof sets
\[
f=\frac{\varphi}{\varphi_1+\cdots+\varphi_m},
\]
using the intersection with an auxiliary curve \(L\). The denominator indeed removes the scalar ambiguity when its trace is nonzero. It can, however, vanish on fibers that meet neither \(L\cap K_0\) nor \(L\cap K_\infty\). Replacing \(f\) by \(1/f\) does not replace the trace of \(\varphi\) by the trace of \(1/\varphi\). Thus the asserted identification of the extra pole group on p. 98 is false.

**Explicit counterexample, our calculation.** On \(X=\mathbf P^1_x\times\mathbf P^1_t\), take fibers \(C_t\), \(K_0=(x=0)\), \(K_\infty=(x=\infty)\), and \(\varphi=x\). Let
\[
L:\quad x^2-tx+1=0.
\]
This is an irreducible curve, the graph \(t=x+x^{-1}\), with two points over a general \(t\). Their \(\varphi\)-trace is \(t\). Therefore \(f=x/t\), and
\[
\operatorname{div}(f)=K_0+C_\infty-K_\infty-C_0.
\tag{III.18}
\]
Both \(L\cap K_0\) and \(L\cap K_\infty\) lie over \(t=\infty\), but the additional pole fiber is \(t=0\). It contains neither intersection. This directly contradicts the printed description of \(\sum' C\). It does not contradict (III.17), since the actual correction is still vertical.

The trace need not even be nonzero: with \(L:x^2=t\), the two values are opposite and the trace vanishes identically. A generic auxiliary choice can often avoid this, but the proof must say why and must still handle the resulting trace-zero fibers. The generic-fiber divisor proof supplies both requirements without attempting the false identification.

#### Third criterion: a complete family of index greater than one

The index \(\nu\) is the number of members through a general point. Enriques states that if a one-dimensional family has index \(\nu>1\), all members are irreducible, and \(K_0,K_\infty\) restrict equivalently to them, then \(K_0\sim K_\infty\). He forms a second trace
\[
\psi(P)=f_1(P)+\cdots+f_\nu(P)
\]
over the curves through \(P\). He acknowledges possible cancellation of poles, but assumes that all poles are on \(K_\infty\). The first normalization has not proved that assumption: its denominators create other poles. Nor is \(\psi\not\equiv0\) established. The final nonnegative-degree calculation is valid only after these missing premises and the absence of curves orthogonal to the family have been supplied.

Completeness of the family is also essential. Let \(X=\operatorname{Bl}_p\mathbf P^2\), with exceptional curve \(E\). Choose a smooth conic in the dual plane, parametrizing a one-dimensional family of lines of index two, and remove the finitely many parameters whose lines pass through \(p\). Their strict transforms are all integral and disjoint from \(E\). Thus \(E\) restricts trivially to every member but is not linearly trivial. To make both compared divisors nonzero and effective, take \(K_0=D+E,K_\infty=D\). Restoring the omitted parameters in the flat closure introduces reducible members containing \(E\). This example shows precisely what an open-family reading of the printed statement would miss.

#### A modern proof with the hypotheses made explicit

The following is our reconstruction, not an attribution of a historical repair. Let \(B\) be a smooth complete connected curve parametrizing a flat family of pairwise distinct integral curves \(C_t\subset X\). Let \(I\subset X\times B\) be its incidence surface, \(p:I\to B\), \(q:I\to X\), and assume \(q\) is generically finite of degree \(\nu>1\). Let \(M\) be a line bundle whose restriction to every fiber \(C_t\) is trivial. The same conclusion follows from generic triviality if its extension to all fibers is separately justified; including it in the hypothesis avoids that hidden step.

1. Proper flat base change gives \(p_*\mathcal O_I=\mathcal O_B\) universally. The see-saw lemma gives \(q^*M=p^*N\) for a line bundle \(N\) on \(B\) (Stacks Project, Lemma 37.33.2, Tag 0EX7).

2. Resolve \(I\) if necessary. On the resolved incidence surface a divisor pulled back from \(B\) has square zero. The projection formula for the generically finite map therefore gives
   \[
   \nu M^2=(q^*M)^2=(p^*N)^2=0.
   \]
   Also \(M C=0\), since its restriction has degree zero.

3. Two distinct family members pass through a general point because \(\nu>1\). They have positive local intersection there, so their common numerical class satisfies \(C^2>0\).

4. The class \(C\) is ample. Indeed, its intersection with any irreducible curve \(E\) is nonnegative, by taking a different member. If \(CE=0\), completeness makes the proper incidence projection \(q\) surjective onto \(X\). Some member must meet a general point of \(E\); positive local intersection then forces that member to equal \(E\). But its class is \(C\), giving \(CE=C^2>0\), a contradiction. Thus \(CE>0\) for every curve, and the Nakai–Moishezon criterion applies.

5. Hodge index, together with \(MC=0,M^2=0,C^2>0\), makes \(M\) numerically trivial. This is numerical, not yet linear, equivalence.

6. Since \(C-M\) is ample, Kodaira vanishing and Serre duality give
   \[
   H^1(X,M-C)^\vee=H^1(X,K_X+C-M)=0.
   \]
   In the restriction sequence
   \[
   0\to M(-C)\to M\to\mathcal O_C\to0,
   \]
   the constant section of \(\mathcal O_C\) therefore lifts to a nonzero global section of \(M\). Its divisor is effective and numerically trivial. An ample divisor has positive intersection with every nonzero effective divisor, so this divisor is zero. Hence \(M\simeq\mathcal O_X\).

This proves the claimed linear equivalence under the displayed complete-family hypotheses. The specific modern inputs are verified in Stacks Tag 0EX7; Brosnan, Theorems 2.1 and 3.15, for Nakai–Moishezon and Hodge index; and Lazarsfeld, Vanishing Theorem 5.2, for Kodaira vanishing. These ingredients are clearly separated from the incorrect trace pole calculation.

#### The continuous-family observations on p. 100

A rationally parametrized family of divisors has constant line-bundle class. One modern proof maps the parameter \(\mathbf P^1\) to the appropriate component of the Picard variety. Translating to \(\operatorname{Pic}^0(X)\), an abelian variety, makes this map constant: invariant one-forms span its cotangent spaces, whereas \(\mathbf P^1\) has no nonzero holomorphic one-forms. Thus the divisors lie in one complete linear system. Enriques attributes the criterion to his 1895 work and refers to Enriques–Chisini for the curve analogue.

The next criterion, attributed to Severi, concerns a connected family \(D_t\) of divisors whose restrictions to one sufficiently general test curve are equivalent. Its modern justification is simpler once the test curve is ample. The differences \(M_t=\mathcal O_X(D_t-D_0)\) lie in \(\operatorname{Pic}^0(X)\), hence are numerically trivial. If \(M_t|_C\) is trivial, the Kodaira-and-restriction argument in step 6 above proves \(M_t\) trivial on \(X\). A complete integral family of test curves with index greater than one supplies ampleness by steps 3–4. This proves the continuous-family version with explicit hypotheses.

The source instead invokes Castelnuovo's enumerative criterion for a series of point groups and a continuity argument that a maximum double-point count persists. It does not write the formula or the conditions preventing specializations of the count. Accordingly it is a sketch relying on the cited curve theory. Baker's 1936 paper explicitly revisits a related Severi lemma for point series; its verified abstract is evidence of that historical discussion, not a verified repair of this particular surface trace proof.

The final paragraph attributes to Torelli an inequality for the number of nodal curves in a one-dimensional series, involving the Zeuthen–Segre invariant, with maximum in the linear case. No inequality, normalization of multiplicities, or equality hypotheses are given in these pages. The bibliographic entry can be located as Torelli (1907), volume 42, pp. 86–99, but its original full text was not inspected. The register therefore records this as an assumed earlier result. No modern formula is invented to stand in for the unspecified historical inequality.

### Own deductions, confidence, and remaining questions

The explicit trace examples (III.18), the complete flex dimension computation (III.10), the specified septic projection and local singularity calculation in III.10, the inverse formulas (III.11)–(III.11a), and the conic/quartic calculations (III.15) are our computations. Their confidence is high because each is verified by a displayed equation, exact sequence, or intersection calculation. They are not claimed as new theorems or as discoveries of historical priority.

A useful additional local extension is available for the ordinary oscnode \(z^2+f_6(x,y)=0\). The weighted condition for an \(m\)-canonical numerator is \(v(g)\geq2m\), with weights \((1,1,3)\). For \(m=2\), the missing monomials are the ten monomials in \(x,y\) of degree at most three and the monomial \(z\): the local bicanonical defect is eleven. This agrees with the double-cover calculation \(3+2\cdot4=11\), namely the canonical Euler defect plus the bicanonical contribution from the \(K^2\) loss. The statement is restricted to the ordinary weighted model; additional infinitely near degenerations need their own valuations.

Exercise 2 is now reconstructed through the explicit subsystem, the ordinary quadruple and triple lines, the isolated double point and its infinitely near tacnode, the unique adjoint cubic, and the quartic rational inverse. Its additional generic hypotheses and its distinction from the full projective-four-dimensional imposed system are part of the conclusion. The historical Torelli inequality and several earlier papers named only through Enriques remain source-verification limits, not gaps silently filled with modern claims.


### References and verification: Chapter III

These references record the scope of verification for Chapter III. “Full text consulted” means that the cited passages were read in an accessible full text; it does not mean that every page of a modern monograph was audited. A publisher record or an author's bibliography verifies metadata, not the proof of a historical theorem. The modern references below support the stated methods; they are not being credited with having repaired Enriques's particular sentences unless that history is independently established.

#### A. Modern sources with the relevant full text consulted

##### SIII01. Adjoint ideals and completeness

Ein, L., & Lazarsfeld, R. (1997). Singularities of theta divisors and the birational geometry of irregular varieties. *Journal of the American Mathematical Society, 10*(1), 243–258.

- Full text: [https://www.math.stonybrook.edu/~cschnell/pdf/references/EinLazarsfeld.pdf](https://www.math.stonybrook.edu/~cschnell/pdf/references/EinLazarsfeld.pdf)
- Exact locator: **Proposition 3.1 and equation (3.1.1), printed p.254**, PDF page12 (zero-based11).
- The adjoint ideal exact sequence and its proof by pushing forward the adjunction sequence are directly inspected. The same proposition identifies trivial adjoint ideal with normal rational singularities. Twisting its sequence in \(\mathbf P^3\), applying projection formula, and using \(H^1(\mathbf P^3,\mathcal O(t))=0\) give the completeness argument in Commentary III.1.
- This is an explicit modern theorem used for reconstruction. No claim is made that this 1997 paper is the first modern account or a historical correction of Enriques.

##### SIII02. Surface identities, birational invariance, and negative intersection

Beauville, A. (1978). *Surfaces algébriques complexes*. Astérisque, 54. Société Mathématique de France.

- Publisher full text: [https://smf.emath.fr/system/files/filepdf/AST_1978__54__R1_0.pdf](https://smf.emath.fr/system/files/filepdf/AST_1978__54__R1_0.pdf)
- Archival record: [https://www.numdam.org/item/AST_1978__54__R1_0/](https://www.numdam.org/item/AST_1978__54__R1_0/)
- Exact locators: **I.12** (Riemann–Roch), **I.13** (Serre duality), printed p.11; **I.15–I.16**, printed pp.12–13 (adjunction and arithmetic versus geometric genus); **III.20**, printed pp.47–48 (birational invariance of \(q,p_g,P_n\)).
- Further inspected locators: **VIII.2–VIII.5**, printed pp.122–124, for Kodaira-dimension-zero discussion and negative intersection statements; **VIII, Exercise 11**, printed p.142, for the special degree-eight K3 model with a degree-three elliptic pencil. The exercise is cited to prevent incorrectly identifying every such K3 with a complete intersection of three quadrics.
- Uses: background identities and model conventions throughout Chapter III. The source's historical “grade” must still be translated individually; these references do not license ignoring changes under blowup.

##### SIII03. Double covers, canonical resolution, and exceptional cycles

Calabri, A., & Ferraro, R. (2002). Explicit resolutions of double point singularities of surfaces. *Collectanea Mathematica, 53*(2), 99–131.

- Full text, version 3 dated 13 March 2002: [https://arxiv.org/pdf/math/9911183](https://arxiv.org/pdf/math/9911183)
- Record: [https://arxiv.org/abs/math/9911183](https://arxiv.org/abs/math/9911183)
- Author-institution publication record: [https://sfera.unife.it/handle/11392/1401224](https://sfera.unife.it/handle/11392/1401224)
- Exact locators: **§3, equations (3.2)–(3.3)**, double-cover structure and canonical formula; **Theorem7.4**, canonical resolution; **§9, equations (9.5)–(9.9) and Theorem9.7**, canonical correction and fiber cycle; **§§10–11**, fundamental and minimal-resolution cycles; **§14, equation (14.7), Lemma14.8, Theorem14.13/equation (14.14), Theorem14.15**, unloading and pluricanonical conditions.
- Page numbering for these locators is that of the 31-page preprint, not the journal pagination. Theorem14.13 is on preprint p.29; its concluding paragraph explicitly warns about \(H^1\) when the global degree is not sufficiently large.
- Bibliography **[13]**, preprint p.31, supplies Franchetta's1946 metadata. Version 3 has two authors; the earlier three-author version is not the one cited.

##### SIII04. Conductor adjunction and the tetrahedral sextic

Dolgachev, I. V. (2016). *A brief introduction to Enriques surfaces* (arXiv:1412.7744, version 2).

- Full text: [https://arxiv.org/pdf/1412.7744](https://arxiv.org/pdf/1412.7744)
- Exact locator: **§2, pp.3–4, equation (1)**.
- The normalization/conductor duality formula and the classical tetrahedral sextic calculation are inspected. This supplies modern corroboration of \(p_g=q=0\) and \(2K=0\) for the general sextic model. Intersecting the same conductor formula with a ruling fiber supplies our short added proof of the scroll count \(n-2\); that derived application is ours.

##### SIII05. Descent for a line bundle trivial on all fibers

The Stacks Project Authors. (n.d.). Lemma37.33.2, Tag 0EX7.

- Full statement and proof links: [https://stacks.math.columbia.edu/tag/0EX7](https://stacks.math.columbia.edu/tag/0EX7)
- Exact hypotheses include a proper flat morphism of finite presentation, universal equality \(f_*\mathcal O_X=\mathcal O_S\), and reduced base. A vector bundle trivial on all fibers descends from the base.
- Applied in Commentary III.13 to the incidence family after expressly imposing the complete, flat, integral-family hypotheses. It does not justify a trace denominator or an arbitrary open family.

##### SIII06. Hodge index, Nakai–Moishezon, and curve adjunction

Brosnan, P. (n.d.). *Algebraic surfaces* [Math808J course notes, University of Maryland].

- **Hodge index, Theorem3.15**: [https://math.umd.edu/~pbrosnan/notes/Surfaces/shit.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/shit.html)
- **Nakai–Moishezon, Theorem2.1**: [https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0007.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0007.html)
- **Adjunction, Proposition 3.1 and Corollary3.2**: [https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0016.html](https://math.umd.edu/~pbrosnan/notes/Surfaces/sect0016.html)
- Statements and surrounding arguments were inspected on the author's university site. These are primary authored expository notes, not the original historical papers of Hodge, Nakai, or Moishezon.
- Uses: the complete-family equivalence proof in III.13 and the curve-genus identities in the explicit examples.

##### SIII07. Kodaira vanishing

Lazarsfeld, R. (with the assistance of G. Fernández del Busto). (1994). *Lectures on linear series* (arXiv:alg-geom/9408011).

- Author-hosted full text: [https://www.math.stonybrook.edu/~roblaz/Reprints/Lazarsfeld.LLS.pdf](https://www.math.stonybrook.edu/~roblaz/Reprints/Lazarsfeld.LLS.pdf)
- Exact locator: **Vanishing Theorem 5.2**, printed p.26, PDF page26 (zero-based25).
- The statement includes the ample case of Kodaira vanishing and the nef-and-big generalization. Commentary III.13 needs only the ample case. The preprint title page and31 August 1994 date are directly verified; no unverified later publication pagination is supplied.

##### SIII07a. Rationality from a genus-zero pencil

The Stacks Project Authors. (n.d.). Theorem 59.67.10, Tsen’s theorem, Tag 03RD.

- Full statement and proof: [https://stacks.math.columbia.edu/tag/03RD](https://stacks.math.columbia.edu/tag/03RD)
- The function field of a curve over an algebraically closed field is C1; in particular every conic over C(t) has a rational point. This closes the rationality inference from the residual quartic pencil in Exercise 1. It is an added modern proof, not an attribution to the source’s spatial transformation.

#### B. Historical bibliographic records verified, without original full-proof verification

##### SIII08. Pedoe and accidental canonical base points

Pedoe, D. (1937). On the canonical systems of certain algebraic surfaces. *Mathematical Proceedings of the Cambridge Philosophical Society, 33*(3), 311–314.

- DOI: [https://doi.org/10.1017/S030500410001968X](https://doi.org/10.1017/S030500410001968X)
- Publisher record: [https://www.cambridge.org/core/journals/mathematical-proceedings-of-the-cambridge-philosophical-society/article/abs/on-the-canonical-systems-of-certain-algebraic-surfaces/F0B93A84E20F27EE6934E6CF237F8632](https://www.cambridge.org/core/journals/mathematical-proceedings-of-the-cambridge-philosophical-society/article/abs/on-the-canonical-systems-of-certain-algebraic-surfaces/F0B93A84E20F27EE6934E6CF237F8632)
- Metadata and abstract were consulted. The abstract concerns accidental base points, consistently with Enriques's p.86 citation. The full article and the precise local claim are not independently verified here.

##### SIII09. Clebsch's double-plane paper and the date error

Clebsch, A. (1870; often cited1871 by bound volume). Ueber den Zusammenhang einer Klasse von Flächen-abbildungen mit der Zweitheilung der Abel'schen Functionen. *Mathematische Annalen, 3*, 45–75.

- Publisher record and DOI: [https://link.springer.com/article/10.1007/BF01443905](https://link.springer.com/article/10.1007/BF01443905)
- The publisher dates the issue to March1870. The frequently used1871 bound-volume convention appears, for example, in the bibliography of Dolgachev's *Classical algebraic geometry*: [https://www.cambridge.org/core/books/abs/classical-algebraic-geometry/references/9497B35666B0DA06722646BC06199E8A](https://www.cambridge.org/core/books/abs/classical-algebraic-geometry/references/9497B35666B0DA06722646BC06199E8A)
- Enriques's printed1861 cannot refer to the identified volume3 article. This audit records the discrepancy and the date convention; it did not inspect the original article body or an original volume title page.

##### SIII10. Franchetta's notes

Franchetta, A. (1946). Sui punti doppi isolati delle superficie algebriche. NotaI; NotaII. *Atti dell'Accademia Nazionale dei Lincei, Rendiconti, Classe di Scienze Fisiche, Matematiche e Naturali*, seriesVIII,1,49–57;162–168.

- Verified as bibliography **[13]** of Calabri–Ferraro's original research paper, with the same1946 attribution in its introduction.
- Enriques prints1945 on p.89. The source discrepancy is recorded; the original Lincei scans were not opened. Calabri–Ferraro supplies modern verification of the algorithms actually used in our commentary.

##### SIII11. Campedelli's construction

Campedelli, L. (1932). Sui piani doppi con curve di diramazione del decimo ordine. *Rendiconti dell'Accademia Nazionale dei Lincei*, seriesVI,15,358–362.

- University-hosted author bibliography: [https://www.mat.uniroma3.it/users/sernesi/BIBLIOGRAFIA/campedelli.htm](https://www.mat.uniroma3.it/users/sernesi/BIBLIOGRAFIA/campedelli.htm)
- This verifies metadata, not the original proof. The chapter's conic-and-quartic construction is worked through independently in Commentary III.12, directly from the supplied Enriques pages. No step of that computation is represented as having been read in Campedelli's original article.

##### SIII12. Baker on a related Severi lemma

Baker, H. F. (1936). On the proof of a lemma enunciated by Severi. *Mathematical Proceedings of the Cambridge Philosophical Society, 32*(2), 253–259.

- DOI: [https://doi.org/10.1017/S0305004100001808](https://doi.org/10.1017/S0305004100001808)
- Publisher record: [https://www.cambridge.org/core/journals/mathematical-proceedings-of-the-cambridge-philosophical-society/article/abs/on-the-proof-of-a-lemma-enunciated-by-severi/E0AE397B5CA20199D230DADE1A9D2D41](https://www.cambridge.org/core/journals/mathematical-proceedings-of-the-cambridge-philosophical-society/article/abs/on-the-proof-of-a-lemma-enunciated-by-severi/E0AE397B5CA20199D230DADE1A9D2D41)
- The accessible extract discusses a lemma about point series on a curve and explains difficulty in making Severi's reasoning precise. It mentions Castelnuovo's alternative enumerative proof.
- This is evidence about a related historical argument. The full paper was not inspected, and no assertion is made that Baker repaired the precise trace construction on Enriques pp.98–100.

##### SIII13. Severi's Abel theorem

Severi, F. (1906; announcement1905). Il teorema d'Abel sulle superficie algebriche. *Annali di Matematica Pura ed Applicata*, seriesIII,12,55–79.

- Publisher record: [https://link.springer.com/article/10.1007/BF02419496](https://link.springer.com/article/10.1007/BF02419496)
- The record dates the journal issue to December1906 and identifies an earlier1905 announcement. Enriques gives1905. The modern online date2007 is not the original publication year.
- The publisher metadata and attached historical notes were consulted; the full original proof was not. Neither the second nor the third equivalence criterion is claimed to be historically repaired in a verified passage of this paper.

##### SIII14. Torelli's final cited theorem

Torelli, R. (1907). Sui sistemi algebrici di curve appartenenti ad una superficie algebrica. *Atti della Reale Accademia delle Scienze di Torino, 42*,86–99.

- University-hosted author bibliography: [https://www.mat.uniroma3.it/users/sernesi/BIBLIOGRAFIA/torelli.htm](https://www.mat.uniroma3.it/users/sernesi/BIBLIOGRAFIA/torelli.htm)
- Metadata was retrieved through the indexed university bibliography; a subsequent direct open timed out. The original article and the exact nodal-curve inequality were not inspected.
- Enriques does not write that inequality on p.100. Accordingly the audit records it as an assumed earlier result, without inventing a formula or equality conditions.

#### C. References verified only as citations in the supplied Enriques pages

The following references are kept in the source-status record. Their stated locations were read in Enriques's footnotes, but their original contents were not independently opened in this chapter audit.

- **Enriques–Conforto, *Le superficie razionali***: BookII, ChapterII, §7,p.273 for the Kronecker–Castelnuovo alternative (Enriques p.69); BookI, ChapterVIII for rational quartics (p.75); pp.196,204,206–207 for the two Noether configurations and their projective complication (pp.85–86). The particular classification inputs remain explicit earlier-work assumptions.
- **Enriques–Chisini, *Lezioni***: BookIV for plane singularities (pp.76,83); BookV, §12, volumeIII,pp.90,93 for double planes and infinity singularities (pp.77–78); BookV, ChapterI, note to§10, volumeIII,p.73 andp.485 for rational families; BookV, ChapterIV,§42,volumeIII,p.482 for Castelnuovo's point-series criterion (p.100).
- **Noether (1878), *Ueber die Einzweideutigen Ebenentransformationen***, Erlangen society proceedings, volume10; and Enriques's descriptions of Geiser, De Paolis, and Bertini on p.79. No independent first-publication or full-proof claim is made.
- **Enriques (1896), *Sui piani doppi di genere uno***, Memorie della Società Italiana delle Scienze, as cited on p.79.
- **Enriques (1896), “Introduzione …”**, the shortened reference used on p.92 for the tetrahedral sextic. The modern geometric calculation is independently corroborated by SIII04; this audit does not expand an abbreviated historical title from memory.
- **Castelnuovo (1896), *Sulle superficie di genere zero***, Memorie della Società Italiana delle Scienze, seriesIII,volume10, cited on p.93. The septimic calculation is supplied from the source configuration and modern intersection theory; the original paper was not opened.
- **Godeaux (1931), *Sur une surface algébrique de genre zéro et de bigenre deux***, Lincei volumeXIV, cited on p.95. The chapter mentions this example but develops Campedelli's.
- **Severi**, *Osservazioni varie di geometria sopra una superficie algebrica* (1906), Atti Istituto Veneto65,partII, and *Alcune relazioni di equivalenza …* (1911),ibid.70, as cited on p.96. The abbreviated latter title is not silently completed.

#### Attribution of the reconstructions

The adjoint-ideal, vanishing, see-saw, and double-cover references are verified modern tools. The explicit counterexamples to the trace-pole assertions, the complete-family reconstruction of the third criterion, the flex-point dimension computation and the explicit septimic projection/local singularity/inverse construction, the detailed Campedelli calculation, and the weighted local computations are the audit's own mathematical arguments. They are identified as such in the commentary. A correct modern proof does not establish who first repaired a historical gap.
