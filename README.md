# Number Guessing Game
# The computer picks a secret number, player tries to guess it

# For now we'll hardcode the number (you can change it each time you play)
secret_number = 42

# Later you can replace the line above with this (after we learn random):
# import random
# secret_number = random.randint(1, 100)

print("Welcome to the Number Guessing Game!")
print("I'm thinking of a number... try to guess it!")
print()  # empty line for nicer output

guess_count = 0

while True:
    # Get guess from player
    guess = input("Your guess: ")
    
    # Make sure it's actually a number
    if not guess.isdigit():
        print("Please enter a whole number (no letters or decimals)")
        continue
    
    # Convert to integer
    guess = int(guess)
    guess_count += 1
    
    # Now check the guess
    if guess == secret_number:
        print("🎉 Congratulations! You got it!")
        print(f"It took you {guess_count} guesses.")
        break
        
    elif guess < secret_number:
        print("Too low! Try a bigger number.")
        
    else:  # guess > secret_number
        print("Too high! Try a smaller number.")
    
    print()  # empty line between guesses

print("Game over. Thanks for playing!")
