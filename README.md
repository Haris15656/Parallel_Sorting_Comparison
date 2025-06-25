# Parallel Programming: Sorting Algorithms Performance Comparison

![C](https://img.shields.io/badge/C-00599C?style=for-the-badge&logo=c&logoColor=white)
![Pthreads](https://img.shields.io/badge/Pthreads-Multi--threading-blue?style=for-the-badge)
![OpenMP](https://img.shields.io/badge/OpenMP-Parallel--Computing-green?style=for-the-badge)
![OS](https://img.shields.io/badge/Operating--Systems-Project-red?style=for-the-badge)

A comprehensive performance analysis comparing three sorting algorithms (Count Sort, Heap Sort, and Radix Sort) implemented using different parallel programming approaches: Serial processing, Pthreads, and OpenMP.

## 🎯 Project Overview

This Operating Systems course project analyzes the performance differences between serial and parallel implementations of sorting algorithms. The study compares execution times across three different programming paradigms to understand the benefits and trade-offs of parallel processing.

### Team Members - Section 5C
- **Bilal Shafiq** (21K-3222)
- **Muhammad Haris** (21K-3415)  
- **Ghufran Ghous** (21I-2991)

*Department of Computer Science*  
*National University of Computer and Emerging Sciences-FAST, Karachi Campus*

## 🧮 Implemented Algorithms

### 1. Count Sort (`Count.c`)
- **Serial Implementation**: Traditional single-threaded approach
- **Pthreads Implementation**: Multi-threaded using POSIX threads
- **OpenMP Implementation**: Parallel processing using OpenMP directives

### 2. Heap Sort (`Heap.c`)
- **Serial Implementation**: Standard heap sort algorithm
- **Pthreads Implementation**: Parallelized heap operations
- **OpenMP Implementation**: OpenMP-based parallel heap sort

### 3. Radix Sort (`Radix.c`)
- **Serial Implementation**: Sequential radix sort
- **Pthreads Implementation**: Multi-threaded radix sort
- **OpenMP Implementation**: Parallel radix sort with OpenMP

## 📊 Performance Results

### Execution Time Comparison (seconds)

| Algorithm | Serial | Pthreads | OpenMP |
|-----------|--------|----------|--------|
| **Count Sort** | 0.002000 | 0.003000 | 0.003000 |
| **Heap Sort** | 0.002000 | 0.008000 | 0.006000 |
| **Radix Sort** | 0.002000 | 0.001000 | 0.004000 |

### Key Observations
- **Count Sort**: Serial implementation performs best for small datasets
- **Heap Sort**: OpenMP shows better performance than Pthreads
- **Radix Sort**: Pthreads implementation achieves fastest execution time

## 🛠️ Prerequisites

### System Requirements
- **GCC Compiler** with C99 support
- **POSIX Threads** library (pthread)
- **OpenMP** library support
- **Linux/Unix** environment (recommended)

### Required Libraries

#include <stdio.h>
#include <stdlib.h>
#include <unistd.h>
#include <pthread.h>
#include <omp.h>
#include <time.h>
🚀 Compilation and Execution
Compile Individual Programs
Count Sort
Copy# Serial + Pthreads + OpenMP version
gcc -o count Count.c -lpthread -fopenmp

# Run the program
./count
Heap Sort
Copy# Serial + Pthreads + OpenMP version
gcc -o heap Heap.c -lpthread -fopenmp

# Run the program
./heap
Radix Sort
Copy# Serial + Pthreads + OpenMP version
gcc -o radix Radix.c -lpthread -fopenmp

# Run the program
./radix
Compilation Flags Explained
-lpthread: Links the POSIX threads library
-fopenmp: Enables OpenMP support
-o: Specifies output executable name
📁 Project Structure
parallel-sorting-algorithms/
├── Count.c                 # Count Sort implementation
├── CountTime.txt          # Count Sort performance results
├── Heap.c                 # Heap Sort implementation  
├── HeapTime.txt           # Heap Sort performance results
├── Radix.c                # Radix Sort implementation
├── RadixTime.txt          # Radix Sort performance results
├── OS Project Report.pdf  # Detailed project report
└── README.md              # Project documentation
🔧 Configuration Parameters
Default Settings
Copyint size = 100;           // Array size for sorting
int n = 100, m = 100, o = 100;  // Thread/process parameters
Customization Options
Array Size: Modify size variable to test with different data sizes
Thread Count: Adjust thread parameters for different parallelization levels
Test Data: Change input arrays to test various data patterns
📈 Performance Analysis
Serial vs Parallel Trade-offs
Advantages of Parallel Processing
Scalability: Better performance with larger datasets
Resource Utilization: Efficient use of multi-core systems
Concurrent Processing: Multiple operations simultaneously
When Serial Performs Better
Small Datasets: Overhead of thread creation exceeds benefits
Simple Operations: Thread management cost > computation cost
Memory-bound Operations: Limited by memory bandwidth
Algorithm-Specific Insights
Count Sort
Best for: Small integer ranges
Parallel Challenge: Limited parallelizable operations
Result: Serial performs best due to low computational complexity
Heap Sort
Best for: General-purpose sorting
Parallel Challenge: Tree structure dependencies
Result: OpenMP shows better load balancing than Pthreads
Radix Sort
Best for: Integer sorting with large datasets
Parallel Advantage: Independent digit processing
Result: Pthreads excels with proper thread management
🧪 Testing and Benchmarking
Running Performance Tests
Copy# Compile all programs
make all

# Run automated testing script
./run_tests.sh

# Compare results
cat *Time.txt
Benchmarking Different Scenarios
Vary Array Sizes: Test with 100, 1000, 10000, 100000 elements
Different Data Patterns: Sorted, reverse-sorted, random data
Thread Count Variation: 2, 4, 8, 16 threads
🔍 Code Features
Thread Management
Pthread Implementation: Manual thread creation and synchronization
OpenMP Implementation: Compiler-directed parallelization
Load Balancing: Dynamic work distribution strategies
Performance Monitoring
Copy// Timing mechanism used in all implementations
clock_t start = clock();
// ... sorting algorithm execution ...
clock_t end = clock();
double cpu_time_used = ((double) (end - start)) / CLOCKS_PER_SEC;
User Interface
Console Display: ASCII art headers for each algorithm
Progress Indicators: Visual feedback during execution
Results Display: Formatted performance metrics output
📊 Research Applications
Academic Use Cases
Algorithm Analysis: Comparative study of sorting techniques
Parallel Computing Research: Threading model comparisons
Performance Optimization: Identifying bottlenecks and improvements
Educational Value
Operating Systems Concepts: Thread management and synchronization
Algorithm Design: Implementation of classic sorting algorithms
Performance Analysis: Empirical measurement and comparison
🤝 Contributing
How to Contribute
Fork the repository
Create a feature branch (git checkout -b feature/algorithm-improvement)
Implement your changes
Test performance impact
Commit changes (git commit -m 'Add algorithm optimization')
Push to branch (git push origin feature/algorithm-improvement)
Open a Pull Request
Areas for Enhancement
 Add more sorting algorithms (Quick Sort, Merge Sort)
 Implement GPU-based parallel sorting (CUDA)
 Add visualization of sorting process
 Extend benchmarking with larger datasets
 Optimize thread synchronization mechanisms
 Add memory usage analysis
