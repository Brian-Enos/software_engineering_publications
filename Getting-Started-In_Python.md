
# **Getting Started in Python**
## **Introduction**

Python is a high-level, interpreted programming language that was created by Guido van Rossum and released in 1991. It is designed to be easy to read and write, with a focus on code readability, and has become one of the most popular programming languages in use today.

Interpreted programming languages use an interpreter for their translation, unlike compiled languages such as C which use compilers for their translation.

An interpreter reads the source code of a program line by line and executes each line as it is read. Python is an interpreted language, which means that it uses an interpreter to execute code.

Python is an object-oriented language, which means it allows you to create reusable blocks of code that can be used across different parts of your program. It also supports functional programming, which allows you to write code that is more modular and easier to test.

Python has an extensive standard library, which provides a wide range of pre-built modules and functions that can be used for tasks such as file I/O, web programming, and regular expressions. In addition, there are many third-party libraries available for Python, which can extend its capabilities even further.

Python is commonly used in fields such as data analysis, scientific computing, web development, and artificial intelligence. It is also popular among beginners due to its ease of use and gentle learning curve.

### **Why Translators?**

We use translators to convert code written in a high-level programming language into a low-level language that can be executed by the computer's CPU. This process is known as "interpretation,"

Both interpreters and compilers have their advantages and disadvantages. Interpreters are generally easier to use and debug, while compilers can generate faster and more efficient code. However, they require more setup and configuration.

### **So, Why should one learn Python?**

There are many reasons why someone might want to learn Python.

Here are a few Reasons:

**Versatility**

Python is a versatile programming language that can be used for a wide range of tasks, from web development to data analysis to machine learning.

**Easy to Learn**

Python is relatively easy to learn, even for beginners. It has a simple syntax that makes it easy to read and understand.

**Huge Community**

Python has a large and supportive community of developers who are constantly creating new libraries and tools to make programming in Python easier and more efficient.

**Career Opportunities**

Python is widely used in a variety of industries, from tech to finance to healthcare. Learning Python can open up a wide range of career opportunities.

**Automation**

Python is great for automation tasks, such as web scraping or automating repetitive tasks.

## **Python Indentation**

Python indentation refers to the whitespace at the beginning of a line of code, which is used to define the code blocks in Python. In Python, code blocks are defined by their indentation, rather than using curly braces or other syntax. The level of indentation determines which code belongs to which block, making the code more readable and easier to follow.

Example

```c
first_name = "Brian"
middle_name = "AboveTheLaw"
if first_name == "Brian" :
    print("Hello Brian!")
    if middle_name == "Enos" :
        print("Goodmorning Brian Enos")  
else:
    print("We don't know you")
```

**Code Explained**

* The first two lines of code are not indented, indicating that they are at the top level and will be executed regardless of any conditions.
    
* The `if` statement that checks if `first_name` equals "Brian" is indented, indicating that the subsequent block of code is part of the `if` block. If the condition is true, the code inside the `if` block will be executed.
    
* The `print("Hello Brian!")` statement is indented further, indicating that it is part of the `if` block and will only be executed if the condition is true.
    
* The nested `if` statement that checks if `middle_name` equals "Enos" is indented even further, indicating that it is part of the `if` block that checks `first_name`. If both conditions are true, the code inside this nested `if` block will be executed.
    
* The `print("Goodmorning Brian Enos")` statement is indented further still, indicating that it is part of the nested `if` block and will only be executed if both conditions are true.
    
* The `else` statement is not indented, indicating that it is not part of any code block and will be executed only if the initial `if` statement is false. If `first_name` does not equal "Brian", the `else` block will be executed and the message "We don't know you" will be printed
    

## **Variables, Data Types and Operators**

### **Variables**

Variables are used to store data values that can be used throughout a program. They are essentially labels or names that refer to specific values in memory and can be assigned and reassigned different values as needed.

### **Data Types**

Data types are the classification of data items based on the type of value they hold. Python has built-in support for various data types, including numeric, string, boolean, and sequence types.

**Commonly used Data Types in Python**

1. **Numeric Types:**
    
    * Integer: `x = 10`
        
    * Floating-point numbers: `x = 3.14159`
        
    * Complex numbers: `x = 2 + 3j`
        
2. **Boolean type:**
    
    * Boolean: `x = True`
        
3. **Sequence Types:**
    
    * Strings: `x = "Hello World"`
        
    * Lists: `x = [1, 2, 3, 4]`
        
    * Tuples: `x = (1, "apple", 3.14)`
        
    * Byte arrays: `x = bytearray(b'Hello')`
        
    * Byte strings: `x = b'Hello'`
        
    * Range objects: `x = range(5)`
        
4. **Mapping Type:**
    
    * Dictionary: `x = {"name": "Brian", "age": 23, "city": "Nairobi"}`
        
5. **Set Types**:
    
    * Set: `x = {1, 2, 3}`
        
    * Frozen set: `x = frozenset({1, 2, 3})`
        

> NOTE: We will use all these as we progress further in this series. Hang in tight!

### **Operators**

Operators in Python are symbols or special keywords used to perform operations on values or variables. Python supports a wide range of operators, including arithmetic, comparison, logical, assignment, and bitwise operators

**Commonly used Operators in Python**

1. **Arithmetic operators:**
    
    * Addition: `2 + 3` returns `5`
        
    * Subtraction: `5 - 2` returns `3`
        
    * Multiplication: `2 * 3` returns `6`
        
    * Division: `6 / 2` returns `3`
        
    * Modulo: `5 % 2` returns `1`
        
    * Exponentiation: `2 ** 3` returns `8`
        
2. **Comparison operators:**
    
    * Equal to: `2 == 3` returns `False`
        
    * Not equal to: `2 != 3` returns `True`
        
    * Greater than: `5 > 2` returns `True`
        
    * Less than: `2 < 5` returns `True`
        
    * Greater than or equal to: `5 >= 5` returns `True`
        
    * Less than or equal to: `2 <= 5` returns `True`
        
3. **Logical operators:**
    
    * And: `True and False` returns `False`
        
    * Or: `True or False` returns `True`
        
    * Not: `not True` returns `False`
        
4. **Assignment operators:**
    
    * Assign: `x = 5`
        
    * Add and assign: `x += 2` is equivalent to `x = x + 2`
        
    * Subtract and assign: `x -= 2` is equivalent to `x = x - 2`
        
    * Multiply and assign: `x *= 2` is equivalent to `x = x * 2`
        
    * Divide and assign: `x /= 2` is equivalent to `x = x / 2`
        
    * Modulo and assign: `x %= 2` is equivalent to `x = x % 2`
        
    * Exponentiation and assign: `x **= 2` is equivalent to `x = x ** 2`
        
    * Floor division and assign: `x //= 2` is equivalent to `x = x // 2`
        
5. **Bitwise operators:**
    
    * Bitwise AND: `0b1010 & 0b1100` returns `0b1000`
        
    * Bitwise OR: `0b1010 | 0b1100` returns `0b1110`
        
    * Bitwise XOR: `0b1010 ^ 0b1100` returns `0b0110`
        
    * Bitwise NOT: `~0b1010` returns `-0b1011`
        
    * Left shift: `0b1010 << 2` returns `0b101000`
        
    * Right shift: `0b1010 >> 2` returns `0b10`
        

# Lists In Python

A list is a data structure that is used to store an ordered collection of items. Lists can contain elements of different data types, such as integers, strings, and even other lists; this means that the elements in the list don't have to be related in any way.

