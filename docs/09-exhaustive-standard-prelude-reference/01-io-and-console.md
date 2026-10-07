# I/O & Console API Reference

All standard I/O functions in `prelude.hpp` are globally available in root scope.

---

## `print(...args)`
Prints one or more arguments separated by a space without trailing newline.

```veyra
print("Sensor #1:", 42.8, "deg C")
```

---

## `println(...args)`
Prints arguments followed by a newline `\n`.

```veyra
println("System initialized successfully")
```

---

## `input(prompt = "") -> string`
Reads a line of text from standard input.

```veyra
let name = input("Enter username: ")
```

---

## `input_int(prompt = "") -> int64`
Reads input and converts it to a 64-bit integer.

```veyra
let port = input_int("Enter port: ")
```

---

## `input_float(prompt = "") -> double`
Reads input and converts it to double-precision float.

```veyra
let factor = input_float("Enter scaling factor: ")
```
