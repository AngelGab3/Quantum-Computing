<div align="center">

# Quantum Computing
### *From Mathematical Foundations to NISQ Simulation & Physical Hardware*

[![Python](https://img.shields.io/badge/Python-3.9%20%7C%203.10%20%7C%203.11%20%7C%203.12-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Qiskit](https://img.shields.io/badge/Qiskit-1.0+-6929C4?style=for-the-badge&logo=qiskit&logoColor=white)](https://qiskit.org/)
[![Cirq](https://img.shields.io/badge/Google_Cirq-1.3+-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://quantumai.google/cirq)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Workshop](https://img.shields.io/badge/UDLAP-Verano_STEM_2026-006341?style=for-the-badge)](https://www.udlap.mx/)
[![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)](LICENSE)

**Language / Idioma:** [English (Current)](README.md) &nbsp;|&nbsp; [Español](README.es.md)

---

</div>

## Overview

This repository contains a modular collection of quantum computing implementations and lecture materials from the **Verano STEM UDLAP 2026** workshop (*"Una Brevísima Introducción a la Computación Cuántica"*).

The repository connects abstract quantum mechanics with modern quantum software engineering across two core frameworks:
* **IBM Qiskit**: Analytical derivations, density matrix tomography, realistic NISQ noise modeling ($T_1, T_2$, depolarizing error), and physical hardware transpilation.
* **Google Cirq**: Algorithmic prototyping, quantum random number generation (QRNG), Born rule convergence, and parametric teleportation.

---

## Repository Structure

```text
Quantum-Computing/
├── qiskit/        # IBM Qiskit implementations and NISQ hardware analysis
├── cirq/          # Google Cirq algorithmic experiments and simulations
├── slides/        # Lecture presentation slides from Verano STEM UDLAP 2026
├── requirements.txt
├── .gitignore
├── LICENSE
├── README.md      # English portal documentation
└── README.es.md   # Documentación general en español
```

---

## Directory Modules

### 1. [IBM Qiskit Track](qiskit/)
Comprehensive studies focusing on mathematical rigor, decoherence, and hardware execution:
* [`First_Steps.ipynb`](qiskit/First_Steps.ipynb): Entangled Bell state $\vert\Phi^+\rangle$ evolution, Bloch sphere multivectors, realistic NISQ noise modeling based on `ibmq_lima`, state tomography, fidelity calculation, and IBM Quantum hardware transpilation.
* [`Quantum_Teleportation.ipynb`](qiskit/Quantum_Teleportation.ipynb): Step-by-step derivation and circuit implementation of the 3-qubit teleportation protocol with conditional Pauli corrections.
* Detailed guide: [qiskit/README.md](qiskit/README.md).

### 2. [Google Cirq Track](cirq/)
Simulations and algorithmic patterns using Google Cirq:
* [`Bell_State_with_Cirq.ipynb`](cirq/Bell_State_with_Cirq.ipynb): EPR pair generation using `LineQubit`.
* [`Hadamard_Transform_with_Cirq.ipynb`](cirq/Hadamard_Transform_with_Cirq.ipynb): Single-qubit superposition on `GridQubit`.
* [`Measurement_Convergence_with_Cirq.ipynb`](cirq/Measurement_Convergence_with_Cirq.ipynb): Law of large numbers validation for Born rule probabilities ($N \in [10, 1000]$).
* [`Quantum_Number_Generator_with_Cirq.ipynb`](cirq/Quantum_Number_Generator_with_Cirq.ipynb): True Quantum Random Number Generator (QRNG) with dynamic qubit scaling and rejection sampling.
* [`Quantum_Teleportation_with_Cirq.ipynb`](cirq/Quantum_Teleportation_with_Cirq.ipynb): Parametric state teleportation with feedforward gates.
* Detailed guide: [cirq/README.md](cirq/README.md).

### 3. [Workshop Slides](slides/)
The complete 57-slide presentation covering the physical limits of Moore's Law, Feynman's challenge, mathematical foundations, interference, entanglement, and hardware topologies.
* Detailed syllabus: [slides/README.md](slides/README.md).

---

## Quickstart & Installation

### 1. Clone and Set Up Virtual Environment
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

## Authors & Acknowledgments

* **Gabriel Velázquez** — *Lic. en Física* (Lead author & notebook implementations)
* **Martha Heredia** — *Ing. en Sistemas Computacionales* (Workshop instructor)
* **Rosh Guadiana** — *Ing. Biomédica* (Workshop instructor)

Developed for and presented at **Verano STEM UDLAP 2026** (*Universidad de las Américas Puebla*).

---

## License

This project is open-source under the [MIT License](LICENSE).