Lists are mutable, which means their elements can be modified after creation.

To create a list in Python, you can use square brackets `[]` and separate the items with commas.

Therefore, lists allow you to store sets of information in one place.

**List Prototype**

```c
name_of_list = [item1, item2, item3, ...]
```

The `name_of_list` is the name of the list and `item1`, `item2`, `item3`, and so on, are the items that make up the list. The items can be of any data type, including numbers, strings, booleans, and even other lists.

## **Accessing Elements in a List**

A list is a collection of items that can be accessed by their index. The index starts at 0 for the first element and increases by 1 for each subsequent element. To access an element in a list, you simply use its index within square brackets.

**Example**

```c
motorcycles =  ['honda', 'yamaha', 'suzuki', 'tvs']
print(motorcycles[1])
```

**Code output**

```c
yamaha
```

You can also apply the string methods on any element of the list.

**Example**

```c
motorcycles =  ['honda', 'yamaha', 'suzuki', 'tvs']
print(motorcycles[1].title())
```

**Code Output**

```c
Yamaha
```

## **Types of Indexing**

* ### **Positive Indexing**
    
* ### **Negative indexing**
    

### **Positive Indexing**

Positive indexing is used to access elements in a sequence, such as a list or a string. It starts from 0 and counts from left to right, with the first element having an index of 0. Positive indexing is commonly used in Python programs to access and manipulate elements in a sequence.

**Example**

```c
motorcycles =  ['honda', 'yamaha', 'suzuki', 'tvs']
```

* **Accessing the first element using positive indexing:**
    

```c
print(motorcycles[0])
```

**Output**

```c
honda
```

* Accessing the second element using positive indexing:
    

```c
print(motorcycles[1])
```

**Output**

```python
yamaha
```

* **Accessing the third element using positive indexing:**
    

```python
print(motorcycles[2])
```

**Output**

```python
suzuki
```

* **Accessing the fourth element using positive indexing:**
    

```python
print(motorcycles[3])
```

**Output**

```python
tvs
```

### **Negative Indexing**

Negative indexing allows access to elements from the end of the list, starting from -1 and counting from right to left. The last element in the list has an index of -1, the second last has an index of -2, and so on. Negative indexing is useful in situations where you need to access elements from the end of a list without knowing its length

**Example**

```python
motorcycles =  ['honda', 'yamaha', 'suzuki', 'tvs']
```

* **Accessing the first element using negative indexing:**
    

```python
print(motorcycles[-4])
```

**Code Output**

```python
honda
```

* **Accessing the second element using negative indexing:**
    

```python
motorcycles =  ['honda', 'yamaha', 'suzuki', 'tvs']
print(motorcycles[-3])
```

**Code Output**

```python
yamaha
```

* **Accessing the third element using negative indexing:**
    

```python
motorcycles =  ['honda', 'yamaha', 'suzuki', 'tvs']
print(motorcycles[-2])
```

**Code Output**

```python
suzuki
```

* **Accessing the fourth element using negative indexing:**
    

```python
motorcycles =  ['honda', 'yamaha', 'suzuki', 'tvs']
print(motorcycles[-1])
```

**Code output**

```python
tvs
```

## **Changing, Adding and Removing Elements from a List**

### **Modifying Elements in a List**

Modifying elements in a list involves accessing the specific element of the list using its index and assigning a new value to that index.

**Example**

In this example, we are modifying the element at index 0 which is **"honda"**

```c
motorcycles = [ "honda" , "yamaha" , "suzuki"]

motorcycles[0] = "tvs"
print(motorcycles)
```

**Code Output**

```c
['tvs', 'yamaha', 'suzuki']
```

### **Adding Elements in a List**

* **Appending Elements to the End of a List**
    

**Method 1**

This is the simplest way to add an element to a list.

When you append, the new element is added to the end of the list

```c
motorcycles = [ "honda" , "yamaha" , "suzuki"]
print("\n Motorcycles before applying append() method \n")
print(motorcycles)

print("\n Motorcycles after appending ducati\n")
motorcycles.append("ducati")
print(motorcycles)
```

**Code Output**

```c
Motorcycles before applying append() method 

['honda', 'yamaha', 'suzuki']

 Motorcycles after appending ducati

['honda', 'yamaha', 'suzuki', 'ducati']
```

**Method 2**

Append method ***append()*** makes it easy to build lists dynamically

You can start with an empty list and then append elements to the list with a series of append calls.

**Example**

```c
print(" \n Added elements to the list with a series of append calls \n ")
motorcycles = []
motorcycles.append("honda")
motorcycles.append("yamaha")
motorcycles.append("suzuki")

print(motorcycles)
```

**Code Output**

```c
Added elements to the list with a series of append calls

['honda', 'yamaha', 'suzuki']
```

* **Inserting Elements into a List**
    

This is done using the `insert()` method.

The `insert()` method is used to insert an element into a list at a specified index. The method takes two arguments: the first argument specifies the index at which the element will be inserted, and the second argument is the element to be inserted.

The `insert()` method creates a space at the index specified and then stores the value desired in that particular index.

**Example**

```c
motorcycles =  ['honda', 'yamaha', 'suzuki']
motorcycles.insert(2, "ducati")
print(motorcycles)
```

**Code Output**

```c
['honda', 'yamaha', 'ducati', 'suzuki']
```

### **Removing Elements from a List**

* **using** `del` **statement**
    

The `del` statement is used to delete an object, such as a variable or an element of a list. When using `del` with a list, it removes the specified element at the given index, shifting the remaining elements to fill the gap.

**Example**

```c
motorcycles =  ['honda', 'yamaha', 'suzuki']
del motorcycles[1]
print(motorcycles)
```

**Code Output**

```c
['honda', 'suzuki']
```

* **Using**`pop()` **method**
    

**Popping the Last element from the List**

The `pop()` method is used to remove and return the last element of a list. It can also take an optional index argument, which will remove and return the element at the specified index.

The `pop()` method allows us to reuse the removed item from the list.

In practical applications, it can be used to remove a user from a list of active members and add them to a list of inactive members.

**Example**

```c
motorcycles =  ['honda', 'yamaha', 'suzuki']
popped_motorcycle = motorcycles.pop()
print(motorcycles)
```

**Code Output**

```c
['honda', 'yamaha']
```

**Popping Elements from any Position in a List**

You can use pop method to remove any item from a list by providing/including the index of the element you want to remove.

**Example**

```c
motorcycles =  ['honda', 'yamaha', 'suzuki']
popped_motorcycle = motorcycles.pop(1)
print(motorcycles)
```

**Code output**

```c
['honda', 'suzuki']
```

* **Removing an item by value**
    

Removing an item by value from a list involves using the `remove()` method. This method takes a single argument, which is the value to be removed from the list. The method will remove the first occurrence of the value from the list.

Commonly used when working with large data in a list and you don't know the index of the item you want to remove from the.

The `remove()` method allows you to work with the value you removed from the list.

**Example 1**

```c
motorcycles =  ['honda', 'yamaha', 'suzuki', 'tvs']
motorcycles.remove("yamaha")
print(motorcycles)
```

**Code Output**

```c
['honda', 'suzuki', 'tvs']
```

**Example 2**

```c
motorcycles =  ['honda', 'yamaha', 'suzuki', 'tvs']
too_old_motorcycle = "suzuki"
motorcycles.remove(too_old_motorcycle)
print(f"The oldest motorcycle in my garage was a {too_old_motorcycle.title()} and i sold it for only 2 dollars in the year 1849!!")
```

