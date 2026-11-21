# Subsection 1.1 — retrospective evidence and status

Recorded: 2026-11-17 (Asia/Tehran). Scope: subsection 1.1 only.
Provenance: tests executed by the user in Mathematica and reported in this conversation; the assistant did not execute Mathematica or independently inspect saved notebook outputs.

## User-reported tests

- Versions reported: Mathematica 15.0.1 (Windows), FeynArts 3.12, FeynCalc 10.2.1.
- Initial InsertFields failed with `TagSetDelayed::tagnf: Tag FourVector not found in -Overscript[mom_, _]^mu___`; subsequent rendering failed or remained unevaluated.
- User reported successful patching after `$LoadFeynArts = True; Needs["FeynCalc`"]` and successful insertion using the Toy model.
- The model exists in FeynCalc's `Examples/Models/Phi4`, not the standard FeynArts Models directory. The supplied tutorial uses both Model and GenericModel pointing to the full Phi4 model base path, after `FAPatch[PatchModelsOnly -> True, FAModelsDirectory -> modelDir]`.
- Following that setup, user reported: "Ok now the diagrams are displayed properly."
- Reported ToPaVe tadpole output, transcribed into plain Mathematica notation:
  `I Pi^2 g A0[mphi^2]/2`
- Reported ToPaVe bubble output, transcribed into plain Mathematica notation:
  `I Pi^2 g^2 (B0[(p2-p3)^2,mphi^2,mphi^2] + B0[(p2-p4)^2,mphi^2,mphi^2] + B0[(p3+p4)^2,mphi^2,mphi^2])/2`
  Here squared vectors abbreviate the scalar-product expressions in the user's report; they are not executable scalar Mathematica powers of vector symbols.

## Derivation drafted

B-01: Euclidean tadpole correction proportional to lambda T/2.
B-02: Euclidean four-point correction proportional to -lambda^2/2 times the three bubble integrals.
Rationale drafted: a quartic interaction gives one tadpole and three externally labeled bubble pairings, with combinatorial weight 1/2 for each graph. These formulas were written by the assistant; detailed contraction counting and the complete package-to-Euclidean normalization were not independently tested.

## Decision

Only important equations explicitly written in the notebook receive anchors, allocated in notebook appearance order. B-01 and B-02 are the latest proposed labels, replacing the earlier speculative registry. The user will paste notebook cells and equation-map entries; neither protected deliverable is edited by the assistant. Present reasoning before the Mathematica code, then use code as a check. Work remains confined to subsection 1.1.

## Status, bounded to the actual evidence

- Diagram rendering and A0/three-B0 structure: Mathematica-checked (user-reported).
- Euclidean tadpole/bubble expressions B-01 and B-02: derived draft; not yet fully Mathematica-checked with project normalization.
- Coupling convention: open. Model output uses `g`; project g = lambda/(16 Pi^2). Do not identify the model's g with the project's rescaled coupling without reading the model's vertex definition.
- Mass replacement: open. The attempted `Mphi -> m` did not remove the reported `mphi`; symbol spelling must be checked.
- External momentum convention: open. Conversion used p1,p2 incoming and p3,p4 outgoing; project formulas use all-incoming momenta. Outgoing momenta must be negated when comparing channel labels. The three reported B0 arguments are consistent with a scattering routing, not literally the all-incoming plus-sign definitions with the same symbol names.
- Wick rotation, loop-measure factors, and Euclidean PaVe arguments: open. Raw i Pi^2 package output is not itself the Euclidean normalized vertex; Euclidean P_E^2 corresponds to Minkowski invariant -P_E^2.
- Exact Fields Notes page/equation anchors: open. Earlier suggested citations were not verified and must not be treated as checked source anchors.
- Notebook math typesetting: open. The previous claim that pasting raw LaTeX inside Ctrl+4 automatically renders it was not tested and should not be relied on.

## Failed approaches / lessons

- Loading independent unpatched FeynArts and FeynCalc caused a symbol conflict. Use compatible patched integration; no need to alter FourVector manually.
- Guessing Model -> "Phi4" in the standard model directory was insufficient. Supply the example model path and its matching GenericModel.
- FAModelsDirectory is a FAPatch option, not a directory-valued variable; using its unevaluated symbol in FileNames did not establish that a model was absent from the installation.
- The assistant's proposed FACreateTopologies/FAInsertFields/FAPaint names were incorrect for this setup; ordinary FeynArts function names remain valid after patching.
- A missing model alone does not establish the cause of the original FourVector conflict. Successful patching and subsequent explicit model loading are separate milestones.
