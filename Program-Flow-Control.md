# **Program Flow Control**

Before we dive deep into the topic, the first thing we should ask ourselves is what a computer program is.

### So, What is a Computer Program?

A computer program is a set of instructions that tell a computer what to do at any specific instance in time.

It is written in a specific programming language and is typically executed by a computer's processor.

Programs can be used for a wide variety of purposes, including performing calculations, processing data, creating graphics or sound, communicating with other devices, and controlling hardware components.

> *Note: Programs typically range in complexity from simple scripts or macros to sophisticated applications and operating systems*.

Having known what a computer program is, we can now jump in and address the elephant in the room, **“Program Flow Control”**

# **INTRODUCTION**

A Program flow control is the ability of a computer program to make decisions and control the order in which its instructions are executed. It allows the program to respond to different inputs or conditions and to execute different sets of instructions based on those inputs and/or conditions.

Flow control structures are used to achieve this objective.

# **FLOW CONTROL STRUCTURES**

A program flow control structure is a programming construct that allows a program to control the order in which its instructions are executed based on different inputs and conditions. These are mainly subdivided into three categories.

They include:

### **Conditional statements**

These statements allow the program to execute a certain set of instructions based on whether a particular condition is true or false. For example, an "if" statement might execute a set of instructions if a certain condition is true. Logical operators as well as conditional operators also fall into this category.

### Loops

Loops allow a program to repeat a set of instructions multiple times. For example, a "for" loop might execute a set of instructions a certain number of times so long as a certain constraint/condition remain “true”.

### Subroutines

Subroutines allow a program to break up its instructions into smaller, reusable pieces. This can make the program easier to understand and maintain.

By using these flow control structures, a computer becomes more flexible and able to handle a wider range of situations.

Let’s dive deep and explore each, shall we?

# **CONDITIONAL STATEMENTS**

A conditional statement is a programming construct that allows a program to execute certain code or actions **only if** a certain condition is met.

Types of conditional Statements:

## **"if" statements**

These statements execute a set of instructions only if a specified condition is true.

**General Construct**

```c
if (condition to test/boolean expression) {
    // body of the conditional statement here
    }
```

**Construct Explained**

* There is a condition expression that is evaluated. If the condition is true, the code block inside the if statement is executed.
    

> NOTE: The condition expression must evaluate to a boolean value (true or false). If the condition is always true, the code inside the if statement will always execute. If the condition is always false, the code inside the if statement will never execute.

**Example**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[] = "Brian";
    if (strcmp(first_name, "Brian") == 0) {
        printf("Good morning Software Engineer!\n");
        printf("Have a lovely day!");
    }
    return 0;
}
```

**Code Explained**

* `#include <stdio.h>` and `#include <string.h>`
    
    These lines include the standard input/output and string libraries in the program, respectively. The `string.h` library provides functions for working with strings, including the `strcmp()` function used in this program.
    
* `int main() { ... }`
    
    This is the main function of the program, which is where the program starts executing. The function returns an integer value, which in this case is 0.
    
* `char first_name[] = "Brian";`
    
    This line declares a character array named `first_name` and initializes it with the value "Brian". The square brackets `[]` are used to specify the size of the array, but in this case, the size is automatically determined based on the length of the string literal.
    
* `if (strcmp(first_name, "Brian") == 0) { ... }`
    
    This line uses the `strcmp()` function to compare the value of `first_name` with the string "Brian". `strcmp()` returns 0 if the two strings are equal, so the `if` statement checks whether the return value is equal to 0. If the condition is true, the code inside the curly braces will be executed.
    
* `printf("Good morning Software Engineer!\n");`
    
    If the condition in the `if` statement is true, this line will print the message "Good morning Software Engineer!" to the console. The `\n` character at the end of the message represents a newline character, which causes the next output to be printed on a new line.
    
* `return 0;`
    
    This line returns the value 0 from the `main` function, which indicates to the operating system that the program executed successfully.
    

**Code Output**

```c
Good morning Software Engineer!
Have a lovely day!
```

## **Nested “if” Statements**

A nested if statement is an **“if”** statement that is placed inside another **“if”** statement.

This is a way of testing for multiple conditions in a more complex way than a single **if** statement allows.

**General Construct**

```c
if (condition to test/boolean expression) {
        if (boolean expression here) {
                //body of conditional statement here
             }
}
```

**Construct Explained**

* There is an outer "if" statement and an inner "if" statement. The inner statement is completely contained within the code block of the outer statement.
    
* The condition expressions are the same as in a simple "if" statement, but there are now two conditions - one for the outer statement and one for the inner statement. The inner statement is executed only if the outer statement's condition is true.
    
* If the outer condition is true, the code block inside the outer if statement is executed. Then, if the inner condition is true, the code block inside the inner if statement is executed.
    

> NOTE: Any number of nested "if" statements can be used, but as the number of nested statements increases, the code can become harder to read and understand. Therefore, it's important to keep the code as simple and concise as possible, while still achieving the desired functionality. Additionally, the use of nested "if" statements can often be avoided by using logical operators such as "&&" (logical AND) and "||" (logical OR) to combine conditions in a more readable and concise way.

