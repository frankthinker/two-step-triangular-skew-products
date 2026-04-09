# Shared-Profile Multi-Frequency Rigidity

## Goal

The pure vertical finite-band theorem shows that one cannot superimpose two distinct pure
vertical frequencies and still retain infinitely many common resonant parameters.

The same mechanism extends to a wider class: several vertical frequencies may carry the same
phase-aligned `x`-profile. In that case the asymptotic-compatibility hierarchy shows that common
infinite resonance is still highly rigid, and typically impossible.

## Shared profile family

Fix a nontrivial phase-aligned profile
\[
b=(b_m)_{|m|\le M},
\]
and let
\[
F_b(t):=\sum_{|m|\le M} b_m J_m(t).
\]
Assume `F_b` lies in the oscillatory-real class, so its positive zeros admit an asymptotic
expansion
\[
t_k=k\pi+\delta_b+\sum_{r=1}^L \lambda_r(b)\,(k\pi)^{-r}+O(k^{-L-1})
\]
to every finite order `L`.

Now choose distinct positive frequencies
\[
\mathcal{N}=\{n_1,\dots,n_s\},
\]
and consider cocycles of the form
\[
h(x,y)=\sum_{n\in\mathcal{N}} c_n
\Bigl(G_b(x)e(ny)+\overline{G_b(x)e(ny)}\Bigr),
\qquad c_n\in\R\setminus\{0\},
\]
where
\[
G_b(x):=\sum_{|m|\le M} b_m i^m e(-ma/2)e(mx).
\]

For each active frequency `n`, the obstruction is simply a nonzero scalar multiple of
`F_b(nz_0)`. Therefore all active frequencies share the same asymptotic invariants:
\[
\delta_n=\delta_b,\qquad \lambda_{n,r}=\lambda_r(b).
\]

## First explicit exceptional hypersurface

Write
\[
A:=\sum b_m\cos(m\pi/2),\qquad
B:=\sum b_m\sin(m\pi/2),
\]
and
\[
C:=\frac18\sum b_m(4m^2-1)\sin(m\pi/2),\qquad
D:=-\frac18\sum b_m(4m^2-1)\cos(m\pi/2).
\]
Then, on the oscillatory sector `\rho^2:=A^2+B^2>0`, the first correction coefficient is
\[
\lambda_1(b)=\frac{AD-BC}{A^2+B^2}.
\]

### Proof

From the earlier note,
\[
\lambda_1(b)=\frac{V}{\rho},
\qquad
V=-C\sin\phi+D\cos\phi,
\]
where
\[
\cos\phi=\frac{A}{\rho},\qquad \sin\phi=\frac{B}{\rho}.
\]
Therefore
\[
V=\frac{-BC+AD}{\rho},
\]
hence
\[
\lambda_1(b)=\frac{AD-BC}{\rho^2}
=\frac{AD-BC}{A^2+B^2}.
\]

### Consequence

The first exceptional locus
\[
\mathscr E_1:=\{b:\rho>0,\ \lambda_1(b)=0\}
\]
is the explicit real-algebraic hypersurface
\[
AD-BC=0.
\]

Since this polynomial is not identically zero, `\mathscr E_1` is a proper subset of the
oscillatory sector.

For example, in the two-parameter family
\[
F_b(t)=b_0J_0(t)+b_1J_1(t),
\]
one has
\[
A=b_0,\quad B=b_1,\quad C=\frac38 b_1,\quad D=\frac18 b_0,
\]
so
\[
\lambda_1(b)=\frac{b_0^2-3b_1^2}{8(b_0^2+b_1^2)}.
\]
Hence the first exceptional locus is
\[
b_0^2=3b_1^2.
\]

## Consequence of the hierarchy

### Theorem 1

Let `r_*(b)\ge 1` be the smallest index such that
\[
\lambda_{r_*(b)}(b)\neq 0.
\]
If at least two distinct positive frequencies are active, then the shared-profile family above
has only finitely many real resonant parameters.

### Proof

Suppose there were infinitely many real resonant parameters. Then by the compatibility hierarchy,
for every pair of active distinct frequencies `m,n` one would have
\[
m^{r+1}\lambda_r(b)=n^{r+1}\lambda_r(b)
\]
for every `r\ge 1`.

Applying this with `r=r_*(b)` gives
\[
m^{r_*(b)+1}\lambda_{r_*(b)}(b)=n^{r_*(b)+1}\lambda_{r_*(b)}(b).
\]
Since `\lambda_{r_*(b)}(b)\neq 0`, we conclude
\[
m^{r_*(b)+1}=n^{r_*(b)+1},
\]
hence `m=n`, a contradiction.

Therefore the real resonant parameter set is finite.

### Generic finite-resonance corollary

If at least two distinct positive frequencies are active and
\[
\lambda_1(b)\neq 0,
\]
then the real resonant parameter set is finite.

Equivalently, outside the explicit hypersurface
\[
AD-BC=0,
\]
the shared-profile multi-frequency family has only finitely many real resonant parameters.

## Examples

1. Pure vertical profile:
   \[
   F_b(t)=J_0(t).
   \]
   Here `r_*(b)=1`, recovering the previously proved pure-vertical theorem.

2. Any phase-aligned profile with nonzero second-order invariant:
   if `\lambda_1(b)\neq 0`, then any multi-frequency superposition with this shared profile has
   only finitely many real resonant parameters.

3. More generally, the same remains true as soon as some higher correction `\lambda_r(b)` is
   nonzero.

4. Explicit first-exception example:
   in the family `b_0J_0+b_1J_1`, the profile
   \[
   \sqrt{3}\,J_0(t)+J_1(t)
   \]
   satisfies `\lambda_1=0`. This is an honest exceptional point of the first hypersurface, so the
   condition `\lambda_1\neq 0` is a genuine generic condition rather than a vacuous one.

## The first exceptional hypersurface is not the end

The example
\[
F(t)=\sqrt{3}\,J_0(t)+J_1(t)
\]
lies on the first exceptional hypersurface `\lambda_1=0`, but it still does not support
multi-frequency infinite resonance.

