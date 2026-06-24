# Fault-Tolerant Biochemical Pipeline for DNA Data Storage 

[![Python Version](https://img.shields.io/badge/python-3.11-blue.svg)](https://www.python.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

An end-to-end software-defined resilience pipeline designed to mitigate biochemical error modalities (substitutions, insertions, deletions) in DNA data storage. This system couples an intelligent **Look-Ahead Constraint Solver** natively with a **Distributed Linear Fountain Code** to achieve a perfect 0% Bit Error Rate (BER) under a 12.5% random noise floor.

> **Note:** This research-backed implementation is authored by a 3rd-year B.E. Computer Engineering student and is currently prepared for submission to the IEEE Section Conference.

---

## Key Features

* **Look-Ahead Constraint Solver:** Actively suppresses homopolymer runs ($\ge 3$ identical bases) and dynamically maps sequences to maintain an ideal 45%–55% GC-content boundary.
* **Distributed Fountain Code:** Employs a bitwise XOR-optimized linear fountain code with an added global parity shield ($\Omega = 1.30$), offering 30% structural redundancy across strand pools.
* **High Performance on Low Overhead:** Replaces computationally intensive matrix inversions with lightweight bitwise operations, scaling linearly with payload magnitude $\mathcal{O}(N)$.

---

## Performance & Simulation Results

### 1. Operational Noise Boundary
Simulation trials confirm that the look-ahead algorithm handles up to **12.5% strand corruption** flawlessly. Beyond this threshold, the system displays a characteristic non-linear degradation profile ideal for archival safety boundaries.

### 2. Computational Latency Scaling
Processing latency scales perfectly lineally with the input data payload magnitude (tested from 10 KB to 1 MB), ensuring predictable timelines for massive cloud-scale deployments.

---

## Installation & Usage

### Prerequisites
* Python 3.11+

### Setup
