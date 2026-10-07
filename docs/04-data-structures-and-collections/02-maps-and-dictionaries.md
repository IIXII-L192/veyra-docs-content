# Maps & Dictionaries

Hash maps (`map[K, V]`) for key-value storage:

```veyra
let mut scores: map[string, int] = {
    "Alice": 100,
    "Bob": 85
}

scores["Charlie"] = 92

if contains(scores, "Alice"):
    println("Alice is present: {scores["Alice"]}")
```
