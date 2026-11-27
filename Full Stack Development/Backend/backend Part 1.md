# Q. What is C# ?
-> modern, object oriented ,strongly typed (know every type of data) programming language developed by Microsoft. 
->It is commonly used in building web application, APIs, desktop application and enterprise software using .NET platform.

## Basic program structure

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, World!");
    }
}
```

Q What is a variable?
=> a named memory location used to store data that can be accessed and modified during program execution.

![[Pasted image 20261126151009.png]]

> [!NOTE]
> * A constant is a value that cannot be changed after it is declared.

```
const double Pi = 3.14159;
```

Real-world use In a fitness application:

```
const int MaximumWorkoutDuration = 180;

```
This represents a fixed limit of 180 minutes.

> [!NOTE]
> *  C# supports implicit type inference using var keyword.

```
var age = 23;
var name = "Ankit";
var isActive = true;
```

## Q. Is C# a dynamically typed language because it supports var?

=> No. C# remains statically typed.
=> The compiler determines the type at compile time, even when var is used.

![[Pasted image 20261126152350.png]]

> [!NOTE]
> .NET is more accurately described as a development platform
> 
> It includes:
> 
> - Runtime — executes managed applications.
>     
> - Base libraries — provide common functionality.
>     
> - SDK and tools — help developers build applications.
>     
> - Frameworks such as ASP.NET Core — help build web applications and APIs














