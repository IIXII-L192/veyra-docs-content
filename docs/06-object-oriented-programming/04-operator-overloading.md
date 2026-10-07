# Operator Overloading

Overload arithmetic, comparison, and container operators:

```veyra
struct Vec3:
    pub x: double
    pub y: double
    pub z: double

    pub fn operator+(self, other: Vec3) -> Vec3:
        return Vec3 { x: self.x + other.x, y: self.y + other.y, z: self.z + other.z }

    pub fn operator*(self, scalar: double) -> Vec3:
        return Vec3 { x: self.x * scalar, y: self.y * scalar, z: self.z * scalar }

let v1 = Vec3 { x: 1.0, y: 2.0, z: 3.0 }
let v2 = Vec3 { x: 4.0, y: 5.0, z: 6.0 }
let v3 = (v1 + v2) * 2.0
println("v3 = ({v3.x}, {v3.y}, {v3.z})")
```
