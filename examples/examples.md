## Examples

```C
// assume we need to make a code that adds two numbers

#include <stdio.h>

void main(void)
{
    int num1, num2, sum;
    scanf("%d %d", &num1, &num2);
    sum = num1 + num2;
    printf("sum is %d\n", sum);
}


```

```C
#include <stdio.h>

void add(void);

void main(void)
{
    add();
    add();
    add();
}


void add(void)
{
    int num1, num2, sum;
    scanf("%d %d", &num1, &num2);
    sum = num1 + num2;
    printf("sum is %d\n", sum);
}

```

```C
#include <stdio.h>

void add(int num1, int num2);

void main(void)
{
    int num1, num2, sum;
    scanf("%d %d", &num1, &num2);
    add(num1, num2);
}

void add(int num1, int num2)
{
    int sum = num1 + num2;
    printf("sum is %d\n", sum);
}

```

```C
#include <stdio.h>

int add(int num1, int num2);

void main(void)
{
    int num1, num2, sum;
    scanf("%d %d", &num1, &num2);
    sum = add(num1, num2);
    printf("sum is %d\n", sum);
}

int add(int num1, int num2)
{
    int sum = num1 + num2;
    return sum;
}

```



## Think

`1`

```C
#include <stdio.h>

int fun(int);

void main(void)
{
    int x, y, z;
    x = fun();
}

int fun(int)
{
    printf("Help");
}

```

`2`


```C
#include <stdio.h>

int fun(int);

void main(void)
{
    int x, y, z;
    x = fun(y);
}

int fun(int)
{
    printf("Help");
}

```

`3`

```C
#include <stdio.h>

void fun(void);

void main(void)
{
    int x, y, z;
    fun(y);
}

void fun(void)
{
    printf("Help");
}

```

`4`

```C
#include <stdio.h>

void fun(int);

void main(void)
{
    int x, y, z;
    fun();
}

void fun(int)
{
    printf("Help");
}

```
`5`

```C
#include <stdio.h>

void fun(int);

void main(void)
{
    int x, y, z;
    fun(x, y, z);
}

void fun(int)
{
    printf("Help");
}

```
`6`

```C
#include <stdio.h>

void fun();

void main(void)
{
    int x, y, z;
    fun(x, y, z);
}

void fun()
{
    printf("Help");
}

```

`7`

```C

#include <stdio.h>

int fun(int i)
{
    i++;
    return i;
}

int main()
{
    int fun(int);
    int i = 3;
    fun(i = fun(fun(i)));
    printf("%d\n", i);
    return 0;
}

```
`8`

```C
#include <stdio.h>
#include <stdlib.h>

int main()
{
    int i = 0;
    i++;
    if (i <= 5)
        printf("Luminous");
    exit(1);
    main();
    return 0;
}
```

`9` `ask all of them`

```C
#include <stdio.h>
function();

main()
{
    int i = 5;
    i = function();
    printf("%d", i);
    return 0;
}

function()
{
    int a;
    a = 250;
}
```

## recursion

`10`

```C
#include <stdio.h>
int sumdig(int);
int main()
{
    int a, b;
    a = sumdig(123);
    b = sumdig(321);
    printf("%d, %d\n", a, b);
    return 0;
}

int sumdig(int n)
{
    int s = 0, d = 0;
    if (n != 0)
    {
        d = n % 10;
        n = n / 10;
        s = d + sumdig(n);
    }
    else
        return 0;
    return s;
}


```


## calling

`11`
```C
#include <stdio.h>
void fun(int x)
{
    x = 30;
}
int main()
{
    int y = 20;
    fun(y);
    printf("%d", y);

    return 0;
}

```

`12`
```C
#include <stdio.h>
void fun(int *ptr)
{

    *ptr = 30;
}

int main()
{
    int y = 20;
    fun(&y);
    printf("%d", y);
    return 0;
}
```

`13`
```C
#include <stdio.h>
#include <stdlib.h>

void swap(int *a, int *b);
int main()
{
    int a, b;
    a = 10, b = 15;
    swap(&a, &b);
    printf("%d %d", a, b);
    return 0;
}

void swap(int *a, int *b)
{
    int temp = *a;
    *a = *b;
    *b = temp;
}

```
`14`

```C
#include <stdio.h>
#include <stdlib.h>

void swap(int a, int b);
int main()
{
    int a, b;
    a = 10, b = 15;
    swap(a, b);
    printf("%d %d", a, b);
    return 0;
}

void swap(int a, int b)
{
    int temp = a;
    a = b;
    b = temp;
}

```

`15`

```C
#include <stdio.h>
#include <stdlib.h>

void swap(int a, int b);
int a, b;
int main()
{

    a = 10, b = 15;
    swap(a, b);
    printf("%d %d", a, b);
    return 0;
}

void swap(int a, int b)
{
    int temp = a;
    a = b;
    b = temp;
}
```