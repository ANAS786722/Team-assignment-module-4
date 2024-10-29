# Team-assignment-module-4\
import random

def guessing_game():
    while True:
        # Generate a random number between 1 and 10
        random_number = random.randint(1, 10)
        print("Please guess the number between 1 and 10.")
        
        while True:
            user_guess = int(input("Enter your guess: "))
            
            if user_guess < random_number:
                print("Higher! Try again.")
            elif user_guess > random_number:
                print("Lower! Try again.")
            else:
                print("Well done, you guessed it!")
                break  # Exit the inner loop if guessed correctly

        # Ask if the user wants to play again
        play_again = input("Would you like to guess another number? (Y/N): ").strip().lower()
        if play_again != 'y':
            print("Thanks for playing!")
            break  # Exit the outer loop if the user does not want to play again

# Run the game
guessing_game()