**Example**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[] = "Brian";
    char middle_name[] = "Enos";
    if (strcmp(first_name, "Brian") == 0) {
        printf("Good morning Software Engineer!\n");
        printf("Have a lovely day!\n");
          if (strcmp(middle_name, "Enos") == 0) {
                printf("Software Engineers Rule the World!!\n");
          }
    }
    return 0;
}
```

**Code Explained**

* `#include <stdio.h>` and `#include <string.h>`
    
    These lines include the standard input/output and string libraries in the program, respectively. The `string.h` library provides functions for working with strings, including the `strcmp()` function used in this program.
    
* `int main() { ... }`
    
    This is the main function of the program, which is where the program starts executing. The function returns an integer value, which in this case is 0.
    
* `char first_name[] = "Brian";` and `char middle_name[] = "Enos";`
    
    These lines declare two character arrays named `first_name` and `middle_name`, respectively, and initialize them with the values "Brian" and "Enos", respectively.
    
* `if (strcmp(first_name, "Brian") == 0) { ... }`
    
    This line uses the `strcmp()` function to compare the value of `first_name` with the string "Brian". If the two strings are equal, the code inside the curly braces will be executed.
    
* `printf("Good morning Software Engineer!\n");` and `printf("Have a lovely day!\n");`
    
    If the condition in the first `if` statement is true, these lines will print the messages "Good morning Software Engineer!" and "Have a lovely day!" to the console, respectively.
    
* `if (strcmp(middle_name, "Enos") == 0) { ... }`
    
    This line uses the `strcmp()` function to compare the value of `middle_name` with the string "Enos". If the two strings are equal, the code inside the curly braces will be executed.
    
* `printf("Software Engineers Rule the World!!\n");`
    
    If the condition in the second `if` statement is true, this line will print the message "Software Engineers Rule the World!!" to the console.
    
* `return 0;`
    
    This line returns the value 0 from the `main` function, which indicates to the operating system that the program executed successfully.
    

**Code Output**

```c
Good morning Software Engineer!
Have a lovely day!
Software Engineers Rule the World!!
```

## **"if.... else" statements**

These statements are used in conjunction with "if" statements and execute a set of instructions **if the condition specified in the "if" statement is false.**

**General Construct**

```c
if (condition to test here) 
{
    //body of if statement here
}
else 
{
//body of else statement here
}
```

**Construct Explained**

* There is a condition expression that is evaluated. If the condition is true, the code block inside the if statement is executed. If the condition is false, the code block inside the else statement is executed.
    
* The condition expression must evaluate to a boolean value (true or false). If the condition is always true, the code inside the if statement will always execute, and the code inside the else statement will never execute. If the condition is always false, the code inside the else statement will always execute, and the code inside the if statement will never execute.
    

> NOTE: It is possible to have multiple "if-else" statements in succession, forming a chain of conditions to be evaluated. In such a case, the conditions are evaluated in sequence until one of them is found to be true, and the corresponding code block is executed. If none of the conditions are true, the code block in the final "else" statement is executed.

**Example**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[] = "Brian";
    char middle_name[] = "Enos";
    if (strcmp(first_name, "Brian") == 0 && strcmp(middle_name, "Enos") == 0) {
        printf("Good morning Software Engineer!\n");
        printf("Have a lovely day!\n");
    }
    else {
        printf("We don't know you!\n");
        printf("Join us and do hard things!!\n");
    }
    return 0;
}
```

**Code Explained**

* This code compares two strings using the `strcmp()` function and prints a message based on the comparison result.
    
* The program first declares two character arrays named `first_name` and `middle_name`, and initializes them with the values "Brian" and "Enos", respectively.
    
* Then, it uses the `strcmp()` function to compare the `first_name` array with the string "Brian", and the `middle_name` array with the string "Enos". The `strcmp()` function returns 0 if the strings are equal, and a nonzero value if they are different.
    
* The `if` statement checks if both `strcmp()` function calls return 0, using the logical AND operator `&&`. If both strings are equal, the program prints the messages "Good morning Software Engineer!" and "Have a lovely day!".
    
* If the strings are not equal, the program prints the messages "We don't know you!" and "Join us and do hard things!!".
    
* Finally, the program returns 0 to indicate successful execution.
    

**Code Output**

```c
Good morning Software Engineer!
Have a lovely day!
```

## **Nested “if…. else”**

A nested “if…else” statement is an “if…else” placed inside another “if…else”

**General Construct**

```c
if (condition 1 to be tested here) {
   // code block to execute if condition 1 is true
   if (condition 2 to be tested here) {
      // code block to execute if condition 2 is true
   }
   else {
      // code block to execute if condition 2 is false
   }
}
else {
   // code block to execute if condition 1 is false
}
```

**Construct Explained**

* There is an **outer "if-else"** statement and an **inner "if-else"** statement. The inner statement is completely contained within the code block of the outer statement.
    
* The condition expressions are the same as in a simple "if-else" statement, but there are now two conditions - one for the outer statement and one for the inner statement. The inner statement is executed only if the outer statement's condition is true.
    
* If the outer condition is true, the code block inside the outer if statement is executed. Then, if the inner condition is true, the code block inside the inner if statement is executed. If the inner condition is false, the code block inside the inner else statement is executed.
    
* If the outer condition is false, the code block inside the outer **else** statement is executed.
    

> NOTE: Any number of nested "if-else" statements can be used, but as the number of nested statements increases, the code can become harder to read and understand. Therefore, it's important to keep the code as simple and concise as possible, while still achieving the desired functionality.

**Example**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[] = "Brian";
    char middle_name[] = "Enos";
    char last_name[] = "Otieno";
    if (strcmp(first_name, "Brian") == 0 && strcmp(middle_name, "Enos") == 0) {
        if (strcmp(last_name, "Otieno") == 0) {
            printf("Good morning Brian Enos Otieno!\n");
            printf("Engineers solve problems by choosing to do hard things.\n");
        } else {
            printf("Your Last Name is not %s\n", last_name);
        }
    } else {
        printf("We don't know you!\n");
        printf("Join us and do hard things!!\n");
    }
    return 0;
}
```

