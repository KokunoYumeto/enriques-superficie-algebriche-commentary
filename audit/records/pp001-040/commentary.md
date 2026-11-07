# Mathematical commentary and audit of Enriques, *Le superficie algebriche* (1949), front matter and pp. 1–40

## Scope, notation, and standards of judgment

This commentary reads the supplied scan as the textual authority. It covers the two prefaces and contents, the entire **Introduzione, §§1–5 (pp. 1–13)**, and **Capitolo I, §§1–13 (pp. 15–40)**. Printed p. 14 is blank. The contents list later chapters, but their headings do not supply the statements or proofs of those chapters; they are not treated as if those chapters had been supplied. References such as “p. 23” below mean the book's printed pagination. For Arabic-numbered pages, the corresponding PDF page is the printed page plus 15. The chapter-opening p. 15 has a handwritten number rather than a printed folio.

The accompanying claims.csv supplies individually identified statements and their local proof status. Its “proved” category means that an actual argument is supplied in these pages; it does not silently certify that every hypothesis is present. A proof with a defect is identified in the separate error and repair columns. “Sketched” means that a mechanism is supplied but essential steps are left implicit. “Assumed from earlier work” is reserved for an actual cited or explicitly imported result, and “stated without proof” includes announced results deferred to a later chapter. The commentary supplies proofs, counterexamples, or an explicitly identified external theorem wherever appropriate. The corrections table is a textual audit, not an instruction to change every old-fashioned expression into modern terminology.

Unless a different setting is stated, the modern replacement is a **smooth, connected, projective surface \(X\) over \(\mathbf C\)**. This fixes assumptions often implicit in the book. A surface in ordinary space with a double curve is generally **not normal in the modern local-ring sense**. For the ordinary projection models used here, its normalization is smooth; a more general singular model can require resolution of its normalization. Divisors, local branches, and intrinsic linear systems are interpreted on the resulting smooth model. Enriques explicitly instructs the reader to separate the two sheets along the ordinary double curve (p. 8). Ignoring that instruction would create spurious counterexamples to his later use of Bertini.

### Translation of recurrent terms

| Enriques's expression | Modern interpretation and qualification |
|---|---|
| \(S_r\), \(\infty^r\) | Projective space \(\mathbf P^r\); an algebraic family of dimension \(r\), respectively. Parameter counting requires an incidence argument and generic-fiber hypotheses. |
| Curva, including a multiple or composite curve | Usually an effective divisor, with multiplicities, on the smooth model. It need not be a reduced irreducible curve. |
| \(C\equiv K\), occasionally \(C=K\) | **Linear equivalence**, written \(C\sim K\) here. This is substantially stronger than numerical equivalence, for which modern texts often use \(\equiv\). |
| Sistema lineare \(\lvert C\rvert\) | A projective space \(\mathbf P(V)\), \(V\subset H^0(X,L)\); the book also uses the same bars for incomplete systems. Completeness must be checked from the surrounding text. |
| Sistema completo | \(\mathbf P H^0(X,\mathcal O_X(D))\), or its explicitly prescribed version with assigned proper and infinitely near base points. Completeness does **not** imply global generation. |
| Ordine | Degree in a specified projective embedding, generally \(H\cdot D\). |
| Grado effettivo | Intersection of two general moving members away from the assigned base cluster; on its resolution this is the square of the moving divisor. |
| Grado virtuale | \(D^2\) on the chosen smooth model, or \((\pi^*D-\sum m_iE_i^*)^2\) when a base cluster is part of the data. It is not the projective degree. |
| Genere effettivo | Geometric genus of a general integral member, after normalization. |
| Genere virtuale | Arithmetic genus \(p_a(D)=1+(D^2+K_X\cdot D)/2\), with the same base-cluster convention. It remains meaningful for reducible, nonreduced, or noneffective divisor classes. |
| Superficie normale (pp. 25–26) | Completeness of the hyperplane system on the abstract smooth model. For a smooth embedded surface this is linear normality. For a nonnormal projected image, ambient linear normality of its singular structure sheaf is a different condition. It is neither modern normality nor, without more, projective normality. |
| Sistema semplice; involuzione | A linear system inducing a generically birational map; a finite generic equivalence relation coming from the fibers of a generically finite map. “Involution” need not mean an automorphism of order two. |
| Singolarità normali | Ordinary projection singularities. “Normal” here does not mean integrally closed local rings. |
| Curva eccezionale di prima specie | In the irreducible smooth-model setting, a smooth rational curve of self-intersection \(-1\), contractible to a smooth point. Composite exceptional cycles require their multiplicities and must not be confused with their individual components. |

Four distinctions control the entire audit. First, the rational map and the particular polynomials representing it are different data: a common fixed divisor may be canceled. Second, the strict transform and the total transform of a divisor are different. Third, a completed intrinsic linear series and the subseries actually induced by a chosen auxiliary system are different. Fourth, an ordinary projection theorem asserts genericity in a specified space of choices; a bare count of equations does not prove transversality or separability.

### Reading the accompanying ledgers

The claim ledger contains **379 rows**: FM001–FM003 for the mathematical front-matter assertions, IN001–IN104 for the Introduction, LS001–LS156 for Chapter I §§1–8, and EC001–EC116 for §§9–13. These prefixes identify source ranges, not different standards of proof. The correction ledger contains **53 entries**, including all **26 '% ??' markers** and every '[sic]' annotation. Its entries are not all errors: retained readings and bounded-confidence editorial decisions are included. The method-and-limits file gives the scan-to-book pagination, verification record, and remaining limits.

## Front matter: Castelnuovo's preface, Enriques's preface, and the contents

### What the pages actually say

The unnumbered title and copyright leaves contain no mathematical theorem. Castelnuovo's preface occupies the leaf corresponding to p. V through p. VIII. His principal mathematical assertion is that an irregular surface has continuous algebraic families of curves not contained in one linear system, and that this is characteristic of irregularity. He explicitly distinguishes the truth of the result from the inadequacy of Enriques's 1904 algebraic proof. He mentions Poincaré's transcendental work and points the reader to Chapter IX, while saying that he does not see how the route proposed there can yet be made rigorous. This is **an explicit acknowledgment of an unresolved proof problem in the edition's historical setting**, not a hidden error discovered in Chapter I.

The additional caution about Chapters VII, VIII, and X concerns detailed classifications and existence questions. It supplies no particular theorem from those chapters for us to adjudicate. Castelnuovo's remarks about intuition, formalism, and the future of mathematics (pp. VII–VIII) are historiographical judgments, not mathematical claims with proofs. His preface is dated January 1949. Enriques's own preface (pp. IX–X) says the text attained its definitive form by April 1942 and was retained with limited bibliographic additions; it is dated September 1945. These dates explain why “1949” must not be read as a claim that every result then known had been incorporated (Enriques, 1949, pp. V–X).

Enriques identifies the four volumes of Enriques–Chisini and Conforto's *Le superficie razionali* as prerequisites. The supplied pages cite them repeatedly for curve theory, infinitely near points, Lüroth's theorem, degeneration, and rational-surface examples. Their citations are preserved at the relevant places below. They are not silently replaced by an assertion that this forty-page extract proves all of those results.

The contents, pp. XI–XV, are also informative about scope. Canonical systems begin in Chapter II, numerical genus and surface Riemann–Roch in Chapter IV, and the principal irregularity discussion in Chapter IX. Consequently the cohomological apparatus supplied in this audit is **modern explanatory context** for Chapter I and its forward references; it is not falsely attributed to these opening pages. The contents' expression \(p^{(1)}=6,5\) lists the two integral cases 6 and 5; it is not a fractional genus 6.5. The printed spelling “Disgressione” in the Chapter IX contents is a textual issue, not a mathematical one.

### Modern statement of the irregularity assertion

For a smooth projective complex surface set

\[
q(X)=h^1(X,\mathcal O_X),\qquad p_g(X)=h^0(X,\omega_X),\qquad
p_a(X)=\chi(\mathcal O_X)-1=p_g(X)-q(X).
\]

Then \(q(X)>0\) if and only if there exists a flat family of effective Cartier divisors over a connected reduced algebraic parameter scheme whose members are not all linearly equivalent. A stronger useful form is this: for a sufficiently positive divisor \(D\), the algebraically equivalent divisors near \(\lvert D\rvert\) form a smooth family of dimension

\[
\dim\lvert D\rvert+q(X).
\]

The proof uses the Picard variety, which is a smooth projective group of dimension \(q(X)\) in characteristic zero. Choose a Poincaré bundle \(\mathcal P\) on \(X\times\operatorname{Pic}^0(X)\). After tensoring with a sufficiently high power \(A\) of an ample bundle on \(X\), relative Serre vanishing gives vanishing of higher cohomology for all twists \(A\otimes\alpha\), uniformly in \(\alpha\in\operatorname{Pic}^0(X)\). Global generation, and then very ampleness, can be achieved uniformly as well. The pushforward of the twisted Poincaré bundle is therefore a vector bundle of constant rank. Its projective bundle of nonzero sections parametrizes effective divisors, with fiber \(\lvert A\otimes\alpha\rvert\). Distinct \(\alpha\)'s give distinct linear-equivalence classes. If \(q=0\), any map from a connected reduced parameter space to the discrete Picard scheme is constant, so a connected family stays inside one complete linear system. This proves both directions, including the existence assertion omitted by a mere tangent-space count.

The distinction between tangent directions and actual families matters. For a smooth divisor \(C\), the sequence

\[
0\longrightarrow\mathcal O_X\longrightarrow\mathcal O_X(C)
\longrightarrow N_{C/X}\longrightarrow0
\]

gives

\[
0\longrightarrow H^0(\mathcal O_X(C))/\mathbf C
\longrightarrow H^0(N_{C/X})
\longrightarrow H^1(\mathcal O_X)
\longrightarrow H^1(\mathcal O_X(C)).
\]

Thus the deficiency of the characteristic series of the **complete linear system** is

\[
\delta(C)=\dim\ker\{H^1(\mathcal O_X)\longrightarrow H^1(\mathcal O_X(C))\}\le q.
\]

For \(H^1(\mathcal O_X(C))=0\), it equals \(q\). But \(H^0(N_{C/X})\) is the tangent space to the divisor scheme: without a smoothness or unobstructedness argument, its elements need not integrate into actual nearby curves. That is the precise modern reason one cannot infer the full completeness theorem simply from infinitesimal intersections.

For attribution, Grothendieck's 1962 Picard-scheme exposés provide the algebraic framework; Proposition 2.10(iii) of Exposé 236 identifies the tangent-dimension issue and characteristic-zero smoothness. The earlier completeness discussion is in **Exposé 221, §§5.4–5.6**, as identified by Kleiman (2005, Remark 5.18). Mumford's *Lectures on curves on an algebraic surface* (1966, pp. 157–159) treats the semiregular obstruction argument, and Kleiman's “Completeness of the characteristic system” (1973, pp. 304–310) gives a further algebraic treatment. Kleiman's 2005 exposition, Theorem 5.11, Corollary 5.14, and Remark 5.18, verifies the precise formulation and these attributions. These are replacements for identified logical steps, not a claim that each author corrected this particular sentence of the 1949 book. In positive characteristic the Picard scheme can be nonreduced, so its dimension and its tangent dimension \(h^1(\mathcal O_X)\) must be separated. Nothing in this audit silently transfers the complex argument to that setting.

### Editorial judgment and a useful extension

**Judgment.** The two prefaces are candid about their scope. The irregularity assertion is true over \(\mathbf C\), and the source explicitly does not offer an adequate proof there. Its modern proof is supplied above. The historical open proof problem should not be listed as a presently open theorem.

**Present commentary's suggestion; high confidence.** Keep both parameter spaces visible when reading p. 40: \(\lvert C\rvert\), with tangent space \(H^0(\mathcal O_X(C))/\mathbf C\), and the divisor scheme, with tangent space \(H^0(N_{C/X})\). Their discrepancy is measured by the connecting map to \(H^1(\mathcal O_X)\). This gives a concrete reading exercise linking the preface's warning with the last page of the supplied extract. It is a pedagogical proposal, not a new theorem or a claimed historical attribution.

## Introduzione: local models, birational transformations, and projection (printed pp. 1–13; p. 14 blank)

### Scope and conventions

The Introduction contains five numbered sections. Its principal results are the existence of a smooth projective model in \(\mathbf P^5\), the existence of a birational model in \(\mathbf P^3\) with ordinary singularities, and Franchetta's irreducibility theorem for the double curve of a general projection. The first is expressly imported from earlier work. The second receives a dimension-count argument, supplemented by the subsequent discussion of tangent configurations. The third receives a substantial geometric argument whose most compressed transitions require additional justification. The assertion that every result here is merely an unsupported intuition would therefore be inaccurate.

Throughout this commentary, the ground field is \(\mathbf C\), or an algebraically closed field of characteristic zero when the argument is algebraic. This makes explicit the setting of the classical geometric language. In particular, separability, generic smoothness, and characteristic-zero differential arguments cannot be silently exported to arbitrary positive characteristic. “General” means outside a specified proper Zariski-closed subset, rather than merely a visually typical picture. We write \(X\) for a smooth model and distinguish it from a possibly nonnormal image \(Y\). Enriques's \(S_r\) is \(\mathbf P^r\); \(\infty^r\) denotes a family of dimension \(r\), not a cardinality.

The ledger entries IN001–IN104 follow the source in order. They include elementary definitions, imported results, displayed equations, intermediate dimension counts, and the assertions used inside the Franchetta argument. The commentary gives the proofs and qualifications needed to interpret those entries together.

### 1. Elementary local geometry (pp. 1–2; IN001–IN018)

#### Equations, smoothness, and multiplicity

An integral surface in affine three-space is a hypersurface \(f(x,y,z)=0\); its projective closure is defined by a homogeneous equation \(F(x_0,x_1,x_2,x_3)=0\). Irreducibility is assumed. Enriques also assumes the projective notions of degree, class, and polar surfaces, citing Enriques–Chisini, Book III, volume II (1918). In modern terms, degree is the intersection number with a general line. The class, in the nondefective situation, is the degree of the dual surface. A first polar has equation \(\sum a_i F_{x_i}=0\). Dual-defective cases require separate conventions for “class”; no such classification is attempted here.

The line-intersection definition of a simple point must use a **general** line through the point, with intersection multiplicities counted. Tangent lines and lines contained in the surface are excluded. If the local expansion is

\[
f=f_m+f_{m+1}+\cdots,\qquad f_m\ne0,
\]

where \(f_i\) is homogeneous of degree \(i\) in local coordinates, then \(m=\operatorname{mult}_pX\). On a general line through \(p\), the local intersection multiplicity is \(m\); a degree-\(n\) hypersurface therefore has \(n-m\) residual intersections. Smoothness is equivalent to \(m=1\), or equivalently \(df(p)\ne0\). These are correct elementary facts; the book does not prove Bézout or the Jacobian criterion anew.

At a smooth point, choose coordinates so that \(f_z(p)\ne0\). The implicit function theorem gives \(z=g(x,y)\). Its Taylor polynomial through any prescribed order represents the corresponding jet of the surface. After placing the tangent plane at \(z=0\), the quadratic approximation is \(z=g_2(x,y)\), Enriques's osculating paraboloid. Algebraically the completed local ring is \(\widehat{\mathcal O}_{X,p}\simeq\mathbf C[[u,v]]\). This is a statement about local analytic or formal coordinates, not a claim that every smooth surface is rational or has a Zariski-open subset isomorphic to a plane. Enriques's finite-order formulation already avoids that erroneous global inference.

Consequently, a curve germ on a smooth surface is a plane-curve germ in suitable local coordinates. Its embedded singularity can be described by a succession of blowups at proper and infinitely near points. Enriques explicitly refers to Enriques–Chisini, Book IV, volume II, for the omitted theory. An infinitely near point is a point on an exceptional divisor of an iterated blowup; an “infinitesimal curve” is not an extra reduced curve lying in the original surface.

#### Ordinary and special multiple points

At an ordinary point of an \(r\)-fold curve, the surface has \(r\) smooth local branches with distinct tangent planes. This describes an ordinary local configuration, rather than every multiplicity-\(r\) curve. Enriques immediately records the exceptions: branches may be tangent or merge into a higher-order branch, as along a cuspidal double curve. At an isolated multiplicity-\(r\) point, the projectivized tangent cone is \(V(f_r)\subset\mathbf P^2\). A line direction lies on that cone precisely when its intersection multiplicity is at least \(r+1\). Irreducibility or smoothness of the cone is an additional ordinary-case hypothesis. Reducible cones and cones supported on a repeated plane are explicitly allowed in the source.

One sentence requires a more substantial qualification. Page 2 says that a uniplanar double point has three distinct infinitely near double points. A doubled tangent plane alone does not imply this. Write, after a change of coordinates,

\[
f=z^2+g_3(x,y)+\text{terms involving }z\text{ or of higher order}.
\]

In the blowup chart \(x=t,\ y=tv,\ z=tw\), the strict transform begins

\[
w^2+t\,g_3(1,v)+\cdots=0.
\]

On the exceptional line, singular points occur at the zeros of the binary cubic \(g_3\). If that cubic has three distinct zeros, each yields an ordinary double point: locally the leading equation is \(w^2+c\,t(v-v_0)=0\), with \(c\ne0\). This proves the three-point assertion for the ordinary uniplanar case. Without that condition, the conclusion fails. For example, \(z^2+x^3+y^4=0\) has a doubled tangent plane, but its first blowup has only one singular point over the origin: in the \(y\)-chart its equation is \(w^2+t u^3+t^2=0\), singular on the exceptional line only at \(u=0\). This is an explicit calculation supplied for this audit, not an assertion that some named later author first discovered the qualification. The scan confirms the unqualified wording; it is not an OCR error.

The tacnode description is likewise a statement about general plane sections. A useful local test case is \(z^2+x^4+y^4=0\). A general plane section through the origin has a double point followed by a double infinitely near point. After blowing up, the strict transform is singular along the exceptional line: \(w^2+t^2(1+v^4)=0\) in one chart. This explains Enriques's “infinitesimal double line.” Special plane sections can degenerate further and should not be included in the generic formulation.

### 2. Rational transformations and their exceptional behavior (pp. 2–5; IN019–IN038)

#### The rational-map formulas and generic degree

The displayed formulas

\[
(X,Y,Z)=\left(\frac{\varphi_1}{\varphi_0},
\frac{\varphi_2}{\varphi_0},\frac{\varphi_3}{\varphi_0}\right)
\]

describe a rational map. Projectively, the \(\varphi_i\) are homogeneous forms of a common degree, after homogenization and cancellation of common divisorial factors. “Nondegenerate” must mean dominant when Enriques counts a finite number of inverse images of a general point of the target three-space. The induced extension of function fields is then finite; in characteristic zero its degree is the number of distinct points of a general fiber. His “involution of order \(n\)” means the partition by these general fibers, not necessarily the orbit partition of a group of order \(n\). No group action is assumed or proved.

A surface chosen generally relative to this finite correspondence is not preserved by a nontrivial subcorrespondence. Its map to the image is therefore generically one-to-one. A clean formulation is that the off-diagonal relation in the fiber product meets \(f\times f\) in dimension at most one; hence it cannot identify the generic point of \(f\) with another point of \(f\). If the surface is instead saturated by all or part of the correspondence, the restriction can have degree \(m>1\). The image as a reduced variety remains a surface; the pushforward cycle has multiplicity \(m\). That is the modern meaning of “a multiple surface.” The page-3 phrase “la trasformata di \(F\)” should read “di \(f\)” in this sentence. The capital \(F\) is printed in the scan, so this is a source slip, not a transcription error.

Enriques correctly distinguishes a birational map between surfaces from a Cremona transformation of their ambient three-spaces. A birational surface map need not extend to a birational map of the ambient spaces.

