# Pointers & References

Direct memory access with native pointers and references:

```veyra
let mut val = 42
let ptr: *int = &val

println("Value via pointer: {*ptr}")

*ptr = 100
println("Mutated value: {val}")    # 100
```
