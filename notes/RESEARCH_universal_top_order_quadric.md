# A Universal Top-Order Quadric Relation for Realized Normalized Pairs

## Goal

The exact small-window calculations revealed two phenomena:

- the normalized-pair images of `(1,1)` and `(2,1)` are both cut out by a single quadratic
  relation involving only the top two coefficient levels;
- multiplication by a degree-`1` multiplier `1+tu` transports the `(1,1)` relation into the
  `(2,1)` relation automatically.

This note explains both phenomena at once. The key point is that there is a **universal
top-order quadric relation** satisfied by every realized normalized pair on every bounded
window, and it is covariant under multiplication by `1+tu`.

So the circle on `(1,1)` and the saturation on `(2,1)` are not isolated accidents. They are the
first visible manifestations of a universal highest-order phase constraint.

## 1. Top coefficients of a realized normalized pair

Let `(K,L)` be a bounded bandwidth window, and let
\[
F(t)=A(u)J_0(t)+B(u)J_1(t),\qquad u=t^{-1},
\]
be a realized profile. Write
\[
x:=A(0),\qquad y:=B(0),\qquad D:=x^2+y^2,
\]
and define the normalized phase pair
\[
C(u)+iS(u):=\frac{A(u)+iB(u)}{x+iy}.
\]
Thus
\[
C(u)=\frac{xA(u)+yB(u)}{D},
\qquad
S(u)=\frac{xB(u)-yA(u)}{D}.
\]

Let
\[
d:=\deg B.
\]
On any bounded even/odd window, the top degree in the normalized pair is always inherited from
the `J_1`-channel, so
\[
\deg C,\deg S\le d.
\]
Write the top of `A` and `B` as
\[
A(u)=a\,u^{d-1}+\cdots,
\qquad
B(u)=b\,u^d+b'\,u^{d-1}+\cdots.
\]
Then
\[
c_d=\frac{yb}{D},
\qquad
s_d=\frac{xb}{D},
\]
and
\[
c_{d-1}=\frac{xa+yb'}{D},
\qquad
s_{d-1}=\frac{xb'-ya}{D},
\]
where
\[
C(u)=\sum_{j=0}^{d} c_j u^j,
\qquad
S(u)=\sum_{j=1}^{d} s_j u^j.
\]

## 2. The universal raw top-coefficient identity

The key observation is that in the parity-adapted normalized Lommel basis, the highest `A` and
`B` coefficients of every active top mode satisfy the same relation
\[
2a+b=0.
\]

This is immediate in the first few modes:
\[
\widetilde J_2=J_0-2uJ_1,
\qquad
\widetilde J_3=4uJ_0+(1-8u^2)J_1,
\qquad
\widetilde J_4=(1-32u^2)J_0+(64u^3-10u)J_1,
\]
and in general follows from the exact highest-term recurrence for the Lommel coefficients.

## 3. The universal top-order quadric

### Theorem 3.1

Every realized normalized phase pair on every bounded bandwidth window satisfies
\[
2(c_{d-1}s_d-s_{d-1}c_d)+c_d^2+s_d^2=0,
\]
where `d=\deg B` is the top `J_1`-degree of the underlying realized profile.

### Proof

Using the formulas above,
\[
c_{d-1}s_d-s_{d-1}c_d
=
\frac{ab}{D},
\]
and
\[
c_d^2+s_d^2
=
\frac{b^2}{D}.
\]
Therefore
\[
2(c_{d-1}s_d-s_{d-1}c_d)+c_d^2+s_d^2
=
\frac{2ab+b^2}{D}.
\]
Since `2a+b=0`, the right-hand side vanishes.

So the top two levels of every realized normalized pair satisfy the same quadratic relation.

## 4. Covariance under degree-1 multipliers

Now let
\[
\widetilde C(u)=(1+tu)C(u),
\qquad
\widetilde S(u)=(1+tu)S(u),
\qquad
t\in\R.
\]
Write the old top relation as
\[
Q_d(C,S):=2(c_{d-1}s_d-s_{d-1}c_d)+c_d^2+s_d^2.
\]
Then the new top coefficients satisfy
\[
\widetilde c_{d+1}=t c_d,
\qquad
\widetilde s_{d+1}=t s_d,
\]
\[
\widetilde c_d=c_d+t c_{d-1},
\qquad
\widetilde s_d=s_d+t s_{d-1}.
\]

### Proposition 4.1

The universal top quadric is covariant under multiplication by `1+tu`:
\[
Q_{d+1}(\widetilde C,\widetilde S)=t^2 Q_d(C,S).
\]

### Proof

Substituting the transformed coefficients gives
\[
\begin{aligned}
Q_{d+1}(\widetilde C,\widetilde S)
&=
2(\widetilde c_d\widetilde s_{d+1}-\widetilde s_d\widetilde c_{d+1})
+\widetilde c_{d+1}^2+\widetilde s_{d+1}^2\\
&=
t^2\bigl(2(c_{d-1}s_d-s_{d-1}c_d)+c_d^2+s_d^2\bigr).
\end{aligned}
\]

## 5. Why `(1,1)` gives a circle and `(2,1)` gives saturation

This universal law explains the two previous exact computations.

### Corollary 5.1

On the window `(1,1)`, the universal top-order quadric is already the full realized
normalized-pair image. Hence the degree-`1` ambiguity locus from `(1,0)` is cut out by a
single conic, namely the circle
\[
p^2+(q+1)^2=1.
\]

### Corollary 5.2

On the window `(2,1)`, the universal top-order quadric is again already the full realized
normalized-pair image. Hence every reduced pair realized in `(1,1)` automatically admits a
degree-`1` lift into `(2,1)`.

### Explanation

The first statement comes from combining the `(1,1)` image equation with the multiplier ansatz
from `(1,0)`. The second comes from the covariance identity
\[
Q_{d+1}((1+tu)C,(1+tu)S)=t^2Q_d(C,S),
\]
since every reduced pair from `(1,1)` already satisfies `Q_d=0`.

So the first reduced-side circle and the first reduced-side saturation are governed by the same
universal top-order law.

## 6. Research meaning

This changes the interpretation of the bounded-bandwidth small-window calculations.

The conic on `(1,1)` and the saturation on `(2,1)` are not separate phenomena. They are the
first two shadows of a single top-order quadric that exists on every bounded window.

So the next frontier is no longer:

- compute another small window by brute force.

It is:

- determine for which windows the universal top-order quadric already cuts out the full
  realized normalized-pair image;
- determine when extra lower-order equations appear beyond this universal first obstruction.

That is a much more structural, and potentially classifiable, problem.
