# macOS Installation Guide

Veyra provides full native support for **macOS** on both **Apple Silicon (M1, M2, M3, M4)** and **Intel x86_64**.

---

## ⚡ Method 1: One-Line Terminal Installer (Recommended)

Open Terminal and run:

```bash
curl -fsSL https://veyra192.vercel.app/install.sh | bash
```

This script:
1. Detects whether your Mac is Apple Silicon (`arm64`) or Intel (`x86_64`).
2. Verifies Xcode Command Line Tools (`clang++ >= 13`). If missing, it prompts you to run `xcode-select --install`.
3. Installs `veyra` to `~/.local/bin/veyra`.
4. Installs the standard prelude headers to `~/.local/include/veyra/`.
5. Configures your `~/.zshrc` (or `~/.bash_profile`) `PATH`.

---

## 🍺 Method 2: Homebrew

```bash
brew tap IIXII-L192/veyra
brew install veyra
```

---

## 🔍 Verification

Reload your shell and check the compiler:

```bash
source ~/.zshrc
veyra --version
```

Output:
```text
Veyra Compiler v0.1.0 (arm64-apple-darwin, Apple Clang C++20 Backend)
```
