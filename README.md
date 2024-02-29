import random

def guess_number():
    secret_number = random.randint(1, 100)
    max_attempts = 5
    attempts = 0
    
    print("I have chosen a number between 1 and 100. Try to guess what it is!")
    
    while attempts < max_attempts:
        try:
            guess = int(input("Enter your guess: "))
            attempts += 1
            
            if guess < secret_number:
                print("Too low! Keep guessing!")
            elif guess > secret_number:
                print("Too high! Keep guessing!")
            else:
                print("Congratulations, you guessed it! It took you {} attempts.".format(attempts))
                break
        except ValueError:
            print("Please enter a valid number!")
    
    if attempts == max_attempts:
        print("Sorry, you have used up all your attempts. The correct answer was {}.".format(secret_number))

guess_number()
