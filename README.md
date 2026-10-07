# Angular Amplitude Reduction — the Oriented Shear Product of the sl(2) Step and the Central-Phase Observable of the Weil Cascade

J. Beau, Independent Researcher, France

## Status

Working note (preprint), v1.3. DOI: [10.5281/zenodo.20601228](https://doi.org/10.5281/zenodo.20601228)

## Abstract

This internal note fixes the numerical observable for the absolute normalisation of the angular
generation split of Q14 §6, and reports the Weil–BFS computations of it (capacity audit of the last section).

A short Baker–Campbell–Hausdorff reduction in $\mathfrak{sl}_2$ identifies the per-step
$J_\Pi$-odd $J_3$ component of the metaplectic cascade generator with the oriented product $ts$ of
the two shear parameters, produced by the $\mathfrak{sl}_2$ commutator $[E,F]=H$ (Q14,
Proposition 6.5), and not with a free shear parameter. In the $\mathrm{SL}(2)$-on-$V$ model of Q14 the computation uses
only the $\mathfrak{sl}_2$ relations and no Heisenberg bracket (PRS, lemma on the exact metaplectic
opening); in the oscillator (Weil) realisation the $\mathfrak{sl}_2$ generators are quadratic in the
Heisenberg generators, and no map between the two brackets is supplied. The
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
amplitude. It identifies the precise Weil–BFS observable to be measured to
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

## Reproduction

Everything below runs from a clone of this repository alone (Python with `numpy`, `matplotlib`, `sympy`; see
`code/requirements.txt`); no sibling repository and no external module is needed.

```bash
python code/frontier_exact.py                       # standard library only, seconds
python code/weil_bfs_angular_area.py --mode full    # about 20 s; symmetric-shell mean Theta_raw = 0 for q = 61, 101, 151
python code/front_NA_capacity_audit.py              # about 2.5 min; obstruction table, onset 1/3, 3q/(20 pi)
python code/front_NAgeom_sym2_conversion.py         # exact symbolic checks
python code/jpi_vs_phi_fingerprint.py
```

- `code/frontier_exact.py`: the per-shell rationals $\langle|\Delta A_c|\rangle_{\partial^+}(m) = \tfrac13, \tfrac59,
  \tfrac23, \tfrac{10}{11}, \tfrac{119}{109}, \tfrac{239}{185}$ (first-shell onset value $\tfrac13$), their
  equality with the $H_3(\mathbb{Z})$ values for $q\in\{61,101,151,211,307\}$ (verified for the shells $m\le 6$ only), and the vanishing of the signed frontier sums.
- `code/q11_oriented_frontier.py` is a vendored copy of the script of the Q11OF repository.
- The scripts write their outputs (`*.csv`, `*.json`, `*.pdf`, `*.jsonl`) in the current directory.
- `data/`: the six June 2026 campaign summaries, with their provenance (`data/README.md`); the scripts regenerate
  them to $10^{-12}$.
- The Heisenberg conventions are the local reference functions of the scripts (identical to those of
  `spectral_O12`, see the provenance comment in each script).
