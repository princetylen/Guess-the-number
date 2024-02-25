# Guess-the-number
import random

def guess_number(low, high):
    number = random.randint(low, high)
    attempts = 0
    while True:
        user_guess = int(input("Guess the number between {} and {}: ".format(low, high)))
        if user_guess == number:
            print("Congratulations! You guessed the correct number in", attempts, "attempts.")
            break
        elif user_guess < number:
            print("Too low! Try again.")
        else:
            print("Too high! Try again.")
        attempts += 1

if __name__ == "__main__":
    low = 1
    high = 100
    print("Welcome to the number guessing game!")
    print("I'm thinking of a number between {} and {}.".format(low, high))
    guess_number(low, high)