Indeed, use the standard two-term Hankel expansions
\[
J_0(t)=\sqrt{\frac{2}{\pi t}}
\left(
\cos\xi+\frac{1}{8t}\sin\xi-\frac{9}{128t^2}\cos\xi+O(t^{-3})
\right),
\]
\[
J_1(t)=\sqrt{\frac{2}{\pi t}}
\left(
\sin\xi+\frac{3}{8t}\cos\xi-\frac{15}{128t^2}\sin\xi+O(t^{-3})
\right),
\]
where `\xi=t-\pi/4`.

Therefore
\[
F(t)=\sqrt{\frac{2}{\pi t}}
\left(
\Bigl(\sqrt{3}+\frac{3}{8t}-\frac{9\sqrt{3}}{128t^2}\Bigr)\cos\xi
+
\Bigl(1+\frac{\sqrt{3}}{8t}-\frac{15}{128t^2}\Bigr)\sin\xi
+O(t^{-3})
\right).
\]

Rotate by the phase `\phi=\pi/6`, so that the leading term becomes `2\cos(\xi-\phi)`. The
coefficient of `t^{-1}\sin(\xi-\phi)` vanishes, exactly as predicted by `\lambda_1=0`. But the
coefficient of `t^{-2}\sin(\xi-\phi)` is
\[
-\Bigl(-\frac{9\sqrt{3}}{128}\Bigr)\sin\phi
+\Bigl(-\frac{15}{128}\Bigr)\cos\phi
=-\frac{3\sqrt{3}}{64}\neq 0.
\]

Hence the zero expansion has a nonzero second correction:
\[
t_k=k\pi+\delta+\frac{\lambda_2}{(k\pi)^2}+O(k^{-3}),
\qquad
\lambda_2\neq 0.
\]
By the shared-profile theorem, any multi-frequency superposition built from this profile has only
finitely many real resonant parameters.

### Meaning

This shows that the exceptional hierarchy is genuinely descending:

- the first exceptional hypersurface `\lambda_1=0` is nonempty;
- but it still contains points where the next obstruction `\lambda_2` is nonzero;
- so infinite common resonance, if it survives at all, is forced into a thinner subset.

## Why this matters

This goes beyond the pure vertical theorem in a meaningful way.

It shows that the obstruction against multi-frequency infinite resonance is not a special feature
of `J_0`. It is inherited by any shared-profile family as soon as the zero sequence of the common
profile is not asymptotically a perfect arithmetic progression to all orders.

So the current project is uncovering a robust principle:

> Single-profile oscillatory families may have infinitely many resonant parameters in one
> frequency, but the moment one superimposes two distinct vertical frequencies, higher-order zero
> asymptotics force the common resonant set to become finite.

This is a nontrivial strengthening of the pure vertical picture.

## Exceptional hierarchy for shared profiles

For the shared-profile multi-frequency family, the asymptotic-compatibility hierarchy collapses
to a particularly clean nested exceptional set picture.

For each `L\ge 1`, define
\[
\mathscr E_L:=\{b:\rho(b)>0,\ \lambda_1(b)=\cdots=\lambda_L(b)=0\}.
\]
Then
\[
\mathscr E_{L+1}\subset \mathscr E_L.
\]

### Theorem 2

Fix at least two distinct active positive frequencies and a shared oscillatory profile `b`.

1. If `b\notin \mathscr E_L` for some `L\ge 1`, then the real resonant parameter set is finite.
2. Therefore, if the shared-profile family admits infinitely many real resonant parameters, one
   must have
   \[
   b\in \bigcap_{L\ge 1}\mathscr E_L.
   \]

### Proof

If `b\notin \mathscr E_L`, then `\lambda_r(b)\neq 0` for some `1\le r\le L`. The shared-profile
theorem then shows that distinct active frequencies cannot satisfy the `r`th compatibility
relation
\[
m^{r+1}\lambda_r(b)=n^{r+1}\lambda_r(b),
\]
so the real resonant parameter set is finite.

The second statement is the contrapositive.

### First geometric information

The first two layers are already nontrivial:

1. `\mathscr E_1` is the explicit algebraic hypersurface
   \[
   AD-BC=0;
   \]
2. `\mathscr E_2` is a proper subset of `\mathscr E_1`, because the example
   \[
   \sqrt{3}\,J_0+J_1
   \]
   lies in `\mathscr E_1` but not in `\mathscr E_2`.

So the hierarchy genuinely descends at least through the first two stages.

## Conceptual reformulation

The shared-profile family now has the following structure:

- one-frequency superpositions may exhibit infinitely many resonant parameters;
- as soon as two distinct frequencies are active, generic profiles are ruled out by the first
  obstruction `\lambda_1`;
- even the first exceptional hypersurface is not enough: one must continue satisfying
  `\lambda_2=0,\lambda_3=0,\dots`.

This means that multi-frequency infinite resonance can survive only on an increasingly rigid
profile locus. That is a much deeper statement than a single explicit family theorem.

## Formal phase-purity criterion

The exceptional hierarchy can be reorganized into a single formal criterion.

Let `F_b` be a shared oscillatory profile. Its full Hankel expansion has the form
\[
F_b(t)\sim \sqrt{\frac{2}{\pi t}}
\Bigl(A_b(t^{-1})\cos\xi+B_b(t^{-1})\sin\xi\Bigr),
\qquad
\xi=t-\frac{\pi}{4},
\]
where `A_b(u),B_b(u)` are formal real power series in `u=t^{-1}` with
\[
A_b(0)=A,\qquad B_b(0)=B,\qquad \rho:=\sqrt{A^2+B^2}>0.
\]

Choose `\phi` so that
\[
\cos\phi=\frac{A}{\rho},\qquad \sin\phi=\frac{B}{\rho},
\]
and set
\[
\psi:=\xi-\phi.
\]
After this rotation,
\[
F_b(t)\sim \sqrt{\frac{2}{\pi t}}
\Bigl(\mathcal A_b(t^{-1})\cos\psi+\mathcal B_b(t^{-1})\sin\psi\Bigr),
\]
where
\[
\mathcal A_b(0)=\rho,\qquad \mathcal B_b(0)=0.
\]