**Code Output**

```c
The oldest motorcycle in my garage was a Suzuki and i sold it for only 2 dollars in the year 1849!!
```

## **Organising Lists**

Organizing lists refers to the process of arranging list elements in a specific order, such as alphabetical or numerical. It can make it easier to access, search, and manipulate list elements based on certain criteria. There are various built-in functions and methods in Python that can be used to organize lists in different ways, depending on the requirements of the program.

### **Sorting a List Permanently**

To sort a list permanently in Python, you can use the `sort()` method. This method modifies the original list and arranges its elements in ascending order.

**Example**

```python
buddy_group = ["mercy" , "evans" , "simon" , "brian" , "consolata" , "becky" , "ronny" , "karuana"]

print("\n Here is the original buddy group ")
print(buddy_group)

print("\n Here is the buddy group list using sort method\n")
buddy_group.sort()
print(buddy_group)

print("\n Here is the  buddy group once again after applying sort method \n")
print(buddy_group)
```

**Code Output**

```python
 Here is the original buddy group 
['mercy', 'evans', 'simon', 'brian', 'consolata', 'becky', 'ronny', 'karuana']

 Here is the buddy group list using sort method

['becky', 'brian', 'consolata', 'evans', 'karuana', 'mercy', 'ronny', 'simon']

 Here is the  buddy group once again after applying sort method 

['becky', 'brian', 'consolata', 'evans', 'karuana', 'mercy', 'ronny', 'simon']
```

> NOTE: The list has now been sorted permanently

You can also sort this list in reverse alphabetical order by passing the argument `(reverse = True` to the sort method.

Note that this too changes the order of the list permanently.

**Example**

```python
buddy_group = ["mercy" , "evans" , "simon" , "brian" , "consolata" , "becky" , "ronny" , "karuana"]
buddy_group.sort(reverse=True)
print(buddy_group)
```

**Code Output**

```python
['simon', 'ronny', 'mercy', 'karuana', 'evans', 'consolata', 'brian', 'becky']
```

### **Sorting a List temporarily**

Sorting a list temporarily means creating a sorted copy of the original list, without modifying the original list. It allows you to retain the original order of elements in the list while being able to manipulate the sorted copy.

To sort a list temporarily, you can use the built-in `sorted()` function which returns a sorted list based on the original list.

**Example**

```python
buddy_group = ["mercy" , "evans" , "simon" , "brian" , "consolata" , "becky" , "ronny" , "karuana"]

print("\n Here is the original buddy group list \n")
print(buddy_group)

print("\n Here is the sorted buddy group list \n")
print(sorted(buddy_group))

print("\n Here is the original buddy group after sorted function once again \n")
print(buddy_group)
```

**Code Output**

```python
 Here is the original buddy group list
['mercy', 'evans', 'simon', 'brian', 'consolata', 'becky', 'ronny', 'karuana']

 Here is the sorted buddy group list

['becky', 'brian', 'consolata', 'evans', 'karuana', 'mercy', 'ronny', 'simon']

 Here is the original buddy group fter sorted function once again 

['mercy', 'evans', 'simon', 'brian', 'consolata', 'becky', 'ronny', 'karuana']
```

### **Printing a List in Reverse Order**

Printing a list in reverse order means displaying the elements of the list in the opposite order, starting from the last element to the first. To print a list in reverse order, you can use the `reverse()` method which modifies the original list in place or the `reversed()` function which returns a reversed iterator that can be used to display the elements of the list in reverse order without modifying the original list.

> NOTE: `reverse()` changes the order of a list permanently but you can revert to the original order by applying `reverse()` method to the same list.

**Example**

```python
buddy_group = ["mercy" , "evans" , "simon" , "brian" , "consolata" , "becky" , "ronny" , "karuana"]

print("\n Here is the originl buddy group list \n")
print(buddy_group)

print("\n Here is the reversed buddy group list \n")
buddy_group.reverse()
print(buddy_group)

print("\n Here is buddy group list   once again after reverse method \n")
print(buddy_group)
```

**Code Output**

```python
Here is the originl buddy group list 

['mercy', 'evans', 'simon', 'brian', 'consolata', 'becky', 'ronny', 'karuana']

 Here is the reversed buddy group list 

['karuana', 'ronny', 'becky', 'consolata', 'brian', 'simon', 'evans', 'mercy']

 Here is buddy group list   once again after reverse method 

['karuana', 'ronny', 'becky', 'consolata', 'brian', 'simon', 'evans', 'mercy']
```

### **Finding the Length of a List**

Finding the length of a list means determining the number of elements in the list. This can be useful in various scenarios, such as iterating through a list or checking if a list is empty. To find the length of a list, you can use the built-in `len()` function which returns the number of elements in the list.

**Example**

```python
buddy_group = ["mercy" , "evans" , "simon" , "brian" , "consolata" , "becky" , "ronny" , "karuana"]

print(len(buddy_group))
```

**Code Output**

```python
8
```

## **Working with Lists**

You can perform various operations on lists, such as appending or removing elements, slicing, sorting, and iterating through them using loops.

### **Looping Through an Entire List**

Looping through an entire involves iterating over all the elements of the list using a loop, such as a `for` loop. This allows you to perform the same action on each element in the list, or to perform a series of actions on the entire list. You can access each element in the list by using the index of the element within the loop, and the loop continues until all the elements in the list have been processed.

**Example**

Let's say we have a list containing the buddy group members and we want to print out each name in the list.

```python
software_engineers = ["mercy" , "evans" , "simon" , "brian" , "consolata" , "becky" , "ronny" , "karuana"]
for software_engineer in software_engineers:
    print(software_engineer.title())
```

**Code Explained**

* This code demonstrates how to loop through a list of software engineers' names and print each name with its first letter capitalized (i.e., title case).
    
* The first line defines a list of software engineer names, which is stored in the variable `software_engineers`.
    
* The second line starts a `for` loop that iterates through each element in the list.This line tells Python to pull a name from the List `software_engineers` and associate it with the variable `software_engineer`
    

The third line indented under the `for` loop uses the `print()` function to print each name just assigned to `software_engineer` in the list with its first letter capitalized, using the `title()` method.

When the code is executed, it will print each name on a separate line, with the first letter of each name capitalized.

**Code Output**

```python
Mercy
Evans
Simon
Brian
Consolata
Becky
Ronny
Karuana
```

> NOTE: It might be helpful to read this code as: for every software\_engineer in software\_enginners, print the software\_engineer's name.
> 
> * Looping allows computers to automate repetitive tasks
>     

### **Doing More Work with a "for" Loop**

You can do anything with each item on the list.

Let's print a message to each software engineer and tell them that they are doing great in their software engineering career.

```python
software_engineers = ["mercy" , "evans" , "simon" , "brian" , "consolata" , "becky" , "ronny" , "karuana"]
for software_engineer in software_engineers:
    print(f"Good to see you engineer {software_engineer.title()}, you are doing great in your career!")
print("The world is proud of you all, keep winning!")
```

**Code Explained**

* The first line defines a list of software engineer names, which is stored in the variable `software_engineers`.
    
* The second line starts a `for` loop that iterates through each element in the list.
    
* The third line indented under the `for` loop uses the `print()` function to print a personalized message for each software engineer. The message includes the engineer's name in title case and a general message about their career. The `title()` method is used to capitalize the first letter of each name.
    
* After the `for` loop, the code prints a final message that applies to all the engineers.
    

## **Numerical Lists**

