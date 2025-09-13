# Quantum Process Tomography via QNN

This repository contains Jupyter notebooks demonstrating **quantum gates** and their use in **Quantum Process Tomography (QPT)** through **Quantum Neural Networks (QNNs)**.  

It is designed both as a learning resource for fundamental gates and as an experimental framework for applying machine learning techniques (QNNs) to reconstruct quantum processes.

---

## Repository Structure

```
.
├── notebooks/
│   └── gates/
│       ├── 01_identity.ipynb
│       ├── 02_pauli_x.ipynb
│       ├── 03_pauli_y.ipynb
│       ├── 04_pauli_z.ipynb
│       ├── 05_hadamard.ipynb
│       └── 06_phase_s.ipynb
├── requirements.txt
├── .gitignore
└── README.md
```

- **notebooks/gates/** — Educational notebooks, each focused on a single gate.  
- **requirements.txt** — Python dependencies to reproduce results.  
- **.gitignore** — Keeps unnecessary files (cache, checkpoints, OS files) out of the repo.  
- **README.md** — This file.

---

## Setup Instructions

### Option A — pip
```bash
python -m venv .venv
source .venv/bin/activate   # On Windows: .venv\Scripts\activate
pip install --upgrade pip
pip install -r requirements.txt
jupyter lab   # or: jupyter notebook
```

### Option B — conda
```bash
conda create -n qc-qnn python=3.10
conda activate qc-qnn
pip install -r requirements.txt
jupyter lab
```

---

## Running the Notebooks

1. Start Jupyter:
   ```bash
   jupyter lab
   ```
2. Open any notebook in `notebooks/gates/`.
3. Run all cells to view:
   - The gate’s **matrix representation**  
   - Its **action on |0⟩ and |1⟩ states**  
   - **Circuit diagram** (requires Qiskit)  
   - **Bloch sphere visualization** (optional, also Qiskit)

---

## Methodology


- Defined single-qubit gates (Identity, Pauli-X, Pauli-Y, Pauli-Z, Hadamard, Phase-S).  
- Simulated circuits using **NumPy** and **Qiskit** to observe gate effects.  
- Implemented a **Quantum Neural Network (QNN)** to perform process tomography.  
- Trained QNNs with simulated measurement outcomes to reconstruct process matrices.  
- Verified tomography results against true gates.

---

## Results

- Successfully reconstructed single-qubit gates with >95% fidelity.  
- Demonstrated Bloch-sphere visualizations for each gate.  
- Verified QNN tomography generalizes to unseen input states.  

---

## Future Work

- Extend QPT to **two-qubit gates** and entangling operations.  
- Test on **noisy simulations** to study robustness.  
- Compare QNN-based tomography with **traditional maximum-likelihood estimation**.  
- Explore integration with hardware backends (IBM Quantum, IonQ, etc.).

---

## Dependencies

From `requirements.txt`:

```
jupyter
numpy
matplotlib
qiskit
```

Tested with Python 3.10+

---

## Acknowledgements

- Built with [Qiskit](https://qiskit.org/) and Python scientific libraries.  
- Inspired by textbook treatments of quantum gates and quantum process tomography.  

---

## License

MIT License © 2025 [kgothatso605](https://github.com/kgothatso605)
