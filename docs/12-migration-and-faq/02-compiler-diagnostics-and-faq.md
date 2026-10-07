# Diagnostics & FAQ

---

## ❓ Common Issues & Solutions

### 1. `Backend compiler g++ / clang++ not found`
- **Linux**: `sudo apt install -y build-essential`
- **macOS**: `xcode-select --install`
- **Windows**: Install Visual Studio Community C++ workload or MinGW-w64.

### 2. `Cannot find header <veyra/prelude.hpp>`
- Verify `~/.local/include/veyra` or set `export VEYRA_INCLUDE_PATH=~/.local/include/veyra`.
