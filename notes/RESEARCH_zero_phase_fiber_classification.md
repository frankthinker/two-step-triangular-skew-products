# Exact Classification of the Zero-Phase Fiber on Bounded-Bandwidth Windows

## Goal

The corrected realized-side map is the self-normalized quadratic Prüfer map
\[
\Psi_{K,L}:[x]\longmapsto [P_x:Q_x],
\qquad
P_x=A(0)A+B(0)B,\quad Q_x=A(0)B-B(0)A.
\]

The first natural nontrivial fiber is the zero-phase fiber
\[
\Psi_{K,L}^{-1}(0).
\]

This note proves that this fiber is not complicated at all. It is universal across all bounded
windows.

> On every bounded bandwidth window, the zero-phase fiber is exactly the union of two projective
> lines.

## 1. The two obvious lines

Let `\mathcal W_{K,L}` be the bounded-bandwidth realized pair space.

The first line is the constant-phase line
\[
\mathcal L_{\mathrm{const}}:=\mathbb P\langle J_0,J_1\rangle.
\]
Indeed, if
\[
x=a_0J_0+c_0J_1,
\]
then `A=a_0`, `B=c_0`, hence `Q_x=0`.

The second line comes from the kernel of the `A`-channel:
\[
\mathcal L_{A=0}:=\mathbb P\langle J_1,\widetilde J_2-J_0\rangle.
\]
Indeed,
\[
\widetilde J_2-J_0=(0,-2u)
\]
in the `(J_0,J_1)` basis, so every point on this line has `A\equiv 0`, hence also `Q_x=0`.

Thus
\[
\mathcal L_{\mathrm{const}}\cup\mathcal L_{A=0}
\subset \Psi_{K,L}^{-1}(0).
\]

## 2. Two auxiliary reconstruction facts

The proof of the converse uses only the triangular central-factorial structure.

### Proposition 2.1

If
\[
F=a_0J_0+\sum_{k=1}^{K} b_k\widetilde J_{2k}+\sum_{\ell=0}^{L} c_\ell \widetilde J_{2\ell+1}
\]
satisfies
\[
A_F\equiv 0,
\]
then
\[
b_k=0\ (k\ge 2),\qquad c_\ell=0\ (\ell\ge 1),\qquad a_0+b_1=0.
\]
Hence
\[
F\in \operatorname{span}\{J_1,\widetilde J_2-J_0\}.
\]

### Proof

In the `A`-channel:

- the coefficient of `u^{2K-2}` recovers `b_K` for `K\ge 2`;
- descending in even degrees recovers `b_{K-1},\dots,b_2`;
- the coefficient of `u^{2L-1}` recovers `c_L` for `L\ge 1`;
- descending in odd degrees recovers `c_{L-1},\dots,c_1`.

So `A_F\equiv 0` forces all these coefficients to vanish. The remaining constant term is
`a_0+b_1`, hence it also vanishes. No condition involves `c_0`, which is exactly the `J_1`
direction.

### Proposition 2.2

Fix `\lambda\in\mathbb R`. If
\[
B_F=\lambda A_F,
\]
then
\[
b_k=0\ (k\ge 1),\qquad c_\ell=0\ (\ell\ge 1),\qquad c_0=\lambda a_0.
\]
Hence
\[
F\in \operatorname{span}\{J_0+\lambda J_1\}.
\]

### Proof

Consider the polynomial identity
\[
B_F-\lambda A_F\equiv 0.
\]

Its highest odd degree is `2K-1`, coming only from `\widetilde J_{2K}`. Hence `b_K=0`.
Its highest even degree is then `2L`, coming only from `\widetilde J_{2L+1}`. Hence `c_L=0`.

Repeating downward in alternating parity gives
\[
b_K=b_{K-1}=\cdots=b_1=0,
\qquad
c_L=c_{L-1}=\cdots=c_1=0.
\]

What remains is
\[
B_F-\lambda A_F=c_0-\lambda a_0,
\]
so `c_0=\lambda a_0`.

## 3. Exact zero-phase classification

### Theorem 3.1

For every bounded bandwidth window `(K,L)`,
\[
\Psi_{K,L}^{-1}(0)

=
\mathcal L_{\mathrm{const}}\ \cup\ \mathcal L_{A=0}

=
\mathbb P\langle J_0,J_1\rangle
\ \cup\
\mathbb P\langle J_1,\widetilde J_2-J_0\rangle.
\]

### Proof

Let `[x]` lie in the zero-phase fiber, so `Q_x=0`.

Write
\[
a:=A_x(0),\qquad b:=B_x(0).
\]
Because `x` belongs to the domain of the normalized map, `(a,b)\neq (0,0)`.

If `a\neq 0`, then
\[
aB_x-bA_x=0
\]
implies
\[
B_x=\lambda A_x,
\qquad \lambda=b/a.
\]
By Proposition 2.2, `x\in \mathcal L_{\mathrm{const}}`.

If `a=0`, then `b\neq 0`, and the identity `aB_x-bA_x=0` reduces to `A_x=0`. By
Proposition 2.1, `x\in \mathcal L_{A=0}`.

The reverse inclusion was already observed in Section 1.

## 4. Geometric interpretation

The zero-phase fiber has a universal shape:

- one line consists of genuinely constant phase profiles;
- the other consists of profiles whose `A`-channel vanishes identically.

These two lines meet at the common point
\[
[J_1].
\]

So the first nontrivial fiber of the realized quadratic Prüfer map is a reducible projective
curve with exactly two components, independent of the window.

## 5. Research meaning

This is the first exact global fiber classification on the realized side.

It shows that:

1. the positive-dimensional fibers are not arbitrary;
2. the zero-phase degeneracy is completely rigid and universal;
3. every more complicated fiber must occur away from `R=0`.

So the next realized-side frontier is more sharply focused:

> classify the nonzero fibers of the quadratic self-normalized Prüfer map, starting with the
> first genuinely nonconstant phase quotients.
