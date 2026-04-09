# Generic Finite Resonance on the Finite-Dimensional Obstruction Quotient

## Goal

The obstruction quotient note shows that every finite-band resonance problem factors through the
explicit finite-dimensional Bessel quotient `\mathcal T_{M,N}`. The shared-profile note now
closes one major sector completely: if several active vertical frequencies carry the same
`x`-profile, then infinite common resonance is impossible.

The next natural target is the genuinely non-synchronized case, where different active
frequencies carry different one-frequency obstruction profiles.

The key point is that the one-frequency trichotomy and the multi-frequency compatibility
hierarchy can be combined directly on the quotient. This gives a generic finite-resonance
theorem: outside a countable union of proper real-analytic subsets, a finite-band obstruction
datum admits only finitely many real resonant parameters.

## Quotient strata and active frequencies

Fix bandwidth `(M,N)`. A quotient point in `\mathcal T_{M,N}` is a tuple
\[
\Xi=\bigl(\Gamma_0,\Gamma_1,\dots,\Gamma_N\bigr),
\]
where
\[
\Gamma_n(t)\in
\operatorname{span}_{\R}\{J_0(n t),\dots,J_M(n t),\, iJ_0(n t),\dots,iJ_M(n t)\}
\qquad (1\le n\le N).
\]

Fix a set of active positive frequencies
\[
\mathcal N=\{n_1,\dots,n_s\}\subset\{1,\dots,N\},
\qquad s\ge 2,
\]
and suppose `\Gamma_n\not\equiv 0` for `n\in\mathcal N`.

For each active `n`, the one-frequency recurrence reduction gives complex polynomials
\[
P_n(u),Q_n(u)\in\C[u]
\]
such that
\[
\Gamma_n(t)=P_n(t^{-1})J_0(nt)+Q_n(t^{-1})J_1(nt).
\]
Define
\[
r_n:=\min\{\operatorname{ord}_0 P_n,\operatorname{ord}_0 Q_n\},
\]
and write
\[
P_n(u)=u^{r_n}\widetilde P_n(u),\qquad
Q_n(u)=u^{r_n}\widetilde Q_n(u),
\]
with
\[
\alpha_n:=\widetilde P_n(0),\qquad \beta_n:=\widetilde Q_n(0).
\]
Then `(\alpha_n,\beta_n)\neq(0,0)`.

On each fixed stratum where the integers `r_n` are constant, the leading coefficients
`\alpha_n,\beta_n` depend real-analytically on the quotient coordinates.

## One-frequency oscillatory-real condition

The one-frequency trichotomy says that a nonzero active frequency can contribute infinitely many
real resonant parameters only if its leading oscillatory profile is real after a common phase.
Equivalently,
\[
R_n:=\Im(\overline{\alpha_n}\beta_n)=0.
\]

If `R_n\neq 0`, then
\[
|\Gamma_n(t)|\gg t^{-r_n-\frac12}
\]
for all sufficiently large `t`, so the real zero set of `\Gamma_n` is finite.

Therefore:

### Proposition 1

Fix a quotient stratum with active frequencies `\mathcal N`. If there exists `n\in\mathcal N`
such that
\[
R_n\neq 0,
\]
then the common real resonant parameter set is finite.

### Proof

If the common real resonant parameter set were infinite, then in particular the real zero set of
`\Gamma_n(nt)` would be infinite. This contradicts the asymptotically nonresonant branch of the
one-frequency trichotomy.

## Oscillatory-real chart

Restrict now to a local real-analytic chart on the quotient stratum where all active frequencies
are oscillatory-real:
\[
R_n=0\qquad (n\in\mathcal N).
\]
On such a chart the positive zeros of each active frequency admit asymptotic expansions
\[
t_{n,k}
=
k\pi+\delta_n+\sum_{r=1}^L \lambda_{n,r}(k\pi)^{-r}+O(k^{-L-1})
\]
to every finite order `L`, with `\delta_n,\lambda_{n,r}` real-analytic on the chart.

