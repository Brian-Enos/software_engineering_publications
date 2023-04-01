# **Time Complexity Analysis**
## **Introduction**

Time complexity is a term used in computer science to describe the amount of time required by an algorithm or a program to execute, as a function of the input size. It is often measured in terms of the number of operations performed by the program or the amount of time taken by the program to execute, in relation to the size of the input.

Time complexity analysis is an important aspect of algorithm design and is used to evaluate the efficiency of an algorithm. It helps to identify algorithms that are more efficient and can process large inputs more quickly. Algorithms with better time complexity can scale well for larger input sizes.

The most commonly used notation for describing the time complexity of an algorithm is Big O notation. Big O notation provides an upper bound on the growth rate of the algorithm as the input size increases. For example, an algorithm with time complexity O(n) means that the execution time of the algorithm increases linearly with the size of the input. An algorithm with time complexity O(n^2) means that the execution time of the algorithm increases quadratically with the size of the input, and so on.

> NOTE: Asymptotic complexity, also known as **time complexity**, is a way of measuring the efficiency of an algorithm. It describes how the running time of an algorithm grows with the input size as the input size approaches infinity.

## **Notations in** Time Complexity Analysis

### **Big O Notation**

Big O notation is a way of describing the upper bound of the growth rate of an algorithm's running time as the input size approaches infinity. In other words, it describes the worst-case scenario for the algorithm's performance.

Formally, if a function **f(n)** is the running time of an algorithm, then **f(n)** is said to be **O(g(n))** if there exist positive constants **c** and **n0** such that for all **n** greater than or equal to **n0, f(n)** is at most **c** times **g(n)**.

Mathematically, this can be expressed as:

```c
f(n) <= c * g(n) for all n >= n0
```

This means that for large enough input sizes, the running time of the algorithm will not exceed a certain level proportional to **g(n).**

Big O notation is useful for describing the upper bound of an algorithm's running time, as it provides an upper limit on the performance of the algorithm. It's often used to compare the efficiency of different algorithms and to choose the one that has the best performance for a given problem size. However, it doesn't necessarily provide information about the average-case or best-case performance of the algorithm, which is where other notations such as Big Omega and Big Theta are useful.

### **Big Omega Notation (Ω)**

Big Omega notation (Ω) is a way of describing the lower bound of the growth rate of an algorithm's running time as the input size approaches infinity. In other words, it describes the best-case scenario for the algorithm's performance.

Formally, if a function **f(n)** is the running time of an algorithm, then **f(n)** is said to be **Ω(g(n))** if there exist positive constants c and n0 such that for all **n** greater than or equal to **n0**, f(n) is at least c times **g(n)**.

Mathematically, this can be expressed as:

```c
f(n) >= c * g(n) for all n >= n0
```

This means that for large enough input sizes, the running time of the algorithm will be at least proportional to **g(n).**

> NOTE: Big Omega notation is useful for describing the lower bound of an algorithm's running time, as it provides a guarantee that the algorithm will not perform worse than a certain level. However, it doesn't necessarily provide information about the actual performance of the algorithm, as the algorithm may still have a better performance for certain inputs. Therefore, it's important to consider other notations such as Big O and Big Theta to get a more complete picture of an algorithm's performance.

### **Big Theta Notation (Θ)**

Big Theta notation (Θ) is a way of describing the tight bound of the growth rate of an algorithm's running time as the input size approaches infinity. In other words, it describes the average-case scenario for the algorithm's performance.

Formally, if a function **f(n)** is the running time of an algorithm, then **f(n)** is said to be **Θ(g(n))** if there exist positive constants **c1, c2,** and **n0** such that for all **n** greater than or equal to **n0, f(n)** is between **c1** times **g(n)** and **c2** times **g(n)**. Mathematically, this can be expressed as:

```c
c1  g(n) <= f(n) <= c2  g(n) ; for all n >= n0
```

This means that for large enough input sizes, the running time of the algorithm will be proportional to **g(n).**

> NOTE: Big Theta notation is useful for describing the average-case performance of an algorithm, as it provides a guarantee that the algorithm will perform within a certain level. It also implies that the lower and upper bounds of the algorithm's running time are of the same order of magnitude, which is useful for analyzing the performance of the algorithm. However, it doesn't necessarily provide information about the best-case or worst-case performance of the algorithm, which is where other notations such as Big Omega and Big O are useful.

## Key Steps in finding Time Complexity

**Identify the input size**

This is the size of the input that the algorithm will process. For example, if the algorithm takes an array of size n as input, then n is the input size.

**Identify the basic operation**

