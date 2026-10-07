# Complete Primitive Types

Veyra provides fixed-width scalar types for precise hardware control.

---

## 🔢 Integer Types Matrix

| Type | Bits | Signed | Range | C++ Equivalent |
| :--- | :--- | :--- | :--- | :--- |
| `int8` | 8 | Signed | -128 to 127 | `int8_t` |
| `int16` | 16 | Signed | -32,768 to 32,767 | `int16_t` |
| `int32` / `int` | 32 / 64 | Signed | Standard integer | `int32_t` / `int64_t` |
| `int64` | 64 | Signed | -9.22 × 10^18 to 9.22 × 10^18 | `int64_t` |
| `uint8` / `byte` | 8 | Unsigned | 0 to 255 | `uint8_t` |
| `uint16` | 16 | Unsigned | 0 to 65,535 | `uint16_t` |
| `uint32` | 32 | Unsigned | 0 to 4,294,967,295 | `uint32_t` |
| `uint64` | 64 | Unsigned | 0 to 1.84 × 10^19 | `uint64_t` |

```veyra
let small_byte: byte = 255
let packet_id: uint32 = 400201
let hex_mask: int = 0xDEADBEEF
let binary_flags: int = 0b11010110
```

---

## 🌊 Floating-Point Types

| Type | Bits | Precision | C++ Equivalent |
| :--- | :--- | :--- | :--- |
| `f32` / `float` | 32 | Single precision (~7 decimal digits) | `float` |
| `f64` / `double` | 64 | Double precision (~16 decimal digits) | `double` |

```veyra
let delta_time: f32 = 0.016667
let precise_pi: f64 = 3.14159265358979323846
```

---

## 🔤 Boolean, Characters & Strings

```veyra
let is_active: bool = true
let separator: char = '|'
let greeting: string = "Hello, Veyra!"
```
