# Lists & Maps

---

## 📋 Lists (`vec[T]`)

```veyra
let mut numbers = [10, 20, 30]

push(numbers, 40)
let removed = pop(numbers)
sort(numbers)
reverse(numbers)

println("Array: {numbers}")
println("Length: {len(numbers)}")
```

---

## 📖 Maps (`map[K, V]`)

```veyra
let mut scores: map[string, int] = {
    "Alice": 100,
    "Bob": 85
}

scores["Charlie"] = 92

if contains(scores, "Alice") {
    println("Alice found!")
}
```
