# Bounded-Bandwidth Reconstruction from the Central-Factorial Moment Jets

## Goal

The central-factorial basis theorem shows that on a fixed-support stratum, sufficiently high jet
coordinates determine the support weights uniquely. But the coefficient formulas are much more
triangular than that.

This note records the stronger bounded-bandwidth statement:

> on every finite even/odd bandwidth window, the coefficient jet map is globally triangular, so
> the mode coefficients are recovered recursively from the highest support downward.

This is a genuine strengthening of the fixed-support discreteness statement.

## 1. The bounded-bandwidth sector

Fix integers `K\ge 1` and `L\ge 0`. Consider the anchored mixed-parity bandwidth window
\[
\mathcal V_{K,L}
:=
\left\{
F(t)=a_0J_0(t)+\sum_{k=1}^{K} b_k \widetilde J_{2k}(t)
+\sum_{\ell=0}^{L} c_\ell \widetilde J_{2\ell+1}(t)
\right\}.
\]

Write the `(J_0,J_1)`-decomposition as
\[
F(t)=A(u)J_0(t)+B(u)J_1(t),
\qquad u=t^{-1}.
\]

Because of parity,
\[
B(u)
=
\sum_{j=0}^{K-1}\beta^{\mathrm{ev}}_j u^{2j+1}
+
\sum_{j=0}^{L}\beta^{\mathrm{odd}}_j u^{2j}.
\]

The key point is that the two parity blocks are already triangular in the support index.

## 2. Even block

By the central-factorial theorem, the even contribution to `B` is
\[
\sum_{k=1}^{K} b_k \widetilde B_{2k}(u)
=
\sum_{k=1}^{K}\sum_{j=0}^{k-1} b_k f_{k,j}u^{2j+1},
\]
where
\[
f_{k,j}=0\qquad (j\ge k),
\]
and
\[
f_{k,k-1}
=
(-1)^k
\frac{2\cdot 4^{k-1}}{(2k-1)!}
k^2\prod_{r=1}^{k-1}(k^2-r^2)^2
\neq 0.
\]

So the coefficient of `u^{2K-1}` in `B` is exactly `b_K f_{K,K-1}`. Hence `b_K` is recovered
immediately. Subtracting its contribution, the coefficient of `u^{2K-3}` recovers `b_{K-1}`,
and so on.

### Proposition 2.1

The linear map
\[
(b_1,\dots,b_K)\longmapsto
\bigl(\beta^{\mathrm{ev}}_0,\dots,\beta^{\mathrm{ev}}_{K-1}\bigr)
\]
is triangular with nonzero diagonal, hence an isomorphism.

Equivalently, the even mode coefficients are reconstructed uniquely from the odd-power
coefficients of `B(u)`.

## 3. Odd block

Similarly, the odd contribution to `B` is
\[
\sum_{\ell=0}^{L} c_\ell \widetilde B_{2\ell+1}(u)
=
\sum_{\ell=0}^{L}\sum_{j=0}^{\ell} c_\ell h_{\ell,j}u^{2j},
\]
with
\[
h_{\ell,j}=0\qquad (j>\ell),
\]
and
\[
h_{\ell,\ell}
=
(-1)^\ell
\frac{4^\ell}{(2\ell)!}
\prod_{r=0}^{\ell-1}(\ell-r)^2(\ell+r+1)^2
\neq 0.
\]

So the coefficient of `u^{2L}` in `B` is exactly `c_L h_{L,L}`. Hence `c_L` is recovered
first, then recursively `c_{L-1},\dots,c_0`.

### Proposition 3.1

The linear map
\[
(c_0,\dots,c_L)\longmapsto
\bigl(\beta^{\mathrm{odd}}_0,\dots,\beta^{\mathrm{odd}}_{L}\bigr)
\]
is triangular with nonzero diagonal, hence an isomorphism.

Equivalently, the odd mode coefficients are reconstructed uniquely from the even-power
coefficients of `B(u)`.

## 4. Global reconstruction theorem

Putting the two parity blocks together gives the main statement.

### Theorem 4.1

For every bandwidth window `(K,L)`, the coefficient jet map
\[
\Phi_{K,L}:\mathcal V_{K,L}\to \mathbb R^{K+L+2},
\]
\[
F\longmapsto
\Bigl(
a_0,\ 
[u^0]B,\ [u^2]B,\dots,[u^{2L}]B,\ 
[u^1]B,\ [u^3]B,\dots,[u^{2K-1}]B
\Bigr)
\]
is a linear isomorphism.

In particular, the full mode coefficients `(a_0,b_1,\dots,b_K,c_0,\dots,c_L)` are recovered
uniquely from a finite jet of the `J_1`-channel alone.

### Proof

The scalar `a_0` is the coefficient of `J_0` in the anchored basis and is already separated.
Propositions 2.1 and 3.1 show that the odd and even power blocks of `B(u)` reconstruct the even
and odd mode coefficients independently and triangularly. Combining the two reconstructions gives
an inverse to `\Phi_{K,L}`.

## 5. Consequences for finite jet maps

The finite-jet principle says that every finite-order normalized Prüfer jet factors through a
finite-dimensional moment-jet map `\mathfrak m_L`. The present theorem strengthens that picture
on bounded bandwidth windows.

### Corollary 5.1

For every fixed `(K,L)`, sufficiently high coefficient jets are globally injective on
`\mathcal V_{K,L}`.

Equivalently, bounded-bandwidth anchored profiles admit exact finite-dimensional reconstruction.

### Corollary 5.2

On every bounded-bandwidth anchored sector, the moment data entering the finite-jet principle are
not merely discrete invariants of fixed-support strata. They determine the full profile
coefficients globally.

## 6. Research meaning

This changes the interpretation of the project again.

The central-factorial basis theorem does not only imply fixed-support discreteness. It implies a
global triangular reconstruction theory on every bounded bandwidth window.

So the real remaining difficulty is not bounded support itself. The real difficulty is what
happens when the support window is not fixed in advance, or when the normalized Prüfer
reparameterization discards part of the raw coefficient-jet data.

That is a much sharper formulation of the frontier than the old family-by-family picture.
