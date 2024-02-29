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