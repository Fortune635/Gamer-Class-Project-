# 🎮 Gamer Class Example
# Author: Fortune Akioya
# Date: October 2025

# Base class
class Gamer:
    def __init__(self, username, level, game):
        self.username = username
        self.level = level
        self.game = game
        self.__score = 0   # Encapsulated attribute (private)

    def play_game(self):
        print(f"{self.username} is playing {self.game} at level {self.level}!")

    def update_score(self, points):
        self.__score += points
        print(f"{self.username} earned {points} points! Total score: {self.__score}")

    def get_score(self):
        return self.__score

    def __str__(self):
        return f"Gamer(username='{self.username}', level={self.level}, game='{self.game}')"


# Derived class (Inheritance)
class ProGamer(Gamer):
    def __init__(self, username, level, game, rank):
        super().__init__(username, level, game)
        self.rank = rank

    # Polymorphism: overriding play_game()
    def play_game(self):
        print(f"🔥 Pro Gamer {self.username} is dominating {self.game} at level {self.level} (Rank: {self.rank})!")

    def participate_tournament(self):
        print(f"{self.username} is competing in an international {self.game} tournament!")


# Create objects from the classes
player1 = Gamer("ShadowNinja", 5, "Minecraft")
player2 = ProGamer("Fortune", 12, "Call of Duty", "Elite")

# Demonstrate functionality
player1.play_game()
player1.update_score(120)
print(f"{player1.username}'s Score:", player1.get_score())

print("\n---\n")

player2.play_game()
player2.update_score(300)
player2.participate_tournament()
print(f"{player2.username}'s Score:", player2.get_score())
