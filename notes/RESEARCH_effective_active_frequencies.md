# Effective Active Frequencies and the Current Resonance Landscape

## Goal

Several different notes now describe complementary parts of the finite-band geometry:

1. a large beta-uniform kernel;
2. a one-frequency trichotomy;
3. complete closure of the shared-profile multi-frequency sector;
4. generic finite resonance on the obstruction quotient in the genuinely non-synchronized case.

The natural synthesis is to isolate the frequencies that actually matter for infinite common
resonance.

## Effective active frequencies

Fix a quotient point
\[
\Xi=\bigl(\Gamma_0,\Gamma_1,\dots,\Gamma_N\bigr)\in\mathcal T_{M,N}.
\]

For `n\ge 1`, call `n` an **effective active frequency** if
\[
\Gamma_n\not\equiv 0.
\]
Automatic kernel frequencies are then exactly the nonzero frequencies with
\[
\Gamma_n\equiv 0.
\]

The point of the definition is simple: a frequency with `\Gamma_n\equiv 0` imposes no resonance
equation at all. Infinite common resonance is governed only by the effective active frequencies.

## Trivial and one-frequency regimes

### Proposition 1

Let `\Xi\in\mathcal T_{M,N}`.

1. If there are no effective active frequencies, then the denominator obstruction vanishes
   identically.
2. If there is exactly one effective active frequency `n_0`, then:
   - if `\Gamma_{n_0}` lies in the asymptotically nonresonant branch, the real resonant
     parameter set is finite;
   - if `\Gamma_{n_0}` lies in the oscillatory-real branch, the real resonant parameter set is
     infinite.

### Proof

If there are no effective active frequencies, all positive-frequency obstruction components
vanish identically. So the quotient point lies entirely in the automatic sector.

Now assume there is exactly one effective active frequency `n_0`. Then the common resonance
equation reduces to the one-frequency equation
\[
\Gamma_{n_0}(n_0 z_0)=0.
\]
The one-frequency trichotomy gives the stated dichotomy between the asymptotically nonresonant
and oscillatory-real branches.

### Corollary 1

Adding any number of automatic-kernel frequencies to a one-frequency oscillatory-real datum does
not destroy infinite resonance.

So the first genuinely nontrivial obstruction to infinite common resonance begins only when
there are at least two effective active frequencies.

## Shared-profile regime

### Proposition 2

Assume there are at least two effective active frequencies and that all of them carry the same
shared reduced profile. Then the real resonant parameter set is finite.

### Proof

This is exactly the complete closure theorem from the shared-profile note.

## Generic non-synchronized regime

### Proposition 3

Assume there are at least two effective active frequencies and the quotient point is genuinely
non-synchronized, so the active frequencies do not all lie on a single shared-profile ray. Then
outside a countable union of proper real-analytic subsets of the quotient stratum, the real
resonant parameter set is finite.

### Proof

This is the generic finite-resonance theorem on the obstruction quotient.

## Current landscape theorem

### Theorem 1

For the finite-band obstruction quotient, the current state of the project is as follows.

1. **Automatic sector.**
   If there are no effective active frequencies, the obstruction vanishes identically.
2. **One effective frequency.**
   Infinite resonance occurs exactly on the oscillatory-real branch of the one-frequency
   trichotomy.
3. **Several effective frequencies, shared profile.**
   Infinite common resonance is impossible.
4. **Several effective frequencies, non-shared profiles.**
   Infinite common resonance, if it exists, is confined to a countable union of proper
   real-analytic bad loci in the finite-dimensional quotient. In particular it is meagre and of
   Lebesgue measure zero on every quotient chart.

### Meaning

This is the cleanest current geometric summary of the project.

Infinite common resonance is no longer a diffuse phenomenon. It has been reduced to the
following hierarchy:

1. it survives freely only in the one-effective-frequency oscillatory-real regime;
2. it is completely ruled out in the shared-profile multi-frequency regime;
3. in the genuinely non-synchronized multi-frequency regime it is already highly nongeneric.

So the true unresolved frontier is now very narrow:

> at least two effective active frequencies, all oscillatory-real, genuinely non-synchronized,
> and lying on one of the thin compatibility strata inside the obstruction quotient.

Equivalently, by the universal-shift-series note, any such configuration must admit a single
formal series
\[
\sigma(v)\in v\R[[v]]
\]
such that every effective active frequency has higher zero-shift series of the form
\[
s_n(u)=n\,\sigma(nu).
\]
So the unresolved sector is governed by one universal normalized shift geometry, not by
independent profiles.

There are now anchored emptiness results in this direction. If one effective active frequency is
the pure vertical profile `J_0`, then a second effective active frequency cannot belong to either
of the low-dimensional nontrivial families
\[
b_0J_0+b_1J_1,
\qquad
b_0J_0+b_1J_1+b_2J_2,
\]
and, more generally, no nontrivial profile supported on `\{0,k\}` can share the same universal
normalized shift series with `J_0`. In particular it cannot belong to any two-term family
\[
b_0J_0+b_kJ_k\qquad (k\ge 1,\ b_0\neq 0),
\]
unless it collapses back to a scalar multiple of `J_0`. So in those first genuinely non-shared
sectors the remaining bad locus is already empty, not merely thin.

