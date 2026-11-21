# Problem: Midterm QFT Project (FeynCalc)

## Task Definition
The project requires a comprehensive analysis of scalar field renormalization in real scalar theory ($\phi^4$) in Euclidean signature, covering the transition from one-loop diagrams to critical phenomena.

## Core Requirements
1. **Part 1: Warm-up with One-loop and Two-regulators**
   - Work in Euclidean signature ($m^2 > 0$).
   - Use the generating functional $Z[j]$ to derive 2-point and 4-point correlation functions.
   - Employ Feynman rules to calculate loop integrals with two types of regulators.
   - Determine symmetry factors and diagrammatic topologies.
   - Use FeynArts and FeynCalc to:
     - Generate topologies (`CreateTopologies`).
     - Insert fields (`InsertFields`).
     - Generate amplitudes (`CreateFeynAmp`).
     - Convert to standard forms (`FCFAConvert`, `ToPaVe`).
2. **Part 2: Cutoff and Dimensional Regularization (DR)**
   - Compare Cutoff and DR ($d=4$) regularization.
   - Derive the generating functional components and their expansions in power series.
   - Identify UV divergences (logarithms and poles).
3. **Part 3: Counterterms and Regulator Independence**
   - Formulate counterterms to cancel divergences.
   - Demonstrate that results (such as the $\beta$-function and fixed points) are independent of the choice of regulator in the limit where the regulator is removed.
4. **Part 4: Beta Function and Fixed Point**
   - Derive the MS $\beta$-function.
   - Identify the non-zero fixed point.
   - Distinguish between MS and finite subtraction conditions.

## Deliverables
- A Mathematica notebook (`.nb`) containing:
  - Theoretical derivations.
  - FeynArts/FeynCalc code segments.
  - Diagram outputs.
  - Analytical results for amplitudes, counterterms, and the $\beta$-function.
- Documentation of conventions (loop-momentum measurement, Wick rotation).
