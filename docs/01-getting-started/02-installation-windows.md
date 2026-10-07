# Windows Installation Guide

Veyra provides full first-class support for **Windows 10 and Windows 11** (64-bit x64 and ARM64).

---

## ⚡ Method 1: Automated PowerShell One-Liner (Recommended)

Open **PowerShell** (Run as Administrator) and execute:

```powershell
irm https://veyra192.vercel.app/install.ps1 | iex
```

### What this script does:
1. Detects your CPU architecture (`x64` or `ARM64`).
2. Checks for a C++20 backend compiler (**MSVC** from Visual Studio, **Clang-cl**, or **MinGW-w64** `g++`).
3. Downloads the latest `veyra.exe` binary into `C:\Program Files\Veyra\bin` (or `%LOCALAPPDATA%\Veyra\bin`).
4. Installs the standard prelude headers into `include\veyra\prelude.hpp`.
5. Automatically configures your system `PATH` environment variable.

---

## 📦 Method 2: Windows Package Managers

### Using Winget
```powershell
winget install IIXII-L192.Veyra
```

### Using Scoop
```powershell
scoop bucket add veyra https://github.com/IIXII-L192/veyra
scoop install veyra
```

---

## 🛠️ Method 3: Manual Installation & Prerequisites

If installing manually, ensure you have one of the following C++20 compilers:
- **Visual Studio 2019/2022 Community** (with "Desktop development with C++" workload installed)
- **MinGW-w64 GCC >= 11** (via MSYS2: `pacman -S mingw-w64-ucrt-x86_64-gcc`)
- **LLVM Clang >= 13**

Extract `veyra-windows-x64.zip` into `C:\Veyra`, and add `C:\Veyra\bin` to your System Environment `PATH`.

---

## 🔍 Verification

Open a new Command Prompt or PowerShell window:

```powershell
veyra --version
```

Output:
```text
Veyra Compiler v0.1.0 (x86_64-pc-windows-msvc, C++20 Native Backend)
```
