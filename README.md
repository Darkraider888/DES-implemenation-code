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

---
----------------------------------------------------------------------------------------------------------------------------
### File 3: The Git Exclusion File
* **Name it exactly:** `.gitignore` *(Remember the dot at the very beginning!)*
* **Why this is important for C:** When you compile C code, it generates executable binaries (`des` or `des.exe`) and object files (`.o`). These files are massive, system-specific machine code that should **never** be pushed to GitHub. This file keeps your repository completely pristine.
* **What to do:** Create a file named `.gitignore` and paste this block inside:

```text
# Prerequisites
*.d

# Object files
*.o
*.ko
*.obj
*.elf

# Linker output folders
*.ilk
*.map
*.exp

# Compiled Executables (System Specific binaries)
des
des.exe
*.out
*.app

# IDE Configurations & Cache
.vscode/
.idea/
.DS_Store
-----------------------------------------------------------------------------------------------------------------------------
# 1. Initialize local repository tracking
git init

# 2. Stage all architectural components
git add .

# 3. Commit the staged assets
git commit -m "Complete repository build: Added functional C DES cipher, gitignore, and compilation README"

# 4. Enforce main as baseline branch
git branch -M main

# 5. Link to your online GitHub repository (Replace with your actual URL)
git remote add origin https://github.com/your-username/your-repository-name.git

# 6. Push the code up online
git push -u origin main
