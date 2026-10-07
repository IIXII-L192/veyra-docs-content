# Variables, Mutability & Scope

In Veyra, variables are immutable by default to prevent accidental side effects and enhance compiler optimizations.

---

## 🔒 Immutable Bindings (`let`)

```veyra
let host = "127.0.0.1"
let port = 8080

# host = "0.0.0.0"  # COMPILE ERROR: Cannot reassign immutable variable 'host'
```

---

## 🔓 Mutable Bindings (`let mut`)

```veyra
let mut request_count = 0
request_count += 1
println("Total requests: {request_count}")
```

---

## 🛡️ Constants (`const`)

Constants are strictly evaluated at compile time:

```veyra
const MAX_BUFFER_SIZE: int = 4096
const DEFAULT_TIMEOUT_MS: int = 5000
```

---

## 📦 Variable Shadowing & Lexical Scope

```veyra
let x = 10
if x > 5:
    let x = 99      # Shadows outer 'x' within this block
    println("Inner x: {x}")  # 99

println("Outer x: {x}")      # 10
```
