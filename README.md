# Quantum Gravity Simulation: Single-File Monorepo

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## Overview

This is a self-contained, executable Python script simulating a simplified model of quantum gravity involving two entangled particles in 3D space. The simulation couples quantum wavefunction evolution (via the Schrödinger equation with Runge-Kutta 4th-order integration) to a classical time field influenced by gravitational effects from matter density. Key features include:

- **6D Configuration Space**: Represents two 3D particles (position vectors in x, y, z for each).
- **Entanglement and Interaction**: Gaussian initial wavefunction with harmonic potentials and an entanglement coupling term.
- **Gravitational Coupling**: A scalar time field `T` evolves via a wave equation sourced by average particle density and curvature-like terms (inspired by semi-classical gravity approximations).
- **Observables**: Tracks normalization, total energy, density projections, entanglement entropy (via reduced density matrix eigenvalues), and density-time correlations.
- **Visualization**: Generates an animated GIF showing projected densities and the time field over time.
- **Configurable**: Uses Hydra for runtime configuration overrides (e.g., grid size, time steps).

The model is conceptual and educational, blending quantum mechanics, field theory, and toy gravitational effects. It's not a full quantum gravity theory (e.g., no loop quantum gravity or string theory elements) but demonstrates emergent phenomena like entropy growth and gravitational backreaction.

## Requirements

- Python 3.8+
- NumPy (for arrays and linear algebra)
- SciPy (for eigenvalue decomposition and gradients)
- Matplotlib (for plotting and animation)
- Hydra-Core (for configuration management)
- OmegaConf (dependency of Hydra)

Install via pip:

```bash
pip install numpy scipy matplotlib hydra-core omegaconf
