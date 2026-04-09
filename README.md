# Exact Denominator Asymptotics, Finite-Jet Rigidity, and Möbius Disjointness

This repository contains the current paper draft and the core research notes for a project on the original Cesàro form of Sarnak's conjecture for a class of two-step triangular skew products.

## Main paper

- [paper.tex](paper.tex)
- [paper.pdf](paper.pdf)

## Core contribution

The paper develops a model-specific but explicit mechanism for
\[
T_h(x,y,z)=(x+\alpha,\ y+\beta\sin(2\pi x),\ z+h(x,y))
\]
on `\mathbb T^3`.

The central point is not a new abstract criterion. It is an explicit denominator-scale analysis:

- exact denominator asymptotics for the top cocycle blocks along the continued-fraction denominators;
- a finite Bessel obstruction vector controlling the main term;
- quantitative rigidity on the resonant variety, leading to original Cesàro Möbius disjointness;
- a finite-dimensional obstruction quotient with explicit geometric consequences;
- a finite-jet rigidity framework based on a parity-adapted central-factorial basis for the normalized Lommel coefficients.

At the current stage, the paper closes the anchored support-two and support-three sectors, proves generic thinness for the remaining multi-frequency quotient strata, and reduces the bounded-bandwidth frontier to an amplitude-lifting problem controlled by Padé reconstruction and boundary gcd strata.

## Why this is distinctive

The novelty is not “one more Möbius disjointness example”. The novelty is that, for this two-step model, the denominator-scale obstruction can be written down explicitly and then pushed into a concrete geometry and finite-jet rigidity theory.

This gives a visibly structured route:

1. exact denominator law;
2. obstruction geometry;
3. resonant rigidity and Möbius disjointness;
4. finite-jet / bounded-bandwidth rigidity.

## Repository layout

- `paper.tex`, `paper.pdf`: current submission draft.
- `notes/`: research notes that directly support the paper's present theorem package and current frontier.

## Current frontier

The main open direction kept in this repository is no longer support-by-support elimination. It is the bounded-bandwidth amplitude-lifting problem for normalized Prüfer fibers, especially the resultant/subresultant geometry of the lower-degree boundary strata.