This is the operation that the algorithm performs repeatedly. For example, if the algorithm loops through the array n times and performs a constant-time operation on each element of the array, then the basic operation is the constant-time operation.

**Determine the number of times the basic operation is performed**

This is the number of times the basic operation is executed in the algorithm. For example, if the algorithm loops through the array n times, then the basic operation is performed n times.

**Express the number of operations as a function of the input size**

This is the mathematical expression that describes the number of operations performed by the algorithm as a function of the input size. For example, if the algorithm loops through the array n times and performs a constant-time operation on each element of the array, then the number of operations is n multiplied by the constant time taken for each operation.

**Simplify the expression and determine the highest-order term**

This is the term with the highest power of n in the expression. This term represents the dominant factor that determines the time complexity of the algorithm.

**Express the time complexity using Big O notation**

This is the notation that describes the upper bound on the growth rate of the algorithm as the input size increases.

**Example 1**

```c
int array_example[6] = {1, 2, 3, 4, 5};
```

This initializes the array with the values 1, 2, 3, 4, and 5, respectively.

Notice that only five out of 6 slots in the array have been utilized.

Assuming we want to append an element **"3"** at the beginning of the array(at index 0), we will have to shift the initial five elements of **array\_example** to the right.

```c
Assume that: i)    1 shift to the right = 1 unit of time
            ii)    therefore, 5 shifts to the right = 5 units of time
```

After shifting, we have that:

```c
int array_example[6] = {3, 1, 2, 3, 4, 5};
```

The above action took five units of time in total.

Assuming we initially had 1, 000, 000 elements in the array, it would have taken 1, 000, 000 units of time.

> NOTE: Running time depends on the size of the input.

```c
if n = size of input ,then f(n) is a function of n and denotes the time          complexity 

In other terms: f(n) represents the number of instructions executed 
                for the input value n
```

Example 1 above can be implemented in a program with the snippet shown below.

```c

int array_example[6] = {1, 2, 3, 4, 5};
/*
 *For Loop to Shift all the five elements to the right
 */
for (int i = 4; i >= 0; i--) {
    array_example[i+1] = array_example[i];
}

/*
*Insert 3 at index 0
*/
array_example[0] = 3;
```

**Code Output**

```c
int array_example[6] = {3, 1, 2, 3, 4, 5};
```

After executing this code, the `array_example` will be `{3, 1, 2, 3, 4, 5}`.

Note that the original values in the array have been shifted to the right by one position, and the value 3 has been inserted at index zero.

**Time Complexity of the Code**

The time complexity of this code is O(n), where n is the number of elements in the array.

The ***for loop*** that shifts all the elements to the right has a time complexity of O(n), where n is the number of elements in the array. This is because, for each element in the array, we need to shift it one position to the right. Therefore, the total time required for this loop is proportional to the number of elements in the array.

The operation of inserting the new element at index 0 takes constant time, which is O(1).

Therefore, the overall time complexity of the code is O(n), which is dominated by the for loop that shifts the elements to the right.

```c
so, f(n) = n , fot the above code.
```

## **Finding f(n)**

We can compare two data structures for a particular operation by comparing their f(n) values.

We are interested in the growth rate of **f(n)** with respect to **n** because it might be possible that for smaller input sizes, one data structure may seem better than the other but for larger input sizes it may not.

This concept is applicable in comparing the two algorithms as well.

**Example 2**

```c
f(n) = 5n^2 + 6n + 12
```

In this example, we can see that:

Taking the value on **n** to be 1, for example;

```c
    for n = 1 ; % of running time for each element in the polynomial can 
                be calculated as shown below:

   5n^2 = (5/(5 + 6 + 12) * 100) = 21.74%
   6n = (6/(5 + 6 + 12) * 100)   = 26.09%
   12 = (12/(5 + 6 + 12) * 100)  = 52.17%
```

Now, taking the value of n to be 10, we can see that:

```c
    for n = 10 ; % of running time for each element in the polynomial can 
                be calculated as shown below:

   5n^2 = ((5*10^2)/(500 + 60 + 12) * 100) = 87.41%
   6n = ((6*10)/(500 + 60 + 12) * 100)     = 10.49%
   12 = (12/(500 + 60 + 12) * 100)  = 2.09%
```

**Time Complexity Explained**

* The time complexity of the function `f(n) = 5n^2 + 6n + 12` is O(n^2), where n is the input size.
    
* This is because the dominant term in the function is the term with the highest exponent of n, which is n^2. As n increases, the other terms become relatively less important compared to the n^2 term. Therefore, the time complexity of the function can be expressed as O(n^2).
    