Numerical lists are a type of list that contains a sequence of numeric values. These values can be integers, floating-point numbers, or a combination of both. Numeric lists can be used for various purposes, such as storing measurements, scores, or statistical data. They can also be manipulated using various methods such as appending, slicing, sorting, and iterating through them using loops.

### **Using the range() Function**

The `range()` function is used to generate a sequence of numbers that can be used in loops or to create lists. The `range()` function takes up to three arguments:

* `start` (optional) - the starting value of the sequence (default is 0)
    

**Example**

```python
for value in range(5) :
    print(value)
```

**Code Explained**

The first line tells Python to extract each digit in the range of 5 (starting from 0 as the default start value) and associate that value with the variable `value`. The next line prints each extracted value.

Note that we only provided the stop value of **5**.

**Code Output**

```python
0
1
2
3
4
```

* `stop` (required) - the ending value of the sequence (exclusive)
    

**Example**

```python
for value in range(1 , 5) :
    print(value)
```

**Code Explained**

* The first line uses the `for` loop to iterate through a sequence of numbers generated by the `range()` function. The `range()` function generates a sequence of numbers from 1 to 4 (i.e., it starts at 1 and ends at 4, but does not include 5).
    
* The second line indented under the `for` loop, uses the `print()` function to print each number in the sequence on a separate line. The `value` variable is used to represent the current number in the sequence.
    

**Code Output**

```python
1
2
3
4
```

> NOTE: Always adjust the end value by 1. In the above example, if we wanted to print the value 5, we could include 6 as the stop value.

```python
for value in range(1,6) :
    print(value)
```

**Code Output**

```python
1
2
3
4
5
```

* `step` (optional) - the difference between each number in the sequence (default is 1)
    

**Example**

```python
for value in range(1 , 6 , 2) :
    print(value)
```

**Code Explained**

* This code demonstrates how to use the `range()` function with a step parameter to loop through a sequence of numbers and print each number on a separate line.
    
* The `range()` function takes three arguments: the start, stop, and step. The first argument specifies the starting value of the sequence, the second argument specifies the ending value (exclusive), and the third argument specifies the step size between each value in the sequence.
    
* In this code, the `range()` function generates a sequence of numbers from 1 to 6, but only includes every second number. The step size of 2 is specified as the third argument to the `range()` function.
    
* The `for` loop is used to iterate through the sequence of numbers generated by the `range()` function.
    
* The second line indented under the `for` loop, uses the `print()` function to print each number in the sequence on a separate line. The `value` variable is used to represent the current number in the sequence.
    

**Code Output**

```python
1
3
5
```

## **Using the range() Function to make a List of Numbers**

To make a list of numbers, you can convert the results of range() directly into a list using the `list()` function.

When you wrap a `list()` function around a call to the range function, the output will be a range of numbers.

**Example**

```python
numbers = list(range(0 , 21 , 4 ))
print(numbers)
```

**Code Explained**

* The `range()` function generates a sequence of numbers starting from 0 and ending at 20 (inclusive) with a step size of 4. The resulting sequence contains the numbers 0, 4, 8, 12, 16, and 20.
    
* The `list()` function is used to convert the sequence into a list. The resulting list is assigned to the `numbers` variable.
    
* The second line uses the `print()` function to print the list of numbers. When the code is executed, it will output the list `[0, 4, 8, 12, 16, 20]` to the console.
    

> NOTE: This code is useful when you want to create a list of numbers with a specific pattern or spacing between the numbers, such as for use in mathematical calculations or for generating test data.

**Code Output**

```python
[0, 4, 8, 12, 16, 20]
```

Here is how you can put the first ten square numbers into a list.

```python
squares = []
for number in range(1 , 11) :
    square = number**2
    squares.append(square)
print(squares)
```

**Code Explained**

* The first line initializes an empty list called `squares` that will be used to store the squared numbers.
    
* The `for` loop is used to iterate through the numbers 1 to 10 generated by the `range()` function.
    
* The second line calculates the square of each number in the sequence using the exponent operator (`**`) and assigns the result to the `square` variable.
    
* The third line appends each squared number to the `squares` list using the `append()` method. The `append()` method adds the squared number to the end of the `squares` list.
    
* The last line uses the `print()` function to print the list of squared numbers to the console. When the code is executed, it will output the list `[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]` to the console.
    

> NOTE: This code is useful when you need to generate a sequence of numbers that follow a specific mathematical pattern and store the results in a list for further processing or analysis.

## **Simple Statistics with a List of Numbers**

**Example**

```python
squares = []

for value in range(1, 11) :
    squares.append(value**2)
print(min(squares))
print(max(squares))
print(sum(squares))
```

**Code Explained**

* This code demonstrates how to use a `for` loop to generate a list of squares of numbers, and then use built-in Python functions `min()`, `max()`, and `sum()` to calculate and print the minimum, maximum, and sum of the resulting list respectively.
    
* The first line initializes an empty list called `squares` that will be used to store the squared numbers.
    
* The `for` loop is used to iterate through the numbers 1 to 10 generated by the `range()` function.
    
* The second line calculates the square of each number in the sequence using the exponent operator (`**`) and appends the result to the `squares` list using the `append()` method.
    
* The third line uses the `min()` function to find the minimum value in the `squares` list and print it to the console.
    
* The fourth line uses the `max()` function to find the maximum value in the `squares` list and print it to the console.
    
* The fifth line uses the `sum()` function to calculate the sum of all the values in the `squares` list and print it to the console.
    

**Code output**

```python
1
100
385
```

## **List Comprehension**

List comprehension is a concise way to create a new list in Python by transforming or filtering an existing list. It consists of a single line of code that includes a `for` loop, an optional `if` statement, and an expression to evaluate each item in the original list.

### **List Comprehension Prototype**

```python
new_list = [expression for item in original_list if condition]
```

* The `expression` is the transformation or calculation to apply to each item in the original list.
    
* The `item` is a variable that represents each item in the original list as it is being processed.
    
* The `original_list` is the list that is being transformed.
    
* The `condition` is an optional filtering expression that specifies which items to include in the new list.
    

**Example**

```python
squares = [value**2 for value in range(1,11)]
print(squares)
```

**Code Output**

* This is an example of list comprehension where a new list `squares` is created using a one-line expression that involves a `for` loop and an expression.
    
* The code starts with defining a new list called `squares`, which will be used to store the squared values of numbers.
    
* The list comprehension statement inside the square brackets `[]` uses a `for` loop to iterate over the numbers in the range from 1 to 10 generated by the `range()` function.
    
* The expression `value**2` calculates the square of each number in the sequence using the exponent operator `**`.
    
* The result of the expression is added to the `squares` list as a new item using the list comprehension syntax.
    
* Finally, the `print()` function is used to print the `squares` list to the console.
    

**Code Output**

```python
[1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
```

> * To use this syntax, begin with a descriptive list such as "squares".
>     
> * Open a square bracket and then define the expression for the value you want to store in that new list; in the above example, the expression is \[value\*\*2\]
>     
> * Write "for" loop to generate the numbers you want to feed into the expression and close the square brackets
>     

## **Slicing a List**

Slicing a list involves selecting a subset of the elements from a list. This is done by specifying the start and end index of the subset, separated by a colon. The resulting slice will include all elements starting from the start index up to but not including the end index.

**Example**

```python
software_engineers = ["mercy" , "evans" , "simon" , "brian" , "consolata" , "becky" , "ronny" , "karuana"]
sliced_list = software_engineers[1:3]
print(sliced_list)
```

