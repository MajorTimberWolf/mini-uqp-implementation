
# Quantum Circuit Topology Analysis

This project explores the impact of different qubit topologies (Star, Linear Chain, Ring, and Fully Connected) on the performance of quantum circuits. Using Qiskit, the project simulates a quantum circuit across these topologies, comparing metrics such as circuit depth, gate count, and final state fidelity to analyze the efficiency and effectiveness of each topology.


## Requirements

- Python 3.8 or higher
- Qiskit 0.34.0 or higher


## Usage

1. **Run the Script**: Execute `main.ipynb` to run the simulations. The script will:
   - Create a quantum circuit with multi-qubit operations.
   - Simulate the circuit using Star, Linear Chain, Ring, and Fully Connected topologies.
   - Transpile the circuits for each topology to observe how they differ.
   - Execute the transpiled circuits on a simulator.
   - Visualize the results with a histogram comparing the measurement outcomes.


2. **Analyze the Results**: The script outputs the transpiled circuits for each topology, the circuit depth, gate counts, and a histogram comparing the outcomes.

### Example Output

- **Transpiled Circuits**: The script prints out the structure of the transpiled circuits for each topology.
- **Measurement Results**: The results are displayed in a histogram, showing the distribution of outcomes (e.g., `000` vs `011` states) for each topology.
- **Circuit Depth and Gate Count**: The output includes the depth of each circuit and the number of gates used, which are key metrics for understanding the efficiency of each topology.

## Key Concepts

- **Topologies**:
  - **Star Topology**: Central qubit interacts with several others, but non-central qubits are not directly connected.
  - **Linear Chain Topology**: Qubits are connected in a straight line, allowing direct operations between adjacent qubits.
  - **Ring Topology**: Qubits are connected in a loop, reducing the need for SWAP operations in some cases.
  - **Fully Connected Topology**: Every qubit is directly connected to every other qubit, minimizing the need for additional gates.

- **Performance Metrics**:
  - **Circuit Depth**: The number of layers of gates in the circuit. A higher depth can increase the likelihood of errors in quantum hardware.
  - **Gate Count**: The number of quantum gates (e.g., CNOT, Hadamard, SWAP) in the circuit. More gates generally mean more complexity and a higher chance of errors.

## Observations

- The **Fully Connected Topology** generally performs the best in terms of minimizing circuit depth and gate count, leading to the most efficient execution.
- The **Star Topology** introduces additional SWAP gates, resulting in higher depth and more gates, making it less efficient for circuits requiring multiple qubit interactions.
- **Linear Chain** and **Ring Topologies** offer a good balance but may require SWAP operations, depending on the circuit's structure.

## Contributions

Feel free to contribute to this project by:

- Adding more complex quantum circuits to compare across different topologies.
- Implementing additional topologies for comparison.
- Enhancing the visualization of results.
