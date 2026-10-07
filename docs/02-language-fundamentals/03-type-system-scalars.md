# Primitive Scalar Types

Veyra provides fixed-width scalar types with explicit bit-widths:

| Type | Bits | Signed | Range | C++ Equivalent |
| :--- | :--- | :--- | :--- | :--- |
| `int8` | 8 | Signed | -128 to 127 | `int8_t` |
| `int16` | 16 | Signed | -32,768 to 32,767 | `int16_t` |
| `int32` / `int` | 32 / 64 | Signed | Standard integer | `int32_t` / `int64_t` |
| `int64` | 64 | Signed | -9.22 × 10^18 to 9.22 × 10^18 | `int64_t` |
| `uint8` / `byte` | 8 | Unsigned | 0 to 255 | `uint8_t` |
| `uint16` | 16 | Unsigned | 0 to 65,535 | `uint16_t` |
| `uint32` | 32 | Unsigned | 0 to 4,294,967,295 | `uint32_t` |
| `uint64` | 64 | Unsigned | 0 to 1.84 × 10^19 | `uint64_t` |
| `f32` / `float` | 32 | Single float | ~7 decimal digits | `float` |
| `f64` / `double` | 64 | Double float | ~16 decimal digits | `double` |
| `bool` | 8 | Boolean | `true` / `false` | `bool` |
| `char` | 8 | Character | 1 byte ASCII/UTF-8 byte | `char` |
| `string` | Dynamic | UTF-8 String | Value type string | `std::string` |
