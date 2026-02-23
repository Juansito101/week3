#1.
# To find the ASCII number of all the characters available on the keyboard


for i in range(128):
    print(f"ASCII: {i}  Character: {repr(chr(i))}")

#2.
10 > 4 and 50 < 100
10 < 4 and 50 < 100

10 < 4 or 50 > 100  # False and False is False
10 > 4 and 50 > 100  # Here first expression is True, the output will be True

10 > 4 # this is True
not(10 > 4) # this is False

#3.

x = 0b1110 # 0b represents binary number, decimal 14
y = 0b1011 # decimal 11
result = x | y # Bitwise or, result in decimal format
print(result)
print(bin(result)) # bin() function converts decimal to binary

# Proof
# 1110
# 1011
# ----
# 1111



#4

# Read two numbers
number1 = int(input("Enter the first number: "))
number2 = int(input("Enter the second number: "))

# Choose the larger number
if (number1 > number2):
    larger_number = number1
else:
    larger_number = number2

# Print the result
print("The larger number is:", larger_number)


Enter the first number: 20
Enter the second number: 30
The larger number is: 30

Process finished with exit code 0

#nested

x = 10

if x > 5:  # True
    if x == 6:  # False
        print("nested: x == 6")
    elif x == 10:  # True
        print("nested: x == 10")
    else:
        print("nested: else")
else:
    print("else")








#5
#a.

a = int(input("Enter first number: "))
b = int(input("Enter second number: "))
c = int(input("Enter third number: "))

if a >= b and a >= c:
    print("Largest number is:", a)

if b >= a and b >= c:
    print("Largest number is:", b)

if c >= a and c >= b:
    print("Largest number is:", c)


#b.

#using and operator

num = int(input("Enter an integer: "))   #  here is where user enters input integer

if num & 1 == 0:        #  here is where it determines if it's even
    print("even")
else:                    #  if not then it will print odd
    print("odd")


#using multiplication and division

num = int(input("Enter an integer: "))      #  here is where it determines if it's even

if num & 1 == 0:       #  here is where it determines if it's even
    print("even")
else:                     #  if not then it will print odd
    print("odd")





#c.


#Takes percentage of input from user
percentage = int(input("Enter your percentage: "))

# Check grade conditions
if percentage > 90:
    print("Grade: A")       # Grade A condition
    print("Description: Work of genuinely superior quality.")

elif percentage >= 80 and percentage <= 89:
    print("Grade: B")        # Grade B condition
    print("Description: Passing performance falls approximately in the upper distribution of passing grades.")

elif percentage >= 71 and percentage <= 79:
    print("Grade: C")        # Grade C condition
    print("Description: Passing performance falls approximately in the center of the distribution of all passing grades.")

elif percentage >= 65 and percentage <= 70:
    print("Grade: D")           # Grade D condition
    print("Description: Passing performance falls approximately in the lower distribution of passing grades.")

elif percentage < 65:
    print("Grade: F")        # Grade F condition
    print("Description: Failing performance that does not satisfy the basic requirements of the course and needs to be improved in significant ways.")

else:
    # Handles any invalid inputs like negative numbers
    print("Invalid percentage entered.")



#d.

#Take operator input from user
operator = input("Enter a logical operator (and, or, not): ").lower()

print("\nTruth Table:\n")

#######################
# AND Operator
#######################

if operator == "and":
    print("A\tB\tA and B")
    print("----------------")
    print("True\tTrue\t", True and True)
    print("True\tFalse\t", True and False)
    print("False\tTrue\t", False and True)
    print("False\tFalse\t", False and False)

#######################
# OR Operator
#######################

elif operator == "or":
    print("A\tB\tA or B")
    print("----------------")
    print("True\tTrue\t", True or True)
    print("True\tFalse\t", True or False)
    print("False\tTrue\t", False or True)
    print("False\tFalse\t", False or False)

#######################
# NOT Operator
#######################

elif operator == "not":
    print("A\tnot A")
    print("--------------")
    print("True\t", not True)
    print("False\t", not False)

#######################
# Invalid Input
#######################

else:
    print("Invalid operator! Please enter and, or, or not.")




#e.  

num = int(input("Enter an integer: "))

if num & 1 == 0:
    print("even")
else:
    print("odd")

Enter an integer: 6
even

Process finished with exit code 0


#6. code revision

# Have user enter their name
name = input("What's your name? ")

#Ask the user for the current time
time = int(input("What time is it? "))



# Check if the time entered is valid
if time >= 0 and time <= 2359:
    
    # Check if it is morning (before 12:00)
    if time < 1200:
        print("Hi " + name + ", good morning!")
    
    # If not morning, check if it is afternoon (12:00 to 17:59)
    elif time < 1800:
        print("Hi " + name + ", good afternoon!")
    
    # Otherwise, it must be evening (18:00 to 23:59)
    else:
        print("Hi " + name + ", good evening!")

# If the time entered is invalid
else:
    print("Invalid time entered.")

# Goodbye message (always printed)
print("Good Bye")




#7  Output Verification



x = 1
y = 1.0
z = "1"

if x == y:
    print("one")
if y == int(z):
    print("two")
elif x == y:
    print("three")
else:
    print("four")



------------------------------------------


x = 1 
y = 1.0 
z = "1" 


x is an integer → 1

y is a float → 1.0

z is a string → "1"



if x == y: print("one") 
#  1 == 1.0 is True

if y == int(z): print("two") 
#  int(z) converts "1" to integer 1

elif x == y: print("three") 

else: print("four")


Final output
one
two




#  It was challenging to know if it was a question or not.
#  It was challenging to remember the bit operators
#  It was challenging to find out how to put the last 3 intergers to be in front of the output results
#

