### Proposition 4

There exists a unique formal power series
\[
s_b(u)=\sum_{r\ge 1}\lambda_r(b)u^r
\]
such that the formal zero condition near the `k`th oscillatory root is
\[
\psi=\frac{\pi}{2}+s_b(u).
\]

Moreover,

1. the coefficients `\lambda_r(b)` are exactly the higher zero-shift invariants from the
   asymptotic expansion of the positive zeros;
2. one has
   \[
   s_b(u)\equiv 0
   \quad\Longleftrightarrow\quad
   \mathcal B_b(u)\equiv 0
   \]
   as formal power series;
3. equivalently,
   \[
   \lambda_r(b)=0\ \text{for every }r\ge 1
   \quad\Longleftrightarrow\quad
   \mathcal B_b(u)\equiv 0.
   \]

### Proof

The formal zero equation is
\[
0=-\mathcal A_b(u)\sin s+\mathcal B_b(u)\cos s,
\]
with unknown formal series `s=s_b(u)` satisfying `s(0)=0`. Since `\mathcal A_b(0)=\rho\neq 0`,
the formal implicit function theorem gives existence and uniqueness of `s_b(u)`.

By construction, substituting `u\sim (k\pi)^{-1}` converts `s_b(u)` into the asymptotic shift of
the `k`th zero, so its coefficients are the `\lambda_r(b)`.

If `s_b(u)\equiv 0`, the zero equation reduces to `\mathcal B_b(u)\equiv 0`. Conversely, if
`\mathcal B_b(u)\equiv 0`, then the zero equation becomes `\mathcal A_b(u)\sin s=0`, whose unique
formal solution with zero constant term is `s_b(u)\equiv 0`.

### Consequence

For shared-profile multi-frequency families with at least two distinct active frequencies,
infinite common resonance can occur only if the rotated sine component of the full Hankel series
vanishes identically:
\[
\mathcal B_b(u)\equiv 0.
\]

So the infinite hierarchy of compatibility conditions collapses to a single formal phase-purity
criterion.

## Complex-amplitude reformulation

The formal phase-purity criterion admits a compact complex form.

For each fixed order `m`, the Hankel expansion may be written as
\[
J_m(t)\sim \sqrt{\frac{2}{\pi t}}\,
\Re\!\Bigl(e^{i(t-\pi/4)}(-i)^m H_m(t^{-1})\Bigr),
\]
where `H_m(u)` is a formal complex power series with real-analytic coefficients and
\[
H_m(0)=1.
\]

Therefore a shared profile
\[
F_b(t)=\sum_{|m|\le M} b_mJ_m(t)
\]
has the form
\[
F_b(t)\sim \sqrt{\frac{2}{\pi t}}\,
\Re\!\Bigl(e^{i(t-\pi/4)}\mathcal G_b(t^{-1})\Bigr),
\]
with formal complex amplitude
\[
\mathcal G_b(u):=\sum_{|m|\le M} b_m(-i)^m H_m(u).
\]

### Proposition 5

The following are equivalent for an oscillatory shared profile `b`.

1. `b` lies in every exceptional layer `\mathscr E_L`.
2. All higher zero-shift coefficients vanish:
   \[
   \lambda_r(b)=0\qquad (r\ge 1).
   \]
3. There exists `\phi\in\R` such that
   \[
   e^{-i\phi}\mathcal G_b(u)\in \R[[u]]
   \]
   as a formal power series.

### Proof

The equivalence of `(1)` and `(2)` is by definition.

Write
\[
e^{-i\phi}\mathcal G_b(u)=\mathcal A_b(u)-i\mathcal B_b(u),
\]
where `\phi` is the leading phase chosen earlier, so `\mathcal A_b(0)=\rho` and
`\mathcal B_b(0)=0`. Then
\[
\Re\!\Bigl(e^{i(t-\pi/4)}\mathcal G_b(t^{-1})\Bigr)
=
\mathcal A_b(t^{-1})\cos\psi+\mathcal B_b(t^{-1})\sin\psi,
\]
with `\psi=t-\pi/4-\phi`.

By Proposition 4, all `\lambda_r` vanish if and only if `\mathcal B_b(u)\equiv 0`, and this is
equivalent to `e^{-i\phi}\mathcal G_b(u)` being real as a formal series.

### Research interpretation

This is the cleanest current formulation of the shared-profile obstruction.

The exceptional intersection
\[
\bigcap_{L\ge 1}\mathscr E_L
\]
is exactly the set of profiles whose formal Hankel amplitude has constant argument.

So the remaining open problem in this direction can be phrased very concretely:

> For which finite Bessel combinations can the formal amplitude `\mathcal G_b(u)` have constant
> argument?

If the answer is “only the trivial profile”, then multi-frequency infinite resonance is
impossible for every nontrivial shared profile.

## Complete classification for the two-term profile family

The previous discussion becomes completely explicit for the two-dimensional profile family
\[
F_{b_0,b_1}(t):=b_0J_0(t)+b_1J_1(t).
\]

This is the first nontrivial low-dimensional family in which the shared-profile hierarchy can be
closed completely.

### Asymptotic coefficients

Using
\[
J_0(t)=\sqrt{\frac{2}{\pi t}}
\left(
\cos\xi+\frac{1}{8t}\sin\xi-\frac{9}{128t^2}\cos\xi+O(t^{-3})
\right),
\]
\[
J_1(t)=\sqrt{\frac{2}{\pi t}}
\left(
\sin\xi+\frac{3}{8t}\cos\xi-\frac{15}{128t^2}\sin\xi+O(t^{-3})
\right),
\]
with `\xi=t-\pi/4`, one obtains
\[
F_{b_0,b_1}(t)=\sqrt{\frac{2}{\pi t}}
\left(
\Bigl(b_0+\frac{3b_1}{8t}-\frac{9b_0}{128t^2}\Bigr)\cos\xi
+
\Bigl(b_1+\frac{b_0}{8t}-\frac{15b_1}{128t^2}\Bigr)\sin\xi
+O(t^{-3})
\right).
\]