* In other words, the time required to execute the function `f(n)` grows quadratically with the input size **n**. If we double the input size, the time required to execute the function will increase by a factor of four (2^2), since the execution time is proportional to the square of the input size.
    

> NOTE: Using the assumed values of n in the above example, we can see an interesting trend in the polynomial. See the table below.

**Table 1**

| n (arbitrary value) | 5n^2 | 6n | 12 |
| --- | --- | --- | --- |
| 1 | 21.74% | 26.09% | 52.07 |
| 10 | 87.41% | 10.49% | 2.09% |
| 100 | 98.79% | 1.19% | 0.02% |
| 1000 | 99.88% | 0.12% | 0.0002% |

```c
If you increase the value of n further, 5n^2 will clearly continue taking more time(refer to table 1 above).
Therefore, 98.88% corresponds to larger n; this therefore means that (6n + 12) can be eliminated since they contribute negligible times in the program 
Hving said that, appropriate value now is near the actual value e desire.
```

> NOTE: As said ealier in the introduction, we want to approximate the runtimes of the operations performed on data structures.We are therefore not interested in exact runtimes;Big O will help us achieve this.

**Example 3**

```c
In the example below, find if f(n) = O(g(n));

f(n) = n 
g(n) =2n
```

**Solution**

To find out whether f(n) = O(g(n)), we need to check whether there exist constants c and n0 such that

```c
 f(n) <= c * g(n) for all n >= n0.
```

In this case, we have:

```c
f(n) = n g(n) = 2n
```

So, we need to find c and n0 such that:

```c
n <= c * 2n for all n >= n0
```

Dividing both sides by 2n (which is positive for all n &gt; 0), we get:

```c
1/2 <= c for all n >= n0
```

So, we can choose any constant c &gt;= 1/2 and any n0 &gt;= 1, and the inequality will hold for all n &gt;= n0. For example, we can choose c = 1 and n0 = 1, and we get:

```c
n <= 2n for all n >= 1
```

Therefore;

```c
f(n) = n is O(g(n)) with c = 1/2 and n0 = 1 (and any larger values of c and n0 also work).
```

Therefore, f(n) = n, which means that f(n) will grow linearly.

**Example 4**

```c
Find Big O of the following function

    f(n) = 4n + 3
```

**Solution**

We need to find a constant c and a value n0 such that:

```c
|f(n)| <= c|n| for all n >= n0
```

Since **f(n) = 4n + 3** and we want to show that **f(n) is O(n)**, we can rewrite this inequality as:

```c
|4n + 3| <= c|n| for all n >= n0
```

We can simplify the left-hand side of the inequality as follows:

```c
|4n + 3| <= |4n| + |3| <= 4|n| + 3
```

Therefore, we can choose c = 5 and n0 = 1 to satisfy the inequality:

```c
|4n + 3| <= 5|n| for all n >= 1
```

This proves that f(n) = 4n + 3 is O(n) with c = 5 and n0 = 1.

> NOTE: The function f(n) = 4n + 3 is a linear function of n, which means that it grows at a constant rate as n increases. Therefore, we can say that f(n) is O(n), meaning that it grows no faster than a constant multiple of n.

**Example 5**

```c
Find Big O of the following function

    f(n) = 5n^2 + 4
```

**Solution**

```c
    Let g(n) = n^2

f(n) <= C * g(n)

Replacing the values of f(n) and g(n) in the next step

Also, let C = 6;

    5n^2 + 4 <= 6 n^2

Collecting the like terms , we have that,

4 <= 6n^2 -  f(n) = 5n^2

Therefore; 4 <= n^2 
Which can be written as ;

n^2 >= 4 ;
This now simplifies to;

n >= 2
```

This therefore means that, f(n) &lt;= C \* (g(n)), which again implies that f(n) will grow quadratically;

> NOTE: The function f(n) = 5n^2 + 4 is a quadratic function of n, which means that it grows faster than a linear function. Therefore, we can say that f(n) is O(n^2), meaning that it grows no faster than a constant multiple of n^2.

**Growth Rate of Standard Functions**

| n | log2n (log n to base 2) | n | nlog2n (n log n to base 2) | n^2 (n squared) | n^3 (n cubed) | 2 ^n (2 raised to n) |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | 0 | 1 | 0 | 1 | 1 | 2 |
| 2 | 1 | 2 | 2 | 4 | 8 | 4 |
| 4 | 2 | 4 | 8 | 16 | 64 | 16 |
| 8 | 3 | 8 | 24 | 64 | 512 | 256 |
| 16 | 4 | 16 | 64 | 256 | 4096 | 65,536 |
| 32 | 5 | 32 | 160 | 1024 | 32768 | 429 \* 10^7 |

