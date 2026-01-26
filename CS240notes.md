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

```
java -cp bin/ X arg2

public class CommandLine {
// public means anyone in the program can see it, if not then only in the same folder
  public static void main(String[] args) {
    for (int i=0; i < args.length; i++) {
      System.out.println("args["+i+"] = "+args[i]); // this prints. you could also use printf("args[%d] = &s\n, i, args[i])
      // or we could just use for (String value: args) and iterate and increase the indexes.
```
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

## Jan 14

### Arrays
You always interact with objects through a pointer, same with arrays. 

``` 
  int[] intArray; // this is just a pointer - it points to anything you point it at so you don't need a size yet
  intArray = new int[10]
  String[] stringArray;
  stringArray = new String[10]; \\this is an array of empty pointers because a string is an object and it doesn't fill it with objects
  //2D array
  char[][] name = new char[3][]
```

### Packages and Folders
Package declaration - pakage edu.byu.cs240 (nested folders)

`import java.util.Data`
then you can just write Date and it is imported.

### Classes in Java and Methods to Override

```
  class ImageEditor {
    private int x;
    private void doThis() {} //  'this' is like self in python. you don't always have to call it though
```
a static method can only call/reference functions or variables that are also static. But be careful, if all the variables are static, you can't have instances. You can avoid this problem by creating a new instance of your class within the non-static function.

```
public class Person extends Object{ \\ this is the common ancestor you don't have to put "extends object" since that is assumed but you could use another base class
  private String name;
  private int age;
  private YearInSchool year; \\this should be a enum with five values.

  public Person() {
    this("", 18, YearInSchool.Freshman)
    }
  
  public Person(String name, int age, YearInSchool year) {
    setName(name);
    setAge(age);
    setYear(year);
  }

  @Override
  public String toString() {
    return String.format("%s: name: %s, age: %d, year:%s", getClass().getName(), name, age, year);
  }
  \\ you might be tempted to hard code person here, but this would be a problem if you had a subclass of Person. Instead use getClass()
```

There are two ways to define equality. One, reference equality (compares addresses). Is this literally the same object? Instead, compare them by their values. (Value-based equality).
- one == two is for reference equality
- one.equals(two) is for value equality
But the equals method by default uses reference equality

Clone() returns a pointer to a copy. (depends on class whether this is a deep or shallow copy)

Only one public class per file, technically you can have a private class that is in the same file

Writing an equals method: check for null, this (self), same class object, then compare strings last.

To compare two strings:
```
Person p = (Person)o; \\ this is type-casting, creating a Person copy (already a person but code doesn't know that) so that way below code works.
return (name.equals(o.name) && age == o.age && year == o.year);
```

**Hash tables** are great since they are fast. They are an array, used to implement sets and maps.
Hashcode method returns an int, if you want to override you can. 
Could just use built in object.hash which will return a hash code, but we should understand how this works

```
public int hashCode() {
  int hash = (name.hashCode() * age) ^ year.hashCode();
```
you can use whatever algorithm you want here, as long as it gives an exclusive hash code. Should be fast, O(1), and produce numbers that look relativley random. each array element is a linked list so if two have the same they are still stored in the same place. The more things stored in the same place, the furhter from O(1)

Creating a counter in a class:
```
private static int nextId = 10000
private static int getNextId() {
  return nextID++;
}
// in initializer
id = getNextId();
```

On phase 0, let intellij generate equals, hash, string for you and then scrutinize them.

## Jun 21

**Practice exam:** clone the starter code for chess phase 0. Follow instructions. 

### Inheritance in Java
Remember last time we created a person class.

Record - like a class. Java can generate the code you need based on another class. Record classes are immutable (once you create an object, it is unchangable).
The automatic getters don't have get in them. 

Inheritance - subclasses. Allows polymorphisms such that a Vehicles array can contain cars, trucks, boats, etc.

