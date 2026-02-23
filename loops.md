

1. While loop
a. Please write Python code using a while loop to perform the following steps.

Take any non-negative and non-zero integer number and name it n0
if the number is even, evaluate a new n0 as n0 ÷ 2;
Otherwise, if the number is odd, evaluate a new n0 as 3 * n0 + 1;
if n0 is not equal to 1, go to point 2.


Sample input: 16
Expected output:


8
4
2
1
steps = 4


n0 = int(input("Enter a non negative, non zero integer: "))

while n0 !=1:
	print(n0)

	if n0 % 2 == 0:   # if even
	     n0 = n0 // 2
	else:              # if odd
	     n0 = 3 * n0 + 1

print(1)









b. Write code that uses a while loop and runs indefinitely. Modify the same code to resolve the infinite loop issue.


while True:
    print("This will run forever!")

# while True is always True so loop never stops


#need to create a condition that eventually becomes fales.

count = 0

while count < 5:  # condition will eventually be False
    print("Count is", count)
    count += 1     # increment count to avoid infinite loop













c. Write a program that takes two integers as input and asks the user to choose an arithmetic operation to perform with those numbers. 

At the end of the program, prompt the user with the question, "Do you want to continue?" 

If the user selects "Y" or "y," the program should restart; otherwise, it should exit and display the message, "Have a good day."





# Take two integers as input

num1 = int(input("Enter the first integer: "))
num2 = int(input("Enter the second integer: "))

# Show operation choices

print("Choose an operation:")
print("1. Addition (+)")
print("2. Subtraction (-)")
print("3. Multiplication (*)")
print("4. Division (/)")

# Take user's choice

choice = input("Enter 1, 2, 3, or 4: ")



# Perform the selected operation

if choice == "1":
    result = num1 + num2
    operation = "+"
elif choice == "2":
    result = num1 - num2
    operation = "-"
elif choice == "3":
    result = num1 * num2
    operation = "*"
elif choice == "4":
    if num2 != 0:
        result = num1 / num2
        operation = "/"
    else:
        result = "Error: Division by zero!"
else:
    result = "Invalid choice"
    operation = ""

# Display the result
print(f"{num1} {operation} {num2} = {result}")



---------------------------------------------

    # Ask if user wants to continue
    user_input = input("Do you want to continue? (yes/no): ").strip().lower()
    if user_input != "yes":
        continue_calculation = False
        print("Have a good day.")













2. For loops


a. Write a code that counts the total number of characters in a text and also counts each character individually. 


For example, consider the sentence "To be, or not to be, that is the question." The code should determine the total number of letters and how many times each letter appears, including specific counts for the letters 't' and 'o', etc. 

Ignore the upper and lower cases letters, and any punctuations symbols. Use only for loop, while loop, break and continue statements where necessary.





Sample input: To be, or not to be, that is the question
Expected output:
Total number of alphabets: 30
Total number of distinct alphabets are:
T = 7
o = 4




# Take input from user
text = input("Enter a sentence: ")

# Convert text to lowercase to ignore case
text = text.lower()

# Initialize total count of alphabets
total_letters = 0

# Dictionary to store counts of each letter
letter_counts = {}

# Loop through each character in the text
for char in text:
    # Ignore non-alphabet characters
    if not char.isalpha():
        continue
    
    # Increment total letter count
    total_letters += 1
    
    # Count each letter
    if char in letter_counts:
        letter_counts[char] += 1
    else:
        letter_counts[char] = 1

# Print total letters
print("Total number of alphabets:", total_letters)

# Print counts of distinct letters
print("Total number of distinct alphabets are:")
for letter, count in letter_counts.items():
    print(f"{letter} = {count}")



Enter a sentence: juan is ok
Total number of alphabets: 8
Total number of distinct alphabets are:
j = 1
u = 1
a = 1
n = 1
i = 1
s = 1
o = 1
k = 1

Process finished with exit code 0




Note: The expected output above is incomplete. The sum of the total distinct alphabets must equal the total number of alphabets in the given text.








Challenges
Please describe the challenges you faced during the exercise.

#  It was challenging to loop evens and converting them to a equation
#  It was challenging to ignore case and punctuation 
#  It was challenging to skip non alphabetic characters and using continue
#  It was challenging to track each letter individually
#
#
#
