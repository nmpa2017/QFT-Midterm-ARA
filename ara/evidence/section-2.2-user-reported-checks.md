# Subsection 2.2 — derivation and user-reported Mathematica checks

Recorded: 2026-11-22T02:07:24+03:30. Retrospective evidence from this conversation; no assistant Mathematica execution or saved-notebook inspection was performed for this record. Notebook and equation map remain untouched.

## Decision and conventions

Continue anchors B-40–B-45. Use Euclidean massless DR at nonzero p^2, d=4-epsilon, g=lambda/(16 Pi^2), original MS scale (not MSbar), phi_0=Sqrt[Z_phi] phi, and gamma_phi=(1/2) mu d Log[Z_phi]/d mu at fixed bare parameters. Derive first, then check only subsection 2.2 algebra using the previously established sunset. Supply conclusion and equation-map additions as pasteable text, not direct edits.

## Derived results

- B-40: Delta Gamma_sunset^(2)=g^2 p^2/12 [1/epsilon-Log[p^2/mu^2]+C_MS], C_MS=Log[4 Pi]+13/4-EulerGamma. The positive inverse-propagator pole uses the analytically derived Euclidean prefactor -lambda^2/6.
- B-41: delta Z_phi=-g^2/(12 epsilon), Z_phi=1-g^2/(12 epsilon)+O(g^3), from pole cancellation.
- B-42: Gamma_R^(2)=p^2 {1+g^2/12 [C_MS-Log[p^2/mu^2]]}+O(g^3).
- B-43: gamma_phi=g^2/12+O(g^3). Expand the fixed-bare derivative in g before removing epsilon; the -epsilon g term in beta multiplies the simple pole.
- B-44: eta=epsilon^2/54+O(epsilon^3). An unknown c epsilon^2 correction to g_* first changes eta at order epsilon^3.
- B-45: with x=p^2/mu^2, normalized inverse propagator is x(1-g^2 Log[x]/12), and normalized propagator is (1+g^2 Log[x]/12)/x through g^2. Matching at g_* gives eta/2=g_*^2/12. Normalization removes the MS finite constant.

## User-pasted execution evidence

The user supplied an Association containing the following expressions (Module suffix `$17731` removed here only for readability):

```text
Z_phi -> 1-g^2/(12 eps)
Gamma_R^(2) -> p2/48 (4 g^2 Log[(4 Pi mu^2)/p2]+(13-4 EulerGamma) g^2+48)
gamma_phi -> g^2/12
eta -> eps^2/54
Normalized inverse propagator -> x-g^2 x Log[x]/12
Normalized propagator -> (g^2 Log[x]+12)/(12 x)
```

All seven checks in the pasted output were True:

1. B-40: inverse-propagator pole.
2. B-41: pole cancellation.
3. B-43: anomalous dimension.
4. B-44: eta.
5. One-loop fixed point suffices.
6. B-45: inverse-propagator logarithm.
7. B-45: propagator logarithm.

Provenance: user-executed Mathematica output pasted in the conversation after the subsection 2.2 verification code. No cell UUID or saved output path was supplied.

## Verification scope and statuses

B-40–B-45: derived and Mathematica-checked for the downstream algebra represented by these seven tests. The two-loop graph sign, symmetry factor, and the input H(p) were supplied to the code; it does not independently compute or validate those diagrammatic inputs. The normalized logarithm check verifies internal agreement with the critical scaling expansion, not an independent measurement of eta.

## Failed approaches or issues

No failed calculation or Mathematica warning was reported for this subsection. Module generated names such as g$17731 and eps$17731; the user found them confusing. Explained that these are collision-avoiding local-symbol names, not additional parameters or factors. The output Association is a labeled collection of results, and its differently factored Gamma_R expression is algebraically identical to B-42. Do not invent an additional failed run.

## Open items

- Precise lecture-note locators for the new two-loop coefficients have not been verified. Supplied equation-map prose explicitly labels those coefficients as derived rather than inventing references.
- Saved notebook cell/output provenance remains uninspected; checks are user-reported, not assistant-executed.
- Independent computational verification of the Euclidean diagram sign/symmetry remains outside these tests. No remaining algebraic failure is reported for subsection 2.2.
