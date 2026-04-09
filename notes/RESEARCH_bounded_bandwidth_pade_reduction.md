# A Padé Reduction of the Bounded-Bandwidth Prüfer Inversion Problem

## Goal

The central-factorial basis theorem and the bounded-bandwidth reconstruction theorem show that
coefficient jets are globally triangular on every finite even/odd bandwidth window. But the
normalized Prüfer map does not expose the raw coefficient jet; it exposes only the phase jet.

This note isolates the remaining gap.

The key point is:

> on every bounded bandwidth window, sufficiently high normalized Prüfer jets determine the
> rational phase quotient exactly.

So the remaining inverse problem is not a support-family problem. It is a finite-dimensional
amplitude-lifting problem inside the central-factorial coefficient space.

## 1. Bounded bandwidth and rational phase quotient

Fix a window
\[
\mathcal V_{K,L}
=
\left\{
F(t)=a_0J_0(t)+\sum_{k=1}^{K} b_k \widetilde J_{2k}(t)
+\sum_{\ell=0}^{L} c_\ell \widetilde J_{2\ell+1}(t)
\right\}.
\]

Write
\[
F(t)=A(u)J_0(t)+B(u)J_1(t),
\qquad u=t^{-1}.
\]

By the exact normalized Lommel formulas:

- each even mode `\widetilde J_{2k}` contributes degree `2k-2` to `A` and degree `2k-1` to `B`;
- each odd mode `\widetilde J_{2\ell+1}` contributes degree `2\ell-1` to `A` and degree
  `2\ell` to `B`.

Hence every element of `\mathcal V_{K,L}` satisfies
\[
\deg A\le d_A:=\max(2K-2,\,2L-1),
\qquad
\deg B\le d_B:=\max(2K-1,\,2L).
\]

Let
\[
z_0:=A(0)+iB(0)\neq 0,
\qquad
C(u)+iS(u):=\frac{A(u)+iB(u)}{z_0}.
\]
Then
\[
C(0)=1,\qquad S(0)=0,
\]
and the normalized Prüfer equation is
\[
\tan s(u)=\frac{S(u)}{C(u)}=:R_F(u).
\]

Since `C,S` are polynomials, `R_F` is a rational function with
\[
\deg \operatorname{num}(R_F)\le d_B,
\qquad
\deg \operatorname{den}(R_F)\le d_A.
\]

## 2. Finite Prüfer jets determine the rational quotient

The formal series `s(u)` determines `R_F(u)=\tan s(u)` coefficientwise. Conversely, if a formal
power series is known to come from a rational function with prescribed numerator/denominator
degree bounds, a sufficiently long jet determines that rational function uniquely by Padé
reconstruction.

### Proposition 2.1

Fix degree bounds `(d_B,d_A)`. Let
\[
R(u)=\sum_{r\ge 1}\rho_r u^r
\]
be a formal power series known a priori to equal a rational function
\[
R(u)=\frac{P(u)}{Q(u)},
\qquad
Q(0)=1,\quad
\deg P\le d_B,\quad
\deg Q\le d_A,
\]
with `P,Q` coprime.

Then the coefficients
\[
\rho_1,\dots,\rho_{d_A+d_B+1}
\]
determine `R` uniquely.

### Proof

Write
\[
P(u)=p_1u+\cdots+p_{d_B}u^{d_B},
\qquad
Q(u)=1+q_1u+\cdots+q_{d_A}u^{d_A}.
\]
The identity `Q(u)R(u)-P(u)=0` modulo `u^{d_A+d_B+2}` gives a square linear system in the
unknown coefficients `(p_i,q_j)`. On the coprime locus this is exactly the standard Padé
reconstruction system, hence has a unique solution.

### Corollary 2.2

On every bounded bandwidth window `\mathcal V_{K,L}`, sufficiently high normalized Prüfer jets
determine the rational phase quotient `R_F=S/C` exactly.

## 3. What remains after Padé reconstruction

Once `R_F` is known exactly, the profile is not yet recovered. One still has to lift the rational
phase quotient to an actual pair `(C,S)` and hence to a coefficient pair `(A,B)`.

There are two sources of nontriviality:

