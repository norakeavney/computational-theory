# computational-theory

**Module:** Computational Theory  
**Assessment:** Secure Hash Standard (SHA-256)  
**Student:** Nora Keavney  
**Student ID:** G00415845  

--- 

## Description

This repository contains my submission for the fourth-year Computational Theory assessment, which focuses on the **Secure Hash Standard (FIPS 180-4)** with particular emphasis on the **SHA-256** algorithm.

The assessment is implemented entirely in Python within a single Jupyter notebook (`problems.ipynb`). Each problem builds progressively toward a complete and standards-compliant understanding of SHA-256, starting from low-level bitwise operations, through constant generation and message padding, to full hash computation and real-world password security analysis.

All implementations are derived directly from the NIST specification and are written to prioritise correctness, clarity, and reproducibility. The repository is structured so that an informed computing professional can clone it and run the notebook with minimal setup, while still being able to clearly follow the reasoning, design choices, and mathematical foundations behind each step.

--- 

## Repository Structure

| File / Folder        | Description                                                                 |
|----------------------|-----------------------------------------------------------------------------|
| `README.md`          | Overview of the repository, its purpose, and instructions for running it. |
| `problems.ipynb`     | Main assessment notebook containing solutions to all five problems, with clear Markdown explanations and testing. |
| `.gitignore`         | Excludes unnecessary files such as virtual environments and notebook checkpoints from version control. |

The repository is intentionally minimal and focused. All assessment work is contained within a single Jupyter notebook, in line with the assessment requirements!

---

## Setup and Running the Code

This repository is designed to be easy to run with minimal setup. All code is contained within a single Jupyter notebook and relies only on standard Python tooling and NumPy.

### Requirements

To run the notebook, you will need:
- Python 3.9 or later
- Jupyter Notebook or JupyterLab
- NumPy

### Installation

Clone the repository locally.  
```
git clone
```
It is recommended to use a virtual environment, though this is optional.  
```
python -m venv venv
source venv/bin/activate
```

Install the required dependencies.  
```
pip install numpy jupyter
```


### Running the Notebook

Launch Jupyter and open the assessment notebook.  
```
jupyter notebook problems.ipynb
```

Once opened, run the notebook from top to bottom to reproduce all results and outputs.

No external data files are required, and all computations are performed locally.

## Problems Overview

| Problem | Title                                   | Description                                                                 |
|--------:|-----------------------------------------|-----------------------------------------------------------------------------|
| 1       | Binary Words and Operations              | Implements the core bitwise and logical functions used by SHA-256, ensuring correct 32-bit behaviour and validating each function with tests. |
| 2       | Fractional Parts of Cube Roots           | Recreates the SHA-256 round constants by computing cube roots of the first 64 prime numbers and extracting the first 32 bits of their fractional parts. |
| 3       | Padding                                  | Implements message padding and parsing according to the Secure Hash Standard, yielding correctly padded 512-bit message blocks. |
| 4       | Hashes                                   | Implements the SHA-256 compression function to compute the next hash state from a message block and current hash value. |
| 5       | Passwords                                | Demonstrates how unsalted SHA-256 password hashes can be attacked, identifies the original passwords, and discusses stronger password hashing techniques. |

Each problem is implemented and documented in `problems.ipynb`, with Markdown explanations, clearly structured code cells, and tests to verify correctness against the Secure Hash Standard.

## References

The primary reference used throughout this assessment is the NIST Secure Hash Standard:

- National Institute of Standards and Technology (NIST), *Federal Information Processing Standard (FIPS) 180-4: Secure Hash Standard*, 2015.  
  https://nvlpubs.nist.gov/nistpubs/FIPS/NIST.FIPS.180-4.pdf

Additional references, including specific sections of the standard and supporting resources, are cited and discussed **within the Markdown cells of `problems.ipynb`** on a problem-by-problem basis, where they are directly relevant to the implementation and analysis.

