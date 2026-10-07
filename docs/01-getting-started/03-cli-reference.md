# CLI Command Reference

The `veyra` CLI tool manages compiling, running, and inspecting Veyra applications.

---

## 📋 General Syntax

```bash
veyra <command> [options] <source.vey> [-- backend_flags]
```

---

## ⚙️ Commands

### `veyra run <file.vey>`
Compiles and executes a `.vey` file in-memory or from cache.

```bash
veyra run script.vey
veyra run script.vey -- arg1 arg2
```

### `veyra build <file.vey>`
Compiles a `.vey` file into an optimized, standalone binary executable.

```bash
# Output binary defaults to filename without extension (e.g. ./main)
veyra build src/main.vey

# Specify custom binary name
veyra build src/main.vey -o my_app

# Maximum optimization with Link-Time Optimization (LTO)
veyra build src/main.vey -O3 -o my_fast_app
```

### `veyra emit <file.vey>`
Transpiles the `.vey` code into formatted C++20 source code.

```bash
veyra emit src/main.vey
veyra emit src/main.vey -o generated.cpp
```
