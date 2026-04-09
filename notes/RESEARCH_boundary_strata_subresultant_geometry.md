# Subresultant Geometry of the Bounded-Bandwidth Amplitude-Lifting Problem

## Goal

The previous boundary-thinness note showed:

> a degree-`s` amplitude-lifting ambiguity forces the top `s` coefficients of the normalized
> `S`-channel to vanish.

That is a useful one-sided consequence, but it still treats the boundary fiber indirectly. The
more conceptual object is the common factor of the normalized phase pair itself.

This note records the correct reformulation:

> nonunique amplitude lifting is exactly the common-factor locus of the normalized phase pair,
> hence is controlled by resultants and subresultants.

So the bounded-bandwidth frontier is not merely a vague lower-degree boundary problem. It is a
real-algebraic gcd stratification problem.

## 1. Normalized phase pairs

Fix a bounded even/odd bandwidth window `\mathcal V_{K,L}`. For
\[
F\in\mathcal V_{K,L},
\]
write
\[
F(t)=A_F(u)J_0(t)+B_F(u)J_1(t),
\qquad
z_{0,F}:=A_F(0)+iB_F(0)\neq 0,
\]
and define
\[
C_F(u)+iS_F(u):=\frac{A_F(u)+iB_F(u)}{z_{0,F}}.
\]
Then
\[
C_F(0)=1,\qquad S_F(0)=0.
\]

The normalized phase quotient is
\[
R_F(u)=\frac{S_F(u)}{C_F(u)}.
\]

Let
\[
d_A:=\max(2K-2,\,2L-1),
\qquad
d_B:=\max(2K-1,\,2L).
\]
Then
\[
\deg C_F\le d_A,
\qquad
\deg S_F\le d_B.
\]

## 2. Common factor = amplitude ambiguity

The correct algebraic formulation is immediate.

### Proposition 2.1

Let `F,G\in\mathcal V_{K,L}`. The following are equivalent:

1. `F` and `G` have the same normalized phase quotient:
   \[
   R_F=R_G.
   \]
2. Their normalized phase pairs satisfy
   \[
   S_FC_G-S_GC_F=0.
   \]
3. There exists a real polynomial `h(u)` with `h(0)=1` such that
   \[
   C_G=h\,C_F,
   \qquad
   S_G=h\,S_F.
   \]

In particular, `F` admits a nontrivial second lift with the same normalized phase quotient if
and only if `C_F` and `S_F` have a nonconstant common real factor.

### Proof

The equivalence of (1) and (2) is immediate by cross-multiplication.

Assume (2). Let `(\widehat C,\widehat S)` be the unique reduced coprime pair representing the
common rational quotient and normalized by `\widehat C(0)=1`. Then there exist unique real
polynomials `h_F,h_G` with `h_F(0)=h_G(0)=1` such that
\[
C_F=h_F\widehat C,\qquad S_F=h_F\widehat S,
\]
\[
C_G=h_G\widehat C,\qquad S_G=h_G\widehat S.
\]
Thus
\[
C_G=\frac{h_G}{h_F}C_F,\qquad S_G=\frac{h_G}{h_F}S_F.
\]
Because all polynomials are real and normalized at `0`, the quotient is again a real polynomial
with value `1` at `0`, proving (3). The converse is obvious.

The last statement is exactly the case `G\neq F`, which occurs if and only if `h` is
nonconstant, i.e. if and only if `C_F` and `S_F` have a nonconstant common factor.

## 3. Resultant and subresultant stratification

The proposition shows that nonuniqueness is a gcd condition. Therefore it is controlled by
classical elimination theory.

### Definition 3.1

For `0\le s\le \min(d_A,d_B)`, let
\[
\mathfrak X_s
:=
\left\{
F\in\mathcal V_{K,L}:\deg\gcd(C_F,S_F)\ge s
\right\}.
\]

Thus:

- `\mathfrak X_0=\mathcal V_{K,L}`;
- `\mathfrak X_1` is the nonunique-lift locus;
- higher `\mathfrak X_s` correspond to higher-degree amplitude ambiguities.

### Theorem 3.2

Each `\mathfrak X_s` is a real-algebraic subset of `\mathcal V_{K,L}`.

More precisely:

1. `\mathfrak X_1` is cut out by the vanishing of the Sylvester resultant
   \[
   \operatorname{Res}(C_F,S_F);
   \]
2. more generally, `\mathfrak X_s` is cut out by the vanishing of the first `s` subresultants of
   `(C_F,S_F)`.

Hence the residual bounded-bandwidth fibers admit a canonical algebraic filtration
\[
\mathcal V_{K,L}\supset \mathfrak X_1\supset \mathfrak X_2\supset\cdots.
\]

### Proof

For polynomials of bounded degrees, the condition
\[
\deg\gcd(C_F,S_F)\ge 1
\]
is equivalent to vanishing of the Sylvester resultant. Likewise,
\[
\deg\gcd(C_F,S_F)\ge s
\]
is equivalent to vanishing of the first `s` subresultants. Since the coefficients of `C_F` and
`S_F` are polynomial functions of the finite-dimensional coordinates on `\mathcal V_{K,L}`, each
such condition defines a real-algebraic subset.

## 4. Relation to boundary thinness

The previous note showed that a degree-`s` ambiguity forces vanishing of the top `s`
coefficients of `S_F`. This now appears as a shadow of the stronger gcd geometry.

### Corollary 4.1

If `F\in\mathfrak X_s`, then `F` lies in the codimension-`s` top-coefficient boundary stratum
from
[RESEARCH_boundary_strata_amplitude_thinness.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_boundary_strata_amplitude_thinness.md).

So the top-coefficient filtration is a visible necessary condition for the deeper subresultant
filtration.

### Proof

If `F\in\mathfrak X_s`, then
\[
C_F=h\,\widehat C,\qquad S_F=h\,\widehat S
\]
for some real polynomial `h` of degree at least `s`. The boundary-thinness proposition then
forces the top `s` coefficients of `S_F` to vanish.

## 5. Generic thinness on bounded windows

The subresultant description gives the correct generic statement.

### Corollary 5.1

If the resultant
\[
\operatorname{Res}(C_F,S_F)
\]
is not identically zero on `\mathcal V_{K,L}`, then the nonunique-lift locus `\mathfrak X_1` is
a proper real-algebraic subset. In particular, it is meagre and has Lebesgue measure zero.

More generally, whenever the first `s` subresultants are not identically zero, `\mathfrak X_s`
is contained in a proper real-algebraic subset of codimension at least one.

### Proof

This is immediate from Theorem 3.2 together with the standard fact that a proper real-algebraic
subset has empty interior and Lebesgue measure zero.

## 6. Research meaning

This reformulation is the cleanest one so far.

The bounded-bandwidth frontier is no longer:

> maybe the lower-degree boundary strata are messy.

It is:

> understand the real-algebraic gcd strata `\mathfrak X_s` cut out by the subresultants of the
> normalized phase pair.

This has two advantages.

1. It replaces an infinite family of potential lift ambiguities by a canonical finite
   elimination package.
2. It separates two issues that were previously mixed together:
   - visible top-degree vanishing;
   - genuine common-factor geometry.

So the next serious theorem is now:

> show that the first resultant is not identically zero on a given bounded-bandwidth window, or
> more ambitiously classify the subresultant strata `\mathfrak X_s`.

That is the right out-of-the-box formulation of the lower-degree boundary problem.
