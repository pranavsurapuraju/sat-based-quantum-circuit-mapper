# SAT-Based Quantum Circuit Mapping

## Overview
This project implements a SAT-based quantum circuit mapper using incremental and parallel optimization techniques.

It compares three approaches:
- Naive heuristic routing
- TKET mapping (baseline)
- SAT-based incremental + parallel optimization

## Goal
Minimize SWAP gates when mapping quantum circuits to constrained hardware (e.g., linear nearest-neighbor architectures).

## Features
- SAT encoding of qubit placement and routing
- Incremental SAT solving with bound tightening
- Parallel solving for faster optimization
- TKET integration for heuristic baseline
- Circuit visualization before and after mapping

## Example Results
Naive SWAPs: 24  
TKET SWAPs:  3  
SAT SWAPs:   4  

## Key Insight
SAT finds optimal solutions within constraints, while TKET uses fast heuristics.

- TKET may outperform SAT on small/simple circuits  
- SAT performs better on complex routing problems  

## How to Run
Open the notebook and run all cells.

## Future Work
- Improve time horizon selection
- Better initial placement strategies
- Hybrid TKET + SAT optimization

## Research Inspiration

This project is based on and inspired by the following research work:

Yang, J., Kharkov, Y. A., Shi, Y., Heule, M. J. H., & Dutertre, B. (2024).
Quantum Circuit Mapping Based on Incremental and Parallel SAT Solving.
Proceedings of the 27th International Conference on Theory and Applications of Satisfiability Testing (SAT 2024).
DOI: 10.4230/LIPIcs.SAT.2024.10

Key concepts implemented:
- SAT encoding of qubit mapping and routing constraints
- Incremental SAT solving with bound tightening (SWAP minimization)
- Parallel solver execution for faster convergence
- Comparison with heuristic approaches such as TKET

The implementation adapts these techniques into a practical workflow using PySAT, Qiskit, and TKET, demonstrating how formal methods can be applied to optimize quantum circuit compilation.
