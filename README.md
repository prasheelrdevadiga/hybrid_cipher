# Design and Analysis of a Hybrid Cipher  

This repository implements a cryptographic system blending substitution principles (via an upgraded Hill Cipher variant) with transposition mechanisms, engineered to deliver 128-bit security-grade encryption. The dual-layer architecture effectively neutralizes traditional decryption strategies including spectral pattern analysis and matrix manipulation attacks.**
---
<br>

## **Table of Contents**  
- **LiveTest**: [ClickHere!!](https://colab.research.google.com/drive/1ggChPjfgLNRMG3t_574T-FTsiZSAuGAG#scrollTo=0SEzQOelqeFs&line=104&uniqifier=1) 
- [Overview](#overview)  
- [Features](#features)  
- [How It Works](#how-it-works)  
- [Installation](#installation)  
- [Usage](#usage)  
- [Example](#example)  
- [Security Justification](#security-justification)   
- [Acknowledgments](#acknowledgments)  
- [Contact](#contact)  

---

## **Overview**  

The hybrid cipher integrates two classical cryptographic techniques:

- **Substitution Layer**: A modified **Hill Cipher** encrypts plaintext blocks using **matrix multiplication over a finite field**.  
- **Transposition Layer**: A **pseudorandom permutation** rearranges the encrypted blocks to disrupt patterns.  

This combination ensures both **confusion (substitution)** and **diffusion (transposition)**, making the cipher **more secure** than either technique alone.  

---

## **Features**  

- **128-bit encryption strength** for enhanced security.  
- **Combines** substitution (Hill Cipher) and transposition for stronger encryption.  
- **Modular design** for scalability (e.g., increasing block size).  
- **Deterministic yet unpredictable** behavior using a seeded **pseudorandom number generator (PRNG)**.  

---

## **How It Works**  

### 🔹 **Substitution Layer**  
1. Converts plaintext into **numerical blocks**.  
2. Encrypts each block using a **randomly generated invertible matrix** (Hill Cipher).  

### 🔹 **Transposition Layer**  
1. **Shuffles** the encrypted blocks using a **PRNG seeded with a secret key**.  

### 🔹 **Decryption**  
1. Reverses the **transposition and substitution layers** to recover the original plaintext.  

---

## **Installation**  

### **Prerequisites**  
You need the following **Python libraries** to run the hybrid cipher:

- `numpy`: For matrix operations.  
- `sympy`: For modular matrix inversion.  

### **Steps to Install Dependencies**  
1. **Clone the repository**:

   First, clone the repository to your local machine using the following command:

   ```sh
   git clone https://github.com/Ragha8951/hybridcipher.git
2. **Install the required libraries using pip:**:
   ```sh
   pip install num py
   pip install numpy sympy

---
# Hybrid Cipher - Usage Guide

Once the dependencies are installed, follow these steps to run the **Hybrid Cipher**:

---

## **Usage**

1. **Save the `hyb.py` file** in your working directory.

2. **Run the script** using Python:

   ```sh
   python hyb.py
---
## **Customizing Parameters**
**block_size: Set the size of each plaintext block (default is 4) for the Hill Cipher encryption.**<br>

**substitution_key: Modify the randomly generated key matrix for the Hill Cipher (it is automatically generated).**<br>

**transposition_key: Provide a custom secret key for shuffling the blocks during the transposition phase (entered by the user).**<br>

---
## Example

### Input:
- **Plaintext**: "HELLO WORLD"
- **Block Size**: 4
- **Substitution Key**: Randomly generated 4×4 matrix.
- **Transposition Key**: "SECRETKEY"

### Output:
- Encrypted ciphertext blocks (numerical representation).
- Decrypted plaintext: "HELLO WORLD"


---

##**Security Justification**

  *Confusion: The Hill Cipher obscures relationships between plaintext and ciphertext by replacing plaintext blocks with seemingly unrelated ciphertext blocks.*
  
  *Diffusion: The transposition layer spreads the influence of each plaintext character across multiple ciphertext blocks, disrupting patterns and ensuring that partial information about the ciphertext is 
    insufficient for decryption.*
    
*128-bit Strength: By operating on large matrices and using modular arithmetic, the cipher achieves computational complexity comparable to modern encryption standards, ensuring brute-force attacks are computationally prohibitive.*

---

##**Acknowledgments**

**The design of this hybrid cipher is inspired by classical cryptographic techniques and modern encryption principles. Special thanks to the open-source community for tools like numpy and sympy, which made this implementation possible.**

---
##***Contact**

 **For questions or feedback, feel free to reach out:**

   **GitHub: https://github.com/prasheelrdevadiga**
   <br>
   **Email: prasheeldevadiga170@gmail.com**
   <br>
   Thank you for visiting
   
---
