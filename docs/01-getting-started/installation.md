# Installation Guide

Welcome to Veyra! Getting started takes less than 10 seconds.

## Linux & macOS (Quick Install)

Run the universal installer script directly in your terminal:

```bash
curl -fsSL https://veyra-lang.org/install.sh | bash
```

Or build from source in 2 seconds:

```bash
git clone https://github.com/IIXII-L192/veyra.git
cd veyra
./install.sh
```

## Windows Installation

Open PowerShell as Administrator:

```powershell
iwr -useb https://veyra-lang.org/install.ps1 | iex
```

## Verifying the Installation

Check that `veyra` is in your system PATH:

```bash
veyra --version
```
Expected output:
```
Veyra Language Compiler v0.1.0 (Target: C++20)
```

## Running Your First Script

Create a file called `main.vey`:

```veyra
println("Hello, Veyra!")
```

Run it in 1 command:

```bash
veyra main.vey
```
