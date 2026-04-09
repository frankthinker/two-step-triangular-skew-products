# Third-Order Complex-Moment Jets for the Anchored Mixed-Parity Fiber

## Goal

The second-order moment normal form shows that the anchored mixed-parity sector does not depend,
to order `2`, on the full support pattern. It depends only on the aggregated moments
\[
(E,O,X,Y,U,V),
\]
or equivalently on three complex moments
\[
z_0,\ z_1,\ z_2.
\]

The natural next question is whether the third normalized Prüfer invariant still sees only a
finite collection of aggregate moments. The answer is yes.

This note records that third-order jet.

## 1. The next aggregated moments

Keep the notation of
[RESEARCH_mixed_parity_second_order_moment_normal_form.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_mixed_parity_second_order_moment_normal_form.md).

The exact low-order mode expansions show that the first new coefficients at order `u^3` come
from:

- the `J_1` channel of even modes;
- the `J_0` channel of odd modes.

Define the corresponding third moments
\[
T:=\sum_{m\in\mathcal E} m^2(m^2-4)^2 b_m,
\]
\[
W:=\sum_{n\in\mathcal O} (n^2-9)(n^2-1)^2 c_n.
\]

Then the mixed-parity anchored profile satisfies
\[
A(u)=E+\frac{X}{2}u-\frac{U}{8}u^2-\frac{W}{48}u^3+O(u^4),
\]
\[
B(u)=O-\frac{Y}{2}u-\frac{V}{8}u^2+\frac{T}{48}u^3+O(u^4).
\]

So the third jet introduces exactly two new aggregate moments and no others.

## 2. Four complex moments

Retain the three complex moments from the second-order note:
\[
z_0:=E+iO,
\qquad
z_1:=-Y-iX,
\qquad
z_2:=-V+iU.
\]

Introduce the new third-order complex moment
\[
z_3:=T+iW.
\]

Then
\[
|z_0|^2=E^2+O^2=:R,
\]
\[
\Re(\overline{z_0}z_1)=-(EY+OX),
\qquad
\Im(\overline{z_0}z_1)=OY-EX,
\]
\[
\Re(\overline{z_0}z_2)=OU-EV,
\qquad
\Im(\overline{z_0}z_2)=EU+OV,
\]
\[
\Re(\overline{z_0}z_3)=ET+OW.
\]

Thus the full third-order jet is governed by four complex moments
\[
z_0,z_1,z_2,z_3.
\]

## 3. Generic rotated-frame formula

Let
\[
C(u)=r+c_1u+c_2u^2+O(u^3),
\qquad
S(u)=s_1u+s_2u^2+s_3u^3+O(u^4),
\]
be the rotated oscillatory coefficients in the usual Prüfer frame, so the zero equation is
\[
-C(u)\sin s(u)+S(u)\cos s(u)=0,
\]
with
\[
s(u)=\lambda_1u+\lambda_2u^2+\lambda_3u^3+O(u^4).
\]

A direct coefficient comparison gives the universal identity
\[
\lambda_3=
\frac{c_1^2s_1-c_1rs_2-c_2rs_1+r^2s_3-\frac13 s_1^3}{r^3}.
\]

This formula is completely general; it is not special to Bessel profiles.

## 4. Third-order mixed-parity moment formula

Substituting the mixed-parity coefficients into the generic rotated-frame identity yields the
first real higher-order theorem of the program.

### Theorem 4.1

For an anchored mixed-parity profile,
\[
\lambda_1(F)=\frac{\Re(\overline{z_0}z_1)}{2|z_0|^2},
\]
\[
\lambda_2(F)
=
\frac{\Re(\overline{z_0}z_2)}{8|z_0|^2}
+\frac{\Re(\overline{z_0}z_1)\Im(\overline{z_0}z_1)}{4|z_0|^4},
\]
and
\[
\lambda_3(F)
=
\frac{
|z_0|^4\Re(\overline{z_0}z_3)
+6|z_0|^2\Im(\overline{z_0}z_1)\Im(\overline{z_0}z_2)
+3|z_0|^2\Im(\overline{z_0}z_1)\Re(\overline{z_0}z_2)
-4\Im(\overline{z_0}z_1)^3
}
{48|z_0|^6}.
\]

Equivalently, writing
\[
a:=\Re(\overline{z_0}z_1),\quad
b:=\Im(\overline{z_0}z_1),\quad
c:=\Re(\overline{z_0}z_2),\quad
e:=\Im(\overline{z_0}z_2),\quad
d:=\Re(\overline{z_0}z_3),
\]
one has
\[
\lambda_1=\frac{a}{2R},
\qquad
\lambda_2=\frac{c}{8R}+\frac{ab}{4R^2},
\]
\[
\lambda_3=\frac{R^2d+3Rbc+6Rbe-4b^3}{48R^3}.
\]

### Proof

From the mixed-parity coefficient expansions one has
\[
A_0=E,\quad A_1=\frac X2,\quad A_2=-\frac U8,\quad A_3=-\frac W{48},
\]
\[
B_0=O,\quad B_1=-\frac Y2,\quad B_2=-\frac V8,\quad B_3=\frac T{48}.
\]

In the rotated frame,
\[
r=\sqrt{A_0^2+B_0^2},
\qquad
s_1=\frac{A_0B_1-B_0A_1}{r},
\qquad
s_2=\frac{A_0B_2-B_0A_2}{r},
\]
\[
s_3=\frac{A_0B_3-B_0A_3}{r},
\qquad
c_1=\frac{A_0A_1+B_0B_1}{r},
\qquad
c_2=\frac{A_0A_2+B_0B_2}{r}.
\]

Using the definitions of `z_0,z_1,z_2,z_3`, these become
\[
r^2=|z_0|^2=R,
\qquad
s_1=\frac{\Re(\overline{z_0}z_1)}{2r},
\qquad
s_2=\frac{\Re(\overline{z_0}z_2)}{8r},
\]
\[
s_3=\frac{\Re(\overline{z_0}z_3)}{48r},
\qquad
c_1=-\frac{\Im(\overline{z_0}z_1)}{2r},
\qquad
c_2=-\frac{\Im(\overline{z_0}z_2)}{8r}.
\]

Substituting these identities into the generic formula of Section 3 and simplifying gives the
displayed expressions.

## 5. Meaning

This is the first real higher-order unification beyond support-three sector theorems.

At third order, the anchored mixed-parity fiber still does not see the full support. It sees
only
\[
z_0,\ z_1,\ z_2,\ z_3.
\]

So the correct frontier is not “classify all support-four families”. The correct frontier is:

> determine whether the higher normalized Prüfer invariants are rigid once the finite complex
> jet
> \[
> (z_0,z_1,z_2,z_3)
> \]
> has been fixed.

This is already much closer to a genuine moduli theorem than to a list of elimination lemmas.

## 6. Research meaning

Combined with the previous moment-normal-form note, the picture is now:

1. second order depends only on `z_0,z_1,z_2`;
2. third order depends only on `z_0,z_1,z_2,z_3`;
3. support size remains invisible up to third order beyond these aggregated jets.

So the support-`≥4` frontier has been compressed to a finite-jet fiber-rigidity problem.

That is the deepest structural reduction reached so far.
