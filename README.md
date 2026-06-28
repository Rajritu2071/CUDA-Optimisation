# CUDA-Optimisation

> ~30–35% performance uplift on NVIDIA RTX 5000 series via low-level CUDA kernel optimization

![CUDA](https://img.shields.io/badge/CUDA-C%2B%2B-76B900?style=flat&logo=nvidia&logoColor=white)
![Language](https://img.shields.io/badge/Language-C%2B%2B-00599C?style=flat&logo=c%2B%2B&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=flat)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat)

---

## Overview

This project focuses on optimizing CUDA kernels for the NVIDIA RTX 5000 series GPUs, targeting significant performance improvements through low-level GPU programming techniques.

Key result: **~30–35% performance uplift** over baseline implementations through systematic profiling and optimization.

---

## Optimization techniques

- **Shared memory optimization** — Reduced global memory access latency by maximizing shared memory utilization
- **Warp-level primitives** — Used warp shuffle instructions to minimize synchronization overhead
- **Kernel fusion** — Combined multiple kernels into single launches to reduce memory bandwidth bottlenecks
- **Memory coalescing** — Restructured memory access patterns for optimal coalesced reads/writes
- **Occupancy maximization** — Tuned thread block dimensions to maximize GPU occupancy
- **Async data transfers** — Overlapped computation with memory transfers using CUDA streams

---

## Benchmark results

| Metric | Baseline | Optimized | Improvement |
|--------|----------|-----------|-------------|
| Kernel execution time | ~100% | ~65–70% | ~30–35% faster |
| Memory bandwidth utilization | Low | High | Significantly improved |
| GPU occupancy | Sub-optimal | Maximized | Notable increase |

*Benchmarked on NVIDIA RTX 5000 series*

---

## Project structure

```
CUDA-Optimisation/
├── src/
│   ├── kernels/          # Optimized CUDA kernel implementations
│   ├── baseline/         # Baseline implementations for comparison
│   └── utils/            # Helper functions and memory management
├── benchmarks/           # Profiling scripts and benchmark results
├── docs/                 # Technical documentation and analysis
└── README.md
```

---

## Tech stack

- **CUDA C++** — Kernel development and GPU programming
- **NVIDIA Nsight** — Performance profiling and analysis
- **C++17** — Host-side code
- **NVIDIA RTX 5000 series** — Target hardware

---

## Getting started

```bash
# Clone the repo
git clone https://github.com/Rajritu2071/CUDA-Optimisation.git
cd CUDA-Optimisation

# Compile
nvcc -O3 -arch=sm_89 src/kernels/optimized_kernel.cu -o cuda_opt

# Run benchmark
./cuda_opt --benchmark
```

**Requirements:** CUDA Toolkit 12.x+, NVIDIA RTX 5000 series GPU, GCC 11+

---

## Author

**Raj (Rituraj)** — AI/ML Engineer · CUDA Systems 
[![LinkedIn](https://img.shields.io/badge/LinkedIn-rajritu2071-0A66C2?style=flat&logo=linkedin&logoColor=white)](https://linkedin.com/in/rajritu2071)
[![X](https://img.shields.io/badge/X-@Rajritu2071-000000?style=flat&logo=x&logoColor=white)](https://x.com/Rajritu2071)
