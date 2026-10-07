# Migrating from Python

Veyra provides Pythonic syntax with 50x–100x native C++ performance.

| Feature | Python | Veyra |
| :--- | :--- | :--- |
| **Print** | `print(f"Hello {name}")` | `println("Hello {name}")` |
| **List** | `nums = [1, 2, 3]` | `let nums = [1, 2, 3]` |
| **Push** | `nums.append(4)` | `push(nums, 4)` |
| **Sort** | `nums.sort()` | `sort(nums)` |
| **For Loop** | `for x in range(10):` | `for x in range(10):` |
| **Enumerate**| `for i, x in enumerate(v):` | `for i, x in enumerate(v):` |
| **Dictionary**| `d = {"k": "v"}` | `let d = {"k": "v"}` |
| **Function** | `def add(a, b):` | `fn add(a: int, b: int) -> int:` |
| **Class** | `class Point:` | `struct Point:` |
