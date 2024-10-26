# codesoft_taskno2

# Python program for simple calculator

# Function to add two numbers
def add(num1, num2):
    return num1 + num2

# Function to subtract two numbers
def subtract(num1, num2):
    return num1 - num2

# Function to multiply two numbers
def multiply(num1, num2):
    return num1 * num2

# Function to divide two numbers
def divide(num1, num2):
    return num1 / num2

print("Please select operation -\n" \
        "1. Add\n" \
        "2. Subtract\n" \
        "3. Multiply\n" \
        "4. Divide\n")


# Take input from the user
select = int(input("Select operations form 1, 2, 3, 4 :"))

number_1 = int(input("Enter first number: "))
number_2 = int(input("Enter second number: "))

if select == 1:
    print(number_1, "+", number_2, "=",
                    add(number_1, number_2))

elif select == 2:
    print(number_1, "-", number_2, "=",
                    subtract(number_1, number_2))

elif select == 3:
    print(number_1, "*", number_2, "=",
                    multiply(number_1, number_2))

elif select == 4:
    print(number_1, "/", number_2, "=",
                    divide(number_1, number_2))
else:
    print("Invalid input")

   
    
# codesoft_taskno3:


import string
import random

# Getting password length
length = int(input("Enter password length: "))

print('''Choose character set for password from these : 
		1. Digits
		2. Letters
		3. Special characters
		4. Exit''')

characterList = ""

# Getting character set for password
while(True):
	choice = int(input("Pick a number "))
	if(choice == 1):
		
		  # Adding letters to possible characters
		
  characterList += string.ascii_letters
	elif(choice == 2):
		
		# Adding digits to possible characters
		
  characterList += string.digits
	elif(choice == 3):
		
		# Adding special characters to possible
		# characters
		
  characterList += string.punctuation
	elif(choice == 4):
		break
	else:
		print("Please pick a valid option!")

password = []

for i in range(length):

	# Picking a random character from our 
	# character list
	
 randomchar = random.choice(characterList)
	
	# appending a random character to password
	
 password.append(randomchar)

# printing password as a string
print("The random password is " + "".join(password))

    

# codesoft_taskno4:
import random

# Print multiline instruction
print('Winning rules of the game ROCK PAPER SCISSORS are:\n'
      + "Rock vs Paper -> Paper wins \n"
      + "Rock vs Scissors -> Rock wins \n"
      + "Paper vs Scissors -> Scissors wins \n")

while True:

    
  print("Enter your choice \n 1 - Rock \n 2 - Paper \n 3 - Scissors \n")

    # Take the input from user
  choice = int(input("Enter your choice: "))

    # Looping until user enters valid input
  while choice > 3 or choice < 1:
        choice = int(input('Enter a valid choice please : '))

    # Initialize value of choice_name variable corresponding to the choice value
  if choice == 1:
        choice_name = 'Rock'
  elif choice == 2:
        choice_name = 'Paper'
  else:
        choice_name = 'Scissors'

    # Print user choice
  print('User choice is:', choice_name)
  print("Now it's Computer's Turn...")

    # Computer chooses randomly any number among 1, 2, and 3
  comp_choice = random.randint(1, 3)

    # Initialize value of comp_choice_name variable corresponding to the choice value
  if comp_choice == 1:
        comp_choice_name = 'Rock'
  elif comp_choice == 2:
        comp_choice_name = 'Paper'
  else:
        comp_choice_name = 'Scissors'

  print("Computer choice is:", comp_choice_name)
  print(choice_name, 'vs', comp_choice_name)

    # Determine the winner
  if choice == comp_choice:
        result = "DRAW"
  elif (choice == 1 and comp_choice == 2) or (comp_choice == 1 and choice == 2):
        result = 'Paper'
  elif (choice == 1 and comp_choice == 3) or (comp_choice == 1 and choice == 3):
        result = 'Rock'
  elif (choice == 2 and comp_choice == 3) or (comp_choice == 2 and choice == 3):
        result = 'Scissors'

    # Print the result
  if result == "DRAW":
        print("<== It's a tie! ==>")
  elif result == choice_name:
        print("<== User wins! ==>")
  else:
        print("<== Computer wins! ==>")

    # Ask if the user wants to play again
  print("Do you want to play again? (Y/N)")
    ans = input().lower()
  if ans == 'n':
        break

  # After coming out of the while loop, print thanks for playing
print("Thanks for playing!")
