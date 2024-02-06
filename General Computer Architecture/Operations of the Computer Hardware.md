Assembly programming languages such as MIPS, Intel x86, and ARM have a strict notation of performing only one operation at a time.

For example, to add two numbers together and store the value into a variable we do this:

```
add a, b, c
```
However when we try to do more complicated operations such as f = (g + h) - (i + j); we would have to do this:

```
add t0, g, h # t0 is a temporary variable
add t1, i, j # t1 is a temporary variable to store the value of i + j
sub f, t0, t1
```
*# is a comment in MIPS assembly*

Assembly is a bare bones programming language that provides the closes level to machine code that is human readable allowing for more speed in our code, but less abstraction for computational task.

#computerorganization #assembly #MIPS 