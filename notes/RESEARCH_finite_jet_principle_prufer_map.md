# A Finite-Jet Principle for the Anchored Mixed-Parity Prüfer Map

## Goal

The second- and third-order notes show a strong pattern:

- at order `2`, the anchored mixed-parity fiber depends only on three complex moments
  `z_0,z_1,z_2`;
- at order `3`, it depends only on four complex moments `z_0,z_1,z_2,z_3`.

This note records the conceptual statement behind those formulas.

The main point is:

> every finite-order normalized Prüfer jet factors through a finite-dimensional moment-jet map.

So the remaining frontier is not “classify all support-`k` families”; it is a finite-jet
fiber-rigidity problem.

## 1. Formal Prüfer equation

Let
\[
F(t)=A(u)J_0(t)+B(u)J_1(t),
\qquad
u=t^{-1},
\]
where
\[
A(u)=A_0+A_1u+\cdots,\qquad B(u)=B_0+B_1u+\cdots,
\qquad
A_0^2+B_0^2\neq 0.
\]

Rotate the leading oscillatory phase so that the zero equation takes the normalized form
\[
-C(u)\sin s(u)+S(u)\cos s(u)=0,
\]
with
\[
C(u)=1+\sum_{r\ge 1} c_r u^r,
\qquad
S(u)=\sum_{r\ge 1} s_r u^r,
\qquad
s(u)=\sum_{r\ge 1}\lambda_r u^r.
\]

Then
\[
\tan s(u)=\frac{S(u)}{C(u)},
\]
hence
\[
s(u)=\arctan\!\Bigl(\frac{S(u)}{C(u)}\Bigr)
\]
as a formal power series.

### Proposition 1.1

For every `L\ge 1`, the truncated Prüfer jet
\[
(\lambda_1,\dots,\lambda_L)
\]
is a universal polynomial-rational expression in the truncated coefficient jet
\[
(c_1,\dots,c_L,s_1,\dots,s_L).
\]

In particular, the first `L` Prüfer coefficients depend only on the first `L` coefficients of
`C` and `S`.

### Proof

The formal quotient `S/C` depends only on the `L`-jet of `(C,S)` modulo `u^{L+1}`. The formal
series `\arctan v` has no constant term, so its coefficient of `u^r` depends only on the
coefficients of `v` up to order `r`. Therefore the coefficient of `u^r` in
\[
\arctan(S/C)
\]
depends only on `(c_1,\dots,c_r,s_1,\dots,s_r)`. This gives the universal dependence for every
`r\le L`.

## 2. Exact mode recurrences and polynomial jet coefficients

Write the normalized modes as
\[
\widetilde J_m(t)=\widetilde A_m(u)J_0(t)+\widetilde B_m(u)J_1(t),
\]
where for even `m=2k` and odd `m=2k+1` we use the sign normalizations from the earlier notes.

The exact Bessel recurrence
\[
J_{n+1}(t)=\frac{2n}{t}J_n(t)-J_{n-1}(t)
\]
induces the exact recurrence
\[
X_{n+1}(u)=2nu\,X_n(u)-X_{n-1}(u)
\qquad (X=A,B).
\]

This has two decisive consequences.

### Proposition 2.1

For every `L\ge 0` there exist polynomials
\[
P^{\mathrm{ev}}_{j}(M),\quad Q^{\mathrm{ev}}_{j}(M),\quad
P^{\mathrm{odd}}_{j}(N),\quad Q^{\mathrm{odd}}_{j}(N)
\]
in one variable such that, for every even `m` with `M=m^2`,
\[
\widetilde J_m(t)
=
\Bigl(\sum_{j=0}^{L}P^{\mathrm{ev}}_j(M)u^{2j}+O(u^{2L+2})\Bigr)J_0(t)
+\Bigl(\sum_{j=0}^{L-1}Q^{\mathrm{ev}}_j(M)u^{2j+1}+O(u^{2L+1})\Bigr)J_1(t),
\]
and for every odd `n` with `N=n^2`,
\[
\widetilde J_n(t)
=
\Bigl(\sum_{j=0}^{L-1}P^{\mathrm{odd}}_j(N)u^{2j+1}+O(u^{2L+1})\Bigr)J_0(t)
+\Bigl(\sum_{j=0}^{L}Q^{\mathrm{odd}}_j(N)u^{2j}+O(u^{2L+2})\Bigr)J_1(t).
\]

