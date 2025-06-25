# LDPC Decoding for 5G NR: Hard and Soft Decision Implementations

![CT216 Project](https://img.shields.io/badge/Project-CT216-blue) 
![MATLAB](https://img.shields.io/badge/Language-MATLAB-orange)
![5G NR](https://img.shields.io/badge/Standard-5G_NR-green)

This repository contains MATLAB implementations of Low-Density Parity-Check (LDPC) codes as specified in the 5G New Radio (NR) standard. The project demonstrates both hard decision and soft decision decoding algorithms with comprehensive performance analysis.

## Table of Contents
- [Project Overview](#project-overview)
- [Key Features](#key-features)
- [Implementation Details](#implementation-details)
- [Performance Metrics](#performance-metrics)
- [Theoretical Benchmarks](#theoretical-benchmarks)
- [Results](#results)
- [Contributors](#contributors)

## Project Overview
This end-of-semester project for CT216: Communication Systems at Dhirubhai Ambani Institute implements and analyzes LDPC codes for 5G NR, including:

- **Encoding** using 5G NR Base Graphs (BG1 and BG2)
- **BPSK modulation** with AWGN channel simulation
- Two decoding approaches:
  - Hard Decision Bit-Flipping Algorithm
  - Soft Decision Min-Sum Algorithm
- Comprehensive performance validation against theoretical limits

## Key Features

### Hard Decision Decoding
- Bit-flipping algorithm implementation
- Tanner graph message passing
- Efficient hardware-friendly design
- Supports multiple code rates (1/4, 1/3, 1/2, 3/5)

### Soft Decision Decoding
- Min-Sum algorithm with scaling factor (0.8)
- Log-Likelihood Ratio (LLR) processing
- Memory-optimized implementation for large block sizes
- Supports both BG1 (NR_1_5_352) and BG2 (NR_2_6_52)

## Implementation Details

### Core Components
1. **LDPC Encoder**: Implements 5G NR encoding using base graph matrices
2. **BPSK Modulator**: Maps bits to ±1 symbols
3. **AWGN Channel**: Adds Gaussian noise based on specified SNR
4. **Decoders**:
   - Hard decision: Iterative bit-flipping
   - Soft decision: Min-Sum message passing

### Performance Evaluation
- Monte Carlo simulations (N = 10,000 trials)
- Bit Error Rate (BER) calculation
- Frame Error Rate (FER) calculation
- Probability of decoding success (Pc)
- Convergence analysis across iterations

## Performance Metrics
The decoders are evaluated using:

1. **Functionality Tests**: Verification in ideal channel conditions
2. **Spot Checks**: Controlled error injection tests
3. **Monte Carlo Simulations**: Statistical performance evaluation across SNR ranges

## Theoretical Benchmarks

Performance is validated against:

1. **Shannon Limit**:
   ```math
   \left( \frac{E_b}{N_0} \right)_{\text{dB}} = 10 \log_{10} \left( \frac{2^R - 1}{R} \right)
   ```

2. **Normal Approximation**:
   ```math
   P_{N,e} = Q\left(\sqrt{\frac{N}{V}} \left(C - R + \frac{\log_2 N}{2N}\right)\right)
   ```

## Results

### Key Findings

- Soft decision decoding provides **2–3 dB gain** over hard decision  
- Performance approaches **Shannon limit** at higher SNRs  
- Convergence typically occurs within **20 iterations**

## Contributors

This project was developed by **Group 7** of CT216 (Winter 2024) at *Dhirubhai Ambani Institute of Information and Communication Technology*:

- Prince Chovatiya (202301067)
- Rishank Dudhat (202301068)
- Yashasvi Ishwarbhai Jadav (202301069)
- Heet Shah (202301070)
- Siddharth Rambhia (202301072)
- Meet Jain (202301073)
- Kavish Patel (202301074)
- Tirth Kanani (202301075)
- Pala Aaditya Vimalkumar (202301076)
- Bhensadadia Happy (202301077)

**Mentor**: Vivek Patel  
**Course Instructor**: Prof. Yash Vasavada

