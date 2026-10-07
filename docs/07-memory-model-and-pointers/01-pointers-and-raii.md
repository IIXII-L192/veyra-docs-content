# Pointers & Deterministic RAII

---

## 🎯 Direct Pointers

```veyra
let mut value = 42
let ptr: *int = &value

println("Value via pointer: {*ptr}")

*ptr = 999
println("Updated value: {value}")
```

---

## 🛡️ Deterministic RAII

Objects and memory are reclaimed deterministically the moment they leave their enclosing `{ ... }` block without any Garbage Collection pause.