**Example 6**

Write a program that calculates the sum of fir N integers entered by a user.

Find the time complexity of the code.

```c
#include <stdio.h>

int main() {
   int number, i, sum = 0;
   printf("Enter a positive integer: ");
   scanf("%d", &number);
   
/*
*Calculate the sum of the first N natural numbers
*/
   for (i = 1; i <= number; i++) {
       sum += i;
   }
   
   printf("The sum of the first %d natural numbers is %d\n", number, sum);
   return 0;
}
```

**Solution**

```c
variable declaration and scanf function both take constant amount of time,therefore f(n) before the for loop = 1

Lets take f(n) as n ; since the for loop runs n times

Now, after the for loop; f(n) = n + 4 

Is f(n) = O(g(n)) ? , well, let's find out
Lets take g(n) as n since n is the dorminant constant in the above function (f(n));

    f(n) <= C * g(n);
replacing the values of f(n) and g(n), we have that,

n + 4 <= C * n 
Taking C = 2 (assuming) , we have that;

    n + 4 <= 2 * n
    4 <= 2n - n ;
    4 <= n ; which can be re-written as shown below;
    n >= 4 ;

This suggests that the function grows linearly therefore f(n) = O(g(n)) pronounced as ( f(n) is big O of g(n) )
```

The time complexity of this code is O(n), where n is the input number. This is because the for loop iterates from 1 to n, and the number of iterations is directly proportional to the value of n. Therefore, as the input size increases, the time taken to execute the loop increases linearly. The other operations in the code such as input/output statements and variable initialization are constant time operations and do not affect the time complexity of the code.

**Example 7**

Find the growth rate of the following program.

```c
#include <stdio.h>

int main() {
   int number, i, sum = 0;
   printf("Enter a positive integer: ");
   scanf("%d", &number);
   
/*
*Calculate the sum of the first N natural numbers
*/
   for (i = 1; i <= number; i++) {
       sum += i;
   }
   
   printf("The sum of modified N natural numbers is %d", (number*(number + 1))/2);
   return 0;
}
```

**Solution**

The time complexity of this code is **O(1)**, which is constant time complexity. Although the input size is n (the value of the input variable "number"), the code does not directly iterate over the input size. Instead of summing the numbers from 1 to n using a loop, the code uses a closed-form formula to calculate the sum. The formula **(number\*(number + 1))/2** performs a constant number of arithmetic operations, regardless of the value of the input number. Therefore, the time taken to execute the loop is **constant** and does not depend on the **size of the input**. The input/output statements and variable initialization are also constant time operations and do not affect the time complexity of the code.

# **Guidelines for Asymptotic Analysis**

## Conditional Statements

### **"if" Statements**

**Example 1**

```c
if (condition to test/boolean expression) {
    // body of the conditional statement here
    }
```

The time complexity of a simple `if` statement is O(1), which means it has a constant time complexity. The code inside the `if` statement is executed only when the condition is true, and it is not dependent on the input size. Therefore, the time complexity of this code does not depend on the size of the input.

**Example 2**

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

The time complexity of this code is O(1). The strcmp function has a time complexity of O(n), where n is the length of the strings being compared, but since the length of "Brian" is constant and known at compile time, the time complexity of the overall program is constant.

