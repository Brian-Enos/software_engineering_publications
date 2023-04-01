# **Functions and Arrays**
## **Introduction**

Functions are self-contained blocks of code that perform a specific task. They are a fundamental building block of software development. Functions are used to break down complex programs into smaller, more manageable pieces of code that can be reused throughout the program or in other programs.

In the [**previous examples**](https://brianenosotieno.hashnode.dev/program-flow-control), our programs have constituted a single function called "main" i.e,

```c
......
int main(void) {
/* 
*Body of the main function here
*/
 }
.......
```

However, we have made use of predefined functions such as printf, scanf, strcpy, strcat e.t.c

**For Example**

```c
.......
printf(" %d \n \n %d \n", a, b);
........
```

The above **printf** function will print **"a"** on a new line, skip a line and print **"b"** on the line after.

## **Main Parts of a Function**

* **Return type**
    
    The return type of a function indicates the data type of the value that the function will return. It can be `int`, `float`, `double`, `char`, `void`, or any other data type.
    
* **Function name**
    
    The function name is a unique identifier for the function, which is used to call the function from other parts of the program.
    
* **Parameters**
    
    Parameters are optional inputs to the function. They are declared inside parentheses after the function name, separated by commas. Parameters can be of any data type and allow the function to accept inputs that can be used within the function.
    
* **Function body**
    
    The function body contains the statements that make up the function's logic. The body is enclosed within curly braces `{}` and can contain one or more statements.
    
* **Return statement**
    
    The return statement is used to return a value from the function to the caller. The return statement is followed by an expression that evaluates to the value that the function will return.
    

## **General Construct**

```c
return_type function_name(parameter_list)
{
    /* 
    *Body of the function here 
    */
}
```

* `return_type`
    
    Is the data type of the value returned by the function (e.g., `int`, `float`, `double`, `void`, etc.).
    
* `function_name`
    
    Is the name of the function.
    
* `parameter_list`
    
    Is a list of input parameters that the function accepts (optional).
    
* The `function body`
    
    Contains the statements that are executed when the function is called.
    

## **Calling A Function**

Functions are called by their name, followed by parentheses that may contain the arguments passed to the function.

## **Example 1**

A function that prints a specified number of newlines to the console.

```c
#include <stdio.h>

void skiplines(int number);

int main() {
    /*
    *Body of main function here
    */
printf("My name is Brian Enos Otieno\n");
skiplines(3);
printf("I am a software Engineer \n");
skiplines(2);
printf("Programming is co cool!, join me and #DoHardThings\n");
return (0);
}
void skiplines(int number) {
    /*
    *Body of skiplines function here
    */
    for (int h = 1; h <= number ; h++);
        printf("\n");
}
```

**Code Explained**

* This code defines a function named `skiplines` that takes an integer parameter `number` and prints a specified number of newlines to the console. The `skiplines` function is declared at the top of the code using a function prototype `void skiplines(int number);` so that it can be called from the `main` function.
    
* The `main` function calls the `skiplines` function twice, first with the argument `3` and then with the argument `2`, to print three and two newlines, respectively, before and after printing some text to the console using the `printf` function.
    
* When the program is executed, the `printf` function is called to print the text "My name is Brian Enos Otieno" to the console. Then, the `skiplines` function is called with the argument `3`, which prints three newlines to the console. Next, the `printf` function is called again to print the text "I am a software Engineer" to the console, followed by a call to `skiplines` with the argument `2`, which prints two newlines to the console. Finally, the `printf` function is called once more to print the text "Programming is co cool!, join me and #DoHardThings" to the console.
    
* The `skiplines` function uses a `for` loop to print a newline character (`\n`) a specified number of times. In this case, the loop starts at 1 and continues as long as the loop variable `h` is less than or equal to the `number` parameter. The loop body contains a single statement, which prints a newline character to the console using the `printf` function. Note that there is a semicolon at the end of the `for` statement, which makes the loop run for zero iterations, resulting in the desired number of newlines being printed to the console.
    

**Code Output**

```c
My name is Brian Enos Otieno

I am a software Engineer
Programming is co cool!, join me and #DoHardThings
```

## **Example 2**

A function that returns the product of two numbers.

```c
#include <stdio.h>

int multiply_two_numbers(int a, int b);

int main()
{
    /*
    * Body of main Function
    */
    int result = multiply_two_numbers(5, 10);
    printf("%d\n", result);
    return 0;
}

int multiply_two_numbers(int a, int b)
{
    /*
    *A function that multilplies two numbers
    */
    return (a * b);
}
```

**Code Explained**

* The function named `multiply_two_numbers` that takes two integer parameters `a` and `b` and returns their product. The `multiply_two_numbers` function is declared at the top of the code using a function prototype `int multiply_two_numbers(int a, int b);` so that it can be called from the `main` function.
    
* The `main` function calls the `multiply_two_numbers` function with the arguments `5` and `10`, and assigns the result to the variable `result`. The `result` is then printed to the console using the `printf` function with the format specifier `%d`, which is used to print integer values.
    
* When the program is executed, the `multiply_two_numbers` function is called with the arguments `5` and `10`, and it returns the product of the two numbers, which is `50`. This value is then assigned to the variable `result`, which is printed to the console as `50`. Finally, the `main` function returns `0`, which indicates that the program has executed successfully
    

**Code Output**

```c
50
```

## **Example 3**

A function that returns the sum of two integers.

```c
#include <stdio.h>

int sum(int a, int b);

int main() {  

    int x , y, z ;
    printf("Enter Two Integer Numbers and press 'Enter': \n");
    scanf("%d %d", &x , & y);
    z = sum(x , y);
    printf("The sum of %d and %d is %d\n", x, y, z);
    return 0;
}

int sum(int a, int b) {
    int result = a + b;
    return result;
}
```

**Code Explained**

* This simple program prompts the user to enter two integer numbers, reads them from the standard input using the `scanf` function, computes their sum using the `sum` function and then prints the result to the standard output using the `printf` function.
    
* The `sum` function is defined above the `main` function and takes two integer arguments `a` and `b`. It computes their sum using the `+` operator and assigns the result to a local variable `result`, which is then returned to the caller using the `return` statement.
    
* In the `main` function, three integer variables `x`, `y`, and `z` are declared. The `printf` function is used to print a message prompting the user to enter two integer numbers, and the `scanf` function is used to read two integer values separated by whitespace from the standard input and store them in `x` and `y`, respectively. The `sum` function is then called with `x` and `y` as arguments, and the result is stored in `z`. Finally, the `printf` function is used to print a message displaying the values of `x`, `y`, and `z`, which correspond to the two input values and their sum, respectively.
    

**Code Output**

If the user enters the numbers `25` and `10` at the prompt, the output of the program will be:

```c
Enter Two Integer Numbers and press 'Enter':
25 10
The sum of 25 and 10 is 35
```

## **Example 4**

A function that checks if each character is an uppercase or lowercase letter, and prints out the position of the letter in the alphabet

```c
#include <stdio.h>

int isUpperCase(char ch);
int position(char ch);
int isLowerCase(char ch);

int main() {
 char c;
 printf("Type some letters and non-letters and press 'Enter': \n");
 while ((c = getchar()) != '\n')
 printf("%c %2d\n", c, position(c));
} /*
    *End of Main
    */

int isUpperCase(char ch) {
 return ch >= 'A' && ch <= 'Z';
} /*
   *end of isUpperCase
   */

int isLowerCase(char ch) {
 return ch >= 'a' && ch <= 'z';
} /*
   *end isLowerCase
   */


int position(char ch) {
 if (isUpperCase(ch)) return ch - 'A' + 1;
 if (isLowerCase(ch)) return ch - 'a' + 1;
 return 0;
} /*
   *end position
   */
```

**Code Explained**

* This program reads input from the user, checks if each character is an uppercase or lowercase letter, and prints out the position of the letter in the alphabet (i.e., A=1, B=2, etc.) if it is a letter.
    
* The program first includes the standard input/output header file `stdio.h` and declares three functions: `isUpperCase`, `position`, and `isLowerCase`.
    
* In the `main()` function, the program declares a character variable `c` and prompts the user to type in some input. It then enters a while loop that reads each character entered by the user using `getchar()`.
    
* For each character read in, the program calls the `position()` function to check if it is an uppercase or lowercase letter. If it is, the position of the letter in the alphabet is printed to the console using `printf()`.
    
* The `isUpperCase()` and `isLowerCase()` functions are helper functions that return `1` if the input character is an uppercase or lowercase letter, respectively. They are used by the `position()` function to determine if a given character is a letter or not.
    
* The `position()` function takes a character input `ch` and first checks if it is an uppercase letter by calling `isUpperCase()`. If so, it returns the position of the letter in the alphabet by subtracting the ASCII value of 'A' from `ch` and adding 1. If `ch` is a lowercase letter, the function returns the position of the letter in the alphabet by subtracting the ASCII value of 'a' from `ch` and adding 1. If `ch` is not a letter, the function returns 0.
    

# **ARRAYS**

An array is a collection of variables of the same type, accessed through a single identifier. Each variable in an array is called an element and is identified by an index or a subscript. Arrays allow programmers to store and manipulate multiple values of the same data type in a single structure.

## **Parts of an Array**

* **Element**
    
    Each value in the array is called an element. Elements are the basic building blocks of an array and they can store any data type such as integer, floating-point, character, etc. In most programming languages, the elements of an array must be of the same data type.
    
* **Index**
    
    Each element in the array is identified by a unique index. The index is an integer value that represents the position of the element in the array. The first element of an array is usually assigned an index of 0 and subsequent elements are assigned increasing index values.
    
* **Size**
    
    The size of an array is the number of elements it contains. The size of an array is fixed at the time of declaration and cannot be changed during runtime. In some programming languages, such as C, the size of an array must be specified explicitly in the declaration.
    
* **Declaration**
    
    The declaration of an array specifies its data type, name, and size. The syntax for declaring an array varies depending on the programming language, but generally follows the format: `data_type array_name[size];`
    
* **Initialization**
    
    The initialization of an array sets the values of its elements at the time of declaration. The initialization can be done using a list of values enclosed in braces, separated by commas. For example: `int my_array[3] = {1, 2, 3};`
    
* **Traversal**
    
    Traversal refers to the process of accessing each element of an array in order to perform some operation on it. Traversal is typically done using a loop that iterates over the elements of the array. In most programming languages, the loop variable is used as the index to access each element of the array.
    

## **General Construct**

```c
data_type array_name[size];
```

**Construct Explained**

This statement declares an array named `array_name` with a fixed size of `size` elements, where each element has the data type `data_type`

**Example**

```c
int number_array[10];
/*
*Example of a 1D Array
*/
```

This creates an array named `number_array` that can store 10 integer values. We can access and manipulate individual elements of the array using index notation.

## **Types of Arrays**

### One-dimensional array

This is the most common type of array and consists of a single row of elements. Each element is accessed using a single index.

### Multi-dimensional array

This type of array consists of multiple rows and columns of elements. Each element is accessed using two or more indices.

### Dynamic array

Also known as a resizable array, this type of array allows for the size of the array to be changed during runtime. It is implemented using pointers and memory allocation functions.

### Jagged array

This is an array of arrays, where each element of the main array is another array of varying size. This allows for more flexibility in terms of the size of the array.

### Sparse array

This is an array in which most of the elements are empty or zero. Rather than storing all elements in memory, only the non-zero or non-empty elements are stored along with their indices. This can be more memory-efficient for large arrays with many empty elements.

### Associative array

Also known as a map, dictionary, or hash table, this type of array allows for elements to be accessed using keys rather than indices. Each element is stored as a key-value pair, and the keys must be unique.

### Constant Arrays

A constant array is an array in programming that has elements that cannot be modified after initialization. Once the elements of a constant array are set, they cannot be changed by the program during runtime.

Declaring an array as constant is useful in situations where you want to ensure that the values in the array are not accidentally modified by the program, which can lead to unexpected behavior.

**General Construct**

```c
const int constant_array_example[3] = {1, 2, 3};
```

**Construct Explained**

The `constant_array_example` array is declared as a constant array with three elements. The `const` keyword before the array name indicates that the elements of the array cannot be modified. Once the values 1, 2, and 3 are assigned to the elements during initialization, they cannot be changed by the program.

> NOTE: In this series, we will only discuss Constant Arrays, One Dimensional Arrays and Multidimensional Arrays.

# **One-Dimensional Arrays**

One-dimensional arrays are a type of array in which elements are arranged in a single row or line. Each element of the array can be accessed using a single index, which is a non-negative integer that represents the position of the element within the array. In most programming languages, the index of the first element of an array is 0 and the index of the last element is **size-1**, where size is the total number of elements in the array.

One-dimensional arrays can be initialized at the time of declaration by assigning values to each element. For example, the following statement declares an array named `number_Array` with 5 integer elements and initializes them with values 10, 20, 30, 40 and 50.

```c
int number_Array[5] = {10, 20, 30, 40, 50};
/*
*Initialisation and Declaration of array
*/
```

Once an array is initialized, individual elements can be accessed and modified using the index notation, as shown below:

```c
number_Array[2] = 50 ;
 /*
  *This will assign 50 o the 3rd Element of the array
  */

int store_variable = number_Array[4]; 
/* 
*Access the value of the 5th element of the array and store it in  variable "store_variable"
*/
```

## **Example 1**

Program to read the marks of 5 students and calculates the sum and averages of the marks.

```c
#include <stdio.h>

int main(void) {
int marks_of_students[5], i ;
int sum_of_marks = 0, average_marks ;

printf("Enter Marks of Five students and Press 'Enter': \n");
/*
*Collecting User Input
*/
for (i = 0; i < 5 ; i++) {
    scanf("%d", &marks_of_students[i]);
/*
*This is the user input loop
*/
}
for (i = 0 ; i < 5 ; i++) {
    sum_of_marks += marks_of_students[i];
    average_marks = (sum_of_marks/5);
    /*
    *This is the printing loop
    */
   }
printf("The sum of marks of the five students are: %d \n ", sum_of_marks);
printf("The average marks of the five students are: %d\n ", average_marks );
return 0;
}
```

**Code Explained**

This code is a simple program in C that prompts the user to enter the marks of five students and then calculates the sum and average of the marks using an array.

`#include <stdio.h>`

This is a preprocessor directive that includes the standard input/output header file in the program. This header file provides functions for input/output operations in C.

`int main(void) {`

This is the main function of the program, which is the starting point of execution. It returns an integer value (0 in this case) to the operating system, indicating the status of the program execution.

`int marks_of_students[5], i ;`

This line declares an integer array `marks_of_students` of size 5, which will store the marks of the five students. It also declares an integer variable `i` to be used as a loop counter.

`int sum_of_marks = 0, average_marks ;`

This line declares an integer variable `sum_of_marks` and initializes it to 0, which will store the sum of the marks. It also declares an integer variable `average_marks` to store the average of the marks.

`printf("Enter Marks of Five students and Press 'Enter': \n");`

This line displays a message to the user to enter the marks of the five students.

## **Example 2**

An array to count and read odd or even numbers of 10 Integers.

```c
#include <stdio.h>

int main(void) {
int ten_integers[10] , i ;
int even_numbers = 0, odd_numbers = 0;

printf("Enter The ten digits/integers and press 'Enter': \n ");
for (i = 0 ; i < 10 ; i++ ) {
    scanf("%d", &ten_integers[i]);
    }
for (i = 0 ; i < 10 ; i++) {
        if ((ten_integers[i] % 2) == 0) {
        even_numbers++ ;
         } 
         else {
               odd_numbers++ ;
          }
}
printf("The odd numbers are : %d\n",odd_numbers);
printf("The even numbers are : %d\n",even_numbers);
return 0;
}
```

**Code Explained**

* This program allows the user to enter ten integers and then it counts the number of even and odd integers in the array.
    
* The first line of the code includes the standard input/output library.
    
* The main function starts with the declaration of an integer array named "ten\_integers" of size 10 and two integer variables "even\_numbers" and "odd\_numbers" initialized to zero.
    
* The printf statement prompts the user to input ten integers separated by a space and hit the enter key.
    
* A for loop is used to iterate over the array from index 0 to index 9. Within the loop, scanf() function is used to read the ten integers from the user and store them in the "ten\_integers" array.
    
* The second for loop is used to iterate over the array and check whether each integer in the array is even or odd. If the integer is even, the "even\_numbers" variable is incremented by 1, and if it's odd, the "odd\_numbers" variable is incremented by 1.
    
* Finally, two printf statements are used to print out the number of even and odd integers counted in the array. The return statement at the end of the main function is used to return a value of 0 to indicate that the program has been completed successfully.
    

> NOTE: This code assumes that the user enters ten integers only. If the user enters more or fewer than ten integers, the program may behave unexpectedly. To make the program more robust, we can add an error handling code to check the number of integers entered by the user.

## **Example 3**

A program to read in two arrays of size 5 and store the arrays into a third array

```c
#include <stdio.h>
int main(void) {
int first_array[5], second_array[5], sum_of_the_two_arrays[5] , i ;
printf("Enter five elements of the first array: \n");
for (i = 0 ; i < 5 ; i++) {
    scanf("%d", &first_array[i]);
   }
printf("Enter five elements of the second array: \n");
for (i = 0 ; i < 5 ; i++) {
    scanf("%d", &second_array[i]);
    }

printf("The sum of the elements of the two arrays is: \n");
for (i = 0 ; i < 5 ; i++ ) {
    sum_of_the_two_arrays[i] = first_array[i] + second_array[i];
    printf("The Element at %d = %d\n ", i , sum_of_the_two_arrays[i]);
    printf("\n");
  }
return 0 ;
}
```

**Code Explained**

* The program defines three arrays of integers, `first_array`, `second_array` and `sum_of_the_two_arrays`, each with a size of 5.
    
* Prompts the user to enter five integers to fill the `first_array` array using the `scanf` function.
    
* Prompt the user to enter five integers to fill the `second_array` array using the `scanf` function.
    
* Add the corresponding elements of `first_array` and `second_array` arrays and store the results in `sum_of_the_two_arrays`.
    
* Print the sum of each element of the `sum_of_the_two_arrays` array using the `printf` function.
    
* Exit the program
    

```c
#include <stdio.h>
```

This line includes the standard input/output library, which provides functions for reading input from the user and printing output to the console.

```c
int main(void) {
```

This line defines the `main` function, which is the entry point of the program.

```c
int first_array[5], second_array[5], sum_of_the_two_arrays[5], i;
```

This line defines three integer arrays `first_array`, `second_array`, and `sum_of_the_two_arrays`, each with a size of 5, and an integer variable `i`, which is used as a loop counter.

```c
printf("Enter five elements of the first array: \n");
for (i = 0 ; i < 5 ; i++) {
    scanf("%d", &first_array[i]);
   }
```

These lines prompt the user to enter five integers to fill the `first_array` array. It uses a `for` loop to iterate through the array, and the `scanf` function to read each integer from the console and store it in the corresponding array element.

```c
printf("Enter five elements of the second array: \n");
for (i = 0 ; i < 5 ; i++) {
    scanf("%d", &second_array[i]);
    }
```

These lines prompt the user to enter five integers to fill the `second_array` array. It uses a `for` loop to iterate through the array, and the `scanf` function to read each integer from the console and store it in the corresponding array element.

```c
printf("The sum of the elements of the two arrays is: \n");
for (i = 0 ; i < 5 ; i++ ) {
    sum_of_the_two_arrays[i] = first_array[i] + second_array[i];
    printf("The Element at %d = %d\n ", i , sum_of_the_two_arrays[i]);
    printf("\n");
  }
```

These lines compute the sum of each corresponding element of `first_array` and `second_array`, and store the results in `sum_of_the_two_arrays`. It uses a `for` loop to iterate through the arrays, and the `printf` function to print the sum of each corresponding element of `first_array` and `second_array`.

```c
return 0 ;
```

This line indicates the successful completion of the program and returns a value of `0` to the operating system.

# **Multi-Dimensional Arrays**

Multidimensional arrays are arrays that have more than one dimension, i.e., they have elements arranged in a tabular or matrix-like format with rows and columns.

## **Types of Multidimensional Arrays**

Are mainly two:

* ### Two-Dimension Arrays
    
* ### Three-Dimensional Array
    

## **Parts of a Multidimensional array**

* **Dimensions**
    
    A two-dimensional array has two dimensions, represented by two sets of square brackets. The first dimension specifies the number of rows in the array, and the second dimension specifies the number of columns in each row.
    
* **Elements**
    
    The elements of a two-dimensional array are the values stored in the array. Each element can be accessed using two indices, one for the row and one for the column. For example, `myArray[0][0]` refers to the element in the first row and first column of the array.
    
* **Rows**
    
    A row is a horizontal set of elements in a two-dimensional array. The number of rows in the array is specified by the first dimension.
    
* **Columns**
    
    A column is a vertical set of elements in a two-dimensional array. The number of columns in each row is specified by the second dimension.
    
* **Indexing**
    
    To access an element in a two-dimensional array, you need to provide two indices: one for the row and one for the column. The indices are enclosed in square brackets and separated by a comma. For example, `myArray[2][3]` refers to the element in the third row and fourth column of the array.
    
* **Iteration**
    
    To iterate over all the elements in a two-dimensional array, you typically use nested loops. The outer loop iterates over each row, while the inner loop iterates over each column in that row. This allows you to perform operations on every element in the array.
    

# **Two Dimensional Arrays**

A two-dimensional array is a type of multi-dimensional array that contains a collection of elements arranged in a grid, with rows and columns. It is also known as a matrix.

In programming, a two-dimensional array is typically declared using two sets of square brackets. The first set specifies the number of rows in the array, and the second set specifies the number of columns in each row.

## **General Construct**

```c
int two_dimensional_array[rows][collumns] ;
```

**Construct Example**

```c
int two_dimensional_array[3][4] ;
```

`two_dimensional_array` is a two-dimensional array with 3 rows and 4 columns. The array can hold a total of 12 elements, which can be accessed using two indices, one for the row and one for the column. For example, `two_dimensional_array[0][0]` would refer to the element in the **first row** and **first column** of the array.

> NOTE: A 2-Dimensional array is an array of 1-Dimensional arrays.

## **Example 1**

Program to prompt the user to enter the elements of a 2D Array , print the arrray elements as well as the sum of the elements of the array

```c
#include <stdio.h>
int main() {
int two_dimensional_array[2][3] , i , j , sum = 0 ;

  printf("Enter the elements of the 2D Array: \n");
  /*
  *User Input Loop
  */
  for (i = 0 ; i < 2 ; i++) {
      for (j = 0 ; j < 3 ; j++) {
        scanf("%d" , &two_dimensional_array[i][j]);
       }
  }
  /*
  *Printing/Output Loop
  */
  printf("The Matrix Entered is : \n");
  
  for (i = 0 ; i < 2 ; i++) {
      for (j = 0 ; j < 3 ; j++) {
        printf( "%d\t " , two_dimensional_array[i][j]);
        sum = sum + two_dimensional_array[i][j];
      }

      printf("\n");
  }
  printf("\n Sum of the matrix =  %d\n" , sum );
  return 0;
}
```

**Code Explained**

* This is a C program that creates a 2D array, takes user input for its elements, prints the array, and calculates the sum of its elements.
    
* First, the program includes the standard **input/output** header file, "stdio.h".
    
* Then, the "**main**" function is defined, which is the entry point of the program.
    
* Inside the "main" function, a 2D integer array named "two\_dimensional\_array" is declared with 2 rows and 3 columns, and three integer variables are declared, "i", "j", and "sum" which will be used later.
    
* The program then prompts the user to enter the elements of the 2D array using the "printf" function to display the message "Enter the elements of the 2D Array: \\n".
    
* Next, the program enters a loop that iterates through the rows and columns of the 2D array using two nested "for" loops. Inside the loop, the "scanf" function is used to take user input and store it in the corresponding element of the array using the syntax "two\_dimensional\_array\[i\]\[j\]".
    
* After taking input from the user, the program enters another loop to print the 2D array using the "printf" function. The loop iterates through the rows and columns of the 2D array using two nested "for" loops. Inside the loop, the "printf" function is used to display each element of the array using the syntax "two\_dimensional\_array\[i\]\[j\]". The variable "sum" is also incremented by the value of the current element in each iteration of this loop.
    
* Once the loop has finished, the program prints the sum of all the elements in the 2D array using the "printf" function with the message "Sum of the matrix = %d\\n" and the variable "sum".
    
* Finally, the "main" function returns 0, indicating successful program completion.
    

**Assuming the user enters : 2 2 2 2 2 2**

**Code Output**

```c
The Matrix Entered is :
2        2       2
2        2       2

Sum of the matrix =  12
```

## **Example 2**

Program to print a matrix and its Transpose

```c
#include <stdio.h>

int main() {

  int two_dimensional_array[2][3] , i , j ;
  printf("Enter the elements of the 2D arrary / Matrix: \n");

  /*
  *Collecting user input loop
  */
  for (i = 0 ; i < 2 ; i++) {
    for (j = 0 ; j < 3 ; j++) {
      scanf("%d" , &two_dimensional_array[i][j]);
    }
  }

  printf("The Matrix before Transpose is: \n" );

  for (i = 0 ; i < 2 ; i++) {
    for (j = 0 ; j < 3 ; j++) {
      printf("%d\t" , two_dimensional_array[i][j]);
    }
    printf("\n");
  }
  printf("\n");
  printf("The Matrix after Transpose is : \n");
  /*
  *Printing/output Loop
  */
  for (i = 0 ; i < 3 ; i ++) {
    for (j = 0 ; j < 2 ; j ++) {
      printf("%d\t" ,two_dimensional_array[j][i]);
    }

    printf("\n");

  }
  return 0 ;
}
```

* This is a C program that creates a 2D array, takes user input for its elements, and then transposes the array, i.e., swaps the rows and columns of the matrix. The program then prints the original matrix and the transposed matrix.
    
* First, the program includes the standard input/output header file, "stdio.h".
    
* Then, the "main" function is defined, which is the entry point of the program.
    
* Inside the "main" function, a 2D integer array named "two\_dimensional\_array" is declared with 2 rows and 3 columns, and two integer variables "i" and "j" are declared.
    
* The program then prompts the user to enter the elements of the 2D array using the "printf" function to display the message "Enter the elements of the 2D array / Matrix: \\n".
    
* Next, the program enters a loop that iterates through the rows and columns of the 2D array using two nested "for" loops. Inside the loop, the "scanf" function is used to take user input and store it in the corresponding element of the array using the syntax "two\_dimensional\_array\[i\]\[j\]".
    
* After taking input from the user, the program enters another loop to print the original matrix using the "printf" function. The loop iterates through the rows and columns of the 2D array using two nested "for" loops. Inside the loop, the "printf" function is used to display each element of the array using the syntax "two\_dimensional\_array\[i\]\[j\]".
    
* Then the program prints a newline character using the "printf" function to move to the next line.
    
* The program then prints the message "The Matrix after Transpose is : \\n" using the "printf" function.
    
* Next, the program enters a loop to print the transposed matrix. This loop iterates through the rows and columns of the transposed 2D array using two nested "for" loops. Inside the loop, the "printf" function is used to display each element of the array using the syntax "two\_dimensional\_array\[j\]\[i\]". This syntax swaps the rows and columns of the original matrix.
    
* After printing the transposed matrix, the "main" function returns 0, indicating successful program completion.
    

**Assuming the user enters: 1 1 1 2 2 2**

**Code Output:**

```c
The Matrix before Transpose is:
1       1       1
2       2       2

The Matrix after Transpose is :
1       2
1       2
1       2
```

## **Example 3**

A Program to print sum of individual rows and collumns of a Matrix

```c
#include <stdio.h>

int main() {
  int two_dimensional_array[3][3], i, j;
  int sum_of_rows = 0, sum_of_columns = 0;

  printf("Enter the elements of the Matrix: \n");

  // Collecting user input
  for (i = 0; i < 3; i++) {
    for (j = 0; j < 3; j++) {
      scanf("%d", &two_dimensional_array[i][j]);
    }
  }

/*
*Printing/Output Loop
*/
  for (i = 0; i < 3; i++) {
    for (j = 0; j < 3; j++) {
      sum_of_rows += two_dimensional_array[i][j];
      sum_of_columns += two_dimensional_array[j][i];
    }
  }

  printf("The sum of rows = %d\n", sum_of_rows);
  printf("The sum of columns = %d\n", sum_of_columns);

  return 0;
}
```

**Code Explained**

* This program is designed to take user input of a 3x3 matrix, calculate the sum of each row and column, and then output the results.
    
* The program first declares a 2D array called `two_dimensional_array` with 3 rows and 3 columns, and two integer variables `i` and `j` for use in loops. It also declares two integer variables `sum_of_rows` and `sum_of_columns` and initializes them to 0.
    
* The program then prompts the user to enter the elements of the matrix, using nested loops to collect the user input and store it in the `two_dimensional_array` array.
    
* After collecting user input, the program uses another nested loop to calculate the sum of each row and column. The outer loop iterates over the rows, and the inner loop iterates over the columns. For each element in the matrix, the program adds it to the corresponding sum variable.
    
* Finally, the program prints the sum of each row and column using `printf()` statements, and returns 0 to indicate successful program completion.
    

**Assuming the user enters: 1 1 1 1 1 1 1 1 1**

**Code Output**

```c
The sum of rows = 9
The sum of columns = 9
```

## **Example 4**

A program to multiply two matrices

```c
#include <stdio.h>

int main() {
  int first_matrix[3][3], second_matrix[3][3], resultant_multiplication_matrix[3][3], i, j, k;

  printf("Enter the elements of matrix1: \n");
  for (i = 0; i < 3; i++) {
    for (j = 0; j < 3; j++) {
      scanf("%d", &first_matrix[i][j]);
    }
  }

  printf("Enter the elements of matrix2: \n");
  for (i = 0; i < 3; i++) {
    for (j = 0; j < 3; j++) {
      scanf("%d", &second_matrix[i][j]);
    }
  }

 /*
*Multiplication Loop
*/
  for (i = 0; i < 3; i++) {
    for (j = 0; j < 3; j++) {
      resultant_multiplication_matrix[i][j] = 0;
      for (k = 0; k < 3; k++) {
        resultant_multiplication_matrix[i][j] += first_matrix[i][k] * second_matrix[k][j];
      }
    }
  }

 /*
*Printing/Output Loop
*/
  printf("The product of the matrices is: \n");
  for (i = 0; i < 3; i++) {
    for (j = 0; j < 3; j++) {
      printf("%d\t", resultant_multiplication_matrix[i][j]);
    }
    printf("\n");
  }

  return 0;
}
```

**Code Explained**

* This program multiplies two matrices entered by the user and prints the result.
    
* The program first declares three 3x3 integer arrays: `first_matrix`, `second_matrix`, and `resultant_multiplication_matrix`. It also declares three integer variables `i`, `j`, and `k` for looping.
    
* The program then prompts the user to enter the elements of the first and second matrices using nested loops that iterate through each row and column of the matrices. The user input is stored in the respective arrays.
    
* The program then performs the matrix multiplication using a nested loop that iterates through each row and column of the resultant matrix. For each element of the resultant matrix, the program performs a dot product of the corresponding row of the first matrix and the corresponding column of the second matrix. The dot product is computed using a third loop that iterates through each element of the row/column pair. The result of the dot product is stored in the corresponding element of the resultant matrix.
    
* Finally, the program prints the elements of the resultant matrix using another nested loop that iterates through each row and column of the matrix. The elements are printed using `printf()` with the `\t` character used to separate the elements within a row and the `\n` character used to start a new row.
    
* The program returns 0 at the end to indicate successful completion of the `main()` function.
    

**Assuming the user enters:**

1 1 1 1 1 1 1 1 1 (First Matrix)

1 1 1 1 1 1 1 1 1 (Second Matrix)

**Code Output**

```c
The product of the matrices is:
3       3       3
3       3       3
3       3       3
```

# Three-Dimensional Arrays

A 3D array is a multidimensional array with three dimensions.

## General Construct

```c
data_type array_name[number of 3D arrays][ rows ][ Collumns];
```

**Construct Explained**

* data\_type
    
    represents the type of data that the array will hold (e.g., `int`, `float`, `char`, etc.),
    
* `array_name` is the name of the array and the rest represent the sizes of the three dimensions.
    

Example

```c
int three_dimensional_array[2][3][3];
```

This means that there are **two** 3D Arrays each 3 by 3 Matrix.

## Assigning & Accessing Elements of a 3D Array

To access all the elements of a 3D array in C language, you can use nested loops. Here's an example of how you could access all the elements of the 3D array `three_dimensional_array`

```c
int three_dimensional_array[2][3][3];
int i, j, k;

/*
*Assign values to the elements of the array
*/
for (i = 0; i < 2; i++) {
    for (j = 0; j < 3; j++) {
        for (k = 0; k < 3; k++) {
            three_dimensional_array[i][j][k] = i + j + k;
        }
    }
}

/*
*Access all the elements of the array
*/
for (i = 0; i < 2; i++) {
    for (j = 0; j < 3; j++) {
        for (k = 0; k < 3; k++) {
            printf("Element at [%d][%d][%d] is %d\n", i, j, k, three_dimensional_array[i][j][k]);
        }
    }
}
```

**Sample Output**

```c
Element at [0][0][0] is 0
Element at [0][0][1] is 1
Element at [0][0][2] is 2
Element at [0][1][0] is 1
Element at [0][1][1] is 2
Element at [0][1][2] is 3
Element at [0][2][0] is 2
Element at [0][2][1] is 3
Element at [0][2][2] is 4
Element at [1][0][0] is 1
Element at [1][0][1] is 2
Element at [1][0][2] is 3
Element at [1][1][0] is 2
Element at [1][1][1] is 3
Element at [1][1][2] is 4
Element at [1][2][0] is 3
Element at [1][2][1] is 4
Element at [1][2][2] is 5
```

## Example 1

A program that demonstrates the use of a three-dimensional array to store and retrieve values.

```c
#include <stdio.h>

int main() {
    int three_dimensional_array[2][3][3];
    int i, j, k;

    /*
    *Ask the user to enter values for the elements of the array
    */ 
    for (i = 0; i < 2; i++) {
        for (j = 0; j < 3; j++) {
            for (k = 0; k < 3; k++) {
                printf("Enter value for element [%d][%d][%d]: ", i, j, k);
                scanf("%d", &three_dimensional_array[i][j][k]);
            }
        }
    }

    /*
    *Accesings all the elements of the array and printing their values
    */
    for (i = 0; i < 2; i++) {
        for (j = 0; j < 3; j++) {
            for (k = 0; k < 3; k++) {
                printf("Element at [%d][%d][%d] is %d\n", i, j, k, three_dimensional_array[i][j][k]);
            }
        }
    }

    return 0;
}
```

**Code Explained**

* The program first creates a three-dimensional integer array `three_dimensional_array` with dimensions 2 x 3 x 3, i.e., it has 2 "layers", each with 3 rows and 3 columns.
    
* It then prompts the user to enter values for each element of the array by using a nested loop to iterate over all the elements. The loop variables `i`, `j`, and `k` are used to index into the array and obtain the corresponding element. The `scanf()` function is used to read in the value from the user and store it in the appropriate element of the array.
    
* After all the values have been entered, the program then accesses all the elements of the array using another nested loop and prints their values to the console using the `printf()` function.
    
* The output indicates the element's indices and the corresponding value stored in the array.
    

## Example 2

A program that prompts the user and uses a 3D array to store the marks of students

```c
#include <stdio.h>

int main() {
    int marks[3][4][2]; 
/*
*a 3D array to store the marks of 3 students in 4 subjects for 2 semesters
*/
    int student, subject, semester;

    /*
    *Ask the user to enter the marks of each student for each subject in each semester
    */
    for (student = 0; student < 3; student++) {
        for (subject = 0; subject < 4; subject++) {
            for (semester = 0; semester < 2; semester++) {
                printf("Enter marks of Student %d for Subject %d in Semester %d: ", student + 1, subject + 1, semester + 1);
                scanf("%d", &marks[student][subject][semester]);
            }
        }
    }

    // Access all the elements of the array and print their values
    for (student = 0; student < 3; student++) {
        for (subject = 0; subject < 4; subject++) {
            for (semester = 0; semester < 2; semester++) {
                printf("Marks of Student %d for Subject %d in Semester %d are %d\n", student + 1, subject + 1, semester + 1, marks[student][subject][semester]);
            }
        }
    }

    return 0;
}
```

**Code Explained**

* This code declares a 3D array "marks" to store the marks of 3 students in 4 subjects for 2 semesters. It then prompts the user to enter the marks of each student for each subject in each semester using nested for loops. Inside the loops, it prints a message asking the user to enter the marks for a particular student, subject, and semester, and then it stores the entered value in the corresponding element of the array.
    
* After the user has entered all the values, the code uses another set of nested for loops to access all the elements of the array and print their values. Inside these loops, it prints a message showing the marks of each student for each subject in each semester.
    
* Finally, the program returns 0, indicating successful completion.
    

**That's it for now, see you around!.**


## **Kind Notice**

* I'm always exploring new ways to optimize code and improve system performance, and I'm happy to share my knowledge with others.
* I hope that my examples and projects will be useful to those looking to learn more software engineering  or those looking to improve their skills in this field.

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
