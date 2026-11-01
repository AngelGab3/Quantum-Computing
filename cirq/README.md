# Google Cirq Track: Algorithmic Prototyping & Simulations

This directory contains personal study notes and implementations of foundational quantum algorithms and statistical simulation experiments by Gabriel Velázquez using Google Cirq.

---

## Directory Contents

| Notebook | Focus | Key Topics |
| :--- | :--- | :--- |
| [`Bell_State_with_Cirq.ipynb`](Bell_State_with_Cirq.ipynb) | Entanglement | `LineQubit`, Bell state circuit, Hadamard, CNOT, measurement histogram |
| [`Hadamard_Transform_with_Cirq.ipynb`](Hadamard_Transform_with_Cirq.ipynb) | Superposition | `GridQubit`, single-qubit Hadamard gate, projective measurement statistics |
| [`Measurement_Convergence_with_Cirq.ipynb`](Measurement_Convergence_with_Cirq.ipynb) | Statistical Physics | Law of large numbers, Born rule convergence $\hat{P}(0) \to 0.5$ across $N \in [10, 1000]$ shots |
| [`Quantum_Number_Generator_with_Cirq.ipynb`](Quantum_Number_Generator_with_Cirq.ipynb) | Applications | True Quantum Random Number Generator (QRNG), $k = \lceil\log_2(M)\rceil$ qubits, rejection sampling |
| [`Quantum_Teleportation_with_Cirq.ipynb`](Quantum_Teleportation_with_Cirq.ipynb) | Protocols | Parametric state teleportation ($H, X, Y, I$), dynamic feedforward corrections with CNOT and CZ |

---

## Technical Overview

### 1. Superposition and Entanglement
* **Single-Qubit Superposition (`Hadamard_Transform_with_Cirq.ipynb`)**: Demonstrates mapping the computational basis state $\vert 0\rangle$ to the symmetric superposition state $\vert +\rangle = \frac{1}{\sqrt{2}}(\vert 0\rangle + \vert 1\rangle)$ on a physical 2D grid qubit `cirq.GridQubit(0, 0)`.
* **Two-Qubit Entanglement (`Bell_State_with_Cirq.ipynb`)**: Constructs an EPR state using linear register qubits `cirq.LineQubit.range(2)` and verifies perfect correlation in measurement outcomes.

### 2. Born Rule Measurement Convergence (`Measurement_Convergence_with_Cirq.ipynb`)
This experiment provides empirical verification of the Born rule and the Law of Large Numbers in quantum systems:

* A single qubit in state $\vert +\rangle$ is measured $N$ times, with $N$ varying from 10 to 1,000.
* The empirical frequency estimator:

$$
\hat{P}(0) = \frac{N_0}{N}
$$

* The resulting trajectory illustrates asymptotic convergence toward the theoretical expectation value $P(0) = 0.5$, showing statistical variance decaying at the rate $\mathcal{O}(1/\sqrt{N})$.

### 3. Quantum Random Number Generator (`Quantum_Number_Generator_with_Cirq.ipynb`)
Implements an unbiased true quantum random number generator for arbitrary intervals $[low, high)$:

1. **Qubit Allocation**: Computes the minimum number of required qubits:

$$
k = \lceil \log_2(high - low) \rceil
$$

2. **Equal Superposition**: Applies Hadamard gates across all $k$ register qubits:

$$
\vert\psi\rangle = H^{\otimes k} \vert 0\rangle^{\otimes k} = \frac{1}{\sqrt{2^k}} \sum_{x=0}^{2^k-1} \vert x\rangle
$$

3. **Measurement and Conversion**: Collapses the state and converts the resulting bitstring into a non-negative integer.
4. **Rejection Sampling**: Rejects values outside the requested interval to eliminate boundary bias.

### 4. Parametric Quantum Teleportation (`Quantum_Teleportation_with_Cirq.ipynb`)
Implements a modular teleportation circuit that supports arbitrary state preparation ($H, X, Y, I$) on Alice's data qubit, with conditional corrections executed via `cirq.CNOT` and `cirq.CZ`.

---

## How to Run

```bash
cd cirq
jupyter notebook
```
