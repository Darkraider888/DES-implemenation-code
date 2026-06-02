# Data Encryption Standard (DES) Implementation in C

A complete, ground-up implementation of the Data Encryption Standard (DES) cryptographic algorithm written natively in C. This educational framework models the inner mathematical transformations of a Feistel cipher network, processing data with structural blocks supporting both ECB and CBC operational modes.

## 📌 Project Architecture
* **Course:** Information Security / Cryptography Lab
* **Institution:** Department of Computer Science and Engineering, Southeast University
* **Batch:** CSE Batch 63
* **Language:** C (C11 Standard)
* **Compiler:** GCC

## 🛠️ Cryptographic Features
- **Full 16-Round Feistel Network:** Complete implementation of round subkey generation (Permuted Choice 1 & 2, left circular bit-shifting schedule).
- **Hardcoded Matrix Mappings:** Native array definitions representing Initial Permutation (IP), Expansion Function (E), Substitution Boxes ($S_1 - S_8$), Permutation Function (P), and Final Inverse Permutation (FP).
- **Block Operational Modes:**
  - **ECB (Electronic Codebook):** Block-by-block isolated encryption.
  - **CBC (Cipher Block Chaining):** Implements bitwise XOR chaining using an 8-byte Initialization Vector (IV).
- **Memory Optimization:** Utilizes fixed-width integer types (`uint64_t`, `uint32_t`, `uint8_t`) for raw bit manipulation performance.

## 🚀 Compilation & Execution

Ensure you have a working C compiler installation (such as `gcc` via MinGW on Windows or built-in on Linux/Xubuntu).

### 1. Compilation
Compile the raw source file using the GNU Compiler Collection (GCC):
```bash
gcc des.c -o des