Write
\[
\rho:=\sqrt{b_0^2+b_1^2},\qquad
\phi:=\operatorname{atan2}(b_1,b_0),\qquad
\delta:=\frac{3\pi}{4}+\phi.
\]
Then the first two zero-shift coefficients are
\[
\lambda_1(b_0,b_1)=\frac{b_0^2-3b_1^2}{8(b_0^2+b_1^2)},
\]
and, on the exceptional locus `\lambda_1=0`,
\[
\lambda_2(b_0,b_1)=\frac{-3b_0b_1}{64(b_0^2+b_1^2)}.
\]

### Proof of the `\lambda_2` formula

On the rotated phase `\psi:=\xi-\phi`, the coefficient of `t^{-1}\sin\psi` is
\[
V_1=\frac{b_0^2-3b_1^2}{8\rho},
\]
hence
\[
\lambda_1=\frac{V_1}{\rho}.
\]
The coefficient of `t^{-2}\sin\psi` is
\[
V_2=
-\left(-\frac{9b_0}{128}\right)\sin\phi
+
\left(-\frac{15b_1}{128}\right)\cos\phi
=-\frac{3b_0b_1}{64\rho},
\]
so once `V_1=0`, the next zero correction is
\[
\lambda_2=\frac{V_2}{\rho}
=\frac{-3b_0b_1}{64(b_0^2+b_1^2)}.
\]

### Theorem 3

Let at least two distinct positive vertical frequencies be active, and let the shared
phase-aligned profile be
\[
F_{b_0,b_1}(t)=b_0J_0(t)+b_1J_1(t),
\qquad (b_0,b_1)\neq (0,0).
\]
Then the common real resonant parameter set is finite.

### Proof

If `\lambda_1(b_0,b_1)\neq 0`, finiteness follows from the generic shared-profile theorem.

Assume now `\lambda_1(b_0,b_1)=0`. Then
\[
b_0^2=3b_1^2.
\]
Since `(b_0,b_1)\neq (0,0)`, one has `b_0b_1\neq 0`, and therefore
\[
\lambda_2(b_0,b_1)=\frac{-3b_0b_1}{64(b_0^2+b_1^2)}\neq 0.
\]
Applying the exceptional-hierarchy theorem with `L=2`, we again obtain finiteness of the common
real resonant set.

So no nontrivial two-term shared profile can support infinite common resonance across two
distinct active frequencies.

### Interpretation

This is a complete low-dimensional model of the hierarchy:

1. the generic region `\lambda_1\neq 0` is already finite-resonance;
2. the first exceptional hypersurface `\lambda_1=0` is nonempty;
3. but on that hypersurface the next invariant `\lambda_2` is automatically nonzero away from the
   origin;
4. hence infinite common resonance never occurs for nontrivial `b_0J_0+b_1J_1`.

This is stronger than the pure vertical theorem and gives a fully closed result beyond the single
frequency case.

## Complete classification for every two-term Bessel profile

The preceding theorem is not special to `J_0` and `J_1`. The same mechanism closes every
two-term profile
\[
F_{p,q}(t):=aJ_p(t)+bJ_q(t),
\qquad
0\le p<q,\quad ab\neq 0.
\]

### Hankel coefficients

Write the standard complex Hankel expansion in the form
\[
J_m(t)\sim \sqrt{\frac{2}{\pi t}}\,
\Re\!\left(
e^{i(t-\pi/4)}(-i)^m
\bigl(
1+i\alpha_m t^{-1}-\beta_m t^{-2}-i\gamma_m t^{-3}+O(t^{-4})
\bigr)
\right),
\]
where
\[
\alpha_m=\frac{4m^2-1}{8},
\qquad
\beta_m=\frac{(4m^2-1)(4m^2-9)}{128},
\qquad
\gamma_m=\frac{(4m^2-1)(4m^2-9)(4m^2-25)}{3072}.
\]

### Theorem 4

Let at least two distinct positive vertical frequencies be active, and let the shared
phase-aligned profile be
\[
F_{p,q}(t)=aJ_p(t)+bJ_q(t),
\qquad
0\le p<q,\quad ab\neq 0.
\]
Then the common real resonant parameter set is finite.

### Proof

Assume for contradiction that the common real resonant set is infinite. By the exceptional
hierarchy, all zero-shift coefficients must vanish:
\[
\lambda_r=0\qquad (r\ge 1).
\]
Equivalently, by the formal phase-purity criterion, the complex amplitude of `F_{p,q}` must have
constant formal argument.

Factor out the common phase `(-i)^p` and set
\[
r:=\frac{b}{a}\in\R\setminus\{0\},
\qquad
\eta:=(-i)^{q-p}\in\{1,-1,i,-i\}.
\]
Then the formal amplitude is
\[
\mathcal G(u)=
1+r\eta
+i(\alpha_p+r\eta\alpha_q)u
-(\beta_p+r\eta\beta_q)u^2
-i(\gamma_p+r\eta\gamma_q)u^3
+O(u^4).
\]

We now distinguish cases according to `\eta`.

#### Case 1: `\eta=\pm 1`

Then the constant term and the `u^2` coefficient are real, while the `u` and `u^3`
coefficients are purely imaginary.

If `1+r\eta\neq 0`, constant formal argument forces
\[
\alpha_p+r\eta\alpha_q=0,
\qquad
\gamma_p+r\eta\gamma_q=0.
\]
Eliminating `r` gives
\[
\frac{\gamma_p}{\alpha_p}=\frac{\gamma_q}{\alpha_q},
\]
that is,
\[
(4p^2-9)(4p^2-25)=(4q^2-9)(4q^2-25).
\]
Writing `x=p^2`, `y=q^2`, this becomes
\[
(16x^2-136x+225)=(16y^2-136y+225),
\]
hence
\[
(x-y)\bigl(16(x+y)-136\bigr)=0.
\]
Since `x\neq y`, this would force `x+y=17/2`, impossible for integers `x,y`.

