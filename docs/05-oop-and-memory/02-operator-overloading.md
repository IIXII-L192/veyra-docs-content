# Operator Overloading

Overload arithmetic, comparison, or container operators:

```veyra
struct Vec2:
    pub x: double
    pub y: double

    pub fn operator+(self, other: Vec2) -> Vec2:
        return Vec2 { x: self.x + other.x, y: self.y + other.y }

let a = Vec2 { x: 1.0, y: 2.0 }
let b = Vec2 { x: 3.0, y: 4.0 }
let c = a + b
println("c = ({c.x}, {c.y})")
```
