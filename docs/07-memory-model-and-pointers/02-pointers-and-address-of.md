# Pointers & Address-Of

Direct hardware memory access when you need low-level efficiency:

```veyra
let mut value = 42
let ptr: *int = &value

println("Value via pointer: {*ptr}")

# Mutate via pointer dereference
*ptr = 999
println("Updated value: {value}")    # 999
```