**Prompting User for Input**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[20];
    
    printf("Please enter your first name: ");
    scanf("%s", first_name);

    if (strcmp(first_name, "Brian") == 0) {
        printf("Good morning Software Engineer!\n");
        printf("Have a lovely day!");
    }
    return 0;
}
```

The time complexity of this program is O(n), where n is the length of the input string. The complexity is dominated by the `strcmp()` function, which needs to compare each character of the input string with the characters in the string "Brian" until a difference is found or the end of the string is reached. This comparison requires iterating over each character in the input string once, giving a time complexity of O(n).

The `scanf()` function also has a time complexity of O(n), where n is the length of the input string.

### **Nested "if" statements**

**Example 1**

```c
if (condition to test/boolean expression) {
        if (boolean expression here) {
                //body of conditional statement here
             }
}
```

The time complexity of this code is O(1) or constant time. It does not depend on the size of any input, as the code only involves a conditional statement that checks for a boolean expression.

**Example 2**

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

The time complexity of the given code is O(1), which means it is a constant time algorithm.

This is because the code performs a fixed number of operations, regardless of the input size. The number of operations remains constant irrespective of the size of the input.

**Prompting User for Input**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[20];
    char middle_name[20];
    
    printf("Please enter your first name: ");
    scanf("%s", first_name);
    
    printf("Please enter your middle name: ");
    scanf("%s", middle_name);

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

The time complexity of this program is O(n), where n is the length of the input strings (first\_name and middle\_name) provided by the user. The program uses the strcmp() function from the string.h library to compare the input strings with the pre-defined strings "Brian" and "Enos". The time complexity of strcmp() is O(n), where n is the length of the longer string being compared. Since the program only performs two comparisons, the overall time complexity is O(n) where n is the length of the longest input string.

### **"if.... else" statements**

**Example 1**

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

The time complexity of this code is constant time complexity, denoted as O(1), because the code either executes the body of the `if` statement or the body of the `else` statement, but not both. The condition to test the condition is checked only once and then the program moves to either the `if` or the `else` block, depending on the result of the condition. The time required to evaluate the condition is generally negligible compared to the time required to execute the code in the `if` or `else` block. Therefore, the time complexity of this code is O(1).

**Example 2**

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

The time complexity of this code is O(1), or constant time complexity.

The code consists of a single `if-else` statement that checks if two strings (`first_name` and `middle_name`) are equal to "Brian" and "Enos", respectively, using the `strcmp()` function. Since the size of the input strings is constant and independent of the input size, the `strcmp()` function runs in constant time.

The `if-else` statement has a fixed number of statements that will be executed, regardless of the input size. Therefore, the time complexity of this code is O(1).

**Prompting User for Input**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[20];
    char middle_name[20];
    
    printf("Please enter your first name: ");
    scanf("%s", first_name);
    
    printf("Please enter your middle name: ");
    scanf("%s", middle_name);

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

The time complexity of this program is O(1). Regardless of the length of the input strings, the program performs only a single comparison operation using the `strcmp` function. Therefore, the time it takes to run the program is constant, or O(1).

### **Nested “if…. else” Statements**

**Example 1**

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

The time complexity of this code is O(1).

The code consists of a nested `if-else` statement with two conditions to be tested, but the size of the input does not affect the number of operations performed by the code. The worst-case scenario involves evaluating both `if` conditions, but the number of operations remains constant regardless of the input size.

Therefore, the time complexity of this code is O(1) or constant time complexity.

**Example 2**

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

The time complexity of this code is O(1), or constant time complexity.

The code consists of a nested `if-else` statement that checks if three strings (`first_name`, `middle_name`, and `last_name`) are equal to "Brian", "Enos", and "Otieno", respectively, using the `strcmp()` function. Since the size of the input strings is constant and independent of the input size, the `strcmp()` function runs in constant time.

The `if-else` statement has a fixed number of statements that will be executed, regardless of the input size. Therefore, the time complexity of this code is O(1), or constant time complexity.

**Prompting User for Input**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[20];
    char middle_name[20];
    char last_name[20];

    printf("Please enter your first name: ");
    scanf("%s", first_name);

    printf("Please enter your middle name: ");
    scanf("%s", middle_name);

    printf("Please enter your last name: ");
    scanf("%s", last_name);

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

The time complexity of this program is O(1) as it performs a constant number of operations regardless of the input size. The strcmp function has a time complexity of O(n), where n is the length of the strings being compared, but in this program, the length of the strings is fixed at 20 characters, so the time complexity of strcmp is also constant.

### **"else if" statements**

**Example 1**

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

The time complexity of this code is O(1).

The code consists of an `if-else` statement with three boolean expressions to be tested. The worst-case scenario involves evaluating all three boolean expressions, but the number of operations remains constant regardless of the input size.

The `if-else` statement has a fixed number of statements that will be executed, regardless of the input size. Therefore, the time complexity of this code is O(1) or constant time complexity.

**Example 2**

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

The time complexity of this code is O(1) or constant time complexity.

The code consists of an `if-else` statement with three `strcmp()` function calls to compare three string variables (`first_name`, `middle_name`, and `last_name`) with constant strings. Since the size of the input strings is constant and independent of the input size, the `strcmp()` function runs in constant time.

The `if-else` statement has a fixed number of statements that will be executed, regardless of the input size. Therefore, the time complexity of this code is O(1) or constant time complexity.

**Prompting User for Input**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[20];
    char middle_name[20];
    char last_name[20];

    printf("Please enter your first name: ");
    scanf("%s", first_name);

    printf("Please enter your middle name: ");
    scanf("%s", middle_name);

    printf("Please enter your last name: ");
    scanf("%s", last_name);

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

The time complexity of this program is O(n), where n is the length of the longest input string. The time complexity of `strcmp` function is O(n), where n is the length of the compared strings. The `scanf` function has a time complexity of O(n), where n is the length of the input string. Since the program uses `strcmp` and `scanf` functions, the time complexity of the program is O(n).

### **"switch" statements**

**Example 1**

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

The time complexity of a `switch` statement is generally considered to be O(1), or constant time complexity.

This is because the expression being tested by the `switch` statement is evaluated only once, and the execution jumps to the corresponding `case` label without the need for iteration or comparison. The number of cases does not affect the time complexity, since the expression is evaluated only once and the execution jumps directly to the appropriate case.

Therefore, the time complexity of a `switch` statement is O(1), or constant time complexity.

**Example 2**

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

The time complexity of this code is O(1). The if-else block that sets the value of the `engineer` variable has a time complexity of O(1) because it involves only a fixed number of constant-time operations (string comparisons). The switch statement that follows also has a time complexity of O(1) because it is based on the value of the `engineer` variable, which has only a fixed number of possible values. Therefore, the overall time complexity of the code is O(1).

**Prompting User for Input**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[20];
    char middle_name[20];
    char last_name[20];
    int engineer;

    printf("Please enter your first name: ");
    scanf("%s", first_name);

    printf("Please enter your middle name: ");
    scanf("%s", middle_name);

    printf("Please enter your last name: ");
    scanf("%s", last_name);

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

The time complexity of this program is O(n), where n is the length of the longest input string (i.e., the length of the last name, since it is the longest string being compared in the `if` statement). The `strcmp` function used to compare the input strings has a time complexity of O(n), where n is the length of the strings being compared.

The `switch` statement and the `printf` statements inside each case have constant time complexity and do not affect the overall time complexity of the program

### **Ternary Operator**

**Example 1**

```c
condition ? expression1 : expression2
```

The time complexity of the ternary operator `condition ? expression1 : expression2` is O(1) because it involves a simple conditional check to determine which expression to evaluate and return. It does not depend on the size of any data structure or input, and therefore the time taken to execute does not increase as the input size increases.

**Example 2**

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

The time complexity of this code is O(1) or constant time. Regardless of the values of `first_name` and `middle_name`, the code will only execute one of the two expression statements inside the ternary operator based on the result of the `strcmp()` function. Therefore, the time taken to execute the code does not depend on the input size or the number of iterations.

**Prompting User for Input**

```c
#include <stdio.h>
#include <string.h>

