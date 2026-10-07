# Syntax & Structure

Veyra features an ultra-clean syntax designed for maximum legibility and zero boilerplate.

---

## 💬 Comments

```veyra
# Python-style single line comment
// C-style single line comment

/*
   Multi-line C-style block comment
*/
```

---

## 🧱 Statements & Blocks

- Semicolons `;` are optional.
- Newlines delimit statements.
- Blocks can use Python-style `:` with indentation, or C-style `{}` braces.

```veyra
# Indentation style
if score > 90:
    println("Outstanding!")

# Brace style
if (score > 90) {
    println("Outstanding!");
}
```

---

## 🏷️ Identifiers & Keywords

Identifiers start with `[a-zA-Z_]` followed by `[a-zA-Z0-9_]`.

Reserved keywords:
`let`, `mut`, `const`, `fn`, `struct`, `class`, `enum`, `pub`, `priv`, `if`, `elif`, `else`, `while`, `for`, `in`, `return`, `break`, `continue`, `import`, `cinclude`, `cpp`, `self`, `true`, `false`, `nullptr`.
