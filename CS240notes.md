# Java Fundamentals
## Jan 12
Oracle - download Java development kit. JDK 25. figure out what type of machine you're on and which version you need. Download intellij community edition. 

Compiled language: like C

Interpreted code: like python where you don't compile, you give it directly to interpreter. Run slower, but they are getting faster.

Java is a compiled language but it's a bit different combining plus stides of interpreted language. It creates a byte code file and a JVM knows how to make it portable to all sorts of different operating systems. Nowadays the two categories blurr together.
### writing a Java program

In C++ you have declarations and classes in header files, while in cpp files have the executable code. Then it goes to .o files which are combined into .exe file

In Java on the other hand, you have one class per file and it has the same name as the file. run javac (java compiler) on .java file to compile into a .class file. Once compiled, all you need is the .class file
main is not a standalone funtion, it is a method on a class. 

The JVM gathers all the .class files you need to run the program. 

java -cp bin/ X arg2

public class CommandLine {
// public means anyone in the program can see it, if not then only in the same folder
  public static void main(String[] args) {
    for (int i=0; i < args.length; i++) {
      System.out.println("args["+i+"] = "+args[i]); // this prints. you could also use printf("args[%d] = &s\n, i, args[i])
      // or we could just use for (String value: args) and iterate and increase the indexes.
to compile this, javac CommandLine.java and then java -cp CommandLine args

in intellij you can run it with the green play buttons, not forgetting to edit configurations to add command line arguments.

### Java classes

each member of a class is induvidually labeled as public or private.

the only way to create an object is to call new

toString makes things strings.

Javadoc: you need the documentation for the class library. API documentation. Looking for Java.base which has the standard library, with packages (folders) inside. 

### Primitive Datatypes
- byte
- short
- int
- long
- float (4 bytes)
- double (8 bytes)
- char (2 bytes, unlike C++ where it is 2 which means you can handle international text)
- boolean

Data types don't have methods in Java, so they have wrapper classes for every corresponding primitive data tyep. For example, Integer.parse() so you can say Interger i = new Integer(34) so you can call methods on it

### New

In Java, all objects live in the heap (meaning you call new) so you get back a refernce to the object (which in C++ is called a pointer).

Runtime stack: mechanism that computers use to implement runtime calls. All the parameters and local variables need to be stored somewhere.

Objects in the heap will point to each other. Primitives are at the base level, and then objects point to them and each other. 

### Working with strings
String s = "Hello"; String s = new String("Hello"); -> these are the same because strings are so common, Java does it for you. 

type names that are not primitives should be capatalized.

Strings are immutable which means they are much less error prone.
- concatenation creates a new string object
- useful methods - length(), charAt() etc. etc. look it up.

If you need a lot of concatenation, use the StringBuilder method. create StringBuilder object and then go object.append

### Chess Phase 0
3 modules - client, server, shared. Chess board and pieces are used by both so they go in shared.

ignore check and checkmate until phase 1

Don't make 6 subclasses from chess piece. Instead give the piece a type and made classes for each type's move, calling it in chess piece. This will make things easier later.









