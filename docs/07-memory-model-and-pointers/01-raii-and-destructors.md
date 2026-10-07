# Deterministic RAII & Destructors

Veyra uses deterministic **Resource Acquisition Is Initialization (RAII)**.

```veyra
class DatabaseConnection:
    priv conn_str: string

    pub fn init(conn_str: string):
        self.conn_str = conn_str
        println("Opened connection to {self.conn_str}")

    pub fn drop(self):
        println("Closed connection to {self.conn_str}")

if true:
    let conn = DatabaseConnection("postgres://localhost:5432/db")
    # Query database...
# conn is automatically closed and freed here immediately without GC pause!
```
