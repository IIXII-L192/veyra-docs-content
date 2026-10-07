# Strings & Interpolation

Veyra strings are UTF-8 capable, dynamic value types backed by high-performance C++ storage.

---

## 🎯 String Interpolation

Embed variables and arbitrary expressions directly inside string literals using `{}`:

```veyra
let user = "Aakarsh"
let level = 45
let attack = 120
let defense = 80

println("Player: {user} | Level: {level}")
println("Combat Power: {attack * 2 + defense}")
```

---

## 🛠️ String Operations

```veyra
let text = "  Veyra Systems Language  "

let size = len(text)
if contains(text, "Systems"):
    println("Keyword found!")
```
