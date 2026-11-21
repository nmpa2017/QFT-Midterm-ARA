# Subsection 2.1 — retrospective derivation and verification record

Recorded at the user's explicit request. Evidence comes from the conversation, not an assistant-executed Mathematica session. The notebook and equation map are not modified by this recording.

## Decisions and conventions

- Use the working Part 1 model setup: real scalar S[1], Classes insertion level, full paths for both Model and GenericModel, and PreFactor -> 1.
- Isolate the sunset with StartingTopologies -> Theta and Adjacencies -> {4}; convert using loop momenta {k,l} and equal incoming/outgoing momentum p.
- Work in Euclidean massless DR with d=4-epsilon, p^2>0, one mu^epsilon factor per loop, g=lambda/(16 Pi^2), and no MSbar scale redefinition.
- Derive before checking. Keep sequential anchors B-31–B-39. Supply equation-map text for the user to paste; do not edit their equation map or notebook.

## Derived results and precise check scope

| Anchors | Result | Evidence status |
|---|---|---|
| B-31 | Sunset contraction factor 1/6; Delta Gamma^(2)=-lambda^2 H/6 | Derived. No explicit package output independently verifying its sign or symmetry factor was pasted. |
| B-32 | General massless convolution identity | Derived analytically; encoded as an input formula in the Mathematica helper, not independently integrated by the check. |
| B-33–B-35 | Two applications of the convolution identity give exact H | Mathematica-checked by user-pasted symbolic output, conditional on B-32. |
| B-36–B-37 | Laurent pole and finite part | Mathematica-checked at pSq=1, mu=1. General scale dependence is derived from the exact prefactor; a symbolic expansion retaining both scales was not shown. |
| B-38 | Inverse-propagator correction and positive g^2 p^2/(12 epsilon) pole | Derived from B-31 and checked integral; no independent CAS sign or prefactor check supplied. |
| B-39 | Four-point counterterm insertions leave momentum-independent scaleless tadpoles | Derived graphically/analytically, not directly CAS-tested in pasted output. |

Exact expression transcribed from the user's output:

```text
((4 Pi)^(eps-4) mu^(2 eps) pSq^(1-eps)
 Gamma[1-eps/2]^3 Gamma[eps-1])/Gamma[3-3 eps/2]
```

Unit-scale Laurent expansion transcribed from the user's output:

```text
-1/(512 Pi^4 eps)
+(-13+4 EulerGamma-4 Log[4 Pi])/(2048 Pi^4)+O[eps]
```

This agrees with the derived full expression

H(p)=-p^2/(512 Pi^4) [1/epsilon+Log[4 Pi mu^2/p^2]+13/4-EulerGamma]+O(epsilon).

The coefficient of 1/epsilon at unit scales is -1/(512 Pi^4); the pole term includes an additional 1/epsilon. The check is symbolic, not numerical. No direct two-loop momentum integration was performed by the helper: it composes the stated convolution identity.

## Failed or incomplete approaches

- Initial FeynArts snippets used invalid options/filters (SelfEnergy singular, Restrictions -> 1PI, FAModelsDirectory on CreateTopologies/InsertFields), wrong fermion field F[1], and bare model names that failed to locate Phi4.gen. User supplied a working scalar/full-path example. Subsequent code follows that example.
- Printed success counts after aborted insertion were not evidence of successful amplitude generation; unevaluated expressions can have nonzero Length.
- Initial H check covered only a gamma ratio and compared a finite coefficient against an expression still containing a pole. Replaced with the two-convolution construction and user-pasted output above.
- The revised script still set pSq=mu=1 before Series; it did not validate the general-scale logarithm by direct symbolic expansion.
- Earlier section 1.4 snippets used undefined CoefficientAll and invalid D[...,p^2]. The later snippet hard-coded betaGResult rather than actually deriving its quadratic coefficient. The user reported checks complete, but that snippet alone is not an independent validation of the beta coefficient.

## Diagram interpretation

The ordinary two-loop tadpole-insertion graph is also 1PI: two lines connect A and B, both external legs attach to A, and B has a self-loop. It is momentum-independent. A four-point sunset subgraph consists of any two of the three lines connecting its vertices; the omitted line supplies two external half-edges of that subgraph. Contracting such a divergent bubble to a local vertex leaves a counterterm tadpole. These are distinct graphs.

## Open items

- Exact notebook cell/output provenance and explicit sunset package output have not been inspected in this recording.
- Precise lecture-note equation/page references for new B-31–B-39 entries remain unverified; the generic master identity must not be labeled as a verified quotation without a source locator.
- General-scale Laurent check, independent symmetry/sign checks, and any CAS test of counterterm insertions remain open if independent computational confirmation is desired.
- Earlier blanket claims that all B-31–B-39 were Mathematica-checked overstate the pasted evidence. Use the anchor-specific statuses above.
