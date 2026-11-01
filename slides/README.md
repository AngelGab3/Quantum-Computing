# Workshop Materials: Lecture Slides

This directory contains the slide deck presented at the **Verano STEM UDLAP 2026** workshop.

---

## Document Details

* **Title:** Una Brevísima Introducción a la Computación Cuántica
* **File:** [`A very brief introduction to quantum computing (workshop slides).pdf`](A%20very%20brief%20introduction%20to%20quantum%20computing%20(workshop%20slides).pdf)
* **Pages:** 57 slides
* **Institution:** Universidad de las Américas Puebla (UDLAP)
* **Presenters:**
  * Gabriel Velázquez (*Lic. en Física*)
  * Martha Heredia (*Ing. en Sistemas Computacionales*)
  * Rosh Guadiana (*Ing. Biomédica*)

---

## Curriculum Breakdown

### Section 1: Why Quantum Computing?
* Physical limits of classical computing and the slowdown of Moore's Law (sub-nanometer scales, quantum tunneling, thermal dissipation).
* Intractable computational problems: exponential ($2^n$) and factorial ($n!$) scaling (molecular simulation, traveling salesperson problem).

### Section 2: Historical Foundations
* Key developments in early quantum mechanics: Rutherford nuclear model, Bohr energy quantization, Planck's blackbody distribution, Einstein's photoelectric effect.
* Richard Feynman's 1981 challenge: simulating nature with quantum-mechanical systems instead of classical approximations.

### Section 3: Mathematical Formalism
* Vector spaces, complex numbers, and Dirac bra-ket notation ($\vert\psi\rangle, \langle\psi\vert, \langle\phi\vert\psi\rangle$).
* Hilbert space $\mathcal{H}$, computational basis vectors $\vert 0\rangle = \begin{pmatrix}1\\0\end{pmatrix}$, $\vert 1\rangle = \begin{pmatrix}0\\1\end{pmatrix}$.
* Born rule and normalization: $\langle\psi\vert\psi\rangle = \vert\alpha\vert^2 + \vert\beta\vert^2 = 1$.
* Operators: unitary matrices ($U^\dagger U = I$) guaranteeing reversibility; Hermitian matrices ($H^\dagger = H$) corresponding to physical observables.
* Tensor product $\mathcal{H}^{\otimes n}$ and exponential Hilbert space growth $\dim(\mathcal{H}^{\otimes n}) = 2^n$.

### Section 4: Physical Phenomena
* De Broglie wave-particle duality ($p = h/\lambda$).
* The double-slit experiment across classical particles, classical waves, single electrons, and observer-induced state collapse.
* Superposition and quantum interference of probability amplitudes.
* Heisenberg uncertainty principle: $\Delta x \Delta p_x \ge \hbar / 2$.
* Quantum entanglement: composite states that cannot be factored as independent tensor products.

### Section 5: Quantum Computation Mechanics
* Classical bits vs. quantum qubits.
* Bloch sphere geometry: $\vert\psi\rangle = \cos(\theta/2)\vert 0\rangle + e^{i\phi}\sin(\theta/2)\vert 1\rangle$.
* Matrix representations of single- and two-qubit logic gates (Pauli-$X$, Pauli-$Z$, Hadamard $H$, CNOT).

### Section 6: Hardware Implementations and Open Challenges
* Physical qubit technologies: superconducting circuits (dilution refrigeration at $\sim 15\,\text{mK}$) and trapped ions.
* Environmental decoherence and fault tolerance (ratio of physical to logical qubits).
* Target applications: pharmaceutical molecular simulation, machine learning acceleration, post-quantum cryptography (PQC), and logistics optimization.
