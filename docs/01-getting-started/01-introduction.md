# Introduction & Philosophy

**Veyra** (`.vey`) is a modern, statically typed systems programming language designed to combine the **effortless syntax and rapid developer velocity of Python** with the **deterministic performance, zero-cost abstractions, and hardware control of C++20/23**.

---

## 🚀 Why Veyra?

For decades, developers have had to make an agonizing trade-off:
1. **High-Level Languages (Python, Ruby, JavaScript)**: Expressive, clean syntax with fast prototyping, but hindered by high memory usage, interpreted runtime overhead, and non-deterministic **Garbage Collection (GC)** pauses.
2. **Systems Languages (C++, C, Rust)**: Peak native speed, minimal memory footprint, and deterministic resource control, but burdened with verbose boilerplate, header file management, complex build tooling, and complex type hierarchies.

**Veyra eliminates this trade-off completely.**

| Feature | Python 3.12 | C++20 | Rust | Veyra 0.1 |
| :--- | :--- | :--- | :--- | :--- |
| **Boilerplate** | Low | High | Medium | **Zero Boilerplate** |
| **Execution Speed** | 1x (Base) | 50x - 100x | 50x - 100x | **50x - 100x (Native C++)** |
| **Garbage Collector** | Yes (GC pauses) | No (RAII) | No (Borrow checker) | **No GC (Deterministic RAII)** |
| **Memory Footprint** | ~30 MB | ~1 MB | ~1 MB | **< 1 MB** |
| **Top-Level Scripts** | Supported | Not supported | Not supported | **Supported (Automatic `main`)** |
| **Direct C/C++ Interop** | Slow (CFFI / PyBind) | Native | Complex FFI | **Zero-Overhead Direct Native** |

---

## ⚡ Core Design Principles

### 1. Zero-Boilerplate Scripting & Systems Programming
In Veyra, you can write a 1-line script that executes immediately or compiles into an ultra-fast standalone native binary:

```veyra
println("Hello, world!")
```

The Veyra compiler automatically infers top-level execution scopes and emits standard C++20 entry points without requiring boilerplate.

### 2. Zero-Cost Value Semantics & Deterministic RAII
Veyra does **not** use a runtime Garbage Collector. Every object has a clear owner and lifetime tied to its lexical scope. Memory and system resources (file descriptors, sockets, GPU buffers) are released deterministically the instant they leave scope.

### 3. Native C++20/23 Backend
Veyra generates clean, human-readable C++20 code, delegating optimization to compilers like `g++` and `clang++`. You get full GCC/LLVM optimization passes (`-O3`, SIMD auto-vectorization, inline expansion) for free.

### 4. Direct C/C++ Ecosystem Interop
Need to call Raylib, SDL2, OpenCV, CUDA, or existing C/C++ libraries? Veyra provides native `cinclude` directives and inline `cpp { ... }` blocks with zero marshalling overhead.