* This code has a list called `software_engineers` with eight elements. Then, a new variable called `sliced_list` is created by selecting a slice of the `software_engineers` list using the indexing notation.
    
* The slice starts from the second element `index 1` and goes up to, but does not include, the fourth element `index 3`. The resulting `sliced_list` will therefore contain the elements "evans" and "simon". Finally, the `sliced_list` is printed to the console using the `print()` function.
    

**Code Output**

```python
['evans', 'simon']
```

### **Looping Through a Slice**

Looping through a slice in Python involves iterating over a subset of elements from a list using a `for` loop. To do this, first, a slice of the list is created using the slicing notation. Then, this slice is passed to the `for` loop to iterate over its elements.

**Example**

```python
software_engineers = ["mercy" , "evans" , "simon" , "brian" , "consolata" , "becky" , "ronny" , "karuana"]
sliced_list = software_engineers[1:3]
for name in sliced_list :
    print(f"Hello engineer {name.title()}, you will be deported to uganda soon, cheers! ")
```

**Code Explained**

* The code has a list of software engineers, a slice is selected from the list of elements using indexing notation and then loops through the sliced list, printing a message for each engineer.
    
* The message uses string formatting to include the engineer's name and states that they will be deported to Uganda soon. The `title()` method is used to capitalize the first letter of each name. Finally, the message is printed to the console using the `print()` function.
    

**Code Output**

```python
Hello engineer Evans, you will be deported to uganda soon, cheers! 
Hello engineer Simon, you will be deported to uganda soon, cheers!
```

## **Copying a List**

Copying a list in Python involves creating a new list with the same elements as an existing list. There are two common methods to copy a list: using the slicing notation or using the built-in `list()` function.

### **Copying a List Using the list() function**

Copying a list using the `list()` function involves passing the original list as an argument to the function. The `list()` function creates a new list with the same elements as the original list and returns it.

**Example**

```python
software_engineers = ["mercy" , "evans" , "simon" , "brian" , "consolata" , "becky" , "ronny" , "karuana"]
copy_of_list = list(software_engineers[ : ])
print(copy_of_list)
```

**Code Explained**

In this code, a new list called `copy_of_list` is created by passing the `software_engineers` list as an argument to the `list()` function. The function creates a new list with the same elements as the original list and assigns it to the `copy_of_list` variable.

> NOTE: Any modifications made to one list will not affect the other.

**Code Output**

```python
['mercy', 'evans', 'simon', 'brian', 'consolata', 'becky', 'ronny', 'karuana']
```

### **Copying a List Using the Slicing Notation**

Copying a list using the slicing notation involves creating a new list that contains all the elements from the original list. To do this, we use the colon "**:"** operator to select all elements of the list and assign the resulting slice to a new variable. The new list will have the same elements as the original list, and any changes made to one list will not affect the other.

**Example**

```python
software_engineers = ["mercy" , "evans" , "simon" , "brian" , "consolata" , "becky" , "ronny" , "karuana"]
copy_of_list = software_engineers[ : ]
print(copy_of_list)
```

### **Code Explained**

* This code creates a list called `software_engineers` creates a new list called `copy_of_list` by using the slicing notation to select all elements from the original list, and then printing the `copy_of_list` to the console using the `print()` function.
    
* The `copy_of_list` will contain the same elements as the original `software_engineers` list. Any modifications made to one list will not affect the other.
    

**Code Output**

```python
['mercy', 'evans', 'simon', 'brian', 'consolata', 'becky', 'ronny', 'karuana']
```

## **Conditional Statements in Lists**

Conditional statements in lists allow you to selectively include or exclude elements from a list based on a condition.

### **"if" Statements**

An `if` statement is a conditional statement that allows you to specify a block of code to execute if a certain condition is true. If the condition is false, the block of code is skipped.

**Example**

```python
software_engineers = ["mercy" , "evans" , "simon" , "brian" , "consolata" , "becky" , "ronny" , "karuana"]
for software_engineer in software_engineers:
    if software_engineer == "evans":
        print(f"Hello {software_engineer.title()}, you will be deported next week!")
    elif software_engineer == "simon":
        print(f"Hello {software_engineer.title()}, you must be deported now!")
    else:
        print(f"Hello {software_engineer.title()}, keep up the good work")
        print("The world is happy!")
```

**Code Explained**

* This code has a list called `software_engineers` containing several names of software engineers.
    
* It then loops through the list using a `for` loop and checks if the current software engineer's name matches **"evans"** or **"simon"**. If it does, it prints a specific message for that engineer with a newline character at the end. If the name doesn't match either, it prints a different message to the remaining engineers in the list with a newline character at the end.
    

**Code Output**

```python
Hello Mercy, keep up the good work
The world is happy!


Hello Evans, you will be deported next week!


Hello Simon, you must be deported now!


Hello Brian, keep up the good work
The world is happy!


Hello Consolata, keep up the good work
The world is happy!


Hello Becky, keep up the good work
The world is happy!


Hello Ronny, keep up the good work
The world is happy!


Hello Karuana, keep up the good work
The world is happy!
```

## **Checking for Equality in a List**

Most conditional tests compare the current value of a variable to a specific value of interest.

The simplest conditional tests check whether the value of a variable is equal to the value of interest.

**Example**

```python
engineer = "brian"
print(engineer == "brian")
```

**Code Explained**

* This code assigns a string value "brian" to the variable `engineer`, and then checks if `engineer` is equal to the string "brian" using the `==` comparison operator.
    
* The output of the code will be `True`, since the value of `engineer` is indeed equal to the string "brian".
    

**Code Output**

```python
True
```

## **Ignoring Case when Checking for Equality**

Testing for equality is case-sensitive in Python.

Two values with different capitalizations are not considered equal in Python.

**Example**

```python
engineer = "brian"
engineer.lower()
print(engineer == "brian")
```

## **Checking for Inequality**

Checking for inequality involves using the **"!="** operator. This operator returns True if the values on either side are not equal and False if they are equal. It can be used in if statements and while loops to test conditions where the two values should not be the same.

**Example**

```python
engineer = "brian"
engineer.lower()
print(engineer != "brian")
```

**Code Explained**

* The code first defines a variable `engineer` with a string value of "brian". It then applies the `lower()` method to the string, but since the original value of `engineer` is not updated, this has no effect.
    
* Finally, it prints out `False` because the string "brian" is equal to "brian" (case-sensitive comparison), and the `!=` operator tests for inequality, which in this case is `False` because the two strings are equal.
    

**Code Output**

```python
False
```

## **Checking Multiple Conditions**

Sometimes you might want two conditions to be true to take the next course of action and other times you might just be satisfied with one condition.

### **Using "and" to Check for Multiple Conditions**

The `and` operator is used to check for multiple conditions in Python. It evaluates to `True` only if all the conditions are `True`. If any one condition is `False`, then the entire expression is `False`.

**Example**

```python
first_engineer = "brian"
second_engineer = "enos"

if (first_engineer == "brian") and (second_engineer == "abovethelaw"):
    print(f"Good day engineer {first_engineer}.title() and {second_engineer.title()}, happy coding.")
else:
    print("Engineers do cool stuff to save the planet")
```

**Code Explained**

* The code defines two variables `first_engineer` and `second_engineer`, which hold the names of two engineers.
    
* It then checks if the value of `first_engineer` is equal to the string **"brian"** and if the value of `second_engineer` is equal to the string **"abovethelaw"**.
    
* The `and` operator is used to combine the two conditions.
    