## First-mismatch finiteness criterion

The compatibility hierarchy can be used in a more concrete way: the first asymptotic order at
which two active frequencies disagree already forces finiteness.

### Proposition 2

Assume all active frequencies are oscillatory-real. Let `m,n\in\mathcal N` be distinct.

1. If
   \[
   n\delta_m-m\delta_n\notin \pi\Z,
   \]
   then the common real resonant parameter set is finite.
2. Suppose
   \[
   n\delta_m-m\delta_n\in \pi\Z.
   \]
   Let `r_*(m,n)\ge 1` be the smallest index such that
   \[
   m^{r+1}\lambda_{n,r}\neq n^{r+1}\lambda_{m,r}.
   \]
   If such an index exists, then the common real resonant parameter set is finite.

### Proof

If infinitely many common resonant parameters existed, the compatibility hierarchy would force
the phase-locking relation
\[
n\delta_m-m\delta_n\in \pi\Z
\]
and every higher-order relation
\[
m^{r+1}\lambda_{n,r}=n^{r+1}\lambda_{m,r}
\qquad (r\ge 1).
\]
So any failure at the first order or at the first higher asymptotic order rules out infinite
common resonance.

### Corollary 1

Assume all active frequencies are oscillatory-real. If there exist two distinct active
frequencies `m,n` such that either

1. the phase-locking relation fails, or
2. their first nonzero higher correction occurs at different orders, or
3. it occurs at the same order `r_*` but
   \[
   m^{r_*+1}\lambda_{n,r_*}\neq n^{r_*+1}\lambda_{m,r_*},
   \]

then the common real resonant parameter set is finite.

### Meaning

This is the usable form of the hierarchy for concrete families. One does not need the whole
infinite tower to prove finiteness: the first asymptotic mismatch already kills multi-frequency
infinite resonance.

## Truncated bad loci

Fix a base frequency `n_1\in\mathcal N`. For each integer vector
\[
\mathbf q=(q_n)_{n\in\mathcal N\setminus\{n_1\}}\in\Z^{s-1},
\]
and each `L\ge 1`, define the truncated bad locus
\[
\mathscr B_{L,\mathbf q}
\]
inside the chart by the equations
\[
R_n=0
\qquad (n\in\mathcal N),
\]
\[
n\delta_{n_1}-n_1\delta_n=q_n\pi
\qquad (n\in\mathcal N\setminus\{n_1\}),
\]
and
\[
n_1^{r+1}\lambda_{n,r}=n^{r+1}\lambda_{n_1,r}
\qquad
(n\in\mathcal N\setminus\{n_1\},\ 1\le r\le L).
\]

### Theorem 1

Fix a quotient stratum with active positive frequencies `\mathcal N` and `s\ge 2`. Then the
subset of quotient points admitting infinitely many common real resonant parameters is contained
in
\[
\bigcup_{\mathbf q\in\Z^{s-1}}\mathscr B_{L,\mathbf q}
\]
for every `L\ge 1`.

### Proof

Assume a quotient point admits infinitely many common real resonant parameters.

By Proposition 1, every active frequency must satisfy `R_n=0`; otherwise one active component
would already have only finitely many real zeros.

Once all active frequencies are oscillatory-real, the asymptotic compatibility hierarchy applies.
For each `n\neq n_1` there exists an integer `q_n` such that
\[
n\delta_{n_1}-n_1\delta_n=q_n\pi,
\]
and for every `1\le r\le L`,
\[
n_1^{r+1}\lambda_{n,r}=n^{r+1}\lambda_{n_1,r}.
\]
So the point belongs to `\mathscr B_{L,\mathbf q}` for the corresponding integer vector
`\mathbf q`.

This proves the containment.

## Generic finiteness

The preceding theorem is stronger than the earlier compatibility statement because it includes
the one-frequency oscillatory-real equations `R_n=0`.

In particular, the candidate infinite-resonance locus must first survive `s` one-frequency
constraints and then, on that thinner chart, satisfy the full multi-frequency hierarchy.

