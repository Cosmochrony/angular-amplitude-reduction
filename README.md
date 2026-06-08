# Angular Amplitude Reduction — The $J_3$ Split as Accumulated Oriented Symplectic Area

J. Beau, Independent Researcher, France

## Status

Working note (preprint), v1.0.

## Abstract

This internal note fixes the numerical observable for the absolute normalisation of the angular
generation split of Q14 §6, before any Weil–BFS computation is written.

A short Baker–Campbell–Hausdorff reduction identifies the per-step $J_\Pi$-odd $J_3$ component
of the metaplectic cascade generator with the oriented symplectic area swept per step — the
central, Carnot-degree-2 increment of $\mathrm{Heis}_3$ — and not with a free shear parameter.
The quantity to be measured is therefore the accumulated oriented $J_3$-odd area along the
Weil–BFS cascade, normalised by the projected capacity $\widehat{I}(n)$; at the intrinsic
saturation rank $n_3^{\mathrm{obs}}$ this equals
$\varepsilon_{\mathrm{Weil}}(n_3^{\mathrm{obs}})$, to be compared with the dictionary value
$\varepsilon = \tfrac{1}{10}$ *without fitting*.

In the O12 construction the two sectors are the two terms of the fingerprint exponent: the
frequency $B_c$ carries the radial capacity $\sigma_c$, the central phase $A_c$ carries the
angular split. A direct evaluation on symmetric BFS shells returns $\Theta_{\mathrm{raw}} = 0$
identically: the symmetric capacity data fix the radial sector but cannot select an oriented
angular branch, so the orientation prescription is an irreducible input prior to
$\mathcal{N}_A$.

## Position in the programme

This note belongs to the **fermionic matter sub-programme** (Presentation Note 6). It is a
companion note to Q14, refining the §6 open deliverable on the inter-generation splitting
amplitude. It identifies, before computation, the precise Weil–BFS observable to be measured to
test the dictionary value $\varepsilon = 1/10$. Together with the **projective-residue-schur**
note (Schur form of $E_\Pi$, A4 stratification, finite/Lorentzian separation) and the
**q11-oriented-frontier** note (front diagnostics), it sets up the locked frame in which the
remaining quantitative step of the fermionic sector can be carried out.

## Compilation

```bash
bash compile.sh
```

Runs `pdflatex → bibtex → pdflatex → pdflatex` on `tex/AngularAmplitudeReduction.tex` and
produces `out/AngularAmplitudeReduction.pdf`.
