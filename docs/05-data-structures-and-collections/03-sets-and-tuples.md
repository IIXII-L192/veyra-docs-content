# Sets & Tuples

---

## 🔮 Sets (`set[T]`)
Unique collections with O(1) membership testing:

```veyra
let mut tags: set[string] = ["systems", "graphics", "network"]
tags.insert("ai")
```

---

## 📦 Pairs & Tuples (`pair[A, B]`)

```veyra
let point: pair[double, double] = (45.12, 120.88)
println("X: {point.first}, Y: {point.second}")
```
