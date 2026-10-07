# Operators & Precedence Matrix

---

## ➕ Arithmetic & Logical Operators

```veyra
let a = 10 + 5 * 2          # 20
let rem = 23 % 5            # 3

if (is_admin and active) or is_root:
    println("Authorized")
```

---

## ⚖️ Precedence Table (Highest to Lowest)

| Level | Operator Category | Operators | Associativity |
| :--- | :--- | :--- | :--- |
| **1** | Primary | `()`, `[]`, `.`, `->` | Left-to-right |
| **2** | Unary | `!`, `~`, `+`, `-`, `*` (deref), `&` (address) | Right-to-left |
| **3** | Multiplicative | `*`, `/`, `%` | Left-to-right |
| **4** | Additive | `+`, `-` | Left-to-right |
| **5** | Bitwise Shifts | `<<`, `>>` | Left-to-right |
| **6** | Relational | `<`, `<=`, `>`, `>=` | Left-to-right |
| **7** | Equality | `==`, `!=` | Left-to-right |
| **8** | Bitwise AND | `&` | Left-to-right |
| **9** | Bitwise XOR | `^` | Left-to-right |
| **10** | Bitwise OR | `\|` | Left-to-right |
| **11** | Logical AND | `and`, `&&` | Left-to-right |
| **12** | Logical OR | `or`, `\|\|` | Left-to-right |
| **13** | Assignment | `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `&=`, `\|=` | Right-to-left |
