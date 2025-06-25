# ⚙️ Parallel Sorting Algorithms: Performance Comparison

![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Pthreads](https://img.shields.io/badge/Pthreads-Multi--threading-blue?style=for-the-badge)
![OpenMP](https://img.shields.io/badge/OpenMP-Parallel--Computing-green?style=for-the-badge)
![OS](https://img.shields.io/badge/Operating--Systems-Project-red?style=for-the-badge)

A comparative analysis of **Count Sort**, **Heap Sort**, and **Radix Sort** implemented in **C** using:
- Serial execution
- POSIX threads (Pthreads)
- OpenMP (shared-memory parallelism)

---

## 📌 Project Overview

This project benchmarks the execution time of sorting algorithms using different parallel programming techniques. It evaluates the trade-offs between serial and parallel implementations in terms of performance.

### 🔗 Implemented Algorithms

Each algorithm has three variants:
- **Serial**
- **Pthreads**
- **OpenMP**

| Algorithm    | File         |
|--------------|--------------|
| Count Sort   | `Count.c`    |
| Heap Sort    | `Heap.c`     |
| Radix Sort   | `Radix.c`    |

---

## 🚀 Getting Started

### ✅ Requirements
- GCC with C99 support
- POSIX threads (usually pre-installed on Linux)
- OpenMP support (`-fopenmp` flag)
- Linux/Unix recommended

### 🧪 Compilation & Execution


# Count Sort
gcc -o count Count.c -lpthread -fopenmp
./count

# Heap Sort
gcc -o heap Heap.c -lpthread -fopenmp
./heap

# Radix Sort
gcc -o radix Radix.c -lpthread -fopenmp
./radix
