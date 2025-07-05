# Quantum Hamming code under random Pauli error

The Hamming codes are a family of $[[2^r-1, 2^r-2r-1, 3]]$ quantum error-correcting codes, for $r = 3, 4, 5, \dots$. They are self-dual perfect CSS codes.
In this project, we fix $r=4$ and implement the $[[15,7,3]]$ CSS code. So, we use $15$ physical qubits and $15-7=8$ syndrome qubits (for error correction). 

For the self-dual [[15,7,3]] quantum Hamming code, we write a Qiskit function that takes an error probability $p$ as its input and outputs a quantum circuit that 
1. prepares the logical all-zero state,
2. runs the state prepared through a random Pauli error channel with error rate $p$ (for each physical qubit),
3. measures syndromes and applies the recovery operations,
4. measures the data qubits and computes the success probability (probability of measuring a component of the logical all-zero state at the end).

The construction uses only Clifford gates, measurements, and classically controlled Pauli operations.
