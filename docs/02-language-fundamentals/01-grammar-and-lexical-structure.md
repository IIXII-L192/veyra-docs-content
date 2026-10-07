# Grammar & Lexical Structure

Veyra's grammar is designed for clarity and high parse speeds.

---

## 💬 Comments

```veyra
# Python-style single line comment
// C-style single line comment

/*
   Multi-line block comment
   Spanning multiple lines
*/
```

---

## 🧱 Statements & Blocks

- **Delimiters**: Statements are delimited by newlines. Semicolons `;` are optional.
- **Blocks**: Can be defined using Python-style indentation with `:` or C-style `{}` braces.

```veyra
# Python-style indentation
if score >= 90:
    println("Outstanding grade!")
    let status = "Passed"

# C-style braces
if (score >= 90) {
    println("Outstanding grade!");
    let status = "Passed";
}
```

---

## 🏷️ Keywords

`let`, `mut`, `const`, `fn`, `struct`, `class`, `enum`, `pub`, `priv`, `if`, `elif`, `else`, `while`, `for`, `in`, `return`, `break`, `continue`, `import`, `cinclude`, `cpp`, `self`, `true`, `false`, `nullptr`.
