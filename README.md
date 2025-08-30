# Large Code Block Example

Here’s a sample Markdown file with a **big code block** to test rendering.

---

## Python Example

```python
# This is a sample Python program to demonstrate a large code block

import random
import time

class Player:
    def __init__(self, name, health=100):
        self.name = name
        self.health = health
    
    def attack(self, enemy):
        damage = random.randint(5, 20)
        enemy.health -= damage
        print(f"{self.name} attacks {enemy.name} for {damage} damage!")

    def heal(self):
        heal_points = random.randint(10, 25)
        self.health += heal_points
        print(f"{self.name} heals for {heal_points} health!")

    def is_alive(self):
        return self.health > 0

def battle(player1, player2):
    turn = 0
    while player1.is_alive() and player2.is_alive():
        time.sleep(0.5)  # add delay for realism
        attacker = player1 if turn % 2 == 0 else player2
        defender = player2 if turn % 2 == 0 else player1

        # Random choice: attack or heal
        if random.choice([True, False]):
            attacker.attack(defender)
        else:
            attacker.heal()

        print(f"Status: {player1.name}({player1.health}) - {player2.name}({player2.health})")
        print("-" * 40)

        turn += 1

    winner = player1 if player1.is_alive() else player2
    print(f"\n🏆 {winner.name} wins the battle! 🏆")

# Example run
if __name__ == "__main__":
    alice = Player("Alice")
    bob = Player("Bob")
    battle(alice, bob)
