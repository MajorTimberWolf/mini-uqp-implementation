
# Quantum Circuit Topology Analysis with Qiskit

This project provides a comparative analysis of different qubit topologies (specifically, star and linear chain topologies) on the execution of quantum circuits. The project uses Qiskit to simulate and visualize the impact of these topologies on quantum circuit performance, with a specific focus on latency, error rates, and gate counts.

## Project Structure

- **main.py**: The main script that sets up and executes the quantum circuits for both topologies, and then compares the results.
- **requirements.txt**: Lists the required Python packages for this project, primarily Qiskit.
- **README.md**: This file. Provides an overview of the project, instructions for running the code, and an explanation of the results.

## Requirements

- Python 3.8 or higher
- Qiskit 0.34.0 or higher


## Usage

1. **Run the Script**: Execute `main.ipynb` to run the simulations. The script will:
   - Create a simple quantum circuit (Bell state preparation).
   - Simulate the circuit using both star and linear chain topologies.
   - Transpile the circuits for both topologies to observe how they differ.
   - Execute the transpiled circuits on a simulator.
   - Visualize the results with a histogram comparing the measurement outcomes.


2. **Analyze the Results**: The script will output the transpiled circuits and a histogram that compares the measurement results for the two topologies.

### Example Output

- **Transpiled Circuits**: The script prints out the structure of the transpiled circuits for each topology.
- **Measurement Results**: The results are displayed in a histogram, showing the distribution of outcomes (e.g., `000` vs `111` states).

## Key Concepts

- **Star Topology**: In this topology, a central qubit is directly connected to all other qubits. This reduces the number of gates required for entanglement in some quantum circuits, potentially leading to lower latency and fewer errors.
- **Linear Chain Topology**: In a linear topology, each qubit is only connected to its immediate neighbors. This can increase the number of gates required to perform operations on distant qubits, potentially increasing latency and error rates.

## Observations

- The star topology demonstrated better performance in terms of preserving the expected quantum state (`111` in the Bell state circuit).
- The linear chain topology introduced more errors, likely due to the additional gates required for operations across qubits that are not directly connected.

## Contributions

Feel free to contribute to this project by:

- Adding more complex quantum circuits to compare across different topologies.
- Implementing additional topologies for comparison.
- Enhancing the visualization of results.


## References

- [Qiskit Documentation](https://qiskit.org/documentation/)
- [Introduction to Quantum Computing](https://qiskit.org/textbook/preface.html)

---
