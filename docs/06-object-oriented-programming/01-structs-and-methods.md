# Structs, Classes & Methods

```veyra
struct Vec2 {
    x: double
    y: double

    fn length(self) -> double {
        return sqrt(self.x * self.x + self.y * self.y)
    }

    fn operator+(self, other: Vec2) -> Vec2 {
        return Vec2 { x: self.x + other.x, y: self.y + other.y }
    }
}

let v1 = Vec2 { x: 3.0, y: 4.0 }
let v2 = Vec2 { x: 1.0, y: 2.0 }
let v3 = v1 + v2

println("Combined: ({v3.x}, {v3.y})")
println("Length: {v1.length()}")
```
