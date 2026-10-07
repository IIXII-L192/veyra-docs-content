# Installation & Environment Setup

Installing the Veyra toolchain takes under 10 seconds.

---

## 📦 Automated Installation

### Linux & macOS (bash / zsh)
Run the automated installation script:

```bash
curl -fsSL https://veyra192.vercel.app/install.sh | bash
```

This script:
1. Detects your operating system and CPU architecture (`x86_64`, `aarch64` / Apple Silicon).
2. Verifies that a C++20 compiler (`g++ >= 11` or `clang++ >= 13`) is available.
3. Installs the `veyra` compiler binary to `~/.local/bin/veyra`.
4. Copies the embedded standard prelude headers to `~/.local/include/veyra/prelude.hpp`.
5. Automatically configures your `~/.bashrc` or `~/.zshrc` `PATH`.

### Windows (PowerShell)
Open PowerShell as Administrator and run:

```powershell
irm https://veyra192.vercel.app/install.ps1 | iex
```

---

## 🔍 Verifying the Installation

After running the installer, reload your shell environment:

```bash
source ~/.bashrc   # or source ~/.zshrc
```

Verify that the CLI is accessible:

```bash
veyra --version
```

Output:
```text
Veyra Compiler v0.1.0 (x86_64-linux-gnu, C++20 Native Backend)
```

Run environment diagnostics:
```bash
veyra --check-env
```

---

## 🔨 Building from Source (All Platforms)

If you prefer building from source, you need **CMake >= 3.20** and a **C++20 compiler** (`g++-11+`, `clang++-13+`, or `MSVC 2019+`).

```bash
# 1. Clone the repository
git clone https://github.com/IIXII-L192/veyra.git
cd veyra

# 2. Configure with CMake
cmake -B build -DCMAKE_BUILD_TYPE=Release

# 3. Compile the binary
cmake --build build --config Release -j$(nproc)

# 4. Install locally
sudo cmake --install build
```