**Code Explained**

* At the beginning of the program, three character arrays are declared and initialized: `first_name`, `middle_name`, and `last_name`.
    
* The program then checks whether `first_name` is "Brian" and `middle_name` is "Enos" using the `strcmp` function. The `strcmp` function compares two strings and returns 0 if they are equal.If this condition is true, the program moves on to the next if statement.
    
* The next if statement checks whether `last_name` is "Otieno". If it is, the program prints a message that greets the person using their full name and encourages them to do hard things. If `last_name` is not "Otieno", the program prints a message informing the user that their last name does not match the expected pattern.
    
* If the first if statement is false, the program skips the second if statement and moves on to the else block, which prints a message stating that the program does not know the person and encourages them to join the community of people who do hard things.
    
* Finally, the program returns 0, which indicates that the program has been executed successfully.
    

> NOTE: This code is a simple program that checks a person's first name, middle name, and last name and prints a message depending on whether the person's full name matches a specific pattern or not.

**Code Output**

```c
Good morning Brian Enos Otieno!
Engineers solve problems by choosing to do hard things.
```

## **"else if" statements**

These statements are used in conjunction with **"if"** statements and allow a program to test multiple conditions in a series. If the first condition is false, the program checks the next condition until a true condition is found.

**General Construct**

```c
if (boolean expression 1) 
{
   // code block to execute if boolean expression 1 is true
}
else if (boolean expression 2) {
   // code block to execute if boolean expression1 is false and boolean expression 2 is true
}
else {
   // code block to execute if both boolean expression 1 and boolean expression 2 are false
}
```

**Construct Explained**

* The "if" statement tests a condition, and if that condition is true, the code block inside the braces is executed. If the condition is false, the code block is skipped and the program continues to the next statement.
    
* The "else if" statement allows for multiple conditions to be tested in sequence. If the condition in the "if" statement is false, the condition in the "else if" statement is tested, and if it is true, the code block inside the braces is executed. If the "else if" condition is false, the program continues to the next "else if" statement or to the "else" statement if there are no more "else if" statements.
    
* The "else" statement provides a default code block to execute if all previous conditions are false.
    

