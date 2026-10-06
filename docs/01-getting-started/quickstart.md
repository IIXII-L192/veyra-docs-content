# Veyra Quickstart

Learn the core workflow and syntax of Veyra in 5 minutes.

## 1. Zero Boilerplate

Unlike standard C++, you do not need to write `#include <iostream>` or wrap everything in `int main()`.

```veyra
# Line 1 of your script
name = "Hero"
score = 1500

println("Player {name} achieved a high score of {score}!")
```

## 2. Compiling and Running

Veyra provides 3 primary CLI modes:

```bash
# 1. Run instantly in 1 step
veyra app.vey

# 2. Build an optimized standalone binary
veyra build app.vey -o myapp -O3

# 3. View the generated C++20 code
veyra emit app.vey
```

## 3. Basic Example Program

```veyra
fn square(n: int) => n * n

items = [10, 20, 30, 40]

for i, val in enumerate(items) {
    println("Item {i + 1}: {val} (squared: {square(val)})")
}
```
