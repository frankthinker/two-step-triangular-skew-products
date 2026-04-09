# Degree-1 Multiplier-Incidence on the Window `(2,1)`

## Goal

The previous note
[RESEARCH_reduced_pair_degree1_small_windows.md](/Users/shunhu/Documents/Codes/Lean/notes/RESEARCH_reduced_pair_degree1_small_windows.md)
showed that on the reduced-pair side,

- `(1,0)` is completely free;
- `(1,1)` cuts out an exact circle of degree-`1` ambiguity.

This note pushes the same question one window farther. The outcome is unexpectedly strong:

> every reduced normalized pair realized in `(1,1)` admits a nontrivial degree-`1` lift into
> `(2,1)`.

So the first multiplier-incidence locus on `(2,1)` is not thin at all: it is the whole reduced
image from the previous window.

## 1. The window `(2,1)`

Write
\[
F(t)
=
aJ_0(t)+b\widetilde J_2(t)+e\widetilde J_4(t)+c\widetilde J_1(t)+d\widetilde J_3(t).
\]
Using
\[
\widetilde J_2(t)=J_0(t)-2uJ_1(t),
\]
\[
\widetilde J_3(t)=4uJ_0(t)+(1-8u^2)J_1(t),
\]
\[
\widetilde J_4(t)=(1-32u^2)J_0(t)+(64u^3-10u)J_1(t),
\]
we obtain
\[
A(u)=a+b+e+4du-32eu^2,
\]
\[
B(u)=c+d+(-2b-10e)u-8du^2+64eu^3.
\]

Set
\[
x:=A(0),\qquad y:=B(0),\qquad D:=x^2+y^2,
\]
and introduce normalized parameters
\[
\alpha:=\frac{-2b-10e}{D},
\qquad
\beta:=\frac{4d}{D},
\qquad
\gamma:=\frac{32e}{D}.
\]
Then the normalized pair
\[
C(u)+iS(u):=\frac{A(u)+iB(u)}{x+iy}
\]
has the form
\[
C(u)=1+(\alpha y+\beta x)u+(-2\beta y-\gamma x)u^2+2\gamma y\,u^3,
\]
\[
S(u)=(\alpha x-\beta y)u+(-2\beta x+\gamma y)u^2+2\gamma x\,u^3.
\]

Write
\[
C(u)=1+c_1u+c_2u^2+c_3u^3,
\qquad
S(u)=s_1u+s_2u^2+s_3u^3.
\]

## 2. The exact normalized-pair image of `(2,1)`

### Proposition 2.1

A sextuple `(c_1,c_2,c_3,s_1,s_2,s_3)` is realized by the window `(2,1)` if and only if
\[
2(c_2s_3-s_2c_3)+c_3^2+s_3^2=0.
\]

### Proof

Necessity is immediate from the displayed formulas above:
\[
c_3=2\gamma y,
\qquad
s_3=2\gamma x,
\]
\[
c_2=-2\beta y-\gamma x,
\qquad
s_2=-2\beta x+\gamma y,
\]
and therefore
\[
2(c_2s_3-s_2c_3)+c_3^2+s_3^2=0
\]
identically.

For sufficiency, first consider `(c_3,s_3)\neq (0,0)`. Choose a nonzero `\gamma` and set
\[
x:=\frac{s_3}{2\gamma},
\qquad
y:=\frac{c_3}{2\gamma}.
\]
Then the equations for `c_2,s_2` become
\[
c_2=-\frac{\beta c_3}{\gamma}-\frac{s_3}{2},
\qquad
s_2=-\frac{\beta s_3}{\gamma}+\frac{c_3}{2}.
\]
The displayed quadric is exactly the compatibility condition for solving `\beta`.

Once `\beta` is fixed, the equations for `c_1,s_1`
\[
2\gamma c_1=\alpha c_3+\beta s_3,
\qquad
2\gamma s_1=\alpha s_3-\beta c_3
\]
solve uniquely for `\alpha`.

If `(c_3,s_3)=(0,0)`, take `\gamma=0`; then the same formulas reduce to the `(1,1)` case and
can be solved directly.

So the normalized-pair image of `(2,1)` is exactly the single quadric above.

## 3. Degree-1 lifts from `(1,1)`

Take a reduced normalized pair realized in `(1,1)`:
\[
\widehat C(u)=1+c_1u+c_2u^2,
\qquad
\widehat S(u)=s_1u+s_2u^2,
\]
with the quadric relation
\[
2(c_1s_2-s_1c_2)+c_2^2+s_2^2=0.
\]
Now multiply by
\[
h(u)=1+tu,
\qquad
t\neq 0.
\]
The lifted coefficients are
\[
C(u)=1+(c_1+t)u+(c_2+tc_1)u^2+tc_2\,u^3,
\]
\[
S(u)=s_1u+(s_2+ts_1)u^2+ts_2\,u^3.
\]
So
\[
c_3'=tc_2,
\qquad
s_3'=ts_2,
\qquad
c_2'=c_2+tc_1,
\qquad
s_2'=s_2+ts_1.
\]
Substituting into the `(2,1)` quadric gives
\[
2(c_2's_3'-s_2'c_3')+(c_3')^2+(s_3')^2
=
t^2\bigl(2(c_1s_2-s_1c_2)+c_2^2+s_2^2\bigr)=0.
\]

### Theorem 3.1

Every reduced normalized pair realized in `(1,1)` admits a degree-`1` multiplier lift into the
window `(2,1)`.

Equivalently,
\[
\mathcal Y_1(2,1)
\]
is the entire reduced normalized-pair image of `(1,1)`.

### Proof

The computation above shows that after multiplication by `1+tu`, the lifted coefficients satisfy
the exact quadric of Proposition 2.1. Hence the lifted pair is realized in `(2,1)`.

## 4. Research meaning

This is the first place where the multiplier-incidence geometry changes character.

For `(1,1)`, the degree-`1` ambiguity locus is a circle on the reduced side. For `(2,1)`, the
same degree-`1` ambiguity is no longer thin: it fills the entire reduced image from the previous
window.

So the bounded-bandwidth frontier now has two sharply different regimes:

- a first conic reduced-side ambiguity at `(1,1)`;
- a full degree-`1` incidence saturation at `(2,1)`.

This strongly suggests that the small-window incidence problem is not monotone. Instead it has a
window-by-window projective geometry that must be classified in its own right.
