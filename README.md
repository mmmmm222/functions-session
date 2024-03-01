# functions-session

* Factorial

~~~
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
~~~

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