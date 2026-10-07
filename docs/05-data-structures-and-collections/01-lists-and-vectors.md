# Lists & Dynamic Arrays (`vec[T]`)

Dynamic arrays in Veyra provide O(1) random access and contiguous memory layout.

```veyra
let mut numbers = [10, 20, 30]

push(numbers, 40)
push(numbers, 50)

let removed = pop(numbers)
println("Popped item: {removed}")

sort(numbers)
reverse(numbers)

println("Array: {numbers}")
println("Length: {len(numbers)}")
```
