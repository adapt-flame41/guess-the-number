# guess-the-number
import random

def guess_the_number():
    number_to_guess = random.randint(1, 100)
    attempts = 0
    print("Welcome to Guess the Number!")
    print("I'm thinking of a number between 1 and 100.")

    while True:
        try:
            guess = int(input("Enter your guess: "))
            attempts += 1

            if guess < number_to_guess:
                print("Too low!")
            elif guess > number_to_guess:
                print("Too high!")
            else:
                print(f"Congratulations! You guessed it in {attempts} attempts.")
                break

        except ValueError:
            print("Invalid input! Please enter a number only.")

# Main loop to replay the game
while True:
    guess_the_number()
    play_again = input("Do you want to play again? (y/n): ").strip().lower()
    if play_again != "y":
        print("Thanks for playing! Goodbye.")
        break
