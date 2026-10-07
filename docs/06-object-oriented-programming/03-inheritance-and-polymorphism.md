# Inheritance & Polymorphism

```veyra
class Actor:
    pub name: string
    pub health: int

    pub fn take_damage(mut self, dmg: int):
        self.health -= dmg
        if self.health < 0: self.health = 0
        println("{self.name} took {dmg} damage! Health: {self.health}")

class Hero : Actor:
    pub mana: int

    pub fn cast_spell(mut self, cost: int):
        self.mana -= cost
        println("{self.name} cast spell (Mana remaining: {self.mana})")
```