More importantly, this is no longer just a list of isolated families. The odd-ladder note now
shows that for every anchored family
\[
J_0+bJ_1+cJ_{2r+1},
\qquad r\ge 1,
\]
the universal quadratic reduction coming from `\lambda_2=0` is followed by exact closure of the
order-`3` and order-`4` residuals. In particular, the entire odd support-three ladder is now
closed: every family
\[
J_0+bJ_1+cJ_{2r+1}
\]
is empty under the anchored universal-shift constraint.

There is now a second global support-three closure of a different type. The new mixed-ladder note
shows that for every anchored family
\[
J_0+bJ_2+cJ_{2r+1},
\qquad r\ge 1,
\]
the anchored equations can be reduced to a parameter-dependent algebraic elimination problem whose
two special branches are explicitly impossible and whose generic branch is excluded by a positive
resultant polynomial in `\mu=4(2r+1)^2`. Consequently the entire ladder
\[
J_0+bJ_2+cJ_{2r+1}
\]
is also empty under the anchored universal-shift constraint.

There is now a third complete support-three ladder as well. The fixed-even-mode note for `J_4`
shows that every anchored family
\[
J_0+bJ_4+cJ_{2r+1},
\qquad r\ge 1,
\]
is empty under the same universal-shift constraint. The proof again runs by a parameter-dependent
elimination theorem, but this time the generic branch is controlled by a seventh-degree
resultant polynomial in `\mu=n^2`, while the exceptional low mode `n=3` is handled by an exact
Groebner basis factor.

There is now a fourth complete support-three ladder too. The note for `J_6` shows that every
anchored family
\[
J_0+bJ_6+cJ_{2r+1},
\qquad r\ge 1,
\]
is empty. Here the generic branch again reduces to a pair of cubic residuals in the profile
parameter `b`, but the decisive final step is even cleaner: the remaining `\mu`-polynomials are
both congruent to odd powers of `\mu` modulo `2`, so they cannot vanish at the relevant odd
squares `\mu=(2r+1)^2`.

The same parity-controlled terminal mechanism now persists for the next five fixed-even ladders.
The notes for `J_8`, `J_{10}`, `J_{12}`, `J_{14}`, and `J_{16}` show that every anchored family
\[
J_0+bJ_m+cJ_{2r+1},
\qquad
m\in\{8,10,12,14,16\},
\qquad
r\ge 1,
\]
is empty under the same universal-shift constraint. In each case the generic branch reduces to a
pair of `\mu`-polynomials, one cubic and one septic, and both are congruent to odd powers of
`\mu` modulo `2`. Since the relevant parameters are odd squares `\mu=(2r+1)^2`, the generic
branch is automatically impossible.

There is now also a conceptual explanation for this parity phenomenon. The note
[RESEARCH_lommel_parity_mechanism.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_lommel_parity_mechanism.md)
shows that in the exact `(J_0,J_1)` recurrence basis, every normalized even mode collapses to
`J_0` modulo `2`, while every normalized odd mode collapses to `J_1` modulo `2`. So the
fixed-even/odd support-three sector has a universal mod-`2` shadow before any elimination is
performed.

From `m=12` onward there is also a visible simplification in the explicit branch geometry: the two
special branches already collapse by uniform order-`2` identities,
\[
b=-1\Longrightarrow \frac{P_2}{d}=2m^2d^2\Bigl(\mu-\frac{m^2}{2}+4\Bigr),
\]
\[
b=-\frac{\mu}{\mu-m^2}\Longrightarrow
\frac{P_2}{d}
=
\frac{m^2\mu}{(\mu-m^2)^2}\Bigl(d^2(\mu-m^2)^2+m^4\Bigr),
\]
so the only remaining obstruction is the generic branch, which is then eliminated by parity.

There is now a stronger, more conceptual synthesis. The new note
[RESEARCH_mixed_parity_second_order_moment_normal_form.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_mixed_parity_second_order_moment_normal_form.md)
shows that the whole anchored mixed-parity sector is governed at second order by six aggregated
moments
\[
(E,O,X,Y,U,V),
\]
or equivalently by three complex moments
\[
z_0=E+iO,\qquad z_1=-Y-iX,\qquad z_2=-V+iU.
\]
The second-order anchored fiber condition is then
\[
2\Re(\overline{z_0}z_2)+q\,\Im(\overline{z_0}z_1)=0,
\qquad q=8\lambda_1>0.
\]
So support size is already invisible at second order beyond these moment aggregates.

Equivalently: once a `J_0` anchor is present, the support-two non-shared anchored sector is
completely closed, the support-three odd-odd sector is completely closed, the support-three
even-odd sector is completely closed, and the support-three even-even sector is completely
closed. The old ladder theorems should now be read as concrete shadows of this broader
fiber-rigidity picture, not as the final form of the result.

So the first genuinely non-shared anchored frontier has moved beyond all support-three families.

## Research meaning

