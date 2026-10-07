# Your First Veyra Program

Let's write, inspect, and compile your very first Veyra program.

---

## 📝 Step 1: Create `hello.vey`

Create a file named `hello.vey`:

```veyra
# hello.vey - Welcome to Veyra!

let name = "Veyra Developer"
let version = 1.0

println("Hello, {name}!")
println("You are running Veyra version {version}")

let numbers = [10, 20, 30, 40, 50]
println("Items in list: {numbers}")

let mut total = 0
for n in numbers:
    total += n

println("Sum total is: {total}")
```

---

## ⚡ Step 2: Run Directly

Run the file using `veyra run`:

```bash
veyra run hello.vey
```

Output:
```text
Hello, Veyra Developer!
You are running Veyra version 1.000000
Items in list: [10, 20, 30, 40, 50]
Sum total is: 150
```

---

## 🔍 Step 3: Inspect the Generated C++20

Let's see what Veyra generated under the hood:

```bash
veyra emit hello.vey
```

---

## 📦 Step 4: Build a Standalone Native Binary

Compile it into a self-contained, optimized native binary:

```bash
veyra build hello.vey -O3 -o hello
./hello
```
