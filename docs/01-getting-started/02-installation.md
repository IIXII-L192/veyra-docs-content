# Installation & Environment Setup

Installing the Veyra toolchain takes only a few seconds.

---

## 🚀 Automated 1-Line Installers

### Windows (PowerShell)
```powershell
irm https://veyra192.vercel.app/install.ps1 | iex
```

### Linux & macOS (Terminal)
```bash
curl -fsSL https://veyra192.vercel.app/install.sh | bash
```

---

## 🔨 Build from Source (All Platforms)

```bash
git clone https://github.com/IIXII-L192/veyra.git
cd veyra
make
sudo make install
```

Verify the installation:
```bash
veyra --version
```
