# Linux Installation Guide

Veyra supports all major Linux distributions on `x86_64` and `aarch64`.

---

## ⚡ Method 1: Automated Installer (All Distros)

```bash
curl -fsSL https://veyra192.vercel.app/install.sh | bash
```

---

## 📦 Method 2: Distribution Package Managers

### Ubuntu / Debian
```bash
sudo apt update
sudo apt install -y curl build-essential g++
curl -fsSL https://veyra192.vercel.app/install.sh | bash
```

### Arch Linux / Manjaro
```bash
sudo pacman -S --needed base-devel git
curl -fsSL https://veyra192.vercel.app/install.sh | bash
```

### Fedora / RHEL / Rocky Linux
```bash
sudo dnf groupinstall "Development Tools"
sudo dnf install gcc-c++
curl -fsSL https://veyra192.vercel.app/install.sh | bash
```

---

## 🔍 Verification

```bash
source ~/.bashrc
veyra --version
veyra --check-env
```
