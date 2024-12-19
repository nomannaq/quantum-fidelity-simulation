# Quantum Teleportation Simulation with Qiskit

This project demonstrates quantum teleportation, a fundamental protocol in quantum information science, using Qiskit. The teleportation protocol allows the transfer of a quantum state from one qubit to another using entanglement and classical communication.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Requirements](#requirements)
- [Setup Instructions](#setup-instructions)
- [Usage](#usage)
- [Code Explanation](#code-explanation)
- [Output](#output)
- [References](#references)

---

## Overview

This project:

1. Creates a quantum circuit to implement the quantum teleportation protocol.
2. Simulates the process using Qiskit's `AerSimulator` backend.
3. Calculates the fidelity of the teleported state to ensure correctness.

The protocol involves three qubits:

- `q_0`: The sender's qubit holding the state to be teleported.
- `q_1`: An auxiliary qubit entangled with the receiver's qubit.
- `q_2`: The receiver's qubit where the state is teleported.

---

## Features

- Generate a random quantum state or use a predefined state for teleportation.
- Simulate the quantum circuit on a local simulator.
- Visualize the quantum circuit.
- Compute and display the fidelity of the teleported state.

---

## Requirements

- Python 3.8 or above
- Qiskit

Install Qiskit via pip:

```bash
!pip install qiskit
```

---

## Setup Instructions

1. Clone this repository:

2. Install the required Python packages:

3. Run the script:

---

## Usage

1. Define a quantum state to teleport (or let the script generate a random state):
   ```python
   specific_state = [1/np.sqrt(2), 1/np.sqrt(2)]  # Example: Equal superposition state
   ```

2. Run the teleportation function:
   ```python
   circuit, initial_state, final_state = run_teleportation(specific_state)
   ```

3. Visualize the circuit and results.

---

## Code Explanation

### Main Functions

1. **`create_teleportation_circuit(state_to_teleport)`**
   - Constructs the quantum circuit for teleportation.
   - Includes entanglement creation, Bell-state measurement, and conditional operations.

2. **`run_teleportation(state_to_teleport, shots)`**
   - Initializes the simulator.
   - Runs the teleportation protocol and computes fidelity.

---

## Output

### Example Output

```plaintext
Teleportation completed!
Receiver state: DensityMatrix([[0.5+0.j, 0.5+6.12e-17j],
                               [0.5-6.12e-17j, 0.5+0.j]])
Fidelity: 1.0000

Quantum Circuit:
     «q_0: »————[Initialize(0.70711, 0.70711)]———[H]——[CNOT]—[Measurement]—[Conditional Gates]—

```

This output indicates successful teleportation with perfect fidelity.

---

## References

1. [Qiskit Documentation](https://qiskit.org/documentation/)
2. [Quantum Teleportation Protocol](https://en.wikipedia.org/wiki/Quantum_teleportation)
