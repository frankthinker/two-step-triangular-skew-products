# The Realized Quadratic Prüfer Map and Transverse Rigidity Along the Zero-Phase Line

## Goal

The realized-side bounded-bandwidth frontier is not governed by a linear determinant map.

The normalization of a profile by its own basepoint value makes the realized quotient map
quadratic. This note records the correct object and the first genuine local rigidity theorem for
it.

The main outcome is:

> the realized map has a universal zero-phase projective line `\mathbb P\langle J_0,J_1\rangle`,
> and along this line the only infinitesimal fiber directions are the obvious ones tangent to that
> line itself.

So although the realized map is not globally linear, it is already transversely rigid along its
most obvious positive-dimensional fiber.

## 1. The correct realized quotient map

Fix a bounded bandwidth window `\mathcal W_{K,L}` of realized pairs `(A,B)`.

For
\[
x=(A,B)\in\mathcal W_{K,L},
\]
write
\[
a:=A(0),\qquad b:=B(0),
\qquad z_0:=a+ib.
\]

The normalized phase pair is
\[
C_x(u)+iS_x(u):=\frac{A(u)+iB(u)}{a+ib},
\]
so explicitly
\[
C_x(u)=\frac{aA(u)+bB(u)}{a^2+b^2},
\qquad
S_x(u)=\frac{aB(u)-bA(u)}{a^2+b^2}.
\]

Hence the normalized realized phase quotient is
\[
R_x(u)=\frac{S_x(u)}{C_x(u)}
=
\frac{Q_x(u)}{P_x(u)},
\]
where
\[
P_x(u):=aA(u)+bB(u),
\qquad
Q_x(u):=aB(u)-bA(u).
\]

This defines the **self-normalized quadratic Prüfer map**
\[
\Psi_{K,L}: \mathbb P(\mathcal W_{K,L}) \dashrightarrow \mathbb P(\mathcal R_{K,L}),
\qquad
[x]\longmapsto [P_x:Q_x].
\]

It is quadratic in the projective coordinates of `x`.

## 2. The zero-phase line

The most basic family is
\[
x_\lambda:=J_0+\lambda J_1,
\qquad \lambda\in\mathbb R.
\]

For this family,
\[
A(u)\equiv 1,\qquad B(u)\equiv \lambda,
\]
so
\[
P_{x_\lambda}(u)=1+\lambda^2,
\qquad
Q_{x_\lambda}(u)=0.
\]

Therefore every point of the projective line
\[
\mathbb P\langle J_0,J_1\rangle
\]
maps to the same phase quotient `R\equiv 0`.

### Proposition 2.1

The line
\[
\mathcal L_0:=\mathbb P\langle J_0,J_1\rangle
\subset \mathbb P(\mathcal W_{K,L})
\]
is contained in a single realized fiber of `\Psi_{K,L}`.

So realized bounded-bandwidth uniqueness is false globally on every window containing
`J_0,J_1`.

## 3. Linearization along the zero-phase line

The right question is therefore not global injectivity, but transverse rigidity along
`\mathcal L_0`.

Fix `\lambda\neq 0` and let
\[
x_\lambda=J_0+\lambda J_1.
\]
For a variation
\[
y=(A_y,B_y)\in\mathcal W_{K,L},
\]
write
\[
\alpha:=A_y(0),\qquad \beta:=B_y(0).
\]

Since `R_{x_\lambda}=0`, the differential of `\Psi_{K,L}` at `x_\lambda` is obtained by
linearizing `Q_x/P_x` around `Q=0`, `P=1+\lambda^2`. This gives
\[
D\Psi_{x_\lambda}(y)
=
\frac{1}{1+\lambda^2}
\Bigl(
B_y(u)-\beta-\lambda\bigl(A_y(u)-\alpha\bigr)
\Bigr).
\]

So the derivative depends only on the positive-order part of `B_y-\lambda A_y`.

## 4. Transverse rigidity theorem

The central-factorial basis theorem now enters in the cleanest possible way.

For normalized modes:

- `J_0` contributes only a constant to `A`;
- `J_1` contributes only a constant to `B`;
- each even mode `\widetilde J_{2k}` contributes a highest odd power `u^{2k-1}` to `B`;
- each odd mode `\widetilde J_{2\ell+1}` with `\ell\ge 1` contributes a highest even power
  `u^{2\ell}` to `B`.

After subtracting the constants `\alpha,\beta`, these highest terms survive unchanged.

### Theorem 4.1

For every bounded bandwidth window `(K,L)` and every `\lambda\neq 0`, the kernel of the
differential of the realized quadratic Prüfer map at `x_\lambda` is exactly
\[
\ker D\Psi_{x_\lambda}

=
\operatorname{span}\{J_0,J_1\}.
\]

Equivalently, the realized phase map is transversely injective along the zero-phase line
`\mathcal L_0`.

### Proof

The directions `J_0` and `J_1` lie in the kernel because they vary the point inside the line
`\mathcal L_0`, along which the quotient is identically zero.

Now let `y` be any variation involving some normalized mode of order at least `2`.

- If `y` contains an even mode `\widetilde J_{2k}`, then
  \[
  B_y(u)-\beta-\lambda(A_y(u)-\alpha)
  \]
  has highest term equal to the highest term of `\widetilde B_{2k}(u)`, namely degree `2k-1`
  with nonzero coefficient.

- If `y` contains an odd mode `\widetilde J_{2\ell+1}` with `\ell\ge 1`, then the same
  expression has highest term equal to the highest term of `\widetilde B_{2\ell+1}(u)-1`,
  namely degree `2\ell` with nonzero coefficient.

These leading degrees are all distinct across the normalized basis. Hence no nontrivial linear
combination of higher modes can lie in the kernel. Therefore the only kernel directions are the
two obvious ones `J_0,J_1`.

## 5. Research meaning

This is the first correct local theorem on the realized side.

It says:

1. the realized quotient map is inherently quadratic;
2. it has an unavoidable positive-dimensional fiber, namely the zero-phase line;
3. but that fiber is not floppy in transverse directions: the map is infinitesimally rigid
   modulo the obvious tangent directions.

So the next realized-side frontier is no longer “is the map generically injective?” That was the
wrong global question.

The right questions are:

- what are the genuine global fibers beyond the zero-phase line?
- is the zero-phase line the only positive-dimensional family in natural bounded windows?
- how does this transverse rigidity interact with the reduced-pair multiplier-incidence strata?