1. `R_F=S/C` remembers only the projective direction of `(C,S)`, not the amplitude `C`;
2. the lifted pair `(A,B)=z_0(C,S)` must lie in the finite-dimensional central-factorial
   coefficient space coming from the bounded bandwidth window.

So the inverse problem decomposes into two layers:

\[
\text{Prüfer jet}
\Longrightarrow
\text{rational phase quotient }R_F
\Longrightarrow
\text{amplitude lift inside the central-factorial model space.}
\]

This is the exact point where the project becomes a finite-dimensional moduli problem rather than
a family-by-family elimination problem.

## 4. The amplitude-lifting problem

Let
\[
\mathcal W_{K,L}
\subset
\mathbb C[u]
\]
denote the space of complex polynomials of the form
\[
Z(u)=A(u)+iB(u)
\]
arising from `\mathcal V_{K,L}`.

Then the bounded-bandwidth Prüfer inversion problem is:

> given a rational function `R(u)`, classify all `Z\in\mathcal W_{K,L}` such that
> \[
> \frac{\Im(Z/Z(0))}{\Re(Z/Z(0))}=R.
> \]

Equivalently, one seeks the fiber of the map
\[
Z\longmapsto \frac{S_Z}{C_Z}
\]
inside the finite-dimensional linear space `\mathcal W_{K,L}`.

The bounded-bandwidth reconstruction theorem shows that `\mathcal W_{K,L}` itself is completely
under control. So all remaining difficulty is concentrated in this amplitude-lifting fiber.

## 5. Generic shell rigidity

The amplitude-lifting problem already has a clean generic answer.

Write
\[
d_B:=\max(2K-1,\,2L).
\]
Because of the parity split:

- if `2K-1>2L`, then the coefficient of `u^{d_B}` in `B` is exactly `b_K f_{K,K-1}`;
- if `2L>2K-1`, then the coefficient of `u^{d_B}` in `B` is exactly `c_L h_{L,L}`;
- if `2L=2K-1`, which never occurs, there would be a mixed top block.

So the top coefficient of `B` comes from a unique highest mode.

### Theorem 5.1

Let `F\in\mathcal V_{K,L}` and assume that its `J_1`-channel polynomial `B_F(u)` has maximal
degree `d_B`. Then the amplitude lift of the normalized phase quotient `R_F=S_F/C_F` is unique
inside `\mathcal V_{K,L}`.

Equivalently, if `G\in\mathcal V_{K,L}` has the same normalized phase quotient as `F`, then
`G=F`.

### Proof

If `F` and `G` have the same normalized phase quotient, then by the discussion above there is a
real polynomial `h(u)` with `h(0)=1` such that
\[
C_G=h\,C_F,
\qquad
S_G=h\,S_F,
\]
hence
\[
B_G=h\,B_F.
\]

If `h` is nonconstant, then
\[
\deg B_G=\deg h+\deg B_F>d_B,
\]
contradicting `G\in\mathcal V_{K,L}`. Therefore `h=1`, so `B_G=B_F`. The bounded-bandwidth
reconstruction theorem then gives `G=F`.

### Corollary 5.2

The normalized Prüfer map is injective on the open dense shell
\[
\{F\in\mathcal V_{K,L}:\deg B_F=d_B\}.
\]

So bounded-bandwidth fiber nonuniqueness, if it exists at all, is forced onto lower-degree
boundary strata.

## 6. Research meaning

This note pushes the finite-jet program one step farther.

Previously the frontier looked like:

\[
\text{finite jet coefficients}
\Longrightarrow
\text{support/family elimination}.
\]

Now it looks like:

\[
\text{finite Prüfer jet}
\Longrightarrow
\text{Padé reconstruction of }R_F
\Longrightarrow
\text{amplitude lifting in }\mathcal W_{K,L}.
\]

And Theorem 5.1 shows that this amplitude-lifting problem is already solved on the generic shell.
So the deepest remaining question on bounded bandwidth windows is no longer “what family should
be eliminated next?” It is:

> when is the amplitude lift unique?

That is the right formulation of local or global fiber rigidity for the bounded-bandwidth
normalized Prüfer map.