**Example**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[] = "Brian";
    char middle_name[] = "Enos";
    char last_name[] = "Otieno";
    if (strcmp(first_name, "Brian") == 0 && strcmp(middle_name, "Enos") == 0 && strcmp(last_name, "Otieno") == 0) {
        printf("Good morning Brian Enos Otieno!\n");
        printf("Engineers solve problems by choosing to do hard things.\n");
    } else if (strcmp(first_name, "Brian") == 0 && strcmp(middle_name, "Enos") == 0) {
        printf("This block has been executed because the if block returned a false value,\n");
    } else {
        printf("We don't know you!\n");
        printf("Join us and do hard things!!\n");
    }
    return 0;
}
```

**Code Explained**

* This code defines three character arrays `first_name`, `middle_name`, and `last_name`, with the values "Brian", "Enos", and "Otieno", respectively. Then, it uses a series of `strcmp` functions to compare the values of these arrays to the expected values.
    
* The code starts with an `if` statement that checks if the first name is "Brian", the middle name is "Enos", and the last name is "Otieno". If this condition is true, the program prints a greeting message and a motivational quote.
    
* If the first `if` statement returns false, the program proceeds to the `else if` statement, which checks if only the first name is "Brian" and the middle name is "Enos". If this condition is true, the program prints a message indicating that this block has been executed because the first `if` statement returned false.
    
* If both `if` statements return false, the program proceeds to the `else` statement, which means that the names provided do not match the expected values. The program prints a message indicating that it does not know the user and encourages them to join and do hard things.
    
* Finally, the program returns 0 to indicate successful execution.
    

**Code Output**

```c
Good morning Brian Enos Otieno!
Engineers solve problems by choosing to do hard things.
```

## **"switch" statements**

These statements allow a program to execute different sets of instructions based on the value of a variable or expression.

**General Construct**

```c
switch (condition to test here) {
   case constant1:
      // code block to execute if expression is equal to constant1
      break;
   case constant2:
      // code block to execute if expression is equal to constant2
      break;
   // more case statements can be added here
   default:
      // code block to execute if expression does not match any of the cases
      break;
}
```

**Construct Explained**

* The "switch" statement evaluates the expression and compares it to each of the constant values listed in the "case" statements. If a match is found, the code block inside the corresponding "case" statement is executed. The "break" statement is used to exit the switch statement and prevent execution of the code in any subsequent "case" statements.
    
* If none of the "case" statements match the expression, the code block inside the "default" statement is executed. The "default" statement is optional, and if it is not included, no code will be executed if none of the "case" statements match the expression.
    

> NOTE: The expression in the "switch" statement must evaluate as an integer or a character. Also, each "case" statement must contain a constant value, and duplicate values are not allowed.

**Example**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[] = "Brian";
    char middle_name[] = "Enos";
    char last_name[] = "Otieno";
    int engineer;

    if (strcmp(first_name, "Brian") == 0 && strcmp(middle_name, "Enos") == 0 && strcmp(last_name, "Otieno") == 0) {
        engineer = 1;
    } else if (strcmp(first_name, "Brian") == 0 && strcmp(middle_name, "Enos") == 0) {
        engineer = 2;
    } else {
        engineer = 3;
    }

    switch ( engineer ) {
        case 1:
            printf("Good morning Brian Enos Otieno!\n");
            printf("Engineers solve problems by choosing to do hard things.\n");
            break;
        case 2:
            printf("This block has been executed because the if block returned a false value,\n");
            break;
        default:
            printf("We don't know you!\n");
            printf("Join us and do hard things!!\n");
            break;
    }

    return 0;
}
```

**Code Explained**

* This code includes two header files, **&lt;stdio.h&gt;** and **&lt;string.h&gt;** that provide functionality for input/output operations and string handling, respectively.
    
* The code defines three character arrays, first\_name, middle\_name and last\_name, each initialized with a string literal.
    
    It also declares an integer variable **engineer**, which will be used later to determine which message to print.
    
* The program then uses the strcmp() function from the **&lt;string.h&gt;** library to compare the three character arrays with their expected values.
    
* If all three strings match their expected values, the **engineer** variable is set to 1, indicating that the person is an engineer with the full name of "Brian Enos Otieno".
    
* If only the first two strings match, the engineer variable is set to 2, indicating that the person is an engineer with the first two names of "Brian Enos". Otherwise, the **engineer** variable is set to 3, indicating that the person is not known and should strive to be an Engineer/join the engineering community.
    
* Finally, a switch statement is used to determine which message to print based on the value of the **engineer** variable. If the **engineer** variable is 1, a personalized greeting is printed along with a message about the problem-solving nature of engineers. If the engineer variable is 2, a message is printed indicating that the if block returned a false value. If the **engineer** variable is neither 1 nor 2, a generic message is printed inviting the person to join the engineering community and do hard things.
    
* The program ends with a return statement, which indicates that the program has finished executing and returns a value of 0 to the operating system.
    

**Code Output**

```c
Good morning Brian Enos Otieno!
Engineers solve problems by choosing to do hard things.
```

## **Conditional/Comparison Operators:**

Comparison operators are symbols used in programming to compare two values and determine whether they are equal, not equal, greater than, less than, greater than or equal to, or less than or equal to each other.

Comparison operators return a Boolean value (either true or false) based on the comparison result.

They include:

**Greater than (&gt;)**

This operator checks if one value is greater than another value. For example, 6 &gt; 5 would return true, while 5 &gt; 6 would return false.

**Less than (&lt;)**

This operator checks if one value is less than another value. For example, 5 &lt; 6 would return true, while 6 &lt; 5 would return false.

**Equal to (==)**

This operator checks if two values are equal to each other. For example, 5 == 5 would return true, while 5 == 6 would return false.

**Not equal to (!=)**

This operator checks if two values are not equal to each other. For example, 5! = 6 would return true, while 5 != 5 would return false.

**Greater than or equal to (&gt;=)**

This operator checks if one value is greater than or equal to another value. For example, 6 &gt;= 5 would return true, while 5 &gt;= 6 would return false.

**Less than or equal to (&lt;=)**

This operator checks if one value is less than or equal to another value. For example, 5 &lt;= 6 would return true, while 6 &lt;= 5 would return false.

> ***NOTE: Comparison operators are commonly used in conditional statements, loops, and other programming constructs to control the flow of the program based on the comparison result***

**Logical Operators**

Logical operators are used in programming to combine two or more conditions and produce a single Boolean value (true or false) as a result\*\*.\*\*

They include:

**AND operator ( && )**

This operator returns true only if both operands are true. Otherwise, it returns false.

**Example**

