# A Second-Order Moment Normal Form for the Anchored Mixed-Parity Fiber

## Goal

The current notes close many anchored support-three sectors one by one:

- even-odd sectors at second order;
- odd-odd sectors at second order;
- even-even sectors at fifth order.

This is effective, but still too family-dependent. The real structural question is:

> what part of the profile is actually visible to the anchored normalized Prüfer fiber at low
> order?

This note records a uniform answer for the whole mixed-parity anchored sector. The point is that
at second order the normalized Prüfer map sees only three aggregated moment blocks, irrespective
of how many even or odd modes are present.

## 1. Setup

Let `\mathcal E\subset 2\Z_{\ge 1}` be a finite set of positive even indices and
`\mathcal O\subset 2\Z_{\ge 0}+1` a finite set of positive odd indices. Consider the anchored
mixed-parity profile
\[
F(t)
=
J_0(t)
+\sum_{m\in\mathcal E} b_m \widetilde J_m(t)
+\sum_{n\in\mathcal O} c_n \widetilde J_n(t),
\]
where
\[
\widetilde J_m:=(-1)^{m/2}J_m
\qquad (m\in\mathcal E),
\]
\[
\widetilde J_n:=(-1)^{(n-1)/2}J_n
\qquad (n\in\mathcal O).
\]

Write
\[
F(t)=A(u)J_0(t)+B(u)J_1(t),
\qquad
u=t^{-1}.
\]

Introduce the aggregated even/odd moments
\[
E:=1+\sum_{m\in\mathcal E} b_m,
\qquad
O:=\sum_{n\in\mathcal O} c_n,
\]
\[
X:=\sum_{n\in\mathcal O}(n^2-1)c_n,
\qquad
Y:=\sum_{m\in\mathcal E}m^2 b_m,
\]
\[
U:=\sum_{m\in\mathcal E}m^2(m^2-4)b_m,
\qquad
V:=\sum_{n\in\mathcal O}(n^2-1)^2c_n.
\]

These are the only mixed-parity moments that survive to order `u^2`.

## 2. Universal second-order normal form

By linearity and the low-order mode expansions from
[RESEARCH_prufer_first_jet_normal_form.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_prufer_first_jet_normal_form.md),
one obtains:

### Proposition 2.1

\[
A(u)=E+\frac{X}{2}u-\frac{U}{8}u^2+O(u^3),
\]
\[
B(u)=O-\frac{Y}{2}u-\frac{V}{8}u^2+O(u^3).
\]

So the whole mixed-parity anchored sector collapses, to second order, to the six scalar moments
`(E,O,X,Y,U,V)`.

## 3. Universal formulas for `\lambda_1` and `\lambda_2`

Let `R:=E^2+O^2`. Rotating the leading oscillatory phase so that the tangent germ has vanishing
constant term, the standard Prüfer computation gives:

### Theorem 3.1

For the mixed-parity anchored profile above,
\[
\lambda_1(F)
=
-\frac{EY+OX}{2R},
\]
and
\[
\lambda_2(F)
=
\frac{OU-EV}{8R}
+\frac{(EX-OY)(EY+OX)}{4R^2}.
\]

Equivalently, if
\[
q:=8\lambda_1(F)>0,
\]
then the second-order anchored compatibility equation `\lambda_2(F)=0` is exactly
\[
2(OU-EV)=q(EX-OY).
\]

So at second order the anchored fiber is governed by one affine relation among the first three
mixed-parity moment blocks.

### Proof

Write
\[
A(u)=A_0+A_1u+A_2u^2+O(u^3),
\qquad
B(u)=B_0+B_1u+B_2u^2+O(u^3),
\]
with
\[
A_0=E,\quad A_1=\frac X2,\quad A_2=-\frac U8,
\qquad
B_0=O,\quad B_1=-\frac Y2,\quad B_2=-\frac V8.
\]

