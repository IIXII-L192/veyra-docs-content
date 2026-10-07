# CLI Command Reference

The `veyra` command-line interface provides tools for compiling, running, inspecting, and managing Veyra projects.

---

## 📋 General Syntax

```bash
veyra <subcommand> [flags] <file.vey> [-- backend_flags]
```

---

## 🚀 Subcommands

### 1. `veyra run`
Compiles a `.vey` source file in-memory or to a temporary binary and executes it immediately. Ideal for fast script iteration.

```bash
# Run a script directly
veyra run script.vey

# Run with arguments passed to the script
veyra run script.vey -- arg1 arg2
```

### 2. `veyra build`
Compiles a `.vey` file into an optimized, standalone native binary.

```bash
# Compile to a binary with default name (e.g. ./app)
veyra build main.vey

# Specify custom output binary name
veyra build main.vey -o my_app

# Build with maximum optimization (-O3, LTO)
veyra build main.vey -O3 -o my_fast_app
```

### 3. `veyra emit`
Transpiles the `.vey` source code into clean, formatted C++20 code without invoking the backend compiler.

```bash
# Print generated C++20 to stdout
veyra emit main.vey

# Save generated C++20 to a file
veyra emit main.vey -o generated.cpp
```

### 4. `veyra new`
Scaffolds a new Veyra project directory with recommended structure.

```bash
veyra new my_project
cd my_project
```

Project layout created:
```text
my_project/
├── veyra.toml       # Project configuration
├── src/
│   └── main.vey     # Entry point
└── tests/
    └── test_main.vey
```

---

## 🚩 Compiler Flags

| Flag | Short | Description |
| :--- | :--- | :--- |
| `--output <file>` | `-o <file>` | Specify output binary or C++ file path |
| `--optimize <0-3>` | `-O<0-3>` | Set optimization level (Default: `-O3`) |
| `--emit-cpp` | `-E` | Emit intermediate C++20 source code |
| `--debug` | `-g` | Include debugging symbols (DWARF/PDB) |
| `--verbose` | `-v` | Display backend compilation commands |
| `--include <dir>` | `-I <dir>` | Add include directory for native headers |
| `--link <lib>` | `-l <lib>` | Link external native library (e.g. `-lraylib`) |
| `--version` | `-V` | Print Veyra compiler version |
| `--help` | `-h` | Show CLI help message |
