import time
import random

GREEN = "\033[92m"
RED = "\033[91m"
RESET = "\033[0m"

print(GREEN + """
╔════════════════════════════╗
║       CYBER TERMINAL       ║
║       SYSTEM ONLINE        ║
╚════════════════════════════╝
""" + RESET)

name = input("Enter username: ")

print("\nInitializing system...")
time.sleep(1)

for i in range(1, 101, 10):
    print(f"Loading... {i}%")
    time.sleep(0.3)

print("\nSystem ready!")
print("Welcome,", name)

secret = random.randint(1, 10)

print("\nGuess the secret number (1-10)")

while True:
    guess = input(">>> ")

    if not guess.isdigit():
        print(RED + "Enter a valid number!" + RESET)
        continue
