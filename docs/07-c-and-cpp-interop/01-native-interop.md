# Native Headers & Inline C++

Veyra provides zero-overhead C/C++ interop:

```veyra
cinclude <chrono>
cinclude <cmath>

cpp {
    std::cout << "Direct native hardware interaction\n";
}
```
