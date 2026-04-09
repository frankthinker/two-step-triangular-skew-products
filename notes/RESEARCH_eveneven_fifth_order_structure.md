# Structure of the Fifth-Order Residual in the Anchored Even-Even Sector

## Goal

The previous note reduced the anchored even-even support-three sector to a unique third-order
candidate curve and a single fifth-order residual polynomial
\[
\mathcal P_{M,N}(q).
\]

This note records the first global structural information about that residual. The point is not
to solve it completely yet, but to show that it already carries nontrivial large-scale geometry.

## 1. The residual polynomial

For distinct even squares
\[
M:=m^2,
\qquad
N:=n^2,
\]
the fifth-order anchored residual has the form
\[
\lambda_5(F)-\frac{13}{1536}q^3
=
\frac{-q\,\mathcal P_{M,N}(q)}{491520\,(4M+4N+3q-32)}.
\]

The polynomial `\mathcal P_{M,N}(q)` has degree `5` in `q`:
\[
\mathcal P_{M,N}(q)=q^5+c_4(M,N)q^4+c_3(M,N)q^3+c_2(M,N)q^2+c_1(M,N)q+c_0(M,N).
\]

It is symmetric in `(M,N)`.

The first three coefficients are
\[
c_4(M,N)=8(M+N)-564,
\]
\[
c_3(M,N)=20(M^2+3MN+N^2)-2640(M+N)-18000,
\]
\[
c_2(M,N)=16(M^3+N^3)+136MN(M+N)-3120(M^2+N^2)-10000MN+100608(M+N)-564480.
\]

## 2. The constant term factorization

The constant term factorizes exactly:
\[
c_0(M,N)=128(M-4)^2(N-4)^2(M+N-32).
\]

This already has geometric meaning.

### Consequences

1. The modes `M=4` or `N=4` are double-boundary points of the fifth-order residual.
2. The first interior threshold appears at
   \[
   M+N=32.
   \]
3. For all even-even sectors with
   \[
   M>4,\qquad N>4,\qquad M+N>32,
   \]
   the residual starts positive at `q=0`.

So the fifth-order geometry is already detecting the boundary between the lowest even modes and
the genuinely large-even regime.

## 3. First-order coefficient at the boundary

The coefficient of `q` is
\[
\begin{aligned}
c_1(M,N)
&=
96M^3N-1984M^3+256M^2N^2-7104M^2N+81920M^2\\
&\quad
+96MN^3-7104MN^2+140288MN-1068032M\\
&\quad
-1984N^3+81920N^2-1068032N+4726784.
\end{aligned}
\]

This polynomial does not factor globally over `\mathbb Z[M,N]`, but on the boundary `M=4` one
gets a complete factorization:
\[
c_1(4,N)=-1600\,(N-16)^2(N-4),
\]
and symmetrically
\[
c_1(M,4)=-1600\,(M-16)^2(M-4).
\]

So when one mode is the lowest even mode `2`, the first nonzero coefficient after the vanishing
constant term is again highly structured: it detects a second threshold at `16`.

## 4. Why this matters

The fifth-order residual is not behaving like a random family of quintics.

It already shows three global features:

1. symmetry in `(M,N)`;
2. explicit boundary factors at `M=4` and `N=4`;
3. a large-even threshold `M+N=32`.

This suggests that the eventual even-even rigidity theorem should not be phrased as a list of
mode pairs. It should separate:

- a boundary regime involving the lowest even modes;
- an interior regime where `M,N>4` and `M+N` is already beyond the threshold `32`.

## 5. Research meaning

The support-three frontier is now organized as follows.

- even-odd: excluded at second order;
- odd-odd: excluded at second order;
- even-even: reduced to a unique third-order candidate curve and a structured fifth-order
  polynomial family.

So the next serious theorem should probably be a large-even statement of the form:

> if `M,N` are distinct even squares in the interior regime, then `\mathcal P_{M,N}(q)>0` for
> all `q>0`.

That would remove the whole large-even support-three frontier in one shot.
