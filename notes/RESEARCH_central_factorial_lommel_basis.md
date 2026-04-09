# A Central-Factorial Basis Theorem for the Normalized Lommel Coefficients

## Goal

The previous note only recorded an order-`6` symbolic pattern:

> the normalized Lommel coefficient polynomials appear to form a parity-adapted
> central-factorial basis in the squared order.

That pattern is now proved in full.

The point is not merely to obtain prettier coefficient formulas. The point is that the finite-jet
maps of the anchored Prüfer problem are built from a triangular basis, so bounded-support fiber
rigidity becomes a Prony-type reconstruction problem.

## 1. Normalized modes

Write
\[
u:=t^{-1}.
\]

For even and odd modes, use the sign-normalized basis
\[
\widetilde J_{2k}:=(-1)^k J_{2k},
\qquad
\widetilde J_{2k+1}:=(-1)^k J_{2k+1}.
\]

Each normalized mode has a unique `(J_0,J_1)`-decomposition
\[
\widetilde J_{2k}(t)=\widetilde A_{2k}(u)J_0(t)+\widetilde B_{2k}(u)J_1(t),
\]
\[
\widetilde J_{2k+1}(t)=\widetilde A_{2k+1}(u)J_0(t)+\widetilde B_{2k+1}(u)J_1(t).
\]

Write the parity expansions as
\[
\widetilde A_{2k}(u)=\sum_{j=0}^{k-1} e_{k,j}u^{2j},
\qquad
\widetilde B_{2k}(u)=\sum_{j=0}^{k-1} f_{k,j}u^{2j+1},
\]
\[
\widetilde A_{2k+1}(u)=\sum_{j=0}^{k} g_{k,j}u^{2j+1},
\qquad
\widetilde B_{2k+1}(u)=\sum_{j=0}^{k} h_{k,j}u^{2j}.
\]

We keep the squared-order variables
\[
M:=(2k)^2,
\qquad
N:=(2k+1)^2.
\]

## 2. Lommel closed forms

The standard Lommel relation gives
\[
J_n(t)=-R_{n-2,2}(t)\,J_0(t)+R_{n-1,1}(t)\,J_1(t)
\qquad (n\ge 1),
\]
where
\[
R_{m,\nu}(t)
=
\sum_{r=0}^{\lfloor m/2\rfloor}
(-1)^r
\binom{m-r}{r}
\frac{\Gamma(\nu+m-r)}{\Gamma(\nu+r)}
\Bigl(\frac{2}{t}\Bigr)^{m-2r}.
\]

Substituting `n=2k,2k+1`, inserting the sign normalization, and re-indexing the summation
gives the coefficient-level formulas below.

### Proposition 2.1

For every `k\ge 1` and `0\le j\le k-1`,
\[
e_{k,j}
=
(-1)^j
\frac{4^j}{(2j)!}\,
k^2
\prod_{r=1}^{j-1}(k^2-r^2)^2
(k^2-j^2),
\]
\[
f_{k,j}
=
(-1)^{j+1}
\frac{2\cdot 4^j}{(2j+1)!}\,
k^2
\prod_{r=1}^{j}(k^2-r^2)^2.
\]

For every `k\ge 0`, `0\le j\le k`,
\[
g_{k,j}
=
(-1)^j
\frac{2\cdot 4^j}{(2j+1)!}\,
(k-j)(k+j+1)
\prod_{r=0}^{j-1}(k-r)^2(k+r+1)^2,
\]
and for every `k\ge 0`, `1\le j\le k`,
\[
h_{k,j}
=
(-1)^j
\frac{4^j}{(2j)!}\,
\prod_{r=0}^{j-1}(k-r)^2(k+r+1)^2,
\qquad
h_{k,0}=1.
\]

### Proof

For `J_{2k}`, the Lommel formula gives
\[
\widetilde J_{2k}(t)
=
(-1)^{k+1}R_{2k-2,2}(t)\,J_0(t)
+(-1)^k R_{2k-1,1}(t)\,J_1(t).
\]

The coefficient of `u^{2j}` in the first term comes from the index `r=k-j-1`, hence
\[
e_{k,j}
=
(-1)^j
2^{2j}
\binom{k+j-1}{2j}
\frac{(k+j)!}{(k-j)!}.
\]
Elementary factorial manipulation yields
\[
\binom{k+j-1}{2j}\frac{(k+j)!}{(k-j)!}
=
\frac{k^2}{(2j)!}
\prod_{r=1}^{j-1}(k^2-r^2)^2
(k^2-j^2),
\]
which gives the claimed formula for `e_{k,j}`.

The coefficient of `u^{2j+1}` in the `J_1` term comes from the index `r=k-j-1`, so
\[
f_{k,j}
=
(-1)^{j+1}
2^{2j+1}
\binom{k+j}{2j+1}
\frac{(k+j)!}{(k-j-1)!}.
\]
Again, the factorials reorganize as
\[
\binom{k+j}{2j+1}\frac{(k+j)!}{(k-j-1)!}
=
\frac{k^2}{(2j+1)!}\prod_{r=1}^{j}(k^2-r^2)^2,
\]
giving the stated formula.

For `J_{2k+1}`, the Lommel formula gives
\[
\widetilde J_{2k+1}(t)
=
(-1)^{k+1}R_{2k-1,2}(t)\,J_0(t)
+(-1)^k R_{2k,1}(t)\,J_1(t).
\]

The coefficient of `u^{2j+1}` in the `J_0` term comes from the index `r=k-j-1`, hence
\[
g_{k,j}
=
(-1)^j
2^{2j+1}
\binom{k+j}{2j+1}
\frac{(k+j+1)!}{(k-j)!},
\]
and factorial rearrangement gives the claimed product form.

