## B-01 — One-loop Tadpole Integral and Amplitude

- Notebook location: Part 1, Subsection 1.1, Amplitude Generation
- Equation:
  $$ \Gamma^{(2)}_{\text{1-loop}}(p) = \frac{\lambda}{2} \int \frac{d^d q}{(2\pi)^d} \frac{1}{q^2+m^2} \equiv \frac{\lambda}{2} T $$
- Fields Notes Source: Sasha_FieldsNotes2025v1.pdf, Chapter 13
- Equation reference: (Refers to tadpole diagram and Eq. 13.7 logic)
- Page: 131
- Relation: derive
- Derivation: Symmetry factor 1/2 from $\phi^4/4!$ vertex contractions; Euclidean propagator $1/(q^2+m^2)$.
- Status: checked

## B-02 — One-loop Bubble Amplitudes and Channel Sum

- Notebook location: Part 1, Subsection 1.1, Amplitude Generation
- Equation:
  $$ \Gamma^{(4)}_{\text{1-loop}}(p_i) = -\frac{\lambda^2}{2} [B(P_{12}) + B(P_{13}) + B(P_{14})] $$
- Fields Notes Source: Sasha_FieldsNotes2025v1.pdf, Chapter 13
- Equation reference: Refers to bubble group sum (p. 127) and integral $I(p^2)$ (Eq. 10.2)
- Page: 127–128
- Relation: derive
- Derivation: Summation of three distinct channels with symmetry factor 1/2 each, where $B(P)$ is the 2-point scalar integral.
- Status: checked

## B-03 — Radial representation of the cutoff tadpole

- Notebook equation:
  \[
  T_\Lambda
  =\frac{1}{8\pi^2}\int_0^\Lambda
  dk\,\frac{k^3}{k^2+m^2}.
  \]
- Relation: derive.
- Source: definition of T in the project brief, subsection 1.2.
- Derivation: use four-dimensional spherical coordinates,
  \(d^4k=k^3dk\,d\Omega_3\), with \(\int d\Omega_3=2\pi^2\).
- Fields Notes equation/page: no direct quotation used.

## B-04 — Exact cutoff tadpole

- Notebook equation:
  \[
  T_\Lambda
  =\frac{1}{16\pi^2}
  \left[
  \Lambda^2-m^2\ln\left(1+\frac{\Lambda^2}{m^2}\right)
  \right].
  \]
- Relation: derive from B-03.
- Derivation: substitute \(u=k^2\) and integrate
  \(u/(u+m^2)=1-m^2/(u+m^2)\).
- Fields Notes equation/page: no direct quotation used.

## B-05 — Large-cutoff expansion of the tadpole

- Notebook equation:
  \[
  T_\Lambda
  =\frac{1}{16\pi^2}
  \left[
  \Lambda^2-m^2\ln\frac{\Lambda^2}{m^2}
  -\frac{m^4}{\Lambda^2}
  +O\!\left(\frac{m^6}{\Lambda^4}\right)
  \right].
  \]
- Relation: derive from B-04.
- Derivation: expand
  \(\ln(1+m^2/\Lambda^2)\) at fixed positive \(m^2\).
- Fields Notes equation/page: no direct quotation used.

## B-06 — Dimensionally continued scalar integral

- Notebook equation:
  \[
  \int\frac{d^dk}{(2\pi)^d}
  \frac{1}{(k^2+m^2)^\alpha}
  =
  \frac{(m^2)^{d/2-\alpha}}{(4\pi)^{d/2}}
  \frac{\Gamma(\alpha-d/2)}{\Gamma(\alpha)}.
  \]
- Relation: quote, with typographical rearrangement only.
- Fields Notes: Chapter 13, Eq. (13.7).
- Printed page: 114.
- PDF page in supplied excerpt: 4.
- Note: this source identity does not include the project's
  additional factor \(\mu^\epsilon\). That factor is inserted
  when applying the identity to each DR loop.

## B-07 — Exact DR tadpole

- Notebook equation:
  \[
  T_{\mathrm{DR}}
  =
  \frac{\mu^\epsilon(m^2)^{d/2-1}}{(4\pi)^{d/2}}
  \Gamma\left(1-\frac d2\right)
  =
  \frac{m^2}{16\pi^2}
  \left(\frac{4\pi\mu^2}{m^2}\right)^{\epsilon/2}
  \Gamma\left(-1+\frac{\epsilon}{2}\right).
  \]
- Relation: derive by specialization of B-06.
- Fields Notes equations used: Eq. (13.7).
- Printed page: 114.
- Derivation: set \(\alpha=1\), use \(\Gamma(1)=1\),
  multiply by \(\mu^\epsilon\), and substitute \(d=4-\epsilon\).

## B-08 — Laurent expansion of the DR tadpole

- Notebook equation:
  \[
  T_{\mathrm{DR}}
  =
  \frac{m^2}{16\pi^2}
  \left[
  -\frac{2}{\epsilon}+\gamma_E-1
  -\ln\frac{4\pi\mu^2}{m^2}
  \right]+O(\epsilon).
  \]
- Relation: derive from B-07.
- Fields Notes equation underlying the calculation:
  Eq. (13.7), printed p. 114.
- Derivation: expand the gamma function and scale factor
  around \(\epsilon=0\), retaining the pole and finite term.
- Note: this Laurent expression is not quoted directly from
  Eq. (13.7). No MSbar scale redefinition is made.

## B-09 — Radial representation of the cutoff bubble

- Notebook equation:
  \[
  B_\Lambda(0)
  =
  \frac{1}{8\pi^2}\int_0^\Lambda
  dk\,\frac{k^3}{(k^2+m^2)^2}.
  \]
