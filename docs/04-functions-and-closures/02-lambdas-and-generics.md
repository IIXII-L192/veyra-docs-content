# Lambdas & Generics

---

## 🏹 Arrow Lambdas

```veyra
let square = (x: int) => x * x
println("Square of 8: {square(8)}")
```

---

## 🧬 Generic Functions

```veyra
fn swap[T](a: *T, b: *T) {
    let temp = *a
    *a = *b
    *b = temp
}

let mut x = 10
let mut y = 99
swap(&x, &y)
println("x: {x}, y: {y}")
```