### Proposition 3

On any quotient stratum with at least two active positive frequencies, the infinite common
resonance locus is contained in a countable union of proper real-analytic subsets.

### Proof

By Theorem 1, it is contained in
\[
\bigcup_{\mathbf q\in\Z^{s-1}}\mathscr B_{1,\mathbf q}.
\]
Each `\mathscr B_{1,\mathbf q}` is real-analytic by construction.

It remains to show that these subsets are proper. The equations `R_n=0` are nontrivial, because
the obstruction quotient splits as a direct sum of the one-frequency quotient factors, and on the
`n`th factor the one-frequency note gives explicit obstruction data with `R_n\neq 0`, for instance
\[
J_0(t)+iJ_1(t),
\]
which lies in the full one-frequency image. Since the stratum is obtained by fixing only the
active set and the integers `r_n`, one may vary the `n`th one-frequency factor independently
inside that stratum. Therefore `R_n` is not identically zero there.

Hence no `\mathscr B_{1,\mathbf q}` can coincide with the entire stratum, so each is a proper
real-analytic subset.

### Corollary 2

Outside a countable union of proper real-analytic subsets of the obstruction quotient, every
finite-band obstruction datum with at least two active positive frequencies admits only finitely
many real resonant parameters.

Equivalently, common infinite resonance is nongeneric on every multi-frequency quotient stratum.

### Corollary 3

Fix bandwidth `(M,N)` and a finite-band coefficient stratum with at least two active positive
frequencies. Then the set of cocycles whose exact obstruction datum admits infinitely many
common real resonant parameters is contained in the inverse image of a countable union of proper
real-analytic subsets of the obstruction quotient.

In particular, generic finite-band cocycles in that stratum have only finitely many real
resonant parameters.

### Proof

The obstruction map from the finite-band coefficient space onto the quotient is surjective and
real-linear. Pulling back Corollary 2 gives the claim immediately.

### Corollary 4

On every finite-dimensional quotient chart, and hence on every finite-band coefficient stratum
with at least two active positive frequencies, the infinite common resonance locus is meagre and
has Lebesgue measure zero.

### Proof

A proper real-analytic subset of a finite-dimensional real-analytic manifold has empty interior
and Lebesgue measure zero. Countable unions preserve both properties. Apply this to Corollary 2
on the quotient chart, and then pull back by the real-linear obstruction map for the coefficient
space statement.

## Comparison with the shared-profile theorem

The shared-profile theorem says more in its own sector: there, infinite common resonance is not
merely nongeneric, but impossible.

The present theorem addresses the complementary case. It does not yet prove impossibility for
every non-synchronized multi-frequency configuration, but it does show that:

1. an active frequency must first lie on its own one-frequency oscillatory-real hypersurface;
2. then the different active frequencies must satisfy the full compatibility hierarchy;
3. therefore infinite common resonance is forced into a countable union of thin analytic loci on
   the quotient.

So, after the complete closure of the shared-profile sector, the remaining unresolved geometry is
already highly nongeneric.

## Research meaning

This is the cleanest current synthesis beyond the shared-profile case.

The exact denominator mechanism now yields three distinct geometric layers:

1. the explicit linear kernel `\mathcal K_{M,N}`, where Möbius disjointness is beta-uniform;
2. the shared-profile sector, where multi-frequency infinite resonance is impossible;
3. the genuinely non-synchronized sector, where infinite common resonance can occur, if at all,
   only on a countable union of proper real-analytic bad loci inside the finite-dimensional
   obstruction quotient.

That is already much closer to a true geometric theorem about the original Cesàro Sarnak problem
than a collection of explicit resonant examples.

## Next step

There are now two plausible directions.

1. Strengthen Proposition 2 from “countable union of proper analytic subsets” to a codimension
   statement on suitable quotient charts.
2. Go after the remaining unresolved sector directly and try to prove that these bad loci are in
   fact empty, or at least finite unions of very explicit compatibility strata.

The second direction is the one closest to a genuinely sharp main theorem.
