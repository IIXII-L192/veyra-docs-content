# Structs & Classes

Veyra provides structs (public fields default) and classes (encapsulation).

---

## 🏗️ Structs

```veyra
struct Point:
    pub x: double
    pub y: double

    pub fn distance_to(self, other: Point) -> double:
        let dx = self.x - other.x
        let dy = self.y - other.y
        return sqrt(dx * dx + dy * dy)

let p1 = Point { x: 0.0, y: 0.0 }
let p2 = Point { x: 3.0, y: 4.0 }
println("Distance: {p1.distance_to(p2)}")
```
