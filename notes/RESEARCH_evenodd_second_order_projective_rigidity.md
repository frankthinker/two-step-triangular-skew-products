# Second-Order Projective Rigidity of the Anchored Even-Odd Support-Three Sector

## Goal

The previous notes established two low-order structural facts for the anchored even-odd
support-three sector
\[
F(t)=J_0(t)+b\widetilde J_m(t)+c\widetilde J_n(t),
\qquad m\ \text{even},\ n\ \text{odd},
\]
with
\[
\widetilde J_m:=(-1)^{m/2}J_m,
\qquad
\widetilde J_n:=(-1)^{(n-1)/2}J_n.
\]

1. The condition `\lambda_2(F)=0` collapses the genuinely support-three branch to a one-parameter
   algebraic curve.
2. Along that curve, the first invariant `\lambda_1(F)` is a fractional-linear coordinate.

This note closes the circle:

> once the anchor normalization `q=8\lambda_1>0` is imposed, the resulting candidate curve has
> `c^2<0` identically.

So the anchored even-odd support-three sector is empty already at second order. This is the
first genuinely local projective-rigidity theorem for the normalized Prüfer map near the `J_0`
anchor.

## 1. Second-order normal form

Write
\[
M:=m^2,\qquad N:=n^2.
\]
The general second-order normal form gives
\[
\lambda_1(F)
=
-\frac{M\,b(b+1)+(N-1)c^2}{2\bigl((1+b)^2+c^2\bigr)},
\]
and
\[
\lambda_2(F)
=
-\frac{c\bigl((b+1)\mathcal Q_{M,N}(b)+c^2\mathcal R_{M,N}(b)\bigr)}
{8\bigl((1+b)^2+c^2\bigr)^2},
\]
where
\[
\mathcal Q_{M,N}(b)
=
(N-1)^2
+b(-M^2-2MN+6M+2N^2-4N+2)
+b^2(M^2-2MN+6M+N^2-2N+1),
\]
\[
\mathcal R_{M,N}(b)
=
-M^2b+2MNb+2Mb-N^2b-N^2+2Nb+2N-b-1.
\]

On the genuinely support-three branch
\[
c\neq 0,\qquad b\neq -1,
\]
the equation `\lambda_2(F)=0` is therefore equivalent to
\[
c^2=-\frac{(b+1)\mathcal Q_{M,N}(b)}{\mathcal R_{M,N}(b)}.
\]

The Möbius-curve note then shows that on this candidate curve
\[
\lambda_1(F)
=
\frac{-M^2b+4Mb+N^2b+N^2-2Nb-2N+b+1}
{4(Mb-Nb-N+b+1)}.
\]

## 2. Solving the anchor normalization

For a common anchored infinite-resonance configuration, the normalized first shift coefficient is
forced to satisfy
\[
q:=8\lambda_1(F)>0.
\]

Solving the Möbius relation `8\lambda_1(F)=q` for `b` gives a unique candidate:
\[
b=b(q):=
\frac{2N^2+Nq-4N-q+2}
{2M^2+Mq-8M-2N^2-Nq+4N+q-2}.
\]

Substituting this into the second-order candidate-curve equation yields an explicit formula for
`c^2`.

### Proposition

Along the anchored second-order candidate locus, one has
\[
c^2
=
-\frac{M^2(2M+q-8)\bigl(q^2+(2M+4N-12)q+8(N-1)^2\bigr)}
{(4N+q-4)\bigl(2M^2+Mq-8M-2N^2-Nq+4N+q-2\bigr)^2}.
\]

### Proof

Substitute the explicit expression `b=b(q)` into
\[
c^2=-\frac{(b+1)\mathcal Q_{M,N}(b)}{\mathcal R_{M,N}(b)}
\]
and simplify. The denominator becomes a perfect square times the positive factor `4N+q-4`.
The remaining numerator factorizes exactly as written.

## 3. Sign theorem

Now restrict to the actual even-odd support-three sector:
\[
M=(2k)^2\ge 4,
\qquad
N=(2r+1)^2\ge 1,
\qquad
q>0.
\]

Then every factor in the denominator is strictly positive:
\[
4N+q-4>0.
\]
Moreover
\[
2M+q-8\ge q>0,
\]
and
\[
q^2+(2M+4N-12)q+8(N-1)^2>0.
\]
Indeed, the quadratic has positive leading coefficient, nonnegative constant term, and
\[
2M+4N-12\ge 2\cdot 4+4\cdot 1-12=0,
\]
with strict positivity unless `(M,N)=(4,1)`, in which case it reduces to `q^2`.

Therefore the numerator in the formula above is strictly positive, and the prefactor `-1`
forces
\[
c^2<0.
\]

This is impossible over the reals.

### Theorem

Let
\[
F(t)=J_0(t)+b\widetilde J_m(t)+c\widetilde J_n(t),
\qquad m\ \text{even},\ n\ \text{odd},
\]
with `m\ge 2` and `n\ge 1`.
Assume `F` lies in the anchored fiber of the normalized Prüfer map, i.e.
\[
\lambda_2(F)=0,
\qquad
8\lambda_1(F)=q>0.
\]
Then the genuinely support-three branch is impossible. Equivalently,
\[
c=0.
\]

So the whole anchored even-odd support-three sector is disjoint from the `J_0` fiber already at
second order.

## 4. Meaning

This theorem is substantially stronger than the previously proved ladder closures.

It shows that:

1. the second-order Möbius curve exists as a formal candidate only before the anchor
   normalization is imposed;
2. once one asks for actual anchored compatibility, that Möbius curve has no real points at all
   in the genuinely support-three region;
3. the fixed-even support-three emptiness theorems are not isolated eliminations, but shadows of
   a single local projective-rigidity mechanism.

In particular, the whole sector
\[
J_0+bJ_{2k}+cJ_{2r+1}
\]
should no longer be regarded as an open frontier. It is already excluded by the second-order
geometry of the normalized Prüfer map.

## 5. Consequences for the global picture

This upgrades the anchored geometry as follows.

- The support-two anchored sector was already fully classified.
- The shared-profile multi-frequency sector is already globally finite-resonance.
- The even-odd support-three sector is now excluded in one shot by second-order projective
  rigidity.

So the first genuinely unresolved anchored frontier is pushed beyond the whole even-odd
support-three regime.

At the level of moduli, the mechanism is now:
\[
\text{second-order candidate locus}
\Longrightarrow
\text{Möbius curve}
\Longrightarrow
\text{anchor normalization}
\Longrightarrow
\text{negative } c^2.
\]

This is the clearest local fiber-rigidity statement obtained so far.
