# Genetic Encryption:Leveraging Chromosomal Crossovers and Mutations for DNA Based Cryptography
# 🔐 D-GET: DNA-Based Genetic Encryption Technique

## Abstract

**D-GET** (DNA-based Genetic Encryption Technique) introduces a novel cryptographic paradigm inspired by biological systems—leveraging genetic crossover, mutation, and chromosomal alignment to achieve high entropy and security. As quantum threats emerge, biologically-inspired randomness offers a non-deterministic alternative to classical cryptography, increasing resilience against conventional and quantum attacks.

## 📌 Table of Contents

- [Why DNA-Based Cryptography?](#why-dna-based-cryptography)
- [System Architecture](#system-architecture)
  - [1. Preprocessing & DNA Encoding](#1-preprocessing--dna-encoding)
  - [2. Symmetric Key XOR Encryption](#2-symmetric-key-xor-encryption)
  - [3. Chromosome Structuring](#3-chromosome-structuring)
  - [4. Genetic Crossover](#4-genetic-crossover)
  - [5. Mutation Operators](#5-mutation-operators)
  - [6. Primer System (Traceability)](#6-primer-system-traceability)
  - [7. Decryption Pipeline](#7-decryption-pipeline)
- [Security Analysis](#security-analysis)
- [Performance Evaluation](#performance-evaluation)
- [Use Cases](#use-cases)
- [Future Work](#future-work)
- [Repository Structure](#repository-structure)
- [Contact](#contact)

## 🔍 Why DNA-Based Cryptography?

Traditional algorithms like RSA, AES, and ECC rely on deterministic mathematical structures, which quantum computers could potentially compromise via Shor’s or Grover’s algorithms. DNA cryptography offers an alternative rooted in biological entropy and stochastic behavior. DNA sequences, composed of four bases (A, C, G, T), allow for exponential keyspace (4ⁿ for n-length sequences). Genetic operations like crossover and mutation introduce chaotic behavior similar to natural evolution, which makes reverse engineering practically infeasible without precise primer metadata.

## 🧪 System Architecture

### 1. Preprocessing & DNA Encoding

Input data is converted from binary into DNA sequences. Each pair of bits is mapped to a nucleotide:
- `00 → A`, `01 → C`, `10 → G`, `11 → T`

This transforms binary plaintext into a DNA-like sequence suitable for biological operations.

### 2. Symmetric Key XOR Encryption

A one-time pad-style symmetric binary key is XORed with the binary input before DNA encoding. This adds initial confusion and ensures that plaintext patterns are obscured, while preserving reversibility for decryption.

### 3. Chromosome Structuring

The DNA sequence is divided into segments or “chromosomes,” emulating genome partitioning. Each chromosome is further split based on the first quartile of its divisors. This hierarchical structuring enables independent genetic operations and contributes to information diffusion.

### 4. Genetic Crossover

Crossover simulates natural recombination:
- **Single-Point Crossover:** Swaps segments across a randomly chosen point.
- **Rotational Crossover:** Performs cyclic shifts within the chromosome.

These operations increase ciphertext diversity and ensure even similar plaintexts yield significantly different outputs when processed.

### 5. Mutation Operators

Two mutation techniques add non-linearity:
- **Complement Mutation:** Random binary bit inversion (0 ↔ 1).
- **Alter Mutation:** Swaps DNA bases (e.g., A ↔ T, G ↔ C) at random positions.

Mutation introduces small, unpredictable changes, ensuring a strong avalanche effect—minor plaintext changes yield drastically different ciphertext.

### 6. Primer System (Traceability)

Each round of encryption generates a “primer”—metadata containing:
- Mutation type
- Crossover pivot index
- Round number

Primers act as a reversible logbook for reconstructing the encryption path, allowing correct decryption when provided alongside the key.

### 7. Decryption Pipeline

To decrypt:
1. Retrieve primers and key.
2. Reverse mutations and crossovers using stored metadata.
3. XOR with original key.
4. Decode DNA back to binary to recover plaintext.

Without the correct primer and key combination, the system becomes computationally infeasible to reverse due to massive permutation possibilities.

## 🔒 Security Analysis

### Keyspace & Entropy

DNA sequences offer exponential growth in keyspace. A DNA strand of length 256 has 4^256 (~10^154) possibilities, far exceeding AES-256’s 2^256 space. With additional layers from mutation and crossover, entropy increases even further.

### Quantum Resistance

D-GET is not based on algebraic constructs susceptible to Shor’s or Grover’s algorithms. Instead, it relies on combinatorial chaos and stochastic behavior, making it resistant to quantum factoring or search acceleration.

### Brute Force Resilience

Due to multiple mutation and crossover combinations per chromosome—each tracked only via hidden primers—the number of viable decryption paths explodes exponentially. Without primers, brute force is impractical.

## ⚙️ Performance Evaluation

- **Parallelism:** Genetic operations can run concurrently across chromosomes.
- **Low Correlation:** High avalanche effect ensures minimal similarity between ciphertexts of similar plaintexts.
- **Scalability:** Capable of encrypting arbitrary file sizes.
- **Efficiency:** XOR and encoding operations are lightweight, with mutation and crossover introducing minimal overhead.

## 🧭 Use Cases

- Post-quantum encrypted messaging
- Secure storage of DNA/genetic data
- Authentication in IoT and edge devices
- Hybrid encryption with AES/DNA layers
- Encrypted transfer of biometric credentials

## 🚀 Future Work

- Hardware-accelerated implementation (FPGA, GPU)
- Integration into secure file systems
- DNA-inspired key generation using live biological data
- Development of standard libraries and APIs for D-GET


