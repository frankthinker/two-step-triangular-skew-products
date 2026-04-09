# Large-Even Positivity in the Anchored Even-Even Support-Three Sector

## Goal

The previous notes reduced the anchored even-even support-three sector to the fifth-order
residual equation
\[
\mathcal P_{M,N}(q)=0,
\qquad
M=m^2,\ N=n^2,
\]
for distinct even integers `m,n`. The purpose of this note is to prove a genuine large-scale
theorem:

> if `M,N` are distinct even squares with `\min(M,N)\ge 36`, then
> \[
> \mathcal P_{M,N}(q)>0\qquad (q>0).
> \]

Equivalently, the entire large-even interior of the anchored even-even support-three sector is
already excluded at fifth order.

## 1. The polynomial in even-square coordinates

Write
\[
M=4x^2,
\qquad
N=4y^2,
\qquad
3\le x<y.
\]

Then the residual polynomial becomes
\[
\mathcal P_{x,y}(q)=q^5+a_4(x,y)q^4+a_3(x,y)q^3+a_2(x,y)q^2+a_1(x,y)q+a_0(x,y),
\]
where
\[
a_0(x,y)=131072(x-1)^2(x+1)^2(y-1)^2(y+1)^2(x^2+y^2-8)>0.
\]

The derivative is
\[
\mathcal P'_{x,y}(q)=5q^4+4a_4(x,y)q^3+3a_3(x,y)q^2+2a_2(x,y)q+a_1(x,y).
\]

Our task is therefore to prove
\[
\mathcal P'_{x,y}(q)>0\qquad (q\ge 0),
\]
because then `\mathcal P_{x,y}` is strictly increasing on `[0,\infty)` and starts from a
positive value.

## 2. Difference coordinates

Set
\[
a:=x^2,
\qquad
d:=y^2-x^2>0.
\]

Then the three lower coefficients of `\mathcal P'_{x,y}` become
\[
Q_2(a,d)=20a^2+20ad-264a+4d^2-132d-225,
\]
\[
Q_1(a,d)=76a^3-787a^2+1342a+4d^3+(46a-149)d^2+(114a^2-787a+671)d,
\]
\[
Q_0(a,d)=28a^4-172a^3+504a^2-450a
+(6a-25)d^3+(34a^2-136a+150)d^2+(56a^3-258a^2+504a-225)d.
\]

So
\[
\mathcal P'_{x,y}(q)
=
5q^4+(128x^2+128y^2-516)q^3+Q_2(a,d)q^2+Q_1(a,d)q+Q_0(a,d).
\]

Because `y\ge x+1`, one has
\[
d=y^2-x^2\ge (x+1)^2-x^2=2x+1.
\]

## 3. Monotonicity in the gap

For fixed `x`, the coefficients are increasing in `d`.

Indeed,
\[
\partial_d Q_2(a,d)=4(5a+2d-33),
\]
\[
\partial_d Q_1(a,d)=12d^2+2(46a-149)d+(114a^2-787a+671),
\]
\[
\partial_d Q_0(a,d)=3(6a-25)d^2+2(34a^2-136a+150)d+(56a^3-258a^2+504a-225).
\]

For `a=x^2\ge 9` and `d\ge 2x+1`, these are all positive:

- for `Q_2`,
  \[
  5a+2d-33\ge 5x^2+4x-31>0 \qquad (x\ge 3);
  \]
- for `Q_1`, the right-hand side is a quadratic in `d` with positive leading term, so it is
  enough to evaluate it at `d=2x+1`, where it becomes
  \[
  114x^4+184x^3-647x^2-548x+385>0 \qquad (x\ge 3);
  \]
- for `Q_0`, similarly it is enough to evaluate at `d=2x+1`, where it becomes
  \[
  2x\bigl(28x^5+68x^4-59x^3-236x^2-25x+150\bigr)>0
  \qquad (x\ge 3).
  \]

Therefore, for fixed `x\ge 3`, each of `Q_2,Q_1,Q_0` is increasing in `d` on the admissible
region.

So the derivative polynomial is coefficientwise minimized by the adjacent pair
\[
y=x+1.
\]

## 4. The consecutive-pair reduction

Set
\[
\Pi_x(q):=\mathcal P'_{x,x+1}(q).
\]

Then
\[
\Pi_x(q)
=
5q^4+(128x^2+128x+48)q^3
+(20x^4+40x^3-228x^2-248x-353)q^2
\]
\[
\qquad
+(76x^6+228x^5-489x^4-1358x^3+53x^2+770x+526)q
+4(7x^8+28x^7+5x^6-83x^5-48x^4+75x^3+56x^2-25).
\]

