# Superseded note: Generic Realized Uniqueness on All Bounded-Bandwidth Windows

> Warning.
> This note relied on the incorrect linear-determinantal realization of the normalized phase
> quotient. The exact realized-side map is quadratic, not linear, because the normalization uses
> the basepoint value `A(0)+iB(0)` of the same profile.
> The corrected framework is now in
> [RESEARCH_realized_quadratic_prufer_map.md](/Users/shunhu/Documents/Codes/Lean/notes/RESEARCH_realized_quadratic_prufer_map.md).
> In particular, the old claim of generic realized uniqueness on all bounded windows should not
> be used in its present form.

## Goal

The projective-determinantal note identifies the realized nonunique-fiber locus on a bounded
window `\mathcal W_{K,L}` as
\[
\Sigma_1(K,L)=\{[x]:\operatorname{rank}T_x\le N-2\},
\qquad N=\dim \mathcal W_{K,L}.
\]

The real question is whether this locus is actually proper on every window.

This note gives a uniform positive answer.

> on every bounded even/odd bandwidth window, the realized Prüfer fiber is generically unique.

Moreover, on the balanced windows the nonunique-fiber locus is automatically a projective
hypersurface of explicitly determined degree.

## 1. The distinguished basepoint

Fix a bounded window `\mathcal W_{K,L}` with basis
\[
J_0,\ \widetilde J_2,\dots,\widetilde J_{2K},\ \widetilde J_1,\dots,\widetilde J_{2L+1}.
\]

For a real parameter `\lambda\neq 0`, consider the distinguished element
\[
x_\lambda:=J_0+\lambda \widetilde J_1.
\]

Since `\widetilde J_1=J_1`, its `(J_0,J_1)`-pair is simply
\[
x_\lambda=(A_x,B_x)=(1,\lambda).
\]

Hence
\[
T_{x_\lambda}(y)=A_xB_y-B_xA_y=B_y-\lambda A_y.
\]

## 2. Maximal rank at the distinguished point

The central-factorial basis theorem gives:

- for even modes `\widetilde J_{2k}`,
  \[
  \deg \widetilde B_{2k}=2k-1,\qquad \deg \widetilde A_{2k}=2k-2;
  \]
- for odd modes `\widetilde J_{2\ell+1}` with `\ell\ge 1`,
  \[
  \deg \widetilde B_{2\ell+1}=2\ell,\qquad \deg \widetilde A_{2\ell+1}=2\ell-1;
  \]
- for `J_0` and `\widetilde J_1`, the images under `T_{x_\lambda}` are constants.

So the leading exponents of the images are completely separated.

### Theorem 2.1

For every bounded bandwidth window `(K,L)` and every `\lambda\neq 0`, the linear map
\[
T_{x_\lambda}:\mathcal W_{K,L}\to\mathbb R[u]
\]
has maximal possible rank
\[
\operatorname{rank}T_{x_\lambda}=N-1.
\]

Equivalently,
\[
\dim\ker T_{x_\lambda}=1.
\]

### Proof

First,
\[
T_{x_\lambda}(J_0)=-\lambda,
\qquad
T_{x_\lambda}(\widetilde J_1)=1,
\]
so the span of the two degree-`0` images is one-dimensional, as expected.

Next, for `1\le k\le K`,
\[
T_{x_\lambda}(\widetilde J_{2k})
=
\widetilde B_{2k}-\lambda \widetilde A_{2k}.
\]
Because
\[
\deg \widetilde B_{2k}=2k-1>\deg \widetilde A_{2k},
\]
this polynomial has leading degree exactly `2k-1` with nonzero leading coefficient.

Similarly, for `1\le \ell\le L`,
\[
T_{x_\lambda}(\widetilde J_{2\ell+1})
=
\widetilde B_{2\ell+1}-\lambda \widetilde A_{2\ell+1},
\]
and since
\[
\deg \widetilde B_{2\ell+1}=2\ell>\deg \widetilde A_{2\ell+1},
\]
its leading degree is exactly `2\ell`.