If `1+r\eta=0`, then the constant term vanishes. In that case the `u` coefficient is nonzero
because `\alpha_p\neq \alpha_q`, while the `u^2` coefficient is real and nonzero because
`\beta_p\neq \beta_q`. So the first two nonzero coefficients already have different arguments,
contradicting formal phase purity.

#### Case 2: `\eta=\pm i`

Here the constant term and the `u` coefficient can be collinear only if
\[
\alpha_p+r^2\alpha_q=0,
\]
so `\alpha_p\alpha_q<0`. This forces one of `p,q` to be zero and the other positive.

Now compare the constant term with the `u^2` coefficient. Collinearity gives
\[
\beta_p=\beta_q.
\]
But the map
\[
m^2\mapsto (4m^2-1)(4m^2-9)
\]
is injective on integer squares, because equality would imply
\[
(x-y)\bigl(16(x+y)-40\bigr)=0
\]
with `x=p^2`, `y=q^2`, hence `x+y=5/2`, impossible.

So this case is also impossible.

All possibilities lead to contradictions. Therefore the formal phase-purity criterion fails, so
the exceptional hierarchy implies that the common real resonant set is finite.

### Interpretation

This is the first fully closed multi-frequency theorem for a genuinely nontrivial family beyond
the pure vertical case.

It shows that no nontrivial two-term Bessel profile can support infinite common resonance across
two distinct active vertical frequencies.

## Same-parity support theorem

The two-term result extends to a much larger class of shared profiles.

Consider a reduced real profile
\[
F(t)=\sum_{m\in S} c_m J_m(t),
\]
where `S\subset \Z_{\ge 0}` is finite, `c_m\in\R`, and all active orders have the same parity.

### Theorem 5

Assume `F` is nontrivial and oscillatory, and that all active orders in `S` have the same
parity. If at least two distinct positive vertical frequencies are active in the shared-profile
family generated by `F`, then the common real resonant parameter set is finite.

### Proof

Since all active orders have the same parity, there exists `\sigma\in\{1,-i\}` and signs
`\varepsilon_m\in\{\pm 1\}` such that
\[
(-i)^m=\sigma\,\varepsilon_m
\qquad (m\in S).
\]
Factor out the common phase `\sigma` from the formal amplitude:
\[
\mathcal G_F(u)=\sigma \sum_{m\in S} \widetilde c_m H_m(u),
\]
where `\widetilde c_m:=\varepsilon_m c_m\in\R`,
where each `H_m(u)` has the Hankel form
\[
H_m(u)=E_m(u)+i\,O_m(u),
\]
with `E_m(u),O_m(u)\in\R[[u]]`, `E_m` even in `u`, `O_m` odd in `u`, and
the coefficient of `u^{2k+1}` in `O_m` is a polynomial `P_k(m^2)` of degree `2k+1` with
nonzero leading coefficient.

If infinite common resonance were possible, the formal phase-purity criterion would imply that
after rotating by the leading phase the amplitude becomes real. Since all active terms already
share the same leading phase, this forces the entire odd part to vanish:
\[
\sum_{m\in S} \widetilde c_m O_m(u)\equiv 0.
\]
Equating coefficients of `u^{2k+1}` gives
\[
\sum_{m\in S} \widetilde c_m P_k(m^2)=0
\qquad (k\ge 0).
\]

For the Hankel expansion, `P_k(x)` is a nonzero constant multiple of
\[
Q_k(x):=\prod_{j=0}^{2k}\bigl(4x-(2j+1)^2\bigr).
\]
Hence
\[
\sum_{m\in S} \widetilde c_m Q_k(m^2)=0
\qquad (k\ge 0).
\]

For an integer `m\ge 0`,
\[
Q_k(m^2)=(-1)^{m+1}(4k+1-2m)!!\,(4k+1+2m)!!.
\]
Normalize by
\[
Q_k(0)=-\bigl((4k+1)!!\bigr)^2\neq 0,
\]
and define
\[
R_m(k):=\frac{Q_k(m^2)}{Q_k(0)}.
\]
Then
\[
\sum_{m\in S} \widetilde c_m R_m(k)=0
\]
for every integer `k\ge 0`.

Now `R_0(k)=1`, and for `m\ge 1`,
\[
R_m(k)=
(-1)^m
\frac{\prod_{u=1}^m(4k+2u+1)}
{\prod_{u=0}^{m-1}(4k-2u+1)}.
\]
So `R_m` is a rational function whose poles are
\[
-\frac14,\ \frac14,\ \frac34,\ \dots,\ \frac{2m-3}{4},
\]
and in particular it has a pole at `k=(2m-3)/4` that does not occur in `R_\ell` for
`\ell<m`.

Therefore the family `\{R_m\}_{m\in S}` is linearly independent over `\R`: if
\[
\sum_{m\in S} a_m R_m(k)\equiv 0
\]
as a rational function, choose the largest `m_*` with `a_{m_*}\neq 0` and inspect the unique
pole at `k=(2m_*-3)/4`; its coefficient cannot cancel with any lower-index term. Hence
`a_{m_*}=0`, a contradiction.

Since the equality
\[
\sum_{m\in S} c_m R_m(k)=0
\]
holds for infinitely many integers `k`, the rational function
\[
\sum_{m\in S} \widetilde c_m R_m(k)
\]
vanishes identically. By linear independence of the `R_m`, all `c_m=0`, contradicting the
nontriviality of `F`.

So the formal phase-purity criterion fails, and the exceptional-hierarchy theorem implies that
the common real resonant set is finite.

### Remarks

1. This includes the pure vertical profile `S=\{0\}` as a special case, recovering the already
   known fact that multi-frequency pure vertical resonance is finite.
2. It contains many genuinely `x`-dependent phase-aligned families, not just pure vertical
   cocycles.

### Meaning

