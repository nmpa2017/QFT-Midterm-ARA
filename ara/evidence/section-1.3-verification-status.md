# Subsection 1.3 — provenance and verification record

Recorded 2026-11-21T18:03:25+03:30 in response to the user's request to record subsection 1.3. Time is the latest supplied session sample, not a test execution timestamp.

## Evidence inspected

Read-only inspection of `QFTMidtermNotebook.nb`: saved notebook content ends at lines 5147–5183 with the subsection 1.2 summary and an empty Input cell (ExpressionUUID 0faff1ca-6bf8-1a48-8ef1-ba95589fcacf). Searches for vertex2, drKernel, slopeDR, B-16, B-21 and B-24 found no subsection 1.3 implementation. No subsection 1.3 Input/Output cells can therefore be linked in this saved snapshot. The live, possibly unsaved notebook was not inspected. No Mathematica evaluation was performed by the assistant.

## Result-level links and statuses

| Record | Anchor | Claim/result discussed in conversation | Mathematica cell | Evaluated output | Status |
|---|---|---|---|---|---|
| R13-01 | B-16 | Zero-momentum conditions Gamma2(0)=m^2, derivative Gamma2=1, Gamma4(0)=lambda | Not present in saved notebook | Not present | Adopted subtraction conditions, not a computational result |
| R13-02 | B-17 | deltaZ=0; delta m_DR^2=-lambda T_DR/2, including finite terms | Not present; proposed symbolic verification cell begins Clear[coupling,...] and defines vertex2 | Not present | Derived and checked analytically by substitution; not Mathematica-checked |
| R13-03 | B-18 | delta lambda_DR=3 lambda^2 B_DR(0)/2, including finite terms | Not present; same proposed cell defines vertex4 | Not present | Derived and checked analytically by substitution; not Mathematica-checked |
| R13-04 | B-19 | deltaZ=0; delta m_Lambda^2=-lambda[Lambda^2-m^2 log(1+Lambda^2/m^2)]/(32 Pi^2) | Not present; proposed symbolic cell is regulator-independent | Not present | Derived and checked analytically by substitution; not Mathematica-checked |
| R13-05 | B-20 | delta lambda_Lambda=3 lambda^2[log(1+Lambda^2/m^2)-Lambda^2/(Lambda^2+m^2)]/(32 Pi^2) | Not present; proposed symbolic cell is regulator-independent | Not present | Derived and checked analytically by substitution; not Mathematica-checked |
| R13-06 | B-21 | DR finite bubble difference = -integral_0^1 dx log(1+x(1-x)P^2/m^2)/(16 Pi^2) | Not present; proposed second cell defines drKernel and drFiniteKernel | Not present | Derived; Mathematica confirmation open |
| R13-07 | B-22 | Form bubble difference on common spherical cutoff domain before taking Lambda to infinity | Not present | Not present; analytic convergence/order-of-operations argument | Derived analytically |
| R13-08 | B-23 | Removed-cutoff difference equals B-21 | Not present; proposed second cell defines cutoffRadial and cutoffFiniteKernel | Not present | Derived; Mathematica confirmation open |
| R13-09 | B-24 | DeltaB(0)=0 and slope=-1/(96 Pi^2 m^2) | Not present; proposed second cell defines slopeDR, slopeCutoff and expectedSlope | Not present | Derived; Mathematica confirmation open |

These record IDs are evidence rows, not new notebook Anchor IDs or crystallized claims. Expected zeros in code supplied in conversation are NOT recorded as evaluated outputs. No notebook UUID or output label is invented.

## Conventions and decisions

- Massive Euclidean theory, m^2>0, all external momenta incoming in the analytic formulas.
- Cutoff: d=4, spherical |k|<Lambda.
- DR: d=4-epsilon with one mu^epsilon per loop; project epsilon=2 epsilon_FC relative to FeynCalc D=4-2 epsilon_FC. No MSbar scale redefinition.
- Counterterms enforce zero-momentum subtraction, including finite constants/logarithms; they are not MS counterterms.
- User accepted analytic substitution checks for counterterms instead of redundant CAS cells.
- For cutoff momentum dependence: form the convergent difference, take Lambda to infinity, then justify the momentum shift. The supplied CAS code checks a post-limit radial representation, not the original finite-domain shift argument.
- The subtracted bubble value is zero at P^2=0; its slope is nonzero. The user explicitly acknowledged the earlier misunderstanding before requesting the derivation.

## Failed approaches / unresolved work

No failed subsection 1.3 Mathematica run was reported. The zero-slope interpretation was a clarified misunderstanding, not an experimental failure. Need a saved subsection 1.3 notebook with evaluated Input/Output cells or user-supplied outputs before recording Mathematica-checked status. No evidence here resolves the separate subsection 1.1 coupling/momentum normalization questions.

Notebook and ara/anchor/equation-map.md were not modified.
