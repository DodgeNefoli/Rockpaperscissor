# Rockpaperscissor
# Small game of rock paper scissor
import random

comp = random.randint(0, 2)

try:
    user = int(input("Enter 0 for rock, 1 for paper, and 2 for scissors\n"))
    if user < 0 or user > 2:
        raise ValueError
except ValueError:
    print("Enter a valid number brother")
    exit()
  # Exit if the input is invalid

def game(comp, user):
    if comp == user:
        return 0
    elif (comp == 0 and user == 2) or (comp == 1 and user == 0) or (comp == 2 and user == 1):
        return -1
    else:
        return 1

result = game(comp, user)
print(f"Computer has chosen {comp}")
print(f"You have chosen {user}")

if result == 0:
    print("Brother, it's a draw.")
elif result == -1:
    print("Sorry mate, you lose.")
else:
    print("Cheers mate, you won this.")
