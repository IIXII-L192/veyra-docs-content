# While & For Loops

---

## 🔁 While Loops

```veyra
let mut count = 5
while count > 0 {
    println("Countdown: {count}")
    count -= 1
}
println("Blastoff!")
```

---

## 🔄 Range & Collection For Loops

```veyra
// Range loop 0..5
for i in 0..5 {
    println("Index: {i}")
}

// Collection loop
let items = ["Alpha", "Beta", "Gamma"]
for item in items {
    println("Item: {item}")
}

// Indexed loop with enumerate()
for i, item in enumerate(items) {
    println("#{i + 1}: {item}")
}
```
