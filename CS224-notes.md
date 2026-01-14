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

` 
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
    `
If you add one to a pointer, it thinks you want the second thing, as if this were an array of integers.



    