- Relation: derive.
- Sources:
  - Project brief, subsection 1.2: definition of B(P).
  - Fields Notes, Chapter 13, Eq. (13.18),
    printed p. 120: the corresponding integral is denoted \(I(p^2)\).
- Derivation: set the external momentum to zero, impose
  \(|k|<\Lambda\), and perform the four-dimensional angular integral.
- Notation change: the notes' \(\tilde m^2\) becomes the
  project's \(m^2\); \(I(0)\) corresponds to \(B(0)\).

## B-10 — Exact cutoff bubble

- Notebook equation:
  \[
  B_\Lambda(0)
  =
  \frac{1}{16\pi^2}
  \left[
  \ln\left(1+\frac{\Lambda^2}{m^2}\right)
  -\frac{\Lambda^2}{\Lambda^2+m^2}
  \right].
  \]
- Relation: derive from B-09.
- Derivation: substitute \(u=k^2\), then use
  \[
  \frac{u}{(u+m^2)^2}
  =\frac{1}{u+m^2}-\frac{m^2}{(u+m^2)^2}.
  \]
- Fields Notes equation/page: no direct quotation of this
  cutoff result used.

## B-11 — Large-cutoff expansion of the bubble

- Notebook equation:
  \[
  B_\Lambda(0)
  =
  \frac{1}{16\pi^2}
  \left[
  \ln\frac{\Lambda^2}{m^2}-1
  +\frac{2m^2}{\Lambda^2}
  +O\!\left(\frac{m^4}{\Lambda^4}\right)
  \right].
  \]
- Relation: derive from B-10.
- Derivation: expand the logarithm and rational term at
  fixed positive \(m^2\).
- Fields Notes equation/page: no direct quotation used.

## B-12 — Derivative identity in the cutoff scheme

- Notebook equation:
  \[
  B_\Lambda(0)
  =-\frac{\partial T_\Lambda}{\partial m^2}.
  \]
- Relation: derive from B-04 and B-10.
- Source of the requested identity: project brief, subsection 1.2.
- Derivation: differentiate the evaluated expression B-04
  with respect to \(m^2\), holding \(\Lambda\) fixed;
  the result equals B-10 exactly.
- Fields Notes equation/page: no direct quotation used.

## B-13 — Exact DR bubble

- Notebook equation:
  \[
  B_{\mathrm{DR}}(0)
  =
  \frac{\mu^\epsilon(m^2)^{d/2-2}}{(4\pi)^{d/2}}
  \Gamma\left(2-\frac d2\right)
  =
  \frac{1}{16\pi^2}
  \left(\frac{4\pi\mu^2}{m^2}\right)^{\epsilon/2}
  \Gamma\left(\frac{\epsilon}{2}\right).
  \]
- Relation: derive by specialization of B-06.
- Fields Notes equations used: Eq. (13.7).
- Printed page: 114.
- Derivation: set \(\alpha=2\), use \(\Gamma(2)=1\),
  multiply by \(\mu^\epsilon\), and substitute \(d=4-\epsilon\).

## B-14 — Laurent expansion of the DR bubble

- Notebook equation:
  \[
  B_{\mathrm{DR}}(0)
  =
  \frac{1}{16\pi^2}
  \left[
  \frac{2}{\epsilon}-\gamma_E
  +\ln\frac{4\pi\mu^2}{m^2}
  \right]+O(\epsilon).
  \]
- Relation: derive from B-13.
- Fields Notes equation underlying the calculation:
  Eq. (13.7), printed p. 114.
- Derivation: expand \(\Gamma(\epsilon/2)\) and the scale
  factor, keeping the pole and finite term.
- Note: the scale-dependent expression shown here is our
  expansion with the project's \(\mu^\epsilon\) convention,
  not a verbatim quotation from the notes.

## B-15 — Derivative identity in dimensional regularization

- Notebook equation:
  \[
  -\frac{\partial T_{\mathrm{DR}}}{\partial m^2}
  =
  \frac{\mu^\epsilon(m^2)^{d/2-2}}{(4\pi)^{d/2}}
  \Gamma\left(2-\frac d2\right)
  =B_{\mathrm{DR}}(0).
  \]
- Relation: derive from B-07 and B-13.
- Fields Notes equation underlying both integrals:
  Eq. (13.7), printed p. 114.
- Derivation: differentiate B-07 at fixed \(\mu\) and \(d\),
  then use \(\Gamma(z+1)=z\Gamma(z)\).
- Additional check: differentiating the pole-plus-finite
  tadpole expression B-08 reproduces B-14.
- Note: the derivative identity itself is established here,
  rather than quoted as a numbered result from the notes.

## B-16 — Zero-momentum normalization conditions

- Notebook equations:
  \[
  \Gamma^{(2)}(0)=m^2,\qquad
  \left.\partial_{p^2}\Gamma^{(2)}\right|_0=1,\qquad
  \Gamma^{(4)}(0)=\lambda.
  \]
- Relation: rewrite.
- Fields Notes: Eqs. (13.12)–(13.13), printed p. 118;
  repeated as Eqs. (13.14)–(13.15) on the same page.
- Explanation: the expansion
  \(\Gamma^{(2)}(p^2)=\tilde m^2+p^2+O(p^4)\)
  is rewritten as separate value and slope conditions.

## B-17 — DR mass and field counterterms

- Notebook equations:
  \[
  \delta Z_\phi^{(1)}=0,\qquad
  \delta m_{\mathrm{DR}}^2=-\frac{\lambda}{2}T_{\mathrm{DR}},
  \]
  together with the Laurent expansion obtained using B-08.
