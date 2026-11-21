# Claims: Midterm QFT Project

## C01: Generating Functional for Free Scalar Fields
- **Statement**: The generating functional $W[j]$ for a free scalar field encapsulates all connected and disconnected time-ordered correlation functions through successive functional derivatives with respect to the source $j(x)$.
- **Conditions**: Free Klein-Gordon scalar field theory in Minkowski spacetime ($d=4$), valid for arbitrary external sources $j(x)$ vanishing at infinity.
- **Status**: verified
- **Falsification criteria**: If functional differentiation of $W[j]$ fails to reproduce the correct time-ordered two-point Green's function (propagator) or yields non-causal propagation poles.
- **Proof**: Verified analytically via path integral Gaussian integration over field configurations $\phi(x)$ (Experiment E01).
- **Sources**: 
  - `[result]` Peskin & Schroeder, *An Introduction to Quantum Field Theory*, Chapter 9.

## C02: Wick's Theorem and Perturbative Expansion
- **Statement**: Time-ordered products of interacting fields can be systematically decomposed into sums of normal-ordered products and all possible pairwise contractions (propagators), enabling diagrammatic evaluation of S-matrix elements.
- **Conditions**: Perturbative regime of interacting scalar field theory (e.g., $\lambda \phi^4$ theory) where coupling constant $\lambda \ll 1$.
- **Status**: verified
- **Falsification criteria**: If the expansion fails to match the order-by-order Dyson series expansion of the time-evolution operator in interaction picture.
- **Proof**: Demonstrated via operator identity expansions and path integral interaction-vertex decoupling (Experiment E02).
- **Sources**:
  - `[result]` Peskin & Schroeder, Chapter 4 & 9.

## C03: Feynman Rules in Momentum Space
- **Statement**: Fourier transforming position-space Green's functions yields momentum-space Feynman rules (propagators as $(k^2 - m^2 + i\epsilon)^{-1}$ and vertices as $-i\lambda$) that conserve four-momentum at every vertex.
- **Conditions**: Momentum representation in translation-invariant Minkowski space with standard $i\epsilon$ Feynman prescription.
- **Status**: verified
- **Falsification criteria**: Violation of four-momentum conservation at vertices or incorrect mass-shell singularity structure for external legs.
- **Proof**: Derived via stationary phase approximation and Fourier convolution integrals of correlation functions (Experiment E03).
- **Sources**:
  - `[result]` Peskin & Schroeder, Chapter 4.