By the monotonicity above,
\[
\mathcal P'_{x,y}(q)\ge \Pi_x(q)
\qquad (y\ge x+1,\ q\ge 0),
\]
coefficientwise.

Hence it is enough to prove
\[
\Pi_x(q)>0
\qquad (x\ge 3,\ q\ge 0).
\]

## 5. The large-even interior theorem

### Proposition 5.1

For every `x\ge 4`, all coefficients of `\Pi_x(q)` are positive. Consequently
\[
\Pi_x(q)>0
\qquad (q\ge 0).
\]

#### Proof

The coefficient of `q^4` is `5`, and the coefficient of `q^3` is clearly positive.

For the remaining coefficients, use the explicit formulas above.

For the `q^2` coefficient,
\[
20x^4+40x^3-228x^2-248x-353>0
\qquad (x\ge 4),
\]
since its derivative
\[
8(2x+1)(5x^2+5x-31)
\]
is positive for `x\ge 4`, and the value at `x=4` is `2687`.

For the `q` coefficient,
\[
76x^6+228x^5-489x^4-1358x^3+53x^2+770x+526>0
\qquad (x\ge 4),
\]
because its derivative
\[
2(2x+1)(114x^4+228x^3-603x^2-717x+385)
\]
is positive for `x\ge 4`, and the value at `x=4` is `337126`.

For the constant coefficient,
\[
4(7x^8+28x^7+5x^6-83x^5-48x^4+75x^3+56x^2-25)>0
\qquad (x\ge 4),
\]
because its derivative
\[
4x(x+1)(2x+1)(28x^4+56x^3-83x^2-111x+112)
\]
is positive for `x\ge 4`, and the value at `x=4` is `3385500`.

So every coefficient is positive, and hence `\Pi_x(q)>0` for every `q\ge 0`. ∎

### Proposition 5.2

For `x=3`,
\[
\Pi_3(q)=5q^4+1584q^3-449q^2+37846q+357020
\]
has no positive real root. Hence
\[
\Pi_3(q)>0
\qquad (q\ge 0).
\]

#### Proof

A direct Sturm count gives
\[
\#\{q>0:\Pi_3(q)=0\}=0.
\]
Since `\Pi_3(0)=357020>0`, the polynomial is positive on `[0,\infty)`. ∎

### Theorem 5.3 (Large-Even Interior Positivity)

Let `M=4x^2`, `N=4y^2` be distinct even squares with
\[
\min(M,N)\ge 36,
\]
equivalently `3\le x<y`. Then
\[
\mathcal P'_{M,N}(q)>0
\qquad (q\ge 0).
\]
Therefore
\[
\mathcal P_{M,N}(q)>0
\qquad (q>0).
\]

#### Proof

Fix `x\ge 3` and `y\ge x+1`. By Section 3, the coefficients of `\mathcal P'_{x,y}` are
increasing in `d=y^2-x^2`, hence
\[
\mathcal P'_{x,y}(q)\ge \Pi_x(q)
\qquad (q\ge 0).
\]

If `x\ge 4`, Proposition 5.1 gives `\Pi_x(q)>0`.

If `x=3`, Proposition 5.2 gives `\Pi_3(q)>0`.

So in all cases `\mathcal P'_{x,y}(q)>0` for `q\ge 0`.

Since
\[
\mathcal P_{M,N}(0)=131072(x-1)^2(x+1)^2(y-1)^2(y+1)^2(x^2+y^2-8)>0,
\]
the polynomial `\mathcal P_{M,N}` is strictly increasing from a positive initial value, hence
stays positive for every `q>0`. ∎

## 6. Interpretation

This is the first genuinely global theorem for the remaining anchored support-three frontier.

It says that the even-even sector does not remain wild after the third-order candidate reduction.
Once both even modes are beyond the lowest boundary layer, the fifth-order residual is
monotone and strictly positive. So there is no anchored common infinite-resonance configuration
in the large-even interior.

The only remaining even-even frontier is therefore a boundary regime involving the lowest even
mode
\[
M=16
\qquad\text{or}\qquad
N=16,
\]
where the residual polynomial may acquire positive roots.

In other words, anchored support-three geometry now separates cleanly into:

- even-odd: excluded at second order;
- odd-odd: excluded at second order;
- even-even large interior: excluded at fifth order by global positivity;
- even-even boundary layer at the lowest even mode: the only remaining support-three frontier.
