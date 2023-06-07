# Description
This project simulates evolution of a 1D spin-½ chain on a current digital quantum computer for the below hamiltonian.

$$
  \hat{H} = -J \sum_{j=1}^{N-1} (\hat{\sigma} _{j}^{x} \hat{\sigma} _{j+1}^{x} + \hat{\sigma} _{j}^{y} \hat{\sigma} _{j+1}^{y}) + U \sum _{j=1}^{N-1} \hat{\sigma} _{j}^{z} \hat{\sigma} _{j+1}^{z} + \sum _{j=1}^{N} h_j\hat{\sigma} _{j}^{z}
$$

This project was done as part of Seminar: Advanced Topics of Quantum Computing at TU Munich, Germany and is based on this brilliant [Paper](https://www.nature.com/articles/s41534-019-0217-0)

# Requirements
The project uses the Qiskit framework for implementing the quantum circuits. Complete list of software requirements can be found in `requirements.txt`. 

One could install all packages in the file using the simple command
```
pip install -r requirements.txt
```

# Implentation details and usage
The complete implementation is included in the python notebook `simulating_quantum_many_body.ipynb`. It is broken into 7 steps.

1. **Functions for implementing the circuit** - Contains a list of functions required to implement symmetric trotter decomposition of the Hamiltonian.
2. **Defining the Observables** - Defines the observables necessary for the study i.e. the local magnetization and Nhalf.
3. **Verification of Results** - Comparision of results from current implementation with the [Paper](https://www.nature.com/articles/s41534-019-0217-0)
4. **XX Chain** - XX chain corresponds to a simplified hamiltoninan where h = 0 and U = 0. Evolution of local magnetization is studied across all sites. The corresponding circuit is also simulated on an IBM quantum computer.
5. **Parametric study** - study on influence of number of trotter steps and number of qubits for XX chain simulation on a quantum computer. Results show that accuracy improves with lower number of trotter steps (lower circuit depth) and less number of particles (lower qubits).
6. **Disordered XX chain** - Studied the case when U = 0 in hamiltonian. Compared simulation results for various values of h which is a measure of disorder in the system.
7. **XXZ chain** - Studied the case when h = 0 in hamiltonian. Compared simulation results for various values of U.

# Results

Following is a small collection of results. THe complete set can be found in the `results` folder. 

**XX Chain**

![XX chain and evoln](https://github.com/rajatchandavar/Quantum_Many_Body_Dynamics/assets/31350861/ca232cd7-d100-4b09-b9cc-3c1dd5dd1a3c)

![Parametric study 1](https://github.com/rajatchandavar/Quantum_Many_Body_Dynamics/assets/31350861/e2f3b3fa-f333-48e2-a1b2-a984c0d54916)

![Parametric study 2](https://github.com/rajatchandavar/Quantum_Many_Body_Dynamics/assets/31350861/ac5ab735-eac0-4771-8219-4e7492c729d1)

**Disordered XX Chain**

![DisorderedXX](https://github.com/rajatchandavar/Quantum_Many_Body_Dynamics/assets/31350861/a20dc200-6ba6-4991-83d3-d42bc1fa7592)










