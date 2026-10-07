# Structs & Methods

Structs are value types with default public visibility:

```veyra
struct Point2D:
    pub x: double
    pub y: double

    pub fn distance(self, other: Point2D) -> double:
        let dx = self.x - other.x
        let dy = self.y - other.y
        return sqrt(dx * dx + dy * dy)

let p1 = Point2D { x: 0.0, y: 0.0 }
let p2 = Point2D { x: 3.0, y: 4.0 }
println("Distance between points: {p1.distance(p2)}")
```
