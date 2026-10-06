# Variables and Mutability

Veyra provides flexible, clean variable declaration with full C++ type safety and automatic inference.

## Implicit Variables (Python Style)

You can assign variables directly without `let` or `mut`:

```veyra
score = 100
player_name = "Shadow"
is_ready = true
```

## Explicit Immutable Variables (`let`)

Use `let` when you want a variable to be constant and immutable:

```veyra
let max_health = 200
let pi = 3.14159
```

## Explicit Mutable Variables (`mut`)

Use `mut` when a variable will change over time:

```veyra
mut health = 100
health -= 25
health += 10
```

## Type Annotations

Type annotations are optional, but available when explicit types are preferred:

```veyra
let count: int = 42
let speed: float = 9.81
let title: string = "Veyra Guide"
let flag: bool = true
```