```c
#include <stdio.h>
int main() {
    int a = 20, b = 40, c = 60 ;
    if (a < b && b < c ) {
        printf("a is less than b and b is less than c \n");
    }
    return (0);
}
```

**Code Explained**

* `#include <stdio.h>`
    
    This line includes the standard input/output library in the program, which provides functions for reading input from the user and printing output to the console.
    
* `int main() { ... }`
    
    This is the main function of the program, which is where the program starts executing. The function returns an integer value, which in this case is 0.
    
* `int a = 20, b = 40, c = 60 ;`
    
    This line declares three integer variables named `a`, `b`, and `c`, and initializes them to the values 20, 40, and 60 respectively.
    
* `if (a < b && b < c )`
    
    This line uses the `if` statement to check whether `a` is less than `b` and `b` is less than `c`. The `&&` operator is a logical AND operator, which means that both conditions must be true for the overall condition to be true.
    
* `printf("a is less than b and b is less than c \n");`
    
    If the condition in the `if` statement is true, this line prints the message "a is less than b and b is less than c" to the console. The `\n` character at the end of the message represents a newline character, which causes the next output to be printed on a new line.
    
* `return (0);`
    
    This line returns the value 0 from the `main` function, which indicates to the operating system that the program executed successfully.
    

**Code Output**

```c
a is less than b and b is less than c
```

**OR operator ( || )**

This operator returns true if at least one of the operands is true. It returns false only if both operands are false.

**Example**

```c
#include <stdio.h>
int main() {
    int a = 20, b = 40, c = 60 ;
    if (a < b || b < c ) {
        printf("a is less than b or b is less than c \n");
    }
    return (0);
}
```

**Code Explained**

* `#include <stdio.h>`
    
    This line includes the standard input/output library in the program, which provides functions for reading input from the user and printing output to the console.
    
* `int main() { ... }`
    
    This is the main function of the program, which is where the program starts executing. The function returns an integer value, which in this case is 0.
    
* `int a = 20, b = 40, c = 60 ;`
    
    This line declares three integer variables named `a`, `b`, and `c`, and initializes them to the values 20, 40, and 60 respectively.
    
* `if (a < b || b < c )`
    
    This line uses the `if` statement to check whether `a` is less than `b` or `b` is less than `c`. The `||` operator is a logical OR operator, which means that either of the conditions can be true for the overall condition to be true.
    
* `printf("a is less than b or b is less than c \n");`
    
    If the condition in the `if` statement is true, this line prints the message "a is less than b or b is less than c" to the console. The `\n` character at the end of the message represents a newline character, which causes the next output to be printed on a new line.
    
* `return (0);`
    
    This line returns the value 0 from the `main` function, which indicates to the operating system that the program executed successfully.
    

**Code Output**

```c
a is less than b or b is less than c
```

**NOT operator ( ! )**

This operator is used to negate the result of a condition. If the condition is true, the operator returns false and vice versa.

**Example**

```c
#include <stdio.h>
int main() {
int a = 20 , b = 40 ;
if(!(a == b)) {
    printf(" a is not equal to b \n ");
    }
return (0);
}
```

**Code Explained**

* `#include <stdio.h>`
    
    This line includes the standard input/output library in the program, which provides functions for reading input from the user and printing output to the console.
    
* `int main() { ... }`
    
    This is the main function of the program, which is where the program starts executing. The function returns an integer value, which in this case is 0.
    
* `int a = 20 , b = 40 ;`
    
    This line declares two integer variables named `a` and `b` and initializes them to the values 20 and 40, respectively.
    
* `if(!(a == b)) { ... }`
    
    This line uses the `if` statement to check whether `a` is not equal to `b`. The `!` operator is a logical NOT operator, which means that it negates the expression that follows it. So `!(a == b)` is equivalent to `(a != b)`, which checks if `a` is not equal to `b`. If the condition is true, the code inside the curly braces will be executed.
    
* `printf(" a is not equal to b \n ");`
    
    If the condition in the `if` statement is true, this line will print the message "a is not equal to b" to the console. The `\n` character at the end of the message represents a newline character, which causes the next output to be printed on a new line.
    
* `return (0);`
    
    This line returns the value 0 from the `main` function, which indicates to the operating system that the program executed successfully.
    

**Code Output**

```c
a is not equal to b
```

## **Ternary Operator**

The ternary operator is a special operator that takes three operands, hence its name. It's also known as the conditional operator because it evaluates a condition and returns one of two values, depending on whether the condition is true or false.

**General Construct**

```c
condition ? expression1 : expression2
```

**Construct Explained**

* `condition` is the boolean expression to evaluate, `expression1` is the value to return if the condition is true, and `expression2` is the value to return if the condition is false.
    
* The ternary operator is often used as a shorthand for if-else statements, as it allows us to write a compact and concise code. However, it can make the code harder to read and understand, especially if the expressions are complex.
    

