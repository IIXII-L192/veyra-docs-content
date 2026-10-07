# 60 FPS Game with Raylib

Because Veyra compiles to native C++20 with zero GC pauses, it is ideal for 60+ FPS game development.

```veyra
cinclude "raylib.h"

InitWindow(800, 450, "Veyra 60 FPS Arcade")
SetTargetFPS(60)

let mut x: float = 400.0
let mut speed: float = 5.0

while !WindowShouldClose():
    x += speed
    if x > 780.0 or x < 20.0:
        speed *= -1.0

    BeginDrawing()
    ClearBackground(Color{ r: 7, g: 7, b: 10, a: 255 })
    DrawText("Veyra + Raylib Native 60 FPS", 20, 20, 20, Color{ r: 255, g: 255, b: 255, a: 255 })
    DrawCircle(int(x), 225, 20.0, Color{ r: 236, g: 72, b: 153, a: 255 })
    EndDrawing()

CloseWindow()
```

Compile and run:
```bash
veyra build game.vey -O3 -o game -lraylib -lGL -lm -lpthread -ldl
./game
```
