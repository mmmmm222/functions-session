# functions-session
<p>&nbsp;</p>

## Table of Contents

- [Functions](#functions)


### Functions
> A function in C is a block of code that performs a specific task and is used to break down a program into  smaller, reusable pieces. It is defined with a name, a return type, and a set of parameters that specify the  input values.

<p>&nbsp;</p>

- Syntax:

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

  - Power Function:

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


<p>&nbsp;</p>

* Factorial Example

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

* pointer Size

~~~
According To Address Bus
(64 bit) or (32 bit)
~~~

* pass by value vs pass by reference

~~~

~~~

* Register keyword

Register variables in C are those variables that are stored in the CPU register instead of the conventional storage place like RAM. Their scope is local and exists till the end of the block or a function.

~~~
#include <stdio.h>

register int var = 22;

int main()
{
    printf("Value of Register Variable: %d\n", var);
    return 0;
}

// error
~~~

~~~
#include <stdio.h>

int main()
{
    register int var = 22;
    printf("Value of Register Variable: %d\n", var);
    return 0;
}
// ok
~~~

* extern Keyword
~~~
- External variables in C can be shared between multiple C files. We can declare an external variable using the extern keyword.

- Their scope is global and they exist between multiple C files.
~~~


* Automatic Variable in C
~~~
All the local variables are automatic variables by default. They are also known as auto variables.

Their scope is local and their lifetime is till the end of the block. If we need, we can use the auto keyword to define the auto variables.

The default value of the auto variables is a garbage value.
~~~