- Relation: derive.
- Equations used:
  - Fields Notes Eqs. (13.14) and (13.16),
    printed pp. 118–119: two-point normalization conditions.
  - Fields Notes Eq. (13.7), printed p. 114:
    scalar DR integral identity, already recorded as B-06.
  - Project brief, subsection 1.3: the explicit Euclidean
    tadpole contribution \(+\lambda T/2\).
  - Notebook B-07–B-08: evaluated DR tadpole.
- Explanation: momentum independence of the tadpole fixes
  the one-loop field counterterm to zero; the mass condition
  fixes the counterterm to minus the complete tadpole correction.
- Source caution: this entry does not quote the unnumbered
  mass-counterterm formula on p. 119. The notebook's sign and
  factor of 1/2 follow explicitly from the project brief.

## B-18 — DR coupling counterterm

- Notebook equation:
  \[
  \delta\lambda_{\mathrm{DR}}
  =\frac{3\lambda^2}{2}B_{\mathrm{DR}}(0),
  \]
  together with its pole-plus-finite expansion.
- Relation: rewrite and derive.
- Fields Notes: Eq. (13.17), printed p. 120, and
  Eq. (13.22), printed p. 122.
- Explanation: the notes write the coupling counterterm as
  \(\delta\tilde\lambda=\tilde\lambda^2 a^{(2)}+\cdots\)
  and give \(a^{(2)}=3I(0)/2\) in Eq. (13.22).
  Replace \(I(0)\) by \(B_{\mathrm{DR}}(0)\), include the
  project's loop factor \(\mu^\epsilon\), and use B-14.

## B-19 — Hard-cutoff mass and field counterterms

- Notebook equations:
  \[
  \delta m_\Lambda^2
  =-\frac{\lambda}{32\pi^2}
  \left[\Lambda^2-m^2\ln(1+\Lambda^2/m^2)\right],
  \qquad \delta Z_\phi^{(1)}=0.
  \]
- Relation: derive.
- Equations used: B-16 and B-04, with the Euclidean
  two-point vertex specified in the project brief.
- Fields Notes basis: Eqs. (13.14) and (13.16),
  printed pp. 118–119.
- Explanation: apply the same normalization conditions
  with the evaluated cutoff tadpole.
- No direct quotation of this cutoff formula from the notes.

## B-20 — Hard-cutoff coupling counterterm

- Notebook equation:
  \[
  \delta\lambda_\Lambda
  =\frac{3\lambda^2}{32\pi^2}
  \left[
  \ln(1+\Lambda^2/m^2)
  -\frac{\Lambda^2}{\Lambda^2+m^2}
  \right].
  \]
- Relation: derive.
- Equations used: B-16 and B-10.
- Fields Notes basis: Eq. (13.15), printed p. 118,
  and the relation \(a^{(2)}=3I(0)/2\) in Eq. (13.22),
  printed p. 122.
- Explanation: use the same subtraction algebra with
  the evaluated cutoff bubble instead of its DR value.
- No direct quotation of this cutoff formula from the notes.

## B-21 — Finite subtracted bubble from DR

- Notebook equation:
  \[
  \Delta B_{\mathrm{DR}}(P^2)
  =-\frac{1}{16\pi^2}\int_0^1dx\,
  \ln\left(1+\frac{x(1-x)P^2}{m^2}\right).
  \]
- Relation: rewrite, with the regulator-limit derivation shown.
- Fields Notes: printed p. 122, first displayed equation
  (unnumbered), specifically its Feynman-parameter integral
  representation of \(I_r(p^2)|_{d=4}\).
- Supporting equations:
  - Eq. (13.18), printed p. 120: definition of \(I(p^2)\).
  - Eq. (13.21), printed p. 121: parameterized bubble.
  - Eq. (13.7), printed p. 114: DR integration identity.
- Explanation: use \(I_r(p^2)=I(p^2)-I(0)\), rename the
  integration parameter to x, and identify the notes' p²
  with the Euclidean P². The project's \(\mu^\epsilon\)
  factor cancels out of the finite regulator-removed difference.

## B-22 — Subtracted bubble with a common cutoff domain

- Notebook equation:
  \[
  \Delta B_\Lambda(P^2)
  =\int_{|k|<\Lambda}\frac{d^4k}{(2\pi)^4}
  \left[
  \frac{1}{(k^2+m^2)((k+P)^2+m^2)}
  -\frac{1}{(k^2+m^2)^2}
  \right].
  \]
- Relation: derive.
- Fields Notes basis: Eq. (13.18), printed p. 120,
  and the subtraction \(I_r(p^2)=I(p^2)-I(0)\)
  appearing below Eq. (13.19) on that page.
- Additional source: project brief, subsection 1.3,
  instruction to form the convergent difference and remove
  the cutoff before shifting loop momentum.
- Explanation: impose the same spherical domain on both
  terms before combining them. This cutoff construction
  is not quoted directly from the notes.

## B-23 — Agreement of the cutoff and DR finite differences

- Notebook equation:
  \[
  \Delta B_{\mathrm{cutoff}}(P^2)
  =-\frac{1}{16\pi^2}\int_0^1dx\,
  \ln\left(1+\frac{x(1-x)P^2}{m^2}\right)
  =\Delta B_{\mathrm{DR}}(P^2).
  \]
- Relation: derive; the resulting integral matches the source.
- Fields Notes: printed p. 122, first displayed equation
  (unnumbered), for the common finite integral representation.
- Additional identity used: printed p. 121, first displayed
  equation (unnumbered),
  \[
  \frac1{AB}=\int_0^1du\,[uA+(1-u)B]^{-2}.
  \]
  This is also the \(\alpha=\beta=1\) specialization of
  the numbered general identity (13.20) on p. 121.
- Explanation: first take \(\Lambda\to\infty\) in B-22.
  Only then parameterize and shift the convergent difference.
  Evaluate its radial integral and compare with B-21.
- The proof using the cutoff limit is our derivation,
  not a direct quotation of the notes' DR calculation.

