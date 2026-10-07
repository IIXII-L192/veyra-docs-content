# Standard Prelude API Reference

All standard functions in `prelude.hpp` are globally available in root scope:

- `print(...args)` / `println(...args)`: Console output.
- `input(prompt) -> string`: Line input from stdin.
- `input_int(prompt) -> int64` / `input_float(prompt) -> double`: Numeric input.
- `len(collection) -> size_t`: Length of string or vector.
- `push(vec, val)` / `pop(vec) -> T`: Dynamic array operations.
- `sort(vec)` / `reverse(vec)`: In-place sorting and reversing.
- `contains(vec/map/str, item) -> bool`: Membership check.
- `read_file(path) -> string` / `write_file(path, content) -> bool`: File I/O.
- `time_now_ms() -> int64` / `sleep_ms(ms)`: High-resolution timing.
- `sqrt`, `pow`, `abs`, `min`, `max`, `clamp`, `sin`, `cos`, `tan`, `rand_int`, `rand_float`.
