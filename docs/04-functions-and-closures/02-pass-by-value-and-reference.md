# Pass by Value vs Reference

In Veyra, pass by value creates a local copy. For zero-copy performance or in-place mutations, pass by reference using `&mut`:

```veyra
fn increment(val: &mut int):
    val += 1

let mut level = 10
increment(level)
println("New level: {level}")    # Prints 11
```
