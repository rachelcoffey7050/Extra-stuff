# Introduction
## Jan 9
We need others in our lives to become perfected. We will need help and we need to help others. You are not going to learn all you can if you are not part of the class community.
- participate in class (be engaged)
- offering help to others
- ask for help when needed
### The terminal
Can use VS Code if you want but don't have to. Goal is to become comfortable with just a terminal.
- ssh rcc934@schizo.cs.byu.edu 
- Then type password
See [lab 1 instructions](https://bitbucket.org/byucs224/byu-cs-224-labs/src/master/1-Linux-Systems/linux-systems.md) for details on how to work in the command line.
The command line has all the functionality. Interfaces may look easier, but they are limited in functionality. The goal of this class is to make you a "power user" - use more than the basic interface.
When you use nano to edit a file, you can use ctrl z to suspend it, and then fg to go back in. 
Be flexible, able and willing to use code and technology in multiple ways. Learn to be happy with whatever tool is in front of you. That includes using the command line.
### Compiling
gcc -o hello hello.c renames the file instead of the default a.out
-Wall sniffs the code for stuff that smells weird (warn all)

## Jan 12 - Memory
Remember command line arguments.
### C
To declare: 
- unsigned short name = 42;
- unsigned ui = 43; (int)
- unsigned long ul = 44;
- char str[] = "Hello world"
printf("unsigned short: %hu\n", us); This works sorta like an f string in python where % acts as a placeholder for variable as second parameter. the hu means short unsigned. Look up which sign to use when you need it. u, lu, s: number, long, string.
In C, strings are read at a certain address. It reads until it sees a null character (0). This is called null-terminated. This is the number 0, not the character.
### Memory
In C everything is done in bytes (size). A byte is 2 nibbles which is 4 bits (1s and 0s). 1011 0011 is one byte, 2 nibbles, 8 bits.
everything is in base 16 0-9 and A-F. A-f can be lower or upper case. One nibble has 16 pieces of information that it holds. (2^4) This is called positional notation.

1011 0011 -> b3. 

sizeof(ui) - tells you how much memory is allocated. 

A short is 2 bytes. an unsigned is four bytes and a long is eight bytes. 

The size of a string varies on the length of the string. The size is len + 1 for the null character.

Overflow: when the number gets to big and it wraps around, leaving you with a negative number. 

Use & to get where exactly in memory it is stored.

Memory is a giant array. index increases as we go up and left (starting in bottom right corner).

Endian - name come from Gulliver's travels. In the novel, the endians like boiled eggs but have a quarrel about which end to crack. CS had the same fight - but currently we start with the least number ie 3 in 123. Little endianess.
write a number with 0x to not have to convert.

### Terminal Help
instead of running program (types) write types > out.txt and then use code out.txt to view. 
Use ! to pull up repeated commands. Use !758 to get a specific command (use history to see) and !gcc to fill in the rest of a command you used recently.

## Jan 14

### More About Memory
%p indicates a pointer address. A string is an array of characters, so an address in memory, so it does not need the & in printf. other times you have a pointer, you need &. 0x indicates this is an address (which you are storing at a different address).

Crack the little end of the egg (least significant byte (LSB) comes first). Except for strings, which are read forwards. This is because they are arrays with no ordering -> the pointer points to the first character which is one byte. You add to move through the array. Strings end in 00, which is part of the size but not the length. In hex, this indicates stop.

0xdeadbeef reads in memory as ef -> be -> ad -> de (hex).

```
int main(int argc, char *argv[]) {
    unsigned ui = 0xdeadbeef
    string str = "Hello world!" //not sure this is correct
    unsigned long ul = 0x0047464544434241 // also not sure but more sure
    
    printf("ui = %#x\n", ui);
    printf("&ui = %p\n", &ui);
    printf("str = %p\n", str);
    printf("&ul = %p\n", &ul);

    printf("(char *)&ul = %s\n", (char *)&ul);
    printf("*(int *)str = %#\n", *((int *)str)0; // when we code we are telling the machine how to interpret memory

    //
    output:
    ui = 0xdeadbeef
    &ui = (address)
    str = (address)
    &ul = (address)
    (char *)&ul = ABDCDEFG
    *(int *)str = 0x6c6c6548 (only 8 digits becuase that is amount of bytes)
    //
    
    scanf("%lx", (unsigned long*)(str+9)); // a long in hex is being taken in and goes to the memory location of str+9 which is unsigned long.
    printf("str = %s\n", str); //prints the string
    printf(ui = %#x\n", ui);

    //output
    str = Hello worFEDCBA // this is because we overwrote it with 0041424344454647
```
If you add one to a pointer, it thinks you want the second thing, as if this were an array of integers.

## Jan 16

### Do-While loops
```
do{
} while(x)
```
does the code first, then checks the condition to know if it should continue.
### Basic types from quiz
In this class there are three basic data types we will work with in C:

1. Integers

2. longs (like an integer but can be larger in absolute value)

3. Characters (single ascii characters like 'a', '1', or '?')

Unlike in C++, C does not have a string data type. Instead of strings, C uses arrays of type char.

C also does not have a bool type. Instead of using the Boolean True or False, C uses 0 as false, and not 0 (default 1) as true. So any math in an if statement or other conditional statement is looking to see if the value it is checking is 0 (false) or not 0 (true). Any conditional statements that use >,<,>=,<=,== act the same as in C++ but remember they are not resolved into a true or false, but a 1 or 0. 
    
### Scanning and Printing from quiz

In C the way we read and print from/to standard in (stdin) is using scanf and printf statements. 

These statements have the following format:

scanf("format string", address of variables);

printf("format string", variable names);

What are format strings? They are a % followed by a character that denotes the type of data you are trying to scan or print. Any format strings will be associated with a variable on the right side of the statement. The scanf statement requires addresses of variables (use &x to get the address of x) you want to set to the scanned value.

Common format strings include:

%d for decimals (ints)

%c for characters

%s for strings (remember there is no string type. We will talk more about this later)


Statement examples:

scanf("%d", &x);    (scans an integer and sets the value of x to that integer)

scanf("%d %c", &num, &letter);    (scans a decimal into num and a char into letter)

printf("this is the value of x: %d", x);    (would print out "this is the value of x: #" where '#' is the value of x)

printf("letter:number - %c:%d", letter, num);    (would print out "letter:number - A:#" where 'A' is the value of letter and '#' is the value of num)

### Arrays and "strings" from quiz

We declare arrays in C the same way we do in C++. However, C does not keep track of the size we declared for an array. This is a fact we will learn more about and learn to exploit later in the class.

Since C does not have a string type we use char arrays to hold groups of characters. When a scanf or printf statement uses the afore mentioned %s format string then you need to give it a character array as the associated variable, scanf will then input the string into the array up to the first white space. (side note about arrays and scanf: because of the way arrays work in C you do not need to put a '&' in front of an array name in the scanf statement to get the address of the array. You can think of an array variable as a "pointer" to the start of the array so it is already an address)

### Fun (?) - example from lab 2

```
#include <stdlib.h>
#include <stdlib.h>

int main(int argc, char*argc[]) {
    int inputs[5] = {0,0,0,0,0}; //you can initialize it either way
    int i = 0; //traditionally, declare all your variables up front

    scanf("%d %d %d %d %d", inputs, inputs+1, inputs+2, inputs+3, inputs+4); //you can also take the address using &inputs[1]

    for(i=0; i<sizeof(inputs)/sizeof(int); ++i) {
        printf("inputs[%d] = %d\n", i, inputs[i]);
    }
    return 1;
}
```

Then compile, consider using: `gcc -Wall -g -o fun fun.c`. The -g sets up the debugger. The -o fun renames the out file.
remember, you can give it input with `fun < input.txt` or try `cat input.txt | fun`. If the current directory is not in your search path, use `./fun`.

### Debugger gdb

To turn on the debugger: `gdb fun` and `quit` to get out. To make your up and down arrows work in command prompt window use `focus cmd`. Add a break point with `break 22` where 22 is the line number. Type 'run' to run the program. `p /s value` will print the desired value at the point you want. `x /x` is the actual contents of memory (addresses). `n` steps forward. 'c' is continue.

### Less fun example
Say in the above code you chance it to:
```
int *inputs = NULL;

//then add
int num_inputs = 0
if (argc != 2) {
    return 1;
}
printf("argv[0] = %s\nargv[1] = %s\n", argv[0], argv[1]);
num_inputs = atoi(argv[1]);

inputs = malloc(num_inputs * sizeof(int));

for (i=0, i < num_inputs; i++){
    scanf("%x, inputs+i);
}

for(i=0; i<sizeof(inputs)/sizeof(int); ++i) {
        printf("inputs[%d] = %d\n", i, inputs[i]);
    }

printf("inputs[%d] = %d\n", i, inputs[i]);
// what numbers can you input that will output "hello world" when they are transformed to characters above.
free(inputs); //what you malloc you should free)
```
DRAW MEMORY. So you understand what is going on.