**Example**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[] = "Brian";
    char middle_name[] = "Enos";
    (strcmp(first_name, "Brian") == 0 && strcmp(middle_name, "Enos") == 0) ?
        (printf("Good morning Software Engineer!\n"), printf("Have a lovely day!\n")) :
        (printf("We don't know you!\n"), printf("Join us and do hard things!!\n"));
    return 0;
}
```

**Code Explained**

* This code checks if the values of two strings, `first_name` and `middle_name`, are equal to the strings "Brian" and "Enos", respectively. It uses the `strcmp()` function from the `string.h` library to compare the strings.
    
* The program uses the ternary operator to print different messages to the console, depending on the result of the comparison. If the comparison is true, which means both strings are equal to "Brian" and "Enos", respectively, the program prints two messages:
    

**Code Output (if condition is true)**

```c
Good morning Software Engineer!
Have a lovely day!
```

* On the other hand, if the comparison is false, the program prints two different messages:
    

**Code Output (if condition is false)**

```c
We don't know you!
Join us and do hard things!!
```

# LOOPS

A loop is a control structure(or a programming construct) that allows a program to execute a set of instructions repeatedly, as long as a certain condition remains “true”.

There are three main types of loops:

### **"for" loops**

These loops are used to iterate over a range of values a specified number of times. The syntax typically includes a variable that is updated with each iteration of the loop, a range of values to iterate over, and a set of instructions to execute each time the loop runs.

**General Construct**

```c
for (initialization; condition; increment/decrement) {
   // code block to execute while the condition is true
}
```

**Construct Explained**

* The "initialization" expression sets the loop variable to an initial value before the loop begins. This expression is executed only once before the loop starts.
    
* The "condition" expression is evaluated before each iteration of the loop. If the condition is true, the code block is executed. If the condition is false, the loop is terminated and program control is passed to the statement following the loop.
    
* The "increment/decrement" expression updates the loop variable after each iteration of the loop. This expression is executed after the code block is executed and before the "condition" expression is evaluated again.
    

**Example**

```c
#include <stdio.h>

int main() {
    int i = 5;

    for (int j = 0; j < i; j++) {
        printf(" %d " , j);
    }

    return 0;
}
```

**Code Explained**

* The `main()` function initializes an integer variable `i` to 5, and then enters a `for` loop.
    
* The `for` loop declares a new integer variable `j` and initializes it to 0. It then tests the condition `j < i`, which checks whether `j` is less than `i`. As long as this condition is true, the loop body will be executed.
    
* In the loop body, the `printf()` function is used to print the value of `j` to the console, followed by a space character. The `%d` format specifier is used to indicate that `j` should be formatted as an integer. The loop then increments `j` by 1 (using the `j++` syntax), and the loop condition is tested again. This process repeats until `j` is no longer less than `i`.
    
* The output of this program will be a sequence of numbers from 0 to 4, separated by spaces. This is because the `for` loop is executed 5 times, with `j` taking the values of 0, 1, 2, 3, and 4. Each time through the loop, the current value of `j` is printed to the console, followed by a space character.
    

**Code Output**

```c
0 1 2 3 4
```

### **Nested “for” Loop**

A nested for loop is a “for” loop that is placed inside another “for” loop.

It is a programming construct that allows for iteration over multiple sets of data in a hierarchical manner. The outer loop controls the number of iterations of the inner loop, and the inner loop executes a set of instructions for each iteration of the outer loop.

**General Construct**

```c
for (initialization1; condition 1; increment/decrement1) {
   // code block to execute while  condition 1 is true
   for (initialization2; condition 2; increment/decrement2) {
      // code block to execute while  condition 2 is true
   }
}
```

**Construct Explained**

* We have an oute**r "for" loop** and an **inner "for" loop**. The inner loop is completely contained within the code block of the outer loop.
    
* The initialization, condition, and increment/decrement expressions are the same as in a simple "for" loop, but there are now two sets of them - one for the outer loop and one for the inner loop. The inner loop is executed repeatedly while the outer loop is running.
    
* The outer loop runs until condition 1 is false. Each time the outer loop runs, the inner loop runs from the beginning to the end of its code block, until condition 2 is false. Then, the outer loop continues to the next iteration, and the inner loop is reset and runs again from the beginning of its code block.
    

> Note: Any number of nested loops can be used, but as the number of nested loops increases, the program's execution time can also increase significantly.

**Example**

```c
#include <stdio.h>

