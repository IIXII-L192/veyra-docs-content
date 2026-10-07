# Exhaustive CLI Command Reference

The `veyra` command-line tool is your central toolchain controller for executing, compiling, debugging, and packaging Veyra programs.

---

## 📋 General Command Syntax

```bash
veyra <subcommand> [flags] <source_file.vey> [-- backend_flags]
```

---

## 🚀 Subcommands

### 1. `veyra run <file.vey>`
Compiles the specified Veyra file in-memory or to a temporary cache directory and executes it immediately.

```bash
# Execute a script immediately
veyra run app.vey

# Pass CLI arguments directly to the script
veyra run server.vey -- --port 8080 --host 0.0.0.0
```

### 2. `veyra build <file.vey>`
Compiles a `.vey` file into an optimized, standalone native binary executable.

```bash
# Default build (generates ./app on Linux/macOS or app.exe on Windows)
veyra build app.vey

# Custom binary output name
veyra build src/main.vey -o my_engine

# Release build with maximum optimization (-O3) and Link-Time Optimization (LTO)
veyra build src/main.vey -O3 -o release_binary
```

### 3. `veyra emit <file.vey>`
Transpiles `.vey` source code into clean, formatted, human-readable C++20 code without invoking the backend compiler.

```bash
# Print generated C++20 to stdout
veyra emit main.vey

# Save generated C++20 to file
veyra emit main.vey -o output.cpp
```

### 4. `veyra new <project_name>`
Scaffolds a complete Veyra project directory structure.

```bash
veyra new arcade_game
```

Created layout:
```text
arcade_game/
├── veyra.toml        # Project configuration & dependencies
├── src/
│   └── main.vey      # Application entry point
├── include/          # Native C/C++ header files
└── tests/
    └── test_main.vey # Test suites
```

---

## 🚩 Compiler Flags & Options

| Flag | Short | Description | Default |
| :--- | :--- | :--- | :--- |
| `--output <file>` | `-o` | Specify output executable or C++ file path | `[input_stem]` |
| `--optimize <0-3>` | `-O` | C++ optimization level (`-O0`, `-O1`, `-O2`, `-O3`) | `-O3` |
| `--emit-cpp` | `-E` | Generate C++20 source code without compiling binary | `false` |
| `--debug` | `-g` | Include debugging symbols (DWARF / PDB) | `false` |
| `--verbose` | `-v` | Show underlying compiler commands and timing metrics | `false` |
| `--include <dir>` | `-I` | Add include directory for native C/C++ header resolution | `.` |
| `--link <lib>` | `-l` | Link native external library (e.g. `-lraylib`, `-lGL`) | None |
| `--lib-dir <dir>` | `-L` | Add library search directory | None |
| `--version` | `-V` | Print compiler version and backend details | - |
| `--help` | `-h` | Display command help screen | - |

---

## ⚙️ Environment Variables

| Variable | Description |
| :--- | :--- |
| `VEYRA_CXX` | Overrides the backend compiler path (e.g. `g++`, `clang++`, `cl.exe`). |
| `VEYRA_CXXFLAGS` | Custom flags forwarded to the backend compiler (e.g. `-march=native -flto`). |
| `VEYRA_INCLUDE_PATH` | Directory containing `veyra/prelude.hpp`. |
