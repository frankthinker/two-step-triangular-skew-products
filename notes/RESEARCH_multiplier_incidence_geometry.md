# Multiplier-Incidence Geometry for Bounded-Bandwidth Amplitude Lifts

## Goal

The gcd/subresultant language is useful, but it is not the exact object controlling
nonuniqueness of bounded-bandwidth amplitude lifts.

What it really controls is the locus of *realized lifts* which are already nonminimal. A phase
quotient may admit more than one lift even when one chosen realized lift is reduced.

This note records the correct exact framework.

> bounded-bandwidth nonuniqueness is governed by multiplier-incidence geometry for reduced phase
> pairs, not merely by the gcd of one realized lift.

## 1. Bounded-bandwidth phase pairs

Fix a bandwidth window `\mathcal V_{K,L}`. For
\[
F\in\mathcal V_{K,L},
\]
write
\[
F(t)=A_F(u)J_0(t)+B_F(u)J_1(t),
\qquad
z_{0,F}:=A_F(0)+iB_F(0)\neq 0,
\]
and define the normalized phase pair
\[
C_F(u)+iS_F(u):=\frac{A_F(u)+iB_F(u)}{z_{0,F}}.
\]
Then
\[
C_F(0)=1,\qquad S_F(0)=0.
\]

The associated normalized phase quotient is
\[
R_F(u)=\frac{S_F(u)}{C_F(u)}.
\]

## 2. Reduced phase pairs and lift multipliers

For a rational quotient `R(u)`, let
\[
(\widehat C,\widehat S)
\]
denote its unique reduced coprime representative normalized by
\[
\widehat C(0)=1,\qquad \widehat S(0)=0.
\]

Every realized lift of `R` inside `\mathcal V_{K,L}` is then of the form
\[
(C,S)=h(\widehat C,\widehat S),
\]
where `h(u)` is a real polynomial satisfying
\[
h(0)=1,
\]
and such that the product pair lies in the bounded-bandwidth model.

This motivates the exact object.

### Definition 2.1

For a reduced normalized phase pair `\widehat Z=(\widehat C,\widehat S)`, define its multiplier
set in the window `\mathcal V_{K,L}` by
\[
\mathcal M_{K,L}(\widehat Z)
:=
\left\{
h\in\mathbb R[u]:
h(0)=1,\quad
h\widehat Z \text{ is realized by some }F\in\mathcal V_{K,L}
\right\}.
\]

Then:

- `\widehat Z` is realized iff `\mathcal M_{K,L}(\widehat Z)\neq\varnothing`;
- its lift fiber is unique iff `|\mathcal M_{K,L}(\widehat Z)|=1`;
- its lift fiber is nonunique iff `|\mathcal M_{K,L}(\widehat Z)|\ge 2`.

So the bounded-bandwidth inverse problem is exactly the classification of these multiplier sets.

## 3. Why gcd of one realized lift is not enough

The previous gcd language detects only those lifts which are already nonminimal.

### Proposition 3.1

Let `R` be a normalized phase quotient with reduced pair `\widehat Z`, and suppose
\[
h_1\widehat Z,\qquad h_2\widehat Z
\]
are two realized lifts in `\mathcal V_{K,L}`.

Then a given realized lift `h_1\widehat Z` has a nonconstant gcd if and only if `h_1` itself is
nonconstant. But the existence of another realized lift `h_2\widehat Z` does **not** imply that
`h_1` is nonconstant.

### Proof

The first statement is immediate from coprimeness of `\widehat Z`.

For the second, one may have `h_1=1` and `h_2\neq 1`. Then the reduced lift `\widehat Z`
coexists with a second nontrivial lift, even though the chosen realized pair `\widehat Z`
itself has gcd `1`.

So nonuniqueness of the phase quotient is a property of the multiplier set
`\mathcal M_{K,L}(\widehat Z)`, not of the gcd of one chosen lift.

## 4. Incidence strata

The correct global geometry is therefore an incidence geometry.

### Definition 4.1

For each integer `s\ge 1`, define the degree-`s` multiplier incidence stratum
\[
\mathcal I_s(K,L)
:=
\left\{
(\widehat Z,h):
\deg h=s,\ h(0)=1,\ h\in \mathcal M_{K,L}(\widehat Z)
\right\}.
\]

Projecting to the reduced phase-pair coordinate gives the degree-`s` ambiguity locus
\[
\mathcal Y_s(K,L)
:=
\left\{
\widehat Z:\exists h,\ \deg h=s,\ h\in\mathcal M_{K,L}(\widehat Z)
\right\}.
\]

Then the full nonunique-lift locus is the union
\[
\mathcal Y_{\ge 1}(K,L):=\bigcup_{s\ge 1}\mathcal Y_s(K,L).
\]