int main() {
    int i, j;
    i = 4;
    j = 3;

    for (int k = 0; k < i; k++) {
        for (int l = 0; l < j; l++) {
            printf("(%d %d) ", k, l);
        }
        printf("\n");
    }

    return 0;
}
```

**Code Explained**

* This code prints out a table of values representing all possible combinations of the numbers 0 to i-1 and 0 to j-1. It starts by including the standard input/output library &lt;stdio.h&gt;.
    
* In the main function, two integer variables i and j are declared and initialized to 4 and 3, respectively. Then, the program enters a nested for loop. The outer loop declares and initializes a loop variable k to 0 and loops while k is less than i. On each iteration of the outer loop, the inner loop is executed.
    
* The inner loop declares and initializes a loop variable l to 0 and loops while l is less than j. On each iteration of the inner loop, a pair of numbers (k, l) is printed to the console using the printf() function, which formats and prints the values of k and l separated by a space and enclosed in parentheses. After the inner loop is finished, a newline character is printed to move to the next line, and the outer loop continues to the next iteration.
    
* The program repeats this process until the outer loop condition is false.
    

**Code Output**

```c
(0 0) (0 1) (0 2) 
(1 0) (1 1) (1 2) 
(2 0) (2 1) (2 2) 
(3 0) (3 1) (3 2)
```

### **"while" loops**

These loops are used to repeat a set of instructions as long as a certain condition is true. The syntax includes a condition that is tested each time the loop runs, and a set of instructions to execute as long as the condition is true.

**General Construct**

```c
while (condition to test here) {
   // code block to execute while the condition is true
}
```

**Construct Explained**

* The "while" loop evaluates a condition, and if the condition is true, the code block inside the braces is executed. The loop continues to execute the code block as long as the condition is true.
    
* The condition expression is evaluated before each iteration of the loop. If the condition is true, the code block is executed. If the condition is false, the loop is terminated and program control is passed to the statement following the loop.
    

> NOTE: The condition expression must evaluate to a boolean value (true or false). If the condition is always true, the loop will continue indefinitely until the program is terminated or a "break" statement is encountered inside the loop. If the condition is always false, the code block will never be executed. It's also important to make sure the loop variable is initialized, updated and condition is defined properly, to avoid infinite loops or unexpected behavior in the program.

**Example**

```c
#include <stdio.h>

int main() {
    int i = 5, j = 0;

    while (j < i) {
        printf(" %d ", j);
        j++;
    }

    return 0;
}
```

**Code Explained**

* This code initializes the variables `i` and `j`, and then enters a `while` loop. The condition for the `while` loop is `j < i`, which means that the loop will continue to execute as long as `j` is less than `i`.
    
* Inside the loop, the code prints the value of `j` to the console using `printf()`, and then increments `j` by 1 using the `j++` syntax. This repeats until `j` is no longer less than `i`.
    
* This code produces the same output as the original code, which is a sequence of numbers from 0 to 4 (inclusive) printed to the console with a space character between each number.
    

**Code Output**

```c
0 1 2 3 4
```

### **Nested “while” Loop**

A nested **“while”** loop is a loop that is placed inside another “while” loop, similar to a nested **“for”** loop. The outer loop controls the number of iterations of the inner loop, and the inner loop executes a set of instructions for each iteration of the outer loop, as long as a certain condition is true.

**General Construct**

```c
while (condition 1 to be tested here) {
   // code block to execute while the condition 1 is true
   while (condition 2 to be tested here) {
      // code block to execute while the condition 2 is true
   }
}
```

**Construct Explained**

* There is an outer "while" loop and an inner "while" loop. The inner loop is completely contained within the code block of the outer loop.
    
* The condition expressions are the same as in a simple "while" loop, but there are now two conditions - one for the outer loop and one for the inner loop. The inner loop is executed repeatedly while the outer loop is running.
    
* The outer loop runs until condition 1 is false. Each time the outer loop runs, the inner loop runs from the beginning to the end of its code block, until condition 2 is false. Then, the outer loop continues to the next iteration, and the inner loop is reset and runs again from the beginning of its code block.
    

> NOTE: Any number of nested loops can be used, but as the number of nested loops increases, the program's execution time can also increase significantly. Also, as with any loop, care should be taken to ensure that the loop conditions are set correctly to avoid infinite loops.

**Example**

```c
#include <stdio.h>

int main() {
    int i = 4, j = 3, k = 0, l = 0;

    while (k < i) {
        while (l < j) {
            printf("(%d %d) ", k, l);
            l++;
        }
        printf("\n");
        k++;
        l = 0;
    }

    return 0;
}
```

**Code Explained**

* The code initializes the variables `i`, `j`, `k`, and `l`, and then enters a `while` loop. The outer loop uses the condition `k < i` to determine when to stop iterating. Inside the outer loop, there's an inner `while` loop that uses the condition `l < j` to determine when to stop iterating.
    
* The body of the inner loop is the same as the body of the inner `for` loop in the original code. It prints a pair of values `(k, l)` to the console, followed by a space character.
    
* After the inner loop completes, the outer loop prints a newline character (`\n`) to the console to start a new line. It then increments `k` by 1 (using the `k++` syntax), resets `l` to 0, and starts the inner loop again. This process repeats until `k` is no longer less than `i`.
    

**Code Output**

```c
(0 0) (0 1) (0 2) 
(1 0) (1 1) (1 2) 
(2 0) (2 1) (2 2) 
(3 0) (3 1) (3 2)
```

> NOTE: This code produces the same output as the original code, which is a grid of pairs of numbers `(k, l)` arranged in rows and columns. Each row has `j` pairs of numbers, and there are `i` rows in total

### "**do……. while" loops**

These loops are similar to "while" loops, but the set of instructions is executed at least once before the condition is checked. The syntax includes a set of instructions to execute and a condition to test at the end of each iteration of the loop.

**General Construct**

```c
do {
   // code block to execute at least once
} while (condition);
```

**Construct Explained**

* The "do-while" loop first executes the code block inside the braces and then checks the condition. If the condition is true, the loop continues to execute and the code block is executed again. The loop continues to execute as long as the condition is true.
    
* Unlike the "while" loop, the "do-while" loop will always execute the code block at least once, even if the condition is false. This makes the "do-while" loop useful when you need to execute a block of code at least once, regardless of whether the condition is true or false.
    

> NOTE: The condition expression must evaluate to a boolean value (true or false). If the condition is always true, the loop will continue indefinitely until the program is terminated or a "break" statement is encountered inside the loop. If the condition is always false, the code block will be executed only once. It's also important to make sure the loop variable is initialized, updated, and the condition is defined properly, to avoid infinite loops or unexpected behavior in the program.

**Example**

```c
#include <stdio.h>

