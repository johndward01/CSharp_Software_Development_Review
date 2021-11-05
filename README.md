# C# Review

<br>
<br>

## Git

*   **Version Control**: a means for managing your source code
*   **Git:** A **[distributed version-control](https://en.wikipedia.org/wiki/Distributed_version_control) system (DVCS)** for tracking changes in [source code](https://en.wikipedia.org/wiki/Source_code) during [software development](https://en.wikipedia.org/wiki/Software_development).  It is designed for coordinating work among [programmers](https://en.wikipedia.org/wiki/Programmer), but it can be used to track changes in any set of [files](https://en.wikipedia.org/wiki/Computer_file).
*   **Github:** GitHub is where our **Remote repository** will live.  Our computer is where our **Local repository** will live. 
*   **A Commit:** A commit is the Git equivalent of a "save".

<br>
<br>
<br>

## Git Commands:

*   `git init`: initializes a new repository in the current directory
*   `git status`: The git status command displays the state of the working directory and the staging area. It lets you see which changes have been staged, which haven't, and which files aren't being tracked by Git
*   `git clone <remote url goes here>`: puts a copy of the remote repository on our machine 
*   `git push`: push those changes to the remote repository 
    *   You must first use `git push -u origin main` BEFORE you can just use `git push`
*   `git pull`: pulls the latest version of the remote repository to our machine.
*   `git add <filename goes here>`: stages only the specified file
*   `git add .`: stages all files in the directory so they are ready to commit
*   `git commit -m "message goes here"`: commits the changes in the currently staged files and includes a message
*   `git branch`: lists the branches in the repository
*   `git branch <branchName>`: creates a new branch  
*   `git checkout <branchName>`: switches to a specific branch  
*   `git checkout –b <branchName>`: creates a new branch, and switches to that branch at the same time  
*   `git merge <branchName>`: merges a specific branch into the current branch 
*   `git pull`: downloads content from a remote repository and immediately update the local repository to match that content  
*   `git log`: display our commit history 
*   `git diff`: enables you to compare changes in the working directory against a previously committed version
*   `git config --global user.email "YourEmailAddressGoesHere@gmail.com"`: sets the user email
*   `git config --global user.name "Your Name"`: sets the user name

<br>
<br>
<br>

## C# Command-line

*   **CLI**: The .NET Core command-line interface (CLI) is a new cross-platform toolchain for developing .NET applications. The CLI is a foundation upon which higher-level tools, such as Integrated Development Environments (IDEs), editors, and build orchestrators, can rest. 
*   **Solution file (.sln)** - a solution is a container used by Visual Studio to organize one or more related projects.  When you open a solution in Visual Studio, it automatically loads all the projects the solution contains
*   **Project file (.csproj)** – contains all the source code that is compiled.  It also contains compiler settings and other configuration files
*   **cd**: Command-line command to change directory
*   **mkdir**: Command-line command to create a new folder (directory)


### Dotnet Commands:

*   **dotne**t **&lt;command>**: dotnet is a tool for managing .NET source code and binaries. It exposes commands that perform specific tasks, such as dotnet build and dotnet run.
*   **dotnet new**: Creates a new project, configuration file, or solution based on the specified template.
    *   Example: **dotnet new console ←- creates a new console application for us**
*   **dotnet build**: Builds a project and all of its dependencies.
*   **dotnet run**: Runs source code without any explicit compile or launch commands.
*   **dotnet sln**: The dotnet sln command provides a convenient way to add, remove, and list projects in a solution file.
*   **dotnet test**: The dotnet test command is used to execute unit tests in a given project. The dotnet test command launches the test runner console application specified for a project. The test runner executes the tests defined for a unit test framework (for example, MSTest, NUnit, or xUnit) and reports the success or failure of each test. If all tests are successful, the test runner returns 0 as an exit code; otherwise, if any test fails, it returns 1. _If the project path is not specified, it defaults to the current directory._
    *   Example: **dotnet test ~/projects/test1/test1.csproj**
*   **dotnet clean**: The dotnet clean command cleans the output of the previous build. It's implemented as an MSBuild target, so the project is evaluated when the command is run. Only the outputs created during the build are cleaned. Both intermediate (_obj_) and final output (_bin_) folders are cleaned.


#### 	Bonus (ASP.NET MVC dotnet command): 

*   **mkdir** VS_Code-MVC
*   **cd** VS_Code-MVC
*   **dotnet new mvc**
*   **code .**

**<span style="text-decoration:underline;">Type the following commands into the terminal</span>**

<br>
<br>
<br>

## Value and Reference Types

C# is a strongly AND statically typed object-oriented programming language.

*   **Strongly typed**:  once a variable’s type is declared, it cannot change. (Although you can change its value)
*   **Statically typed**: every variable must have a type at compile time.
*   **Signed**: A signed integer is one with either a plus or minus sign  

    in front. (It can be either positive or negative)

*   **Unsigned**: integer is assumed to be positive
*   **The Stack**: The Stack is used for static memory allocation.  This is where Value Types are stored. It utilizes a LAST IN, FIRST OUT procedure.
*   **The Heap**: The Heap is used for dynamic memory allocation. This is where Reference types are stored. Elements can be removed in any order from the heap.
*   **Value Type**: A variable of a value type contains an instance of the type.
*   **Reference Type**: A reference type contains a reference (*pointer) to an instance of the type.

![alt_text](img/Value%20and%20Reference%20Types/CSharp_Data-Types.png)

<br>
<br>
<br>

## C# Variables

A variable is a memory location. It has a name that is associated with that location. The memory location is used to hold data. The key difference when comparing a constant to a variable is that the value associated with a variable name may change during the execution of the program.

*   **Variable**: A variable is a container for storing value. 
*   **Constant**: A constant is a container for storing a value that never changes.
*   **Variable Name**: A variable name is an identifier for the value stored in a particular location of computer memory
*   **Data Type**: A data type specifies the size and type of variable values.
*   **Camel Case**: The first letter of the first word will be lowercase, for the first time, but uppercase everytime after
    *   Example: camelCaseExample
*   **Pascal Case**: The first letter of every word is uppercase
    *   Example: PascalCaseExample

*   **Declaring a Variable**: To declare a variable, you must specify the data type and the variable name.
    ```cs
    string firstName;
    ```

*   **Initializing a Variable**: To initialize a variable, you must assign that variable a value
    ```cs
    firstName = "John";
    ```

*   **Declaring and Initializing a variable**: 
    ```cs
    int age = 11; // Declaring and Initializing a variable
    ```

<br>
<br>
<br>

## C# Operators

*   **Operator**: Operators are special symbols that perform actions on operands
    *   Example : `2 + 2` ( **2** is the operand and **+** is the operator)
*   **Operand**: The quantity on which the operation is performed.
*   **Unary Operator**: An operator with only 1 operand.
    *   Example: `x++`
    *   Example: `!isTrue;`
    *   Example: `--x;`
*   **Binary Operator**: An operator with 2 operands.
    *   Example: `1 + 1`; (**+** is the binary operator)
*   **Ternary Operator**: An operator that requires 3 operands.
    ```cs
    var answer = x < y ? true : false;  // ? is the ternary operator
    ```
*   **Arithmetic Operators**: These are used to perform arithmetic/mathematical operations on operands.
```cs
int num1 = 0;
int num2 = 10;

int answer = num1 + num2; // Add
answer = num1 - num2; // Subtract
answer = num1 * num2; // Multiply
answer = num1 / num2; // Divide
answer = num1 % num2; // Modulus (gets the remainder after division)
answer = Math.Pow(num1, num2); // Exponent (the first number raised to the second number)
```
*   **Relational Operators**: Relational operators are used for comparison of two values.
```cs
int num1 = 0;
int num2 = 1;

bool isGreater = num1 > num2; // greater than... false
isGreater = num1 < num2; // less than... true
isGreater = num1 >= num2; // greater than OR equal to... false
isGreater = num1 <= num2; // less than OR equal to... true
```
*   **Logical Operators**: Logical operators are used to combine two or more conditions or to complement the evaluation of the original condition in consideration.

### `&&` **Logical AND** 
```cs
int x = 10;
int y = 11;
// the left expression AND the right expression must evaluate to be TRUE in order for the code to be run
if (x < y && x == 10) 
{
    x++; // both conditions are true so the code runs
}
```
### `||` **Logical OR** 
```cs
int x = 10;
int y = 20;
// the left expression OR the right expression must evaluate to be TRUE in order for the code to be run
if (x > y && x == 10) 
{
    x++; // code still runs even though x is not less than y
}
```
### `!` **Logical NOT** 
```cs
bool isPresent = true;
// the NOT operator ! flips the value to the opposite one

Console.WriteLine(!isPresent); // outputs false
```

*   **Assignment Operator**: Assignment operators are used to assign a value to a variable. The left side operand of the assignment operator is a variable and the right side operand of the assignment operator is a value. 
> Note: The **value** on the right side must be of the same **data-type** as the variable on the left side, otherwise the compiler will raise an error.
```cs
int x = 100; // = is the simple assignment operator
int y = 200;

x += y; // same as long form x = x + y;
x -= y; // same as long form x = x - y;
x *= y; // same as long form x = x * y;
x /= y; // same as long form x = x / y;
x %= y; // same as long form x = x % y;
```

<br>
<br>
<br>

## Selection Statements

**Selection statements** enable you to branch to different sections of code, depending on one or more specified conditions. The components when concerning selection statements are **if**, **else if**, **else**, and **switch/case**.
### `if`
```cs
bool condition = true;

if (condition)
{
    Console.WriteLine("Because the condition was true this code IS executed");
}
```

```cs
int x = 10; 
int y = 11;

if (x == y)
{
    Console.WriteLine("This code IS NOT run because the condition evaluated to false");
}
```

### `if / else`

```cs
int num1 = 20;
int num2 = 30;

if(num1 == num2)
{
    Console.WriteLine("The condition is false therefore this code IS NOT executed");
}
else
{
    Console.WriteLine("The above condition was false so the code in this scope IS executed ");
}
```

### `if / else if / else`

```cs
int x = 1;
int y = 2;
int z = 3;

if (x > y || y > x)
{
    Console.WriteLine("The condition is false therefore this code IS NOT executed");
}
else if (z < y || z < x)
{
    Console.WriteLine("The condition here is also false therefore this code IS NOT executed");
}
else
{
    Console.WriteLine("If all conditions are false, then this code IS executed");
}
```

*   `switch/case`: A switch is a selection statement that chooses a single case section to execute based on if the value passed in matches the case conditional. The switch statement is a control statement different from the if statement because it evaluates a single expression against a list of possible cases. <span style="text-decoration:underline;">The switch statement is often used as an alternative to an if-else construct if a single expression is tested against three or more conditions.</span>
*   `default`: Specifies the code block to run if all else fails.
*   `break`: Terminates the **switch/case** statement.
*   `case`: Each case label specifies a pattern to compare to the match expression. If they match, control is transferred to the switch section that contains the first matching case label. If no case label pattern matches the match expression, control is transferred to the section with the default case label, if there's one. If there's no default case, no statements in any switch section are executed, and control is transferred outside the switch statement.

```cs
int day = 4;

switch (day)
{
    case 0:
        Console.WriteLine("Sunday");
        break;
    case 1:
        Console.WriteLine("Monday");
        break;
    case 2:
        Console.WriteLine("Tuesday");
        break;
    case 3:
        Console.WriteLine("Wednesday");
        break;
    case 4:
        Console.WriteLine("Thursday");
        break;
    case 5:
        Console.WriteLine("Friday");
        break;
    case 6:
        Console.WriteLine("Saturday");
        break;
} // outputs Thursday
```

___


```cs
public interface ICallable 
{
    public ICallable GetPhone();
}

public class PhoneFactory : ICallable
{
    public static ICallable GetPhone(string phoneType)
    {
        switch (phoneType.ToLower())
        {
            case "android":
                return new AndroidPhone();                    
            case "apple":                    
            case "iphone":
                return new ApplePhone();
            case "google":
                return new GooglePhone();
            default:
                return new AndroidPhone();                    
        }
    }
}
```

<br>
<br>
<br>

## C# Syntax Sugar

*   **CCR**: Clear, Concise, and Readable
*   **Syntax**: the grammar for programming
*   **Best Practices**: This is syntax that is not required, but is considered the best thing to do.
```cs
Point p = new Point(); // Explicit 
var p = new Point(); // Inferred (best practice)
```

*   **Syntax Sugar**: This is syntax that is not required and not necessarily best practice, but merely makes coding more convenient or concise.
```cs
    var isGreater = num1 > num2 ? num1 : num2;
```
*    **Code Smell**:  Any indicator in a program that a potentially deep-seated issue is present.  (usually subjective and depends on factors including the particular language and experience)
*   **Explicit Typing**: When you specifically say what each variable’s type is.
```cs
DateTime d = new DateTime();
Console.WriteLine(d.ToLongDateString());
```
*   **Inferred Typing**: Inferred typing is where the compiler defines the variable’s type by looking at what the variable’s value is and inferring what the most probable type is.
```cs
var x = 10; // var -> int
var y = true; // var -> bool
var z = new List<int>(); // var -> List<int>
```
<br>
<br>
<br>

## Iteration Statements & Loops

*   **while**: The **while** loop executes a statement or a block of statements while a specified Boolean expression evaluates to true. Because that expression is evaluated before each execution of the loop, a while loop executes zero or more times.
```cs
int counter = 5;

while (counter > 0)
{
    Console.Write($"{counter} "); // outputs => 5 4 3 2 1
    counter--;
}
```

<br>

*   **do-while**: The **do-while** loop executes a statement or a block of statements while a specified Boolean expression evaluates to true. Because that expression is evaluated after each execution of the loop, a do-while loop is guaranteed to execute at least one or more times.
```cs
int counter = 5;
do
{
    Console.Write($"{counter} "); // outputs => 5 4 3 2 1
    counter--;
} 
while(counter > 0);
```

<br>

*   **for**: The “**for**” loop executes a statement or a block of statements while a specified Boolean expression evaluates to true.
    *   the **initializer** - runs once at the beginning and sets an initial value to serve as a counter     **int i = 0;**
    *   the **conditional** - evaluates before each iteration to determine whether the loop should continue executing     **i &lt; 10;**
    *   the **increment** - after the body of the loop is executed, the increment updates the value of the counter     **i++;**
    *   and the **body**  - the is the block of code the loop will execute.  We also call this the **scope** of the loop     **{  }**
```cs
for(int i = 5; i > 0; i--)
{
    Console.Write($"{i} "); // outputs => 5 4 3 2 1     
}
```

<br>

*   **foreach**: A “**foreach**” loop executes a statement or a block of statements for each element in an instance of the type that implements the [System.Collections](https://docs.microsoft.com/en-us/dotnet/api/system.collections.ienumerable).IEnumerable;

```cs
var myList = new List<int>() {5, 4, 3, 2, 1 };
foreach (var num in myList)
{
    Console.Write($"{num} "); // outputs => 5 4 3 2 1
}
```



### Recap:

- Use a while loop if you need to execute some code until something happens.
- Use a do-while loop if you need to execute some code at least once, then continue execution until something happens.
- Use a for loop if you need to execute some code a specific number of times. 
- Use a foreach loop if you need to execute some code on each element in a collection of elements.

<br>
<br>
<br>

## Methods/Functions

**Method**: A method, or function, helps you separate your code into modules that perform a given task... You execute this code by calling the Method. In C# a method consists of a few things:

*   **Access Modifiers**: Access modifiers are keywords used to specify the declared accessibility of a member or a type.
*   **Return Type**: the type returned by the method, or void when not returning anything
    *   **void**: **void** is the absence of a return type
*   **Name**: a descriptive method name using PascalCase
    *   **PascalCase**: every first letter of every word is capitalized
*   **Parameters**: an optional list of variables to be passed to the method
*   **Scope/Body**: the block of code to be executed when the method is called
*   **Argument**: the value you pass into the function when it is being called

![alt_text](img/Methods/5PartsOfMethods.png)

<br>

```cs
// Declaring a public Add Method that accepts 2 whole numbers 

public int Add(int x, int y)
{
    return x + y;
}
```

<br>
<br>
<br>

## Method Overloading

*   **Method Overloading**: When multiple methods share the same name but have a different signature
    *   1. The number of parameters
    *   2. The order of the parameters
    *   3. The data types of the parameters
*   **Signature**: A method signature is a unique identification of a method for the C# compiler. The signature consists of a method name and the type and kind (value, reference, or output) of each of its formal parameters. Method signature does not include the return type.

![Method Overloading](img/Method%20Overloading/MethodOverloading.png)

*   **Rules for overloading a method**
    *   Where a parameter represents the same value as that in another method, the parameters should have the same name.
    *   Parameters with the same name should appear in the same position in each method’s parameter list.
    *   You should not use ref or out modifiers to overload methods.
    *   You cannot overload method declarations that differ only by return type.

### Method Overloading Examples `Console.WriteLine();`

![Console.WriteLine()](img/Method%20Overloading/cw-Overload.png)

<br>
<br>
<br>

## Arrays & Lists

*   **Arrays**: Arrays are used to store multiple values in a single variable, instead of declaring separate variables for each value. In C#, arrays are actually objects, and not just addressable regions of contiguous memory as in C and C++. Therefore, using dot notation, you have access to the properties and methods of the abstract [Array](https://docs.microsoft.com/en-us/dotnet/api/system.array?view=net-5.0) class.

### Declaring and Initializing Arrays:
```cs
// Example 1 => Declaring an int array of size 3 (explicitly)
int[] myArray1 = new int[3];

// Example 1 => Initializing each of the array's indices 
myArray1[0] = 10;
myArray1[1] = 20;
myArray1[2] = 30;

// Example 2 => Declaring and initializing an int array (at the same time)
int[] myArray2 = new int[] { 3, 2, 1 };

// Example 3 => Declaring and initializing an int array (implicitly)
var myArray3 = new int[] { 10, 11, 12 };

// Example 4 => Shorthad Syntax
int[] myArray4 = { 100, 200, 300 };
```

### Accessing Elemets of Arrays:
```cs
string[] cars = { "Tesla", "Ford", "Honda", "Toyota" };

// To access an element inside an array, use the name of the array with bracket [] notation

Console.WriteLine(cars[0]); // 0 is the first index so the output is: Tesla
Console.WriteLine(cars[2]); // output: Honda

// You can run expressions inside of the brackets as long as that expression evaluates to an INTEGER
Console.WriteLine(cars[cars.Length - 1]); // output: Toyota
// cars.Length = 4 so we subtract 1 to get the 3rd index or the last element in the array

Console.WriteLine(cars[4]); // throws an exception (System.IndexOutOfRangeException)
```

<br>
----
<br>

*   **Lists**: Collections provide a more flexible way to work with groups of objects. Unlike arrays, the group of objects you work with can grow and shrink dynamically as the needs of the application change. For some collections, you can assign a key to any object that you put into the collection so that you can quickly retrieve the object by using the key.

### Declaring and Initializing Lists:
```cs
public class Person
{
    public string FirstName {get; set;}
    public string LastName {get; set;}

    public Person(string firstName, string lastName)
    {
        FirstName = firstName;
        LastName = lastName;
    }
}

// Declaring an empty List of type int called numbers
var numbers = new List<int>();

// Declaring and Initializing a list of string called myList with 3 string values
var myList = new List<string>() { "The 1st string","The 2nd string", "The 3rd string" };

// Declaring and Initializing a list of Person Objects called people (object initializer syntax)
var people = new List<Person>() 
{ 
    new Person("John", "Ward"),
    new Person("Jon", "Doe"),
    new Person("Jane", "Doe")
}
```

### Looping through Arrays and Lists:
```cs
// Declaring/Initializing an int array called numbers then looping through it 1 by 1 and printing out each element to the console
var evenNumbers = new int[] { 0, 2, 4, 6, 8, 10 };

for (int i = 0; i < evenNumbers.Length; i++)
{
    Console.Write(evenNumbers[i]); // outputs => 0246810
}
```
```cs
// Declaring/Initializing a list of ints called oddNumbers then looping through it 1 by 1 and printing out each element to the console
var oddNumbers = new List<int>() { 1, 3, 5, 7, 9, 11 };

foreach (var num in oddNumbers)
{
    Console.Write(num); // outputs => 1357911
}
```
<br>
<br>
<br>

## Classes

Before classes and Object-Oriented Programming was a thing, programmers used functional programming as a programming paradigm...

*   **Functional Programming**: Functional programming allows building a program using mathematical functions. In other words, it binds the program into a purely mathematical function. Using functional programming, the developer can build a program as a combination of separate mathematical functions.
*   **Object-Oriented Programming**: Object-oriented programming (OOP) is a [programming paradigm](https://en.wikipedia.org/wiki/Programming_paradigm) based on the concept of "[objects](https://en.wikipedia.org/wiki/Object_(computer_science))", which can contain [data](https://en.wikipedia.org/wiki/Data) and code: data in the form of [fields](https://en.wikipedia.org/wiki/Field_(computer_science)) (often known as attributes or properties), and code, in the form of procedures (often known as [methods](https://en.wikipedia.org/wiki/Method_(computer_science))).
*   **Class**: Classes are the cornerstone of Object-Oriented Programming. They help you take all the properties and behaviors of an object in your program, and combine them into a single object, then re-use that object wherever you need it in your program. Using classes in your code enables you to implement **Encapsulation, Abstraction, Inheritance, and Polymorphism**.
*   **Object**: An object is defined as a singular instance of a class or type. A class can be thought of as a **blueprint**, a **template** or a **cookie cutter**. A class describes an object, but it is not that object.

*   **Class Members**: Classes have members sort of like how methods have variables; however, classes are not only limited to variables. Examples:
    *   **Fields** - a variable of any type that is declared directly in a class or struct.
    *   **Properties** - a member that provides a mechanism to read, write, or compute the value of a private field.
    *   **Methods** - a code block that contains a series of statements to execute.
    *   **Constructors** - Whenever a class or struct is created, its constructor is called.

*   **Dot Notation**: The way we access the methods and properties of a class is with the ( . ) **Dot** operator, Dot Notation, or Class Member Access Operator.

### Parts of a class

1. **Access Modifier** Keywords - **OPTIONAL**
2. **class** keyword - **REQUIRED**
3. **Name** - **REQUIRED**
4. **Scope** or “curly brackets” - **REQUIRED**
    1. **Fields/Properties** - **OPTIONAL**
    2. **Methods** - **OPTIONAL**
    
```cs
class Cat // the access modifier is optional (will default to internal)
{ // opening curly brace

    // class members (will default to private)
    // Methods
    // Properties
    // Fields 
    // Constructors
    // Etc...

} // closing curly brace
```
- Dog Class Example
```cs
using System;

namespace Class_Demo
{
    public class Dog
    {
        // Constructors
        public Dog()
        {

        } 

        // Fields
        private int _id;
        private string _name;
        private readonly IDbConnection _conn;

        // Properties
        public int Age {get; set;}
        public DateTime BirthDay {get; set;}

        // Methods
        public void Bark()
        {
            Console.WriteLine("Woof woof");
        }
    }

    public class Program 
    {
        static void Main(string[] args)
        {
            // (Creating an instance of type Dog), (Instantiating a dog object), etc...
            Dog dog1 = new Dog();

            // We access the class members of the object using dot notation ( . )
            dog1.Birthday = DateTime.Now;
            dog1.Bark();
        }
    }
}
```

<br>
<br>
<br>

## Encapsulation

#### Encapsulation means, that a group of related properties, methods, and other members are treated as a single unit or object.
#### The key advantage of using an Object Oriented Programming language like C# is that it provides your code security, flexibility, and easy maintainability through encapsulation. Encapsulation is also useful in hiding the data (instance variables) of a class from illegal direct access. 
#### Encapsulation is one of the 4 pillars of Object Oriented Programming.

> Note: Encapsulation is also called information hiding.

- An easy way to remember the 4 pillars is this acronymn: **OOPs A PIE**

    - **O**bject
    - **O**riented 
    - **P**rogramming
    - **A**bstraction
    - **P**olymorphism
    - **I**nheritance
    - **E**ncapsulation

___

### We can implement Encapsulation by using Access Modifiers.

C# supports the following access modifiers:

`public` - access modifier makes the member accessible from outside of the class

`private` - makes members accessible only from within the class it was created in and hides the member from the outside

`protected` - the member can only be accessed by code in the same class or in a derived class

`internal` - the member can be accessed by any code in the same assembly, but not from another assembly

`protected internal` - the member can be accessed by any code in the same assembly, or by any derived class in another assembly

<br>

## Encapsulation Example Below

- Encapsulation is used to restrict access to members of a
class so as to prevent the user of a given class from
manipulating objects in ways that are not intended by the
Designer.

- Encapsulation hides the internal implementation of
functionalities of a class without affecting the overall
functioning of the system.

- It allows the class to service a request for functionality and
add or modify its internal structure (data or methods) to
suit changing requirement.

```cs
public class PersonalInfo
{
    private readonly int _ssn; // this Field is 'private' (only accessible inside this class) AND 'readonly' (you can't modify after it's been set {after initialization})

    public Personal_Info(int ssn) // this constructor sets the private Field _ssn upon instantiation
    {
        _ssn = ssn;
    }

    public void Show_SSN(int ssn) // this is the 'public' facing method used to display the ENCAPSULATED Field
    {
        Console.WriteLine($"SSN: {ssn}");
    }
}
```

<br>
<br>
<br>

## Inheritance

**Inheritance**, together with **encapsulation**, **abstraction**, and **polymorphism**, is one of the four pillars of **object-oriented programming**. 

### Inheritance enables you to create new classes that reuse, extend, and modify the behavior that is defined in other classes.

![base/derived](img/Inheritance/Inheritance.png)

```cs
public class BankAccount
{
    public long AccountNumber {get; set;}
    public decimal Balance {get; set;}
    public DateTime DateOpened {get; set;}
    public string AccountType {get; set;}
}

public class CheckingAccount : BankAccount
{
    public int ChecksOrdered {get; set;}
    public bool IssuedDebitCard {get; set;}
}

public class Program 
{
    static void Main(string[] args)
    {
        var bankAccount1 = new BankAccount(); // Base Class
        Console.WriteLine(bankAccount1.AccountNumber);
        Console.WriteLine(bankAccount1.Balance);
        Console.WriteLine(bankAccount1.DateOpened);
        Console.WriteLine(bankAccount1.AccountType);

        var checkingAccount1 = new CheckingAccount(); // Derived Class
        Console.WriteLine(checkingAccount1.AccountNumber);
        Console.WriteLine(checkingAccount1.Balance);
        Console.WriteLine(checkingAccount1.DateOpened);
        Console.WriteLine(checkingAccount1.AccountType);
        Console.WriteLine(checkingAccount1.ChecksOrdered);
        Console.WriteLine(checkingAccount1.IssuedDebitCard);
    }    
}
```

<br>

![MicrosoftDocs](img/Inheritance/Inheritance1.png)

```cs
// WorkItem implicitly inherits from the Object class.
public class WorkItem
{
    // Static field currentID stores the job ID of the last WorkItem that
    // has been created.
    private static int currentID;

    //Properties.
    protected int ID { get; set; }
    protected string Title { get; set; }
    protected string Description { get; set; }
    protected TimeSpan jobLength { get; set; }

    // Default constructor. If a derived class does not invoke a base-
    // class constructor explicitly, the default constructor is called
    // implicitly.
    public WorkItem()
    {
        ID = 0;
        Title = "Default title";
        Description = "Default description.";
        jobLength = new TimeSpan();
    }

    // Instance constructor that has three parameters.
    public WorkItem(string title, string desc, TimeSpan joblen)
    {
        this.ID = GetNextID();
        this.Title = title;
        this.Description = desc;
        this.jobLength = joblen;
    }

    // Static constructor to initialize the static member, currentID. This
    // constructor is called one time, automatically, before any instance
    // of WorkItem or ChangeRequest is created, or currentID is referenced.
    static WorkItem() => currentID = 0;

    // currentID is a static field. It is incremented each time a new
    // instance of WorkItem is created.
    protected int GetNextID() => ++currentID;

    // Method Update enables you to update the title and job length of an
    // existing WorkItem object.
    public void Update(string title, TimeSpan joblen)
    {
        this.Title = title;
        this.jobLength = joblen;
    }

    // Virtual method override of the ToString method that is inherited
    // from System.Object.
    public override string ToString() =>
        $"{this.ID} - {this.Title}";
}

// ChangeRequest derives from WorkItem and adds a property (originalItemID)
// and two constructors.
public class ChangeRequest : WorkItem
{
    protected int originalItemID { get; set; }

    // Constructors. Because neither constructor calls a base-class
    // constructor explicitly, the default constructor in the base class
    // is called implicitly. The base class must contain a default
    // constructor.

    // Default constructor for the derived class.
    public ChangeRequest() { }

    // Instance constructor that has four parameters.
    public ChangeRequest(string title, string desc, TimeSpan jobLen,
                         int originalID)
    {
        // The following properties and the GetNexID method are inherited
        // from WorkItem.
        this.ID = GetNextID();
        this.Title = title;
        this.Description = desc;
        this.jobLength = jobLen;

        // Property originalItemId is a member of ChangeRequest, but not
        // of WorkItem.
        this.originalItemID = originalID;
    }
}
```

<br>
<br>
<br>

## Static Keyword 

In code when we create an instance of a class we are allocating a certain amount of memory for that object to reference. We may have a class that performs a particular function or method in multiple parts of our code. As a programmer, you should always strive to have the most efficient and readable code possible. Instead of instantiating the object and allocating the memory every time in our code just to invoke a couple of methods; we can use the static keyword.

### So what is static? Static simply means that when applied to a class member, it belongs to the type/class itself and not to the object instance.

```cs
using System;

namespace InheritanceDemo
{
    public class Teacher
    {
        public string Name {get; set;}
        public static string Subject {get; set;}
    }

    public class Program
    {
        static void Main(string[] args)
        {
            Teacher t = new Teacher(); // Teacher instance
            t.Name = "Some Teacher's Name"; // instance property

            Teacher.Subject = "C#"; // static property
        }
    }
}
```

Another example of using a static class and static class methods, one we all should be pretty familiar with by now, is `System.Console` i.e. `Console.WriteLine()` and `Console.ReadLine()`. We do not need to create a console object to just print something to the console, we just call the static method **WriteLine()** to do that for us.

![Console.](img/Static%20Keyword/StaticKeyword.png)

![WriteLine()](img/Static%20Keyword/StaticKeyword1.png)

<br>
<br>
<br>

## Abstract Classes

Abstract classes have the following features: 
- An abstract class cannot be instantiated. 
- An abstract class may contain abstract methods and accessors.
- A non-abstract class derived from an abstract class must include actual implementations of all inherited abstract methods and accessors.

![abstract1](img/Abstract%20Classes/Abstract1.png)

So in essence, an abstract class acts as a stubbed-out template class that other classes will derive from and use as an incomplete base. The derived class will define its own way to complete the stubbed-out template provided by the abstract class. 

> **The purpose of an abstract class is to define some common behavior that can be inherited by multiple subclasses, without implementing the entire class.**

```cs
// Abstract Class
public abstract class Vehicle
{
    // Instance Properties
    public int NumberOfTies {get; set;}
    public string Make {get; set;}
    public string Model {get; set;}
    public DateTime Year {get; set;}

    // Abstract Method
    public abstract void Drive(Vehicle vehicle);

    // Virtual Method
    public virtual void ShowInfo(Vehicle vehicle)
    {
        Console.WriteLine($"{vehicle.Year}");
        Console.WriteLine($"{vehicle.Make}");
        Console.WriteLine($"{vehicle.Model}");
        Console.WriteLine($"{vehicle.NumberOfTires}");       
    }    

    /*
    The virtual modifier keyword - use this to mark a property or method virtual.
    This will tell the compiler that the base class will provide an implementation of the property or method. 
    If the derived class wishes to override the implementation it can. 
    */
}

// Concrete Class
public class Car : Vehicle
{
    public override void Drive(Vehicle vehicle)
    {
        // This will keep the base implementation
        // Plus anything you add to this method
        base.ShowInfo(vehicle);
    }

    /*
    The override modifier keyword - You MUST override an abstract member.
    If you want to modify any virtual methods, properties, etc... you will also use the override keyword
    */
}
```
<br>

> Method Overloading gives us **static polymorphism**

> Abstract Classes give us **dynamic polymorphism**

<br>
<br>
<br>

## Interfaces

Interfaces in C# provide another way to achieve runtime polymorphism. 

What is runtime polymorphism? 

By runtime polymorphism, we can point to any derived class from the object of the base class at runtime that shows the ability of runtime binding. 

Using interfaces we can invoke functions from different classes through the same Interface reference, whereas using virtual functions we can invoke functions from different classes in the same inheritance hierarchy through the same reference.

```cs
using System;

namespace InterfacesDemo
{
    public interface ISecurity
    {
        public int ID {get; set;}
        public string Role {get; set;}
        
        public void Status();
    }

    public class Account : ISecurity
    {
        // Fields
        private string _accountType;

        // Constructors
        public Account(string accountType)
        {
            _accountType = accountType
        }

        // Properties
        public int ID {get; set;}
        public string Role {get; set;}

        // Methods
        public override void Status()
        {
            Console.WriteLine($"Account Type: {_accountType}")
            Console.WriteLine($"ID: {ID}");
            Console.WriteLine($"Role: {Role}");
        }
    }

    public class User : ISecurity
    {        
        // Fields
        private string _userType;
        
        // Constructors
        public User(string user)
        {
            _userType = user;
        }

        // Properties
        public string FirstName {get; set;}   
        public string LastName {get; set;}
        public char MiddleInitial {get; set;}
        public string Suffix {get; set;} = "";

        public int ID {get; set;}
        public string Role {get; set;}

        // Methods
        public override void Status()
        {
            Console.WriteLine($"Full Name: {FirstName} {MiddleInitial} {LastName} {Suffix}");
            Console.WriteLine($"Account Type: {_accountType}")
            Console.WriteLine($"ID: {ID}");
            Console.WriteLine($"Role: {Role}");
        }
    }

    public class Program
    {
        static void Main(string[] args)
        {
            ISecurity account1 = new Account("Tier 1")
            {
                ID = 1,
            };

            ISecurity user1 = new User("Gold")
            {
                FirstName = "John",
                MiddleInitial = 'X',
                LastName = "Doe",
                ID = 1,
                Role = "customer",
            }

            account1.Status();
            // outputs => 
            // Account Type: Tier 1
            // ID: 1
            // Role: 

            user1.Status();         
            // outputs => 
            //  FirstName: John
            //  MiddleInitial: X
            //  LastName: Doe
            //  ID: 1
            //  Role: customer

            /* Using interfaces we can invoke functions from different classes through the same Interface reference */
            // Runtime polymorphism Achieved (Interface reference = ISecurity)
        }
    }
}
```

```cs
using System;
using System.Collections.Generic;
using System.Linq;

namespace ConsoleApp1
{
    public abstract class Shape
    {
        public string ShapeName { get; set; } = "Polygon";
        public abstract double[] Sides { get; set; }
        public abstract double Radius { get; set; }

        public abstract double Area(double radius, double[] sides);

        public virtual double Perimeter(double radius, double[] sides)
        {
            // Default Implementation
            return 0.0;
        }
    }

    public class Circle : Shape
    {
        public override double[] Sides { get; set; } // 0
        public override double Radius { get; set; }

        public override double Area(double radius, double[] sides)
        {
            return Math.PI * Math.Pow(radius, 2);
        }

        public override double Perimeter(double radius, double[] sides)
        {
            if (sides.Length == 0)
            {
                return Math.PI * radius * 2;
            }

            return sides.Sum();
        }
    }

    public class Triangle : Shape
    {
        #region Herons Formula
        //   a = side a
        //   b = side b
        //   c = side c
        //  s = (a + b + c)/2
        #endregion
        public override double[] Sides { get; set; } // Herons Formula:  Area = √[s(s-a)(s-b)(s-c)]       
        public override double Radius { get; set; }

        public override double Area(double radius, double[] sides)
        {
            double semiperimeter = sides.Sum() / 2;
            double area = Math.Sqrt(semiperimeter * (semiperimeter - sides[0]) * (semiperimeter - sides[1]) * (semiperimeter - sides[2]));
            return area;
        }

        public override double Perimeter(double radius, double[] sides)
        {
            return sides.Sum();
        }
    }

    class Program
    {
        static void Main(string[] args)
        {
            Shape shape1 = new Circle();
            shape1.ShapeName = "Circle";
            shape1.Radius = 10;
            shape1.Area(shape1.Radius, new double[] { });

            Shape shape2 = new Triangle();
            shape2.ShapeName = "Triangle";
            shape2.Sides = new double[] { 4, 13, 15}; // https://www.triangle-calculator.com/?what=sss&a=4&b=13&c=15&submit=Solve
            Console.WriteLine(shape2.Area(0, shape2.Sides)); 

            //  using virtual functions we can invoke functions from different classes in the same inheritance hierarchy through the same reference
            // Runtime Polymorphism Achieved (Inheritance Hierarchy Reference = Shape)
        }
    }
}
```
<br>
<br>
<br>

## Factory Pattern

