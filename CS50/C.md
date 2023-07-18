the stdio.h header defines three variable types, macros and functions for performing input and output I/O
```c
#include <stdio.h>
```
i needs to be required at the top of the document in order to be able to use functions such as 
```c
printf("");
```

functions

```c
if (x < y)
{
	printf("x is less than y\n");
}
else if (x > y)
{
	printf("x is not less than y\n");
}
else
{
	printf("x is equal to y\n");
}
```

double quotes for strings
single 
quotes for chars 
```c
int main(void)
{
    char c = get_char("do you agree? ");
    if (c == 'y')
    {
        printf("agreed.\n");
    }
```

variables
```c
int counter = 0; //int or string when you initialise it for the first time
counter = counter + 1;
counter += 1; //is the same as above
counter++; //the same as above

counter--; //decrement by 1
```

while loops to action the same function a specified number of times

```c
int i = 3;
while (i > 0)
{
	printf("meow\n");
	i--;
}

//int is is the number of times the function while should run, the while will run for as long as i is more than 0, each time it will print a meow and decrement the int i by 1
```

you should always aim to start counting at 0, so the above is correct however it should be rewritten
```c
int i = 0;
while (i < 3)
{
	printf("meow\n");
	i++;
}
```

alternative to while loops are for loops 
```c
for (int i = 0; i < 3; i++)
{
	printf("meow\n");
}
//loop that will go on forever will be
while (true)
{
	printf("meow\n");
}
```

clang is the compiler that works with C -> when hitting "make" clang for (c-language) will compile the machine language file

use `%s` in c to replace with any variable you collected (it's a placeholder
```c
string name = get_string("What's your name? ");
printf("hello, %s\n", name);
```

compiling (make)
1. prepocessing 
```c
#include <cs50.h>
// temporary placeholders for the global find and replace e.g. if you use 
string name = get_string(""); 
//it will look up cs50 library and find the blovk of code associated with this prompt
```
2. compiling
assembly language that is very familiar to the machine, machine language 
3. assembling
once the code is compiled and translated into assembly language it is then converted into binary 0s and 1s machine code 
4. linking
hello.c cs50.c and stdio.c (takes source code, author's of C's code and machine code  to implement it together)

**debugging**
- printf
- debugger
- rubber duck

data types in C:
- bool
- int
- long
- float
- double
- char
- string /0

```c
int main (void); //takes no arguments

int main(int argc, string argv[]); 
int argc //argument count
string argv //
```
A main() function can be called using command line arguments. It is a function that contains two parameters, integer (int argc) and character (char *argv) data type. The argc parameter stands for argument count, and argv stands for argument values.