int main() {
    int i = 5, j = 0;

    do {
        printf(" %d ", j);
        j++;
    } while (j < i);

    return 0;
}
```

**Code Explained**

* The program starts by including the standard input/output library `stdio.h`.
    
* The main function is declared and it initializes two integer variables `i` and `j`. `i` is initialized to 5 and `j` is initialized to 0.
    
* The program enters a do-while loop. This loop will execute at least once, regardless of the condition specified in the while statement.
    
* Inside the loop, the program prints the value of `j` to the console using the `printf` function.
    
* The program increments `j` by 1 using the `++` operator.
    
* The loop checks whether `j` is less than `i`. If it is, the loop repeats from step 4. If not, the loop terminates.
    
* Finally, the program returns 0 to indicate successful completion of the main function.
    

**Code Output**

```c
0  1  2  3  4
```

### **Nested “do…. while” Loop**

A nested do-while loop is a loop structure in which one do-while loop is placed inside another do-while loop. The outer loop controls the number of iterations of the inner loop, and the inner loop executes a set of instructions for each iteration of the outer loop, as long as a certain condition is true.

**General Construct**

```c
do {
   // code block to execute at least once
   do {
      // code block to execute at least once
   } while (condition 2 to test here);
} while (condition 1 to test here);
```

**Construct Explained**

* There is an outer "do-while" loop and an inner "do-while" loop. The inner loop is completely contained within the code block of the outer loop.
    
* The condition expressions are the same as in a simple "do-while" loop, but there are now two conditions - one for the outer loop and one for the inner loop. The inner loop is executed repeatedly while the outer loop is running.
    
* The outer loop runs until condition 1 is false. Each time the outer loop runs, the inner loop runs from the beginning to the end of its code block, until condition 2 is false. Then, the outer loop continues to the next iteration, and the inner loop is reset and runs again from the beginning of its code block.
    

> NOTE: Any number of nested loops can be used, but as the number of nested loops increases, the program's execution time can also increase significantly. Also, as with any loop, care should be taken to ensure that the loop conditions are set correctly to avoid infinite loops

**Example**

```c
#include <stdio.h>

int main() {
    int i = 4, j = 3, k = 0, l = 0;

    do {
        do {
            printf("(%d %d) ", k, l);
            l++;
        } while (l < j);
        printf("\n");
        k++;
        l = 0;
    } while (k < i);

    return 0;
}
```

**Code Explained**

* The code initializes the variables `i`, `j`, `k`, and `l`, and then enters a `do-while` loop. The condition for the outer `do-while` loop is `k < i`, which means that the loop will continue to execute as long as `k` is less than `i`.
    
* Inside the outer loop, there's another `do-while` loop that runs `l` from 0 to `j-1` (inclusive), printing out the current values of `k` and `l` at each iteration. After the inner loop is finished, the code prints a newline character and increments `k` by 1 while resetting `l` to 0.
    
* This repeats until `k` is no longer less than `i`.
    

**Code Output**

```c
(0 0) (0 1) (0 2)
(1 0) (1 1) (1 2)
(2 0) (2 1) (2 2)
(3 0) (3 1) (3 2)
```

> NOTE: This code produces the same output as the original code, which is a 2D grid of coordinates printed to the console.

# **SUBROUTINES**

A subroutine is a named block of code within a computer program that can be called or executed repeatedly at different points in the program's execution. Subroutines are used to break down a large and complex program into smaller, more manageable pieces, which can make the code more readable, reusable, and easier to understand and maintain.

**Types of Subroutines:**

### **Functions**

Functions are subroutines that **return a value**. They take one or more input arguments and produce an output value based on the computations performed within the function.

Functions can be called from other parts of the program, and their return values can be used as inputs for other functions or stored in variables.

### **Procedures**

Procedures are subroutines that do not return a value.

They perform a specific task or set of tasks within the program, but they do not produce an output that can be used by other parts of the program.

Procedures can take input arguments, but they do not have a return statement.

> **NOTE: The next article in this series will be a deep dive into Subroutines and how we can use them in our programs to simplify our work by making the program modular.**

**Thank you for taking the time to read up to this point.**

**That’s it for now. So long!**


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
