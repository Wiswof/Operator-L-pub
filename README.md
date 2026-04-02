# Neural Operator Learning for Quantum Simulations

This repository contains the code accompanying our work on applying neural operator learning to quantum systems.

## Overview

We develop neural operator-based methods to learn mappings in quantum simulations, enabling efficient approximation of quantum system behaviors and observables. The framework focuses on learning from generated or measured quantum data and generalizing across system configurations.

## Repository Structure

```
.
├── Nqubits_op_data_gen_0526.ipynb      # Exact coefficient data generation
├── Nqubits_trunc_sin_emb_5_X_0604_clean.ipynb  # Core training and modeling script
├── Circuit_measurement0701.ipynb       # Data acquisition from quantum devices (virtual/real)
├── Coff_O_Data_5qbits.npz              # Generated coefficient dataset
├── models/                            # Pretrained models (2 reference models included)
└── README.md
```

## Components

### Data Generation

**`Nqubits_op_data_gen_0526.ipynb`**
Generates exact coefficient data for quantum systems. The output dataset:

* `Coff_O_Data_5qbits.npz`

contains the processed coefficients used for training.

### Training & Modeling

**`Nqubits_trunc_sin_emb_5_X_0604_clean.ipynb`**
The main notebook for:

* Model construction
* Neural operator training
* Embedding design (truncated sine embedding)
* Performance evaluation

### Quantum Measurement

**`Circuit_measurement0701.ipynb`**
Used to collect data from:

* Simulated quantum circuits
* Real quantum hardware

This enables validation of learned models against realistic quantum outputs.

### Pretrained Models

Two trained models are provided in the repository as references. These can be used for:

* Benchmarking
* Fine-tuning
* Transfer learning

## Usage

1. Generate or load dataset:

   * Run `Nqubits_op_data_gen_0526.ipynb` or use provided `.npz` file

2. Train the model:

   * Run `Nqubits_trunc_sin_emb_5_X_0604_clean.ipynb`

3. (Optional) Collect measurement data:

   * Run `Circuit_measurement0701.ipynb`

## Notes

* Ensure required Python libraries are installed (e.g., NumPy, PyTorch, Qiskit if used)
* GPU acceleration is recommended for training

## License

This project is released under the MIT License.
