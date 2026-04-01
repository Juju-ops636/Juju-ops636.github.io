# Juju-ops636.github.io
import random

def play_game():
    number = random.randint(1, 100)
    attempts = 0
    print("I'm thinking of a number between 1 and 100.")

    while True:
        try:
            guess = int(input("Enter your guess: "))
            attempts += 1
            if guess < number:
                print("Too low! Try again.")
            elif guess > number:
                print("Too high! Try again.")
            else:
                print(f"Correct! You won in {attempts} tries.")
                break
        except ValueError:
            print("Please enter a valid number.")
