# Digital Quantum Simulation of Field Theories using Quantum Link Models

This repository contains my personal simulations of field theories using QLMs. 
My current focus is on understanding the framework of QLMs and how can they be used to digitally simulate relevant physical properties. Most of the code will be written in Qiskit, and some may also include some structures from Pennylane and other framework.
I will try to focus on the architecture for which the theory may be efficiently expressed. For example a $Z_2$ theory can be simulated using qubits, $Z_3$ can be simulated efficiently by qutrits and so on. Ultimately, I want to create a general framework incorporating the natural and efficient architecture for the corresponding field theories.

Many of these codes were originally written for my own exploration. I am now gradually rewriting them in a tutorial-style format, adding detailed explanations of the theory, simulation methods, and interpretation of results.

As of now, the simulations typically reproduce existing theoretical proposals rather than presenting new research. I try to reference the papers that were used for writing the codes at the end of each notebook. The primary goal is to deepen my own understanding while building a collection of open-source educational resources.

Since this is an ongoing personal learning project, some implementations may contain mistakes. I continuously refine and debug the codes as I learn more.

Notebooks in this repo:
1. **schwinger_model_qiskit.ipynb**: This notebook provides a fully self-contained quantum simulation of the Schwinger model — quantum electrodynamics (QED) in 1+1 dimensions — using IBM's Qiskit framework. Based on **U(1) Wilson lattice gauge theories in digital quantum simulators by Muschik et al.** All circuits run on Qiskit Aer's statevector simulator, mimicking a trapped-ion digital quantum computer with all-to-all Mølmer–Sørensen gates.

2. **qudit_processor_and_quantum_link_model_v2.ipynb**: A from-scratch Qiskit reconstruction of the Ringbauer et al.\ trapped-ion qudit processor (arXiv:2109.06903), validated against the paper's own numbers: the 10 addressable $^{40}\mathrm{Ca}^{+}$ transitions, Algorithm~1 $\mathrm{SU}(d)$ compilation, qutrit/ququint randomized benchmarking, and the $\mathrm{Cex}/\mathrm{Cinc}$ entangling gates. Building on it, a qudit-native $U(1)$ lattice gauge theory that fuses each matter site with its gauge link into one $d=6$ qudit, turning the three-body coupling into a two-body gate compiled from two phase-compensated MS gates. Includes noise-model dynamics showing the encoding buys $\sim 3\times$ in register size but that entangling-gate error, not the encoding, is the real bottleneck.

3. **s3_nonabelian_lattice_gauge_theory_v2.ipynb**: The first non-abelian extension: an $S_{3}$ gauge theory with matter, where the finite group makes each link exactly a $d=6$ qudit with no truncation. The core result is a factorisation theorem that compiles the entire non-abelian gauge-matter coupling into a single two-qudit controlled gate of just 7 MS gates and leaving the dynamics as ordinary free-fermion hopping. Tracks genuinely non-abelian observables (flux changing irrep as quarks move, non-commuting Gauss constraints), with an honest cost analysis versus qubit encodings.