int main() {
    char first_name[20];
    char middle_name[20];

    printf("Please enter your first name: ");
    scanf("%s", first_name);

    printf("Please enter your middle name: ");
    scanf("%s", middle_name);

    if (strcmp(first_name, "Brian") == 0 && strcmp(middle_name, "Enos") == 0) {
        printf("Good morning Software Engineer!\n");
        printf("Have a lovely day!\n");
    } else {
        printf("We don't know you!\n");
        printf("Join us and do hard things!!\n");
    }

    return 0;
}
```

The time complexity of the program is O(n), where n is the length of the input strings (first\_name and middle\_name) since the time it takes to compare two strings using strcmp is proportional to the length of the strings being compared.

## **Loops**

### **"for" loops**

**Example 1**

```c
for (initialization; condition; increment/decrement) {
   // code block to execute while the condition is true
}
```

The time complexity of a for loop with initialization, condition, and increment/decrement is generally expressed as O(n), where n is the number of times the loop body executes. The loop body will execute until the condition is no longer true, at which point the loop will exit. The number of times the loop body executes depends on the condition and the increment/decrement. In the worst-case scenario, the loop body will execute n times, making the time complexity O(n).

**Example 2**

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

The time complexity of this code is O(n), where n is the value of `i`. The loop iterates `i` times, so the time taken by the loop is proportional to the value of `i`. Therefore, as `i` increases, the time taken by the loop also increases linearly.

**Prompting User for Input**

```c
#include <stdio.h>

int main() {
    int i;

    printf("Please enter a positive integer: ");
    scanf("%d", &i);

    for (int j = 0; j < i; j++) {
        printf(" %d " , j);
    }

    return 0;
}
```

The time complexity of this program is O(n), where n is the value entered by the user. The `for` loop iterates `n` times, printing the value of `j` each time. Therefore, the time complexity of the program is proportional to the size of the input `n`.

### Nested For Loop

**Example 1**

```c
for (initialization1; condition 1; increment/decrement1) {
   // code block to execute while  condition 1 is true
   for (initialization2; condition 2; increment/decrement2) {
      // code block to execute while  condition 2 is true
   }
}
```

The time complexity of a nested for loop with `n` iterations for the outer loop and `m` iterations for the inner loop is O(n\*m).

**Example 2**

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

The time complexity of the given code is O(i\*j) since it has two nested loops. The outer loop iterates i times, while the inner loop iterates j times for each iteration of the outer loop. Therefore, the total number of iterations of the inner loop is i \* j. if i = j = n, the the time complexity is O(n^2).

**Prompting User for Input**

```c
#include <stdio.h>

