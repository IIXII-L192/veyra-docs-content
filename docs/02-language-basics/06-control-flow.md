# Control Flow

Conditionals and loop constructs in Veyra.

---

## 🔀 Conditionals (`if / elif / else`)

```veyra
let score = 88

if score >= 90:
    println("Grade: A")
elif score >= 80:
    println("Grade: B")
else:
    println("Grade: C")
```

---

## 🔄 For Loops & Ranges

```veyra
# Range loop: 0 to 9
for i in range(10):
    println("i = {i}")

# List iteration
let items = ["Engine", "Compiler", "Debugger"]
for item in items:
    println("Component: {item}")

# Enumerate with index
for idx, item in enumerate(items):
    println("#{idx + 1}: {item}")
```
