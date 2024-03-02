```C
#include <stdio.h>

void sum(void);

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