* If both conditions are `True`, the code prints a message that includes the capitalized names of both engineers. If either or both of the conditions are `False`, the code prints a generic message about engineers doing cool stuff to save the planet.
    

**Code Output**

```python
Engineers do cool stuff to save the planet
```

### **Using "or" to Check for Multiple Conditions**

The `or` operator is used to check for multiple conditions. It evaluates to `True` if at least one of the conditions is `True`. If all the conditions are `False`, then the entire expression is `False`.

**Example**

```python
first_engineer = input("Please input your name: ")
second_engineer = input("Please input your name: ")

if (first_engineer == "brian") or (second_engineer == "abovethelaw"):
    print(f"Good day engineer {first_engineer}.title() and {second_engineer.title()}, happy coding.")
else:
    print("Engineers do cool stuff to save the planet")
```

**Code Explained**

* The code prompts the user to input two engineer names and stores them in the variables `first_engineer` and `second_engineer`.
    
* It then uses the `or` operator to check if either the value of `first_engineer` is equal to the string "brian" or the value of `second_engineer` is equal to the string **"abovethelaw"**.
    
* If either or both of the conditions are `True`, the code prints a message that includes the capitalized names of both engineers.
    
* If both conditions are `False`, the code prints a generic message about engineers doing cool stuff to save the planet.
    

## **Checking whether a Value is in a List**

You can check whether a value is in a list using the `in` operator. This operator returns a Boolean value (`True` or `False`) depending on whether the value is found in the list.

**Example**

```python
software_engineers = []

while True:
    engineer_name = input("Please input your name (enter 'done' to exit): ")
    engineer_name = engineer_name.lower()
    
    if engineer_name == "done" or engineer_name == "":
        break  
    else :
        software_engineers.append(engineer_name)
if "brian" in software_engineers :
    print(f"Hello Brian, good to see you!")
```

**Code Explained**

* This code prompts the user to input their name, converts the name to lowercase, and adds it to a list called `software_engineers` until the user enters "done" or a null character to exit the loop.
    
* After the loop has ended, the code checks whether the string `"brian"` is in the `software_engineers` list using the `in` operator. If the name `"brian"` is found in the list, the code prints a message that says "Hello Brian, good to see you!".
    

## **Checking whether a Value is Not in a List**

You can check whether a value is not in a list using the `not in` operator. This operator returns a Boolean value (`True` or `False`) depending on whether the value is not found in the list.

**Example**

```python
software_engineers = []

while True:
    engineer_name = input("Please input your name (enter 'done' to exit): ")
    engineer_name = engineer_name.lower()
    
    if engineer_name == "done" or engineer_name == "":
        break  
    else :
        software_engineers.append(engineer_name)
if "brian" not in software_engineers :
    print(f"brian is not in the list of software engineers!")
print(software_engineers)
```

**Code Explained**

* This code prompts the user to input their name, converts the name to lowercase, and adds it to a list called `software_engineers` until the user enters "done" or a null character to exit the loop.
    
* After the loop has ended, the code checks whether the string `"brian"` is not in the `software_engineers` list using the `not in` operator. If the name `"brian"` is not found in the list, the code prints a message that says "brian is not in the list of software engineers!".
    
* Finally, the code prints the entire `software_engineers` list, which contains all the names that were entered by the user during the loop.
    

## **Checking that a List is Not Empty**

Checking that a list is not empty is important to ensure that you can perform operations on it without encountering errors. You can use the boolean value of a list to check if it is empty or not. An empty list evaluates to False, while a non-empty list evaluates to True

**Example**

```python
software_engineers = []

while True:
    engineer_name = input("Please input your name (enter 'done' to exit): ")
    engineer_name = engineer_name.lower()
    
    if engineer_name == "done" or engineer_name == "":
        break  
    else:
        software_engineers.append(engineer_name)

if software_engineers:
    print(f"The list of software engineers is not empty: {software_engineers}")
else:
    print("The list of software engineers is empty.")
```

**Code Explained**

This code prompts the user to enter names and adds them to a list named `software_engineers`. It then checks if the list is empty using the `if` statement with the list name, and prints a message indicating whether it's empty or not. If it's not empty, the message will show the contents of the list using an f-string. If it is empty, the message will simply say that the list is empty.

## **Using Multiple Lists**

Multiple lists can be used to store related data that can be processed together. For example, if you have a list of names and another list of ages, you can store them separately but still link the data by the index. You can perform operations such as iterating over multiple lists simultaneously, slicing and concatenating lists, and sorting multiple lists based on a shared criterion. Using multiple lists allows for more organized and efficient data management in Python programs.

**Example**

```python
software_engineers = []
software_languages = []

while True:
    engineer_name = input("Please input your name (enter 'done' to exit): ")
    engineer_name = engineer_name.lower()
    
    if engineer_name == "done" or engineer_name == "":
        break  
    else:
        software_engineers.append(engineer_name)
        
    language_name = input("Please input a programming language: ")
    language_name = language_name.lower()
    
    if language_name == "done" or language_name == "":
        break  
    else:
        software_languages.append(language_name)

if software_engineers and software_languages:
    print(f"The list of software engineers is not empty: {software_engineers}")
    print(f"The list of software languages is not empty: {software_languages}")
else:
    print("The lists of software engineers and/or languages are empty.")
```

**Code Explained**

* This code prompts the user to enter their name and a programming language they are familiar with, until the user enters 'done' or an empty string. The code then creates two separate lists: `software_engineers` and `software_languages`, containing the names and programming languages respectively. Finally, the code checks if both lists are not empty, and if they are not, it prints out the list of software engineers and software languages. If either or both lists are empty, the code prints a message indicating that the lists are empty.
    

## **Loops in Lists**

### **"for" Loops**

A for loop is a type of loop in programming that allows you to iterate over a collection of items and perform a set of instructions for each item in the collection. When working with lists in programming, you can use for loops to iterate over each item in a list and perform a set of instructions for each item.

**Example**

```python
software_engineers = []
software_languages = []

for i in range(1,3):
    engineer_name = input("Please input your name (enter 'done' to exit): ")
    engineer_name = engineer_name.lower()

    language_name = input("Please input your favourite programming language: ")
    language_name = language_name.lower()
    
    if engineer_name == "done" or engineer_name == "":
        break  
    else:
        software_engineers.append(engineer_name)
    
    if language_name == "done" or language_name == "":
        break  
    else:
        software_languages.append(language_name)

if software_engineers and software_languages:
    print(f"The list of software engineers is not empty: {software_engineers}")
    print(f"The list of software languages is not empty: {software_languages}")
else:
    print("The lists of software engineers and/or languages are empty.")
```

**Code Explained**

* This code is an example of how to use a for loop to collect input from users and store it in lists. The program first creates two empty lists called `software_engineers` and `software_languages`.
    
* The for loop then runs twice using the `range()` function with the parameters `1` and `3`, meaning it will loop twice, incrementing the `i` variable from 1 to 2. This is done to collect input from two software engineers.
    
* Inside the for loop, the program prompts the user to input their name and favorite programming language using the `input()` function. It then converts the user's input to lowercase letters using the `lower()` method.
    
* The program checks if the user entered "done" or left the input field blank. If so, the loop is broken out of using the `break` statement. Otherwise, the program adds the user's name to the `software_engineers` list using the `append()` method, and adds their favorite programming language to the `software_languages` list using the `append()` method as well.
    
* After the for loop completes, the program checks if both lists are not empty using an `if` statement. If both lists are not empty, the program prints a message stating that the lists of software engineers and languages are not empty and displays the contents of the two lists using formatted string literals. Otherwise, if one or both lists are empty, the program prints a message stating that the lists are empty.
    