This sharpens the strategic picture considerably.

A deeper reformulation is now available in
[RESEARCH_prufer_moduli_mechanism.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_prufer_moduli_mechanism.md).
There the remaining frontier is recast as a fiber-rigidity problem for a normalized formal
Prüfer map on the obstruction quotient. In that language, the current theorems are no longer a
disconnected list: they are partial injectivity results for that normalized Prüfer map.

The new mixed-parity moment note sharpens this again: for anchored mixed-parity fibers, the
second-order normalized Prüfer map factors through a finite moment map. So the next real problem
is not “compute more support-four families”, but rather:

> understand whether higher normalized Prüfer invariants are rigid once the second-order moment
> identity has been imposed.

This has now been pushed one step farther by
[RESEARCH_mixed_parity_third_order_moment_jets.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_mixed_parity_third_order_moment_jets.md).
Up to third order, the anchored mixed-parity fiber does not see the full support pattern either;
it sees only four complex moments
\[
z_0,\ z_1,\ z_2,\ z_3.
\]
So the support-`\ge 4` frontier has been compressed from an infinite family problem to a finite
jet fiber-rigidity problem.

The new note
[RESEARCH_finite_jet_principle_prufer_map.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_finite_jet_principle_prufer_map.md)
packages this into a general statement: for every finite order `L`, the `L`-jet of the
anchored mixed-parity normalized Prüfer map factors through a finite-dimensional moment-jet map
`\mathfrak m_L`. In other words, no finite-order obstruction can ever see the full support
pattern directly; it can only see finitely many aggregated moments.

There is now a further structural sharpening in
[RESEARCH_central_factorial_lommel_basis.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_central_factorial_lommel_basis.md).
The normalized Lommel coefficient polynomials do form a parity-adapted central-factorial basis
in the squared order. This is now a theorem, not a conjectural pattern. In particular, the
bounded-support anchored problem has been reduced to a generalized Prony reconstruction problem
in a parity-split central-factorial basis, and finite-jet fibers are discrete on every
fixed-support anchored stratum.

This has now been sharpened further in
[RESEARCH_bounded_bandwidth_moment_reconstruction.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_bounded_bandwidth_moment_reconstruction.md).
On every finite even/odd bandwidth window, the `J_1`-channel jet is already globally triangular:
the highest odd power recovers the top even mode, the highest even power recovers the top odd
mode, and descending recursively reconstructs all coefficients. So bounded-bandwidth anchored
profiles admit exact finite-dimensional reconstruction, not just fixed-support discreteness.

There is now a second layer to this bounded-bandwidth picture:
[RESEARCH_bounded_bandwidth_pade_reduction.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_bounded_bandwidth_pade_reduction.md)
shows that sufficiently high normalized Prüfer jets determine the rational phase quotient exactly
by Padé reconstruction. Hence the remaining bounded-bandwidth inverse problem is an
amplitude-lifting problem inside the finite-dimensional central-factorial coefficient space.
The new note
[RESEARCH_boundary_strata_amplitude_thinness.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_boundary_strata_amplitude_thinness.md)
shows that a degree-`s` amplitude-lifting ambiguity is forced onto a codimension-`s`
top-coefficient boundary stratum. So bounded-bandwidth nonuniqueness, if it occurs at all, is
stratified by an explicit boundary filtration and becomes thinner with the degree of the
ambiguity.

There is now a deeper reformulation in
[RESEARCH_boundary_strata_subresultant_geometry.md](/Users/shunhu/Documents/Codes/Lean/RESEARCH_boundary_strata_subresultant_geometry.md).
Nonunique amplitude lifting is exactly the common-factor locus of the normalized phase pair
`(C_F,S_F)`. Hence the residual bounded-bandwidth fibers are controlled by the resultant and its
subresultants:
\[
\mathfrak X_1\supset \mathfrak X_2\supset\cdots,
\]
where `\mathfrak X_s` is the degree-`\ge s` gcd stratum. This upgrades the boundary problem from
“top coefficients vanish” to a canonical real-algebraic gcd stratification problem.

The unresolved problem is no longer “understand multi-frequency resonance” in general. It is:

1. remove the automatic frequencies;
2. ignore the one-effective-frequency regime, which is already completely understood;
3. ignore the shared-profile regime, which is completely closed;
4. attack only the thin non-synchronized compatibility loci.

That is a real reduction of the problem, not a change of language.

## Next step

The next serious target is now twofold.

1. Decide whether the remaining thin non-synchronized bad loci are actually nonempty.
2. Push the new moment-normal-form picture beyond third order, especially into support `\ge 4`.
3. Understand whether the finite jet maps `\mathfrak m_L` are locally injective on natural
   anchored regions.
4. Push the central-factorial theorem from fixed-support discreteness to stronger local or
   global injectivity statements for the finite jet maps on natural anchored regions.

A strong next theorem would be:

> if at least two effective active frequencies are genuinely non-synchronized, then the common
> real resonant parameter set is always finite.

At the moment this is not proved. But the current notes show that any counterexample would have
to live on a very small and explicitly constrained subset of the obstruction quotient.
