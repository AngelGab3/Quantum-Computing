<div align="center">

# Computación Cuántica
### *De los Fundamentos Matemáticos a la Simulación NISQ y Hardware Físico*

[![Python](https://img.shields.io/badge/Python-3.9%20%7C%203.10%20%7C%203.11%20%7C%203.12-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Qiskit](https://img.shields.io/badge/Qiskit-1.0+-6929C4?style=for-the-badge&logo=qiskit&logoColor=white)](https://qiskit.org/)
[![Cirq](https://img.shields.io/badge/Google_Cirq-1.3+-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://quantumai.google/cirq)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Taller](https://img.shields.io/badge/UDLAP-Verano_STEM_2026-006341?style=for-the-badge)](https://www.udlap.mx/)
[![Licencia](https://img.shields.io/badge/Licencia-MIT-yellow?style=for-the-badge)](LICENSE)

**Idioma / Language:** [Español (Actual)](README.es.md) &nbsp;|&nbsp; [English](README.md)

---

</div>

## Visión General

Este repositorio contiene una colección modular de implementaciones y material didáctico de computación cuántica originados en el taller **Verano STEM UDLAP 2026** (*"Una Brevísima Introducción a la Computación Cuántica"*).

El repositorio conecta la mecánica cuántica analítica con el desarrollo moderno de software cuántico mediante dos herramientas centrales:
* **IBM Qiskit**: Derivaciones rigurosas, tomografía de matrices de densidad, modelado realista de ruido NISQ ($T_1, T_2$, error despolarizante) y transpilación a procesadores físicos.
* **Google Cirq**: Prototipado de algoritmos, generación cuántica de números aleatorios (QRNG), convergencia de la regla de Born y teletransportación cuántica paramétrica.

---

## Estructura del Repositorio

```text
Quantum-Computing/
├── qiskit/        # Implementaciones en IBM Qiskit y análisis de hardware NISQ
├── cirq/          # Experimentos algorítmicos y simulaciones en Google Cirq
├── slides/        # Presentación del taller en Verano STEM UDLAP 2026
├── requirements.txt
├── .gitignore
├── LICENSE
├── README.md      # Documentación principal en inglés
└── README.es.md   # Documentación general en español
```

---

## Módulos y Carpetas

### 1. [Módulo IBM Qiskit](qiskit/)
Estudios teóricos y de hardware cuántico:
* [`First_Steps.ipynb`](qiskit/First_Steps.ipynb): Preparación del estado de Bell $\vert\Phi^+\rangle$, multivectores en la esfera de Bloch, modelo de ruido para `ibmq_lima`, tomografía de estado, cálculo de fidelidad y transpilación a hardware de IBM Quantum.
* [`Quantum_Teleportation.ipynb`](qiskit/Quantum_Teleportation.ipynb): Derivación matemática e implementación del circuito de teletransportación de 3 qubits con correcciones condicionales de Pauli.
* Documentación detallada: [qiskit/README.md](qiskit/README.md).

### 2. [Módulo Google Cirq](cirq/)
Simulaciones de física estadística y diseño algorítmico:
* [`Bell_State_with_Cirq.ipynb`](cirq/Bell_State_with_Cirq.ipynb): Generación de pares EPR mediante `LineQubit`.
* [`Hadamard_Transform_with_Cirq.ipynb`](cirq/Hadamard_Transform_with_Cirq.ipynb): Superposición de un qubit en `GridQubit`.
* [`Measurement_Convergence_with_Cirq.ipynb`](cirq/Measurement_Convergence_with_Cirq.ipynb): Validación de la ley de los grandes números para la regla de Born ($N \in [10, 1000]$).
* [`Quantum_Number_Generator_with_Cirq.ipynb`](cirq/Quantum_Number_Generator_with_Cirq.ipynb): Generador Cuántico de Números Aleatorios (QRNG) con escalamiento logarítmico y muestreo por rechazo.
* [`Quantum_Teleportation_with_Cirq.ipynb`](cirq/Quantum_Teleportation_with_Cirq.ipynb): Teletransportación paramétrica con compuertas dinámicas controladas.
* Documentación detallada: [cirq/README.md](cirq/README.md).

### 3. [Diapositivas del Taller](slides/)
Presentación oficial de 57 diapositivas con los fundamentos teóricos, límites de la Ley de Moore, reto de Feynman, álgebra lineal cuántica, interferencia y plataformas de hardware.
* Temario completo: [slides/README.md](slides/README.md).

---

## Guía Rápida de Instalación

### 1. Clonar y Configurar el Entorno Virtual
```bash
git clone https://github.com/AngelGab3/Quantum-Computing.git
cd Quantum-Computing

python3 -m venv .venv
source .venv/bin/activate  # En Windows: .venv\Scripts\Activate.ps1
```

### 2. Instalar Dependencias
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### 3. Iniciar Jupyter
```bash
jupyter lab
# o bien
jupyter notebook
```

---

## Equipo y Reconocimientos

* **Gabriel Velázquez** — *Lic. en Física* (Autor principal e implementaciones en notebooks)
* **Martha Heredia** — *Ing. en Sistemas Computacionales* (Instructora del taller)
* **Rosh Guadiana** — *Ing. Biomédica* (Instructor del taller)

Desarrollado para el taller **Verano STEM UDLAP 2026** (*Universidad de las Américas Puebla*).

---

## Licencia

Este proyecto está bajo la [Licencia MIT](LICENSE).
