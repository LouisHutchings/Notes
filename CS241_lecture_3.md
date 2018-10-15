# CS241 Operating Systems Lecture 3
## *Introduction to C*
*4/10/18*

### What is C?
> C is a low-level systems programming language
Operating systems, drivers, embedded systems etc.

### Comparison with Java
* Comments are the same.
* Import additional functionality with ```#include``` .
* C has conditional compilation.
* C does not have Objects.
* Signed and unisgned types are available in C.
* No boolean types, typically an integer where ```0``` is false and anything else is true is used.
* Entry point is
```C
int main(int argc, char *argv[])
```
* In C functions must be defined before they are called, or a function prototype must be defined
* ```printf()``` is used instead of System.out.println(). % signs are used for formatting e.g %d integers, %f floating point numbers, %s character strings.
* Control flow is the same except brackets are always necessary around if statements
* ```Const``` used instead of ```Final```
* C has no inline type declaration in loops
* Arrays in C have no size infromation (hence why there are two arguments for main)

### Compilation
> \> gcc main.c -o [output filename]
<br>Produces an executable binary application.   

The C Compiler gives a lot more control over compilation than Java. A **makefile** is used to provide compilation instructions. This will not be necessary for the coursework.

### Structs
> Composition of primitive types

Used in system calls to return multiple values

**Example**
```C
#include <stdio.h>
struct point {                                                
  int x;                                                    
  int y;  
};
int main(int argc, char *argv[]){
struct
 point a;                                           
    a.x = 3;
    a.y = 4;
    printf("Point(%d, %d)", a.x, a.y);                        
return 0;  
}
```
Bit Fields allow

### Pointers
> A pointer is a variable that holds a memory address
