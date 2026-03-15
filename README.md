# Digital Quantum Simulation of Field Theories using Quantum Link Models

This repository contains my personal simulations of field theories using QLMs. 
My current focus is on understanding the framework of QLMs and how can they be used to digitally simulate relevant physical properties. Most of the code will me written in Qiskit, and some may also include some structures from Pennylane and other framework.
I will try to focus on the architecture for which the theory may be efficiently expressed. For example a $Z_2$ theory can be simulated using qubits, $Z_3$ can be simulated efficiently by qutrits and so on. I want to create a general framework incorporating the natural and efficient architecture for the corresponding field theories.

Many of these codes were originally written for my own exploration. I am now gradually rewriting them in a tutorial-style format, adding detailed explanations of the theory, simulation methods, and interpretation of results.

As of now, the simulations typically reproduce existing theoretical proposals rather than presenting new research. I try to reference the papers that were used for writing the codes at the end of each notebook. The primary goal is to deepen my own understanding while building a collection of open-source educational resources.

Since this is an ongoing personal learning project, some implementations may contain mistakes or approximations. I continuously refine and debug the codes as I learn more.

Notebooks in this repo:
1. **schwinger_model_qiskit.ipynb**: This notebook provides a fully self-contained quantum simulation of the Schwinger model — quantum electrodynamics (QED) in 1+1 dimensions — using IBM's Qiskit framework. Based on **U(1) Wilson lattice gauge theories in digital quantum simulators by Muschik et al.** All circuits run on Qiskit Aer's statevector simulator, mimicking a trapped-ion digital quantum computer with all-to-all Mølmer–Sørensen gates.
