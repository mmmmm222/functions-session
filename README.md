# functions-session
<p>&nbsp;</p>

## Table of Contents

- [Functions](#functions)
- [Recursion](#Recursion)
- [passing arguments](#passing-arguments)

<p>&nbsp;</p>



### Functions
> A function in C is a block of code that performs a specific task and is used to break down a program into  smaller, reusable pieces. It is defined with a name, a return type, and a set of parameters that specify the  input values.

<p>&nbsp;</p>

- start with the example

<p>&nbsp;</p>


- Syntax:

  - The syntax of function can be divided into 3 aspects:

  >  `1- Function Declaration`
      `2- Function Definition`
      `3- Function Calls`


- Function Declaration

<img src = "https://github.com/mmmmm222/functions-session/assets/95083236/6b7123bb-059d-43bb-a7d0-bc6853927e1b" width ="800" height = "500" >


- Function Definition

  ```C
      return_type function_name(parameter1, parameter2, ...) {

          // Code that performs a specific task

          // Return statement
          return result;
      }
  ```

  for example:

  ```C
      int add(int a, int b) {
          int result = a + b;
          return result;
      }

      int main(){
          int x = 11;
          int y = 12;

          printf("%d\n", add(x,y));
      }
  ```

<p>&nbsp;</p>

- solve from `1` to `7`

<p>&nbsp;</p>

- Applications:

  - Range Prime Checker Function:

    prototype :

          bool isPrime(int);

    body :

    ```C
        bool isPrime(int x){
            if(x < 2)
                return false;
            for(int i = 2;i < x;i++){
                if(x % i == 0)
                    return false;
            }
            return true;
        }
    ```

    usage:

    ```C

        // Calculate The number of primes in Range from Left to Right

        int left,right;
        scanf("%d%d",&left,&right);
        int primeNumbers = 0;
        for(int i = left;i <= right;i++){
            if(isPrime(i))
                primeNumbers++;
        }
        printf("The number of Primes in Range [%d : %d] = %d",left,right,primeNumbers);


    ```

  - Power Function: => Think how to do it in 5 minutes

    prototype :

          int power(int,int);

    body :

    ```C
        int power(int b,int p){
            int result = 1;
            while(p--){
                result *= b;
            }
            return result;
        }
    ```

    usage:

    ```C

        // Evaluate This Function (F) for any value of (x)
        // F(x) = 11 * (x ^ 4) - 3 * (x ^ 3) + 12 * x  - 25

        int x;
        scanf("%d",&x);

        int result = 11 * power(x,4) - 3 * power(x,3) + 12 * x - 25;

        printf("F(%d) = %d",x,result);


    ```

  - Factorial

    ```C
        #include <stdio.h>

        double factorial(int x);

        void main(void)
        {
            int s = factorial(5);
            printf("%d", s);
        }

        double factorial(int x)
        {
            int f = 1;
            for (; x > 0; x--)
                f *= x;
            return f;
        }
    ```
<p>&nbsp;</p>

- solve `7` `8` `9`


### Recursion:

> Defining a problem in terms of itself.

for example:
 
  ```C
     int factorial(int n) {
         if (n == 0) {
             return 1;
         }
         else {
             return n * factorial(n-1);
         }
     }
  ```
 
 Let's see how this function works for the input `n = 5` :
 
     factorial(5)    = 5 * factorial(4)
                     = 5 * 4 * factorial(3)
                     = 5 * 4 * 3 * factorial(2)
                     = 5 * 4 * 3 * 2 * factorial(1)
                     = 5 * 4 * 3 * 2 * 1 * factorial(0)
                     = 5 * 4 * 3 * 2 * 1 * 1
                     = 120



<p>&nbsp;</p>

- solve `10`

<p>&nbsp;</p>

### passing arguments

   - We can pass arguments to the C function in two ways:

>  `1- Pass by Value`     `2- Pass by Reference`

<p>&nbsp;</p>

* `Pass by Value`

>  Parameter passing in this method copies values from actual parameters into formal function parameters. As a result, any changes made inside the functions do not reflect in the caller’s parameters. 

Example :

```C

#include <stdio.h>

void swap(int var1, int var2)
{
int temp = var1;
var1 = var2;
var2 = temp;
}

int main()
{
int var1 = 3, var2 = 2;
printf("Before swap Value of var1 and var2 is: %d, %d\n",var1, var2);
swap(var1, var2);
printf("After swap Value of var1 and var2 is: %d, %d",var1, var2);
return 0;
}

```
<p>&nbsp;</p>

* `Pass by Reference`

>  The caller’s actual parameters and the function’s actual parameters refer to the same locations, so any changes made inside the function are reflected in the caller’s actual parameters. 

Example :

```C

#include <stdio.h>

void swap(int *var1, int *var2)
{
int temp = *var1;
*var1 = *var2;
*var2 = temp;
}

int main()
{
int var1 = 3, var2 = 2;
printf("Before swap Value of var1 and var2 is: %d, %d\n", var1, var2);
swap(&var1, &var2);
printf("After swap Value of var1 and var2 is: %d, %d", var1, var2);
return 0;
}

```