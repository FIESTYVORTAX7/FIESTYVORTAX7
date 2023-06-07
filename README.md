- 👋 Hi, I’m @FIESTYVORTAX7
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
FIESTYVORTAX7/FIESTYVORTAX7 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
import random

def generate_bomb_location():
    row = random.randint(0, 4)
    col = random.randint(0, 4)
    return row, col

def calculate_distance(row1, col1, row2, col2):
    return abs(row1 - row2) + abs(col1 - col2)

def play_bomb_squad():
    bomb_row, bomb_col = generate_bomb_location()

    print("Welcome to Bomb Squad!")
    print("Can you find and defuse the bomb?")

    attempts = 0
    while True:
        guess_row = int(input("Enter row (0-4): "))
        guess_col = int(input("Enter column (0-4): "))

        if guess_row == bomb_row and guess_col == bomb_col:
            print("Congratulations! You've defused the bomb!")
            break

        distance = calculate_distance(guess_row, guess_col, bomb_row, bomb_col)
        print(f"Close, but you're {distance} units away from the bomb.")
        attempts += 1

    print(f"You defused the bomb in {attempts} attempts.")

play_bomb_squad(fiestyvsslash
)

