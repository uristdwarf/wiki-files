This article will follow the style of the book \"The C Programming
Language\" (a.k.a \"K&R\"), though a lot of projects use their own
styles (for example, the Linux kernel style
[uses](https://en.wikipedia.org/wiki/Indentation_style#Variant:_Linux_kernel)
8 spaces instead of 4 for indentation)

## Simple Hello World {#simple_hello_world}

``` c
/*
Multiline comments are written like this
*/

// Tell the compiler to include the standard input/output library.
#include <stdio.h>

// Define a function called main. main is a special function that your program will enter when compiled and executed
// the 'int' at the beginning tells the return value of the function will be of type int
int main()
{
    // Call function printf and supply it with a value
    printf("hello world\n"); 
    // When no return value is given in main, 0 will be returned.
}
```

## Variables

### Declaring variables and basic data types {#declaring_variables_and_basic_data_types}

You can declare variables either globally or in functions

``` c
int integer; // Integer
float floating; // floating point
char c; // single character, 1 byte
short sint; // smaller int (maximum/minimum size depends on system)
double dfloat; // double precision float

int main()
{
    int integer2;
}
```

### Assigning variables {#assigning_variables}

You can assign variables when declaring them or after they\'ve been
declared.

``` c
#include <stdio.h>

int integer;
float floating = 4.2; // floating point

int main()
{
    integer = 4; // You can also assign another variable
    printf("%f\n", floating);
    printf("%i\n", integer);
}
```

## Loops

### While-loop {#while_loop}

``` c
// Print numbers 1 to INTCOUNT
#include <stdio.h>

const int INTCOUNT = 10; // Constant declaration

int main() 
{
    int i = 1;
    while (i <= INTCOUNT) {
        printf("%i\n", i);
        ++i; // You can also write it as i++
    }   
}
```

### For-loop {#for_loop}

``` c
// Same as above, but using for
#include <stdio.h>

const int INTCOUNT = 10; // Constant declaration

int main() 
{
    for (int i = 1; i <= INTCOUNT; ++i) // You don't need to use braces for single line statements
        printf("%i\n", i);
}
```

### Do-loop {#do_loop}