This is a broad theorem showing that multi-frequency infinite resonance fails for an entire
structural class of profiles, not just for isolated examples or low-dimensional slices.

## Three-term mixed-parity model `J_0,J_1,J_2`

The first unresolved mixed-parity family after Theorems 4 and 5 is
\[
F_{b_0,b_1,b_2}(t):=b_0J_0(t)+b_1J_1(t)+b_2J_2(t).
\]

### Asymptotic data

Using the standard Hankel expansions for `J_0,J_1,J_2`, one obtains
\[
F_{b_0,b_1,b_2}(t)=\sqrt{\frac{2}{\pi t}}
\left(
\Bigl(A+\frac{C}{t}+\frac{E}{t^2}\Bigr)\cos\xi
+
\Bigl(B+\frac{D}{t}+\frac{F}{t^2}\Bigr)\sin\xi
+O(t^{-3})
\right),
\]
where
\[
A=b_0-b_2,\qquad B=b_1,
\]
\[
C=\frac{3b_1}{8},\qquad D=\frac{b_0+15b_2}{8},
\]
\[
E=\frac{-9b_0+105b_2}{128},\qquad F=\frac{15b_1}{128}.
\]

Hence
\[
\lambda_1=\frac{AD-BC}{A^2+B^2}
=\frac{b_0^2+14b_0b_2-15b_2^2-3b_1^2}
{8\bigl((b_0-b_2)^2+b_1^2\bigr)}.
\]

On the first exceptional locus `\lambda_1=0`, the second correction is
\[
\lambda_2=
\frac{-EB+FA}{A^2+B^2}
=
\frac{3b_1(b_0-5b_2)}
{16\bigl((b_0-b_2)^2+b_1^2\bigr)}.
\]

### Second exceptional reduction

If `\lambda_1\neq 0`, finiteness follows from the shared-profile theorem.

If `\lambda_1=\lambda_2=0`, then
\[
b_0^2+14b_0b_2-15b_2^2-3b_1^2=0,
\qquad
b_1(b_0-5b_2)=0.
\]

Thus either:

1. `b_1=0`, which reduces to the already settled same-parity family `b_0J_0+b_2J_2`; or
2. `b_0=5b_2`, in which case
   \[
   80b_2^2-3b_1^2=0.
   \]

So the unresolved mixed-parity locus in the `J_0,J_1,J_2` family is reduced to the two rays
\[
(b_0,b_1,b_2)=
\left(5,\ \pm 4\sqrt{\frac53},\ 1\right)\cdot t,
\qquad t\neq 0.
\]

### Third correction on the exceptional rays

On these two rays, the `t^{-3}` coefficient in the rotated expansion can be computed explicitly.
The unrotated `t^{-3}` terms are
\[
\frac{-315b_1}{3072}\cos\xi
+
\frac{-225b_0+945b_2}{3072}\sin\xi.
\]
Hence the rotated `t^{-3}\sin(\xi-\phi)` coefficient is
\[
V_3=\frac{-GB+JA}{\rho},
\]
where
\[
G=\frac{-315b_1}{3072},\qquad
J=\frac{-225b_0+945b_2}{3072},
\qquad
A=b_0-b_2,\quad B=b_1.
\]

Substituting
\[
(b_0,b_1,b_2)=
\left(5,\ \pm 4\sqrt{\frac53},\ 1\right)\cdot t
\]
gives
\[
-GB+JA=\frac52\,t^2,
\qquad
A^2+B^2=\frac{128}{3}\,t^2.
\]
Therefore
\[
\lambda_3=\frac{V_3}{\rho}=\frac{-GB+JA}{A^2+B^2}=\frac{15}{256}\neq 0.
\]

### Theorem 7

Let at least two distinct positive vertical frequencies be active, and let the shared
phase-aligned profile be
\[
F_{b_0,b_1,b_2}(t)=b_0J_0(t)+b_1J_1(t)+b_2J_2(t),
\qquad
(b_0,b_1,b_2)\neq (0,0,0).
\]
Then the common real resonant parameter set is finite.

### Proof

If `\lambda_1\neq 0`, finiteness follows immediately.

If `\lambda_1=0` but `\lambda_2\neq 0`, finiteness again follows.

If `\lambda_1=\lambda_2=0`, then either the profile reduces to the same-parity family
`b_0J_0+b_2J_2`, which is settled by Theorem 5, or else it lies on one of the two exceptional
rays above. On those rays, `\lambda_3=15/256\neq 0`, so the exceptional-hierarchy theorem again
forces finiteness.

Thus every nontrivial profile in the `J_0,J_1,J_2` family has finite common real resonant set as
soon as at least two distinct positive vertical frequencies are active.

### Meaning

The `J_0,J_1,J_2` family is fully closed after all. This is the first completely settled
three-term mixed-parity family.

## Complete classification for every consecutive three-term profile

The previous theorem extends to all consecutive triples
\[
F_{p}(t):=aJ_p(t)+bJ_{p+1}(t)+cJ_{p+2}(t),
\qquad p\ge 0.
\]

### Theorem 8

Let at least two distinct positive vertical frequencies be active, and let the shared
phase-aligned profile be
\[
F_{p}(t)=aJ_p(t)+bJ_{p+1}(t)+cJ_{p+2}(t),
\qquad
(a,b,c)\neq (0,0,0).
\]
Then the common real resonant parameter set is finite.

### Proof

The case `p=0` is exactly Theorem 7, so assume `p\ge 1`.

If `\lambda_1\neq 0`, finiteness follows immediately. Assume therefore `\lambda_1=0`.

If `b=0`, then
\[
F_p(t)=aJ_p(t)+cJ_{p+2}(t),
\]
which has same-parity support, so finiteness follows from Theorem 5.

