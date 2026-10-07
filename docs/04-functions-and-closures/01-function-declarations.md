# Function Declarations & Signatures

Functions are declared with `fn`.

```veyra
fn add(a: int, b: int) -> int:
    return a + b

fn print_status(message: string):
    println("[STATUS] {message}")

let sum = add(100, 250)
print_status("Total sum calculated: {sum}")
```
