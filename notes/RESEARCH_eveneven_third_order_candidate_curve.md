# Third-Order Candidate Curve in the Anchored Even-Even Support-Three Sector

## Goal

The new second-order rigidity theorems show that both the even-odd and the odd-odd anchored
support-three sectors are already excluded at low order. This leaves only the even-even
support-three sector as the first genuinely open anchored support-three frontier.

This note identifies its exact low-order geometry:

> in the anchored even-even support-three sector, the order-$1$ and order-$3$ conditions reduce
> the genuinely support-three branch to a unique one-parameter candidate curve, and the next
> obstruction is a single explicit fifth-order residual polynomial.

So even here the problem is no longer two-dimensional after low-order normalization.

## 1. Setup

Let `m,n` be distinct even positive integers, and normalize signs by
\[
\widetilde J_m:=(-1)^{m/2}J_m,
\qquad
\widetilde J_n:=(-1)^{n/2}J_n.
\]

Consider the profile
\[
F(t)=J_0(t)+b\widetilde J_m(t)+c\widetilde J_n(t),
\]
and write
\[
M:=m^2,
\qquad
N:=n^2.
\]

Using the exact Lommel recurrence in the `(J_0,J_1)` basis, one obtains the normalized even-mode
expansions
\[
\widetilde J_\ell(t)
=
\Bigl(1-\frac{\ell^2(\ell^2-4)}{8}u^2
+\frac{\ell^2(\ell^2-4)^2(\ell^2-16)}{384}u^4+O(u^6)\Bigr)J_0(t)
\]
\[
\qquad\qquad
+\Bigl(-\frac{\ell^2}{2}u+\frac{\ell^2(\ell^2-4)^2}{48}u^3
-\frac{\ell^2(\ell^2-4)^2(\ell^2-16)^2}{3840}u^5+O(u^7)\Bigr)J_1(t),
\qquad
u=t^{-1}.
\]

Hence
\[
F(t)=A(u)J_0(t)+B(u)J_1(t),
\]
with
\[
A(u)=A_0+A_2u^2+A_4u^4+O(u^6),
\qquad
B(u)=B_1u+B_3u^3+B_5u^5+O(u^7),
\]
where
\[
A_0=1+b+c,
\]
\[
A_2=-\frac{M(M-4)b+N(N-4)c}{8},
\qquad
A_4=\frac{M(M-4)^2(M-16)b+N(N-4)^2(N-16)c}{384},
\]
\[
B_1=-\frac{Mb+Nc}{2},
\qquad
B_3=\frac{M(M-4)^2b+N(N-4)^2c}{48},
\]
\[
B_5=-\frac{M(M-4)^2(M-16)^2b+N(N-4)^2(N-16)^2c}{3840}.
\]

## 2. General odd-order Prüfer coefficients

For a profile of the form
\[
A(u)=A_0+A_2u^2+A_4u^4+O(u^6),
\qquad
B(u)=B_1u+B_3u^3+B_5u^5+O(u^7),
\]
the zero-shift series
\[
\delta=\lambda_1u+\lambda_3u^3+\lambda_5u^5+O(u^7)
\]
satisfies
\[
\lambda_1=\frac{B_1}{A_0},
\]
\[
\lambda_3=
\frac{A_0^2B_3-A_0A_2B_1-\frac13 B_1^3}{A_0^3},
\]
\[
\lambda_5=
\frac{A_0^4B_5-A_0^3(A_2B_3+A_4B_1)+A_0^2B_1(A_2^2-B_1B_3)+A_0A_2B_1^3+\frac15 B_1^5}
{A_0^5}.
\]

Applying these identities to the coefficients above gives the complete low-order Pr\"ufer data for
the even-even sector.

## 3. Two adapted coordinates

Introduce the linear coordinates
\[
U:=b+c,
\qquad
D:=Mb+Nc.
\]
Then
\[
b=\frac{D-NU}{M-N},
\qquad
c=\frac{MU-D}{M-N}.
\]

In these coordinates the first and third invariants simplify dramatically.

### Proposition

