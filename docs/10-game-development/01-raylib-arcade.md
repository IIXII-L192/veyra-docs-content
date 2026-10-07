# 60 FPS Game with Raylib

```veyra
cinclude "raylib.h"

InitWindow(800, 450, "Veyra 60 FPS Arcade")
SetTargetFPS(60)

let mut x: float = 400.0
let mut speed: float = 5.0

while !WindowShouldClose() {
    x += speed
    if x > 780.0 || x < 20.0 {
        speed *= -1.0
    }

    BeginDrawing()
    ClearBackground(Color{ r: 7, g: 7, b: 10, a: 255 })
    DrawCircle(int(x), 225, 20.0, Color{ r: 236, g: 72, b: 153, a: 255 })
    EndDrawing()
}

CloseWindow()
```