# **Tuples**

A tuple is an ordered collection of elements, similar to a list. However, unlike lists, tuples are immutable, meaning that once a tuple is created, its elements cannot be changed.

Tuples are defined using parentheses `()` and can contain elements of any data type, including other tuples.

Once defined, you can access the individual elements like you would with a normal list by indexing.

### **Tuple Prototype**

```python
tuple_prototype = ("string tuple" , integer(eg 5), ....etc)
```

**Example**

```python
my_tuple = ("oranges" , 1.5, "age")
my_dimension_tuple = (2230,5, 38,100)

print(my_dimension_tuple)
print(my_tuple)
```

**Code Output**

```python
(2230, 5, 38, 100)
('oranges', 1.5, 'age')
```

## **Looping through all Values in a Tuple**

You can loop over all the values in a tuple using a for loop just as you would with a list.

**Example**

```python
my_dimension_tuple = (2230,5, 38,100)

for dimension in my_dimension_tuple:
    print(f"{dimension} is a dimension in the tuple")
```

**Code Explained**

* This code defines a tuple called "my\_dimension\_tuple" with four elements. Then, using a for loop and iterating through the elements of the tuple, each dimension is printed out as a string with a message.
    

**Code Output**

```python
2230 is a dimension in the tuple
5 is a dimension in the tuple
38 is a dimension in the tuple
100 is a dimension in the tuple
```

## **Slicing a Tuple**

Slicing a tuple means creating a new tuple that contains a specified subset of elements from the original tuple. You can slice a tuple by specifying a range of indices to extract, using the brackets "\[:\]" operator. The syntax for slicing a tuple is `tuple[start:end:step]`, where `start` is the index of the first element to include in the slice, `end` is the index of the first element to exclude from the slice, and `step` is the size of the step between elements in the slice (default is 1). The resulting slice is a new tuple that contains the specified range of elements from the original tuple.

**Example**

```python
dimensions = (100, 150, 200, 250, 300)
sliced_dimension = dimensions[1:3]
print(sliced_dimension)
```

**Code Explained**

* This code defines a tuple called "dimensions" with five elements. A new tuple called "sliced\_dimension" is created using a slice of the "dimensions" tuple, starting at index 1 and ending before index 3.
    
* The "sliced\_dimension" tuple is then printed, which contains the second and third elements of the "dimensions" tuple.
    

**Code Output**

```python
(150, 200)
```

## **Writing Over a Tuple**

Tuples are immutable, meaning their values cannot be changed after they are created. However, it is possible to overwrite a tuple by creating a new tuple with the same variable name. This can be done by assigning a new tuple with different values to the variable, effectively replacing the original tuple with the new one.

**Example**

```python
my_dimension_tuple = (2230,5, 38,100)
print("These are the dimensions before modification: ")
print(my_dimension_tuple)

print("These are the dimensions after modification: ")
my_dimension_tuple = (10,120,134)
print(my_dimension_tuple)
```

**Code Explained**

* This code defines a tuple called "my\_dimension\_tuple" with four elements. It then prints out a message followed by the values of the tuple.
    
* After that, a new tuple with different values is assigned to the same variable, effectively overwriting the original tuple. The new tuple is printed out with another message.
    

**Code Output**

```python
These are the dimensions before modification: 
(2230, 5, 38, 100)
These are the dimensions after modification: 
(10, 120, 134)
```

# **Methods in Python**

A method is a function t associated with an object. Methods are called on objects and they perform operations on the data contained within the object. Methods can modify the object and return a result, or they can simply return a result without modifying the object.

## **Commonly Used Methods in Python**

* `print()`: Outputs text to the console.
    

```c
print("I am a Software Engineer")
```

Output

```c
I am a Software Engineer
```

* `len()`: Returns the length of a string, list, or other iterable.
    

```c
full_name = "Brian Enos Otieno"
print("The length of string in variabllen full_name is :" , len(full_name))
```

Output

```c
The length of string in variabllen full_name is : 17
```

* `type()`: Returns the data type of a variable.
    

```c
full_name = "Brian Enos Otieno"
print("The data type of the above variable is :" , type(full_name))
```

Output

```c
The data type of the above variable is : <class 'str'>
```

* `str()`: Converts an object to a string.
    

```c
my_age = 23
age_converted_to_string = str(my_age)
print(age_converted_to_string)
print("My age has now been converted to a string!: type(age_converted_to_string))
```

Output

```c
23
My age has now been converted to a string!: <class 'str'>
```

* `int()`: Converts a string or float to an integer.
    

```c
my_age_string = "23"
age_string_converted_to_integer = int(my_age_string)
print(age_string_converted_to_integer)
print("My age string has now been conveted to an integer!:", type(age_string_converted_to_integer))
```

Output

```c
23
My age string has now been conveted to an integer!: <class 'int'>
```

> NOTE: You cannot convert a string containing letters and spaces to an integer using the `int()` function. The `int()` function can only convert strings that contain numbers.

* `float()`: Converts a string or integer to a float.
    

```c
my_age_string = "23"
age_string_converted_to_float = float(my_age_string)
print(age_string_converted_to_float)
print("My age string has now been conveted to a float !:", type(age_string_converted_to_float))
```

Output

```c
23.0
My age string has now been conveted to a float !: <class 'float'>
```

* `list()`: Converts an iterable to a list.
    

```c
full_name = "Brian Enos Otieno"
my_list_from_fullname = list(full_name)
print(my_list_from_fullname)
print("Full name has now been converted to a list! : " , type(my_list_from_fullname))
```

Output

```c
['B', 'r', 'i', 'a', 'n', ' ', 'E', 'n', 'o', 's', ' ', 'O', 't', 'i', 'e', 'n', 'o']
Full name has now been converted to a list! :  <class 'list'>
```

* `tuple()`: Converts an iterable to a tuple.
    

```c
full_name = "Brian Enos Otieno"
my_tuple_from_fullname = tuple(full_name)

print(my_tuple_from_fullname)
print("Full name has now been converted to a tuple! : " , type(my_tuple_from_fullname))
```

Output

```c
('B', 'r', 'i', 'a', 'n', ' ', 'E', 'n', 'o', 's', ' ', 'O', 't', 'i', 'e', 'n', 'o')
Full name has now been converted to a tuple! :  <class 'tuple'>
```

* `dict()`: Creates a new dictionary or converts an iterable to a dictionary.
    

```c
full_name = "Brian Enos Otieno"
my_age = 23
first_name, middle_name, last_name = full_name.split()

my_dictionary_from_fullname = {"first_name": first_name, "middle_name": middle_name, "last_name": last_name, "age": my_age}

print(my_dictionary_from_fullname)
print("Full name has now been converted to a Dictionary! : ", type(my_dictionary_from_fullname))
```

Output

```c
{'first_name': 'Brian', 'middle_name': 'Enos', 'last_name': 'Otieno', 'age': 23}
Full name has now been converted to a Dictionary! :  <class 'dict'>
```

* `set()`: Creates a new set or converts an iterable to a set.
    

```c
full_name = "Brian Enos Otieno"
my_set_from_fullname = set(full_name)

print(my_set_from_fullname)
print("Full name has now been converted to a Set! : ", type(my_set_from_fullname))
```

output

```c
{'a', 't', 'n', 'B', 'i', 'o', 'E', 's', 'r', 'e', ' ', 'O'}
Full name has now been converted to a Set! :  <class 'set'>
```

