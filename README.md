<div align="center">

# Quantum Computing
### *A Personal Learning Journey from Theoretical Foundations to NISQ Reality*

[![Author](https://img.shields.io/badge/Author-Gabriel_Velázquez-0052CC?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AngelGab3)
[![Python](https://img.shields.io/badge/Python-3.9%20%7C%203.10%20%7C%203.11%20%7C%203.12-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Qiskit](https://img.shields.io/badge/Qiskit-1.0+-6929C4?style=for-the-badge&logo=qiskit&logoColor=white)](https://qiskit.org/)
[![Cirq](https://img.shields.io/badge/Google_Cirq-1.3+-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://quantumai.google/cirq)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

**Language / Idioma:** [English (Current)](README.md) &nbsp;|&nbsp; [Español](README.es.md)

---

</div>

## Overview

This repository documents the personal quantum computing learning journey, study notes, and research implementations of **Gabriel Velázquez** (*Lic. en Física*).

The project is structured to track progression from fundamental quantum physics and mathematical formalism (Hilbert spaces, Dirac bra-ket algebra, tensor products) into hands-on quantum software engineering across two major quantum platforms:
* **IBM Qiskit**: Analytical derivations, reduced density matrix representations on the Bloch sphere, realistic NISQ hardware noise modeling ($T_1, T_2$, gate depolarization), state tomography, and circuit transpilation for physical superconducting quantum devices.
* **Google Cirq**: Algorithmic prototyping, quantum random number generation (QRNG) with rejection sampling, empirical validation of Born's rule convergence, and parametric teleportation.

The repository also includes the slide deck from the introductory workshop *"Una Brevísima Introducción a la Computación Cuántica"* (Verano STEM UDLAP 2026), delivered collaboratively with Martha Heredia and Rosh Guadiana.

---

## Repository Structure

```text
Quantum-Computing/
├── qiskit/        # IBM Qiskit study notebooks and NISQ hardware experiments
├── cirq/          # Google Cirq algorithmic implementations and simulations
├── slides/        # Workshop slides (co-authored for Verano STEM UDLAP 2026)
├── requirements.txt
├── .gitignore
├── LICENSE
├── README.md      # English portal documentation
└── README.es.md   # Documentación general en español
```

---

## Directory Modules

### 1. [IBM Qiskit Track](qiskit/)
Personal study notes emphasizing theoretical depth, mathematical rigor, and realistic physical device modeling:
* [`First_Steps.ipynb`](qiskit/First_Steps.ipynb): Entangled Bell state $\vert\Phi^+\rangle$ evolution, Bloch multivectors for entangled subsystems, custom noise modeling based on IBM's `ibmq_lima`, state tomography, fidelity analysis, and transpilation targeting physical basis gates $\{cx, id, rz, sx, x\}$.
* [`Quantum_Teleportation.ipynb`](qiskit/Quantum_Teleportation.ipynb): Complete analytical derivation and quantum circuit implementation of the 3-qubit teleportation protocol with conditional Pauli corrections.
* Module documentation: [qiskit/README.md](qiskit/README.md).

### 2. [Google Cirq Track](cirq/)
Algorithmic prototyping, quantum measurement statistics, and simulation workflows using Google Cirq:
* [`Bell_State_with_Cirq.ipynb`](cirq/Bell_State_with_Cirq.ipynb): EPR pair preparation on linear register qubits `cirq.LineQubit`.
* [`Hadamard_Transform_with_Cirq.ipynb`](cirq/Hadamard_Transform_with_Cirq.ipynb): Single-qubit superposition on a 2D grid qubit `cirq.GridQubit`.
* [`Measurement_Convergence_with_Cirq.ipynb`](cirq/Measurement_Convergence_with_Cirq.ipynb): Empirical confirmation of the Law of Large Numbers for Born rule probabilities across $N \in [10, 1000]$ shots.
* [`Quantum_Number_Generator_with_Cirq.ipynb`](cirq/Quantum_Number_Generator_with_Cirq.ipynb): True Quantum Random Number Generator (QRNG) for arbitrary intervals using logarithmic qubit allocation and rejection sampling.
* [`Quantum_Teleportation_with_Cirq.ipynb`](cirq/Quantum_Teleportation_with_Cirq.ipynb): Parametric state teleportation with feedforward measurement corrections.
* Module documentation: [cirq/README.md](cirq/README.md).

### 3. [Workshop Slides](slides/)
The 57-slide presentation deck *"Una Brevísima Introducción a la Computación Cuántica"* presented at Verano STEM UDLAP 2026.
* Presenters: Gabriel Velázquez, Martha Heredia, Rosh Guadiana.
* Syllabus and section breakdown: [slides/README.md](slides/README.md).

---

## Quickstart & Installation

### 1. Clone Repository and Set Up Environment
```bash
git clone https://github.com/AngelGab3/Quantum-Computing.git
cd Quantum-Computing

python3 -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\Activate.ps1
```

### 2. Install Dependencies
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 3. Launch Notebooks
```bash
jupyter lab
# or
jupyter notebook
```

---

## Authors & Collaborators

* **Gabriel Velázquez** — *Lic. en Física*  
  Repository author, research notebooks, and circuit implementations.

### Workshop Collaborators (Lecture Slides)
* **Martha Heredia** — *Ing. en Sistemas Computacionales*  
  Co-author and co-instructor for the workshop presentation *'Una Brevísima Introducción a la Computación Cuántica'* ([`slides/`](slides/)).
* **Rosh Guadiana** — *Ing. Biomédica*  
  Co-author and co-instructor for the workshop presentation *'Una Brevísima Introducción a la Computación Cuántica'* ([`slides/`](slides/)).

---

## License

This project is open-source under the [MIT License](LICENSE).