## B-24 — Value and slope at zero momentum

- Notebook equations:
  \[
  \Delta B(0)=0,\qquad
  \left.\frac{d\Delta B}{dP^2}\right|_0
  =-\frac{1}{96\pi^2m^2}.
  \]
- Relation: derive from B-21 and B-23.
- Fields Notes equation used: printed p. 122,
  first displayed equation (unnumbered), its finite
  Feynman-parameter integral representation.
- Explanation: differentiate under the parameter integral
  and use \(\int_0^1dx\,x(1-x)=1/6\).
- The slope is derived here; it is not quoted as a separate
  numbered result from the supplied notes.


## B-25 — MS coupling pole and bare coupling relation

- Subsection: 1.4; analytically derived, not CAS-checked.
- Equations:
  \[
  \delta\lambda_{\mathrm{MS}}=\frac{3\lambda^2}{16\pi^2\epsilon}+O(\lambda^3),
  \qquad g=\frac{\lambda}{16\pi^2},\qquad
  g_0\equiv\frac{\lambda_0}{16\pi^2}
  =\mu^\epsilon\left[g+\frac{3g^2}{\epsilon}+O(g^3)\right].
  \]
- Relation: derive from the pole of B-14 and the three-channel amplitude B-02.
- Project brief: subsection 1.4; coupling normalization in Part 1 preamble.
- Source caution: g_0 here is dimensionful, of mass dimension epsilon. Field renormalization affects this relation only at higher order than displayed.
- Distinction: B-18 subtracts the finite zero-momentum bubble as well; MS retains only the pole.

## B-26 — Fixed-bare definition and differentiation

- Equations:
  \[
  \beta_g=\left.\mu\frac{dg}{d\mu}\right|_{\lambda_0,m_0^2,\epsilon},\qquad
  0=\epsilon\left[g+\frac{3g^2}{\epsilon}+\cdots\right]
  +\beta_g\left[1+\frac{6g}{\epsilon}+\cdots\right].
  \]
- Relation: derive by differentiating B-25, before removing epsilon.
- Chapter 21 supporting context: Eq. (21.5), printed p. 218 (PDF p. 5), RG equation with dimensionless coupling; text immediately preceding it introduces lambda=mu^(4-d) times a dimensionless coupling. This is context, not a quotation of the fixed-bare MS derivation.

## B-27 — One-loop MS beta function in project normalization

- Equation:
  \[
  \beta_g=-\epsilon g+3g^2+O(g^3).
  \]
- Relation: derive from B-26 by setting beta_g=-epsilon g+b g^2+... and obtaining b=3.
- Chapter 21: printed p. 219 (PDF p. 6), unnumbered small-epsilon beta function following Eq. (21.8): beta(lambda)=-epsilon lambda+3 lambda^2/(4 pi)^2+O(lambda^3).
- Notation conversion: the notes' dimensionless lambda is the project's lambda=16 pi^2 g.
- Scheme caution: Chapter 21 obtains its expression from the finite symmetric-momentum normalization Eq. (21.3), not MS. It supports the leading small-epsilon result; B-27 is independently derived from MS poles. Do not identify the full finite-d scheme-dependent functions.

## B-28 — Perturbative fixed points

- Equations:
  \[
  g_{\mathrm G}^*=0,\qquad g_{\mathrm{WF}}^*=\frac{\epsilon}{3}+O(\epsilon^2).
  \]
- Relation: derive by solving B-27 to the stated order.
- Chapter 21: Eq. (21.9), printed p. 220 (PDF p. 7), lambda_*=(4 pi)^2 epsilon/3+O(epsilon^2); divide by 16 pi^2.
- Scope: small positive epsilon; no stability analysis required by subsection 1.4.

## B-29 — One-loop field counterterm from momentum independence

- Equations:
  \[
  \Sigma_{\mathrm{tad}}^{(1)}(p)=\frac{\lambda}{2}T_{\mathrm{DR}},\qquad
  \frac{\partial\Sigma_{\mathrm{tad}}^{(1)}}{\partial p^2}=0,\qquad
  \delta Z_{\phi,\mathrm{MS}}^{(1)}=0,\quad Z_\phi=1+O(g^2).
  \]
- Relation: derive from the project's two-point vertex and B-08; restates the field result of B-17 in MS.
- Reason: the pole lambda T_DR/2=-g m^2/epsilon+finite has no p^2 dependence. It requires a mass counterterm, delta m_MS^2=+g m^2/epsilon, not a kinetic counterterm.
- Chapter 21 consistency checks: printed p. 218 (PDF p. 5), unnumbered \(\Gamma^{(2)}(p^2)=p^2+O(\lambda^2)\) preceding Eq. (21.7); printed p. 219 (PDF p. 6), unnumbered \(\gamma(\lambda)=O(\lambda^2)\). Those statements concern the massless critical theory; the massive derivation here does not set the tadpole to zero.

## B-30 — Absence of a one-loop momentum-exponent correction

- Equations:
  \[
  \gamma_\phi=\frac12\left.\mu\frac{d\ln Z_\phi}{d\mu}\right|_{\mathrm{bare}}=O(g^2),
  \qquad \eta=2\gamma_\phi(g_*)=O(\epsilon^2),
  \qquad G_{\mathrm{crit}}(p)\propto(p^2)^{-1+\eta/2}.
  \]
- Relation: derive absence of an O(g) anomalous dimension from B-29; use critical scaling relation specified in project subsection 2.2 and g_*=O(epsilon) from B-28.
- Chapter 21: \(\gamma(\lambda)=O(\lambda^2)\), printed p. 219 (PDF p. 6), unnumbered after Eq. (21.8), corroborates the perturbative order.
- Explanation: the tadpole shifts the momentum-independent mass term only. It cannot generate a \(p^2\ln(p^2/\mu^2)\) term or change the kinetic power. The critical power-law statement applies after tuning the mass in Part 2; Part 1 retains \(m^2>0\). No two-loop coefficient or evaluated CAS result is asserted.