int main() {
    int i, j;

    printf("Please enter two positive integers, separated by a space: ");
    scanf("%d %d", &i, &j);

    for (int k = 0; k < i; k++) {
        for (int l = 0; l < j; l++) {
            printf("(%d %d) ", k, l);
        }
        printf("\n");
    }

    return 0;
}
```

The time complexity of this program is O(i \* j), where i and j are the two positive integers entered by the user.

The outer `for` loop will iterate i times, and the inner `for` loop will iterate j times for each iteration of the outer loop. Therefore, the inner `for` loop will iterate a total of i *j times, resulting in a time complexity of O(i* j).

This is because the time complexity of nested loops is equal to the product of the number of iterations of each loop. In this case, the outer loop has i iterations and the inner loop has j iterations, so the total time complexity is O(i \* j).

### **"while" loops**

**Example 1**

```c
while (condition to test here) {
   // code block to execute while the condition is true
}
```

The time complexity of a `while` loop depends on the condition being tested. If the condition always evaluates to true, then the loop will execute indefinitely and the time complexity will be infinite. However, if the condition eventually becomes false, then the time complexity will depend on the number of iterations required to reach that point. Therefore, the time complexity of a `while` loop is generally expressed as O(n), where n is the number of iterations required to exit the loop.

**Example 2**

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

The time complexity of this code is O(n), where n is the value of `i` (in this case, 5). The `while` loop will iterate `i` times, incrementing `j` with each iteration until `j` is no longer less than `i`.

**Prompting User for Input**

```c
#include <stdio.h>

int main() {
    int i, j = 0;

    printf("Please enter a positive integer: ");
    scanf("%d", &i);

    while (j < i) {
        printf(" %d ", j);
        j++;
    }

    return 0;
}
```

The time complexity of this program is O(i), where i is the user-input positive integer.

The `while` loop will iterate i times, printing out the value of j each time. The time it takes to execute the loop is proportional to the value of i, since the number of iterations is directly determined by the value of i.

Therefore, the time complexity of this program is linear in terms of **i**, or **O(i)**.

### **Nested “while” Loop**

**Example 1**

```c
while (condition 1 to be tested here) {
   // code block to execute while the condition 1 is true
   while (condition 2 to be tested here) {
      // code block to execute while the condition 2 is true
   }
}
```

The time complexity of a nested while loop with condition 1 and condition 2 is O(n \* m), where n is the number of times condition 1 is executed and m is the number of times condition 2 is executed within each iteration of the outer loop.

**Example 2**

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

The time complexity of the nested while loop in this program is O(N^2), where N is the value of the variable "i" (or equivalently, "j").

The outer while loop executes "i" times, and for each iteration of the outer loop, the inner while loop executes "j" times. Therefore, the total number of iterations of the inner loop is equal to i *j. Since the program prints a message for each iteration of the inner loop, the total number of messages printed is also i* j.

> NOTE: When the values of i and j are both large, the time complexity of this program can become quite high, so it is important to be careful when using nested loops in this way.

**Prompting User for Input**

```c
#include <stdio.h>

