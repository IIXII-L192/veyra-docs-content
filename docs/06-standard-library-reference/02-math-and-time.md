# Math, Time & Files API

---

## 🧮 Math API
- `abs(x)`, `min(a, b)`, `max(a, b)`, `clamp(x, min, max)`
- `sqrt(x)`, `pow(base, exp)`
- `sin(x)`, `cos(x)`, `tan(x)`
- `rand_int(min, max)`, `rand_float(min, max)`

---

## ⏱️ Time API
- `time_now_ms() -> int64`: Epoch time in milliseconds.
- `time_now_sec() -> double`: Epoch time in seconds.
- `sleep_ms(ms)`: Sleep for specified milliseconds.

---

## 📁 File I/O
- `read_file(path) -> string`: Read full file.
- `read_lines(path) -> vec[string]`: Read lines.
- `write_file(path, content) -> bool`: Write file.
- `append_file(path, content) -> bool`: Append file.