## B-31 — Sunset symmetry factor and Euclidean inverse-propagator contribution

- Subsection: 2.1; analytically derived, FeynArts/FeynCalc diagram generation verified.
- Equations:
  \[
  \Delta\Gamma_{\mathrm{sunset}}^{(2)}(p)
  =-\frac{\lambda^2}{6}H(p),
  \qquad
  H(p)=\mu^{2\epsilon}
  \int\frac{d^dk\,d^d\ell}{(2\pi)^{2d}}
  \frac{1}{k^2\ell^2(p-k-\ell)^2}.
  \]
- Relation: derive using Wick rotation and the symmetry factor \(1/6\) from second-order \(\phi^4\) contractions.
- Explanation: Euclidean sign convention gives a minus sign when passing from the connected propagator to the inverse propagator \(\Gamma^{(2)}\).

## B-32 — Massless DR convolution identity

- Equations:
  \[
  J_{\alpha,\beta}(Q)
  =
  \int\frac{d^dq}{(2\pi)^d}
  \frac{1}{(q^2)^\alpha[(Q-q)^2]^\beta}
  =
  \frac{(Q^2)^{d/2-\alpha-\beta}}{(4\pi)^{d/2}}
  \frac{
  \Gamma(\alpha+\beta-d/2)
  \Gamma(d/2-\alpha)
  \Gamma(d/2-\beta)
  }{
  \Gamma(\alpha)\Gamma(\beta)
  \Gamma(d-\alpha-\beta)
  }.
  \]
- Relation: quote and apply using Feynman parameters and shifting loop momentum.
- Source: standard DR master integral used for successive convolutions.

## B-33 — First convolution over the loop momentum \(\ell\)

- Equation:
  \[
  \int\frac{d^d\ell}{(2\pi)^d}
  \frac{1}{\ell^2(p-k-\ell)^2}
  =
  \frac{[(p-k)^2]^{d/2-2}}{(4\pi)^{d/2}}
  \frac{
  \Gamma(2-d/2)\Gamma(d/2-1)^2
  }{
  \Gamma(d-2)
  }.
  \]
- Relation: derive by specializing B-32 to \(\alpha=\beta=1\) and \(Q=p-k\).

## B-34 — Exact sunset integral \(H(p)\) via second convolution

- Equation:
  \[
  H(p)=
  \frac{\mu^{2\epsilon}(p^2)^{d-3}}{(4\pi)^d}
  \frac{
  \Gamma(3-d)\Gamma(d/2-1)^3
  }{
  \Gamma(3d/2-3)
  }.
  \]
- Relation: derive by applying B-32 a second time to integrate over \(k\) with \(\alpha=1\) and \(\beta=2-d/2\).
- Mathematica verification: confirmed via automated convolution script.

## B-35 — Sunset integral in terms of \(\epsilon\) and \(p^2\)

- Equation:
  \[
  H(p)=
  \frac{p^2}{(16\pi^2)^2}
  \left(\frac{4\pi\mu^2}{p^2}\right)^\epsilon
  \frac{
  \Gamma(\epsilon-1)\Gamma(1-\epsilon/2)^3
  }{
  \Gamma(3-3\epsilon/2)
  }.
  \]
- Relation: substitute \(d=4-\epsilon\) into B-34.

## B-36 — Laurent expansion of the sunset integral

- Equation:
  \[
  H(p)=
  -\frac{p^2}{2(16\pi^2)^2}
  \left[
  \frac1\epsilon
  +\ln\frac{4\pi\mu^2}{p^2}
  +\frac{13}{4}-\gamma_E
  \right]
  +O(\epsilon).
  \]
- Relation: derive by expanding the gamma functions and scale factor around \(\epsilon=0\).
- Mathematica verification: confirmed by `Series` expansion of B-34.

## B-37 — Momentum-dependent pole of the sunset integral

- Equation:
  \[
  \left.H(p)\right|_{\mathrm{pole}}
  =
  -\frac{p^2}{2(16\pi^2)^2\epsilon}.
  \]
- Relation: extract the \(1/\epsilon\) pole term from B-36.

## B-38 — Sunset contribution to the inverse propagator and pole

- Equations:
  \[
  \Delta\Gamma_{\mathrm{sunset}}^{(2)}(p)
  =
  \frac{g^2p^2}{12}
  \left[
  \frac1\epsilon
  +\ln\frac{4\pi\mu^2}{p^2}
  +\frac{13}{4}-\gamma_E
  \right]
  +O(g^2\epsilon),
  \qquad
  \left.\Delta\Gamma_{\mathrm{sunset}}^{(2)}(p)\right|_{\mathrm{pole}}
  =\frac{g^2p^2}{12\epsilon}.
  \]
- Relation: combine B-31 and B-36 using \(g=\lambda/(16\pi^2)\).

## B-39 — Vanishing of four-point subdivergence counterterm contributions

- Equations:
  \[
  \Delta\Gamma_{\mathrm{4pt\;CT}}^{(2)}(p)
  \ \propto\
  \delta\lambda_{\mathrm{MS}}\,
  mu^\epsilon\int\frac{d^dq}{(2\pi)^d}\frac1{q^2}
  =0,
  \qquad
  \frac{\partial}{\partial p^2}
  \Delta\Gamma_{\mathrm{4pt\;CT}}^{(2)}(p)=0.
  \]
