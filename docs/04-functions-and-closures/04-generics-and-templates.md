# Generics & Templates

Generics compile to zero-overhead C++ template instantiations:

```veyra
fn swap_items[T](a: *T, b: *T):
    let temp = *a
    *a = *b
    *b = temp

let mut x = 10
let mut y = 99
swap_items(&x, &y)
println("x: {x}, y: {y}")
```
