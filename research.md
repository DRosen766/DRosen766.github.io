---
layout: default
title: Research
---

# Research

## Interests

Compute-in-memory hardware for biorealistic neural simulation, with emphasis on:

- RRAM-based architectures
- Kinetic neural modeling
- Hardware-software co-design
- Whole Brain Emulation

## Experience

### Graduate Research Assistant
**BRICCS Lab, Virginia Tech** | *Summer 2024 - Present*

- Designing RRAM-based compute-in-memory architectures for biorealistic kinetic modeling of synaptic receptor populations
- Developing software platforms for standards-based neural simulation on digital neuromorphic hardware
- Developing spiking neural network models for low-latency, low-power edge vision using DVS data

### Team Lead, Undergraduate Research Assistant
**Hume Center for National Security** | *Spring 2022 - Spring 2024*

- Managed a multidisciplinary team of undergraduate students to develop a custom OpenAI Gym environment
- Performed extensive training and performance assessment of Reinforcement Learning for Wireless Communication applications
- Optimized python package and user interface for widespread usage in the Wireless Communications community

## Publications and Manuscripts
*[Google Scholar](https://scholar.google.com/citations?user=1jEpqIUAAAAJ&hl=en)*

### Published

D. Rosen et al., "**RFRL Gym: A Reinforcement Learning Testbed for Cognitive Radio Applications**," 2023 International Conference on Machine Learning and Applications (ICMLA), Jacksonville, FL, USA, 2023, pp. 279-286, doi: [10.1109/ICMLA58977.2023.00046](https://doi.org/10.1109/ICMLA58977.2023.00046).

S. Vangaru, D. Rosen et al., "**A Multi-Agent Reinforcement Learning Testbed for Cognitive Radio Applications**," 2025 IEEE 22nd Consumer Communications & Networking Conference (CCNC), Las Vegas, NV, USA, 2025, pp. 1-9, doi: [10.1109/CCNC54725.2025.10976191](https://doi.org/10.1109/CCNC54725.2025.10976191).

### Under Review

**Small-scale neural simulation of *Caenorhabditis elegans* on Loihi-2 using NeuroML2Loihi** — first author, ACM JETC 2026

- Deployed the full 302-neuron *C. elegans* neural model on Intel Loihi 2 using the [NeuroML2Loihi](https://github.com/DRosen766/NeuroML2Loihi) framework
- Achieved up to 1,211× lower latency and 44% lower instantaneous power than NEURON running on an NVIDIA Jetson Orin edge GPU

**Energy-Efficient Drone Detection and Recognition using Dynamic Vision Sensing** — fifth author, IEEE TETCI 2026

- Implemented and evaluated spiking neural networks (SNNs) and convolutional neural networks (CNNs) for drone-recognition workloads using Dynamic Vision Sensor (DVS) data

### In Revision

**Convolutional Legendre-SNNs for Efficient Multivariate Time Series Classification**

- Proposed ConvLSNN, a convolutional spiking variant of DeepLSNN for multivariate time-series classification
- Developed and evaluated late-fusion and convolutional SNN variants; results motivate future deployment and energy analysis on neuromorphic hardware

### In Progress

**RRAM-based Architecture for Kinetic Modeling of Synaptic Receptor Populations**

- Designing an analog RRAM-based compute-in-memory architecture implementing a two-state AMPA receptor population model, with RRAM conductance encoding the ratio of open to closed receptors
- Using the SKY130 RRAM model
- Implemented and taped out digital baseline architectures via TinyTapeout for comparison against the analog design

## Projects

### [NeuroML2Loihi](https://github.com/DRosen766/NeuroML2Loihi)
**Technologies**: Python, Lava, Intel Loihi 2, NeuroML

- Framework for deploying standards-based **NeuroML** neural models onto **Intel Loihi 2**
- Used to deploy the full 302-neuron *C. elegans* connectome on neuromorphic hardware
- Enables latency and energy benchmarking against CPU/GPU simulation baselines

### TinyTapeout Silicon Designs
**Technologies**: Verilog, Verilog-A, SPICE, OpenLane, Cadence Virtuoso

- [Exact integration of single synaptic receptor population state on SKY130](https://github.com/DRosen766/tt-sky26c)
- [LIF neuron on GF180](https://github.com/DRosen766/ttgf-26b)
- Digital baselines taped out for comparison against an analog RRAM compute-in-memory design

### [The Radio Frequency Reinforcement Learning Gym](https://github.com/vtnsi/rfrl-gym)
**Technologies**: Pytorch, Mushroom RL, OpenAI Gym

- Open-source Custom OpenAI Gym environment for wireless communications
- Reinforcement Learning applications for radio frequency problems
- Performance optimization for widespread community usage

### [RadioNode](https://github.com/DRosen766/RadioNode)
**Technologies**: Python, Flask, PyTorch, AWS IoT, AWS S3, Docker

- End-to-end pipeline for **remote radio signal collection, storage, and learning**
- Streams raw **IQ data and signal metadata** from distributed radio clients to a centralized server using AWS IoT (MQTT)
- **PyTorch-based convolutional neural network** and training scripts for modulation classification on collected IQ data
- Supports containerized deployment of radio clients, data ingestion servers, and model training/inference workflows