Thus every finite jet coefficient is a polynomial in the squared order.

### Proof sketch

This is proved by induction on the order using the exact recurrence above. The parity statement
is preserved by the recurrence, and after sign normalization the coefficients become invariant
under `m\mapsto -m`, hence polynomial in `m^2`. The same argument applies to odd modes.

The first instances are exactly the explicit formulas already proved in the second- and
third-order notes.

## 3. Moment jets

Consider an anchored mixed-parity profile
\[
F(t)=J_0(t)+\sum_{m\in\mathcal E} b_m\widetilde J_m(t)+\sum_{n\in\mathcal O} c_n\widetilde J_n(t).
\]

Fix an order `L`. Using Proposition 2.1, the coefficients of
\[
A(u)=\sum_{r=0}^{L}A_r u^r+O(u^{L+1}),
\qquad
B(u)=\sum_{r=0}^{L}B_r u^r+O(u^{L+1})
\]
can be written as finite linear combinations of the aggregated moments
\[
M^{\mathrm{ev}}_j:=\sum_{m\in\mathcal E} P^{\mathrm{ev}}_j(m^2)b_m,
\qquad
N^{\mathrm{ev}}_j:=\sum_{m\in\mathcal E} Q^{\mathrm{ev}}_j(m^2)b_m,
\]
\[
M^{\mathrm{odd}}_j:=\sum_{n\in\mathcal O} P^{\mathrm{odd}}_j(n^2)c_n,
\qquad
N^{\mathrm{odd}}_j:=\sum_{n\in\mathcal O} Q^{\mathrm{odd}}_j(n^2)c_n.
\]

So every finite jet of `(A,B)` factors through a finite-dimensional moment-jet map.

## 4. Finite-jet principle

Combining Sections 1 and 3 gives the main statement.

### Theorem 4.1

For every `L\ge 1` there exists a finite-dimensional real vector space `\mathcal M_L` and a
real-analytic moment-jet map
\[
\mathfrak m_L:\{\text{anchored mixed-parity profiles}\}\to \mathcal M_L
\]
such that the first `L` normalized Prüfer coefficients factor as
\[
F\mapsto \mathfrak m_L(F)\mapsto (\lambda_1(F),\dots,\lambda_L(F)).
\]

Equivalently, the `L`-jet of the normalized Prüfer map depends only on finitely many aggregated
moments of the profile and is completely insensitive to support size beyond those moments.

### Proof

By Proposition 2.1, the `L`-jet of `(A,B)` is a function of finitely many aggregated moments.
By Proposition 1.1, the first `L` Prüfer coefficients depend only on the `L`-jet of the
rotated pair `(C,S)`, hence only on the `L`-jet of `(A,B)`. Therefore they factor through a
finite-dimensional moment-jet map.

## 5. What this changes

This theorem is the conceptual compression that the previous support-three notes were pointing
toward.

The old picture was:

> many support families, each with its own elimination.

The new picture is:

> the normalized Prüfer map has finite jet fibers, and support-family eliminations are low-order
> shadows of that moduli problem.

So the remaining frontier is not primarily combinatorial in support. It is geometric:

> how rigid are the fibers of the finite jet maps `\mathfrak m_L`?

## 6. Immediate consequences

1. `support-three` is no longer the natural unit of analysis.
2. `support \ge 4` is already compressed to finite-dimensional jet geometry.
3. Any future theorem that proves injectivity of `\mathfrak m_L` on a natural region will
   automatically collapse infinitely many family-level problems at once.

This is the deepest unified mechanism obtained so far.
