# Structs and Methods

Structs in Veyra represent contiguous, cache-friendly data structures with zero garbage collection overhead.

## Defining a Struct

```veyra
struct Vector2D {
    x: float = 0.0
    y: float = 0.0

    fn length() => sqrt(x * x + y * y)
}
```

## Creating Instances

```veyra
v1 = Vector2D(10.0, 20.0)
println("Length: {v1.length()}")
```

## Methods and Mutability

Methods can read or modify struct fields:

```veyra
struct Player {
    name: string
    health: int = 100

    fn take_damage(dmg: int) {
        health -= dmg
    }
}

mut hero = Player("Arthur", 100)
hero.take_damage(25)
println("{hero.name} has {hero.health} HP")
```

## Inheritance

Structs and classes can inherit from base types:

```veyra
struct Entity {
    name: string
    health: int = 100
}

struct Boss : Entity {
    rage_mode: bool = false
}
```