Assume now `b\neq 0` and suppose also `\lambda_2=0`. Using the signed Hankel coefficients
\[
\alpha_m=\frac{4m^2-1}{8},
\qquad
\beta_m=\frac{(4m^2-1)(4m^2-9)}{128},
\]
the second-order condition is
\[
a(\beta_p-\beta_{p+1})+c(\beta_{p+1}-\beta_{p+2})=0.
\]
Now
\[
\beta_p-\beta_{p+1}
=-\frac{(2p-1)(2p+1)(2p+3)}{16},
\]
\[
\beta_{p+2}-\beta_{p+1}
=\frac{(2p+1)(2p+3)(2p+5)}{16},
\]
so
\[
\frac{a}{c}=-\frac{2p+5}{2p-1}.
\]

Substituting this into the first-order condition yields
\[
b^2
=
-\frac{16(p+1)^2(2p+5)}{(2p-1)(2p+1)(2p+3)}\,c^2.
\]
For `p\ge 1`, the right-hand side is strictly negative, impossible for real `b`.

Hence the system `\lambda_1=\lambda_2=0` has no genuinely mixed-parity solution when `p\ge 1`.
Therefore every nontrivial profile in the consecutive three-term family has either

1. `\lambda_1\neq 0`, or
2. `\lambda_2\neq 0`, or
3. `b=0`, reducing to the same-parity case.

In all three cases the common real resonant set is finite.

### Meaning

This closes an entire infinite sequence of mixed-parity three-term families, not just the
special case `J_0,J_1,J_2`.

## A nonconsecutive mixed-parity triple: `J_0,J_1,J_3`

To go beyond consecutive triples, consider
\[
F_{a,b,c}(t):=aJ_0(t)+bJ_1(t)+cJ_3(t).
\]

### Asymptotic data

Factoring the common even phase, one obtains
\[
F_{a,b,c}(t)=\sqrt{\frac{2}{\pi t}}
\left(
\Bigl(A+\frac{C}{t}+\frac{E}{t^2}\Bigr)\cos\xi
+
\Bigl(B+\frac{D}{t}+\frac{F}{t^2}\Bigr)\sin\xi
+O(t^{-3})
\right),
\]
where
\[
A=a,\qquad B=b-c,
\]
\[
C=\frac{3b-35c}{8},\qquad D=\frac{a}{8},
\]
\[
E=-\frac{9a}{128},\qquad F=\frac{15b+945c}{128}.
\]

Hence
\[
\lambda_1=\frac{AD-BC}{A^2+B^2}
=\frac{a^2-(b-c)(3b-35c)}{8\bigl(a^2+(b-c)^2\bigr)}.
\]

On the first exceptional locus `\lambda_1=0`, the second correction is
\[
\lambda_2=
\frac{-EB+FA}{A^2+B^2}
=
\frac{3a(b+39c)}{16\bigl(a^2+(b-c)^2\bigr)}.
\]

### Theorem 9

Let at least two distinct positive vertical frequencies be active, and let the shared
phase-aligned profile be
\[
F_{a,b,c}(t)=aJ_0(t)+bJ_1(t)+cJ_3(t),
\qquad
(a,b,c)\neq (0,0,0).
\]
Then the common real resonant parameter set is finite.

### Proof

If `\lambda_1\neq 0`, finiteness follows immediately.

Assume `\lambda_1=0`. If `a=0`, then the profile reduces to
\[
bJ_1+cJ_3,
\]
which has same-parity support and is settled by Theorem 5.

Assume `a\neq 0`. If `\lambda_2=0`, then
\[
b=-39c.
\]
Substituting this into `\lambda_1=0` gives
\[
a^2=(-40c)(-152c)=6080c^2.
\]

Now look at the `t^{-3}` term. The corresponding coefficients are
\[
G=\frac{-315b+10395c}{3072},\qquad
J=-\frac{225a}{3072},
\]
so the rotated `t^{-3}\sin(\xi-\phi)` coefficient satisfies
\[
-GB+JA
=
-\left(\frac{945c}{128}\right)(-40c)-\frac{225}{3072}a^2
=-150c^2\neq 0.
\]
Therefore `\lambda_3\neq 0`, and the exceptional-hierarchy theorem forces finiteness.

So every nontrivial `J_0,J_1,J_3` shared profile has finite common real resonant set as soon as
at least two distinct positive vertical frequencies are active.

### Meaning

This is the first settled nonconsecutive mixed-parity three-term family. It shows that the
mechanism goes beyond the consecutive-triple template.

## Current frontier for shared profiles

Combining Theorem 4, Theorem 5, Theorem 7, and Theorem 8 gives a sharper description of what
remains unresolved.

### Corollary 6

Let `F_b` be a nontrivial shared oscillatory profile. Suppose the associated shared-profile
multi-frequency family has infinitely many common real resonant parameters for at least two
distinct active positive vertical frequencies.

Then:

1. the reduced support of `F_b` contains at least three active Bessel orders;
2. the support of `F_b` mixes both parities;
3. the support is not contained in any same-parity set;
4. the support is not contained in any consecutive three-term set
   \[
   \{p,p+1,p+2\}.
   \]
5. the support is not contained in the settled nonconsecutive triple `\{0,1,3\}`.

### Proof

If the reduced support had only one or two active orders, Theorem 4 would force finiteness.
If all active orders had the same parity, Theorem 5 would force finiteness.
If the support lies in a consecutive three-term set `\{p,p+1,p+2\}`, Theorem 8 forces
finiteness.
If the support lies in `\{0,1,3\}`, Theorem 9 forces finiteness.

Therefore any hypothetical infinite-resonance shared profile must have at least three active
orders, must involve both even and odd indices, and must lie beyond all same-parity and
consecutive-three-term sectors, as well as beyond the first settled nonconsecutive triple.

### Research meaning

This is the narrowest unresolved zone reached so far for shared profiles.

The difficult case is no longer “general finite Bessel combinations”. It has been reduced to:

- support size at least three;
- mixed parity;
- outside the completely settled two-term and same-parity sectors;
- outside every consecutive three-term sector `\{p,p+1,p+2\}`;
- outside the settled nonconsecutive triple `\{0,1,3\}`;
- and membership in every exceptional layer
  \[
  \mathscr E_1,\mathscr E_2,\dots.
  \]

