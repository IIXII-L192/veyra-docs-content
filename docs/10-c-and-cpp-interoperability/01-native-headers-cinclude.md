# Native Headers & Inline C++

Veyra provides zero-overhead interoperability with C and C++.

---

## 🔌 `cinclude` Directive

```veyra
cinclude <chrono>
cinclude <cmath>
cinclude "raylib.h"

println("Imported C/C++ native headers with zero wrapper overhead!")
```

---

## ⚡ Inline `cpp { ... }` Blocks

```veyra
cpp {
    std::cout << "[Native C++ layer] Direct CPU intrinsics\n";
}
```
