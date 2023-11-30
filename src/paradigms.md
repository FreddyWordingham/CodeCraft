# Paradigms

All programming languages are Turing complete, meaning they can be used to solve any problem that can be solved by a computer.
However, some languages are better suited to certain tasks than others.
This is because each language is designed with a specific paradigm in mind.

A programming paradigm is a style or way of thinking about programming.
It's not a specific language feature or syntax, but rather a way of approaching software design.
A paradigm is a set of rules and regulations that define how a programmer can build a program to solve a problem.

## Table of Contents

-   [Paradigms](#paradigms)
    -   [Table of Contents](#table-of-contents)
    -   [Imperative Programming](#imperative-programming)
    -   [Procedural Programming](#procedural-programming)
    -   [Functional Programming](#functional-programming)
    -   [Object-Oriented Programming (OOP)](#object-oriented-programming-oop)
    -   [Structured Programming](#structured-programming)
    -   [Logic Programming](#logic-programming)
    -   [Declarative Programming](#declarative-programming)
    -   [Concurrent Programming](#concurrent-programming)
    -   [Event-Driven Programming](#event-driven-programming)
    -   [Reflective Programming](#reflective-programming)
    -   [Aspect-Oriented Programming (AOP)](#aspect-oriented-programming-aop)
    -   [Generic Programming](#generic-programming)
    -   [Metaprogramming](#metaprogramming)

## Imperative Programming

Dates back to the earliest programming languages.

```sql
initialize result = 0
for each item in list:
    add item to result
return result
```

Imperative programming is a programming paradigm that uses statements to change a program's state.
It involves writing a sequence of instructions for the computer to follow and often reflects the way humans think about how a task is accomplished. The instructions tell the computer how to perform a series of steps that lead to a desired goal.

Early Supporter: Assembly languages and early high-level languages like Fortran and COBOL were imperative, focusing on how a program operates.

## Procedural Programming

Emerged in the 1950s.

```css
function addNumbers(a, b):
    return a + b

result = addNumbers(5, 3)
```

Procedural programming, a subtype of imperative programming, is based on the concept of procedure calls.
It structures programs as a collection of procedures, also known as routines or functions, which are blocks of code that perform a specific task.
In procedural programming, a program is typically divided into reusable and modular procedures, each handling a part of the task. This approach promotes code reusability and clarity.
C is a classic example of a procedural programming language.

Early Supporter: Fortran (1957). It was one of the first high-level languages to implement procedural programming, focusing on the procedure of the program.

## Functional Programming

Originated in the 1950s, but gained popularity in the 1970s.

```go
function applyFunctionToList(func, list):
    return list.map(func)

applyFunctionToList(x => x * 2, [1, 2, 3])
```

Functional programming is a paradigm where programs are constructed by applying and composing functions. It emphasizes the use of pure functions, which avoid shared state and mutable data.
In functional programming, the output value of a function depends only on its arguments, making it easier to predict and test.
This paradigm is known for its expressiveness and is used in languages like Haskell and Scala.
It's particularly suited for parallel processing and complex computations, fitting well with your interest in programming and physics.

Early Supporter: Lisp (1958). It's one of the earliest languages supporting functional programming, emphasizing functions and recursion.

## Object-Oriented Programming (OOP)

Emerged in the 1960s.

```javascript
class Animal:
    function makeSound():
        print "Some sound"

class Dog inherits Animal:
    function makeSound():
        print "Bark"

dog = new Dog()
dog.makeSound()
```

Functional programming is a paradigm where programs are constructed by applying and composing functions.
It emphasizes the use of pure functions, which avoid shared state and mutable data.
In functional programming, the output value of a function depends only on its arguments, making it easier to predict and test.
This paradigm is known for its expressiveness and is used in languages like Haskell and Scala.
It's particularly suited for parallel processing and complex computations, fitting well with your interest in programming and physics.

Early Supporter: Simula (1967). Often credited as the first language to offer object-oriented features like classes and objects.

## Structured Programming

Gained prominence in the late 1960s and early 1970s.

```css
if condition:
    doActionA()
else:
    doActionB()
while anotherCondition:
    repeatAction()
```

Structured programming is a programming paradigm aimed at improving the clarity, quality, and development time of a computer program by making extensive use of subroutines, block structures, for and while loops, and if/then/else structures.
It's a subset of imperative programming, focusing on linear flow and clear, structured control constructs. This approach avoids using the GOTO statement, which can lead to complex or unmanageable code.
Structured programming makes programs easier to understand and modify, and is fundamental in languages like C and Pascal.
As a programmer, you'd appreciate its emphasis on straightforward, maintainable code structures.

Early Supporter: ALGOL (1958). Influenced subsequent languages like C for structured programming, focusing on clear structure and blocks.

## Logic Programming

Emerged in the 1970s.

```scss
isDog(Animal): -Animal hasFur, Animal barks. query isDog(spot) .;
```

Logic programming is a programming paradigm based on formal logic.
In logic programming, you write programs by declaring statements in logical form, and the program execution involves finding solutions that satisfy these statements.
The most notable feature is that it focuses on what needs to be done, rather than how to do it, making it a form of declarative programming.

Early Supporter: Prolog (1972). Introduced the paradigm of logic programming, focusing on formal logic.

## Declarative Programming

Became more distinct as a paradigm in the 1970s.

```sql
SELECT name FROM users WHERE age > 20
```

Declarative programming is a style of building programs that expresses the logic of a computation without describing its control flow.
In contrast to imperative programming, which focuses on the "how" to achieve something, declarative programming focuses on the "what" - the outcome you want to achieve.

Early Supporter: SQL (1974) for databases and Prolog for logic programming. These languages allow the programmer to express the logic without necessarily detailing the control flow.

## Concurrent Programming

Became more prominent in the 1970s and 1980s.

```vbnet
thread1:
    while true:
        performTaskA()

thread2:
    while true:
        performTaskB()

start thread1
start thread2
```

Concurrent programming is a computing paradigm in which several computations are executed during overlapping time periods—concurrently—instead of sequentially.
This is a form of computing in which multiple processes are executing and making progress at the same time.

Early Supporter: Ada (1980). It was designed with built-in support for concurrent programming, including features for handling tasks, synchronization, and communication.

## Event-Driven Programming

Rose to prominence in the 1980s and 1990s.

```lua
function onClick(event):
    print "Button clicked"

button.addEventListener("click", onClick)
```

Event-driven programming is a paradigm in which the flow of the program is determined by events such as user actions (mouse clicks, key presses), sensor outputs, or messages from other programs/threads.
It's a prominent model in developing applications with graphical user interfaces (GUIs), real-time systems, and other systems that need to respond to changes in their environment or user interactions.

Early Supporter: Visual Basic (1991) and other GUI-based languages. This paradigm is centered around the system responding to user or system-generated events.

## Reflective Programming

Gained attention in the 1980s.

```csharp
object = getObject()
if object hasMethod "update":
    object.update()
```

Reflective programming is a programming paradigm that allows a program to examine and modify its own structure and behavior at runtime.
This kind of programming is closely related to the ability of a program to introspect or reflect upon itself, hence the term "reflective."

Early Supporter: Smalltalk (1980). One of the first languages to support reflection, allowing a program to manipulate the structure and behavior of the program itself.

## Aspect-Oriented Programming (AOP)

Emerged in the late 1990s.

```scss
aspect Logging {
    before methodCall():
        log "Method called"
}

call methodCall() // Logging happens automatically
```

Aspect-Oriented Programming (AOP) is a programming paradigm that aims to increase modularity by allowing the separation of cross-cutting concerns.
It does this by adding additional behavior to existing code (an advice) without modifying the code itself, instead separately specifying which code is modified via a "pointcut" specification, such as "log all function calls when the function's name begins with 'set'".

Early Supporter: AspectJ (2001). An extension of Java, AspectJ was one of the first languages to support AOP, which allows separation of cross-cutting concerns.

## Generic Programming

Gained prominence in the 1990s.

```javascript
function sortList<T>(list: List<T>): List<T>
    // sort logic here
    return sortedList

sortedNumbers = sortList<Number>([3, 1, 4])
sortedStrings = sortList<String>(["b", "a", "c"])
```

Generic programming is a programming paradigm that focuses on designing algorithms and data structures in a way that they can work with any data type.
The key idea is to write code that is independent of any specific type and can be reused with different types. This is achieved through the use of generics, which allow you to write a function or class to work with any data type, specified as a parameter.

Early Supporter: Ada and C++ (with templates introduced in 1989). This paradigm focuses on writing algorithms in terms of types to be specified later.

## Metaprogramming

While the concept is older, it gained particular traction in the 1990s and 2000s.

```scss
program generateProgram(input):
    code = "function doSomething() { return " + input + " }"
    return compile(code)

newProgram = generateProgram("Hello World")
newProgram.doSomething() // returns "Hello World"
```

Metaprogramming is a programming technique in which computer programs have the ability to treat other programs as their data.
It means that a program can be designed to read, generate, analyze or transform other programs, and even modify itself while running.

Early Supporter: Lisp (with macros) and later Ruby and Python. This involves writing programs that write or manipulate other programs (or themselves).
