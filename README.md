# first-rep
import random

def game():
    # generate a random number between 1 and 50
    target = random.randint(1, 50)

    # initialize the number of attempts
    attempts = 0

    while True:
        # ask the user for their guess
        guess = input("Guess a number between 1 and 50: ")

        # try to convert the user's guess to an integer
        try:
            guess = int(guess)
        except ValueError:
            print("That's not a valid number. Please try again.")
            continue

        # increment the number of attempts
        attempts += 1

        # check if the guess is too high, too low, or correct
        if guess < target:
            print("Too low!")
        elif guess > target:
            print("Too high!")
        else:
            print(f"Congratulations! You guessed the number in {attempts} attempts.")
            break

# start the game
game()
