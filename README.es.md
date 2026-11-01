<div align="center">

# Computación Cuántica
### *Curva de Aprendizaje Personal: De los Fundamentos Teóricos a la Realidad NISQ*

[![Autor](https://img.shields.io/badge/Autor-Gabriel_Velázquez-0052CC?style=for-the-badge&logo=github&logoColor=white)](https://github.com/AngelGab3)
[![Python](https://img.shields.io/badge/Python-3.9%20%7C%203.10%20%7C%203.11%20%7C%203.12-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://www.python.org/)
[![Qiskit](https://img.shields.io/badge/Qiskit-1.0+-6929C4?style=for-the-badge&logo=qiskit&logoColor=white)](https://qiskit.org/)
[![Cirq](https://img.shields.io/badge/Google_Cirq-1.3+-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://quantumai.google/cirq)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebooks-F37626?style=for-the-badge&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Licencia](https://img.shields.io/badge/Licencia-MIT-yellow?style=for-the-badge)](LICENSE)

**Idioma / Language:** [Español (Actual)](README.es.md) &nbsp;|&nbsp; [English](README.md)

---

</div>

## Visión General

Este repositorio constituye el registro personal de la curva de aprendizaje, notas de estudio e implementaciones de investigación en computación cuántica de **Gabriel Velázquez** (*Lic. en Física*).

El proyecto documenta la progresión desde el formalismo de la mecánica cuántica (espacios de Hilbert, notación de Dirac, operadores unitarios y productos tensoriales) hasta la ingeniería práctica de algoritmos y circuitos en dos marcos de vanguardia:
* **IBM Qiskit**: Derivaciones analíticas, representación de subsistemas en la esfera de Bloch, modelado realista de ruido NISQ ($T_1, T_2$, despolarización), tomografía cuántica de estados y transpilación para hardware físico de IBM.
* **Google Cirq**: Prototipado algorítmico, convergencia estadística de la regla de Born mediante la ley de los grandes números, generador cuántico de números aleatorios (QRNG) y teletransportación paramétrica.

Adicionalmente, se preserva en el repositorio el material en diapositivas del taller introductorio *"Una Brevísima Introducción a la Computación Cuántica"* impartido en el Verano STEM UDLAP 2026, desarrollado en colaboración con Martha Heredia y Rosh Guadiana.

---

## Estructura del Repositorio

```text
Quantum-Computing/
├── qiskit/        # Implementaciones personales en IBM Qiskit y análisis de hardware NISQ
├── cirq/          # Experimentos algorítmicos y simulaciones en Google Cirq
├── slides/        # Presentación del taller impartido en Verano STEM UDLAP 2026
├── requirements.txt
├── .gitignore
├── LICENSE
├── README.md      # Documentación principal en inglés
└── README.es.md   # Documentación general en español
```

---

## Módulos y Carpetas

### 1. [Módulo IBM Qiskit](qiskit/)
Notas de estudio personal centradas en rigor matemático, física de estados y hardware real:
* [`First_Steps.ipynb`](qiskit/First_Steps.ipynb): Evolución del estado entrelazado de Bell $\vert\Phi^+\rangle$, análisis del estado reducido en la esfera de Bloch, modelo de ruido para `ibmq_lima`, tomografía de estado, cálculo de fidelidad y transpilación a compuertas nativas $\{cx, id, rz, sx, x\}$.
* [`Quantum_Teleportation.ipynb`](qiskit/Quantum_Teleportation.ipynb): Derivación analítica completa y circuito de teletransportación de 3 qubits con correcciones condicionales de Pauli.
* Documentación detallada: [qiskit/README.md](qiskit/README.md).

### 2. [Módulo Google Cirq](cirq/)
Diseño algorítmico y física estadística computacional:
* [`Bell_State_with_Cirq.ipynb`](cirq/Bell_State_with_Cirq.ipynb): Creación de pares EPR en registros lineales `cirq.LineQubit`.
* [`Hadamard_Transform_with_Cirq.ipynb`](cirq/Hadamard_Transform_with_Cirq.ipynb): Superposición en grilla bidimensional con `cirq.GridQubit`.
* [`Measurement_Convergence_with_Cirq.ipynb`](cirq/Measurement_Convergence_with_Cirq.ipynb): Demostración empírica de la convergencia asintótica de la regla de Born ($N \in [10, 1000]$).
* [`Quantum_Number_Generator_with_Cirq.ipynb`](cirq/Quantum_Number_Generator_with_Cirq.ipynb): Generador Cuántico de Números Aleatorios (QRNG) en rangos arbitrarios mediante muestreo por rechazo.
* [`Quantum_Teleportation_with_Cirq.ipynb`](cirq/Quantum_Teleportation_with_Cirq.ipynb): Teletransportación cuántica modular con compuertas dinámicas controladas.
* Documentación detallada: [cirq/README.md](cirq/README.md).

### 3. [Diapositivas del Taller](slides/)
Presentación de 57 diapositivas *"Una Brevísima Introducción a la Computación Cuántica"* impartida en el Verano STEM UDLAP 2026.
* Ponentes: Gabriel Velázquez, Martha Heredia, Rosh Guadiana.
* Temario y estructura: [slides/README.md](slides/README.md).

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

## Autoría y Colaboradores

* **Gabriel Velázquez** — *Lic. en Física*  
  Autor del repositorio, notas de estudio, derivaciones matemáticas e implementaciones en código.

### Colaboradoras en Taller (Diapositivas)
* **Martha Heredia** — *Ing. en Sistemas Computacionales*  
  Coautora y coponente de la presentación del taller *"Una Brevísima Introducción a la Computación Cuántica"* ([`slides/`](slides/)).
* **Rosh Guadiana** — *Ing. Biomédica*  
  Coautora y coponente de la presentación del taller *"Una Brevísima Introducción a la Computación Cuántica"* ([`slides/`](slides/)).

---

## Licencia

Este proyecto está bajo la [Licencia MIT](LICENSE).
