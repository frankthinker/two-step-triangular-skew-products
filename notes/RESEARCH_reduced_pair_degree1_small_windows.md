# Exact Degree-1 Multiplier-Incidence on the Smallest Bounded Windows

## Goal

The multiplier-incidence framework identifies the correct reduced-pair frontier
\[
\mathcal Y_s(K,L),
\]
but so far this frontier has only been analyzed abstractly.

This note gives the first exact nontrivial classification on the reduced side:

- the smallest window `(1,0)` has only the trivial degree-`1` ambiguity;
- the next window `(1,1)` has a completely explicit degree-`1` ambiguity locus, namely a circle.

So the reduced-pair incidence geometry is not merely thin in these minimal windows; it is
exactly computable.

## 1. The window `(1,0)`

Write
\[
F(t)=aJ_0(t)+b\widetilde J_2(t)+c\widetilde J_1(t),
\qquad
\widetilde J_2(t)=J_0(t)-2uJ_1(t),
\qquad
u=t^{-1}.
\]
Then
\[
A(u)=a+b,
\qquad
B(u)=c-2bu.
\]
Set
\[
x:=A(0)=a+b,
\qquad
y:=B(0)=c,
\qquad
D:=x^2+y^2.
\]
The normalized phase pair
\[
C(u)+iS(u):=\frac{A(u)+iB(u)}{x+iy}
\]
is therefore
\[
C(u)=1-\frac{2by}{D}u,
\qquad
S(u)=-\frac{2bx}{D}u.
\]

### Proposition 1.1

On the window `(1,0)`, every pair
\[
C(u)=1+pu,
\qquad
S(u)=qu
\]
with `p,q\in\mathbb R` is realized by some `F\in\mathcal V_{1,0}`.

### Proof

Take
\[
x:=q,
\qquad
y:=p,
\qquad
b:=-\frac{p^2+q^2}{2}.
\]
Then `D=p^2+q^2`, and
\[
-\frac{2by}{D}=p,
\qquad
-\frac{2bx}{D}=q.
\]
Finally choose `a:=x-b`, `c:=y`.

### Corollary 1.2

The reduced-pair space on `(1,0)` is the full affine plane
\[
\{(1+pu,qu): p,q\in\mathbb R\}.
\]

## 2. The window `(1,1)`

Now write
\[
F(t)=aJ_0(t)+b\widetilde J_2(t)+c\widetilde J_1(t)+d\widetilde J_3(t),
\]
where
\[
\widetilde J_3(t)=-J_3(t)=4uJ_0(t)+(1-8u^2)J_1(t).
\]
Hence
\[
A(u)=a+b+4du,
\qquad
B(u)=c+d-2bu-8du^2.
\]
Set
\[
x:=A(0)=a+b,
\qquad
y:=B(0)=c+d,
\qquad
D:=x^2+y^2,
\]
and introduce
\[
\alpha:=-\frac{2b}{D},
\qquad
\beta:=\frac{4d}{D}.
\]
Then the normalized pair becomes
\[
C(u)=1+(\alpha y+\beta x)u-2\beta yu^2,
\]
\[
S(u)=(\alpha x-\beta y)u-2\beta xu^2.
\]

Write
\[
C(u)=1+c_1u+c_2u^2,
\qquad
S(u)=s_1u+s_2u^2.
\]

### Proposition 2.1

A normalized pair `(C,S)` of degrees `(2,2)` is realized in the window `(1,1)` if and only if
\[
2(c_1s_2-s_1c_2)+c_2^2+s_2^2=0.
\]

### Proof

If `\beta=0`, then `c_2=s_2=0`, so the identity is immediate.

If `\beta\neq 0`, then from
\[
c_2=-2\beta y,
\qquad
s_2=-2\beta x
\]
we recover
\[
x=-\frac{s_2}{2\beta},
\qquad
y=-\frac{c_2}{2\beta}.
\]
Substituting into the formulas for `c_1,s_1` gives
\[
c_1=-\frac{\alpha c_2}{2\beta}-\frac{s_2}{2},
\qquad
s_1=-\frac{\alpha s_2}{2\beta}+\frac{c_2}{2}.
\]
Eliminating `\alpha/\beta` yields exactly
\[
2(c_1s_2-s_1c_2)+c_2^2+s_2^2=0.
\]

Conversely, if `(c_2,s_2)\neq (0,0)` and the displayed identity holds, choose
\[
\beta:=-\frac12,
\qquad
x:=s_2,
\qquad
y:=c_2.
\]
Then `c_2=-2\beta y` and `s_2=-2\beta x`. The same identity is precisely the compatibility
condition for solving the two linear equations for `\alpha`. Thus the pair is realized. If
`(c_2,s_2)=(0,0)`, take `\beta=0` and solve directly for `\alpha`.

So the realized normalized-pair image of `(1,1)` is a quadric hypersurface.

## 3. Exact degree-1 ambiguity from `(1,0)` to `(1,1)`

Take a reduced pair on `(1,0)`:
\[
\widehat C(u)=1+pu,
\qquad
\widehat S(u)=qu.
\]
Consider a degree-`1` multiplier
\[
h(u)=1+tu,
\qquad
t\neq 0.
\]
The lifted pair is
\[
C(u)=(1+tu)(1+pu)=1+(p+t)u+pt\,u^2,
\]
\[
S(u)=(1+tu)(qu)=qu+qt\,u^2.
\]
So
\[
c_1=p+t,\qquad c_2=pt,\qquad s_1=q,\qquad s_2=qt.
\]
Substituting into the quadric identity of \Cref{prop:quadric-11} gives
\[
2\bigl((p+t)(qt)-q(pt)\bigr)+(pt)^2+(qt)^2=0,
\]
hence
\[
t^2\bigl(p^2+(q+1)^2-1\bigr)=0.
\]

### Theorem 3.1

For the reduced-pair space of `(1,0)`, the degree-`1` ambiguity locus into the window `(1,1)` is
exactly the circle
\[
\mathcal Y_1^{(1,0)\to(1,1)}
=
\{(p,q)\in\mathbb R^2: p^2+(q+1)^2=1\}.
\]

Equivalently, a reduced pair
\[
\widehat C(u)=1+pu,
\qquad
\widehat S(u)=qu
\]
admits a nontrivial degree-`1` multiplier lift into `(1,1)` if and only if
\[
p^2+(q+1)^2=1.
\]

### Proof

Necessity is the computation above, using the quadric equation from Proposition 2.1.

For sufficiency, if the circle identity holds and `t\neq 0`, then the lifted coefficients satisfy
the quadric equation of Proposition 2.1. Hence the lifted pair is realized in `(1,1)`.

In particular, the zero phase point `(p,q)=(0,0)` is not isolated: it lies on the same circle.

## 4. Research meaning

This is the first exact reduced-side multiplier-incidence classification.

The outcome is strikingly rigid:

- on `(1,0)`, the reduced phase-pair space is completely free;
- on `(1,1)`, the realized normalized-pair image is a quadric;
- degree-`1` ambiguity from `(1,0)` to `(1,1)` is therefore cut out by a single circle.

So the multiplier-incidence geometry is not merely thin in the smallest windows. It has exact
projective geometry already at the first nontrivial level.

More conceptually, the circle appears because the `(1,1)` image is quadratic while the
degree-`1` multiplier ansatz is affine in `(p,q,t)`. Eliminating the multiplier parameter `t`
therefore leaves a single conic on the reduced-pair side. In this smallest nontrivial window,
the first multiplier-incidence locus is literally a projective conic.
