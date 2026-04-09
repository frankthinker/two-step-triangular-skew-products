# Global Beta-Uniform Obstruction-Free Subspace

## Goal

The one-frequency notes reveal large automatic-resonance kernels. The natural next question is
whether these kernels assemble into a clean global object inside the full finite-band cocycle
space.

They do. For the current two-step model, there is an explicit linear subspace of finite-band
cocycles on which the denominator obstruction vanishes identically in `beta`. Together with the
mean-zero `n=0` sector, this gives a large beta-uniform obstruction-free family.

This is more structural than any individual resonant family theorem.

## Finite-band decomposition

Fix bandwidths `M,N\ge 1`. Every real-valued finite-band trigonometric polynomial can be written
uniquely as
\[
h(x,y)=u_0(x)+\sum_{n=1}^N\Bigl(G_n(x)e(ny)+\overline{G_n(x)e(ny)}\Bigr),
\]
where

- `u_0(x)` is a real trigonometric polynomial of degree at most `M`,
- `G_n(x)=\sum_{|m|\le M} g_{m,n}e(mx)` with arbitrary complex coefficients `g_{m,n}`.

The `n=0` part is separated because its behavior is different: it does not involve the Bessel
mechanism.

## Exact obstruction decomposition

For the current model,
\[
\Gamma_n(h;z_0)=
\sum_{|m|\le M} g_{m,n}(-i)^m e(ma/2)J_m(nz_0)
\qquad (1\le n\le N),
\]
while
\[
\Gamma_{-n}(h;z_0)=\overline{\Gamma_n(h;z_0)},
\qquad
\Gamma_0(h;z_0)=\widehat u_0(0).
\]

Thus the obstruction vector splits completely by vertical frequency.

## The positive-frequency automatic kernel

For each fixed `n\ge 1`, define the reduced coefficients
\[
d_{m,n}:=g_{m,n}(-i)^m e(ma/2).
\]
Then
\[
\Gamma_n(h;z_0)=\sum_{|m|\le M} d_{m,n}J_m(nz_0).
\]
Using `J_{-m}=(-1)^mJ_m`, this vanishes identically in `z_0` if and only if
\[
d_{0,n}=0,\qquad d_{-m,n}=-(-1)^m d_{m,n}\quad (1\le m\le M).
\]

This gives a real `2M`-dimensional automatic kernel for each positive frequency `n`.

## The zero-frequency sector

Write
\[
u_0(x)=\sum_{|m|\le M} c_m e(mx),
\]
with `c_{-m}=\overline{c_m}`. Its denominator blocks are
\[
S_{q_j}u_0(x)=\sum_{|m|\le M} c_m e(mx)D_{q_j}(m\alpha).
\]
Under the Diophantine hypothesis on `alpha`,

- the `m=0` term contributes `q_j c_0`,
- the `m\neq 0` terms contribute `O(q_j^{-1})`.

Therefore the `n=0` component is obstruction-free exactly when it has zero mean:
\[
c_0=\widehat u_0(0)=0.
\]

The mean-zero `n=0` subspace has real dimension `2M`.

## Global obstruction-free subspace

### Theorem 1

Fix bandwidths `M,N\ge 1`. Let `\mathcal{H}_{M,N}` be the real vector space of finite-band
cocycles
\[
h(x,y)=u_0(x)+\sum_{n=1}^N\Bigl(G_n(x)e(ny)+\overline{G_n(x)e(ny)}\Bigr),
\]
with `\deg u_0,\deg G_n\le M`.

Define `\mathcal{K}_{M,N}\subset\mathcal{H}_{M,N}` by the conditions:

1. `u_0` has zero mean;
2. for each `1\le n\le N`,
   \[
   d_{0,n}=0,\qquad d_{-m,n}=-(-1)^m d_{m,n}
   \quad (1\le m\le M),
   \]
   where `d_{m,n}=g_{m,n}(-i)^m e(ma/2)`.

Then:

1. `\mathcal{K}_{M,N}` is a real linear subspace of dimension
   \[
   2M(N+1);
   \]
2. for every `h\in\mathcal{K}_{M,N}`,
   \[
   \Gamma_n(h;z_0)\equiv 0\qquad \text{for all } n\in\Z;
   \]
3. if `alpha` is Diophantine, then for every `h\in\mathcal{K}_{M,N}` the corresponding skew
   product
   \[
   T_h(x,y,z)=(x+\alpha,\ y+\beta\sin(2\pi x),\ z+h(x,y))
   \]
   is Möbius disjoint in the original Cesàro sense for every real `beta`.

### Proof

The subspace property is immediate. The dimension count is:

- `2M` real degrees from the mean-zero `u_0` sector;
- `2M` real degrees from each positive-frequency automatic kernel.

Hence
\[
\dim_\R \mathcal{K}_{M,N}=2M+N\cdot 2M=2M(N+1).
\]

For `h\in\mathcal{K}_{M,N}`, the positive-frequency obstruction coefficients vanish identically by
the one-frequency kernel classification, and `\Gamma_0=\widehat u_0(0)=0`. Thus the entire
obstruction vector vanishes identically.

If `alpha` is Diophantine, the quantitative denominator law from the main project yields
\[
\sup_{x,y}|S_{q_j}h(x,y)|\ll q_j^{-1}.
\]
Hence the corresponding system satisfies the polynomial-rigidity hypothesis needed for the KLR
criterion, and therefore original Cesàro Möbius disjointness for every real `beta`.