int main() {
    int i, j, k = 0, l = 0;

    printf("Please enter two positive integers, separated by a space: ");
    scanf("%d %d", &i, &j);

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

The time complexity of this program is O(i \* j), where i and j are the user-input positive integers.

The outer `while` loop will execute i times, and the inner `while` loop will execute j times per outer loop iteration. Therefore, the total number of iterations of the inner loop is **i \* j**.

Within each inner loop iteration, a constant amount of work is performed, consisting of printing out the coordinates and incrementing the `l` variable. Therefore, the time complexity of each inner loop iteration is O(1).

> Overall, the time complexity of this program is O(i \* j), which represents the total number of iterations of the nested `while` loops.

### **"do……. while" loops**

**Example 1**

```c
do {
   // code block to execute at least once
} while (condition);
```

The time complexity of a do-while loop depends on the number of iterations required to satisfy the condition. In the worst case, the loop will execute the code block once and then check the condition, resulting in a time complexity of O(1). However, in the best case, the loop may execute many times, resulting in a time complexity of O(n). Therefore, the time complexity of a do-while loop cannot be determined without knowing the specific conditions under which it will execute.

**Example 2**

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

The time complexity of the do-while loop is O(n) since the loop body will always execute at least once and then execute n-1 more times if the condition is true, where n is the value of `i` in this case. Therefore, the time complexity of the given code is O(n).

**Prompting User for Input**

```c
#include <stdio.h>

int main() {
    int i, j = 0;

    printf("Please enter a positive integer: ");
    scanf("%d", &i);

    do {
        printf(" %d ", j);
        j++;
    } while (j < i);

    return 0;
}
```

The time complexity of this program is O(i), where i is the user-input positive integer.

> The `do-while` loop will iterate **i** times, printing out the value of **j** each time. The time it takes to execute the loop is proportional to the value of **i**, since the number of iterations is directly determined by the value of i.

Therefore, the time complexity of this program is linear in terms of **i,** or **O(i).**

### **Nested “do…. while” Loops**

**Example 1**

```c
do {
   // code block to execute at least once
   do {
      // code block to execute at least once
   } while (condition 2 to test here);
} while (condition 1 to test here);
```

The time complexity of a nested do-while loop with conditions to test in both loops is determined by the number of iterations in each loop.

Assuming the number of iterations in the inner do-while loop is m, and the number of iterations in the outer do-while loop is n, the total number of iterations will be n\*m.

Thus, the time complexity of the nested do-while loop can be expressed as O(nm).

**Example 2**

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

The time complexity of the nested do-while loops in the given code is O(i \* j), where i is the value of `i` and j is the value of `j`.

The outer loop executes i times, while the inner loop executes j times for each iteration of the outer loop. Therefore, the total number of iterations of the inner loop is i *j. Since the code block inside the inner loop has a constant time complexity, the overall time complexity of the nested do-while loops is O(i* j).

**Prompting User for Input**

```c
#include <stdio.h>

int main() {
    int i, j, k = 0, l = 0;

    printf("Enter the value for i: ");
    scanf("%d", &i);
    printf("Enter the value for j: ");
    scanf("%d", &j);

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

The time complexity of this code is O(i\**j).*

> *where i and j are the values inputted by the user. The outer do-while loop iterates* ***i*** *times and the inner do-while loop iterates* ***j*** *times for each iteration of the outer loop. Therefore, the total number of iterations is* ***i \* j****. Each iteration of the inner loop performs a constant amount of work, so the overall time complexity can be expressed as* ***O(i\**j).**

## **Functions**

### **Example 1**

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

The time complexity of the `skiplines()` function is O(n), where n is the value of the `number` parameter passed to the function. The for loop in the function will iterate `number` times, and each iteration takes a constant amount of time. Therefore, the time complexity of the function is proportional to the value of `number`, and can be expressed as O(number).

**Prompting User for Input**

```c
#include <stdio.h>

void skiplines(int number);

int main() {
    int num_lines;

    printf("Enter the number of lines to skip: ");
    scanf("%d", &num_lines);

    printf("My name is Brian Enos Otieno\n");
    skiplines(num_lines);
    printf("I am a software Engineer \n");
    skiplines(num_lines);
    printf("Programming is co cool!, join me and #DoHardThings\n");

    return 0;
}

void skiplines(int number) {
    for (int h = 1; h <= number; h++) {
        printf("\n");
    }
}
```

The time complexity of this code depends on the value entered by the user for num\_lines. The skiplines() function has a time complexity of O(number), where number is the value of num\_lines entered by the user. The loop in the skiplines() function will iterate number times, and each iteration takes a constant amount of time. Therefore, the time complexity of the skiplines() function is proportional to the value of number, and can be expressed as O(number).

Overall, the time complexity of the main function will also be O(number), as it calls the skiplines() function twice with the same value of num\_lines. Therefore, the time complexity of the entire program is O(number).

### **Example 2**

**Prompting User for Input**

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

The time complexity of this code is constant or O(1) because the function `sum` performs a single operation (addition) and returns the result. The input size does not affect the execution time of the function, so the time complexity is not dependent on the input size. The `main` function also performs a constant number of operations regardless of the input size, so the overall time complexity of the code is also constant.

### **Example 3**

**Prompting User for Input**

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

The time complexity of this code is O(n), where n is the number of characters inputted by the user. The while loop in the main function will iterate over each character until it reaches the newline character '\\n', which takes a constant amount of time to process each character. Within the loop, the position() function is called, which has a constant time complexity for each character. Therefore, the overall time complexity is proportional to the number of characters, which is O(n).

### **Example 4**

**Prompting User for Input**

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

The time complexity of this code is O(1), which means it takes a constant amount of time to execute regardless of the size of the input. The reason for this is that the sum function only performs a single operation, which is the addition of two numbers. This operation takes a constant amount of time, regardless of the size of the numbers being added. Similarly, the input reading and output writing operations in the main function take a constant amount of time, which also makes the overall time complexity of the code O(1).


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
