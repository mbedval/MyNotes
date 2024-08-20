
C# is an object oriented programming language, The four basic priniciples of object-oriented programming are:
1. Abstraction : the relevant attributes and interactions of entities as classes to define an abstract representation  of a system
2. Encapsulation : Hiding the internal state and functionality of an object and only allowing access through a public set of functions
3. Inheritance: Ability to create new abstraction based on existing abstractions
4. Polymorphism : Ability to implement inherited properties or methods in different ways across multiple abstractions.


### CLASSES
```
namespace Classes;

//[access modifier] - [class] - [identifier]
public class BankAccount
{
    public string Number { get; }
    public string Owner { get; set; }
    public decimal Balance { get; }

    public void MakeDeposit(decimal amount, DateTime date, string note)
    {
    }

    public void MakeWithdrawal(decimal amount, DateTime date, string note)
    {
    }
}

BankAccount object1 = new BankAccount();

```

Creating Constructor with initial value
```
public class Container
{
    // Initialize capacity field to a default value of 10:
    private int _capacity = 10;
}
```

Creating Constructor when user need to provide value
```
public class Container
{
    private int _capacity;

    public Container(int capacity) => _capacity = capacity;
}

// with C# 12, we can declare construction as
public class Container(int capacity)
{
    private int _capacity = capacity;
}


```


### INTERFACE
An interface contains definitions for a group of related functionalities that a non-abstract [`class`](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/class) or a [`struct`](https://learn.microsoft.com/en-us/dotnet/csharp/language-reference/builtin-types/struct) must implement. An interface may define `static` methods, which must have an implementation. An interface may define a default implementation for members. An interface may not declare instance data such as fields, auto-implemented properties, or property-like events.
```
interface IEquatable<T>
{
    bool Equals(T obj);
}


public class Car : IEquatable<Car>
{
    public string? Make { get; set; }
    public string? Model { get; set; }
    public string? Year { get; set; }

    // Implementation of IEquatable<T> interface
    public bool Equals(Car? car)
    {
        return (this.Make, this.Model, this.Year) ==
            (car?.Make, car?.Model, car?.Year);
    }
}
```

> By convention, interface names begin with a capital `I`
#### inheritance
```
public class Manager : Employee
{
    // Employee fields, properties, methods and events are inherited
    // New Manager fields, properties, methods and events go here...
    // When a class declaration includes a base class, it inherits all the members of the base class except the constructors.
}

```

> Importance points

- A class in C# can only directly inherit from one base class. However, because a base class may itself inherit from another class, a class might indirectly inherit multiple base classes. Furthermore, a class can directly implement one or more interfaces. For more information
- 