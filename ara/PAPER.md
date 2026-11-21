---
title: "Midterm QFT Project: Quantum Field Theory Foundations and Path Integral Formalism"
authors: ["Sharif QFT1 Student"]
year: 2026
venue: "Sharif University of Technology - QFT1 Midterm Project"
doi: "ara-qft1-midterm-2026"
ara_version: "1.0"
domain: "Quantum Field Theory"
keywords: ["path integral", "scalar field", "correlation functions", "generating functional", "Feynman rules"]
claims_summary:
  - "The generating functional W[j] for a free scalar field generates all time-ordered n-point Green's functions via functional differentiation."
  - "Wick's theorem reduces time-ordered products of interacting fields into sums of normal-ordered products and contractions (propagators)."
  - "Perturbative expansion in interacting scalar field theory (lambda phi^4) establishes Feynman diagrams in position and momentum space."
abstract: "This research artifact formalizes the midterm project for Quantum Field Theory I, compiling the theoretical foundations, path integral formulations, generating functionals, and perturbative expansions for scalar quantum fields. It structures the derivations, claims, problem specifications, and verification experiments into an Agent-Native Research Artifact (ARA)."
---

# Midterm QFT Project: Quantum Field Theory Foundations and Path Integral Formalism

## Overview
This ARA artifact compiles the theoretical framework, mathematical derivations, functional methods, and perturbative techniques developed for the Quantum Field Theory I midterm project. It covers canonical quantization vs. path integral formulation, generating functionals for free and interacting scalar fields, Wick's theorem, and Feynman diagram expansions.

## Layer Index

### Cognitive Layer (`/logic`)
| File | Description |
|------|-------------|
| [problem.md](logic/problem.md) | Observations → gaps → key insight |
| [claims.md](logic/claims.md) | 3 falsifiable claims (C01–C03) |
| [concepts.md](logic/concepts.md) | Key technical terms (generating functional, propagator, Feynman rules) |
| [experiments.md](logic/experiments.md) | 3 verification and analytical derivation plans |
| [solution/constraints.md](logic/solution/constraints.md) | Boundary conditions and assumptions |
| [solution/formalization.md](logic/solution/formalization.md) | Path integral quantization and generating functionals |
| [related_work.md](logic/related_work.md) | Typed dependency graph (Peskin & Schroeder, Zee, Weinberg) |

### Physical Layer (`/src`)
| File | Description | Claims |
|------|-------------|--------|
| [environment.md](src/environment.md) | Analytical runtime environment and mathematical software dependencies | — |

### Exploration Graph (`/trace`)
| File | Description |
|------|-------------|
| [exploration_tree.yaml](trace/exploration_tree.yaml) | 3-node research DAG |

### Evidence (`/evidence`)
| File | Description |
|------|-------------|
| [README.md](evidence/README.md) | Index of analytical derivations and equations |
| [proofs/scalar_path_integral.md](evidence/proofs/scalar_path_integral.md) | Functional derivation of the scalar propagator |
