# Boundary-Strata Thinness for the Bounded-Bandwidth Amplitude-Lifting Problem

## Goal

The bounded-bandwidth Pad\'e reduction shows that a sufficiently high normalized Prüfer jet
determines the rational phase quotient
\[
R_F(u)=\frac{S_F(u)}{C_F(u)}.
\]

The remaining inverse problem is the amplitude lift:

> given `R_F`, how many normalized pairs `(C,S)` inside the bounded-bandwidth model space realize
> it?

This note records the first genuinely general answer.

The point is not to prove full uniqueness on the boundary. The point is to prove that every
nontrivial lift ambiguity is forced onto explicitly thin boundary strata.

## 1. Bounded-bandwidth normalized phase pairs

Fix a bounded even/odd window `\mathcal V_{K,L}` as in
[RESEARCH_bounded_bandwidth_pade_reduction.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_bounded_bandwidth_pade_reduction.md).

For `F\in\mathcal V_{K,L}`, write
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

Since division by the nonzero scalar `z_{0,F}` does not change degrees,
\[
\deg C_F\le d_A,
\qquad
\deg S_F\le d_B,
\]
where
\[
d_A:=\max(2K-2,\,2L-1),
\qquad
d_B:=\max(2K-1,\,2L).
\]

## 2. Multiplicative relation for common phase quotient

If two bounded-bandwidth profiles `F,G` have the same normalized phase quotient, then
\[
\frac{S_F}{C_F}=\frac{S_G}{C_G}.
\]
Equivalently,
\[
S_FC_G-S_GC_F=0.
\]

Let `(\widehat C,\widehat S)` be the unique reduced coprime pair representing this common
quotient and normalized by
\[
\widehat C(0)=1.
\]
Then there exist unique real polynomials `h_F,h_G` with
\[
h_F(0)=h_G(0)=1
\]
such that
\[
C_F=h_F\widehat C,\qquad S_F=h_F\widehat S,
\]
\[
C_G=h_G\widehat C,\qquad S_G=h_G\widehat S.
\]

Thus every ambiguity between two lifts is measured by the real polynomial
\[
h:=h_G/h_F,
\]
and the degree of the ambiguity is the degree of `h`.

## 3. Top-shell rigidity revisited

If `h` is nonconstant of degree `s\ge 1`, then
\[
S_G=h\,S_F.
\]
Since `\deg S_G\le d_B`, the product `hS_F` must suffer cancellation at the top `s` degrees.
This is the source of boundary thinness.

Define the descending boundary flag by
\[
\mathcal B_s
:=
\left\{
F\in\mathcal V_{K,L}:
[u^{d_B}]S_F=\cdots=[u^{d_B-s+1}]S_F=0
\right\},
\qquad s\ge 1.
\]

Because the normalized phase map is real-analytic and the coefficients of `S_F` are
real-analytic functions of the profile coefficients, each `\mathcal B_s` is a real-analytic
subset. Whenever the corresponding top coefficients are genuinely present in the window, these
strata have codimension at least `s`.

## 4. Degree-s ambiguity forces codimension-s vanishing

### Proposition 4.1

Let `F,G\in\mathcal V_{K,L}` have the same normalized phase quotient. Suppose the associated
multiplier `h` is a nonconstant real polynomial of degree `s\ge 1`. Then
\[
F,G\in\mathcal B_s.
\]

Equivalently, every degree-`s` amplitude-lifting ambiguity is forced onto the codimension-`s`
top boundary stratum of the normalized `S`-channel.

### Proof

Write
\[
h(u)=1+h_1u+\cdots+h_su^s,
\qquad
h_s\neq 0,
\]
and
\[
S_F(u)=\sum_{r=0}^{d_B}\sigma_r u^r.
\]
Since
\[
S_G=hS_F
\]
and `\deg S_G\le d_B`, the coefficients of `u^{d_B+s},u^{d_B+s-1},\dots,u^{d_B+1}` in `hS_F`
must all vanish.

The coefficient of `u^{d_B+s}` is `h_s\sigma_{d_B}`, hence `\sigma_{d_B}=0`. Then the
coefficient of `u^{d_B+s-1}` reduces to `h_s\sigma_{d_B-1}`, hence `\sigma_{d_B-1}=0`.
Continuing downward gives
\[
\sigma_{d_B}=\sigma_{d_B-1}=\cdots=\sigma_{d_B-s+1}=0.
\]
Thus `F\in\mathcal B_s`. The same argument with `F` and `G` interchanged shows `G\in\mathcal
B_s`.

## 5. Residual fibers are very thin

The proposition gives an immediate geometric corollary.

### Corollary 5.1

Fix a bounded bandwidth window `\mathcal V_{K,L}`. If the normalized Prüfer fiber of a point
contains two distinct lifts whose relative amplitude multiplier has degree `s`, then that fiber
meets the codimension-`s` boundary stratum `\mathcal B_s`.

In particular:

1. the generic shell `\mathcal V_{K,L}\setminus \mathcal B_1` has unique lift;
2. any nonuniqueness locus is contained in the finite union
   \[
   \bigcup_{s=1}^{d_B}\mathcal B_s;
   \]
3. higher-degree lift ambiguities are forced onto successively thinner strata.

This is the precise sense in which the residual fibers are very thin.

## 6. Research meaning

This is the first general theorem about the lower-degree boundary problem.

It does not yet prove uniqueness on the boundary. But it proves something conceptually stronger
than a list of examples:

> nontrivial amplitude lifts are filtered by degree, and a degree-`s` ambiguity costs at least
> `s` top-order vanishing conditions.

So the bounded-bandwidth frontier is no longer a vague “maybe the boundary is messy” problem. It
is a stratified boundary-rigidity problem with an explicit codimension filtration.

The next serious step is therefore:

> decide whether any of the boundary strata `\mathcal B_s` actually support nontrivial lifts, or
> whether they are themselves rigid except on still thinner exceptional sets.