- Relation: analyze overlapping four-point subgraphs.
- Explanation: replacing divergent four-point subgraphs by local counterterms leaves momentum-independent tadpoles that vanish in massless DR and cannot modify the \(p^2/\epsilon\) pole coefficient.


## B-40 — Sunset contribution with the momentum logarithm explicit

- Notebook location: Part 2, subsection 2.2.
- Equations:
  \[
  \Delta\Gamma_{\mathrm{sunset}}^{(2)}(p)
  =
  \frac{g^2p^2}{12}
  \left[
  \frac1\epsilon
  -\ln\frac{p^2}{\mu^2}
  +C_{\mathrm{MS}}
  \right]
  +O(g^2\epsilon),
  \qquad
  C_{\mathrm{MS}}
  =\ln(4\pi)+\frac{13}{4}-\gamma_E.
  \]
- Relation: rewrite B-38, using
  \(\ln(4\pi\mu^2/p^2)=\ln(4\pi)-\ln(p^2/\mu^2)\).
- Explanation: the Euclidean inverse-propagator contribution is
  \(-\lambda^2H(p)/6\). The negative pole in H therefore gives
  the positive pole \(g^2p^2/(12\epsilon)\).
- Source basis: B-31 and B-36; project subsection 2.2 requests
  the inverse-propagator contribution, including its sign.
- Fields Notes equation/page: no direct quotation used;
  a precise lecture-note locator for the two-loop contribution
  has not been verified.
- Check: user-reported Mathematica output confirms the pole
  coefficient, conditional on the supplied H and prefactor
  \(-\lambda^2/6\). The diagrammatic sign is derived analytically,
  not independently tested by this code.
- Status: derived and Mathematica-checked within this scope.

## B-41 — MS field counterterm and field renormalization constant

- Notebook location: Part 2, subsection 2.2.
- Equations:
  \[
  \phi_0=Z_\phi^{1/2}\phi,
  \qquad
  \delta Z_{\phi,\mathrm{MS}}
  =-\frac{g^2}{12\epsilon}+O(g^3),
  \qquad
  Z_\phi=1-\frac{g^2}{12\epsilon}+O(g^3).
  \]
- Relation: derive by canceling the momentum-dependent pole
  in B-40.
- Explanation: the kinetic counterterm contributes
  \(+\delta Z_\phi p^2\) to the inverse propagator, so
  \[
  \delta Z_\phi p^2+\frac{g^2p^2}{12\epsilon}=0.
  \]
  The higher-order terms in Z_phi may contain further poles.
- Source basis: B-40 and the field-renormalization convention;
  extraction of Z_phi is requested in project subsection 2.2.
- Fields Notes equation/page: no direct quotation used;
  a precise locator for this two-loop MS coefficient remains
  unverified.
- Check: Mathematica solves for the counterterm coefficient
  and confirms cancellation of the \(1/\epsilon\) pole.
- Status: derived and Mathematica-checked by user-reported output.

## B-42 — Finite renormalized inverse propagator

- Notebook location: Part 2, subsection 2.2.
- Equation:
  \[
  \Gamma_R^{(2)}(p)
  =
  p^2\left[
  1+\frac{g^2}{12}
  \left(
  C_{\mathrm{MS}}-\ln\frac{p^2}{\mu^2}
  \right)
  \right]
  +O(g^3),
  \]
  where
  \[
  C_{\mathrm{MS}}
  =\ln(4\pi)+\frac{13}{4}-\gamma_E.
  \]
- Relation: combine the tree inverse propagator, B-40,
  and the counterterm B-41, then remove the regulator.
- Explanation: MS removes the pole only. The finite constant
  remains because no finite field-normalization condition
  is imposed. The scale is the original DR scale mu,
  not an MSbar-redefined scale.
- Source basis: B-40 and B-41.
- Fields Notes equation/page: no direct quotation used.
- Check: the user-reported Mathematica expression is
  algebraically identical and contains no remaining
  \(1/\epsilon\) term.
- Status: derived and Mathematica-checked by user-reported output.

## B-43 — Two-loop field anomalous dimension

- Notebook location: Part 2, subsection 2.2.
- Equations:
  \[
  \gamma_\phi(g)
  =
  \frac12
  \left.\mu\frac{d\ln Z_\phi}{d\mu}\right|_{\mathrm{bare}}
  =
  \frac12\beta_g(g)\frac{\partial\ln Z_\phi}{\partial g}
  =
  \frac{g^2}{12}+O(g^3).
  \]
- Relation: derive from B-41 and
  \(\beta_g=-\epsilon g+3g^2+O(g^3)\), B-27.
- Explanation:
  \[
  \ln Z_\phi=-\frac{g^2}{12\epsilon}+O(g^3),
  \qquad
  \gamma_\phi
  =\frac12(-\epsilon g)
  \left(-\frac{g}{6\epsilon}\right)+O(g^3).
  \]
  Retain the engineering term \(-\epsilon g\) until after
  differentiation. Terms of order \(g^3\) cannot be determined
  consistently without higher-order field counterterms.
- Source basis: project subsection 2.2 supplies the definition
  of gamma_phi. Chapter 21, printed p. 219 (PDF p. 6),
  states \(\gamma(\lambda)=O(\lambda^2)\) in the text immediately
  after Eq. (21.8); this supports the perturbative order,
  not the coefficient derived here.
- Check: Mathematica expands the fixed-bare derivative through
  \(g^2\) and returns \(g^2/12\).
- Status: derived and Mathematica-checked by user-reported output.

## B-44 — Critical exponent eta through order epsilon squared

- Notebook location: Part 2, subsection 2.2.
- Equations:
  \[
  \eta=2\gamma_\phi(g_*)
  =\frac{\epsilon^2}{54}+O(\epsilon^3),
  \qquad
  G_{\mathrm{crit}}(p)
  \propto
  (p^2)^{-1+\epsilon^2/108+O(\epsilon^3)}.
  \]
