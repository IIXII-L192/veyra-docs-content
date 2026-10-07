# Enumerate & Destructuring

Use `enumerate()` to iterate over collections with an index:

```veyra
let servers = ["prod-01", "prod-02", "backup-01"]

for idx, host in enumerate(servers):
    println("Server #{idx + 1}: {host}")
```