Let `r:=\sqrt{A_0^2+B_0^2}` and rotate the leading oscillatory profile into the form
`r\cos(\xi-\phi)`. In the rotated frame, the zero equation near the positive oscillatory root is
\[
-C(u)\sin s(u)+S(u)\cos s(u)=0,
\]
where
\[
C(u)=r+c_1u+c_2u^2+O(u^3),
\qquad
S(u)=s_1u+s_2u^2+O(u^3),
\]
with
\[
s_1=\frac{A_0B_1-B_0A_1}{r},
\qquad
s_2=\frac{A_0B_2-B_0A_2}{r},
\]
\[
c_1=\frac{A_0A_1+B_0B_1}{r}.
\]

Writing
\[
s(u)=\lambda_1u+\lambda_2u^2+O(u^3)
\]
and comparing coefficients in
\[
-C(u)\sin s(u)+S(u)\cos s(u)=0
\]
gives
\[
\lambda_1=\frac{s_1}{r},
\qquad
\lambda_2=\frac{s_2-c_1\lambda_1}{r}.
\]
Substituting the expressions for `A_i,B_i` yields the formulas above.

## 4. A complex-moment reformulation

The previous theorem has a cleaner complex form.

Define
\[
z_0:=E+iO,
\qquad
z_1:=-Y-iX,
\qquad
z_2:=-V+iU.
\]
Then
\[
|z_0|^2=R,
\]
and
\[
\Re(\overline{z_0}z_1)=-(EY+OX),
\qquad
\Im(\overline{z_0}z_1)=OY-EX,
\]
\[
\Re(\overline{z_0}z_2)=OU-EV.
\]

So Theorem 3.1 becomes:

### Corollary 4.1

\[
\lambda_1(F)=\frac{\Re(\overline{z_0}z_1)}{2|z_0|^2},
\]
\[
\lambda_2(F)
=
\frac{\Re(\overline{z_0}z_2)}{8|z_0|^2}
+\frac{\Re(\overline{z_0}z_1)\Im(\overline{z_0}z_1)}{4|z_0|^4}.
\]

Equivalently, along the anchor fiber `q=8\lambda_1(F)>0`,
\[
2\Re(\overline{z_0}z_2)+q\,\Im(\overline{z_0}z_1)=0.
\]

This is the real reason the low-order anchored geometry keeps collapsing: the second-order fiber
condition depends only on three complex moments `z_0,z_1,z_2`, not on the full support pattern.

## 5. Why the old sector theorems follow from this

This theorem strictly contains the old support-three second-order formulas.

### Even-odd support-three

If there is exactly one even mode `m` and one odd mode `n`, then
\[
E=1+b,\quad O=c,\quad X=(n^2-1)c,\quad Y=m^2b,
\]
\[
U=m^2(m^2-4)b,\quad V=(n^2-1)^2c,
\]
and Theorem 3.1 specializes exactly to the formulas in
[RESEARCH_evenodd_second_order_normal_form.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_evenodd_second_order_normal_form.md).

### Odd-odd support-three

If there are no secondary even modes, then
\[
E=1,\qquad Y=U=0,
\]
so
\[
\lambda_1(F)=-\frac{OX}{2(1+O^2)},
\]
\[
\lambda_2(F)
=
-\frac{V}{8(1+O^2)}
+\frac{EX\cdot OX}{4(1+O^2)^2},
\]
which, after rewriting `O,X,V` in the two-mode coordinates, is exactly the odd-odd formula from
[RESEARCH_oddodd_second_order_projective_rigidity.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_oddodd_second_order_projective_rigidity.md).

So the old sector theorems are not isolated eliminations; they are shadows of one common
moment-normal-form theorem.

## 6. Research meaning

This changes the scale of the problem.

The real low-order object is no longer “a support-three family”. It is the mixed-parity moment
jet
\[
(z_0,z_1,z_2).
\]

Consequently:

1. support size is invisible at second order beyond these aggregate moments;
2. the anchored mixed-parity fiber is a low-dimensional moment-constraint problem, not a
   support-by-support problem;
3. higher-support rigidity should be attacked by studying the higher moment jets
   `z_3,z_4,\dots`, not by computing more families one at a time.

So the next genuinely structural target is:

> determine whether the higher normalized Prüfer invariants are fiber-rigid once the second-order
> moment identity
> \[
> 2(OU-EV)=q(EX-OY)
> \]
> has been imposed.

That is the right support-`≥4` frontier.