For the anchored even-even support-three profile above one has
\[
\lambda_1(F)=-\frac{D}{2(U+1)},
\]
and
\[
\lambda_3(F)
=
\frac{\mathcal L_{M,N}(U,D)}{48(U+1)^3},
\]
where `\mathcal L_{M,N}` is the explicit cubic polynomial
\[
\begin{aligned}
\mathcal L_{M,N}(U,D)
&=
2D^3
-3D^2M(U+1)
-3D^2N(U+1)
+12D^2(U+1)\\
&\quad
+D M^2(U+1)^2
+D N^2(U+1)^2
+D M N(4U^2+5U+1)\\
&\quad
-8D(M+N)(U+1)^2
+16D(U+1)^2\\
&\quad
-MN(M+N-8)U(U+1)^2.
\end{aligned}
\]

## 4. The third-order candidate curve

For an anchored common infinite-resonance configuration one must have
\[
q:=8\lambda_1(F)>0,
\qquad
\lambda_3(F)=-\frac{25}{384}q^2.
\]

The first equation gives
\[
D=-\frac{q(U+1)}{4}.
\]
Substituting this into the second collapses the cubic equation to a linear one in `U`:
\[
R_3(U;q)=0,
\]
where
\[
R_3(U;q)
=
\frac{\mathcal A_{M,N}(q)\,U+\mathcal B_{M,N}(q)}{1536(U+1)},
\]
with
\[
\mathcal A_{M,N}(q)
=
-32M^2N-8M^2q-32MN^2-32MNq+256MN
-6Mq^2+64Mq
\]
\[
\qquad
-8N^2q-6Nq^2+64Nq-q^3+124q^2-128q,
\]
\[
\mathcal B_{M,N}(q)
=
-q\bigl(8M^2+8MN+6Mq-64M+8N^2+6Nq-64N+q^2-124q+128\bigr).
\]

Therefore there is a unique third-order candidate:
\[
U=U(q):=-\frac{\mathcal B_{M,N}(q)}{\mathcal A_{M,N}(q)}.
\]

Equivalently,
\[
U(q)=
-q\,
\frac{8M^2+8MN+6Mq-64M+8N^2+6Nq-64N+q^2-124q+128}
{32M^2N+8M^2q+32MN^2+32MNq-256MN+6Mq^2-64Mq+8N^2q+6Nq^2-64Nq+q^3-124q^2+128q}.
\]

So the genuinely support-three even-even sector is already one-dimensional at order `3`.

## 5. The next obstruction is one variable

Substituting `D=-q(U+1)/4` into the fifth-order coefficient and then restricting to the
third-order candidate `U=U(q)` produces a single residual:
\[
R_5(q)=0.
\]

More precisely,
\[
\lambda_5(F)-\frac{13}{1536}q^3
=
\frac{-q\,\mathcal P_{M,N}(q)}{491520\,(4M+4N+3q-32)},
\]
where `\mathcal P_{M,N}(q)` is an explicit polynomial in `q` of degree `5`, whose coefficients
are polynomial in `(M,N)`.

The first few terms are
\[
\begin{aligned}
\mathcal P_{M,N}(q)
&=
128M^3N^2+128M^2N^3\\
&\quad
+(96M^3N+256M^2N^2+96MN^3)q\\
&\quad
+(16M^3+136M^2N+136MN^2+16N^3)q^2\\
&\quad
+\cdots+q^5.
\end{aligned}
\]

Since
\[
4M+4N+3q-32>0
\]
for even `m,n\ge 2` and `q>0`, the fifth-order anchored compatibility problem is now reduced to
a single numerator polynomial:
\[
\mathcal P_{M,N}(q)=0.
\]

## 6. Meaning

This is the exact analogue, for the even-even sector, of the second-order M\"obius reduction in
the even-odd sector.

The upshot is:

1. the even-even anchored support-three frontier is not two-dimensional after low-order
   normalization;
2. it is already reduced to a unique third-order candidate curve `q\mapsto(U(q),D(q))`;
3. the next obstruction is a single one-variable fifth-order residual polynomial.

So the real remaining problem is no longer “classify all even-even support-three profiles”. It
is:

> understand the sign and zero set of the family of fifth-order residual polynomials
> `\mathcal P_{M,N}(q)`.

This is the natural next step toward a full local fiber-rigidity theorem beyond support size
three.
