# String, Math, Files & Time API

---

## 🔤 String Utilities
- `len(str) -> size_t`: Character length.
- `contains(str, substr) -> bool`: Substring check.
- `str(val) -> string`: String conversion.
- `to_int(str) -> int64`: Parses integer.
- `to_float(str) -> double`: Parses float.

---

## 🧮 Math Functions
- `abs(x)`: Absolute value.
- `min(a, b)`, `max(a, b)`: Minimum / Maximum.
- `clamp(val, low, high)`: Clamps value to range.
- `sqrt(x)`: Square root.
- `pow(base, exp)`: Power.
- `sin(x)`, `cos(x)`, `tan(x)`: Trigonometry (radians).
- `rand_int(min_val, max_val) -> int64`: Random integer.
- `rand_float(min_val, max_val) -> double`: Random float.

---

## 📁 File System API
- `read_file(path) -> string`: Reads file content into string.
- `read_lines(path) -> vec[string]`: Reads file into lines.
- `write_file(path, content) -> bool`: Overwrites file.
- `append_file(path, content) -> bool`: Appends to file.

---

## ⏱️ Time & System API
- `time_now_ms() -> int64`: Milliseconds since UNIX epoch.
- `time_now_sec() -> double`: Seconds with microsecond precision.
- `sleep_ms(ms)`: Thread sleep for specified milliseconds.
