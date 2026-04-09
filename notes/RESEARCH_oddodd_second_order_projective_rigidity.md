# Second-Order Projective Rigidity of the Anchored Odd-Odd Support-Three Sector

## Goal

The anchored odd ladder
\[
J_0+bJ_1+cJ_{2r+1}
\]
was previously closed by a higher-order elimination argument. This note shows that the real
mechanism is much more rigid:

> the whole anchored odd-odd support-three sector is already excluded at second order.

In particular, the odd ladder is not an isolated family. It is one slice of a general local
projective-rigidity theorem.

## 1. Setup

Let `m,n` be odd positive integers, and normalize signs by
\[
\widetilde J_m:=(-1)^{(m-1)/2}J_m,
\qquad
\widetilde J_n:=(-1)^{(n-1)/2}J_n.
\]

Consider
\[
F(t)=J_0(t)+b\widetilde J_m(t)+c\widetilde J_n(t),
\]
and write
\[
M:=m^2,
\qquad
N:=n^2.
\]

For odd normalized modes, the `(J_0,J_1)` expansion begins as
\[
\widetilde J_\ell(t)
=
\Bigl(\frac{\ell^2-1}{2}u+O(u^3)\Bigr)J_0(t)
\;+\;
\Bigl(1-\frac{(\ell^2-1)^2}{8}u^2+O(u^4)\Bigr)J_1(t),
\qquad
u=t^{-1}.
\]

Hence
\[
F(t)=A(u)J_0(t)+B(u)J_1(t),
\]
with
\[
A(u)=1+\frac{(M-1)b+(N-1)c}{2}u+O(u^3),
\]
\[
B(u)=(b+c)-\frac{(M-1)^2b+(N-1)^2c}{8}u^2+O(u^4).
\]

The key point is that the odd-odd sector has no free even perturbation in the `J_0` channel and
no free odd perturbation in the `J_1` channel. This makes the second-order Pr\"ufer geometry
collapse.

## 2. A universal second-order normal form

Introduce the linear coordinates
\[
u:=b+c,
\qquad
d:=(M-1)b+(N-1)c.
\]

Then solving for `(b,c)` gives
\[
b=\frac{d-(N-1)u}{M-N},
\qquad
c=\frac{(M-1)u-d}{M-N},
\]
as long as `m\neq n`. The degenerate case `m=n` is support-two and is irrelevant here.

In these coordinates, the first two zero-shift coefficients simplify drastically.

### Proposition

For the odd-odd support-three profile above one has
\[
\lambda_1(F)
=
-\frac{du}{2(1+u^2)},
\]
and
\[
\lambda_2(F)
=
\frac{2ud^2-(M+N-2)(1+u^2)d+(M-1)(N-1)u(1+u^2)}
{8(1+u^2)^2}.
\]

### Proof

Rotate the leading phase so that the tangent series has vanishing constant term. Applying the
standard first two Pr\"ufer coefficient formulas to the expansions of `A(u),B(u)` above gives
explicit rational formulas in `(b,c)`. Rewriting them in the coordinates `(u,d)` yields the two
displayed identities.

## 3. Imposing the anchor normalization

In any common anchored infinite-resonance configuration, the normalized first shift coefficient
must satisfy
\[
q:=8\lambda_1(F)>0.
\]

Using the formula for `\lambda_1(F)`, this is equivalent to
\[
d=-\frac{q(1+u^2)}{4u}.
\]

Substituting this into the numerator of `\lambda_2(F)` gives an exact one-variable reduction:
\[
8(1+u^2)\lambda_2(F)
=
\frac{\bigl(q^2+2(M+N-2)q+8(M-1)(N-1)\bigr)u^2+q\bigl(q+2(M+N-2)\bigr)}
{8u}.
\]

Since `q>0`, `M\ge 1`, and `N\ge 1`, every coefficient in the numerator is nonnegative, and in
fact strictly positive in the genuinely odd-odd sector.

Therefore the equation `\lambda_2(F)=0` forces
\[
u^2
=
-\frac{q\bigl(q+2(M+N-2)\bigr)}
{q^2+2(M+N-2)q+8(M-1)(N-1)}
<0,
\]
which is impossible over the reals.

## 4. Main theorem

### Theorem

Assume that one active positive vertical frequency carries the pure vertical anchor profile
`J_0`. Let a second active positive vertical frequency carry a profile of the form
\[
F(t)=aJ_0(t)+bJ_m(t)+cJ_n(t),
\qquad
a\neq 0,
\qquad
m,n\ \text{odd}.
\]
Then the genuinely support-three odd-odd branch is impossible. Equivalently, if `m\neq n` and
the two active frequencies belong to a common infinite-resonance configuration, then
\[
bc=0.
\]

In particular, the entire anchored odd-odd support-three sector is disjoint from the `J_0`
fiber of the normalized Pr\"ufer map already at second order.

### Proof

By scaling, assume `a=1`, and normalize signs as above. If `m=n`, the profile is support-two.
Assume therefore `m\neq n`.

Suppose `bc\neq 0`. Then `u=b+c` and `d=(M-1)b+(N-1)c` are well defined, and the profile lies in
the genuinely support-three odd-odd sector. The anchored compatibility conditions impose
\[
q:=8\lambda_1(F)>0,
\qquad
\lambda_2(F)=0.
\]
By the computation above, these two relations force `u^2<0`, impossible over the reals.

Hence `bc=0`. So no genuinely support-three odd-odd profile can lie in the anchored fiber.

## 5. Consequences

This theorem strictly strengthens all previously proved anchored odd-ladder closures.

It shows that:

1. the odd ladder `J_0+bJ_1+cJ_{2r+1}` is only one slice of a larger second-order rigidity
   phenomenon;
2. the odd-odd anchored sector does not require higher-order elimination at all;
3. the real local fiber-rigidity problem near `J_0` is now pushed beyond both the even-odd and
   the odd-odd support-three sectors.

So the first genuinely open anchored frontier should now begin at support size at least `4`, or
at non-support-three sectors not captured by these second-order Pr\"ufer normal forms.
