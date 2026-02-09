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

## Jan 21 - Prepare for Project 1

### xxd
Project 1 is to imitate behavior of xxd. Use xxd to figure out correct output and then test it. Implement both bits and hex.

All this information is in the write up so don't worry.

xxd - a program that outputs raw data. It takes a file (any type), opens it, and reads bytes. Outputs as Hex or binary. 
Made out of segments. `ctrl d` gets you out of interactive mode - means end of input. `ctrl c` on the other hand sends `sig kill` to shut down a running process. 
- Seg 1: `00000010:` - an index into an array of bytes. 16 base 10.
- Seg 2: hex - `7574 2064....` 
- Seg 3: `This is some inp`

echo - `"echo this" | xxd` Use piping to give input, do small tests on your program.  

cat - reads file pipes it `cat xxd | myxxd.md`

or `xxd < myxxd.md`

You need some way to compare your output with xxd's. Use `diff`. It takes two files and compares to see if they are the same byte for byte. 
No output = they are the same. 

To see large output, pipe it into `less` so you can scroll up and down.

You need a function that takes byte and gives a string of ones and zeros - bytes to bits. 
Algorithm: 13 -> 13%2 = 1 -> 13/2 = 6 -> 6%2 = 0 -> 6/2=3 -> 3%2=1. So answer is reversed - 01101

## Jan 26

Homework is on interpreting memories. It will draw it in a variety of ways and directions. So pay close attention! 
It doesn't matter how memory is drawn as long as you keep track of endianess. The Lab is longer because it has a lot of questions to give you practice.

06 13 10 15
01 6d af
Convert Binary to Hex - convert to base 10 which goes to hex (or memorize the conversion). When you have left over it can be replaced by zeros.

8 bytes for the array.
4 bytes per int.
It's reading in as hexadecimal is bytes. Reads left one in backwards. 
Read in as: `array, array+1, array+2, array+3` +1 means array start plus size of item (int).
Undos the endianess when you print: 64616564. It will print out the same as when in when its the same type.
Ignores leading zeros so 00000021 -> 0x21.
When you interpret as characters it turns into deadbeef.
decimal value is a large number.

## Jan 28 - endianess
Endianess - for multi-bytes things. It decodes the order of bytes in a mutli-byte thing.
Does not affect the bit order.

Big-ediam machines (IBM Power) store the byte of largest significance (ie the first letters of the word) first. 
Little-endian machine (Intel, AMD, ARM, m-series) store the byte of least significance first (ie the last letters of the word).

Point: if you overwrite a variable with a larger value, it could corrupt memory.

## Jan 30
**Converting:** 
`1101 -> 1*2^3 + 1*2^2 + 0*2^1 + 1*2^0 = 8+4+0+1 = 13 (d)`

### Adding
overflow. 1+1 = 2 which is 10 in binary. Carry the one.
`1011 + 0110 = 1 0001`. Which is 11+6 = 1. Binary does not follow the same rules as the natural numbers.
Range changes based on the hardware.
3 in binary is 11.

**Adding in hex**:
`e+b (14+11) = 25 = 1 9 (16+9)`. Carry the 1. 26 = 1 a

**Adding natural numbers**
0010 + 0011 = 0101
1010 + 0100 = 1110
0111 + 1000 = 1111

**Adding integers**
Most significant bit gets a negative weight. So `1*-2^3` so 1101 becomes -3.
if they are all ones left of the 3rd ie in 1101 then you can just take the 3rd digit as the negative. 

Converting from positive to negative: 0111 = 7
1. invert all bits (1000)
2. add one. (1001 = -7)
Ranges are asymmetric. unsigned goes from 0 to (2^n)-1. signed goes from -2^(n-1) to (2^n-1)-1. for example n=5: 0-31 vs -16-15.
Can overflow from the other side, too.

`0x%x%x/n", (unsigned)(*str));`
Figure out what units it is supposed to be in, and figure out how the data needs to be converted.
Sign extension - how do I turn one byte into 4 bytes. If it is unsigned, 0 fill. if signed, you extend it by copying. so 0 or f depending on if positive or negative.

## Feb 2

