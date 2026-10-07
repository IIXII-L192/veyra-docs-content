# First Programs & Workflow

Let's walk through building, running, and compiling programs in Veyra.

---

## 📝 1. Scripting Mode (Zero Boilerplate)

Create `script.vey`:

```veyra
# script.vey
let language = "Veyra"
println("Welcome to {language}!")

let mut scores = [95, 82, 99, 74, 88]
sort(scores)
println("Sorted scores: {scores}")
```

Run directly:
```bash
veyra run script.vey
```

---

## 🏗️ 2. Structured Application with Functions & Types

Create `math_demo.vey`:

```veyra
struct Circle:
    pub radius: double

    pub fn area(self) -> double:
        return 3.141592653589793 * self.radius * self.radius

fn main_app():
    let c = Circle { radius: 5.0 }
    println("Circle radius: {c.radius}")
    println("Calculated Area: {c.area()}")

main_app()
```

Compile to standalone release binary:
```bash
veyra build math_demo.vey -O3 -o math_demo
./math_demo
```
