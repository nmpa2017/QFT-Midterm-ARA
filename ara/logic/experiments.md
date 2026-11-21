# Experiments: Midterm QFT Project (FeynCalc)

## E01: FeynCalc One-Loop Diagram Generation
- **Verifies**: C02, C03
- **Setup**: FeynArts model `Phi4`.
- **Procedure**:
  1. Define model parameters and interaction vertices.
  2. Generate 1PI 2-point and 4-point topologies using `CreateTopologies[1, 2->2]`.
  3. Insert fields and generate amplitudes.
  4. Perform trace and momentum algebra.
- **Expected outcome**: Correct algebraic expression for 2-point and 4-point amplitudes.

## E02: Regularization Comparison (Cutoff vs. DR)
- **Verifies**: C03 (Regularization independence)
- **Setup**: Evaluated amplitudes from E01.
- **Procedure**:
  1. Apply sharp cutoff regularization ($\Lambda$) to loop integrals.
  2. Apply Dimensional Regularization ($d=4-\epsilon$).
  3. Extract divergences (poles/logarithms).
- **Expected outcome**: Consistent pole structure and divergent logarithm coefficients between regulators.

## E03: Beta Function Calculation
- **Verifies**: C01 (Renormalization group flow)
- **Setup**: Normalized 1PI 4-point amplitude.
- **Procedure**:
  1. Define counterterms to cancel poles in DR.
  2. Compute the renormalized coupling constant $\lambda_R$.
  3. Calculate the $\beta$-function $\beta(\lambda) = \mu \frac{\partial \lambda_R}{\partial \mu}$.
- **Expected outcome**: Correct $\beta$-function expression and identification of the non-trivial fixed point.
