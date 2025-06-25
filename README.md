
 ⚙️ Parallel Sorting Algorithms: Performance Comparison

![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Pthreads](https://img.shields.io/badge/Pthreads-Multi--threading-blue?style=for-the-badge)
![OpenMP](https://img.shields.io/badge/OpenMP-Parallel--Computing-green?style=for-the-badge)
![OS](https://img.shields.io/badge/Operating--Systems-Project-red?style=for-the-badge)

A comparative analysis of **Count Sort**, **Heap Sort**, and **Radix Sort** implemented in **C** using:
- Serial execution
- POSIX threads (Pthreads)
- OpenMP (shared-memory parallelism)

---
 📌 Project Overview

This project benchmarks the execution time of sorting algorithms using different parallel programming techniques. It evaluates the trade-offs between serial and parallel implementations in terms of performance.

 🔗 Implemented Algorithms

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

 🚀 Getting Started

 ✅ Requirements
- GCC with C99 support
- POSIX threads (usually pre-installed on Linux)
- OpenMP support (`-fopenmp` flag)
- Linux/Unix recommended

 🧪 Compilation & Execution


# Count Sort
gcc -o count Count.c -lpthread -fopenmp
./count

# Heap Sort
gcc -o heap Heap.c -lpthread -fopenmp
./heap

# Radix Sort
gcc -o radix Radix.c -lpthread -fopenmp
./radix


---

 📊 Results Snapshot

| Algorithm  | Serial  | Pthreads | OpenMP  |
| ---------- | ------- | -------- | ------- |
| Count Sort | 0.002 s | 0.003 s  | 0.003 s |
| Heap Sort  | 0.002 s | 0.008 s  | 0.006 s |
| Radix Sort | 0.002 s | 0.001 s  | 0.004 s |

 🔍 Observations

* **Count Sort**: Best performance in serial due to low complexity.
* **Heap Sort**: OpenMP outperforms Pthreads, likely due to better load balancing.
* **Radix Sort**: Pthreads offer best performance with fine-grained control.



---
 ⚙️ Configuration

Inside the code:

int size = 100;   // Modify for array size
int n = 4;        // Thread count for Pthreads/OpenMP


---

 📈 Performance Analysis Highlights

 ✅ When Parallel Wins

* Large datasets
* Independent operations (e.g., Radix digit processing)

 🚫 When Serial Wins

* Small datasets (threading overhead > speedup)
* Memory-bound operations

---

 🤝 Contributing

 How to Contribute

1. Fork the repo
2. Create a branch:
   `git checkout -b feature/improve-performance`
3. Commit changes:
   `git commit -m "Improve performance of Heap Sort"`
4. Push:
   `git push origin feature/improve-performance`
5. Open a Pull Request 🎉

 Ideas for Enhancement

* Add Quick Sort or Merge Sort
* Implement CUDA for GPU-based sorting
* Add benchmarking automation
* Analyze memory usage and thread scaling

---


 👥 Authors

* **Bilal Shafiq** (21K-3222)
* **Muhammad Haris** (21K-3415)
* **Ghufran Ghous** (21I-2991)

  


