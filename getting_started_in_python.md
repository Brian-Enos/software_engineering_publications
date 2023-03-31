# **Introduction**

Python is a high-level, interpreted programming language that was created by Guido van Rossum and released in 1991. It is designed to be easy to read and write, with a focus on code readability, and has become one of the most popular programming languages in use today.

Interpreted programming languages use an interpreter for their translation, unlike compiled languages such as C which use compilers for their translation. An interpreter reads the source code of a program line by line and executes each line as it is read. Python is an interpreted language, which means that it uses an interpreter to execute code.

Python is an object-oriented language, which means it allows you to create reusable blocks of code that can be used across different parts of your program. It also supports functional programming, which allows you to write code that is more modular and easier to test.

Python has an extensive standard library, which provides a wide range of pre-built modules and functions that can be used for tasks such as file I/O, web programming, and regular expressions. In addition, there are many third-party libraries available for Python, which can extend its capabilities even further.

Python is commonly used in fields such as data analysis, scientific computing, web development, and artificial intelligence. It is also popular among beginners due to its ease of use and gentle learning curve.

**Why Translators?**

We use translators to convert code written in a high-level programming language into a low-level language that can be executed by the computer's CPU. This process is known as "interpretation,"

Both interpreters and compilers have their advantages and disadvantages. Interpreters are generally easier to use and debug, while compilers can generate faster and more efficient code. However, they require more setup and configuration.

**So, Why should one learn Python?**

There are many reasons why someone might want to learn Python.

Here are a few:

Versatility: Python is a versatile programming language that can be used for a wide range of tasks, from web development to data analysis to machine learning.

Easy to learn: Python is relatively easy to learn, even for beginners. It has a simple syntax that makes it easy to read and understand.

Huge community: Python has a large and supportive community of developers who are constantly creating new libraries and tools to make programming in Python easier and more efficient.

Career opportunities: Python is widely used in a variety of industries, from tech to finance to healthcare. Learning Python can open up a wide range of career opportunities.

Automation: Python is great for automation tasks, such as web scraping or automating repetitive tasks.



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
    

**Variables, Data Types and Operators**

**Variables**

Variables are used to store data values that can be used throughout a program. They are essentially labels or names that refer to specific values in memory and can be assigned and reassigned different values as needed.

**Data Types**

Data types are the classification of data items based on the type of value they hold. Python has built-in support for various data types, including numeric, string, boolean, and sequence types.

**Commonly used Data Types in Python**

1. Numeric types:
    
    * Integer: `x = 10`
        
    * Floating-point numbers: `x = 3.14159`
        
    * Complex numbers: `x = 2 + 3j`
        
2. Boolean type:
    
    * Boolean: `x = True`
        
3. Sequence types:
    
    * Strings: `x = "Hello World"`
        
    * Lists: `x = [1, 2, 3, 4]`
        
    * Tuples: `x = (1, "apple", 3.14)`
        
    * Byte arrays: `x = bytearray(b'Hello')`
        
    * Byte strings: `x = b'Hello'`
        
    * Range objects: `x = range(5)`
        
4. Mapping type:
    
    * Dictionary: `x = {"name": "Brian", "age": 23, "city": "Nairobi"}`
        
5. Set types:
    
    * Set: `x = {1, 2, 3}`
        
    * Frozen set: `x = frozenset({1, 2, 3})`
        

> NOTE: We will use all these as we progress further in this series. Hang in tight!

**Operators**

Operators in Python are symbols or special keywords used to perform operations on values or variables. Python supports a wide range of operators, including arithmetic, comparison, logical, assignment, and bitwise operators

**Commonly used Operators in Python**

1. Arithmetic operators:
    
    * Addition: `2 + 3` returns `5`
        
    * Subtraction: `5 - 2` returns `3`
        
    * Multiplication: `2 * 3` returns `6`
        
    * Division: `6 / 2` returns `3`
        
    * Modulo: `5 % 2` returns `1`
        
    * Exponentiation: `2 ** 3` returns `8`
        
2. Comparison operators:
    
    * Equal to: `2 == 3` returns `False`
        
    * Not equal to: `2 != 3` returns `True`
        
    * Greater than: `5 > 2` returns `True`
        
    * Less than: `2 < 5` returns `True`
        
    * Greater than or equal to: `5 >= 5` returns `True`
        
    * Less than or equal to: `2 <= 5` returns `True`
        
3. Logical operators:
    
    * And: `True and False` returns `False`
        
    * Or: `True or False` returns `True`
        
    * Not: `not True` returns `False`
        
4. Assignment operators:
    
    * Assign: `x = 5`
        
    * Add and assign: `x += 2` is equivalent to `x = x + 2`
        
    * Subtract and assign: `x -= 2` is equivalent to `x = x - 2`
        
    * Multiply and assign: `x *= 2` is equivalent to `x = x * 2`
        
    * Divide and assign: `x /= 2` is equivalent to `x = x / 2`
        
    * Modulo and assign: `x %= 2` is equivalent to `x = x % 2`
        
    * Exponentiation and assign: `x **= 2` is equivalent to `x = x ** 2`
        
    * Floor division and assign: `x //= 2` is equivalent to `x = x // 2`
        
5. Bitwise operators:
    
    * Bitwise AND: `0b1010 & 0b1100` returns `0b1000`
        
    * Bitwise OR: `0b1010 | 0b1100` returns `0b1110`
        
    * Bitwise XOR: `0b1010 ^ 0b1100` returns `0b0110`
        
    * Bitwise NOT: `~0b1010` returns `-0b1011`
        
    * Left shift: `0b1010 << 2` returns `0b101000`
        
    * Right shift: `0b1010 >> 2` returns `0b10`
        

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



## **Kind Notice**

* I'm always exploring new ways to optimize code and improve system performance, and I'm happy to share my knowledge with others.
* I hope that my examples and projects will be useful to those looking to learn more about low-level programming or those looking to improve their skills in this field.

* Please feel free to contribute to this repository or reach out to me with any questions or suggestions.

  
  
### **Thank you for  visiting my repository and I hope you find it helpful in your own software engineering projects, see you around!** :smiling_face_with_three_hearts:



# **Connect with me on:** 

[Hash Node](https://brianenosotieno.hashnode.dev)
                        
[Twitter](https://twitter.com/brian_tatling) 
                        
[Linked In](https://www.linkedin.com/in/brian-enos/)


## **A Famous Programming Quote**
***"When done well, software is invisible," Bjarne Stroustrup*** :muscle: :muscle: :muscle:
## **Happy Coding Engineers!** :computer: :computer: :computer:
<img align ="left" alt="Coding" width="400" src= "https://camo.githubusercontent.com/e20822b4282c07ffd010cd05f855a6561d3b62358ca9e607e4901288dd748fcb/68747470733a2f2f63646e2e6472696262626c652e636f6d2f75736572732f323133313939332f73637265656e73686f74732f343934383733362f74686f75676874776f726b732d6769665f6472696262626c652e676966">
