# Subsection 2.3 — scaling derivation and comparison status

Retrospective record requested by the user on 2026-11-22. No new Mathematica execution, notebook inspection, or literature verification was performed. The notebook and equation map are not modified.

## Derived results: B-46–B-52

- B-46: Delta_phi=(d-2+eta)/2 and Delta_h=d-Delta_phi=(d+2-eta)/2 follow from the critical propagator and scale invariance of the uniform source term.
- B-47: critical scaling M(h)=b^(-Delta_phi) M(b^Delta_h h) gives delta=Delta_h/Delta_phi=(d+2-eta)/(d-2+eta).
- B-48: substitute d=4-epsilon and eta=epsilon^2/54+O(epsilon^3), then expand: delta=3+epsilon+25 epsilon^2/54+O(epsilon^3).
- B-49: set epsilon=1 only after truncation: eta=1/54 and delta=241/54.
- B-50: M is proportional to rho-rho_c. Along T=T_c, dP=n d mu_chem and n_c is nonzero, giving h proportional to mu_chem-mu_chem,c and hence to P-P_c at leading order. Thus (P-P_c)/P_c is asymptotic to A sgn(rho-rho_c) |(rho-rho_c)/rho_c|^delta. Field mixing and real-fluid asymmetry can affect subleading behavior.
- B-51: critical scattering S(q) proportional to q^(-2+eta) for xi^-1 << q << a^-1 gives slope -107/54 in the truncated three-dimensional prediction.
- B-52: project-supplied Delta_sigma=0.518148806(24) gives eta_B=2 Delta_sigma-1 and delta_B=3/Delta_sigma-1. Water input is delta_water=4.324. No water eta/scattering slope is supplied.

## Check and status

All B-46–B-52 are analytically derived. A local-symbol Mathematica Module was supplied to verify the delta series and generate a comparison Grid with bootstrap central values and the water fit, but the user has not supplied execution output or confirmation. Therefore do not label the subsection or table Mathematica-checked yet. Previous subsection 2.2 remains checked within its separately recorded scope.

The assistant advised that no additional CAS work beyond the existing expansion/table cell is necessary: dimensional analysis and thermodynamic identification need analytical reasoning, not further loop integrals. This is an assistant recommendation, not an explicit user decision that the table code was executed or checks were waived.

## Numerical plausibility discussion (derived, not an independent experiment)

The assistant compared the predicted values with the supplied central benchmarks: eta approximately 0.01852 versus 0.03630 (roughly 49 percent low), delta approximately 4.46296 versus 4.78984 (roughly 6.8 percent low), and scattering slope approximately -1.98148 versus -1.96370 (absolute difference approximately 0.01778). Delta is approximately 3.2 percent above the specified water fit. These were explanatory comparisons in the conversation, not new Mathematica output.

Interpretation offered by the assistant: deviations are plausible for a short unresummed epsilon expansion evaluated at epsilon=1. Numerical proximity is only a sanity check, not a controlled error estimate or proof. The apparent agreement of the scattering slope partly reflects the dominant canonical -2 term; closeness to the water fit does not establish superiority to the bootstrap benchmark. Experimental fitting range/corrections are possible explanations for differences, not established findings about that fit. Agreement of pole renormalization with finite-log scaling and the standard leading coefficients is stronger internal evidence.

## Decisions and failures

- User requested normal analytic derivation followed by Mathematica comparison-table code, and then pasteable equation-map notes. Preserve B-46–B-52 numbering and protected deliverables.
- No failed Mathematica approach or new calculation error was reported for subsection 2.3. Avoid inventing an executed check from the user's statement that the derivation is straightforward.
- Do not substitute epsilon=1 into the unexpanded ratio as if it were the specified second-order truncation; this was a methodological warning, not a user-reported failed run.

## Open items

- Execution of the supplied series/table cell and its output.
- Precise lecture-note locators for scaling/source relations; original benchmark publications were not independently inspected.
- Saved notebook cell/output provenance. No action to inspect or edit the notebook is inferred from this recording request.