This is the exact replacement for the older heuristic frontier.

## 5. Algebraicity of the incidence problem

The multiplier-incidence problem is finite-dimensional from the outset.

Indeed, for fixed `(K,L)` and `s`, every reduced pair `\widehat Z=(\widehat C,\widehat S)` that
could contribute to `\mathcal Y_s(K,L)` has bounded degrees
\[
\deg \widehat C\le d_A-s,
\qquad
\deg \widehat S\le d_B-s,
\]
because multiplication by a degree-`s` polynomial must still fit into the window bounds
`\deg C\le d_A`, `\deg S\le d_B`.

So one may regard `\widehat Z` and `h` as points of a finite-dimensional affine space with
coordinates given by their polynomial coefficients.

### Theorem 5.1

Fix `(K,L)` and `s\ge 1`. Then:

1. the degree-`s` incidence set `\mathcal I_s(K,L)` is a real-algebraic subset of a
   finite-dimensional affine coefficient space;
2. the ambiguity locus `\mathcal Y_s(K,L)` is a semialgebraic, indeed constructible, subset of
   the reduced-pair parameter space.

### Proof

Choose coefficient coordinates for all reduced pairs
\[
\widehat Z=(\widehat C,\widehat S)
\]
with the degree bounds above, together with coordinates for
\[
h(u)=1+h_1u+\cdots+h_su^s.
\]

The condition that `h\widehat Z` be realized in `\mathcal V_{K,L}` is a finite system of linear
conditions on the coefficients of the pair `h\widehat Z`, hence a finite polynomial system in
the coefficients of `\widehat Z` and `h`. The normalization conditions
`\widehat C(0)=1,\widehat S(0)=0` are polynomial, and coprimeness is the nonvanishing of the
appropriate resultant, hence a Zariski-open condition.

Therefore `\mathcal I_s(K,L)` is algebraic inside the ambient affine space after restricting to
the reduced locus. The projection to the reduced-pair coordinates is then constructible by
elimination, hence semialgebraic over `\mathbb R`.

### Corollary 5.2

For each bounded window `(K,L)`, the full nonunique-lift locus
\[
\mathcal Y_{\ge 1}(K,L)=\bigcup_{s\ge 1}\mathcal Y_s(K,L)
\]
is a finite union of constructible subsets.

### Proof

Only finitely many values of `s` can occur, namely
\[
1\le s\le \min(d_A,d_B),
\]
so the union is finite.

## 6. Relation to boundary-thinness

The codimension estimates from the boundary-thinness note still remain valid, but now in the
correct direction.

### Proposition 6.1

If
\[
\widehat Z\in\mathcal Y_s(K,L),
\]
then every realized lift
\[
(C,S)=h\widehat Z
\]
with `\deg h=s` lies in the codimension-`s` top-coefficient boundary stratum of
`S`.

### Proof

This is exactly the top-coefficient vanishing statement from
[RESEARCH_boundary_strata_amplitude_thinness.md](/Users/shunhu/Documents/Codes/Lean/notes/RESEARCH_boundary_strata_amplitude_thinness.md),
applied to the realized lift `h\widehat Z`.

So the boundary filtration is still present, but it should be understood as a visible shadow of
the deeper multiplier-incidence geometry.

## 7. Relation to gcd/subresultant strata

The gcd/subresultant strata from
[RESEARCH_boundary_strata_subresultant_geometry.md](/Users/shunhu/Documents/Codes/Lean/notes/RESEARCH_boundary_strata_subresultant_geometry.md)
can now be interpreted precisely.

### Proposition 7.1

For each `s\ge 1`, the realized-gcd stratum `\mathfrak X_s` is the image under the realized-lift
map of the multiplier incidence stratum `\mathcal I_{\ge s}`.

Equivalently, gcd/subresultant geometry describes the geometry of realized nonminimal lifts,
whereas multiplier-incidence geometry describes the geometry of phase quotients with nonunique
lifts.

### Proof

A realized lift lies in `\mathfrak X_s` exactly when it has the form `h\widehat Z` with
`\deg h\ge s`. This is precisely the image of the corresponding incidence set.

## 8. Research meaning

This changes the frontier in an essential way.

The correct bounded-bandwidth inverse problem is not:

> classify the gcd strata of realized pairs.

It is:

> classify the multiplier sets `\mathcal M_{K,L}(\widehat Z)` of reduced phase pairs.

In particular, the real next questions are:

1. is `\mathcal Y_1(K,L)` empty on some windows?
2. more generally, are the ambiguity loci `\mathcal Y_s(K,L)` proper, empty, or stratified by
   increasing codimension?
3. how do these incidence strata project to the visible subresultant strata of realized lifts?

This is the right moduli-theoretic formulation of the bounded-bandwidth amplitude-lifting
problem.
