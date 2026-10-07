# Variables & Mutability

Veyra uses `let` for immutable variable bindings and `mut` for mutable ones.

---

## 🔒 Immutable vs Mutable

```veyra
# Immutable binding (default)
let language = "Veyra"
# language = "Other"  # COMPILE ERROR: Cannot reassign immutable variable

# Mutable binding
let mut counter = 0
counter += 1

# Explicit type annotation
let pi: double = 3.14159265359
let mut user_id: int64 = 1001
```

---

## ⚡ Type Inference

Veyra's static type checker infers types automatically:

```veyra
let name = "Alice"           # Inferred as string
let age = 30                 # Inferred as int64
let ratio = 0.75             # Inferred as double
let is_active = true         # Inferred as bool
let items = [1, 2, 3, 4]     # Inferred as vec<int64>
```
