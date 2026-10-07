# Introduction & Architecture

**Veyra** (`.vey`) is a high-performance, statically typed systems programming language that compiles directly to native machine code through an optimized **C++20/23 backend**.

Veyra is designed to combine the **clean syntax and developer velocity of Python** with the **deterministic performance, zero-cost abstractions, and hardware control of C++**.

---

## 🚀 The Core Philosophy

```veyra
// A complete, standalone high-performance Veyra script
let name = "Veyra"
println("Welcome to {name}!")

let numbers = [10, 20, 30, 40, 50]
let mut total = 0

for n in numbers {
    total += n
}

println("Computed total: {total}")
```

---

## 🏗️ Compiler Architecture

The Veyra compiler pipeline consists of:

```
[ Source Code (.vey) ]
        │
        ▼
[ Lexer (Tokens) ]
        │
        ▼
[ Recursive-Descent Parser (AST) ]
        │
        ▼
[ C++20 Code Generator + Embedded Standard Prelude ]
        │
        ▼
[ Host C++ Compiler (GCC / Clang with -O3) ]
        │
        ▼
[ Standalone Native Executable (.exe / ELF / Mach-O) ]
```

### Key Architectural Pillars:
- **No VM, No Interpreter Runtime**: Compiles to standalone machine code with `< 1 MB` memory baseline and `< 1 ms` startup time.
- **Deterministic RAII Memory Model**: No Garbage Collector (GC) pauses. Resources, sockets, and memory are cleaned up the exact microsecond they exit scope.
- **Embedded Standard Prelude**: Built-in high-performance vectors (`vec[T]`), hash maps (`map[K, V]`), strings, math functions, and file utilities.