Similarly, the coefficient of `u^{2j}` in the `J_1` term comes from `r=k-j`, giving
\[
h_{k,j}
=
(-1)^j
2^{2j}
\binom{k+j}{2j}
\frac{(k+j)!}{(k-j)!},
\]
which simplifies to the stated product formula.

## 3. Squared-order form

Rewriting Proposition 2.1 in `M=(2k)^2` and `N=(2k+1)^2` yields the exact coefficient
polynomials appearing in the finite-jet notes.

### Theorem 3.1

For even modes,
\[
\widetilde A_{2k}(u)=\sum_{j=0}^{k-1} E_j(M)u^{2j},
\qquad
\widetilde B_{2k}(u)=\sum_{j=0}^{k-1} F_j(M)u^{2j+1},
\]
with
\[
E_0(M)=1,
\]
\[
E_j(M)
=
(-1)^j\,
\frac{
M(M-4)^2(M-16)^2\cdots(M-(2j-2)^2)^2(M-(2j)^2)
}
{4^j(2j)!}
\]
for `j\ge 1`, and
\[
F_j(M)
=
(-1)^{j+1}\,
\frac{
M(M-4)^2(M-16)^2\cdots(M-(2j)^2)^2
}
{2\cdot 4^j(2j+1)!}
\]
for `j\ge 0`.

For odd modes,
\[
\widetilde A_{2k+1}(u)=\sum_{j=0}^{k} G_j(N)u^{2j+1},
\qquad
\widetilde B_{2k+1}(u)=\sum_{j=0}^{k} H_j(N)u^{2j},
\]
with
\[
G_j(N)
=
(-1)^j\,
\frac{
(N-(2j+1)^2)(N-1)^2(N-9)^2\cdots(N-(2j-1)^2)^2
}
{2\cdot 4^j(2j+1)!},
\]
\[
H_0(N)=1,
\]
\[
H_j(N)
=
(-1)^j\,
\frac{
(N-1)^2(N-9)^2\cdots(N-(2j-1)^2)^2
}
{4^j(2j)!}
\]
for `j\ge 1`.

### Proof

This is the same theorem as Proposition 2.1 after the substitutions
\[
M=4k^2,\qquad N=(2k+1)^2,
\]
and the elementary identities
\[
4k^2-(2r)^2=4(k^2-r^2),
\qquad
(2k+1)^2-(2r+1)^2=4(k-r)(k+r+1).
\]

## 4. Why this is a central-factorial basis

The coefficient families of Theorem 3.1 have three decisive properties.

### 4.1 Exact degree growth

\[
\deg E_j=2j,\qquad
\deg F_j=2j+1,\qquad
\deg G_j=2j+1,\qquad
\deg H_j=2j.
\]

### 4.2 Spectral vanishing with parity splitting

- `E_j` and `F_j` vanish at lower even squares;
- `G_j` and `H_j` vanish at lower odd squares.

Moreover, all interior same-parity squares occur with multiplicity `2`.

### 4.3 Triangularity

If the even supports are ordered by `2k_1<\cdots<2k_s`, then
\[
E_{k_\ell-1}\bigl((2k_i)^2\bigr)=0
\qquad (i<\ell),
\]
but
\[
E_{k_\ell-1}\bigl((2k_\ell)^2\bigr)\neq 0.
\]
The same statement holds for `F`, and similarly on the odd side with `G` or `H`.

So these families form a parity-adapted central-factorial basis, not just a collection of
polynomials with nice roots.

## 5. Bounded-support Prony reconstruction

The triangularity has an immediate rigidity consequence.

### Corollary 5.1

Fix distinct even supports
\[
2k_1<\cdots<2k_s
\]
and distinct odd supports
\[
2\ell_1+1<\cdots<2\ell_t+1.
\]
On the anchored stratum supported exactly on these modes, sufficiently high finite jets of the
normalized Prüfer map determine all support weights uniquely.

In particular, every finite-jet fiber is discrete on every fixed-support anchored stratum.

### Proof

The `(J_0,J_1)` coefficient jets are linear combinations of the basis values
\[
E_j\bigl((2k_i)^2\bigr),\ F_j\bigl((2k_i)^2\bigr),\ 
G_j\bigl((2\ell_r+1)^2\bigr),\ H_j\bigl((2\ell_r+1)^2\bigr).
\]

By the triangularity above, the matrices
\[
\bigl(E_{k_\ell-1}((2k_i)^2)\bigr)_{1\le \ell,i\le s},
\qquad
\bigl(H_{\ell_r}((2\ell_i+1)^2)\bigr)_{1\le r,i\le t}
\]
are triangular with nonzero diagonal after ordering supports increasingly. The same is true with
`F` or `G`. Hence the support weights may be solved recursively from sufficiently many jet
coordinates. Since the normalized Prüfer jet factors through these finitely many coefficient
moments, the finite-jet fiber is discrete on the fixed-support stratum.

## 6. Research meaning

This theorem changes the current project in a decisive way.

The finite-dimensional jet maps `\mathfrak m_L` are not arbitrary truncations. They are built
from an exact parity-split central-factorial basis. Therefore the bounded-support fiber problem
is not a vague support-combinatorics problem; it is a Prony-type reconstruction problem in a
highly structured basis.

So the right next theorem is no longer:

> compute one more low-order elimination.

It is:

> understand whether the central-factorial moment jets are globally or locally injective on
> natural anchored regions.

That is the current deepest route to a genuinely unified rigidity theorem.