#### Base loci, blowups, and branch separation

The common zero set of the homogeneous coordinate sections is the base locus of the chosen presentation. One must first remove common factors; a common zero of a nonminimal presentation can be removable. At a genuine base point the map is resolved by a modification of the source. Over a smooth surface point, a point blowup introduces \(\mathbf P^1\); a succession of blowups introduces a configuration of rational curves. Its image on another birational model may be one curve, several curves, or a contracted configuration. Thus the introductory singular “exceptional curve” is preliminary terminology, refined later in Chapter I.

For an ordinary multiple curve with distinct branches, normalization separates the generic branches. Over a general multiplicity-\(r\) point, there are \(r\) distinct points of the normalization. Blowing up an isolated ordinary hypersurface point exposes its projectivized tangent cone as the exceptional curve; if this cone is smooth, the first blowup resolves the singularity along it. These assertions explain the source's “generally,” but are not true for an arbitrary collection of forms merely because they vanish at the center. The forms must generate an appropriate ideal and separate the directions or branches in question.

The phrase on p. 4 about reducing “from \(r\) to \(r-1\) the neighborhood” does not define a decreasing invariant. A blowup makes first-neighbor points proper points of the new surface; it need not lower the multiplicity. The preceding \(z^2+x^3+y^4\) example still has a double point after its first blowup. The charitable reading is that one level of the infinitely near structure has been exposed. It cannot be used as a termination proof for resolution.

#### The five equations and what their count establishes