- Relation: combine B-43 with
  \(g_*=\epsilon/3+O(\epsilon^2)\), B-28.
- Explanation:
  \[
  \eta=\frac{g_*^2}{6}+O(g_*^3).
  \]
  An unknown correction \(c\epsilon^2\) to g_* changes
  \(g_*^2\) only from order \(\epsilon^3\). An unknown
  \(O(g^3)\) term in gamma_phi also contributes only from
  order \(\epsilon^3\). The one-loop fixed point therefore
  suffices through order \(\epsilon^2\).
- Source basis: project subsection 2.2 supplies
  \(\eta=2\gamma_\phi(g_*)\) and
  \(G(p)\propto(p^2)^{-1+\eta/2}\).
  Chapter 21, Eq. (21.9), printed p. 220 (PDF p. 7),
  supplies the leading fixed point in lambda normalization;
  its conversion to g is recorded in B-28.
- Fields Notes locator for the coefficient \(1/54\):
  not verified; this coefficient is derived here.
- Check: Mathematica returns \(\epsilon^2/54\) and confirms
  that adding \(c\epsilon^2\) to g_* does not change the
  result through order \(\epsilon^2\).
- Status: derived and Mathematica-checked by user-reported output.

## B-45 — Finite-logarithm check of the momentum exponent

- Notebook location: Part 2, subsection 2.2.
- Equations: with \(x=p^2/\mu^2>0\), at the fixed point,
  \[
  \frac{\Gamma_R^{(2)}(p)}{\Gamma_R^{(2)}(\mu)}
  =
  x\left[
  1-\frac{g_*^2}{12}\ln x+O(\epsilon^3)
  \right],
  \]
  \[
  \frac{G_R(p)}{G_R(\mu)}
  =
  \frac1x\left[
  1+\frac{g_*^2}{12}\ln x+O(\epsilon^3)
  \right].
  \]
  Comparison with the expansions of
  \(x^{1-\eta/2}\) and \(x^{-1+\eta/2}\) gives
  \[
  \frac{\eta}{2}=\frac{g_*^2}{12},
  \qquad
  \eta=\frac{\epsilon^2}{54}+O(\epsilon^3).
  \]
- Relation: normalize B-42 at \(p^2=\mu^2\), expand the ratio
  consistently, and compare with the critical power law.
- Explanation: normalization cancels C_MS. The negative
  logarithm in the inverse propagator becomes a positive
  logarithm in the propagator, confirming the sign and
  coefficient of eta. The expansion is understood
  perturbatively at fixed x.
- Source basis: B-42 and the critical propagator scaling
  relation specified in project subsection 2.2.
- Fields Notes equation/page: no direct quotation used
  for this normalized finite-logarithm comparison.
- Check: Mathematica confirms both normalized expressions
  agree with the corresponding power-law expansions through
  \(g^2\). Both comparison tests return True.
- Status: derived and Mathematica-checked by user-reported output.


## B-46 — Scaling dimensions of the field and uniform source

- Notebook location: Part 2, subsection 2.3.
- Equations:
  \[
  S_h[\phi]=S[\phi]-\int d^dx\,h\phi(x),
  \qquad
  \Delta_\phi=\frac{d-2+\eta}{2},
  \qquad
  \Delta_h=d-\Delta_\phi=\frac{d+2-\eta}{2}.
  \]
- Relation: derive.
- Explanation: the critical two-point function scales as
  \(\langle\phi(x)\phi(0)\rangle\propto|x|^{-2\Delta_\phi}\),
  corresponding to \(G(p)\propto(p^2)^{-1+\eta/2}\).
  Scale invariance of the integrated source term requires
  \(\Delta_h+\Delta_\phi=d\).
- Source basis: the critical propagator scaling relation used
  in B-44 and the uniform source specified in project
  subsection 2.3.
- Fields Notes equation/page: precise locator not yet verified;
  these relations are derived here, not presented as a
  verified quotation.
- Status: derived.

## B-47 — Critical-isotherm exponent from scaling dimensions

- Notebook location: Part 2, subsection 2.3.
- Equations:
  \[
  M(h)=b^{-\Delta_\phi}M(b^{\Delta_h}h),
  \qquad
  M(h)\propto\operatorname{sgn}(h)
  |h|^{\Delta_\phi/\Delta_h},
  \]
  \[
  \delta=\frac{\Delta_h}{\Delta_\phi}
  =\frac{d+2-\eta}{d-2+\eta}.
  \]
- Relation: derive from B-46.
- Explanation: at criticality choose the scale factor so that
  \(b^{\Delta_h}|h|\) is fixed. Comparing the resulting source
  dependence with
  \(M\propto\operatorname{sgn}(h)|h|^{1/\delta}\)
  gives \(1/\delta=\Delta_\phi/\Delta_h\).
- Conditions: critical fixed-point scaling below four
  dimensions, with the thermal scaling field tuned to zero.
- Source basis: project subsection 2.3 specifies the definition
  of delta and requests this scaling relation.
- Fields Notes equation/page: precise locator not yet verified;
  no direct quotation claimed.
- Status: derived.

## B-48 — Epsilon expansion of the critical-isotherm exponent

- Notebook location: Part 2, subsection 2.3.
- Equation:
  \[
  \delta
  =
  \frac{6-\epsilon-\epsilon^2/54+O(\epsilon^3)}
       {2-\epsilon+\epsilon^2/54+O(\epsilon^3)}
  =
  3+\epsilon+\frac{25}{54}\epsilon^2
  +O(\epsilon^3).
  \]
- Relation: derive by substituting \(d=4-\epsilon\) and
  \(\eta=\epsilon^2/54+O(\epsilon^3)\), B-44, into B-47,
  then expanding the ratio consistently.
