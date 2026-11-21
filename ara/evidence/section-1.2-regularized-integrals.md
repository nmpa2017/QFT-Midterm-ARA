# Subsection 1.2 — derivations and user-reported Mathematica checks

Recorded 2026-11-19T20:39:02+03:30, retrospectively at the user's request.
Provenance: analytic work and code supplied by the assistant; Mathematica executed by the user. No assistant-side Mathematica execution or independent saved-output inspection.

## Conventions and decisions

- Massive Euclidean integrals, m^2>0; spherical |k|<Lambda cutoff in d=4.
- DR uses d=4-epsilon, one mu^epsilon per loop, with positive mu. epsilon is the project's epsilon, not FeynCalc's half-sized parameter.
- Derive each integral/regulator combination before writing its Mathematica check.
- Shorten the DR derivation by specializing Fields Notes Eq. (13.7), verified in the supplied chapter excerpt at printed p. 114 (PDF page 4). This is the revised meaning of B-06, replacing the earlier proposed Schwinger-parameter intermediate formula.
- Verify the derivative identity from the evaluated regularized expressions at fixed regulator and scale, not only by differentiating the integrand. Also compare the pole-plus-finite DR expressions.
- Mathematica symbols massSq, cutoff, muScale, epsDR keep computational names separate from presentation notation and package symbols.

## Equations derived

B-03: T_Lambda = (1/(8 Pi^2)) integral_0^Lambda dk k^3/(k^2+m^2).
B-04: T_Lambda = [Lambda^2 - m^2 log(1+Lambda^2/m^2)]/(16 Pi^2).
B-05: T_Lambda = [Lambda^2 - m^2 log(Lambda^2/m^2) - m^4/Lambda^2 + O(m^6/Lambda^4)]/(16 Pi^2).
B-06 (revised): integral d^d k/(2 Pi)^d (k^2+m^2)^(-alpha) = (m^2)^(d/2-alpha) Gamma(alpha-d/2)/[(4 Pi)^(d/2) Gamma(alpha)]; Fields Notes Eq. (13.7).
B-07: T_DR = m^2/(16 Pi^2) (4 Pi mu^2/m^2)^(epsilon/2) Gamma(-1+epsilon/2).
B-08: T_DR = m^2/(16 Pi^2) [-2/epsilon + EulerGamma - 1 - log(4 Pi mu^2/m^2)] + O(epsilon).
B-09: B_Lambda(0) = (1/(8 Pi^2)) integral_0^Lambda dk k^3/(k^2+m^2)^2.
B-10: B_Lambda(0) = [log(1+Lambda^2/m^2) - Lambda^2/(Lambda^2+m^2)]/(16 Pi^2).
B-11: B_Lambda(0) = [log(Lambda^2/m^2)-1+2 m^2/Lambda^2+O(m^4/Lambda^4)]/(16 Pi^2).
B-12: B_Lambda(0) = -partial T_Lambda/partial(m^2) at fixed Lambda, demonstrated with B-04 and B-10.
B-13: B_DR(0) = (4 Pi mu^2/m^2)^(epsilon/2) Gamma(epsilon/2)/(16 Pi^2).
B-14: B_DR(0) = [2/epsilon - EulerGamma + log(4 Pi mu^2/m^2)]/(16 Pi^2) + O(epsilon).
B-15: -partial T_DR/partial(m^2) = B_DR(0), using Gamma(z+1)=z Gamma(z), and independently through pole-plus-finite order.

## Checks actually supplied and confirmed

1. Cutoff tadpole: Mathematica Integrate applied to the radial integral; exact difference from B-04 vanishes. User: "I ran the input and it returned the same answer and of course their difference vanished".
2. Cutoff tadpole expansion: Series at infinity compared with B-05. User: "all is good and confirmed here".
3. DR tadpole: code specializes Eq. (13.7), checks the exact rearrangement B-07, then Series through finite order checks B-08. The user proceeded to the next integral without explicitly posting these results. Status derived; standalone check confirmation remains open. Do not infer a passed run merely from progression.
4. Cutoff bubble: exact formula B-10 differentiated against B-04 in the B-12 check; B-11 checked by Series. User: "All is great as the results are as expected." Status Mathematica-checked for the derivative comparison and expansion. No independent Integrate evaluation of the bubble radial integral B-09 was supplied; B-10's integration remains analytically derived and indirectly consistency-checked.
5. DR bubble: code specializes Eq. (13.7) with alpha=2, compares exact B-13, and compares its Laurent expansion with B-14. Then exact and pole-plus-finite derivative differences are checked against zero. User asked what the second zero meant and then stated: "This check was also passed." Together with the earlier passing-check context this records the DR checks as Mathematica-checked by user report, without raw output archival.

## Physical interpretation derived

The cutoff tadpole has a quadratic divergence and a mass-dependent logarithmic term. The cutoff bubble has only a logarithmic divergence. Near four dimensions the DR integrals show poles, with no explicit quadratic cutoff term. Their raw regulated values need not match between schemes. No MSbar rescaling was applied: EulerGamma and log(4 Pi) remain. The exact derivative identity holds in both schemes and the DR finite-term check confirms cancellation of the tadpole's constant -1 after mass differentiation.

## Failed approach and remedy

The initial cutoff-series/check attempt returned an equation containing an unevaluated tCutoffExpected symbol instead of zero or True. This showed the expected expression had no assigned value at evaluation time; the precise cause (cell execution order, clear, or restart) was not established. A self-contained cell defining all quantities before comparison succeeded. This was a notebook-state issue, not a failure of the analytic integral.

## Remaining open items / evidence limits

- Standalone DR tadpole check output confirmation (B-07/B-08); later derivative tests do not replace an independently reported series check.
- Optional direct Mathematica integration of the bubble radial integral B-09 to B-10; current checks establish consistency, not a fresh independent integration.
- Final notebook subsection note and source-map entries still user-pasted; actual notebook and equation-map contents were not inspected or modified for this recording.
- Exact source relation for each anchor beyond the verified common Eq. (13.7) still to be documented as quote/specialization/derivation. No guessed page or equation citations.
- Subsection 1.1 convention issues remain separate and are not resolved by these scalar integral checks.