For two points \(p=(x,y,z)\), \(q=(x',y',z')\) in the chart \(\varphi_0\ne0\), equality of their images is expressed by

\[
\varphi_i(p)\varphi_0(q)-\varphi_i(q)\varphi_0(p)=0
\quad(i=1,2,3),\qquad f(p)=f(q)=0.
\]

The transcription of these equations agrees with the scan. They are five equations in six affine variables. The diagonal \(p=q\) is a two-dimensional component, and the expected dimension of the residual off-diagonal locus is one. Enriques also gives the ambient version in a footnote: the off-diagonal finite-correspondence relation is three-dimensional before intersecting the two copies of the surface.

This is an expected-dimension argument, not a theorem that every rational map creates a double curve. It requires proper intersection, exclusion of the diagonal and base-locus components, and generic finiteness. For an ambient birational map there may be no off-diagonal relation at all on its isomorphism locus. In scheme language, one works with the fiber product on the domain of definition, removes the diagonal there, and then takes closure; cross-multiplication without this restriction can add spurious components. General projection theorems justify the expected count in the setting subsequently used by Enriques.

The last observations are possibilities: special maps may create higher multiple curves or contract curves to isolated singularities. Contracting a curve does not invariably produce a singular point; the exceptional curve of a point blowup contracts to a smooth point, as Chapter I will emphasize. Reading p. 5 as a universal claim to the contrary would create an artificial contradiction.

### 3. Smooth models and the limits of the graph construction (pp. 5–6; IN039–IN049)

#### Higher-dimensional embeddings

With \(r+1\) sections one obtains a rational map to \(\mathbf P^r\). The image is the closure of its graph-theoretic image, equivalently an irreducible component of a suitable algebraic intersection after elimination. Enriques's count predicts that a surface projected generally to \(\mathbf P^4\) has only finitely many identifications, whereas projection to \(\mathbf P^5\) has none. Point separation alone, however, does not establish smoothness: tangent directions must also be separated.

Here is the exact embedding argument. Embed a smooth projective surface \(X\) in \(\mathbf P^N\). The closure of the union of its secant lines, including limiting tangent lines, has dimension at most five: pairs of points give at most four parameters and the point on the line gives one more. A general center \(\Lambda\simeq\mathbf P^{N-6}\) avoids this set because

\[
\dim\Lambda+\dim\operatorname{Sec}(X)\le N-1.
\]

Projection from \(\Lambda\) separates every pair of points and every nonzero tangent direction. Equivalently, it separates length-two subschemes. The resulting proper morphism is a closed immersion into \(\mathbf P^5\). This proves the five-dimensional embedding assertion once a smooth projective model exists. It also explains why the tangent variety, not just the set of distinct-point secants, must be included.

#### A genuine qualification to Levi's graph remark

Page 6 says that the surface of pairs \((x,y,z,X,Y,Z)\) can have only singularities corresponding to singularities common to the two surfaces. Used to separate branches identified by one projection while the other projection is a local isomorphism, this is correct. As a statement about the closure of an arbitrary birational graph it is false.

An explicit counterexample is the birational map between two affine planes

\[
X=\frac{x^2}{y},\qquad Y=\frac{x^3}{y^2},
\qquad
x=\frac{X^2}{Y},\qquad y=\frac{X^3}{Y^2}.
\]

Its graph closure has equations

\[
yX=x^2,\qquad yY=xX,\qquad xY=X^2.
\]

This is the affine cone over the twisted cubic, parametrized by
\((y,x,X,Y)=(s^3,s^2t,st^2,t^3)\). It is a two-dimensional irreducible variety whose three defining equations have no linear parts at the origin. The Zariski tangent space there has dimension four, so the origin is singular. Both endpoint planes are smooth. If desired, insert \(z=Z=0\) to place the example in exactly the six-coordinate ambient space used by Enriques. Normalizing the graph does not automatically remove this particular defect: the twisted-cubic cone is already normal.

The repair is precise: a graph is smooth at points where one of its projections is a local isomorphism to a smooth surface. Over simultaneous indeterminacy, one must resolve the graph, or principalize the base ideal on a smooth model. This counterexample and its calculation are supplied by the present audit; no claim of historical priority is made. The source's resolution theorem does not depend on accepting the graph assertion in this unqualified form, because the theorem is explicitly imported from independent references.

#### Resolution: what is cited and what a modern proof uses

Enriques expressly declines to prove resolution. His references on p. 6 are B. Levi (1897), O. Chisini (1921), G. Albanese (1924), R. J. Walker (1935), and O. Zariski (1939), with an additional pointer to *Annals of Mathematics* (1941). He credits Levi with the first rigorous treatment. The present audit does not independently certify that historical priority or the completeness of every early cited proof. Walker's and Zariski's papers are already part of Enriques's reference list; they should not be presented as later repairs newly unknown to him.

The modern input is the surface-resolution theorem: an integral projective surface over \(\mathbf C\) has a projective birational modification \(\pi:X\to Y\) with \(X\) smooth. Lipman's theorem applies more generally to excellent surfaces. A precise, checked modern statement and proof is The Stacks Project, Theorem 54.14.5, Tag 0BGP; its local construction and termination are developed in §§54.7–54.14. Normalize first, reduce to finitely many normal surface singularities, resolve those by normalized blowups, and glue the local modifications. Excellence ensures the finiteness and formal-normality hypotheses. This supplies a genuine termination theorem rather than an assumed decrease of multiplicity. Composing a projective resolution with the preceding secant-avoidance embedding proves the exact theorem on p. 6 (Lipman, 1978; The Stacks Project, 2026).

This is a proof of Enriques's formulation **using** a stated modern resolution theorem. It is not a purported new derivation of Lipman's entire 57-page argument. The nontrivial vanishing, boundedness, and local termination results remain explicitly cited dependencies.

### 4. Ordinary singularities of projections (pp. 6–8; IN050–IN066)

#### Correct modern statement and terminology

For a smooth nondegenerate projective surface in characteristic zero, a general linear projection to \(\mathbf P^3\) is finite and birational onto an image with only ordinary singularities. The local analytic models at singular points are

\[
xy=0,\qquad xyz=0,\qquad x^2-y^2z=0.
\]

They are respectively an ordinary point of the double curve, an ordinary triple point, and a pinch point. The reduced double curve is smooth at a pinch point; “cuspidal point” on p. 8 describes the surface's folding behavior, not a cusp of that reduced curve. Its only singular points in the strict ordinary model are ordinary triple points. The normalization is smooth. These statements and the stronger formulation for a surface in \(\mathbf P^4\) with only ordinary improper double points are recorded in Ciliberto and Flamini (2011, Definition 2.1, Remark 2.2, Theorem 2.5).

“Normal singularities” in Enriques's terminology must not be confused with normality of a variety. A hypersurface with a double curve is not normal. An “improper double point” in \(\mathbf P^4\) is two smooth surface branches with independent tangent planes, rather than an intrinsic normal surface node such as \(xy-z^2=0\).

#### What the dimension counts prove

For a nondegenerate surface in \(\mathbf P^5\), the secant-line family has dimension four. Its point-line incidence has dimension five. Hence a general point lies on finitely many secants if the secant variety fills \(\mathbf P^5\), and on none if it does not. “Finite” must allow zero: the Veronese surface is the important exceptional example. Avoiding the tangent variety makes the projection to \(\mathbf P^4\) an immersion, with only finitely many pairs identified in general. The two tangent planes at each such pair must also meet transversely; that assertion uses genericity beyond a bare count.

For projection to \(\mathbf P^3\) from a line \(L\subset\mathbf P^5\), secant lines meeting \(L\) form a one-dimensional family: meeting a fixed line has codimension three in \(G(1,5)\). Trisecant planes containing \(L\) are expected to be finite: planes spanned by three surface points form a six-dimensional family, and containment of \(L\) imposes six conditions in \(G(2,5)\). These counts explain the double curve and isolated triple points.

Enriques invokes the trisecant lemma for space curves, citing Enriques–Chisini, Book III, chapter IV, §43, p. 289. His reduction is useful: if every general secant of the surface were trisecant, a suitable nonplanar hyperplane-section curve would have the same impossible property. Likewise, if all planes through three general surface points contained a fourth, inner projection of an appropriate hyperplane-section curve would produce a nonplanar curve whose general chord was trisecant. The bad family of quadrisecant planes is consequently proper in the six-dimensional trisecant-plane family; adjoining a line in such a plane gives dimension at most seven, smaller than \(\dim G(1,5)=8\), so a general center line avoids it.

These arguments control numbers of distinct points in fibers. They do not, on their own, classify nonreduced fibers, prove transverse intersections of all branches, or show that ramification points are simple crosscaps. Those are the missing local and incidence statements behind the sentence “rigorously demonstrated” on p. 8. This is a precise limitation of the displayed proof, not a counterexample to the ordinary-projection theorem.

#### A complete existence proof after a sufficiently ample re-embedding

The existential theorem on p. 8 can be justified without assuming arbitrary embeddings have all the required jet properties. The following is a modern reconstruction for this audit. Its hypotheses are deliberately sufficient rather than optimal.

Start with a smooth projective resolution \(X\). Choose a sufficiently high power \(L\) of a very ample line bundle so that sections separate all the finite jets used below, simultaneously at up to four distinct points. Such an \(L\) exists: the relevant zero-dimensional schemes have bounded length, their Hilbert schemes are projective, and relative Serre vanishing gives uniform surjectivity of the evaluation maps. A general quadruple of sections defines a morphism \(f:X\to\mathbf P^3\). Four simultaneous zeros impose four independent conditions on a two-dimensional source, so the general quadruple has no base point.

Surjectivity of the jet evaluations means that the corresponding universal evaluation maps are smooth. Thus ordinary codimension calculations in jet space apply to a general choice of sections, by generic smoothness and the fiber-dimension theorem. There are only finitely many kinds of bad strata needed here:

1. For \(k\) distinct source points to have a common image imposes \(3(k-1)\) conditions on a configuration space of dimension \(2k\). The expected dimension is \(3-k\). Double fibers therefore form a curve, triple fibers are isolated, and fibers with four distinct points do not occur.
2. At one point, the derivative is a \(3\times2\) matrix. Rank at most one has codimension two, so ramification points are isolated. Rank zero has codimension six and does not occur.
3. At a double fiber of immersion points, equality of the two tangent planes is an additional codimension-two condition. It therefore does not occur in the one-dimensional double-fiber locus. At an isolated triple fiber, dependence of the three normal directions is an additional condition and is absent generally.
4. A rank-one point sharing its image with a second point imposes the three coincidence conditions and two rank conditions on a four-dimensional pair space. It is absent. The failure of the crosscap condition on the two-jet at a rank-one point is one additional condition and is absent as well.

To identify the remaining ramification germ, choose coordinates with

\[
f(u,v)=(u,g(u,v),h(u,v)),\qquad dg(0)=dh(0)=0.
\]

The generic two-jet condition is that \((g_{vv},h_{vv})\) and \((g_{uv},h_{uv})\) are independent. A target linear change makes \(g_{vv}\ne0\). The analytic Morse lemma with parameter \(u\) changes \(g\) to \(v^2\), after removing a function of \(u\). Write the remaining analytic function uniquely as \(A(u,v^2)+vB(u,v^2)\). Remove \(A\) by a target coordinate change. Independence gives \(B_u(0)\ne0\), so \(x=B(u,v^2)\) is a permissible new coordinate. The map becomes

\[
(x,v)\longmapsto(x,v^2,xv),
\]

whose image has equation \(z^2=x^2y\), the pinch-point model. Two or three mutually transverse immersion branches give \(xy=0\) or \(xyz=0\) by the analytic implicit function theorem.

Finally, the map is finite: a contracted curve would have degree zero against \(f^*\mathcal O_{\mathbf P^3}(1)=L\), contradicting ampleness. A proper morphism with finite fibers is finite. The one-dimensional coincidence locus also shows that the map is generically one-to-one, hence birational in characteristic zero. This proves the existence of the required ordinary model. The stronger theorem for every fixed smooth embedding is a genuine additional generic-projection theorem, not a consequence of assuming that every very ample bundle separates arbitrary higher jets.

#### The apparent nodes and the polar calculation

Page 8 permits “incroci,” or nodes, of the double curve. Pages 10–11 then seek to rule out precisely the associated tacnodal configurations for a general center. The final modern ordinary model does not include these extra nodes. It is more accurate to describe p. 8 as an overbroad interim list, subsequently narrowed, than to claim that Enriques's final theorem predicts such nodes.

The pinch-point assertion about polars can be checked directly. For

\[
F=x^2-y^2z,
\quad
\nu(u,v)=(uv,u,v^2),
\]

the polar \(aF_x+bF_y+cF_z\) pulls back to

\[
u(2av-2bv^2-cu).
\]

The factor \(u\) is the fixed conductor/double-curve component. The residual polar curves have equations \(2av-2bv^2-cu=0\): they all pass through \((0,0)\), and a general member has nonzero linear term. The pinch point is therefore a simple base point of the residual polar system, exactly as claimed. At a general double point, normalization instead gives two distinct smooth points, one for each branch. This justifies the bookkeeping convention used in the rest of the book.

### 5. Irreducibility of the double curve (pp. 8–13; IN067–IN104)

#### The theorem and its dependencies

The final statement is: if \(X\subset\mathbf P^5\) is smooth, irreducible, and nondegenerate, then the reduced double curve of its general projection to \(\mathbf P^3\) is irreducible, except when \(X=v_2(\mathbf P^2)\) is the Veronese surface. That exceptional image is the Steiner quartic, with three concurrent double lines. The intermediate statement for a surface in \(\mathbf P^4\) with at most ordinary improper double points is also a classical Franchetta theorem. Enriques cites Franchetta (1941), with a 1947 addendum. Ciliberto and Flamini (2011, Theorem 2.6) state the modern theorem, while Lopez and Ran (2003; checked preprint pp. 2 and 7) explain the simpler incidence argument in the \(\mathbf P^5\) case and credit it to Mumford.

The existential refinement at the start of §5 remains true even for a rational surface: one may change its embedding. The exception is a particular embedding by plane conics, not an obstruction attached to the birational class of \(\mathbf P^2\). A sufficiently ample re-embedding avoids that exceptional situation.

#### A rigorous replacement for the tangent-plane lemma

The lemma on p. 9 says that a three-dimensional family of pairs \((p,q)\) with tangent planes meeting in a line cannot have its joining secants fill \(\mathbf P^4\). Its conclusion has a short differential proof that avoids the compressed infinitesimal integration in the text.

Let \(T\) be an irreducible family of such pairs, with distinct smooth points general on it. On local affine cones choose lifts \(\widehat p,\widehat q\). The secant evaluation is

\[
\Psi:T\times\mathbf P^1\dashrightarrow\mathbf P^4,
\qquad(p,q,[a:b])\mapsto[a\widehat p+b\widehat q].
\]

Every derivative of \(\Psi\) lies in the projective span \(\langle T_pX,T_qX\rangle\). If the tangent planes meet in a line, this span is a \(\mathbf P^3\). Thus the generic differential rank is at most three. A dominant map to \(\mathbf P^4\) in characteristic zero has generic differential rank four. The alleged filling is impossible. This proves exactly the needed lemma, including the case where the global surface has isolated singularities but the selected points are smooth. It does not rely on classifying all developable plane families.

Enriques's proof fixes \(p\), considers a curve of possible \(q\)'s, and argues that the tangent planes along that curve lie in a fixed hyperplane. It then obtains planar contact curves, a ruling or a developable family of planes, and non-filling. The potentially delicate step is treating an infinitesimal containment as a fixed hyperplane along the entire curve. The differential-rank proof supplies the missing justification for the desired conclusion without claiming that every subsidiary classification sentence has been proved by the brief printed argument.

#### Connectedness and linearity (pp. 9–10)

The apparent double divisors \(C_O=\sum K\) on the normalization vary with the center \(O\). A rationally parametrized family of divisor classes is constant in the Picard variety: a rational map from projective space to an abelian variety is constant. One proof restricts to general lines; a morphism \(\mathbf P^1\to A\) is constant because invariant one-forms span the cotangent bundle of \(A\), while \(H^0(\mathbf P^1,\Omega^1)=0\). Resolving the rational map gives the same conclusion. Thus the divisors lie in one complete linear system. Enriques attributes this principle to earlier work and cites Enriques–Chisini, Book V, chapter I, §9, pp. 78 and 485.

If the general member of the relevant linear system is integral, every member has connected support. One can restrict to a pencil through the proposed member and a general integral member, then use the proper universal family and Stein factorization: its generic fiber is geometrically connected, and the finite birational factor over the normal base \(\mathbf P^1\) is trivial. Enriques calls this the degeneration principle, citing Book V, chapter III, §36, p. 405. If the moving general member is instead reducible, Bertini's second theorem says that it is composed with a pencil, after removing fixed components. Distinct fibers have no moving intersections. The curves obtained by fixing one point \(A\) and varying its two secant partners provide the variable intersections that exclude this case. The distinction between moving intersections and fixed base points is essential to this argument.

This discussion is on a smooth normalization or resolution. Working directly with Cartier divisors on the singular \(\mathbf P^4\) image without controlling their pullbacks would be an additional gap. The source's convention that ordinary improper double points stand for two distinct smooth points supplies the intended interpretation.

#### The local case analysis and where its proof is compressed

Distinct irreducible components of the reduced double curve can meet at an ordinary triple point, or, in the interim singularity list, at a node of that curve. Enriques treats the second possibility first.

For a node arising from two distinct source points, the corresponding image branches have a common tangent plane. Their two source tangent planes then lie in a common \(\mathbf P^3\), meeting in a line. If this occurred for a general center, the associated bad secants would fill \(\mathbf P^4\), contradicting the preceding lemma. The dimension/dominance statement must be formulated on an incidence variety; saying merely “there are many pairs” is insufficient.

For an infinitesimal pair, Enriques interprets the image as tacnodal and the corresponding hyperplane section as having two successive double points. He separately lists the multiplicity distributions \((2,2)\), \((3,1)\), and \((4,0)\), rather than silently ignoring the degenerations. The first two are related to a degenerate Gauss map or developability. The argument does not explicitly establish the necessary dominance of the family of higher-contact hyperplanes. The modern ordinary-projection theorem, or the sufficiently ample jet argument above for the existential result, excludes these bad strata directly.

There is also a small numerical error on p. 11. The scan reads that a developable surface in \(\mathbf P^4\) has only \(\infty^1\), rather than \(\infty^3\), tangent hyperplanes of this kind. For a nonplanar developable surface, its tangent planes form a one-dimensional family and each tangent plane lies in a one-dimensional family of hyperplanes; the generic total is two-dimensional. A cone over a nonplanar curve makes this explicit. Thus \(\infty^2\) is the appropriate count, and it still contradicts the required \(\infty^3\). This is a source-level numerical slip with no effect on the stated contradiction, not an OCR correction.

The last subcase uses the assertion that a space curve whose osculating plane has contact at least four at every general point is planar. In characteristic zero this follows from a Wronskian: for a homogeneous local lift \(v(t)\),

\[
\det(v,v',v'',v''')\equiv0
\]

forces the four coordinate functions to be linearly dependent over the constants. The surface conclusion then uses that a general hyperplane section of a nondegenerate integral surface in \(\mathbf P^4\) spans its hyperplane \(\mathbf P^3\). The link from the postulated family of quadruple hyperplane contacts to this pointwise condition is stated very tersely in the text and still requires the incidence and jet argument. The Wronskian observation by itself is not the missing global proof.

At a triple point, the partitions of the three double-curve branches among irreducible components are \(1+1+1\) and \(1+2\). For three preimages \(p_1,p_2,p_3\), the corresponding apparent double curves have the pair incidences \((p_2,p_3)\), \((p_1,p_3)\), and \((p_1,p_2)\). In the \(1+2\) case one component passes once through \(p_2,p_3\), while the other passes once through those two points and twice through \(p_1\). These multiplicities agree with the normalization of the local model \(xyz=0\): on each branch the conductor has two crossing branches.

The center is then varied along the trisecant line. If an apparent component stays fixed, the book deduces that it is a plane conic. The geometric reasoning can be made explicit: for a general point \(p\) of that component, its partners obtained as the center varies lie in the plane spanned by \(p\) and the center line. If the component is irreducible and the partners vary, it must lie in that plane. Projection from a general point of the line is generically two-to-one on this plane curve, so its degree is two. The next inference, from a two-dimensional conic family to the Veronese surface, invokes a classification result and retains the smooth nondegenerate \(\mathbf P^5\) lifting hypothesis. The bare assertion “a surface with \(\infty^2\) conics is Veronese” is false: a cubic scroll in \(\mathbf P^4\) also has a two-dimensional family of conics. That scroll does not satisfy the retained lifting setup and does not contradict Franchetta's theorem.

If the component moves, Enriques asserts that some member passes through the third preimage, producing tangent branches and a forbidden filling family of secants. Properness makes an incidence specialization plausible, but the text does not show that the required specialization occurs at an admissible center, rather than only at one of the points where projection is undefined. Nor does it explicitly establish the dominance needed after specialization. These are genuine missing steps in the printed argument. They are not evidence that the theorem is false, and this audit does not attribute discovery of these particular textual gaps to a later author without a verified source.

#### Modern proof for the smooth \(\mathbf P^5\) case

Here is a proof with its deep input made explicit. Let \(X\subset\mathbf P^5\) be smooth and nondegenerate, and first suppose \(\operatorname{Sec}(X)=\mathbf P^5\). Blow up the diagonal in \(X\times X\). The resulting smooth fourfold parametrizes ordered distinct pairs together with limiting tangent directions. Over it take the projective-line bundle of their secant lines. Its total space \(I\) is smooth and irreducible of dimension five, and evaluation gives a proper dominant generically finite map

\[
e:I\longrightarrow\mathbf P^5.
\]

For a general line \(L\), the curve \(e^{-1}(L)\) is irreducible by successive applications of Bertini's irreducibility theorem to the pullback hyperplane system. At each step before the final curve the image has dimension at least two, so the system is not composed with a pencil. Its image in the first factor \(X\) is the apparent double divisor; away from the finite exceptional configurations, each first point has a unique partner. The image of an irreducible curve is irreducible, and its further image in \(\mathbf P^3\) is the double curve. This is the Mumford–Bertini proof described by Lopez and Ran and located by them in Moishezon (1977, p. 115).

The remaining input is Severi's classification of smooth defective surfaces in \(\mathbf P^5\): the only smooth nondegenerate surface with \(\dim\operatorname{Sec}(X)<5\) is the Veronese surface of conics. This is the exact extra theorem needed to identify the exception; it is not proved by the preceding Bertini argument. Ciliberto and Flamini give its statement as Theorem 2.4 and refer to Severi and to Mezzetti–Portelli, Theorem 3. The latter full text was not independently accessible in this audit, so that theorem-number pointer is reported through the checked source rather than presented as a directly read proof.

The exception itself is completely concrete. Represent the Veronese surface by rank-one symmetric \(3\times3\) matrices. Its secant variety is the cubic hypersurface of matrices of rank at most two. A general center line meets that cubic in three rank-two points. Each has a conic as entry locus on the Veronese surface, and each entry conic maps two-to-one to a line in the image. The image has degree four and the three double lines are concurrent at an ordinary triple point. In suitable coordinates a representative Steiner quartic is

\[
x^2y^2+y^2z^2+z^2x^2-xyzw=0.
\]

Its three coordinate lines through \([0:0:0:1]\) are double lines. At the common point the lowest-degree term is \(-xyz\), giving the ordinary triple point. This verifies the asserted geometry without mistaking the three conics upstairs for the three lines downstairs.

For the existential statement, the defective-surface classification can even be avoided: a sufficiently positive embedding separates first jets at two points, so two general affine tangent spaces are independent and the secant variety has dimension five. A general projection to \(\mathbf P^5\) preserves the embedding and makes that secant variety fill \(\mathbf P^5\). The preceding incidence proof then gives an irreducible double curve. This also clarifies why changing the embedding removes the Veronese exception at the level of birational models.

### Audit-generated examples and questions

The following suggestions are the present commentator's, not statements attributed to Enriques.

* **A local comparison exercise, high confidence.** Compute the first blowups of \(z^2+xy(x-y)=0\), \(z^2+x^3+y^4=0\), and \(z^2+x^4+y^4=0\). They separate three phenomena that p. 2 compresses: three isolated neighbors, one more complicated neighbor, and an entire infinitesimal double curve. The chart calculations above already establish the first distinctions.
* **A graph diagnostic, high confidence.** Use the monomial birational map of two planes above to distinguish graph closure, normalization, and resolution. This prevents the seductive but false rule that a graph between smooth models must be smooth.
* **An embedding-sensitive comparison, high confidence.** Compare the conic embedding of \(\mathbf P^2\), which yields the Steiner double locus, with a sufficiently high Veronese embedding of the same surface. Franchetta's exception concerns the embedding, while the existence of an ordinary model with irreducible double curve is birational.
* **A focused research exercise, moderate confidence about difficulty.** Reconstruct the specialization argument on pp. 12–13 as a proper incidence correspondence over the open set of admissible centers, including its boundary. The theorem is settled; the unresolved item here is the exact scheme-theoretic justification of this particular printed proof. It would be misleading to advertise that textual reconstruction problem as an open theorem in surface theory.
* **A characteristic question, deliberately not a claimed result.** Determine which parts of the projection proof survive in positive characteristic for a chosen embedding. The differential-rank lemma, Wronskian planarity argument, and branch normal forms all use characteristic-zero or separability hypotheses. No assertion about the complete positive-characteristic analogue is made without a separate investigation.

## Capitolo I: Sistemi lineari di curve (printed pp. 15–40)

### Conventions needed for an exact modern reading

In these sections \(F\) is initially an ordinary singular surface in \(\mathbf P^3\). For intrinsic divisor statements, work on its smooth normalization \(X\), or on a further smooth projective model when base points must be resolved. All statements below use an algebraically closed field of characteristic zero, with \(\mathbf C\) for analytic or topological comments. Enriques's ordinary singularities are not the modern normality condition. Likewise his later “superficie normale” is a statement about completeness of a linear series, not about integrally closed local rings.

A linear system is a pair \((L,V)\), where \(L\) is an invertible sheaf and \(0\ne V\subset H^0(X,L)\); its parameter space is \(\mathbf P(V)\) and its dimension is \(\dim V-1\). The complete system is \(|L|=\mathbf P H^0(X,L)\). A section is identified with its effective zero divisor, including multiplicities. Common fixed divisors must be separated from the zero-dimensional base ideal. After resolving that ideal, the moving system has class
\[
M=\pi^*D-\sum_jm_jE_j^*,
\]
where the \(E_j^*\) are total transforms of exceptional curves, including points infinitely near to earlier ones. Its effective degree is \(M^2\), not automatically \(D^2\). These conventions make precise the repeated cancellation of fixed parts and “variable intersections” in the text.

Enriques's sign \(\equiv\) in §§7–8 means **linear equivalence**, denoted here by \(\sim\). It does not mean the numerical equivalence customarily denoted \(\equiv\) today. A claim marked “proved” below is proved in the supplied pages, possibly using clearly identified standard preliminaries. “Sketched” is used for a genuine compressed argument, not as a synonym for “false.”

### I.1. Linear pencils (pp. 15–17)

**Definitions and formulas.** A nonconstant \(t\in\mathbf C(X)\), written \(\varphi/\psi\), gives the rational map \(t:X\dashrightarrow\mathbf P^1\). Its level divisors are the members of the pencil generated by \(\varphi\) and \(\psi\), after both are regarded as sections of one line bundle. The fibers at \(0\) and \(\infty\) are the zero and pole divisors. If a chosen representation has a common effective component \(K\), it can either be retained as a fixed component of every member or removed. A common component in that representation is not an actual simultaneous positive and negative component of \(\operatorname{div}(t)\): principal divisors have already undergone this cancellation.

For
\[
\tau=\frac{\alpha t+\beta}{\gamma t+\delta},
\qquad \alpha\delta-\beta\gamma\ne0,
\]
the pencil is unchanged and its parameter is changed by an automorphism of \(\mathbf P^1\). Enriques leaves the nonzero determinant implicit in the word “substitution”; a singular matrix would give a constant and must be excluded. Three distinct chosen members, labelled \(0,\infty,1\), determine the parameter uniquely. Equal zero and pole divisors imply \(t/\tau\in\mathbf C^\times\): on a normal projective model this ratio has no zero or pole and is therefore a global unit. Projectivity and normality are the modern hypotheses behind this familiar argument. Equality only of supports, without multiplicities, would not suffice.

For an irreducible affine equation \(F=0\), equality of two rational expressions means equality in the function field, hence
\[
\frac{\varphi}{\psi}=\frac{\varphi_1}{\psi_1}
\iff \varphi\psi_1-\psi\varphi_1\in(F)
\iff \varphi\psi_1-\psi\varphi_1=AF.
\]
The equality is asserted where the fractions are defined, then extended as a function-field identity. It is not pointwise evaluation at their indeterminacy points. The displayed denominator on p. 16 is indeed \(\psi_1\), as shown by magnifying the scan; a visually tempting \(\varphi_1\) is not an error in the source. The doubtful punctuation is separately logged.

All members have the same projective degree because they are linearly equivalent. The apparent drop of affine degree for a special value of the parameter means that a component has moved into the hyperplane at infinity. For instance, if \(\deg\varphi<a=\deg\psi\), homogenizing \(\varphi\) to degree \(a\) introduces the factor \(x_4^{a-\deg\varphi}\). This is an actual component with that multiplicity in the homogeneous zero divisor. Enriques both states this phenomenon and explains its repair by homogenization.

The ambient equations \(\varphi-t\psi=0\) give a pencil of surfaces cutting the given pencil on \(F\); replacing the ambient equations modulo \(F\) need not change the induced pencil. Their ambient common curve \(\Gamma\) usually meets \(F\) in finitely many points. After removing fixed divisorial parts, these intersections form the base scheme. A base point has multiplicity \(i\) when a general member has order \(i\) there. Enriques's argument that a genuine moving base point is an essential indeterminacy point is sound: distinct level curves approach it with distinct constant \(t\)-values. Algebraically, after cancelling a common local divisorial factor on the smooth model, the ideal \((\varphi,\psi)\) is not generated by one invertible local section at a genuine base point. A removable \(0/0\) introduced merely by multiplying numerator and denominator by the same factor is different and was already excluded by the cancellation convention.

**Proof status.** This section consists chiefly of definitions and short proofs by rational-function algebra. It does not purport to prove finite resolution of base ideals. The projective reformulation and the possibility of different ambient pencils are proved directly. A modern reference for the correspondence between generating sections and maps to projective space is the Stacks Project, Lemma 27.13.1, Tag 01ND; the elementary divisor calculations here are supplied explicitly.

### I.2. Rational and irrational pencils (pp. 17–18)

An algebraic one-parameter family of moving curves has index one if exactly one member contains a general point of the surface. On normalizing its parameter curve \(B\), the incidence correspondence defines \(f:X\dashrightarrow B\). When \(B\simeq\mathbf P^1\), the coordinate on \(B\) pulls back to a rational function on \(X\), so the family is linear. Enriques's “single-valued, hence rational” is justified by the algebraicity of this incidence construction: a generically one-to-one correspondence between integral varieties in characteristic zero induces a birational map. It would not be a valid inference for an arbitrary single-valued analytic function.

An irrational pencil means \(g(B)>0\). This genus is the genus of the parameter curve, not the genus of its fibers. The generators of a ruled surface over \(B\) are an example: the fibers are rational lines although the pencil has genus \(g(B)\). For an ordinary spatial ruled model, a general plane section meets each generator once and is birational to \(B\).

The cone construction on p. 17 projects a curve \(B\) of genus \(p\) from a vertex line in \(\mathbf P^4\); intersecting the resulting threefold scroll/cone with a hypersurface gives a surface fibered over \(B\). The phrase “fascio irrazionale di curve di genere \(p\)” is potentially misleading. The construction determines the **base genus** \(p\). A smooth plane fiber cut by a degree-\(d\) hypersurface has genus \((d-1)(d-2)/2\), independently of \(p\). The scan really contains the phrase; the mathematical repair is to distinguish base and fiber genus, not to invent a different transcription. The construction is an example sketch, with generality and irreducibility of the chosen intersection implicit.

**Base-point rationality theorem.** An index-one pencil of moving integral curves with a genuine base point at a smooth point of \(X\) has rational parameter curve. The word “moving” is essential: adding a fixed curve to every fiber of an irrational fibration would otherwise manufacture “base points” without making its base rational.

Enriques first considers distinct moving tangent directions. At a simple base point the pencil is parametrized by those directions; at multiplicity \(i\), it parametrizes degree-\(i\) groups on the exceptional \(\mathbf P^1\), and Lüroth's theorem gives rationality. He explicitly notices the defect in this first argument when all tangents are fixed, then passes to the first moving infinitely near point. The preliminary result cited is Enriques–Chisini, Book II, chapter I, §3, volume I, p. 167.

A precise completion is short. Resolve the rational map to \(B\) by finitely many point blowups. Every component of the exceptional fiber over the smooth base point is a rational curve. Since the strict transform of every general member meets that exceptional fiber, at least one of its finitely many components dominates \(B\). Thus there is a nonconstant \(\mathbf P^1\to B\). Lüroth, or the Riemann–Hurwitz formula, implies \(g(B)=0\). This supplies exactly the finiteness and the first moving direction used implicitly on p. 18. It also proves that an irrational pencil on a smooth projective surface has no genuine base points. It does not make such a statement at an arbitrary singular point of a singular model.

### I.3. Linear systems, degree, genus, and characteristic series (pp. 18–19)

Restricting an ambient vector space \(W=\langle\varphi_0,\ldots,\varphi_R\rangle\) of sections gives a quotient \(V\). If the projectivized kernel, consisting of hypersurfaces containing \(F\), has dimension \(h\), then
\[
r=\dim\mathbf P(V)=R-h-1.
\]
This is elementary rank-nullity; if the kernel is zero, its projective dimension is conventionally \(-1\). Fixed components are common divisorial factors, and the base scheme is the common zero scheme after accounting for them. The scan reads “delle \(C\)” on p. 18: the transcription's “dalle \(C\)” and its accusatory “[sic]” are both misleading.

An intrinsic description is
\[
V=\langle1,t_1,\ldots,t_r\rangle\subset
L(D):=\{f\in\mathbf C(X):\operatorname{div}(f)+D\ge0\}\cup\{0\},
\]
where \(D\) bounds the poles. The functions \(1,t_1,\ldots,t_r\), not merely the \(t_i\), must be linearly independent. Enriques's displayed relation in the homogeneous \(\varphi_i\) says precisely this. “Same pole curve” must mean that the poles are bounded by a common divisor: cancellation can reduce the actual pole divisor of a sum. The equation \(t_0=\sum_i\lambda_it_i\), with the level value allowed to vary, produces \(\sum_{i=0}^r\lambda_i\varphi_i=0\). Choosing a different denominator corresponds to a change of basis in \(V\); no member of the system is intrinsically the polar member.

Exactly one member passes through \(r\) general points. Indeed the evaluation functionals at suitably chosen points span \(V^\vee\), since the rational map defined by \(V\) has nondegenerate image. A general \(r\)-tuple gives \(r\) independent linear equations in \(r+1\) coefficients and hence a one-dimensional solution space. This property holds for reducible linear systems too; its converse needs the extra hypothesis discussed in §I.4.

The system is irreducible if its general member is integral. Its effective genus is the genus of the normalization of that member, equivalently the genus of the smooth general strict transform after resolving the fixed singularities. Its effective degree is the number \(n\) of intersections of two general members outside the common base cluster, counted with intersection multiplicity. On the resolved model \(n=M^2\). For a pencil all pairwise intersections are base intersections, so \(n=0\).

For an irreducible system, restricting its sections to a general strict transform \(C\) gives the characteristic series
\[
\operatorname{im}\!\left(V\longrightarrow H^0(C,\mathcal O_C(M))\right),
\qquad \deg\mathcal O_C(M)=n.
\]
The kernel is the line generated by the section defining \(C\). Therefore its projective dimension is \(r-1\), yielding a \(g_n^{r-1}\). The curve inequality \(h^0(C,A)\le \deg A+1\) for an effective line bundle gives
\[
r-1\le n,\qquad r\le n+1.
\]
One proof of the curve inequality is to impose vanishing at \(n+1\) distinct points: a nonzero section of degree \(n\) cannot vanish at all of them. Enriques gives this restriction argument, invoking the familiar curve-theoretic inequality rather than proving it. The hypothesis of an integral general member is indispensable: a higher-dimensional system of sums of fibers can have \(n=0\). The text itself discusses that case immediately afterwards, so its inequality should not be exported to all reducible systems.

The characteristic series need not be complete. Even for a complete \(|D|\), the exact sequence
\[
0\longrightarrow\mathcal O_X
\longrightarrow\mathcal O_X(D)
\longrightarrow\mathcal O_C(D)
\longrightarrow0
\]
shows that the cokernel of restriction injects into \(H^1(X,\mathcal O_X)\), with the subsequent map to \(H^1(X,\mathcal O_X(D))\). Thus its defect is at most \(q=h^1(\mathcal O_X)\), and equals \(q\) when \(H^1(\mathcal O_X(D))=0\). This is modern context for the characteristic series, not a result that Enriques has already established on p. 19. It links this chapter to the irregularity problem mentioned in the front matter and to the virtual characteristic series on p. 40.

For a system without fixed components, \(n=0\) means that its resolved morphism has one-dimensional image. To see this, a surface image would give \(M^2=(\deg f)\deg f(X)>0\), whereas a curve image gives a pullback from a curve and square zero. Stein factorization gives \(X\to B\to f(X)\), and the members are sums of fibers. This is the precise modern proof of Enriques's final argument on p. 19. It does not force \(B\) to be rational when the members are reducible.

Enriques attributes the characteristic series to Segre and Castelnuovo around 1890, specifically citing Castelnuovo's 1891 “Ricerche generali sopra i sistemi lineari di curve piane,” reprinted in the 1937 selected papers, pp. 137 ff. This historical citation is recorded as his citation; its entire 1891 text has not been rechecked here.

### I.4. The characteristic incidence property: the missing hypothesis is essential (pp. 19–20)

**Correct theorem.** Let \(T\) be a complete irreducible \(r\)-dimensional algebraic family of effective divisors on a smooth projective complex surface, with integral general member and \(r>1\). Suppose exactly one member contains \(r\) general points of the surface. Then the family is a projective linear subsystem of a complete linear system. For a family initially defined only on an open parameter set, its closure is the linear system; deleting arbitrary members obviously need not leave the entire projective space.

The statement at the end of p. 19 does not include irreducibility, and p. 20 calls it a simplifying supposition. It is an essential restriction. If \(f:X\to B\) is an irrational fibration, the family
\[
\left\{f^*(b_1+\cdots+b_r):(b_1+\cdots+b_r)\in\operatorname{Sym}^rB\right\}
\]
has dimension \(r\), and exactly one member contains \(r\) general points of \(X\). It is not a linear system: the degree-\(r\) divisors on \(B\) vary in \(\operatorname{Pic}^r(B)\), rather than in one linear-equivalence class. For example, on \(X=B\times\mathbf P^1\), restriction to a section of \(f\) would identify these varying classes if the family were linear.

This is not a newly discovered failure of Enriques's 1893 theorem. The cited original paper explicitly gives the same sums-of-fibers counterexample and then states the theorem for irreducible curves (Enriques, 1893, pp. 4–5). Thus the defensible repair is to restore Enriques's own original hypothesis. There is no reason to credit a later author with repairing a theorem already correctly formulated in 1893.

**What p. 20 proves.** For \(r=2\), Enriques forms a quotient surface from the groups of \(n\) common intersections, reducing to an incidence family of degree one. Pencils through two chosen points on that quotient are rational by §I.2. He identifies them with plane pencils and infers that the quotient curves are lines. He then sketches the induction, representing nets through fixed points as stars of planes. This is a substantial geometric proof sketch. It suppresses the construction of the algebraic quotient, the handling of exceptional/boundary incidence, and compatibility of the projective identifications. Those details should not be replaced by the bare assertion that an arbitrary set-theoretic incidence plane is an algebraic projective plane.

**A modern completion, supplied here.** First remove common fixed base conditions on a smooth model, and work on the dense open where the family and its incidence have their expected dimensions.

For a two-dimensional family, the members through a general point \(x\) form an index-one pencil: through \(x\) and a second general point there is exactly one member. There is only one positive-dimensional component of this pencil, since two such components, each containing moving integral curves through \(x\), would both sweep the surface and violate uniqueness. By §I.2 the pencil is linear. Two general members of the original family meet away from fixed base points. Otherwise all distinct members on the resolved model would be disjoint, incompatible with the positive-dimensional family of members through a general point. An intersection point may be chosen in the good open locus: requiring that an intersection lie on a prescribed proper curve has incidence dimension at most \(2r-1\), rather than \(2r\). The two members therefore lie in one of the linear pencils and are linearly equivalent.

For \(r>2\), impose \(r-2\) general points. The resulting two-dimensional families satisfy the preceding case. Pairs of members belonging to these nets dominate \(T\times T\): their parameter count is \(2(r-2)+4=2r\), and the fiber over a pair of distinct integral curves is finite, consisting of choices among their finitely many moving intersections. Hence two general original members are linearly equivalent. The family lies in some \(|D|\).

Finally, the condition of containing a point \(x\) is a hyperplane in \(|D|\). Intersecting the closure of \(T\) with \(r\) general point-incidence hyperplanes gives one reduced point, because the corresponding incidence map is generically one-to-one and separable. Boundary families of smaller dimension cannot contain \(r\) general surface points. Thus the projective degree of \(T\) is one; an integral projective variety of degree one is a linear subspace. This proves the asserted linearity. The argument uses only the base-point rationality theorem, standard incidence dimensions, and the elementary degree-one criterion, and avoids attributing an unverified modern proof to a named author.

### I.5. Bertini's two theorems and the actual historical gap (pp. 20–21)

**Smoothness theorem.** On a smooth variety in characteristic zero, a general member of a linear system has no singularities away from its base locus and fixed components. On a singular variety, the singular locus of the ambient variety must also be excluded. On the ordinary spatial model \(F\), apparent double points caused by identifying two distinct points of the normalization are not singularities of the intrinsic curve on \(X\). This distinction is required to reconcile the initial convention of p. 15 with the statement on p. 21.

Enriques's infinitesimal argument can be made rigorous directly. Locally write a pencil as \(u+t v=0\), and suppose a singular point \(x(t)\) of its general member moves algebraically with \(t\). Differentiating
\[
u(x(t))+t\,v(x(t))=0
\]
gives \(v(x(t))=0\), because the differential in the surface direction vanishes at a singular point. Therefore also \(u(x(t))=0\). Varying the pencil direction through a general member puts the point in every member. A fixed divisorial locus is treated as a fixed component, and after its removal the remaining locus is the base locus. To justify differentiating, one works at the generic point of a component of the singular incidence and uses separability in characteristic zero.

There is also a clean sheaf-theoretic proof. Over the complement \(U\) of the base locus, evaluation \(V\otimes\mathcal O_U\to L|_U\) is surjective. Its kernel is a vector bundle, and the universal incidence
\[
\mathscr I=\{(x,[s]):s(x)=0\}\subset U\times\mathbf P(V)
\]
is a projective bundle over the smooth \(U\). It is smooth. The generic fiber over \(\mathbf P(V)\) is regular, hence geometrically regular in characteristic zero; spreading out smoothness gives a dense open set of smooth members. This proves the theorem in its proper scope. Zariski's 1944 paper gives the intrinsic development; modern embedded and incidence forms are treated in the Stacks Project, Tags 0FD4 and 0G4C. Characteristic zero is substantive: a linear span of \(p\)th powers in characteristic \(p\) has nonreduced general members even without base points.

**Reducibility theorem.** If a linear system on a smooth projective surface has no fixed components and its general member is reducible, it is composed with a pencil, whose parameter curve need not be rational. After resolving the base ideal and taking Stein factorization, the system has the form
\[
f:X\longrightarrow B,\qquad
C=f^*(b_1+\cdots+b_d),
\]
with the degree-\(d\) point divisors varying in a linear series on \(B\). The letter \(r\) used on p. 21 for the number of components is not necessarily the earlier projective dimension \(r\); modern notation \(d\) avoids that collision.

A proof on the resolved surface makes the logical step precise. If the associated map has surface image, its line bundle \(M\) is nef and \(M^2>0\). The general divisor is smooth by the first theorem. It must be connected. Indeed, if a smooth member decomposed as disjoint effective divisors \(A+B\), then
\[
A\cdot B=0,\qquad A^2=M\cdot A\ge0,\qquad
B^2=M\cdot B\ge0.
\]
At least one square is positive; the Hodge index theorem would make the other square strictly negative unless that divisor were numerically zero. A nonzero effective divisor cannot be numerically zero because it meets an ample divisor positively. This is a contradiction. Smoothness and connectedness imply irreducibility. Consequently a reducible general member forces a curve image. Stein factorization gives connected fibers over a normal projective curve \(B\); generic smoothness makes the general connected fiber integral. Pulling back the hyperplane divisor on \(B\) gives the asserted sums. This is a complete modern reduction to Bertini, Stein factorization, and the Hodge index theorem, not a claim that Enriques proves those later tools here.

Adding back fixed components gives exactly the three alternatives on p. 21: a fixed part plus an irreducible moving part; a sum of several moving fibers; or that latter sum plus a fixed part. Systems of dimension greater than one and effective degree zero fall in the fiber-composed alternatives. The first theorem concerns a **general** member; special singular or reducible members are allowed and ubiquitous.

**Historical assessment.** Enriques explicitly refers to Enriques–Chisini, Book II, chapter I, §5, volume I, p. 180, and cites his 1893 and 1896 papers. His component-motion argument does leave the algebraicity of the families of components implicit. Here a named repair is verifiable: van der Waerden (1937, especially p. 709) supplies this missing algebraic-family step using Chow coordinates; Zariski (1941) gives another rigorous proof. Kleiman (1998, §5, Theorem 5.3) identifies this precise gap in the Enriques–Campedelli treatment and reconstructs the argument. This supports a specific diagnosis, not the assertion that the entire Italian proof was invalid. The derivative proof of the first theorem is itself repairable and essentially sound.

The citation “Bertini ... 1880” on p. 20 is a manuscript date: the paper appeared in 1882. The p. 21 reference to Noether, volume VIII, “1874” is bibliographically inaccurate for the cited volume-8 paper, which appeared in 1875, pp. 495–533. Moreover, the historical assertion that Noether had already observed the reducibility theorem is stronger than what Kleiman's examination supports: he reports that Noether did not clearly formulate or prove a particular case. Accordingly the ledger records Enriques's attribution as an attribution, not as independently established priority.

### I.6. The map defined by a linear system and its exceptional behavior (pp. 22–24)

For \(V=\langle\varphi_0,\ldots,\varphi_r\rangle\), the map is
\[
\phi_V:X\dashrightarrow\mathbf P(V^\vee),\qquad
x\longmapsto[\varphi_0(x):\cdots:\varphi_r(x)].
\]
The members through \(x\) form a hyperplane of \(V\), equivalently the star of hyperplanes through \(\phi_V(x)\). This proves the intrinsic construction described on p. 22 and its coordinate formula on p. 23.

When the general member is integral and \(r\ge2\), the image is a surface, apart from the pencil case already separated. On a resolution let \(M=\phi_V^*\mathcal O(1)\), and let \(m=[\mathbf C(X):\mathbf C(Y)]\) be the generic degree onto the reduced image \(Y\). Then
\[
n=M^2=m\deg Y,\qquad \deg Y=\frac n m.
\]
This follows by pulling back two general hyperplanes: they meet \(Y\) in \(\deg Y\) general points, each with \(m\) preimages. Thus the opening assertion “image of order \(n\)” on p. 22 is valid in the birational case, and the later paragraph explicitly corrects it to \(n/m\) for a composite system. It should not be extracted without that qualification.

Enriques calls the general fibers of such a degree-\(m\) map an “involution.” This does not mean an automorphism of order two, or even a quotient by a group: a finite function-field extension need not be Galois. A “simple” system is one for which \(m=1\), hence one giving a birational map onto its image. His dimension count for simplicity when \(r\ge3\) is a genericity heuristic, not a proof that every such system is simple; the text itself immediately gives counterexamples. A general projection of an embedding to \(\mathbf P^3\) is birational, but a specified subsystem can factor through a multiple cover.

For a net, \(r=2\), the nondegenerate surface image is \(\mathbf P^2\), so the degree of the map is \(n\). This is the “multiple plane.” The branch locus is more precisely the discriminant locus of the finite map obtained after resolution and Stein factorization. At a general simple branch point two points of the fiber coalesce. Arbitrary nets can have higher ramification, so “a double point in the group” is not a blanket theorem of simple branching.

**A genuine printed error.** At the bottom of p. 22, let \(F\subset\mathbf P^3\) have degree \(m\), and take degree-\(a\) cones with a fixed vertex outside \(F\). Projection from the vertex has degree \(m\); the cone system is its composition with the degree-\(a\) Veronese map of \(\mathbf P^2\). Therefore
\[
M=aH,\qquad M^2=ma^2,\qquad
\deg(\text{image})=a^2.
\]
Enriques uses \(n\) for the cone order and the scan prints \(mn\), without a square. The correct effective degree is \(mn^2\). This is not an OCR error: the transcription is faithful at this point. The calculation also confirms that the map belongs to an involution of degree \(m\), as claimed.

The asserted relation between birational geometry with a chosen simple system and projective geometry of its image is exact in the following sense. A birational map identifying two systems identifies their spaces of sections up to scalars and hence gives a projective equivalence of the image models; conversely a projective equivalence of birational image models lifts to the birational identification. A subspace \(W\subset V\) gives the linear projection
\[
\mathbf P(V^\vee)\dashrightarrow\mathbf P(W^\vee)
\]
with center \(\mathbf P(\ker(V^\vee\to W^\vee))\). The intersection of this center with the image records the base scheme of \(W\); a fixed component records a divisorial part of that intersection. Enriques sketches these correspondences correctly. On a singular or nonnormal image the full scheme structure, not just the set of intersection points, is needed.

**One ordinary base point.** Blow up a smooth point \(O\) of multiplicity \(i\). If there is no fixed tangent, the leading homogeneous forms give a base-point-free subsystem of
\[
H^0(E,\mathcal O_E(i)),\qquad E\simeq\mathbf P^1.
\]
Consequently \(M\cdot E=i\). What always follows is
\[
\deg(E\longrightarrow\phi(E))\cdot\deg\phi(E)=i.
\]
The stronger claim on p. 23 that the image curve itself has degree \(i\) requires degree one on \(E\). It is valid for the standard sufficiently separating model, but does not follow just from global birationality and the absence of fixed tangents.

**Explicit counterexample, constructed here.** On \(\mathbf P^2\), use
\[
[x:y:z]\longmapsto[x^2z:y^2z:x^3:y^3].
\]
The only base point is \(O=[0:0:1]\), of multiplicity two, with no common tangent factor. On a dense open the inverse affine coordinates are \(x/z=X_2/X_0\) and \(y/z=X_3/X_1\), so the map is birational. On the exceptional curve of the blowup it becomes
\[
[u:v]\longmapsto[u^2:v^2:0:0],
\]
a degree-two map onto a line. The image degree is one, not \(i=2\). The moving class is \(3H-2E\), whose square is five; its image has equation \(X_0^3X_3^2-X_1^3X_2^2=0\) and is nonnormal along the image line. This example shows exactly which exceptional separation condition is missing. Confidence is high: the base ideal, inverse coordinates, restriction to \(E\), image equation, and intersection number are all explicit.

**One additional simple infinitely near point.** If the base cluster is \(O\) of multiplicity \(i\) followed by one simple point \(O_1\), and no further base points, use total exceptional classes \(E_0^*,E_1\):
\[
M=\pi^*D-iE_0^*-E_1,\qquad
E_0'=E_0^*-E_1,\qquad
M\cdot E_0'=i-1,\quad M\cdot E_1=1.
\]
This proves the degree splitting \(i-1+1=i\) asserted in the standard birational model. As above, intersection degrees must be divided by mapping degrees when a component is mapped multiply. If \(i=1\), \(E_0'\) is a \((-2)\)-curve with zero \(M\)-degree. In the normal model contracting just that curve, its image is the ordinary \(A_1\) double point, analytically \(ab=c^2\), and the image of \(E_1\) is a line through it. This is the quadric-cone model invoked by Enriques. Normality and the exclusion of additional contracted components are needed for this exact singularity type.

**The note on p. 24.** The asserted correspondence between exceptional components and “branches” is too loose to serve as a modern counting theorem. Exceptional divisors on a smooth resolution are indexed by blowup centers, with their incidence and multiplicities determined by proximity; they are not in general counted by the analytic branches of one plane-curve germ. An ordinary multiple point has several analytic branches but one exceptional component after its first blowup; a unibranch singularity such as \(y^2=x^5\) needs repeated blowups even just to make its strict transform smooth. Further contractions can alter the number of components visible on a singular image. The correct invariant data are the cluster of infinitely near points, its proximity relations, and the total versus strict exceptional divisors. Enriques explicitly cites that theory and returns to it in §§11–12, so the comment is best treated as an imprecise preview rather than substituted for his later formulas.

The cited paper is Barber and Zariski (1935), “Reducible exceptional curves of the first kind,” pp. 119–141. The scan's “E. Barber” is a wrong initial; the author is S. F. Barber. The journal is American Journal of Mathematics, whereas the scan really prints “Mathematik.” The abbreviated Du Val reference has been identified against the journal issue as Du Val (1936), “Reducible exceptional curves,” pp. 285–289. It must not be confused with his 1934 papers on isolated surface singularities.

### I.7. Linear equivalence and complete systems (pp. 24–26)

Two effective divisors \(C,K\) are linearly equivalent if \(C-K=\operatorname{div}(t)\) for some nonzero rational function. Equivalently they are members of one linear system; distinct members span a pencil and a single member gives dimension zero. Equal degree in a chosen embedding is a consequence, not a sufficient condition. The identification with zero and pole curves is literal when the effective divisors have no common components; otherwise their common part is cancelled, or retained as a fixed part of the pencil.

Reflexivity uses \(t=1\), symmetry uses \(1/t\), and transitivity uses products or quotients. With Enriques's choices
\[
\operatorname{div}(t)=K-C,\qquad
\operatorname{div}(\tau)=K-L,
\]
one gets \(\operatorname{div}(\tau/t)=C-L\). Thus the quotient on pp. 24–25 has the right sign. There is no hidden sign error to correct.

**Completeness theorem.** The totality of effective divisors linearly equivalent to \(C\) is
\[
|C|=\mathbf P H^0(X,\mathcal O_X(C)).
\]
A section represented by \(f\) corresponds to the effective divisor \(C+\operatorname{div}(f)\). Two nonzero sections give the same divisor exactly when their ratio is a nonzero constant. Conversely every linearly equivalent effective divisor has this form. The finiteness of \(H^0\) on a projective variety makes this a finite-dimensional projective linear system. This proves both existence and uniqueness of the complete system and shows that it can be recovered from any one member. Enriques gives the rational-function construction and uniqueness argument; modern sheaf cohomology supplies a uniform finiteness statement even outside the irreducible moving situation.

The enlargement procedure on p. 25 is valid after fixing the divisor class and the prescribed base conditions: any strictly increasing chain of subspaces of \(H^0\) must terminate, and their unique maximal member is \(H^0\) itself. The earlier bound \(r\le n+1\) justifies termination only in its irreducible moving setting. It should not be applied to a reducible degree-zero system. This is a limitation of the suggested proof, not a failure of the completeness theorem.

**Completeness does not imply base-point-freeness.** Enriques actually says “in general,” then introduces the convention “virtually” without base points. These words must not be promoted to a universal theorem. For a concrete counterexample, blow up eight general points of \(\mathbf P^2\). Cubics through them form a complete pencil on the blowup and still have a ninth base point, by Bézout. Its general member is an integral cubic. Completeness means that all sections of the given line bundle have been used; it does not say that they generate the line bundle at every point.

A complete system with prescribed base cluster \((p_j,m_j)\) is
\[
\mathbf P H^0\!\left(Y,\pi^*\mathcal O_X(C)
                 \otimes\mathcal O_Y(-\sum m_jE_j^*)\right)
\]
on the blown-up surface. Equivalently it is a complete space of sections satisfying the corresponding ideal conditions on \(X\). The exceptional divisors appearing in the total pullback must be subtracted to obtain the strict/moving transform. After further blowing up any remaining base points, the moving series is base-point-free. Enriques correctly stresses this subtraction. His maximality statement “same degree” concerns the moving degree with those base conditions retained; removing imposed conditions can increase that degree.

**What “normal surface” means here.** Fix a smooth or normalized model and its hyperplane line bundle \(L\). Enriques calls an image normal when its hyperplane sections give the complete intrinsic system \(H^0(L)\), so that it cannot be lifted to a larger projective space by adjoining missing sections while preserving the degree. If the embedded surface is already smooth, this is modern linear normality. If the image is nonnormal, it refers to sections on the normalization and is stronger than ambient restriction onto \(H^0(F,\mathcal O_F(1))\). In fact every hypersurface in \(\mathbf P^3\) has surjective restriction of linear forms, whereas Enriques's quintic example still lifts from \(\mathbf P^3\) to \(\mathbf P^5\). Calling both notions simply “linear normality” without naming the model would conceal that difference. Neither intrinsic completeness nor linear normality is the same as projective normality, which also concerns higher multiplication maps and the homogeneous coordinate ring.

The uniqueness of the final complete image in pp. 25–26 is consequently a uniqueness for the fixed polarized birational model: any two bases of \(H^0(L)\) differ by an invertible linear transformation. All chains of adjoining sections end in the same projective model up to projective equivalence. It is not a general uniqueness theorem for all projective embeddings of the underlying surface.

**The quintic example, reconstructed.** Let
\[
S=\operatorname{Bl}_{A_1,\ldots,A_4}\mathbf P^2,
\quad D=3H-E_1-\cdots-E_4=-K_S,
\]
with the four points in general position. Cubics form a vector space of dimension ten; the four independent point conditions leave \(h^0(D)=6\). Also
\[
D^2=9-4=5,\qquad
p_a(D)=1+\frac{D(D+K_S)}2=1.
\]
The complete system embeds the degree-five del Pezzo surface in \(\mathbf P^5\). A four-dimensional vector subspace \(V\subset H^0(D)\) gives a general quintic image in \(\mathbf P^3\). Intermediate five-dimensional subspaces \(W\) containing \(V\) are parametrized by
\(\mathbf P(H^0(D)/V)\simeq\mathbf P^1\), explaining Enriques's \(\infty^1\) family of lifts to \(\mathbf P^4\). The final six-dimensional system is unique.

The intermediate models are generally projectively inequivalent. One must read “birationally distinct” here as “not carried to one another with their specified linear systems”; all the surfaces themselves are rational and hence birational. The polarized automorphism group of the smooth degree-five del Pezzo surface is finite, namely \(\mathfrak S_5\), so it cannot identify a one-parameter family into a single projective orbit. Special coincidences need not be ruled out by this argument. The anticanonical model and this automorphism group are verified in Bauer and Catanese (2021, §2).

Enriques additionally specifies a degree-five double curve lying on a quadric cone and one triple point at its vertex. These details are stated without a calculation. Here is a modern reconstruction for a general projection with ordinary singularities. The conductor divisor on \(S\) is
\[
\Delta=(5-4)D-K_S=2D,
\]
so \(D\Delta=10\); since it maps two-to-one onto the double curve \(B\), \(\deg B=5\). Adjunction gives \(p_a(\Delta)=6\). The conductor exact sequence gives
\[
\chi(\mathcal O_F)=\chi(\mathcal O_S)+\chi(\mathcal O_B)
                 -\chi(\mathcal O_\Delta).
\]
Here the quintic hypersurface has \(\chi(\mathcal O_F)=5\), the rational smooth model has \(\chi(\mathcal O_S)=1\), and \(\chi(\mathcal O_\Delta)=-5\). Hence \(p_a(B)=2\).

Let \(t\) be the number of ordinary triple points and \(b\) the number of pinch points. The rank-one degeneracy locus of \(df:T_S\to f^*T_{\mathbf P^3}\) has, by the Thom–Porteous formula,
\[
b=c_2(f^*T_{\mathbf P^3}-T_S)
 =6D^2+4D K_S+K_S^2-c_2(S)
 =30-20+5-7=8.
\]
An ordinary triple point contributes three nodes to \(\Delta\), but contributes delta invariant two to the spatial curve \(B\), whose three tangents are not coplanar. Normalizing and applying Riemann–Hurwitz to the two-to-one conductor cover yields
\[
-5+3t=2(-1+2t)-\frac b2.
\]
Thus \(t=1\). These equations also work componentwise, using Euler characteristics if a conductor curve is disconnected. The unique quadric adjoint is explained by
\[
H^0(\mathbf P^3,\mathcal I_B(2))
\simeq H^0(S,\mathcal O_S(2D-\Delta))
\simeq\mathbf C.
\]
At the triple point its gradient must vanish because the three tangent directions of \(B\) span the ambient tangent space. The quadric cannot split into two planes: its pullback is the reduced divisor \(\Delta\), so no component of \(B\) can lie in both planes. Each plane pullback would then map two-to-one onto the double-curve components it supports, forcing its hyperplane degree \(D^2=5\) to be even. A double plane would likewise give a nonreduced pullback. Thus the unique quadric is irreducible and singular, hence a quadric cone, and the triple point is its vertex. This reconstruction uses the ordinary-projection hypotheses, the conductor computation in §I.8, and the standard degeneracy-locus theorem (Fulton, 1998, §14.4). It is additional analysis here, not a proof present on p. 26.

### I.8. Sums, differences, Noether's residual theorem, and virtual divisors (pp. 26–30)

**Addition and the distinction between two sums.** If \(C_1\sim C_2\) and \(K_1\sim K_2\), multiplication of their rational functions gives
\[
C_1+K_1\sim C_2+K_2.
\]
If positive and negative components overlap, the principal divisor cancels them; the displayed equivalence still holds. The complete sum is \(|C+K|\). The smallest linear system containing every sum of a member of \((L,V)\) and a member of \((N,W)\) is instead
\[
\mathbf P\,\operatorname{im}
\left(V\otimes W\longrightarrow H^0(X,L\otimes N)\right).
\]
This is Enriques's minimal sum. The multiplication map need not be onto, even if the two starting systems are complete relative to their assigned conditions.

If the two positive-dimensional systems have integral general members and are not the same pencil, their minimal sum already has a surface image. Indeed its map is the Segre composite of their two maps; a curve image would force both systems to come from the same one-dimensional fibration. Bertini then makes its general member irreducible. The complete sum, which contains it, is also generically irreducible. In particular multiples of a non-pencil irreducible moving system are irreducible in this sense. The pencil exception means that the argument gives no such guarantee. It must not be read as a claim that every unrestricted multiple of every pencil remains reducible: base-point conditions may disappear when the complete divisor class is enlarged.

The sentence that assigned base points remain base points in the sum is correct only with its adjective “assigned”: prescribed vanishing conditions are retained in taking the relative complete sum. It is false for the unrestricted complete divisor class. For example, pencils of lines through two different points of \(\mathbf P^2\) both have class \(H\), but \(|2H|\) is the base-point-free complete system of conics. In the relative interpretation the imposed conditions persist, and their multiplicities add at any common base point.

**The quadric example and its degree restriction.** Put \(O=[0:0:0:1]\) on a smooth degree-\(d\) surface \(F\subset\mathbf P^3\). Hyperplanes through \(O\) give a three-dimensional vector space. Their pairwise products span the six-dimensional space of quadratic forms in \(x_0,x_1,x_2\), namely cones with vertex \(O\). A quadric section has multiplicity at least two at \(O\) on \(F\) precisely when its value and its two tangent derivatives vanish: three independent linear conditions in the ten-dimensional space of quadrics leave dimension seven. For \(d\ge3\), restriction of quadrics to \(F\) is injective, so Enriques's projective dimensions are
\[
\mathbf P^5\subsetneq\mathbf P^6.
\]
This proves the claimed failure of the minimal double to be complete relative to the double base point.

The printed example says merely “degree \(n\)” and needs \(n\ge3\). If \(F\) is a smooth quadric, its own equation lies in the seven-dimensional tangency space and vanishes on \(F\), leaving only six independent restrictions. The six cone quadrics restrict injectively and already fill the system; both projective dimensions are five. For a plane, the starting hyperplane-section system itself drops dimension. These are genuine omitted low-degree qualifications, not transcription errors.

**Residual systems and the exact algebra.** If an effective member of \(|C|\) is \(K+L\), the residual system to \(K\) is
\[
|C-K|=\mathbf P H^0(X,\mathcal O_X(C-K)).
\]
Multiplication by the canonical section of \(\mathcal O_X(K)\) identifies it with the subspace of \(|C|\) consisting of divisors containing \(K\). If \(K'\sim K\), then \(\mathcal O_X(C-K')\simeq\mathcal O_X(C-K)\), so the **complete residual system** is the same. Equivalently, every effective \(L\sim C-K\) satisfies \(L+K'\sim C\). This proves the residual theorem on pp. 27–28 and the identities \(|C-K|=|L|\), \(|L+K|=|C|\).

Completeness is essential. For an arbitrary incomplete subsystem \(V\subset H^0(C)\), the residual vector space is the inverse image of \(V\) under multiplication by the particular section \(s_K\); replacing \(K\) by a linearly equivalent divisor can change it. The italic formulation on p. 28 uses “a system \(|C|\),” but its immediately preceding construction explicitly assumes the complete system. The modern statement must retain that assumption.

**The projective complement, asserted for later proof on p. 28.** This is distinct from the intrinsic residual theorem. For a smooth hypersurface \(F\) of degree \(d\),
\[
0\longrightarrow\mathcal O_{\mathbf P^3}(e-d)
\longrightarrow\mathcal O_{\mathbf P^3}(e)
\longrightarrow\mathcal O_F(e)\longrightarrow0.
\]
Since \(H^1(\mathbf P^3,\mathcal O(k))=0\) for every integer \(k\), all sections of \(\mathcal O_F(e)\) are cut by degree-\(e\) ambient surfaces. This is completeness of the ambient cut, not merely an asymptotic assertion.

For an ordinary singular hypersurface, let \(\nu:X\to F\) be its smooth normalization, \(B\) its reduced double curve, and \(\Delta\) the conductor divisor on \(X\). The conductor ideal on \(F\) is
\[
\mathfrak c=
\mathcal H om_{\mathcal O_F}(\nu_*\mathcal O_X,\mathcal O_F)
=\mathcal I_{B/F}=\nu_*\mathcal O_X(-\Delta).
\]
The equality with the reduced double-curve ideal can be checked in the ordinary local models \(xy=0\), \(xyz=0\), and \(x^2=y^2z\). At the pinch point, normalize by \(y=u,\ x=uv,\ z=v^2\); the conductor is \((x,y)\) downstairs and \((u)\) upstairs. At a triple point it is the ideal \((xy,xz,yz)\); on each normalization branch it cuts the two intersecting conductor curves.

Writing \(H=\nu^*\mathcal O_F(1)\), restriction gives
\[
0\longrightarrow\mathcal O_{\mathbf P^3}(e-d)
\longrightarrow\mathcal I_B(e)
\longrightarrow\nu_*\mathcal O_X(eH-\Delta)
\longrightarrow0.
\]
The same vanishing therefore proves that adjoint surfaces of degree \(e\), passing through \(B\), cut the complete residual system \(|eH-\Delta|\). Finite duality and hypersurface adjunction identify
\[
K_X\sim(d-4)H-\Delta,\qquad
eH-\Delta\sim K_X+(e-d+4)H.
\]
Thus this is also the modern canonical meaning of “adjoint.” No gap in the truth of the p. 28 completeness assertion appears under the ordinary-singularity convention. For arbitrary singularities one must use the conductor or adjoint ideal; passage through only the reduced singular locus is not sufficient. The required standard facts are the Stacks Project, Lemma 30.8.1, Tag 01XS, and finite duality in Remark 48.20.12, Tag 0AU5. The local conductor checks and exact-sequence argument have been given here.

Noether's Restsatz consequently has the two parts Enriques explicitly distinguishes: intrinsic independence of the complete residual system from the representative of \(K\), and completeness of the projectively cut adjoint system. Once both are available, every \(C'\sim C\) is residual to every \(K'\sim K\) in the appropriate complete adjoint class. The book cites Noether, Mathematische Annalen VIII, and, for the curve analogue, Brill–Noether VII and Enriques–Chisini, Book V; p. 28 postpones the projective proof rather than pretending it has just proved it.

**Subtraction can destroy irreducibility and introduce base loci.** If \(f:X\to\mathbf P^1\) has connected fibers \(L\) and no base points, then
\[
H^0(X,\mathcal O_X(2L))\simeq H^0(\mathbf P^1,\mathcal O(2)).
\]
A general member of \(|2L|\) is the sum of two fibers. Choose a moving system \(K\) such that \(|K+2L|\) is irreducible; subtracting \(K\) leaves this reducible system. On \(\mathbf P^1\times\mathbf P^1\), \(|(1,2)|-|(1,0)|=|(0,2)|\) makes the example explicit. On \(\operatorname{Bl}_p\mathbf P^2\), \(|H|-|(H-E)|=|E|\) gives an irreducible starting system whose residual has a fixed exceptional component. On the blowup of eight general plane points, taking \(C=nA\), with \(A\) ample and \(n\) large, and choosing an effective \(K\sim nA+K_X\), gives residual \(|-K_X|\), the cubic pencil with a ninth base point described above. Blowing up a newly created base point turns its contribution in the total pullback into a fixed exceptional component, exactly as on p. 29.

**Virtual divisors.** If \(H^0(X,\mathcal O_X(C-K))=0\), the effective residual system is empty, but the divisor class \(C-K\) remains meaningful in \(\operatorname{Pic}(X)\). Formal differences of effective classes obey
\[
C-K\sim L-M
\iff C+M\sim K+L.
\]
Addition is associative in the divisor class group:
\[
D+(C-K)=D+C-K.
\]
If \(A\) is ample, \(\mathcal O_X(mA+C-K)\) has sections, and is indeed globally generated, for \(m\gg0\). This supplies the precise meaning of “sufficiently ample” in p. 29; it follows from the ample-twist theorem and Serre vanishing, not from a numerical assertion about an arbitrary large self-intersection. Conversely every line bundle on a projective variety is a difference of effective divisors after such a twist. The analogy with negative numbers is the group completion of the monoid of effective divisor classes.

Enriques also proposes the narrower notion of a noneffective class having an effective positive multiple. That is a separate condition, not the definition of all virtual classes. For example, \(-H\) on \(\mathbf P^2\) has no effective positive multiple. By contrast, on \(E\times\mathbf P^1\) let \(M\ne\mathcal O_E\) be an order-\(a\) torsion line bundle and put
\[
L=p_E^*M\otimes p_{\mathbf P^1}^*\mathcal O(1).
\]
Then \(H^0(L)=0\) because a nontrivial degree-zero line bundle on an elliptic curve has no section, but
\[
L^{\otimes a}\simeq p_{\mathbf P^1}^*\mathcal O(a),
\qquad h^0(L^{\otimes a})=a+1.
\]
This is an explicit noneffective virtual class with effective nonzero multiples. It is an example supplied here, not attributed to Enriques.

The historical paragraph continuing onto p. 30 credits the idea to Enriques's canonical-class work of 1893–1896, the terminology “virtual curve” to Severi (1905), and the topological interpretation to Lefschetz. Its mathematically precise topological map is
\[
\operatorname{Pic}(X)\longrightarrow H^2(X,\mathbf Z),
\qquad L\longmapsto c_1(L),
\]
or the Poincaré-dual two-cycle class on the underlying compact oriented four-manifold. This does not identify virtual divisors with all two-cycles and does not recover linear equivalence: classes in \(\operatorname{Pic}^0(X)\) have zero first Chern class. The historical priority claims are retained as statements made by the book; the specific 1905 Severi paper and an exact Lefschetz passage were not independently read in this audit.

### Additional examples and questions for §§1–8

The explicit cubic map in §I.6 is a useful test case for every statement that turns the intersection number \(M\cdot E\) into the degree of the image of \(E\). Its calculation is complete and the confidence is high. A natural further exercise is to compute the conductor of its nonnormal quintic image and compare its normalization with the ordinary projected model used elsewhere in the chapter.

The product \(B\times\mathbf P^1\) gives a controlled laboratory for three distinctions at once: irrational versus linear pencils, algebraic versus linear equivalence, and the essential irreducibility hypothesis in Enriques's incidence theorem. The counterexample to an unrestricted converse is proved above and was already recognized by Enriques in 1893; the choice to organize these distinctions around one product example is ours.

The multiplication map \(V\otimes W\to H^0(L\otimes N)\) provides a concrete extension of “minimal sum.” One can compute its cokernel for the quadric example, then ask what positivity conditions make it surjective. That is a projective-normality and syzygy question, not an automatic consequence of completeness. No unverified general surjectivity theorem is being asserted.

Finally the conductor formulation isolates exactly why the ordinary-singularity hypothesis matters. Replacing an ordinary model by a non-seminormal singular model and comparing its conductor with the reduced singular locus would test which classical adjoint arguments survive. This is a proposed exercise/research direction, not a claim that the general conductor theory is open. None of the corrected characteristic-zero statements treated in these pages is presented here as an unresolved theorem.

### I.9. The image of a sum of linear systems (pp. 30–31)

Throughout this section, work on a smooth projective complex surface \(X\), after resolving the assigned base points of the systems. The symbol \(K\) in Enriques's \(|C+K|\) denotes an auxiliary system; it is **not** the canonical divisor, which will be written \(K_X\). If \(V\subset H^0(X,L)\) and \(W\subset H^0(X,M)\) have dimensions \(r+1\) and \(s+1\), the minimum sum is the projectivization of

\[
U=\operatorname{im}\bigl(V\otimes W\longrightarrow H^0(X,L\otimes M)\bigr).
\]

Its map is the product of the two rational maps followed by the Segre embedding, with any linear dependencies among the products removed. The complete sum uses all of \(H^0(X,L\otimes M)\). Enriques's assertion that the image is generally a surface and \(R=\dim U-1>r+s\) has a general-position qualification in the printed text. It must not be universalized: two copies of one pencil give a conic image and \(R=2=r+s\). The construction in the ensuing paragraphs concerns two systems whose joint map has two-dimensional image. A common finite correspondence can still make that map generically many-to-one (Enriques, 1949, p. 30).

The strict dimension inequality can be justified in the intended case, with both systems positive-dimensional and with integral general members, as in the preceding discussion. The family of sums of one integral member from each system has dimension \(r+s\): the decomposition of a general divisor into its two integral components is unique, up to the finite interchange when appropriate. These sums are reducible. The minimum sum has an irreducible general member when its joint map has two-dimensional image, by the Bertini argument of §8. Thus the \(r+s\)-dimensional family of decomposable members is a proper closed subset of \(\mathbf P(U)\), forcing \(R>r+s\). This proves the bound rather than assuming injectivity of the entire multiplication map.

Here is the linear algebra behind the construction, including the step that Enriques leaves implicit. Choose \(c_0\in V\), \(k_0\in W\) with divisors \(C_0,K_0\) having no common component. The subspaces \(k_0V,c_0W\subset U\) meet precisely in the line spanned by \(c_0k_0\): a section divisible by both divisors is divisible by their sum, and the quotient is a global regular function on the connected projective surface. The subsystem

\[
U_0=k_0V+c_0W,\qquad \dim U_0=r+s+1,
\]

therefore gives a map to \(\mathbf P^{r+s}\). It is the projection from the common \(\mathbf P^{R-r-s-1}\) of the two centers in \(\mathbf P^R\). The fixed \(K_0\) lies in the center \(\mathbf P^{R-r-1}\), and fixed \(C_0\) in \(\mathbf P^{R-s-1}\). After projection they lie in \(\mathbf P^{s-1}\) and \(\mathbf P^{r-1}\), respectively. On the open set \(c_0k_0\ne0\), the coordinates recover all ratios \(c_i/c_0\) and \(k_j/k_0\). Thus the projected map generates exactly the joint function field of the two original maps. It is birational precisely when that field is \(\mathbf C(X)\). This proves the assertion about systems not belonging to a common involution, with “involution” read as their common generic finite equivalence relation, not as an automorphism of order two.

Two small **printed errors** occur in this otherwise sound argument. The ambient space in the second paragraph is printed \(S_r\), although it must be \(S_R\). The following paragraph interchanges \(C\) and \(K\) when naming the curves in the two centers. Both discrepancies are present in the scan; neither should be attributed to the transcription. The dimensions following the projection and the specialization \(r=2,s=1\) confirm the intended assignment.

For the net–pencil case, choose coordinates

\[
[c_0k_0:c_1k_0:c_2k_0:c_0k_1]\in\mathbf P^3.
\]

The curve \(K_0\) goes to \(O=[0:0:0:1]\), while \(C_0\) maps to the line \(a=\{x_0=x_3=0\}\), which does not contain \(O\). Planes through \(O\) cut the net and planes through \(a\) cut the pencil. Write \(C^2=n\), \(C\cdot K=i\), and \(K^2=0\) on the model where the pencil is a morphism. Assuming the chosen \(C_0,K_0\) meet transversely in \(i\) points, blow those points up, with exceptional divisors \(E_1,\ldots,E_i\). The moving divisor of the four-dimensional vector space above is

\[
D=\pi^*(C+K)-\sum_{j=1}^{i}E_j,\qquad
D^2=n+i.
\]

Consequently a birational image has degree \(n+i\). Each \(E_j\) has \(D\cdot E_j=1\), so maps to a line. These are the \(i\) lines in the plane \(Oa=\{x_0=0\}\) left after removing the multiple line \(a\). The net contributes multiplicity \(i\) at \(O\); a general plane through \(a\) has residual pencil member of degree \(i\), so \(a\) has multiplicity \(n\). These are generic statements about the prescribed model. Nontransverse intersections must be replaced by their scheme lengths and infinitely near contributions; if the joint map has degree \(d>1\), the basic identity is \(D^2=d\deg\Phi\), rather than \(\deg\Phi=D^2\). Enriques explicitly imposes birationality before his degree computation (pp. 30–31).

Finally, products of a plane through \(O\) with one through \(a\) span the quadrics through \(O\cup a\). Their ambient vector space has dimension \(10-3-1=6\), hence projective dimension five. Restricting them to the surface and removing fixed parts recovers the minimum sum. This does not assert that the restricted system always has dimension five: when the image surface itself is a quadric, its equation gives a relation. This distinction prevents an artificial “dimension error” in Enriques's last paragraph.

**Assessment.** Enriques gives a genuine geometric construction, including the birationality condition and its numerical consequences. The modern calculation above fills in kernels, dimensions, and base schemes; it does not replace a false theorem. The two letter-level source slips are separately recorded in the correction ledger.

### I.10. Virtual degree and virtual genus (pp. 31–33)

#### Addition and the intrinsic definitions

For Cartier divisors \(A,B\) on \(X\), the modern statements are

\[
(A+B)^2=A^2+B^2+2A\cdot B,\qquad
p_a(A+B)=p_a(A)+p_a(B)+A\cdot B-1,
\]

where

\[
p_a(D)=1+\frac{D^2+D\cdot K_X}{2}.
\]

For an effective divisor this equals \(1-\chi(\mathcal O_D)\); for a formal divisor class the same numerical expression defines its virtual arithmetic genus. Enriques writes these as \(n=n_1+n_2+2i\) and \(\pi=\pi_1+\pi_2+i-1\), with degrees and genera evaluated after resolving the assigned base cluster. If the general curves are smooth there, their geometric genera equal these arithmetic genera. The first formula is bilinearity; Enriques assumes the second from Noether and cites Enriques–Chisini, book V, vol. III, p. 399 (Enriques, 1949, p. 31).

A proof valid also for nonreduced divisors uses

\[
0\longrightarrow\mathcal O_X(-D)\longrightarrow\mathcal O_X
\longrightarrow\mathcal O_D\longrightarrow0
\]

and surface Riemann–Roch. The latter says

\[
\chi(\mathcal O_X(D))=\chi(\mathcal O_X)
+\frac{D\cdot(D-K_X)}2.
\]

Subtracting Euler characteristics gives the displayed genus formula; expanding its quadratic expression gives the addition formula. This explains precisely the “continuity” used in the text: Euler characteristic is constant in a flat proper family, whereas normalization genus can drop. The required intersection and Riemann–Roch framework is given in Beauville (1996, chap. I); an independently accessible proof is Vakil (2002, class 6, §2). No claim is made that these modern expositions were the first historical repairs.

Enriques defines the virtual degree of an isolated curve \(C\) by choosing \(|K|\) such that \(|K|\) and \(|C+K|\) have irreducible general members, then setting

\[
n=N-m-2i,\qquad N=(C+K)^2, m=K^2, i=C\cdot K.
\]

Existence of such an auxiliary system follows by taking an ample \(H\) and \(m\gg0\), so that both (mH-C) and (mH) are very ample. Its independence is not merely asserted: p. 32 computes the degree of \(C+K_1+K_2\) in two orders and cancels terms to obtain \(n_1=n_2\). This is a complete algebraic verification once the addition formula and the availability of sufficiently positive auxiliaries are granted. The analogous genus calculation, only indicated in the text, is

\[
p_a(C+K_1+K_2)
=p_a(C)+p_a(K_1)+p_a(K_2)
+C K_1+C K_2+K_1K_2-2.
\]

It is visibly symmetric in \(K_1,K_2\). The same argument applies to differences (C-K), regardless of whether their linear systems contain an effective divisor. Serre vanishing and very-ampleness after sufficiently high twisting supply the auxiliary systems (Stacks Project, Tag 0B5U).

Multiple components cause no failure. For an integral \(C\) and integer \(m>0\), for example,

\[
(mC)^2=m^2C^2,\qquad
p_a(mC)=1+m(p_a(C)-1)+\frac{m(m-1)}2C^2.
\]

This is the scheme-theoretic genus, not the genus of the reduced support. It can be negative. The assertion on p. 32 is therefore stronger and more useful than a statement only about smooth moving curves.

#### Birational behavior and assigned points

Let \(\pi:Y\to X\) blow up a smooth point \(p\in X\), with exceptional divisor \(E\), and let a curve \(C\) have multiplicity \(m\) at \(p\). Then

\[
\pi^*C=\widetilde C+mE,\quad E^2=-1,\quad
K_Y=\pi^*K_X+E,\quad\pi^*C\cdot E=0,
\]

and hence

\[
\widetilde C^{\,2}=C^2-m^2,\qquad
p_a(\widetilde C)=p_a(C)-\binom m2.
\]

Total transform preserves both \(C^2\) and \(p_a(C)\). Strict transform does not. Enriques's \(\bar C+o\) on pp. 32–33 is the multiplicity-one illustration; the general expression requires (mE). His discussion is not a claim that self-intersection is an invariant of a bare curve under arbitrary birational maps. It is about a divisor together with the decision whether particular proper or infinitely near points are assigned base points.

More precisely, for an assigned cluster with multiplicities \(m_i\), let \(E_i^*\) denote the total transforms of the exceptional divisors. The corresponding class is

\[
D'=\pi^*D-\sum_i m_iE_i^*.
\]

Because \(E_i^*\cdot E_j^*=-\delta_{ij}\), one obtains

\[
(D')^2=D^2-\sum_i m_i^2,\qquad
p_a(D')=p_a(D)-\sum_i\binom{m_i}{2}.
\]

These equations also explain the unusual but deliberate permission on p. 33 to assign a multiplicity smaller than the curve's actual multiplicity. If the actual multiplicity is \(a>m\), the virtual transform includes \((a-m)E\); it need not equal the reduced strict transform. The appropriate modern setting is the divisor class on the specified blowup, or the language of virtual multiplicities and clusters (Casas-Alvero, 2000, chaps. 3–4).

Two qualifications are essential. First, \(\binom m2\) is the **arithmetic genus drop of one blowup**. The normalization-genus defect of an arbitrary multiplicity-\(m\) singularity may be larger, because additional singularities remain infinitely near. For \(y^2=x^5\), the first drop is one and the total delta invariant is two. Second, \(m^2\) is the contribution removed by the first blowup from the intersection of two multiplicity-\(m\) curves. Their entire local intersection number equals \(m^2\) only if their tangent cones have no common direction. For instance \(y=0\) and \(y=x^2\) have multiplicities one but local intersection two; one unit remains infinitely near. Enriques's infinitesimal conventions can accommodate both facts, but the last two sentences of p. 33 are not safe as unrestricted formulas about normalization genus or total local intersection.

### I.11. Exceptional curves and contraction (pp. 33–37)

#### Definitions and examples

An irreducible exceptional curve of the first kind is, in the modern smooth-surface formulation, a smooth rational curve \(E\simeq\mathbf P^1\) with \(E^2=-1\). Equivalently, it is the entire exceptional fiber of the blowup of a smooth point, or a curve contractible by a birational morphism to a smooth point with no other exceptional component in that local fiber. The qualification “entire” matters: a \((-2)\)-component of a larger exceptional fiber need not itself be contractible to a smooth point. Enriques explains this distinction explicitly in §12. His words about the neighborhood of a smooth point are stronger than simply “a curve mapped to some point” (pp. 33–35).

His second kind refers to curves made exceptional through a birational transformation with assigned base points on the curve. For a smooth rational curve with self-intersection \(\nu\ge0\), blowing up \(\nu+1\) smooth points on it gives a \((-1)\)-curve, which can then be contracted. The distinction depends on the model, not solely on the birational class of the surface. A safely formulated version of the converse requires keeping track of the assigned singularity cluster and of the entire exceptional fiber. Resolving an arbitrary rational map can produce several exceptional components, so “resolve the base points” alone is not a proof that every named component is a \((-1)\)-curve.

All the elementary examples on p. 34 fit this interpretation. On a smooth cubic surface the 27 lines are \((-1)\)-curves. Its familiar presentation as the blowup of six general plane points gives their classes: the six \(E_i\), fifteen \(H-E_i-E_j\), and six \(2H-\sum_{j\ne i}E_j\). Each has square \(-1\), arithmetic genus zero, and anticanonical degree one; the anticanonical embedding therefore makes it a line. This uses the classical cubic-surface representation assumed in Enriques's example. In the plane, a degree-\(d\) curve has square \(d^2>0\), so there is no first-kind curve. A line is contracted by the standard quadratic map after assigning two of its base points on the line; its strict transform has square \(1-1-1=-1\). A smooth conic is contracted by a homaloidal cubic net of type \((3;2,1,1,1,1)\), whose five base points lie on it: the net meets the conic in \(6=2+1+1+1+1\) assigned intersections, and the conic's strict transform has square \(4-5=-1\). The double point here is a double base point of the *net*, not a double point of the conic. Generic placement is required for this to be the stated homaloidal net.

The intersection count \(C\cdot\omega=\sum i_j\) in the transformation discussion on p. 34 likewise presupposes multiplicity-one branches of \(\omega\) at the assigned centers. For a singular curve the resolved formula is \(\sum i_j\operatorname{mult}_{p_j}\omega_j\), including the infinitely near centers and strict transforms. Adding a positive auxiliary system should be understood as constructing a projective model of the resolved graph: a sufficiently ample auxiliary realizes the required morphisms. Multiplying sections alone on the original surface does not erase their original base ideal.

The formulas \(\varrho=0,\nu=-1\) for the first kind are correctly obtained by Enriques from \(C=E+C_1\), \(E\cdot C_1=1\), and the sum formulas. In modern terms, \(N_{E/X}\simeq\mathcal O_{\mathbf P^1}(-1)\), so \(E^2=-1\); adjunction gives \(p_a(E)=0\). Conversely, an integral curve of arithmetic genus zero is smooth rational: its normalization sequence gives \(p_a(E)=g(\widetilde E)+\sum\delta_p\), with nonnegative summands. Thus Enriques's assertion that a first-kind curve cannot have a double point is correct. It does not depend on an unproved general smoothing principle.

For the second kind, \(\varrho=0\) on p. 35 must be read with the assigned-point convention of §10 when the original curve is singular. It is **not** a true assertion that every birationally contractible integral plane curve has arithmetic genus zero. A nodal plane cubic has \(p_a=1\); blow up its node to get a smooth rational curve of square \(9-4=5\), then blow up six smooth points on its strict transform to obtain a \((-1)\)-curve and contract it. The resulting rational map contracts the original cubic to a smooth point. Its adjusted genus is \(1-\binom22=0\), exactly as the assigned-cluster convention predicts. The stated numerical examples \(\nu=0,1,4\) for a ruling fiber, a line, and a conic are their self-intersections on the indicated models.

#### The converse: what is and is not proved on p. 36

Enriques anticipates Castelnuovo's criterion. Starting with a sufficiently general system \(|C|\), he adds \(E\) until \(C+iE\), where \(i=C\cdot E\), has zero intersection with \(E\). The calculations

\[
(C+E)^2=n+2i-1,\qquad
p_a(C+E)=\pi+i-1,
\]

are correct, and \(n-2\pi\) increases by one. The crucial assertion is that the addition actually produces new sections and eventually a base-point-free contracting system. Enriques explicitly says that its effectiveness will be justified later. Thus these pages offer a sketch with an acknowledged dependency, not a completed proof of contraction.

A modern completion makes the positivity requirement explicit. Choose a very ample \(H\), sufficiently positive that \(H^1(X,\mathcal O_X(H))=0\), and put \(i=H\cdot E>0\). For \(1\le j\le i\), use

\[
0\to\mathcal O_X(H+(j-1)E)\to\mathcal O_X(H+jE)
\to\mathcal O_{\mathbf P^1}(i-j)\to0.
\]

Inductively, \(H^1(H+jE)=0\), the restriction map is onto, and

\[
h^0(H+jE)-h^0(H+(j-1)E)=i-j+1.
\]

The old sections generate away from \(E\); the lifted sections of \(\mathcal O_{\mathbf P^1}(i-j)\) generate on \(E\). Hence \(|H+iE|\) is generated everywhere and restricts trivially to \(E\). Its map contracts \(E\) and is birational and quasi-finite off \(E\). Take its Stein factorization \(b:X\to Y\). The remaining issue is that (b(E)) is smooth, which does not follow just from \(E\cdot(H+iE)=0\).

For that last step, successive infinitesimal neighborhoods of \(E\) have quotients \(\mathcal O_E(-mE)\simeq\mathcal O_{\mathbf P^1}(m)\). Their first cohomology vanishes. The associated graded ring at the contracted point is generated by the two sections of \(\mathcal O_{\mathbf P^1}(1)\), with degree-\(m\) piece of dimension \(m+1\); the formal-functions argument identifies the completed local ring with \(\mathbf C[[u,v]]\). Thus the point is regular and \(b\) is its blowup. This supplies precisely the step missing from a purely numerical contraction argument. Full scheme-theoretic versions of the construction and smoothness argument are Stacks Project, Tags 0C2M and 0C2L. The name Castelnuovo's criterion is standard; this report does not attribute the first complete historical proof to the modern online exposition.

#### Numerical inequality, ruled surfaces, and termination

For a smooth general member \(D\) of a moving system, adjunction rewrites Enriques's inequality as

\[
N>2\Pi-2\quad\Longleftrightarrow\quad K_X\cdot D<0.
\]

After resolving its base points, \(D\) is nef. An effective pluricanonical divisor would have nonnegative intersection with it. Hence all \(P_m=h^0(X,mK_X)\) vanish. Over \(\mathbf C\), the classification identifies these surfaces as birationally ruled, including rational surfaces. Conversely, sufficiently positive sections on a ruled model have square larger than (2g-2). Enriques announces that classification implication for later chapters; it is not proved within pp. 1–40. The modern classification is summarized in Beauville (1996, chaps. III, V, and the classification chapters). The stated bound \(n\le2\pi-2\) on a nonruled surface is consequently correct with the same resolved-system convention.

There is also a clean proof of the claim about second-kind curves in its smooth rational formulation. If \(E\simeq\mathbf P^1\) and \(E^2=\nu\ge0\), then \(E\) is nef and \(K_X\cdot E=-\nu-2<0\). Again no pluricanonical divisor can be effective. Alternatively, Enriques's repeated addition is made effective by starting with a sufficiently positive \(H\) as above; restriction degrees now never decrease. Direct calculation gives

\[
(H+jE)^2-2p_a(H+jE)+2
=H^2-2p_a(H)+2+j(\nu+2),
\]

which eventually becomes positive. This justifies his iterative argument on pp. 36–37, without treating arithmetic growth alone as a guarantee of sections.

For finitely many first-kind curves \(E_j\), one must preserve the original numerical hypothesis when choosing the positive starting divisor. On the smooth model under discussion, the moving divisor \(C\) is nef. Put \(G=\sum_jE_j-K_X\). The source's hypothesis is exactly \(C\cdot G>0\), by adjunction. Choose an ample divisor \(A\) and then \(m\gg0\) so that \((mC+A)\cdot G>0\). Since \(C\) is nef, \(mC+A\) is ample. A sufficiently large multiple \(H=t(mC+A)\) is very ample, has \(H^1(X,\mathcal O_X(H))=0\), and still satisfies \(H\cdot G>0\). Thus replacement by \(H\) retains the needed inequality; an arbitrary positive replacement would not justify that step.

Now set \(i_j=H\cdot E_j\). If the curves are disjoint, simultaneous contraction gives

\[
D=H+\sum_j i_jE_j,\quad
D^2=H^2+\sum_j i_j^2,\quad
p_a(D)=p_a(H)+\sum_j\binom{i_j}{2}.
\]

Thus the displayed hypothesis \(\sum i_j>2\pi-2-n\) implies the desired inequality. Intersecting \((-1)\)-curves cannot be simultaneously interpreted as disjoint blowup fibers. Nevertheless the *existence inequality* need not be discarded: starting with sufficiently positive \(H\), add each \(E_j\) exactly \(i_j\) times. At each stage the restriction degree is at least \(i_j-m\ge0\), augmented by nonnegative intersections with previously added curves, so the same cohomology argument gives a generated system with irreducible general member. Cross terms change its square and genus, but cancel in

\[
-K_X\cdot D=-K_X\cdot H+\sum_j i_j.
\]

Finally, a succession of actual \((-1)\)-contractions terminates because each lowers the Picard number by one. This yields a minimal smooth model without any numerical circularity. On a nonruled surface the second-kind phenomenon above is absent, so this is the interpretation of Enriques's model “without exceptional curves.” It may still contain rational \((-2)\)-curves. Such curves can contract to singular points and are not exceptions to the smooth-point assertion.

### I.12. Reducible exceptional curves, proximity, and multiplicity (pp. 37–39)

The correct modern objects are **total exceptional divisors**, distinguished from the strict transforms of their components. Blow up a sequence of proper or infinitely near points \(p_0=O,p_1=O_1,\ldots,p_s=O_s\). Denote the final strict transforms by \(E_0,\ldots,E_s\), and by \(E_i^*\) the total transform of the exceptional divisor created at step \(i\). At creation each is a \((-1)\)-curve. The total-transform classes always satisfy

\[
E_i^*\cdot E_j^*=-\delta_{ij},\qquad
p_a(E_i^*)=0.
\]

For distinct proper points these cycles are disjoint reduced curves. Specializing centers to infinitely near points makes their supports connected and can make the cycles nonreduced. This supplies a rigorous replacement for the “principle of continuity”: use pullbacks in a sequence of blowups, or a flat family of blowups when a specialization is explicitly desired. Numerical invariance follows immediately from pullback, rather than from an unspecified degeneration.

For a free chain along a smooth branch, the source's formulas become

\[
\Omega_i=E_i^*=E_i+E_{i+1}+\cdots+E_s,\qquad 0\le i\le s.
\]

The graph is a chain with \(s+1\) vertices and \(s\) edges. One has \(E_j^2=-2\) for \(j<s\), \(E_s^2=-1\), adjacent intersections one, and all other intersections zero. Therefore

\[
\Omega_0^2=s(-2)-1+2s=-1,\qquad
p_a(\Omega_0)=\sum_{j=0}^s0+s-s=0.
\]

The scan on p. 38 instead prints (s-1) in both calculations and stops the sequence of blowups at \(F_s\), despite listing \(O,O_1,\ldots,O_s\). These are consistent indexing slips, not evidence against the claimed characters. Under the displayed indexing, the last surface must be \(F_{s+1}\) and the edge count must be \(s\). The same shift affects the sentence locating the creation of \(\omega_i\) on \(F_i\).

The degrees \(i-i_1,i_1-i_2,\ldots,i_s\) on p. 37 are **projective orders with respect to the transforming system**, not self-intersections. On the blown-up surface that system has class \(L=\pi^*A-\sum m_iE_i^*\). For a free chain,

\[
L\cdot E_j=m_j-m_{j+1},\quad j<s,\qquad
L\cdot E_s=m_s.
\]

These are degrees of the restricted line bundles. As in §6, if the induced map on \(E_j\) has degree \(d_j\) onto its image, the precise equality is \(L\cdot E_j=d_j\deg\varphi(E_j)\). The printed projective orders therefore require degree one on each component; sufficiently strong separation of the relevant jets supplies that condition. Positivity of the differences alone does not. Subject to this mapping-degree qualification, the formulas give the stated telescoping degree sum. They also prevent a mistaken identification of these positive orders with the negative virtual degrees computed on p. 38.

The first satellite example is equally exact. Blow up \(p_0\), then \(p_1\in E_0\), then the intersection of the two resulting exceptional components. On the final surface,

\[
E_0^2=-3,\quad E_1^2=-2,\quad E_2^2=-1,\qquad
E_0E_1=0, E_0E_2=E_1E_2=1,
\]

and

\[
\Omega_0=E_0+E_1+2E_2,\quad
\Omega_1=E_1+E_2,\quad\Omega_2=E_2.
\]

The factor two occurs because the last center has multiplicity two on the previous total exceptional divisor. Directly,

\[
\Omega_0^2=-3-2-4+4+4=-1,\qquad
K_Y\Omega_0=1+0-2=-1,\qquad p_a(\Omega_0)=0.
\]

The source correctly prints \(\omega+\omega_1+2\omega_2\) on p. 38 but incorrectly says on p. 39 that the transformed \(\omega_1\) must be counted twice. The latter must be \(\omega_2\). This is a scan-confirmed source slip.

In general, write \(p_j\succ p_i\) when \(p_j\) lies on the current strict transform of the exceptional divisor created at \(p_i\). Then

\[
E_i=E_i^*-\sum_{p_j\succ p_i}E_j^*.
\]

If \(t_i\) later centers are proximate to \(p_i\), this gives \(E_i^2=-1-t_i\). For the degree of the restricted line bundle, and hence for projective order under the same degree-one qualification, it gives the proximity expression

\[
L\cdot E_i=m_i-\sum_{p_j\succ p_i}m_j.
\]

The final intersection graph must be updated at every blowup: blowing up a smooth point of one component appends an edge; blowing up an intersection removes that edge and inserts the new component between its two endpoints. This is the precise version of Enriques's statement that \(\omega_i\) may meet \(\omega_{i+t}\) rather than its chronological successor. Merely knowing that two centers were consecutive does not determine the final adjacency.

The coefficients in \(\Omega_0=\sum h_iE_i\) have a simple recursion. The initial coefficient is one; a free blowup inherits the coefficient of the component through its center, while a satellite blowup receives the sum of the two coefficients through its center. To interpret Enriques's minimum-order rule, choose a curvette transverse to \(E_i\) away from the other exceptional components. Its image is a branch through the specified chain, with multiplicity \(h_i\) at \(O\). Any branch passing through that chain has at least this multiplicity; this follows by intersecting its strict transform with the total transform of a general line through \(O\). Thus the coefficient equals the minimum possible order of such a branch. Apply the same construction starting at \(p_i\) to obtain every \(\Omega_i\).

Enriques attributes the general analysis to Barber and Zariski. The verified citation is **Barber, S. F., and Zariski, O. (1935), “Reducible exceptional curves of the first kind,” American Journal of Mathematics, 57(1), 119–141, DOI 10.2307/2372025**. The printed “E. Barber” and “Ann. Journ. of Math.” are bibliographic errors. The paper's identity and bibliographic data were verified; its full proof was not accessible in this audit, so the recurrence above is supplied directly rather than represented as a quotation or page-specific paraphrase of that paper. Casas-Alvero (2000, chaps. 3–4) is a verified modern reference for the infinitely near and virtual-multiplicity framework.

There is a further mixed transcription/source issue in the footnotes. After “Enriques” the enlarged scan reads **(2)**, although the LaTeX conjectures **(3)**. Note (2) explains how to regard an infinitely near point as proper; note (3) is the Enriques–Chisini reference. The transcription therefore silently repairs a printed cross-reference slip. A faithful edition should print the source's (2), flag it, and identify (3) as the intended reference. The superscript in \(\omega_i^{h_i}\) really is \(h_i\). The odd “con-le” in the final paragraph is present in the scan.

**Own extension, high confidence.** The final sum on p. 39 has a natural interpretation not yet given there:

\[
\Omega_0+\cdots+\Omega_s=K_Y-\pi^*K_X.
\]

It is the relative canonical divisor of the composite blowup. This follows by applying the one-point canonical formula at each step. In the satellite example it is \(E_0+2E_1+4E_2\). Its square is \(-(s+1)\) and its arithmetic genus is \(-s\), as expected for a flat limit of \(s+1\) disjoint rational curves. Connected nonreduced support therefore does not force arithmetic genus to be nonnegative. This is a useful preparatory example for the canonical systems of the next chapter; it is an explanatory extension, not a claim of a new result.

### I.13. The virtual characteristic series (p. 40)

For a smooth effective curve \(C\subset X\), its intrinsic virtual characteristic series is

\[
|N_{C/X}|=|\mathcal O_C(C)|,\qquad \deg N_{C/X}=C^2.
\]

The characteristic series obtained by deforming \(C\) *within its complete linear system* is the projectivized image of

\[
H^0(X,\mathcal O_X(C))/\mathbf C\longrightarrow H^0(C,N_{C/X}).
\]

The two need not be equal on an irregular surface. The defining sequence is

\[
0\to\mathcal O_X\to\mathcal O_X(C)\to N_{C/X}\to0.
\]

Its boundary \(\delta:H^0(N_{C/X})\to H^1(\mathcal O_X)\) measures the missing directions. Thus the defect in vector-space dimension is \(\dim\operatorname{im}\delta\le q\), with equality if \(H^1(X,\mathcal O_X(C))=0\). This makes the relation to the front matter's irregularity discussion precise.

Enriques constructs the virtual series using an auxiliary \(|K|\), restricting \(|C+K|\) to \(C\), imposing the divisor \(C\cap K_0\) for a fixed \(K_0\in|K|\), and removing it. The words “passes through the intersections” must include this removal: the unreduced degree would be \(C^2+C\cdot K\). After removal, the underlying line bundle is intrinsically \(N_{C/X}\). His final sentence about choosing \(K\) sufficiently large is justified by

\[
0\to\mathcal O_X(K)\to\mathcal O_X(C+K)
\to\mathcal O_C(C+K)\to0.
\]

For \(K=mH\), \(m\gg0\), Serre vanishing gives \(H^1(X,\mathcal O_X(K))=0\), so restriction is surjective and the residual series is the entire \(|N_{C/X}|\). This is a correct modern completion of the existence claim (Stacks Project, Tag 0B5U).

There is, however, a real qualification to the preceding independence assertion. Arbitrary auxiliary systems satisfying only the two stated irreducibility conditions can produce different **subseries**. If \(k\in H^0(X,\mathcal O_X(K))\) defines \(K_0\), a diagram of the two exact sequences shows that the vector space of residual sections obtained from this \(K_0\) is

\[
V_K=\{s\in H^0(N_{C/X}):
 k_*\delta(s)=0\text{ in }H^1(X,\mathcal O_X(K))\}.
\]

It equals all of \(H^0(N_{C/X})\) when \(H^1(K)=0\), but this need not happen for a small auxiliary pencil. Consequently the line bundle, its complete series, or the eventual sufficiently positive construction is independent; a literal assertion about every actually cut subseries is too strong. Comparing three sum systems does not by itself prove that all their restriction maps are surjective.

**Own worked example, high confidence.** Let \(E\) be an elliptic curve, \(f:E\to\mathbf P^1\) a map of degree two, \(A=f^*\mathcal O_{\mathbf P^1}(1)\), and \(X=E\times\mathbf P^1\). Let \(C\) be the graph of \(f\), and let \(|K|\) be the pencil \(E\times\{t\}\). Then

\[
\mathcal O_X(C)=p_1^*A\otimes p_2^*\mathcal O(1),\quad
C^2=4,\quad N_{C/X}=A^2,
\]

\[
h^0(X,\mathcal O_X(C))=2\cdot2=4,\qquad
h^0(C,N_{C/X})=4.
\]

The ordinary characteristic image has vector dimension three after quotienting by the section defining \(C\). Multiplication \(H^1(\mathcal O_X)\to H^1(\mathcal O_X(K))\) by \(k\) is injective, by the product cohomology formula. Therefore this auxiliary pencil still yields vector dimension three, whereas a sufficiently ample auxiliary system yields four. Both \(|K|\) and \(|C+K|\) have irreducible general members; the latter system is base-point-free with a two-dimensional image, so its general member is smooth and irreducible by Bertini. For an explicit double cover \(E:y^2=q_4(x)\), the three pullback sections \(1,x,x^2\) lie in \(H^0(A^2)\), while \(y\) supplies its fourth direction. This verifies the defect without any historical attribution.

The hypothesis \(n=C^2>0\) on p. 40 is not needed to define the normal bundle. Nor does positive degree alone ensure a nonempty complete linear series on a curve of high genus. The modern definition allows an empty projectivized space, degree zero, and negative degree. For Cartier divisors that are singular or nonreduced, \(\mathcal O_C(C)\) and its normal sheaf still make sense; interpreting a linear series via moving effective point divisors requires the usual additional care about sections which vanish on a component.

Finally, first-order embedded deformations of a Cartier divisor have tangent space \(H^0(N_{C/X})\). A family \(C_t\) differentiates to such a section, and the characteristic divisor is its zero divisor when defined. This proves the local meaning of the final paragraph's “infinitely near curves.” It does **not** assert that every tangent vector integrates to an actual smooth family, or that every family has complete characteristic series. Obstructions and semiregularity are separate questions; the precise modern treatment is the normal-sheaf and Picard-scheme framework discussed in Kleiman (2005, Remark 5.18), together with the sources cited there. Thus p. 40 introduces the object needed for the later completeness problem, rather than solving that problem.

The historical notes distinguish three attributions. Enriques cites his 1896 *Introduzione*, §§15–16, for virtual characters; Severi's 1904 paper for the virtual characteristic series; and a Castelnuovo communication dated 25 December 1898, no. 4, for the implicit earlier appearance. The verified full Severi reference is *Osservazioni sui sistemi continui di curve appartenenti ad una superficie algebrica*, *Atti della Reale Accademia delle Scienze di Torino*, 39, 376–392. The specific letter and its text were not independently located in this audit, so that claim remains explicitly Enriques's attribution. His genus-two symmetric-product example concerns the surface of unordered pairs of points of a genus-two curve; it is birational to its Jacobian by the degree-two Abel map, with the canonical pencil contracted. The old adjective “iperellittica” here must not be identified with the modern bielliptic-surface class.

### Further questions and proposals arising from §§9–13

These are the present commentator's suggestions, not statements ascribed to Enriques.

1. **A reproducible proximity calculation (high confidence).** Encode the proximity relations in a triangular matrix, compute total transforms by substitution, and verify their Gram matrix is \(-I\). This tests all free and satellite examples and isolates indexing errors before invoking any degeneration. The formulas above give the proof and the satellite case gives a complete check.
2. **A criterion for auxiliary completeness (high confidence).** The equation \(V_K=\ker(k_*\delta)\) completely isolates the hypothesis missing from an unrestricted reading of p. 40. It suggests a useful exercise: classify, for a specified pair \(X,C\), the effective auxiliaries whose multiplication map annihilates \(\operatorname{im}\delta\). This is a concrete problem about cohomology maps, not an asserted unsolved research problem.
3. **A philological question (unsettled).** Did Enriques intend the word “series” in the auxiliary-independence sentence to mean its completed linear-equivalence class, or did he intend an unstated sufficiently-large condition? The supplied page does not decide this. The intrinsic normal-bundle statement is correct under either repair; the example above prevents conflating it with literal equality of all cut subseries.
4. **An adjacent limit of the audit (high confidence).** Rational \((-2)\)-curves on minimal nonruled surfaces, and the nonreduced cycles in §12, show why contraction to a singular point requires a different criterion from Castelnuovo's. A treatment of rational singularities or general negative-definite exceptional divisors would go beyond these pages; it should not be attributed to the criterion proved here.

### Cohomological companion to Chapter I: proofs behind the virtual characters

This subsection fixes the modern foundations used throughout the chapter commentary. It is especially relevant to §§7–8, 10–13. In these pages Enriques has not yet proved surface Riemann–Roch. Using it to check his formulas is legitimate provided that this dependence is identified explicitly.

#### Divisors, sections, and completeness

For a divisor \(D\) on smooth projective \(X\), set

\[
L(D)=H^0(X,\mathcal O_X(D))
=\{0\}\cup\{f\in\mathbf C(X)^*: \operatorname{div}(f)+D\ge0\}.
\]

The map \(f\mapsto\operatorname{div}(f)+D\) identifies the effective divisors linearly equivalent to \(D\) with \(\mathbf P L(D)\). Indeed, equal divisors imply a quotient with no zeros or poles, hence a global invertible regular function on the projective integral surface, hence a nonzero constant. Conversely, linear equivalence is precisely the existence of such a rational function. Finite-dimensionality is the properness/coherence theorem. It is a complete justification of the unique maximal linear system, including isolated divisors and empty systems; it does not require a dimension estimate based on irreducible curves.

If base conditions are prescribed by an ideal \(\mathcal I_Z\), the relevant vector space is \(H^0(X,\mathcal O_X(D)\otimes\mathcal I_Z)\). For infinitely near conditions it is cleaner to use a sequence of blowups \(\pi:Y\to X\), the total exceptional classes \(E_i^*\), and the divisor \(\pi^*D-\sum_i m_iE_i^*\). This explains why the phrases “complete” and “without base points” cannot be interchanged.

#### Adjunction and surface Riemann–Roch

For a smooth curve \(C\subset X\), the conormal sequence

\[
0\to\mathcal O_C(-C)\to\Omega_X^1|_C\to\Omega_C^1\to0
\]

gives, after taking determinants,

\[
\omega_C\simeq(\omega_X\otimes\mathcal O_X(C))|_C,\qquad
2g(C)-2=C\cdot(C+K_X).
\]

Here is a direct reduction of the surface Riemann–Roch formula to the curve theorem. Write \(D=A-B\) with \(A\) and \(B\) smooth very ample divisors; this is possible after choosing \(B\) sufficiently positive and applying Bertini. The two exact sequences obtained by restricting \(\mathcal O_X(A)\) to \(A\) and to \(B\) give

\[
\chi(\mathcal O_X(D))-\chi(\mathcal O_X)
=\chi(\mathcal O_A(A))-\chi(\mathcal O_B(A)).
\]

Curve Riemann–Roch and adjunction give the right-hand side as

\[
\frac{A^2-A\cdot K_X}{2}
-\left(A\cdot B-\frac{B^2+B\cdot K_X}{2}\right)
=\frac{D\cdot(D-K_X)}2.
\]

Consequently

\[
\boxed{\chi(\mathcal O_X(D))=\chi(\mathcal O_X)+\tfrac12D\cdot(D-K_X).}
\]

Serre duality \(h^2(\mathcal O_X(D))=h^0(\mathcal O_X(K_X-D))\) rewrites this as

\[
h^0(D)-h^1(D)+h^0(K_X-D)
=1+p_a(X)+\tfrac12D\cdot(D-K_X).
\]

This identity is not the assertion that \(h^1(D)=0\). Treating an expected dimension as an actual dimension without a vanishing theorem is exactly the kind of step the audit checks. The standard textbook locations are Hartshorne (1977), Chapter V, §§1 and 3, with surface Riemann–Roch at Theorem V.1.6; the underlying curve formula, divisor sequences, and projective cohomology can also be checked in the separately identified Stacks Project references in the bibliography. The algebra displayed here is supplied in full so that the check does not depend on an inaccessible book passage.

For any effective Cartier divisor \(D\), possibly reducible or nonreduced, the sequence \(0\to\mathcal O_X(-D)\to\mathcal O_X\to\mathcal O_D\to0\) now yields

\[
\boxed{p_a(D):=1-\chi(\mathcal O_D)=1+\tfrac12D\cdot(D+K_X).}
\]

This is Enriques's virtual genus on an unmarked smooth model. In particular,

\[
\begin{aligned}
(A+B)^2&=A^2+2A\cdot B+B^2,\\
p_a(A+B)&=p_a(A)+p_a(B)+A\cdot B-1,\\
p_a(sD)&=1+\tfrac12(s^2D^2+sD\cdot K_X),\\
p_a(A-B)&=p_a(A)+p_a(B)-1-A\cdot B-B\cdot K_X.
\end{aligned}
\]

The last formula follows by expansion and avoids the tempting, incorrect idea that arithmetic genus is additive under formal subtraction. For a reduced integral curve, normalization gives \(p_a(C)=g(\widetilde C)+\sum_P\delta_P\). For a disconnected divisor, arithmetic genus may be negative. For the zero divisor the displayed virtual-genus polynomial gives 1, consistently with \(1-\chi(\mathcal O_{\varnothing})=1\). Thus a virtual genus is a numerical function, not an assertion that a smooth curve of that genus exists.

#### Blowups and the precise invariance convention

Let \(\pi:Y\to X\) blow up a smooth point \(P\), with exceptional curve \(E\). The local construction gives \(E\simeq\mathbf P^1\) and \(\mathcal O_E(E)\simeq\mathcal O_{\mathbf P^1}(-1)\). Hence

\[
E^2=-1,\quad \pi^*D\cdot E=0,\quad K_Y=\pi^*K_X+E.
\]

If \(m=\operatorname{mult}_P D\), the strict transform is \(D'=\pi^*D-mE\), so

\[
(D')^2=D^2-m^2,\qquad
p_a(D')=p_a(D)-\frac{m(m-1)}2.
\]

These are exact one-blowup identities, even when the original singularity is not ordinary. They do **not** say that a multiplicity-\(m\) singularity always has total delta invariant \(m(m-1)/2\); infinitely near singularities can contribute more. For a reduced integral curve, repeating the identities until its strict transform is smooth accounts for those further contributions. Likewise, two multiplicity-\(m\) curves with no common local component have local intersection at least \(m^2\), with equality when their projectivized tangent cones have no common point; common infinitely near intersections add to that number.

Total pullback preserves both \(D^2\) and the virtual genus. Strict transform generally preserves neither. Thus when Enriques discusses “invariance” of virtual characters, one must retain the assigned base conditions as part of the object. A birational transformation alone does not make the square of an arbitrarily chosen strict transform invariant. In the total exceptional basis of a sequence of blowups, \(E_i^*\cdot E_j^*=-\delta_{ij}\), which makes every base-point correction explicit.

#### Surface genera and plurigenera: context, rather than an imported later chapter

For a smooth projective surface, \(p_g=h^0(K_X)\), \(q=h^1(\mathcal O_X)\), and \(P_m=h^0(mK_X)\) are birational invariants. One can check this for a blowup and then use factorization of birational maps between smooth surfaces. Indeed \(\pi_*\mathcal O_Y=\mathcal O_X\) and \(R^1\pi_*\mathcal O_Y=0\), while any pluricanonical form on \(Y\) is a pluricanonical form away from the exceptional point and extends across that codimension-two point on smooth \(X\). Pullback gives the reverse inclusion. Therefore \(p_a(X)=p_g-q\) is invariant too. By contrast \(K_Y^2=K_X^2-1\); an expression involving \(K^2\), such as \(p_a(K_X)=K_X^2+1\), requires its chosen-model or minimal-model convention.

These facts clarify the preface and pp. 29–30, 36–37. They do not pretend that the supplied extract proves the classification of complex surfaces, Castelnuovo's rationality criterion, or the positive-characteristic classification. A full proof of those later theories would be a different task. Where the present pages explicitly appeal to a later classification criterion, the particular criterion and its role are stated in §I.11 above, with a modern proof route and a verified reference. No unsupported attribution to Kodaira or Bombieri–Mumford is used merely because those names appeared in the task's examples.

#### Exactly where the completeness theorem enters

For an effective Cartier divisor \(C\), put \(N=\mathcal O_C(C)\) and consider the two connecting maps

\[
H^0(N)\xrightarrow{\delta}H^1(\mathcal O_X),\qquad
H^1(N)\xrightarrow{\sigma}H^2(\mathcal O_X).
\]

The first measures the difference between deformations within one linear system and deformations which change the line bundle. The second is the semiregularity map: \(C\) is **semiregular** when \(\sigma\) is injective. These are different assertions.

Set

\[
R=q+h^0(\mathcal O_X(C))-1-h^1(\mathcal O_X(C)).
\]

The long exact sequence itself gives

\[
h^0(N)=R+\dim\ker\sigma.
\]

To check this without an expected-dimension shortcut, write \(a\) for the rank of \(H^1(\mathcal O_X)\to H^1(\mathcal O_X(C))\). Exactness gives \(h^0(N)=h^0(C)-1+q-a\) and \(\dim\ker\sigma=h^1(C)-a\), which is the asserted identity.

The additional deformation theorem says, over \(\mathbf C\), that semiregularity implies smoothness of the divisor scheme at \([C]\). Obstruction classes lie in \(H^1(N)\) and have zero image under \(\sigma\); injectivity therefore kills them. The assertion about their image is a genuine theorem, not a consequence of the preceding dimension count: Mumford (1966, pp. 157–159) gives the obstruction calculation, and Kleiman (1973, theorem on p. 307; 2005, Remark 5.18) gives the algebraic formulation. Together with the tangent-space identification \(T_{[C]}\operatorname{Div}(X)=H^0(N)\), this yields the precise equivalence

\[
C\text{ semiregular}
\quad\Longleftrightarrow\quad
\operatorname{Div}(X)\text{ smooth of dimension }R\text{ at }[C].
\]

The dimension qualification cannot be omitted. In the sufficiently positive case actually used in the front-matter proof, \(H^1(\mathcal O_X(C))=0\); here the Abel map to the smooth Picard scheme is smooth, and the required family is already explicitly constructed as a projective bundle. Thus that argument does not assume the full semiregularity theorem in order to manufacture the family it needs. Grothendieck (1961, Exposé 221, Corollary 5.4 and §§5.5–5.6) directly treats the normal-sheaf tangent space and the two relevant vanishing cases. Page 40 of Enriques introduces the characteristic object; none of these later deformation-theoretic conclusions is claimed to be proved on that page.

## References and verification notes

The entries use author–date citations and APA-style bibliographic details. Each verification note distinguishes an inspected mathematical text from a verified bibliographic identity. In-text theorem numbers refer to the specified edition or preprint. No unseen proof is treated as inspected.

Barber, S. F., & Zariski, O. (1935). Reducible exceptional curves of the first kind. *American Journal of Mathematics, 57*(1), 119–141. https://doi.org/10.2307/2372025. Bibliographic identity checked against the journal issue; the whole paper was not re-proved or fully read here.

Bauer, I., & Catanese, F. (2021). \(\mathfrak S_5\)-equivariant syzygies for the Del Pezzo surface of degree 5. *Rendiconti del Circolo Matematico di Palermo, Series 2, 70*, 97–120. https://doi.org/10.1007/s12215-020-00483-9. Published online in 2020; volume year 2021. Section 2 and the abstract verify the anticanonical model and its automorphism group.

Beauville, A. (1996). *Complex algebraic surfaces* (2nd ed.). Cambridge University Press. https://doi.org/10.1017/CBO9780511623936. **Verified:** publisher's book and chapter metadata; companion author's lecture text below inspected for formulas, blowups, and contraction statements.

Beauville, A. (2020, July). *Algebraic surfaces* [Lecture slides]. Université Côte d'Azur. https://math.univ-cotedazur.fr/~beauvill/conf/Shanghai.pdf. **Inspected:** Lecture I, slides 2–12, intersection and genus formulas; Lecture II, slides 18–27, blowups and minimal surfaces. This is an auxiliary accessible primary exposition, not a substitute for exact source-page citations to Enriques.

Calabri, A., & Ciliberto, C. (2010). Birational classification of curves on rational surfaces. *Nagoya Mathematical Journal, 199*, 43–93. https://doi.org/10.1215/00277630-2010-003. **Verified:** journal metadata and its Barber–Zariski bibliography; full PDF retrieval was unsuccessful, so no page-specific proof is attributed to it.

Casas-Alvero, E. (2000). *Singularities of plane curves*. Cambridge University Press. https://doi.org/10.1017/CBO9780511569326. Chapter 3, “Infinitely near points,” pp. 67–118, https://doi.org/10.1017/CBO9780511569326.005; chapter 4, “Virtual multiplicities,” pp. 119–158, https://doi.org/10.1017/CBO9780511569326.006. **Verified:** publisher metadata and chapter summaries; no uninspected theorem number is claimed.

Ciliberto, C., & Flamini, F. (2011). On the branch curve of a general projection of a surface to a plane. *Transactions of the American Mathematical Society, 363*(7), 3457–3471. https://doi.org/10.1090/S0002-9947-2011-05401-2 . The full author preprint https://arxiv.org/abs/0811.0467 (v2, 2010) was checked, especially §2, Definitions 2.1 and 2.3, Remark 2.2, and Theorems 2.4–2.6. Its newly proved plane-branch theorem is beyond the present extract; it must not be confused with the \(\mathbf P^3\) double-curve theorem quoted there.

Du Val, P. (1936). Reducible exceptional curves. *American Journal of Mathematics, 58*(2), 285–289. https://doi.org/10.2307/2371038. Bibliographic identity checked against the journal issue.

Enriques, F. (1893). Una questione sulla linearità dei sistemi di curve appartenenti ad una superficie algebrica. *Rendiconti della Reale Accademia dei Lincei, Series 5, 2*, 3–8. Official collected-works scan: https://www.federigoenriques.org/wp-content/uploads/opere/pdf/GM_Enriques_1893_3.pdf. The statement, counterexample, and proof on original pp. 4–7 were checked directly.

Enriques, F. (1896). Introduzione alla geometria sopra le superficie algebriche. *Memorie della Società Italiana delle Scienze detta dei XL*, Series 3, *10*, 1–81. https://www.federigoenriques.org/indice-cronologico-delle-opere/. **Verified:** national-edition bibliographic record; the supplied book cites §§15–16, but the article's large scan was not retrieved in full here.

Enriques, F. (1949). *Le superficie algebriche*. Nicola Zanichelli. **Primary source:** the supplied scans of the title and preliminary leaves, Castelnuovo's preface (V–VIII), Enriques's preface (IX–X), contents (XI–XV), Introduzione (pp. 1–13), and Capitolo I (pp. 15–40); all 55 PDF pages were visually inspected. Printed p. 14 is blank.

Franchetta, A. (1941). Sulla curva doppia della proiezione di una superficie generale dell'\(S_4\), da un punto generico su un \(S_3\). *Atti della Reale Accademia d'Italia. Rendiconti della Classe di Scienze Fisiche, Matematiche e Naturali*, ser. 7, *2*, 282–288. The year 1941 agrees with Enriques and Lopez–Ran; some later bibliographies give 1940. The original journal issue was not independently inspected, so the year discrepancy remains bibliographic, not silently “corrected.”

Franchetta, A. (1947). Sulla curva doppia della proiezione di una superficie generale dell'\(S_4\), da un punto generico su un \(S_3\). *Rendiconti dell'Accademia Nazionale dei Lincei*, ser. 8, *2*, 276–279. Title and pages corroborated by the checked modern references; the original article was not independently read.

Fulton, W. (1998). *Intersection theory* (2nd ed.). Springer. https://doi.org/10.1007/978-1-4612-1700-8. Chapter 14, §14.4, Thom–Porteous formula; publisher chapter preview: https://doi.org/10.1007/978-1-4612-1700-8_15.

Grothendieck, A. (1961). Techniques de construction et théorèmes d'existence en géométrie algébrique IV : Les schémas de Hilbert. *Séminaire Bourbaki, 6*, Exposé 221, 249–276. [Original text](https://www.numdam.org/item/SB_1960-1961__6__249_0.pdf). Corollary 5.4 and §§5.5–5.6 were inspected directly for tangent spaces, the characteristic homomorphism, and the vanishing cases. This is the relevant Exposé for the completeness discussion; it must not be confused with Exposé 236 merely because the latter begins on printed p. 221.

Grothendieck, A. (1962a). Technique de descente et théorèmes d'existence en géométrie algébrique. V. Les schémas de Picard : Théorèmes d'existence. *Séminaire Bourbaki, 7*, Exposé 232, 143–161. [Bibliographic record and original text](https://numdam.org/book-part/SB_1961-1962__7__143_0/). Used for the construction framework; the detailed modern presentation actually checked is Kleiman (2005).

Grothendieck, A. (1962b). Technique de descente et théorèmes d'existence en géométrie algébrique. VI. Les schémas de Picard : Propriétés générales. *Séminaire Bourbaki, 7*, Exposé 236, 221–243. [Original text](https://numdam.org/item/SB_1961-1962__7__221_0.pdf). Proposition 2.10(iii), concerning tangent dimension and characteristic-zero smoothness, was checked directly. A published erratum exists; none of the more general relative-family claims subject to additional qualifications is needed here.

Hartshorne, R. (1977). *Algebraic geometry* (Graduate Texts in Mathematics, Vol. 52). Springer. [Publisher record](https://doi.org/10.1007/978-1-4757-3849-0). Chapter III supplies coherent cohomology and duality; Chapter V, §§1, 3, and 5 supplies intersection theory, blowups, and birational geometry of surfaces, including surface Riemann–Roch at Theorem V.1.6. Publisher and chapter metadata were verified. The full book was not available for a fresh page-by-page inspection; the actual formulas and elementary proofs used here are written out in the commentary and cross-checked against the accessible references.

Kleiman, S. L. (1973). Completeness of the characteristic system. *Advances in Mathematics, 11*(3), 304–310. The theorem's location on p. 307 is verified through Kleiman (2005, Remark 5.18); the corrected page range 304–310 is corroborated by the author's 2014 bibliography, reference 37. The 2005 preprint bibliography starts the range at 305. The original 1973 article was not directly inspected in full, and no DOI is guessed.

Kleiman, S. L. (1998). Bertini and his two fundamental theorems. *Rendiconti del Circolo Matematico di Palermo, Series 2, Supplement 55*, 9–37. https://arxiv.org/abs/alg-geom/9704018. The 1997 preprint was checked at §§4–5, especially Theorems 4.1 and 5.3 and the discussion of van der Waerden. The publication year and pages are verified by the Stacks Project bibliography: https://stacks.math.columbia.edu/bibliography/Kleiman-Bertini.

Kleiman, S. L. (2005). The Picard scheme. In B. Fantechi, L. Göttsche, L. Illusie, S. L. Kleiman, N. Nitsure, & A. Vistoli, *Fundamental algebraic geometry: Grothendieck's FGA explained* (Mathematical Surveys and Monographs, Vol. 123, pp. 235–321). American Mathematical Society. [Author preprint](https://arxiv.org/abs/math/0504020). Checked: the historical introduction; Theorems 5.4 and 5.11; Corollaries 5.13–5.14; and Remark 5.18. The theorem/remark labels refer to that checked preprint. Its stray phrase equating a zero semiregularity map with injectivity is not used: the definition and the exact sequence require **injectivity**.

Kleiman, S. L. (2014). *The Picard scheme* [Author preprint]. arXiv. [Text](https://arxiv.org/abs/1402.0409). This is a separate historical exposition from the 2005 chapter, despite the identical title. Used narrowly to verify the 1973 bibliography and distinguish the two publications.

Lipman, J. (1978). Desingularization of two-dimensional schemes. *Annals of Mathematics, 107*, 151–207. https://doi.org/10.2307/1971141 . The theorem on p. 151 and the introductory account of its dependencies were checked in the author's PDF at https://www.math.purdue.edu/~jlipman/papers-older/%5B1978%5D%20Desingularization%20of%20two-dimensional%20schemes.pdf .

Lopez, A., & Ran, Z. (2003). On the irreducibility of secant cones, and an application to linear normality. *Duke Mathematical Journal, 117*, 389–401. https://doi.org/10.1215/S0012-7094-03-11731-7 . The proof cited here was checked in the author preprint https://arxiv.org/abs/math/0111147 (2001), pp. 2 and 7; no assertion that every theorem number is unchanged between versions is needed.

Mezzetti, E., & Portelli, D. (1997). A tour through some classical theorems on algebraic surfaces. *Analele Ştiinţifice ale Universităţii Ovidius Constanţa, Seria Matematică, 5*(2), 51–78. Bibliographic identity verified; theorem pointers 3, 5, and 8 are reported by Ciliberto–Flamini, not independently read here.

Moishezon, B. (1977). *Complex surfaces and connected sums of complex projective planes* (Lecture Notes in Mathematics, Vol. 603). Springer. https://doi.org/10.1007/BFb0063355 . The publisher verifies the chapter “Generic projections of algebraic surfaces into \(\mathbf{CP}^3\),” pp. 72–115; the specific p. 115 attribution to Mumford is supplied by the checked Lopez–Ran text. The chapter itself was not independently read in full.

Mumford, D. (1966). *Lectures on curves on an algebraic surface* (with a section by G. M. Bergman; Annals of Mathematics Studies, No. 59). Princeton University Press. [Bibliographic record](https://stacks.math.columbia.edu/bibliography/Mum). The tangent-space and obstruction pointers, pp. 154 and 157–159, are independently identified in the inspected Kleiman (2005, Remark 5.18); the full book was not independently read here.

Noether, M. (1875). Zur Theorie des eindeutigen Entsprechens algebraischer Gebilde. *Mathematische Annalen, 8*, 495–533. Publisher issue record: https://link.springer.com/journal/208/volumes-and-issues/8-4. This verifies the date correction; no claim is made that the entire original article was read.

Severi, F. (1904). Osservazioni sui sistemi continui di curve appartenenti ad una superficie algebrica. *Atti della Reale Accademia delle Scienze di Torino, 39*, 376–392. **Verified bibliographically** in Tannenbaum (1984), reference 9; the original paper's text was not inspected.

Tannenbaum, A. (1984). On the classical characteristic linear series of plane curves with nodes and cuspidal points: Two examples of Beniamino Segre. *Compositio Mathematica, 51*(2), 169–183. https://www.numdam.org/item/CM_1984__51_2_169_0/. **Use here:** verification of Severi's bibliography only, not attribution of the elliptic-product example above.

The Stacks Project Authors. (2026). *The Stacks Project*. Retrieved November 7, 2026, from [the project](https://stacks.math.columbia.edu/). Relevant directly checked stable tags are [0B5B](https://stacks.math.columbia.edu/tag/0B5B), curve Riemann–Roch, especially Lemma 53.5.2; [0B5U](https://stacks.math.columbia.edu/tag/0B5U), Lemma 30.17.1, ample twists and cohomology; [01XS](https://stacks.math.columbia.edu/tag/01XS), cohomology of projective space; [0C2L](https://stacks.math.columbia.edu/tag/0C2L) and [0C2M](https://stacks.math.columbia.edu/tag/0C2M), contraction to a smooth point. Additional directly checked locators are listed immediately below. Stable tags are provided because online chapter and lemma numbering can change.

Additional Stacks locators: resolution of surfaces, overview [0ADX](https://stacks.math.columbia.edu/tag/0ADX) and Theorem 54.14.5, [0BGP](https://stacks.math.columbia.edu/tag/0BGP); projective space, Lemma 27.13.1 in [01ND](https://stacks.math.columbia.edu/tag/01ND); linear series on curves, [0CCM](https://stacks.math.columbia.edu/tag/0CCM); Bertini theorems, [0FD4](https://stacks.math.columbia.edu/tag/0FD4) and [0G4C](https://stacks.math.columbia.edu/tag/0G4C); finite duality, Remark 48.20.12 in [0AU5](https://stacks.math.columbia.edu/tag/0AU5); and the exceptional-curve contraction context [0C2I](https://stacks.math.columbia.edu/tag/0C2I). Statements and the relevant displayed proofs or proof dependencies were inspected; the tag identifies the reference if online numbering changes.

Vakil, R. (2002). *Complex algebraic surfaces: Class 6* [Course notes]. Stanford University. https://math.stanford.edu/~vakil/02-245/sclass6A.pdf. **Verified:** §2, surface Riemann–Roch and the genus formula.

van der Waerden, B. L. (1937). Zur algebraischen Geometrie. X. Über lineare Scharen von reduziblen Mannigfaltigkeiten. *Mathematische Annalen, 113*, 705–712. Reprinted in *Zur algebraischen Geometrie: Selected papers* (1983), pp. 225–232, https://doi.org/10.1007/978-3-642-61782-9_17. Bibliography and the reprint's statement were checked; the specific historical repair is documented in Kleiman's analysis, not claimed from an independent reading of every page of the 1937 paper.

Walker, R. J. (1935). Reduction of the singularities of an algebraic surface. *Annals of Mathematics, 36*(2), 336–365. https://doi.org/10.2307/1968575 . Cited by Enriques on p. 6; bibliographic identity checked, full proof not independently audited.

Zariski, O. (1939). The reduction of the singularities of an algebraic surface. *Annals of Mathematics, 40*(3), 639–689. https://doi.org/10.2307/1968949 . Cited by Enriques on p. 6; bibliographic identity checked, full proof not independently audited.

Zariski, O. (1941). Pencils on an algebraic variety and a new proof of a theorem of Bertini. *Transactions of the American Mathematical Society, 50*(1), 48–70. https://doi.org/10.1090/S0002-9947-1941-0004241-4. Bibliographic identity verified against AMS/JSTOR records; direct AMS PDF retrieval was unavailable.

Zariski, O. (1944). The theorem of Bertini on the variable singular points of a linear system of varieties. *Transactions of the American Mathematical Society, 56*, 130–140. Bibliography and the intrinsic argument are verified through Kleiman, §4 and reference 46. Direct original full-text access was not obtained, so no unverified internal theorem number is supplied.

### Further historical citations retained from the source

The source's other historical pointers are retained as printed: Enriques–Chisini, Books I, III, IV, V; B. Levi, “Risoluzione delle singolarità puntuali delle superficie algebriche,” *Atti Acc. Torino* (1897), with *Annali di Matematica* (1897); O. Chisini, “La risoluzione delle singolarità delle superficie mediante trasformazioni birazionali dello spazio,” *Memorie Acc. Bologna* (1921); G. Albanese, “Trasformazione birazionale di una superficie algebrica qualunque in un'altra priva di punti multipli,” *Circolo Matematico di Palermo* (1924); Enriques, “Sulle singolarità che nascono per proiezione di una superficie o varietà algebrica,” in the Berzolari volume (1936), p. 351. Page 8 names Noether (1888) without giving a title. Missing bibliographic fields have not been invented.
