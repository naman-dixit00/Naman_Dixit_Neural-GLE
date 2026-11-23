# Neural Generalized Langevin Equation (Neural GLE) for Non-Markovian Stochastic Dynamics

**Author & Principal Investigator:** Naman Dixit  
**Affiliation:** B.C.A. (Hons. with Research), University of Rajasthan, India  
**Status:** Technical Proposal Archived (`v1.0-proposal`) | Benchmark Prototype In Progress (`v1.1-prototype`)  
[![DOI](https://zenodo.org)](https://doi.org)

---

## Overview & Original Contribution

This repository contains the original research proposal, mathematical formulation, and forthcoming numerical benchmarks for the **Neural Generalized Langevin Equation (Neural GLE)** framework, conceived and developed by **Naman Dixit**.

Extending data-driven Markovian Stochastic Langevin Regression (SLR) to non-equilibrium viscoelastic biological membranes and intermittent small-scale fluid interfaces, this framework resolves three core bottlenecks:
1. **Ante Hoc Interpretable Non-Markovian Memory:** Parameterizes viscoelastic memory kernels via a damped-oscillatory Prony series:
   $$\Gamma_\theta(t) = \sum_{k=1}^{M} C_k e^{-\gamma_k t} \cos(\omega_k t)$$
   enabling direct extraction of physical relaxation timescales ($\tau_k = 1/\gamma_k$) and oscillatory frequencies ($\omega_k$).
2. **$\mathcal{O}(N)$ Linear-Time Markovian Embedding:** Eliminates $\mathcal{O}(N^2)$ direct history-integral bottlenecks by lifting the memory convolution into coupled auxiliary state-space ODEs $(z_k^c, z_k^s)$.
3. **Colored Thermal Noise & High-Order Multiplicative Integration:** Combines state-space colored noise filtering $\eta(t)$ with strong order-1.0 **Milstein stochastic integration** to eliminate tail-statistics errors (KL-divergence spikes) in state-dependent multiplicative noise regimes.

---

## Repository Structure

* `Naman_Dixit_Neural_GLE.pdf` — Complete mathematical formulation, theoretical guarantees, and phased validation roadmap authored by Naman Dixit.
* `benchmarks/` *(Uploading in v1.1)* — Reproducible Python implementations comparing Euler-Maruyama vs. Milstein integration in small-$L$ intermittent regimes and $\mathcal{O}(N)$ auxiliary-state Prony scaling.
* `LICENSE` — Strict All-Rights-Reserved proprietary research license.

---

## Authorship & Citation

If you wish to reference the theoretical formulation or proposal archived in this repository (subject to the strict terms in `LICENSE`), you must cite the author as follows:

```bibtex
@misc{dixit2026neuralgle,
  author       = {Dixit, Naman},
  title        = {Neural Generalized Langevin Equation (Neural GLE): Extending Stochastic Langevin Regression to Non-Markovian Viscoelastic Membranes and Intermittent Regimes},
  year         = {2026},
  publisher    = {Zenodo},
  doi          = {10.5281/zenodo.24472917},
  url          = {https://doi.org}
}
```

---

## Copyright & Strict Usage Notice

**Copyright © 2026 Naman Dixit. All Rights Reserved.**

This research framework, mathematical formulation, proposal document, and associated code are the exclusive intellectual property of **Naman Dixit**. **Strict permission is required prior to any use, reproduction, modification, implementation, or distribution.** See the [`LICENSE`](LICENSE) file for full legal terms.
