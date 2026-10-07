# Troubleshooting & Diagnostics

Quick diagnostics guide for Veyra:

1. **`Backend compiler g++ not found`**: Install `build-essential` or `clang++`.
2. **`Cannot find header <veyra/prelude.hpp>`**: Check `~/.local/include/veyra` or set `export VEYRA_INCLUDE_PATH=~/.local/include/veyra`.
3. **`Linker errors with external libraries`**: Pass `-l<libname>` directly to `veyra build`.
