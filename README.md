# Angular Amplitude Reduction — The $J_3$ Split as Accumulated Oriented Symplectic Area

J. Beau, Independent Researcher, France

## Status

Working note (preprint), v1.3 (local candidate, not deposited; last deposited version 1.2). DOI: [10.5281/zenodo.20601228](https://doi.org/10.5281/zenodo.20601228)

## Abstract

This internal note fixes the numerical observable for the absolute normalisation of the angular
generation split of Q14 §6, before any Weil–BFS computation is written.

A short Baker–Campbell–Hausdorff reduction in $\mathfrak{sl}_2$ identifies the per-step
$J_\Pi$-odd $J_3$ component of the metaplectic cascade generator with the oriented product $ts$ of
the two shear parameters, produced by the $\mathfrak{sl}_2$ commutator $[E,F]=H$ (Q14,
Proposition 6.5), and not with a free shear parameter; the Heisenberg bracket does not enter. The
observable proposed for the Weil–BFS cascade is the accumulated oriented central-phase increment
$A_c$ of the Heisenberg lift, normalised by the projected capacity $\widehat{I}(n)$. That $A_c$
carries the $J_3$ signal is an input of this note, not a consequence of the reduction: the increment
$ts$ and the Heisenberg cocycle have the same form, which is an analogy and not an identification.
Under this input, at the intrinsic saturation rank $n_3^{\mathrm{obs}}$ the normalised increment
equals $\varepsilon_{\mathrm{Weil}}(n_3^{\mathrm{obs}})$, to be compared with the dictionary value
$\varepsilon = \tfrac{1}{10}$ *without fitting*.

In the O12 construction the two sectors are the two terms of the fingerprint exponent: the
frequency $B_c$ carries the radial capacity $\sigma_c$, and the central phase $A_c$ is, under that
input, the carrier of the angular split. A direct evaluation on symmetric BFS shells returns
$\Theta_{\mathrm{raw}} = 0$ identically: the symmetric capacity data fix the radial sector but
cannot select an oriented angular branch, so the orientation prescription is an irreducible input
prior to $\mathcal{N}_A$.

## Position in the programme

This note belongs to the **fermionic matter sub-programme** (Presentation Note 6). It is a
companion note to Q14, refining the §6 open deliverable on the inter-generation splitting
amplitude. It identifies, before computation, the precise Weil–BFS observable to be measured to
test the dictionary value $\varepsilon = 1/10$. Together with the **projective-residue-schur**
note (Schur form of the compression remainder, conditional generation reading and A4 reduction) and the
**q11-oriented-frontier** note (front diagnostics), it sets up the locked frame in which the
remaining quantitative step of the fermionic sector can be carried out.

## Compilation

```bash
bash compile.sh
```

Runs `pdflatex → bibtex → pdflatex → pdflatex` on `tex/AngularAmplitudeReduction.tex` and
produces `out/AngularAmplitudeReduction.pdf`.
