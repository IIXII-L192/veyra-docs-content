# Type Inference & Type Casting

Veyra uses bidirectional static type inference to deduce variable types without requiring verbose annotations.

---

## ⚡ Type Inference

```veyra
let name = "Veyra"          # Inferred as string
let count = 42              # Inferred as int64
let ratio = 3.14            # Inferred as double
let flags = [true, false]   # Inferred as vec<bool>
```

---

## 🔄 Explicit Casting & Type Conversions

```veyra
let integer_val: int = 100
let float_val: double = double(integer_val)

# String conversions
let s = "4096"
let parsed_num: int64 = to_int(s)
let parsed_flt: double = to_float("123.456")
let text_repr: string = str(9999)
```
