# 🔐 C++ Parallel File Encryptor

## Overview
**Parallel File Encryptor** is a C++ project that demonstrates **efficient file encryption and decryption using parallel processing techniques**. By leveraging both **multiprocessing** and **multithreading**, this project significantly improves the performance of cryptographic operations compared to sequential processing.

---

## Branches / Approaches

### 1️⃣ `add/childProcessing` – Multiprocessing
This branch implements **parallel processing using multiple processes**:
- **Process Management:** Uses `fork()` to create child processes.
- **Task Queue:** Organizes encryption/decryption tasks in a queue.
- **Concurrent Execution:** Each child process independently executes tasks in parallel.

### 2️⃣ `add/multithreading` – Multithreading
This branch demonstrates **parallel processing using threads and shared memory**:
- **Multithreading:** Implements concurrent execution using POSIX threads (`pthread`).
- **Shared Memory:** Efficient inter-thread communication.
- **Semaphores:** Ensures synchronization and data consistency.

---

## Features
- Encrypt and decrypt files/folders in parallel.
- Compare efficiency of **multiprocessing** vs **multithreading** approaches.
- System-level programming: `fork()`, `pthread`, shared memory, semaphores.
- Command-line interface for easy usage.

---

## Getting Started

### Clone the repository
```bash
git clone <repo-url>
cd "cpp file encrypter"
git checkout <branch>
```
### Setup And Run
```bash
# Optional: create a Python virtual environment for helper scripts
python -m venv myvenv
source myvenv/bin/activate   # Windows: myvenv\Scripts\activate

# Prepare directories
python makeDirs.py

# Build and run
make
./encrypty

# Follow prompts:
# 1. Enter the directory name created from makeDirs.py
# 2. Type ENCRYPT or DECRYPT
```
### Usage example
```bash
Enter directory name: test
Action (ENCRYPT/DECRYPT): ENCRYPT
Encryption completed successfully!
```

