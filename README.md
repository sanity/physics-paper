# A Learned Latent Algebra for Physical Systems Closed Under Spatial Composition and Time Evolution

Draft preprint by Ian Clarke (2026-05-08).

We learn an embedding of physical state that supports a compositional algebra:
encode subsystems, combine them, evolve them, and decode back to observables —
with the algebra closed under both spatial composition (combine) and time
evolution. We demonstrate the framework on rigid bodies and Lennard-Jones
fluids/gases.

**[paper.pdf](paper.pdf)** — current draft (work in progress).

## Highlights

- Sliced Wasserstein density loss drops 64-particle density RMSE from 0.190 to 0.093.
- Multi-size paired-union supervision closes the OOD scene-size gap (128p direct
  encoding RMSE 0.188 → 0.110; 128p via combine 0.207 → 0.135).
- A compose-evolve commutativity loss yields cosine similarity ≥ 0.989 between
  `evolve(combine(A, B))` and `combine(evolve(A), evolve(B))` out to 8 evolution
  steps (vs. 0.859 for the same model without the explicit commutativity loss).
- Cross-regime transfer to Lennard-Jones at three temperatures (T*=0.3 in flight,
  T*=1.0 fluid: density 0.220, T*=2.0 gas: density 0.179).

## Files

- `paper.pdf` — compiled paper
- `paper.tex` — LaTeX source
- `references.bib` — bibliography (used for completeness; the paper itself uses
  inline `\thebibliography` to avoid a bibtex dependency)

## Status

Draft. Not yet submitted to arXiv. Numbers and structure may change.
