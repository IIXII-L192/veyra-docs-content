# Classes & Encapsulation

Classes provide encapsulation with `pub` and `priv` visibility:

```veyra
class BankAccount:
    priv balance: double
    pub owner: string

    pub fn init(owner: string, initial_deposit: double):
        self.owner = owner
        self.balance = initial_deposit

    pub fn deposit(mut self, amount: double):
        if amount > 0.0:
            self.balance += amount

    pub fn get_balance(self) -> double:
        return self.balance
```