- Explanation: expand through epsilon squared before setting
  epsilon to one. Substitution into the unexpanded ratio
  would retain uncontrolled higher-order terms generated
  by the denominator.
- Source basis: B-44, B-47, and the expansion order specified
  in project subsection 2.3.
- Fields Notes equation/page: no direct quotation used for
  this series coefficient.
- Check: Mathematica Series code supplied; execution has not
  yet been reported.
- Status: derived.

## B-49 — Three-dimensional truncated exponent predictions

- Notebook location: Part 2, subsection 2.3.
- Equations:
  \[
  \eta_{\epsilon^2}^{(d=3)}
  =\frac1{54}\simeq0.0185185,
  \qquad
  \delta_{\epsilon^2}^{(d=3)}
  =\frac{241}{54}\simeq4.462963.
  \]
- Relation: set epsilon to one in the truncated expansions
  B-44 and B-48.
- Explanation: these are unresummed epsilon-expansion
  estimates through order epsilon squared, not exact
  three-dimensional exponents or controlled error bounds
  at epsilon equal to one.
- Source basis: B-44 and B-48.
- Fields Notes equation/page: no direct quotation used.
- Check: numerical evaluation included in the supplied
  comparison-table code; execution not yet reported.
- Status: derived.

## B-50 — Fluid critical-isotherm equation of state

- Notebook location: Part 2, subsection 2.3.
- Equations:
  \[
  M\propto\rho-\rho_c,
  \qquad
  h\propto\mu_{\mathrm{chem}}-\mu_{\mathrm{chem},c}
  \propto P-P_c
  \quad (T=T_c),
  \]
  \[
  \frac{P-P_c}{P_c}
  \sim
  A\,\operatorname{sgn}(\rho-\rho_c)
  \left|\frac{\rho-\rho_c}{\rho_c}\right|^\delta.
  \]
- Relation: derive from the critical response in B-47 and
  the leading identification of fluid scaling variables.
- Explanation: at fixed temperature the Gibbs–Duhem relation
  gives \(dP=n\,d\mu_{\mathrm{chem}}\). Since the number density
  tends to a nonzero critical value,
  \[
  P-P_c
  =n_c(\mu_{\mathrm{chem}}-\mu_{\mathrm{chem},c})
  +\text{subleading terms}.
  \]
  Inverting the critical response yields the pressure-density
  power law. The amplitude A absorbs nonuniversal
  normalization factors.
- Notation: mu_chem denotes chemical potential and is distinct
  from the DR renormalization scale mu.
- Conditions: leading asymptotic behavior on the critical
  isotherm. Real-fluid asymmetry, field mixing, and corrections
  to scaling can modify subleading terms.
- Source basis: project subsection 2.3 requests the fluid
  identifications and normalized equation of state;
  Gibbs–Duhem supplies the thermodynamic justification.
- Fields Notes equation/page: precise locator not yet verified;
  no direct quotation claimed.
- Status: derived.

## B-51 — Critical scattering slope

- Notebook location: Part 2, subsection 2.3.
- Equations:
  \[
  S(q)\propto q^{-2+\eta},
  \qquad
  \xi^{-1}\ll q\ll a^{-1},
  \]
  \[
  \frac{d\ln S(q)}{d\ln q}=-2+\eta,
  \qquad
  (-2+\eta)_{\epsilon^2}^{(d=3)}
  =-\frac{107}{54}\simeq-1.981481.
  \]
- Relation: derive from the critical propagator exponent and
  substitute B-49.
- Explanation: critical density fluctuations share the leading
  order-parameter scaling. The momentum window excludes
  finite-correlation-length behavior at small q and molecular
  structure at large q. The stated slope is the leading
  scaling prediction, neglecting corrections to scaling.
- Source basis: project subsection 2.3 specifies the scattering
  law and momentum window; eta is obtained in B-44.
- Fields Notes equation/page: precise locator not yet verified.
- Check: numerical slope included in the supplied table code;
  execution not yet reported.
- Status: derived.

## B-52 — Bootstrap benchmark and water comparison inputs

- Notebook location: Part 2, subsection 2.3.
- Equations and supplied inputs:
  \[
  \Delta_\sigma=0.518148806(24),
  \qquad
  \eta_B=2\Delta_\sigma-1,
  \qquad
  \delta_B=\frac3{\Delta_\sigma}-1,
  \qquad
  s_B=-2+\eta_B,
  \]
  \[
  \delta_{\mathrm{water}}=4.324.
  \]
- Relation: use the supplied benchmark dimension in the
  three-dimensional scaling identities. The expression for
  delta_B follows from
  \(\delta=(d-\Delta_\phi)/\Delta_\phi\) at d=3, with
  \(\Delta_\phi=\Delta_\sigma\).
- Source of numerical inputs: project subsection 2.3,
  comparison-values block.
  - Bootstrap: C.-H. Chang et al., JHEP 03 (2025) 136,
    Table 1, as cited by the project.
  - Water: J. Straub, Physica 63 (1973) 492–498,
    Table I and p. 495, as cited by the project.
- Source caution: the original benchmark publications have
  not been independently inspected here. Numerical inputs
  are transcribed from the project brief.
- Explanation: the comparison table contains the truncated
  epsilon-expansion predictions B-49/B-51, bootstrap-derived
  central values, and the supplied water delta. No water eta
  or scattering slope is supplied, so those entries are left
  blank rather than inferred.
- Uncertainty: the supplied code uses the bootstrap central
  value; it does not propagate the quoted uncertainty.
- Check: Mathematica code supplied to construct the comparison
  table and compute the relative difference from the water
  delta. Execution results have not yet been reported.
- Status: derived; numerical comparison execution open.