That is a substantial reduction of the original problem.

## Complete closure of the shared-profile sector

The preceding sections progressively shrank the possible locus of shared profiles that could
support infinitely many common real resonant parameters. The remaining question is whether the
formal phase-purity criterion can ever hold for a nontrivial shared profile.

It turns out that the answer is no.

### Even and odd Hankel parts

Write the standard formal Hankel amplitude as
\[
H_m(u)=E_m(u)+i\,O_m(u),
\]
where
\[
E_m(u)\in \R[[u^2]],\qquad O_m(u)\in u\,\R[[u^2]].
\]
From the standard Hankel expansion,
\[
H_m(u)
=
\sum_{r\ge 0}
\frac{i^r}{r!\,8^r}
\prod_{j=1}^{r}\bigl(4m^2-(2j-1)^2\bigr)\,u^r,
\]
so
\[
E_m(u)=\sum_{r\ge 0} e_{m,r}u^{2r},
\qquad
e_{m,r}
=
\frac{(-1)^r}{(2r)!\,8^{2r}}
\prod_{j=1}^{2r}\bigl(4m^2-(2j-1)^2\bigr),
\]
and
\[
O_m(u)=\sum_{r\ge 0} o_{m,r}u^{2r+1},
\qquad
o_{m,r}
=
\frac{(-1)^r}{(2r+1)!\,8^{2r+1}}
\prod_{j=1}^{2r+1}\bigl(4m^2-(2j-1)^2\bigr).
\]

For each fixed `r`, the coefficient `e_{m,r}` is a polynomial in `m^2` of exact degree `2r`,
and `o_{m,r}` is a polynomial in `m^2` of exact degree `2r+1`.

### Proposition 10

Let `m_1,\dots,m_s` be distinct nonnegative integers. Then
\[
\{E_{m_1},\dots,E_{m_s}\}
\quad\text{and}\quad
\{O_{m_1},\dots,O_{m_s}\}
\]
are each linearly independent over `\R`.

### Proof

Consider first the family `\{E_{m_j}\}`. If
\[
\sum_{j=1}^s a_j E_{m_j}(u)\equiv 0,
\]
then comparing the coefficients of `u^{2r}` for `0\le r\le s-1` gives
\[
\sum_{j=1}^s a_j e_{m_j,r}=0
\qquad (0\le r\le s-1).
\]
Now `e_{m,r}` is a polynomial in `x=m^2` of exact degree `2r`, so the matrix
\[
\bigl(e_{m_j,r}\bigr)_{0\le r\le s-1,\ 1\le j\le s}
\]
is a generalized Vandermonde matrix: its rows are obtained from the monomials
`1,x^2,\dots,x^{2s-2}` by an invertible upper-triangular change of basis. Since the numbers
`m_1^2,\dots,m_s^2` are distinct, this matrix is nonsingular. Hence all `a_j=0`.

The argument for `\{O_{m_j}\}` is identical: the coefficients `o_{m,r}` are polynomials in
`x=m^2` of exact degrees `1,3,\dots,2s-1`, so the evaluation matrix
\[
\bigl(o_{m_j,r}\bigr)_{0\le r\le s-1,\ 1\le j\le s}
\]
is again a generalized Vandermonde matrix and is therefore nonsingular. Thus any relation
\[
\sum_{j=1}^s a_j O_{m_j}(u)\equiv 0
\]
forces all `a_j=0`.

### Theorem 10

Let
\[
F_b(t)=\sum_{m\in S} c_m J_m(t)
\]
be a nontrivial reduced shared oscillatory profile, with finite support
`S\subset \Z_{\ge 0}`. Assume that at least two distinct positive vertical frequencies are
active in the associated shared-profile family. Then the common real resonant parameter set is
finite.

### Proof

Assume for contradiction that the common real resonant parameter set is infinite. By
Proposition 5, the formal phase-purity criterion holds: there exists `\phi\in\R` such that
\[
e^{-i\phi}\mathcal G_b(u)\in \R[[u]],
\qquad
\mathcal G_b(u):=\sum_{m\in S} c_m (-i)^m H_m(u).
\]

Writing `H_m=E_m+iO_m`, the vanishing of the imaginary part gives
\[
\sum_{m\in S} c_m
\Bigl(
-\sin(\phi+m\pi/2)\,E_m(u)
+\cos(\phi+m\pi/2)\,O_m(u)
\Bigr)=0.
\]
Since the first sum is even in `u` and the second is odd in `u`, they must vanish separately:
\[
\sum_{m\in S} c_m \sin(\phi+m\pi/2)\,E_m(u)=0,
\]
\[
\sum_{m\in S} c_m \cos(\phi+m\pi/2)\,O_m(u)=0.
\]

By Proposition 10, the families `\{E_m\}_{m\in S}` and `\{O_m\}_{m\in S}` are each linearly
independent. Therefore for every active index `m\in S`,
\[
c_m\sin(\phi+m\pi/2)=0,
\qquad
c_m\cos(\phi+m\pi/2)=0.
\]
Hence `c_m=0` for every `m\in S`, contradicting the nontriviality of `F_b`.

So the formal phase-purity criterion can never hold for a nontrivial shared profile, and the
common real resonant parameter set must be finite.

### Corollary 7

Every nontrivial shared-profile multi-frequency family with at least two distinct active
positive vertical frequencies has only finitely many real resonant parameters.

In particular, the shared-profile sector is completely closed: there is no nontrivial shared
profile supporting multi-frequency infinite resonance.

### Meaning

This is a genuine conceptual upgrade over the preceding family-by-family analysis.

The earlier theorems identified many explicit sectors in which multi-frequency infinite
resonance is impossible. The new theorem shows that those examples were not isolated: the
formal phase-purity criterion itself is incompatible with any nontrivial shared profile.

So the shared-profile frontier disappears entirely. The only remaining place where
multi-frequency infinite resonance could still hide is outside the shared-profile sector, in
genuinely non-synchronized finite-band profiles where the active vertical frequencies carry
different `x`-profiles.