## Explicit basis

An explicit real basis of `\mathcal{K}_{M,N}` is given by:

1. the mean-zero `n=0` basis
   \[
   \cos(2\pi m x),\qquad \sin(2\pi m x),
   \qquad 1\le m\le M;
   \]
2. for each `1\le n\le N` and `1\le m\le M`,
   \[
   \sin\!\bigl(2\pi m(x-a/2)\bigr)\cos(2\pi n y),\qquad
   \sin\!\bigl(2\pi m(x-a/2)\bigr)\sin(2\pi n y).
   \]

## Research meaning

This is the global version of the one-frequency kernel phenomenon.

It says that the finite-band cocycle space contains a large explicit beta-uniform
obstruction-free subspace whose dimension grows linearly in both bandwidth parameters.

So the current mechanism is not merely producing isolated resonant examples. It contains a large
linear sector where the obstruction vanishes identically and Möbius disjointness follows for all
real `beta`.

## Relation to the other notes

This subspace is only one part of the picture.

- Inside `\mathcal{K}_{M,N}`, Möbius disjointness is beta-uniform.
- Outside `\mathcal{K}_{M,N}`, one-frequency oscillatory directions may still give infinitely many
  resonant `beta`.
- For several active frequencies, the compatibility-hierarchy notes suggest that infinite common
  resonance should be very thin.

The global geometric picture therefore starts to look like:

1. a large explicit linear kernel;
2. a thin oscillatory resonant locus outside the kernel;
3. finite resonance away from that locus.

That is the strongest current candidate for a genuinely nontrivial strengthening of the project.

## Exact finite-dimensional obstruction image

The previous theorem identifies a large kernel. One can go further and describe the entire
finite-band obstruction map exactly.

Define the target space
\[
\mathcal{T}_{M,N}
:=
\R
\oplus
\bigoplus_{n=1}^N
\operatorname{span}_{\R}
\{J_0(n\cdot),\dots,J_M(n\cdot),\, iJ_0(n\cdot),\dots,iJ_M(n\cdot)\}.
\]

Its real dimension is
\[
\dim_\R \mathcal{T}_{M,N}=1+N(2M+2).
\]

The finite-band obstruction map is
\[
\mathcal{O}_{M,N}:\mathcal{H}_{M,N}\to \mathcal{T}_{M,N},
\qquad
h\mapsto \bigl(\Gamma_0(h),\Gamma_1(h;\cdot),\dots,\Gamma_N(h;\cdot)\bigr).
\]

### Theorem 2

The map `\mathcal{O}_{M,N}` is surjective, and
\[
\ker \mathcal{O}_{M,N}=\mathcal{K}_{M,N}.
\]
Consequently,
\[
\mathcal{H}_{M,N}/\mathcal{K}_{M,N}\cong \mathcal{T}_{M,N},
\]
and
\[
\dim_\R \mathcal{K}_{M,N}=2M(N+1).
\]

### Proof

The kernel statement is exactly Theorem 1.

For surjectivity, it is enough to show that each summand in `\mathcal{T}_{M,N}` can be realized
independently.

1. The `\R` summand is obtained from the constant cocycle `h(x,y)\equiv c`.
2. Fix `1\le n\le N`. Given arbitrary real coefficients `a_0,\dots,a_M,b_0,\dots,b_M`, define
   complex numbers `d_{m,n}:=a_m+ib_m` for `0\le m\le M`, set
   \[
   d_{-m,n}:=0\qquad (1\le m\le M),
   \]
   and then
   \[
   g_{m,n}:=d_{m,n} i^m e(-ma/2).
   \]
   The corresponding one-frequency cocycle contributes
   \[
   \Gamma_n(h;\cdot)=\sum_{m=0}^M (a_m+ib_m)J_m(n\cdot),
   \]
   which realizes an arbitrary element of the `n`th summand.

Thus `\mathcal{O}_{M,N}` is onto.

### Direct-sum interpretation

To see that the decomposition by frequencies is genuinely direct, suppose
\[
c+\sum_{n=1}^N \sum_{m=0}^M \gamma_{m,n}J_m(nz)\equiv 0,
\]
with `\gamma_{m,n}\in\C`.

Evaluate at `z=iy` with `y\to +\infty`. Since
\[
J_m(iny)=i^m I_m(ny),
\qquad
I_m(ny)\sim \frac{e^{ny}}{\sqrt{2\pi ny}},
\]
the largest active frequency dominates exponentially. Therefore all coefficients with the largest
`n` must vanish. Descending induction on `n` then shows every `\gamma_{m,n}=0`, and finally
`c=0`.

So `\mathcal{T}_{M,N}` is indeed the direct sum of the individual frequency images.

## Research meaning, sharpened

This upgrades the previous kernel theorem into a full structural statement.

For fixed bandwidth `(M,N)`, the denominator obstruction is exactly a linear map

\[
\mathcal{H}_{M,N}
\twoheadrightarrow
\mathcal{T}_{M,N},
\]

with explicit finite-dimensional image and explicit kernel.

So at the finite-band level, the exact denominator mechanism is not just computable. It is
linear-algebraically complete:

1. the entire obstruction data lives in a finite-dimensional Bessel model;
2. the beta-uniform Möbius sector is exactly the kernel;
3. all further resonance questions take place on the quotient.

This is much closer to a genuine mechanism theorem than the original pure vertical family alone.