```
// declaring the least specific type such as collection allows more flexibility
void someMethod(Collection<String>) sList {}
```
A class can only have one superclass, unlike c++.
```
//defualt constructor
pubic Studnet(){
  super();
  setYear(Freshman);
  setGpa(0.0f);
}

//requires input constructor
public Student(variables){
  super(name, age);
  this.year = year;
  this.gpa = gpa;
}
```
### Other types of methods. Abstract and Final.
```
public int getPriority() {
  return agePriority() + caregoryPriority();
}
protected int agePriority(){
  return 1;
}
// protected is this class and decendants. private is just this class that way you can override those classes in the children, but not call them on parent.
```
Abstract means you don't provide a body of the method at all, relying on the children to override. The class is abstract then and you have to declare it as such at the top.

If you don't want subclasses to be able to override, declare it as final. String class is final. 

So final means you can't inherit from it, abstract means you must inherit from it.

### Interfaces

Class can implement an interface this is the way to get around only being able to have one parent. other classes inherit from interface. 
By definition they are all public and abstract. A class can implement as many interfaces as you want.
You can even create a sub-interface. 

Practically, it means we can get ride of duplication. Create an abstract class that extends the interface, and then extend for your classes.

## Jan 26

### Copying objects
Shallow copy - copy variable values (so they both point to the same thing).

Most often you want a deep copy. If an object is immutable you don't need to copy it, but mutable objects need to be deep copied.

Deep copies: copy constructor and clone method.
```
Faculty profCopy = new Faculty(prof)

Faculty progCopy2 = prof.clone();
```
Implementing clone putting a copy constructor within the class:
```
public Course clone(){
  return new Course(this);
}
```
In order to create a copy constructor, you need to iteracte over the students and courses calling new with their own copy constructors.

### Exceptions
You don't do a lot of error handling in school because you don't need to handle all the errors for the test. But in the real world, it is super important. 
One source of error: bugs. In that case, just fix your bugs. 
Write tests for things you can't control: bad input, broken dependancy, out of memory, stack overflow, bad internet connection.

**Handle or Declare Rule:**
Applies to Checked exceptions (not runtime exceptions or errors). 
```
// handle - lets you continue
try {
} catch(Exception ex) {
}
// declare - just tells you it could throw exception.
public void method() throws Exception {
}
```
Java forces you to handle exceptions correctly. If an excpetion is thrown, you must catch it.
Put try-catch in main to catch errors that are thrown in other methods - catches anything that leaks out.

You can only throw objects, not primitives. Use try-catch on Exceptions (not errors) that are not runtime exceptions.
- Exception
  - IO exception and others. If you don't handle these correctly Java gets mad.
  - RuntimeException - you have a bug. Java doesn't check these.    
- Error. Catastrophic. Ignore, there is nothing we can do about out of memory.

Example - this function throws filenotfound. You either need to handle it or declare it now and handle it in main. 
Printing the stack trace is one option.
```
private static void processFile(File file) {
scanner scall = null;
scan = new Scanner(file);
}
//this gives a redline error

```
**Finally Clause:** execute it every time, no matter what happens with the excpetion. You can use this to close the scan. 
An even easier way is the try with resource. 
`try (Scanner scan = new Scanner(file)){}` It will handle closing the scanner for you.

You can create a custom exception class. 

### Java Collections
When regular arrays don't suffice.

Implementations of helpful algorithms are on collections - sort, shuffle. Collections can only store objects, not primitives. 

Sets (hash set, tree set), maps (hash map, treemap, linkedhashmap)(entryset() is a useful method that gives all key values pairs), iterators, queue (array deque, priority queue, linked list), stack (performance issues, don't use)

Equals - what definion do I want? If your equals or hash code doesn't work right, the collection won't work.

Sorted collections - treeSet (BST), TreeMap (BST), PriorityQueue (binary heap) are all sorted. So the objects need to be comparable. May need to override a compareTo method to rank them. This would also allow you to sort them using Java's sort algorithms.

Can't change an object in a tree or hash table. You need to remove, change, and then put it back in. (Because changing the object changes the hash code or position. 

