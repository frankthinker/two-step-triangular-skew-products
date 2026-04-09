# Superseded note: Projective-Determinantal Geometry of Bounded-Bandwidth Prüfer Fibers

> Warning.
> This note is no longer the correct exact formulation of realized Prüfer fibers.
> It mistakenly compared raw pairs `(A,B)` instead of the self-normalized phase pairs.
> The correct realized-side object is the quadratic self-normalized map recorded in
> [RESEARCH_realized_quadratic_prufer_map.md](/Users/shunhu/Documents/Codes/Lean/notes/RESEARCH_realized_quadratic_prufer_map.md).
> The only part that remains conceptually useful here is the idea that bounded-bandwidth fibers
> should admit a canonical projective geometry; the exact linear determinantal formulas below
> should not be used as final statements.

## Goal

The multiplier-incidence language is exact, but it is still not the cleanest object on the
*realized* side. For a fixed bounded-bandwidth window, the fiber of the normalized phase map can
be described directly by a linear determinant operator.

This gives a sharper formulation:

> the realized fiber geometry is a projective determinantal geometry.

That is the right linear-algebraic object behind amplitude lifting.

## 1. The linear window

Fix a bounded bandwidth window `\mathcal V_{K,L}` and let
\[
\mathcal W_{K,L}
\subset
\mathbb R[u]^2
\]
be the corresponding finite-dimensional linear space of polynomial pairs `(A,B)` arising in the
exact `(J_0,J_1)`-decomposition
\[
F(t)=A(u)J_0(t)+B(u)J_1(t).
\]

The normalized phase quotient of a nonzero pair `(A,B)` with
\[
z_0:=A(0)+iB(0)\neq 0
\]
depends only on the projective class of
\[
Z:=A+iB\in \mathcal W_{K,L}\otimes_\mathbb R\mathbb C,
\]
since replacing `Z` by a nonzero scalar multiple does not change
\[
\frac{Z(u)}{Z(0)}.
\]

So the realized bounded-bandwidth inverse problem is a projective problem on `\mathbb P(\mathcal
W_{K,L})`.

## 2. The determinant operator

For `x=(A_x,B_x)\in\mathcal W_{K,L}`, define the linear map
\[
T_x:\mathcal W_{K,L}\to\mathbb R[u]
\]
by
\[
T_x(y):=\det(x,y):=A_xB_y-B_xA_y.
\]

This is linear in `y`.

### Proposition 2.1

For two nonzero realized pairs `x,y\in\mathcal W_{K,L}`, the following are equivalent:

1. `x` and `y` have the same normalized phase quotient;
2. `\det(x,y)=0`;
3. `y\in\ker T_x`.

### Proof

The normalized phase quotients agree exactly when
\[
\frac{B_x}{A_x}=\frac{B_y}{A_y}
\]
as rational functions, equivalently
\[
A_xB_y-B_xA_y=0.
\]
This is precisely `T_x(y)=0`.

## 3. Exact fiber formula

The determinant operator completely describes the realized projective fiber.

### Theorem 3.1

Let `[x]\in \mathbb P(\mathcal W_{K,L})` be a realized projective point. Then its realized fiber
under the normalized phase map is exactly
\[
\mathbb P(\ker T_x).
\]

In particular:

- the fiber is unique iff `\dim\ker T_x=1`;
- the fiber is nonunique iff `\dim\ker T_x\ge 2`;
- equivalently, if `N:=\dim\mathcal W_{K,L}`, then the fiber is nonunique iff
  \[
  \operatorname{rank}T_x\le N-2.
  \]

### Proof

By Proposition 2.1, a projective point `[y]` lies in the same realized fiber as `[x]` iff
`y\in\ker T_x`. Projectivizing the nonzero part of the kernel gives the fiber.

Since `x\in\ker T_x` always, one always has `\dim\ker T_x\ge 1`. Uniqueness means the kernel is
exactly the line spanned by `x`, while nonuniqueness means it is larger. The rank statement is
the rank-nullity formula.

## 4. Determinantal strata

This suggests the canonical realized stratification.

### Definition 4.1

Let `N=\dim\mathcal W_{K,L}`. For `r\ge 1`, define
\[
\Sigma_r(K,L)
:=
\left\{
[x]\in\mathbb P(\mathcal W_{K,L}):
\dim\ker T_x\ge r+1
\right\}
\]
equivalently
\[
\Sigma_r(K,L)
=
\left\{
[x]:\operatorname{rank}T_x\le N-r-1
\right\}.
\]

Thus:

- `\Sigma_1(K,L)` is the nonunique realized fiber locus;
- `\Sigma_2(K,L)` is the locus where the realized fiber has projective dimension at least `2`;
- and so on.

### Corollary 4.2

Each `\Sigma_r(K,L)` is a projective determinantal variety cut out by the maximal minors of the
matrix of `T_x`.

### Proof

In any fixed basis of `\mathcal W_{K,L}`, the coefficients of `T_x` depend linearly on the
coordinates of `x`. The rank condition
\[
\operatorname{rank}T_x\le N-r-1
\]
is therefore cut out by the vanishing of the corresponding minors.

## 5. Relation to multiplier-incidence geometry

The determinantal picture is exact on the realized side. The multiplier-incidence picture is
exact on the reduced-pair side.

### Proposition 5.1

The realized nonunique-fiber locus `\Sigma_1(K,L)` is exactly the image in
`\mathbb P(\mathcal W_{K,L})` of the multiplier-incidence union
\[
\mathcal Y_{\ge 1}(K,L)
\]
under the realized-lift map.

### Proof

A reduced phase pair `\widehat Z` with at least two realized multipliers gives at least two
projectively distinct realized lifts in `\mathbb P(\mathcal W_{K,L})`, hence lands in
`\Sigma_1(K,L)`. Conversely, any nonunique realized fiber determines a reduced representative and
therefore a reduced phase pair with at least two realized multipliers.

So:

- `\mathcal Y_s(K,L)` is the exact reduced-pair ambiguity locus;
- `\Sigma_r(K,L)` is the exact realized projective-fiber locus.

These are two sides of the same inverse problem.

## 6. Small-window experiments

The determinantal model is also computationally usable. On the smallest windows, the rank-drop
locus is cut out by a single explicit polynomial.

For example:

- on `\mathcal V_{1,0}`, the nonunique realized fiber locus is the projective hyperplane
  \[
  x_0+x_1=0;
  \]
- on `\mathcal V_{1,1}`, it is a projective quadric;
- on `\mathcal V_{2,1}`, it is a projective cubic hypersurface.

These are not yet final theorems in the paper, but they strongly suggest that bounded-bandwidth
fiber geometry may admit an explicit determinantal classification window by window.

## 7. Research meaning

This changes the frontier once again.

The bounded-bandwidth inverse problem is not only:

- a Pad\'e reconstruction problem for phase quotients,
- plus a multiplier-incidence problem for reduced pairs.

It is also:

- a projective determinantal problem on the realized window `\mathbb P(\mathcal W_{K,L})`.

This has two conceptual advantages.

1. It replaces “is there another lift?” by a direct rank-drop condition.
2. It converts the realized fiber geometry into a standard determinantal stratification problem.

So the next natural theorem is:

> determine whether `\Sigma_1(K,L)` is empty, proper, or explicitly classifiable on natural
> bounded-bandwidth windows.

This is the cleanest exact formulation so far of the realized bounded-bandwidth frontier.
