# Primitive Types & Conversions

Veyra provides standard integer, floating-point, boolean, and character scalar types.

---

## 🔢 Integer Types

| Type | Bits | Signed | Range |
| :--- | :--- | :--- | :--- |
| `int8` | 8 | Signed | -128 to 127 |
| `int16` | 16 | Signed | -32,768 to 32,767 |
| `int32` / `int` | 32 / 64 | Signed | Standard integer |
| `int64` | 64 | Signed | -9.22 × 10^18 to 9.22 × 10^18 |
| `uint8` / `byte`| 8 | Unsigned | 0 to 255 |
| `uint16` | 16 | Unsigned | 0 to 65,535 |
| `uint32` | 32 | Unsigned | 0 to 4,294,967,295 |
| `uint64` | 64 | Unsigned | 0 to 1.84 × 10^19 |

---

## 🌊 Floating Point Types

| Type | Precision | Bits |
| :--- | :--- | :--- |
| `f32` / `float` | Single precision | 32 |
| `f64` / `double` | Double precision | 64 |

---

## 🔄 Type Conversion & Helpers

```veyra
let s = "12345"
let num = to_int(s)          # String to int64
let fnum = to_float("3.14")  # String to double
let str_val = str(42)        # Value to string
```
