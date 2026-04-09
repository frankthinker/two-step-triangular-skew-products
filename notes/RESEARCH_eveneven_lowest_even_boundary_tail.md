# The Stable Tail of the Lowest-Even Boundary Layer

## Goal

The large-even interior theorem leaves one support-three boundary layer unresolved:
\[
M=16
\qquad\text{or}\qquad
N=16.
\]

This note shows that even this boundary layer stabilizes after finitely many odd square modes.
More precisely:

> in the anchored even-even support-three sector with one even mode equal to `2`, the only
> remaining fifth-order candidates occur for the next two even modes `6` and `8`; the entire
> tail `n\ge 10` is already excluded at fifth order.

By symmetry it is enough to treat
\[
M=16,
\qquad
N=4y^2,
\qquad
y\ge 3.
\]

## 1. The boundary polynomial

Substituting `M=16`, `N=4y^2` into the fifth-order residual gives
\[
\mathcal P_{16,4y^2}(q)
=
q^5+4(8y^2-109)q^4+80(4y^4-84y^2-689)q^3
\]
\[
\qquad
+256(4y^6-59y^4-384y^2+1219)q^2
-4096(y^2-1)^2(7y^2-118)q
\]
\[
\qquad
+1179648(y-2)(y-1)^2(y+1)^2(y+2).
\]

Numerically, this polynomial has positive roots for `y=3,4`, and no positive roots for
`y\ge 5`. The point of this note is to prove the latter statement uniformly.

## 2. Boundary scaling

Set
\[
r:=y^2-9\ge 0,
\qquad
q=(r+8)z.
\]

Then, after dividing by `(r+8)^2`, the residual becomes
\[
G_r(z)
=(r+8)^3z^5+4(8r-37)(r+8)^2z^4+80(4r^2-12r-1121)(r+8)z^3
\]
\[
\qquad
+256(4r^3+49r^2-474r-4100)z^2-4096(r+8)(7r-55)z
+1179648(r+5).
\]

Thus
\[
\mathcal P_{16,4y^2}(q)=0
\quad\Longleftrightarrow\quad
G_r(z)=0,
\qquad
r=y^2-9,\ z=\frac{q}{r+8}.
\]

The advantage is that the parameter `r` now measures distance from the first nontrivial
boundary point `y=3`, and the threshold `y=5` is exactly
\[
r\ge 16.
\]

## 3. Two positive quadratic blocks

Write
\[
G_r(z)=a_5z^5+a_4z^4+a_3z^3+a_2z^2-bz+c,
\]
with
\[
a_5=(r+8)^3,
\qquad
a_4=4(8r-37)(r+8)^2,
\qquad
a_3=80(4r^2-12r-1121)(r+8),
\]
\[
a_2=256(4r^3+49r^2-474r-4100),
\qquad
b=4096(r+8)(7r-55),
\qquad
c=1179648(r+5).
\]

Two natural quadratic blocks appear.

### Lemma 3.1

If `r\ge 16`, then
\[
a_2z^2-bz+c>0
\qquad (z>0).
\]

#### Proof

The discriminant is
\[
b^2-4a_2c
=
-\frac{16777216\,(288r^4+4919r^3-16110r^2-462705r-1500200)}{r+8}.
\]
Writing `r=s+16` gives
\[
288s^4+23351s^3+662370s^2+7518159s+25994952>0,
\qquad
s\ge 0.
\]
So `4a_2c-b^2>0`, and the quadratic is positive for every real `z`. ∎

### Lemma 3.2

If `r\ge 16`, then
\[
a_4z^2+a_3z+a_2>0
\qquad (z>0).
\]

#### Proof

Its discriminant is
\[
a_3^2-4a_4a_2
=
-256(r+8)^2\bigl(112r^4+6304r^3+130920r^2-916792r-28988825\bigr).
\]
Again writing `r=s+16`,
\[
112s^4+13472s^3+605544s^2+9949128s+23019239>0
\qquad (s\ge 0),
\]
so the discriminant is negative. Since `a_4>0` and `a_2>0` for `r\ge 16`, the quadratic is
strictly positive. ∎

## 4. The stable tail

### Theorem 4.1

For every `y\ge 5`,
\[
\mathcal P_{16,4y^2}(q)>0
\qquad (q>0).
\]

Equivalently, in the anchored even-even support-three sector with one mode equal to `2`, the
entire tail
\[
n\ge 10
\]
is already excluded at fifth order.

#### Proof

Let `r=y^2-9`. Then `y\ge 5` means `r\ge 16`, and it is enough to prove
\[
G_r(z)>0
\qquad (z>0).
\]

If `r\ge 19`, then
\[
a_3=80(4r^2-12r-1121)(r+8)>0.
\]
Hence
\[
z^3(a_5z^2+a_4z+a_3)>0
\qquad (z>0),
\]
and by Lemma 3.1,
\[
a_2z^2-bz+c>0.
\]
Therefore
\[
G_r(z)=z^3(a_5z^2+a_4z+a_3)+(a_2z^2-bz+c)>0.
\]

It remains to treat `r=16,17,18`, corresponding to `y=5,6,7`. In these cases
the polynomials are explicitly
\[
G_{16}(z)=384(36z^5+546z^4-1445z^3+11496z^2-608z+2688),
\]
\[
G_{17}(z)=\frac{1}{25}
\bigl(390625z^5+6187500z^4-8450000z^3+138592000z^2-6553600z+25952256\bigr),
\]
\[
G_{18}(z)=\frac{8}{13}
\bigl(28561z^5+470158z^4-138580z^3+11053952z^2-472576z+1695744\bigr).
\]
A direct Sturm count shows that each of these quintics has no positive real root. Since all
three have positive constant term, they are positive on `(0,\infty)`.

Thus `G_r(z)>0` for every `r\ge 16`, and therefore
\[
\mathcal P_{16,4y^2}(q)>0
\qquad (q>0,\ y\ge 5).
\]
∎

## 5. Interpretation

The large-even theorem from the previous note excluded the whole interior
\[
\min(M,N)\ge 36.
\]
The present note shows that the lowest-even boundary layer is also mostly rigid:

- positive roots occur only at `y=3,4`, i.e. `N=36,64`;
- from `y\ge 5`, the boundary layer stabilizes and is again excluded.

So the anchored even-even support-three frontier is now reduced to two isolated boundary rungs:
\[
(M,N)=(16,36),
\qquad
(16,64),
\]
up to symmetry.

This is a much sharper picture than “the lowest even mode is still open”: the boundary layer
does not stay wild indefinitely; it collapses after two exceptional cases.
