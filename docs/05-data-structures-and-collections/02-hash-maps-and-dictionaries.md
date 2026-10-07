# Hash Maps & Dictionaries (`map[K, V]`)

Hash tables with O(1) average lookup:

```veyra
let mut player_gold: map[string, int] = {
    "Arthur": 500,
    "Merlin": 1200
}

player_gold["Lancelot"] = 850

if contains(player_gold, "Merlin"):
    println("Merlin has {player_gold["Merlin"]} gold")
```