* `range()`: Returns a sequence of numbers.
    

```c
my_range = range(5)
print(list(my_range))
```

Output

```c
[0, 1, 2, 3, 4]
```

* `zip()`: Combines multiple iterables into a single iterable of tuples.
    

```c
my_number_list = [1, 2, 3, 4, 5]
my_first_name = ['b', 'r' , 'i' , 'a' , 'n']
my_zip = zip(my_number_list, my_first_name)
print(list(my_zip))
```

Output

```c
[(1, 'b'), (2, 'r'), (3, 'i'), (4, 'a'), (5, 'n')]
```

* `sorted()`: Sorts a list or other iterable.
    

```c
my_number_list = [5, 2, 1, 4, 3]
my_first_name = ['b', 'r' , 'i' , 'a' , 'n']

sorted_number_list = sorted(my_number_list)
sorted_first_name = sorted(my_first_name)

print(sorted_number_list)
print(sorted_first_name)
```

Output

```c
[1, 2, 3, 4, 5]
['a', 'b', 'i', 'n', 'r']
```

* `sum()`: Returns the sum of elements in a list or other iterable.
    

```c
my_number_list = [5, 3, 2, 4, 1]
sum_of_number_list = sum(my_number_list)
print(sum_of_number_list)
```

Output

```c
15
```

* `max()`: Returns the maximum value in a list or other iterable.
    

```c
my_number_list = [5, 3, 2, 4, 1, 9, 10]


maximum_number_in_number_list = max(my_number_list)

print(maximum_number_in_number_list)
```

Output

```c
10
```

* `min()`: Returns the minimum value in a list or other iterable.
    

```c
my_number_list = [5, 3, 2, 4, 1, 9, 10]


mminimum_number_in_number_list = min(my_number_list)

print(miniimum_number_in_number_list)
```

Output

```c
1
```

* `abs()`: Returns the absolute value of a number.
    

```c
my_number = -10
absolute_number = abs(my_number)
print(absolute_number)
```

Output

```c
10
```

* `round()`: Rounds a floating-point number to a specified number of decimal places.
    

```c
number = 3.14159
rounded_number = round(number, 2)
print(rounded_number)
```

Output

```c
3.14
```

* `replace()`: Replaces a substring in a string with another substring.
    

```c
full_name_string = "Brian , Enos , Otieno"
new_string = full_name_string.replace("Otieno" , "AboveTheLaw")
print(new_string)
```

Output

```c
Brian , Enos , AboveTheLaw
```

* `strip()`: Removes leading and trailing whitespace from a string.
    

```c
full_name_string = "Brian , Enos , Otieno"
new_string = full_name_string.strip()
print(new_string)
```

Output

```c
Brian , Enos , Otieno
```

* `split()`: Splits a string into a list of substrings based on a delimiter.
    

```c
full_name_string = "Brian  Enos Otieno"
my_list = full_name_string.split(",")
print(my_list)
```

Output

```c
['Brian  Enos Otieno']
```

* `join()`: Joins a list of strings into a single string using a delimiter.
    

```c
my_list = ["Brian", "Enos" , "Otieno"]
my_string = (", ").join(my_list)
print(my_string)
```

Output

```c
Brian, Enos, Otieno
```

* `capitalize()`: Capitalizes the first letter of a string.
    

```c
full_name_string = "Brian Enos Otieno"
new_string = full_name_string.capitalize()
print(new_string)
```

Output

```c
Brian enos otieno
```

* `title()`: Capitalizes the first letter of each word in a string.
    

```c
full_name_string = "brian enos otieno"
new_string = full_name_string.title()
print(new_string)
```

Output

```c
Brian Enos Otieno
```

* `lower()`: Converts a string to lowercase.
    

```c
full_name_string = "BRIAN ENOS OTIENO"
new_string = full_name_string.lower()
print(new_string)
```

Output

```c
brian enos otieno
```

* `upper()`: Converts a string to uppercase.
    

```c
full_name_string = "brian enos otieno"
new_string = full_name_string.upper()
print(new_string)
```

Output

```c
BRIAN ENOS OTIENO
```

* `startswith()`: Returns True if a string starts with a specified substring.
    

```c
full_name_string = "Brian Enos Otieno"
result = full_name_string.startswith("Brian")
print(result)
```

Output

```c
True
```

* `endswith()`: Returns True if a string ends with a specified substring.
    

```c
full_name_string = "Brian Enos Otieno"
result = full_name_string.endswith("Otieno")
print(result)
```

Output

```c
True
```

* `count()`: Returns the number of occurrences of a substring in a string.
    

```c
full_name_string = "Brian Enos Otieno"
count = full_name_string.count("Otieno")
print(count)
```

Output

```c
1
```

* `find()`: Returns the index of the first occurrence of a substring in a string, or -1 if the substring is not found.
    

```c
full_name_string = "Brian, Enos, Otieno"
index_of_substring = full_name_string.find("Otieno")
print(index_of_substring)
```

Output

```c
13
```

* `isalpha()`: Returns True if a string contains only letters.
    

```c
full_name_string = "Brian, Enos, Otieno"
result = full_name_string.isalpha()
print(result)
```

Output

```c
False
```

* `isdigit()`: Returns True if a string contains only digits.
    

```c
full_name_string = "Brian, Enos, Otieno"
result = full_name_string.isdigit()
print(result)
```

Output

```c
False
```

* `isalnum()`: Returns True if a string contains only letters and digits.
    

```c
full_name_string = "Brian, Enos, Otieno"
result = full_name_string.isalnum()
print(result)
```

Output

```c
False
```

* `islower()`: Returns True if a string contains only lowercase letters.
    

```c
full_name_string = "Brian, Enos, Otieno"
result = full_name_string.islower()
print(result)
```

Output

```c
False
```

* `isupper()`: Returns True if a string contains only uppercase letters.
    

```c
full_name_string = "Brian, Enos, Otieno"
result = full_name_string.isupper()
print(result)
```

Output

```c
False
```

* `isspace()`: Returns True if a string contains only whitespace characters.
    

```c
full_name_string = "Brian, Enos, Otieno"
result = full_name_string.isspace()
print(result)

my_string = "  "
result = my_string.isspace()
print(result)
```

Output

```c
False
```




## **Note**

* I'm always exploring new ways to optimize code and improve system performance, and I'm happy to share my knowledge with others.
* I hope that my examples and projects will be useful to those looking to learn more about System Engineering DevOps or those looking to improve their skills in this field.

* Please feel free to contribute to this repository or reach out to me with any questions or suggestions.

  
  
## **Thank you for visiting this repository, see you around!** :smiling_face_with_three_hearts:



# **Connect with me on:** 

[Hash Node](https://brianenosotieno.hashnode.dev)
                        
[Twitter](https://twitter.com/brian_tatling) 
                        
[Linked In](https://www.linkedin.com/in/brian-enos/)

## **Famous Programming Quote**
 ***"When done well, software is invisible," Bjarne Stroustrup*** :muscle: :muscle: :muscle:
## **Happy Coding Engineers!** :computer: :computer: :computer:
<img align="left" alt="Coding" width="400" src= "https://camo.githubusercontent.com/e20822b4282c07ffd010cd05f855a6561d3b62358ca9e607e4901288dd748fcb/68747470733a2f2f63646e2e6472696262626c652e636f6d2f75736572732f323133313939332f73637265656e73686f74732f343934383733362f74686f75676874776f726b732d6769665f6472696262626c652e676966">
