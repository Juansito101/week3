#List

1. Lists



a. Using a range function, generate a list of 100 integers and assign the list to my_list. Verify that the variable my_list data type is list. Use your favorite four methods and apply on the list. You can find the methods on Python Docs



# Step 1: Generate a list of 100 integers
my_list = list(range(100))  # Creates a list from 0 to 99

# Step 2: Verify that my_list is of type list
print(type(my_list))  # Output should be: <class 'list'>



-----------------------------------------------

# Method 1: append() - add an element at the end
my_list.append(100)
print("After append:", my_list[-5:])  # Show last 5 elements



# Method 2: remove() - remove a specific element
my_list.remove(50)
print("After remove 50:", 50 in my_list)  # Should be False





# Method 3: reverse() - reverse the list
my_list.reverse()
print("First 5 elements after reverse:", my_list[:5])




# Method 4: count() - count occurrences of an element
count_25 = my_list.count(25)
print("Occurrences of 25:", count_25)






b. Suppose that you have a list of 10 items long. How might you move the last three items from the end of the list to the beginning, keeping them in the same order?


my_list = [1,2,3,4,5,6,7,8,9,10] 

index = 7,8,9 first



-------------------------------------------------


lst = lst[-3:] + lst[:-3]



check results


lst = [1,2,3,4,5,6,7,8,9,10]
lst = lst[-3:] + lst[:-3]
print(lst)


results:

[8, 9, 10, 1, 2, 3, 4, 5, 6, 7]










c. What would be the result of len([[1,2]] * 3)? Try to do it without coding and then verify using Python.


len([[1,2]] * 3)

#[[1,2]] is a list containing one element, and that element is another list [1,2].


if you multiply then it becomes


[[1,2], [1,2], [1,2]]

# Python repeats the outer list three times.

outer layer is now 3 elements.



results would be

len([[1,2]] * 3) = 3


verify with Python

result = [[1,2]] * 3
print(result)
print(len(result))


output:

[[1, 2], [1, 2], [1, 2]]
3













d. Create a list my-list-ten of 10 items that includes some duplicate entries. 

Then, generate a second list my-list-ten-mem that contains the memory addresses of the items from the list my-list-ten. 

Use Python to research and identify the unique and duplicate memory addresses.



my_list_ten = [4, 3, 5, 3, 7, 9, 1, 11, 7, 1]


my_list_ten_mem = [id(item) for item in my_list_ten]
print(my_list_ten_mem)








e. Delete the list my-list-ten created in the above step.



del my_list_ten


check results

print(my_list_ten)


resulst would be 

NameError








f. Create a new list my-new-list of the same 10 items used in my-list-ten. Generate memory addresses of the items in my-new-list and compare them with the memory addresses in my-list-ten-mem. Discuss what do you observe.



my-new-list = [4, 3, 5, 3, 7, 9, 1, 11, 7, 1]
my-new-list_mem = [id(item) for item in my-new-list]
print(my-new-list_mem)




the memory addresses in my_new_list_mem are the same stored as my_list_ten_mem.  The duplicate values share the same memory address within the list.







g. Suppose that you have the following list: x = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]. What code could you use to get a copy y of that list in which you could change the elements without the side effect of changing the contents of x?

x = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]


y = x.copy()




h. Is it possible to use multiple expressions within a list comprehension?


Yes, but only if a list comprehension multiple for loops and if filters.


ex.

pairs = [(x, y) for x in range(3) for y in range(2)]
print(pairs)

results

[(0, 0), (0, 1), (1, 0), (1, 1), (2, 0), (2, 1)]







i. Using a list comprehension, count how many spaces are in the following statement. "To be, or not to be, this is the question"



statement = "To be, or not to be, this is the question"
space_count = len([char for char in statement if char == " "])
print(space_count)




more ex.

space_count = sum(1 for char in statement if char == " ")



more ex.
space_count = statement.count(" ")





j. Choose any 5 lists operations of your choice from the link https://docs.python.org/3/tutorial/datastructures.html




1.list.clear()
Remove all items from the list. Similar to del a[:].



2.list.insert(i, x)

Insert an item at a given position. The first argument is the index of the element before which to insert, so a.insert(0, x) inserts at the front of the list, and a.insert(len(a), x) is equivalent to a.append(x).



3.list.count(x)
Return the number of times x appears in the list.




4.list.sort(*, key=None, reverse=False)
Sort the items of the list in place (the arguments can be used for sort customization, see sorted() for their explanation).




5.list.copy()
Return a shallow copy of the list. Similar to a[:].








Challenges


Please describe the challenges you faced during the exercise.


# It was challenging to understand ranger and converting to list
# remembering and choosing the methods to modify and analyze	
# unexpected results when you mix them
#
#
#
