# IBM Qiskit Track: Deep Dive & Hardware Execution

This directory contains advanced implementations of quantum information protocols using IBM Qiskit, spanning exact mathematical derivations, ideal statevector simulations, realistic NISQ hardware noise modeling, and execution workflows on physical superconducting processors.

---

## Directory Contents

| Notebook | Focus | Key Topics |
| :--- | :--- | :--- |
| [`First_Steps.ipynb`](First_Steps.ipynb) | Theory, Simulation & Hardware | Bell state $\vert\Phi^+\rangle$, Bloch sphere multivectors, QASM sampling, NISQ noise ($T_1, T_2$, depolarizing), state tomography, fidelity, IBM Quantum transpilation |
| [`Quantum_Teleportation.ipynb`](Quantum_Teleportation.ipynb) | Quantum Protocol | No-cloning theorem, 3-qubit teleportation circuit, Bell basis measurement, conditional Pauli corrections ($X, Z$) |

---

## Technical Overview

### 1. Bell State Preparation and Characterization (`First_Steps.ipynb`)

#### Theoretical Derivation
The composite state space of two qubits is defined on the tensor product Hilbert space $\mathcal{H} = \mathcal{H}_1 \otimes \mathcal{H}_2 \cong \mathbb{C}^4$, equipped with the computational basis:

$$
\{\vert 00 \rangle, \vert 01 \rangle, \vert 10 \rangle, \vert 11 \rangle\}
$$

Starting from the ground state $\vert 00 \rangle$, applying a Hadamard gate on qubit 0 and a subsequent CNOT gate creates the maximally entangled Bell state $\vert\Phi^+\rangle$:

$$
\vert 00 \rangle \xrightarrow{H \otimes I} \frac{1}{\sqrt{2}} (\vert 0 \rangle + \vert 1 \rangle) \otimes \vert 0 \rangle = \frac{1}{\sqrt{2}} (\vert 00 \rangle + \vert 10 \rangle) \xrightarrow{CNOT_{0 \to 1}} \vert\Phi^+\rangle = \frac{1}{\sqrt{2}} (\vert 00 \rangle + \vert 11 \rangle)
$$

#### Bloch Sphere and Reduced Density Matrices
Because $\vert\Phi^+\rangle$ is a maximally entangled pure state, the partial trace over either subsystem yields a maximally mixed state:

$$
\rho_A = \operatorname{Tr}_B (\vert\Phi^+\rangle\langle\Phi^+\vert) = \frac{1}{2} \vert 0 \rangle \langle 0 \vert + \frac{1}{2} \vert 1 \rangle \langle 1 \vert = \frac{1}{2} I
$$

On the single-qubit Bloch sphere, this state is located at the origin ($r = 0$), demonstrating that neither qubit possesses an independent pure state.

#### Realistic NISQ Noise Modeling
To replicate physical quantum processors such as `ibmq_lima`, the notebook configures a custom noise model incorporating:
* Single-qubit depolarizing error: $p_1 = 0.02$
* Two-qubit CNOT gate depolarizing error: $p_2 = 0.05$
* Thermal relaxation: longitudinal relaxation time $T_1 = 50\,\mu\text{s}$, transverse dephasing time $T_2 = 70\,\mu\text{s}$, gate duration $t_{\text{gate}} = 50\,\text{ns}$

#### State Tomography and Fidelity
The impact of decoherence is quantified using state fidelity:

$$
F(\rho, \sigma) = \left( \operatorname{Tr} \sqrt{ \sqrt{\rho} \sigma \sqrt{\rho} } \right)^2
$$

The real and imaginary components of the reconstructed density matrix $\rho_{\text{noisy}}$ are visualized in 3D city plots.

#### Physical Hardware Transpilation
The circuit is transpiled down to the native basis gates $\{cx, id, rz, sx, x\}$ of IBM superconducting processors, respecting physical coupling topology.

---

### 2. Quantum Teleportation Protocol (`Quantum_Teleportation.ipynb`)

The quantum teleportation protocol transfers an arbitrary unknown quantum state $\vert\psi\rangle = \alpha\vert 0\rangle + \beta\vert 1\rangle$ from Alice to Bob using an entangled pair and 2 classical bits:

1. **State Initialization**: Alice holds qubit $A$ in state $\vert\psi\rangle$.
2. **Entanglement Distribution**: A Bell pair $\vert\Phi^+\rangle_{BC} = \frac{1}{\sqrt{2}}(\vert 00\rangle + \vert 11\rangle)$ is distributed between Alice (qubit $B$) and Bob (qubit $C$).
3. **Alice's Operations**: Alice applies $CNOT_{A \to B}$ followed by $H_A$.
4. **State Factorization**: Expanding the system reveals the correlations:

$$
\vert\Psi_3\rangle = \frac{1}{2} \Big[ \vert 00 \rangle_{AB} (\alpha\vert 0\rangle + \beta\vert 1\rangle)_C + \vert 01 \rangle_{AB} (\alpha\vert 1\rangle + \beta\vert 0\rangle)_C + \vert 10 \rangle_{AB} (\alpha\vert 0\rangle - \beta\vert 1\rangle)_C + \vert 11 \rangle_{AB} (\alpha\vert 1\rangle - \beta\vert 0\rangle)_C \Big]
$$

5. **Measurement & Correction**: Alice measures qubits $A$ and $B$, obtaining classical bits $c_0, c_1$. Bob applies conditional recovery operators:
   * Outcome `00`: $I$
   * Outcome `01`: $X$
   * Outcome `10`: $Z$
   * Outcome `11`: $ZX$

---

## How to Run

Activate your environment and start Jupyter:

```bash
cd qiskit
jupyter notebook
```

To run on IBM Quantum physical processors, configure your API credentials once:

```python
from qiskit_ibm_runtime import QiskitRuntimeService

QiskitRuntimeService.save_account(
    channel="ibm_quantum",
    token="YOUR_IBM_QUANTUM_API_TOKEN",
    overwrite=True
)
```