Therefore the images of the basis vectors have distinct leading exponents
\[
0,\ 1,\ 3,\dots,2K-1,\ 2,\ 4,\dots,2L,
\]
with exactly one-dimensional constant part. Hence they are linearly independent modulo the single
obvious dependence coming from `x_\lambda` itself, so the image has dimension
\[
1+K+L=N-1.
\]

## 3. Generic realized uniqueness

The determinantal interpretation now immediately gives the generic statement.

### Corollary 3.1

For every bounded bandwidth window `(K,L)`, the realized nonunique-fiber locus
\[
\Sigma_1(K,L)
\subset \mathbb P(\mathcal W_{K,L})
\]
is a proper projective determinantal subset.

In particular, generic realized points have unique normalized phase quotient fiber.

### Proof

Theorem 2.1 gives a point `x_\lambda` with
\[
\operatorname{rank}T_{x_\lambda}=N-1.
\]
Hence the rank-drop condition
\[
\operatorname{rank}T_x\le N-2
\]
is not automatic, so `\Sigma_1(K,L)` is proper.

## 4. Balanced windows

The previous theorem becomes sharper on the balanced windows.

### Definition 4.1

Call `(K,L)` balanced if
\[
L=K
\qquad\text{or}\qquad
L=K-1.
\]

### Proposition 4.2

On a balanced window `(K,L)`, the determinant matrix `T_x` has size
\[
(N-1)\times N.
\]

### Proof

The exponent set appearing in `T_x(y)` is
\[
\{0,1,\dots,\max(2K,2L+1)-1\}.
\]
Hence the number of coefficient rows is
\[
\max(2K,2L+1).
\]
If `L=K-1`, this equals `2K=K+L+1=N-1`. If `L=K`, it equals `2L+1=2K+1=K+L+1=N-1`.

### Proposition 4.3

On every balanced window `(K,L)`, the realized nonunique-fiber locus `\Sigma_1(K,L)` is cut out
by the maximal minors of an `(N-1)\times N` matrix whose entries are linear in the projective
coordinates of `x`. Consequently every irreducible component of `\Sigma_1(K,L)` has degree at
most `N-1=K+L+1`.

### Proof

By Proposition 4.2, `T_x` is an `(N-1)\times N` matrix. Its maximal minors are homogeneous
polynomials of degree `N-1`, and `\Sigma_1(K,L)` is exactly the common zero locus of those
minors.

### Observation 4.4

The small balanced windows suggest a sharper hypersurface law:

- `(1,0)` gives a degree-`1` hyperplane;
- `(1,1)` gives a degree-`2` quadric;
- `(2,1)` gives a degree-`3` cubic.

So it is natural to conjecture that on balanced windows `\Sigma_1(K,L)` is often, perhaps
always, a single projective hypersurface of degree `K+L+1`.

## 5. Relation to the small-window exact equations

The small exact classifications now fall into place:

- `(1,0)` is a degree-`1` balanced window;
- `(1,1)` is a degree-`2` balanced window;
- `(2,1)` is a degree-`3` balanced window.

So the hyperplane, quadric, and cubic equations found in the small-window note are not isolated
coincidences. They are the first instances of a more systematic balanced-window hypersurface
phenomenon.

## 6. Research meaning

This is the first global theorem on the realized bounded-bandwidth frontier.

It says:

1. realized nonuniqueness is never generic on any bounded window;
2. on balanced windows, it is automatically hypersurface-type;
3. the projective-determinantal geometry is not merely formal, but already governs the global
   codimension-one picture.

So the next genuine frontier is no longer “is generic uniqueness true?” That question is now
settled on the realized side.

The next frontier is:

- determine whether the balanced windows always give a single hypersurface and, if so, identify
  its degree-`K+L+1` equation;
- understand the reducible, non-balanced windows;
- and relate these realized hypersurfaces to the reduced-pair incidence loci
  `\mathcal Y_s(K,L)`.
