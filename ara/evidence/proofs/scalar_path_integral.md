# Scalar Path Integral Derivation

## Sources
- Peskin & Schroeder, *An Introduction to Quantum Field Theory*, §9.2

## Derivation
The generating functional for the free scalar field is:
$$Z[j] = \int \mathcal{D}\phi \exp\left(i \int d^4x (\mathcal{L}_0 + j\phi)\right)$$
where $\mathcal{L}_0 = -\frac{1}{2}\phi(\square + m^2 - i\epsilon)\phi$.
Completing the square with $\phi'(x) = \phi(x) - \int dy \Delta_F(x-y)j(y)$:
$$Z[j] = Z[0] \exp\left(-\frac{1}{2} \int dx dy j(x) \Delta_F(x-y) j(y)\right)$$
Taking functional derivatives $\frac{\delta}{\delta j}$ yields the correlation functions (Wick's theorem).
