# C#/.NET interview prep

- [x] types of programming
    - declerative: *what* to execute
    - imperative: *how* to execute
    - procedural/structured: defines each step of the program
    - functional: avoids state and mutable data
- [x] four OOP principles
    - encapsulation: each instance of an object has its own protected data
    - abstraction: you don't have to know how the class works, jsut what you can do with it
    - inheritance: classes can inheret other classes in order to not duplicate methods/properties that multiple classes need
    - polymorphism: a child class can be used just like the parent class (e.g. each class that inherets from Vehicle will have a drive() function that does what's expected)
- [x] OOP explained with a car analogy
    - the objects: Vehicle made up of NumberOfWheels, MPG, etc.
    - the methods: Drive(), Refuel()
    - child classes inherit from Vehicle and define specific vehicle types (Truck, Car, Motorcycle, etc.)
        - each child class has additional fields, including CarType enum for cars, TowingCapacity for trucks, etc.
        - the constructor for each child class defines a default NumberOfWheels
- [x] what is CLR?
    - it manages running the code and does garbage collection, etc.
- [x] managed vs. unmanaged code
    - managed code is code that is managed by the CLR during runtime
    - unmanaged code is not (duh)
- [ ] abstract vs. interface
- [ ] struct vs. class
- [x] ref vs. out
    - ref designates an argument as a reference value, so the object doesn't have to be returned, it's changed in the function
    - out takes a variable (that doesn't have to be instantiated) and assigns whatever the return value is to that variable
- [ ] what are extension methods?
- [ ] what are generics?
- [ ] list the accessibility modifiers
- [ ] what is a virtual method?
- [ ] value vs. reference types
- [ ] does C# support multiple inheritance? if not, what's a work-around for that?
- [ ] what is boxing and unboxing?
- [ ] what are partial classes?
- [ ] what are sealed classes?
- [ ] late vs. early binding
- [ ] what are indexers?
- [ ] == vs. Equals()
- [ ] is vs. as operators
- [ ] what are different ways a method can be overloaded?
- [ ] what is reflection?
- [ ] const vs. readonly
- [ ] String vs. StringBuilder
- [ ] IEnumerable vs. IQueryable
- [ ] what is LINQ?
- [ ] what are accessors?
- [ ] what are indexers?
- [ ] dispose vs. finalize
- [ ] what are delegates?
- [ ] what is a multicast delegate?
- [ ] what is constructor chaining?
- [ ] Array.CopyTo() vs. Array.Clone()
- [ ] throw exception vs. throw clause
- [ ] what is an object pool in .NET?
- [ ] what is serialization?
- [ ] describe the singleton design pattern
- [ ] describe the MVC pattern
- [ ] describe the design pattern we use at work
