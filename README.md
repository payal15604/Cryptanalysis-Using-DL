# Cryptanalysis Using Deep Learning

This project explores the cryptanalysis of the Grain Cipher using deep learning methods. The Grain Cipher utilizes Linear Feedback Shift Registers (LFSRs) and Non-linear Feedback Shift Registers (NFSRs) for encryption. The primary focus is on generating keystreams corresponding to initialization vectors (IVs), a constant key, and plaintext inputs.

**Key Highlights**

* **Updates:**
    * **Initial Approach:** Encountered challenges in the initial code
    * **Revised Strategy:** Transitioned to C language, importing the Grain module from GitHub repositories (as it is not openly available).

**Grain Cipher Overview**

The Grain Cipher encrypts data by generating keystreams using two key components:

* **Linear Feedback Shift Register (LFSR):** Generates predictable sequences based on linear operations.
* **Non-linear Feedback Shift Register (NFSR):** Introduces non-linearity for added security.

The implementation aims to:

* Generate keystreams for a given key and randomly generated IVs.
* Store keystreams and corresponding IVs in a structured format for analysis.

**Keystream Outline**

**Key Details**

The key, represented by the key1 array in hexadecimal format, is as follows:

```c
01 23 45 67 89 AB CD EF 12 34
```

Each element in the key1 array represents a byte (8 bits) of the key. The key remains constant across iterations.

**IV and Keystream Generation**

* IVs are randomly generated for each iteration.
* The keystreams are computed based on the constant key and generated IVs.
* A total of 10,000 unique IV-keystream pairs are stored in a CSV file (data.csv) using the `transferDataToCSV` function.

**Hexadecimal Representation**

In this implementation, hexadecimal values are used extensively. The representation format `0xXX` indicates hexadecimal values in C programming.

**Examples:**

* `0x01`: Hexadecimal value 01 (decimal: 1).
* `0x23`: Hexadecimal value 23 (decimal: 35).
* `0x45`: Hexadecimal value 45 (decimal: 69).



