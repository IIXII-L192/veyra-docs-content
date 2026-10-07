# 60 FPS Game with Raylib

```veyra
cinclude "raylib.h"

InitWindow(800, 450, "Veyra Native 60 FPS Game")
SetTargetFPS(60)

let mut ball_x: float = 400.0
let mut ball_y: float = 225.0
let mut speed_x: float = 5.0
let mut speed_y: float = 4.0

while !WindowShouldClose():
    ball_x += speed_x
    ball_y += speed_y

    if ball_x > 780.0 or ball_x < 20.0:
        speed_x *= -1.0
    if ball_y > 430.0 or ball_y < 20.0:
        speed_y *= -1.0

    BeginDrawing()
    ClearBackground(Color{ r: 8, g: 7, b: 13, a: 255 })
    DrawText("Veyra + Raylib Native 60 FPS", 20, 20, 20, Color{ r: 255, g: 255, b: 255, a: 255 })
    DrawCircle(int(ball_x), int(ball_y), 18.0, Color{ r: 236, g: 72, b: 153, a: 255 })
    EndDrawing()

CloseWindow()
```

Compile and run:
```bash
veyra build game.vey -O3 -o game -lraylib -lGL -lm -lpthread -ldl
./game
```
