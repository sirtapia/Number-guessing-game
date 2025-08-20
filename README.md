# Number-guessing-game
#day 1-100 (day 4 project)  number guessing game 
#day 4 quick project
import random
print("Welcome to the Number Guessing Game!")
print("I'm thinking of a number between 1 and 100")
print("Please select the difficulty level")
print("""
1. Easy (10 chances)
2. Medium (5 chances)
3. Hard (3 chances)""")
level = int(input("Please enter your choice: "))

def game(level):
  number = random.randint(1,100)
  if level == 1:
    chances = 10
    print("Great! You have selected easy level")   
  elif level == 2:
    chances = 5
    print("Great! You have selected medium level")
  elif level == 3:
    chances = 3
    print("Great! You have selected hard level")
  else:
    print("Invalid option") 
    return


#checking the guesses 
  for i in range(chances):
    print(f"You have {chances-i} attempts left")
    guess = int(input("Please enter your guess: "))
  
  if guess == number:
    print(f"You got it! You guessed the number in {i+1} attempts")
    return
  elif guess > number:
    print(f"the number is greater than {guess}")
  else:
    print(f"the number is less than {guess}")
 
    return
    

  print("You have no attempts left")
  print(f"The number was {number}")

while True: 
  print("Welcome to the Number Guessing Game!")
  print("I'm thinking of a number between 1 and 100")
