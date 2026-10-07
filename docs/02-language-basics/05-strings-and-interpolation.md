# Strings & Interpolation

Veyra strings are UTF-8 capable value types backed by high-efficiency C++ `std::string` memory storage.

---

## 🎯 Formatted String Interpolation

Embed variables and expressions directly inside double-quoted strings using `{}`:

```veyra
let user = "Aakarsh"
let score = 99.4

println("Welcome {user}, your high score is {score}!")

let width = 10
let height = 20
println("Calculated Area: {width * height} sq units")
```