### Type Casting
Widening - taking something that is one byte and making it more (ie 4 bytes, an int). It does not change the value (trust the process). 
Add 1s if negative and 0 if positive.
Widen according to the type and then apply the cast.
- `*((int*)u_str)`-> taking an unsigned char and interpreting it as an int -> keep going for 4 deadbeef
- `(unsigned)(*u_str)`-> taking an unsinged char and making it unsigned -> ef - 000000ef
- `(int)(*u_str)`-> taking an insigned char and extending it to an int -> ef (ignores leading 0s) it widens it before it interprets it, during dereferencing
- `(unsigned)(*str)`-> taking a signed char and making it unsigned -> ffffffef when you print, but its a large positive number
- `(int)(*str)`-> taking a signed char and extending it to an int -> ffffffef when you print, but it is a negative number
- `(unsigned)(*ptr_us)` -> beef -> widen with 0s that disapear.
- `(unsigned)(*(ptr_us + 1))` -> dead
- `(int)(*ptr_us))` -> beef
- `(int)(*(ptr_us + 1)` -> dead
- `(unsigned)(*ptr_s)` -> ffffbeef -> because be is 1001 a negative number
- `(unsigned)(*(ptr_s + 1))` -> ffffdead
- `(int)(*ptr_s))` -> ffffbeef
- `(int)(*(ptr_s + 1)` -> ffffdead

Narrowing - the opposite. You will lose information. 
- `(unsigned short)(*ptr_i)` - beef

### bitmap project
Turn image into grayscale and threshold. Mutating the pixels to change the colors.

```
gcc -g -Wall -o bmpFilter solution-bmpFilter.c
bmpFilter -h image name
```
has filters -g for grayscale and default for threshold.
use diff and > to pipe in image and check for differences.

## Feb 4

Purpose of the bitmap project is to reinforce modulization (creating small functions).
You should never had a function more than 15 lines of code or more than 2 nested deep. 
This might mean you have to pass lots of variables down, which indicates you should put them into a more complex object.

-g for grayscale, nothing for threshold. 
In C, make sure to free things that go on the heap (when you call new). 

Find the size of DIB header/where the pixel array starts. First header is a total of 14 bytes. bmpfiles + offset. Offset = bmpfile(byte) + 10 (units).
Pull out the width and the height of the image. Than you can used those to iterate through all the pixels.

Image is stored in row major order, meaning the pixels in the same row are stored in one chunk, in the right order.
Each pixel is 3 bytes (r,g,b). Each row needs to be a multiple of 4 bytes. So we add padding.
Padding holds no real information, it just helps with layout. width*3+padding = next row.

## Feb 9
### Free points: Problem 1
Consider a 5-bit machine that supports both signed and unsigned
arithmetic.
On this machine both int and unsigned are encoded using all 5-bits.
Assume as well that two’s-complement encoding is used for the signed
values.
Fill in the missing entries in the following table, where:
• Umin indicates the minimum possible unsigned value
• Umax indicates the maximum possible unsigned value
• Tmin indicates the minimum possible int value
• Tmax indicates the maximum possible int value
Number/Type Decimal Value Binary Encoding
- Umin - 0                  0 0000
- Umax - 31                 1 1111
- Tmin - -16                1 0000
- Tmax 15                   0 1111
- Umin-1 - 31 00000-11111 = 1 1111
- Tmin-1 - 15               0 1111
- -Tmin - -16               1 1010*maybe
- Tmax+Tmax -2              1 1110
- int -11                   1 1110
- int - -16                 1 1010

### bit shifting
shifting left means multiplying by two.
Fill in the following table showing the effects of the different shift
operators on single-byte quantities. Each of the answers should be 8
binary digits or 2 hexadecimal digits. Note that the third column is
a logical right shift operator, while the rightmost column is an
arithmetic right shift operator.
- x                  x << 1 (Logical) x >> 5 (Arithmetic) x >> 5
- Hex Binary         Binary   Hex     Binary Hex Binary Hex
- 0xcb 1100 1011  1 1001 0110 96
- 0x64 0110 0100  1100 1000   C8

### Masking - 
sets or unsets specific bits. 
