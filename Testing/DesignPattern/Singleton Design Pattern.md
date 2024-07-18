
Singleton Design Pattern: Ensures that only one instance of a class is created and provides a global access point to that instance

The singleton design pattern is a creational design pattern that ensures a class has only one instance and provides a global point of access to it. 

#### **Purpose**:

- Ensure a class has only one instance.
- Provide a global point of access to that instance.

#### **When to Use**:

- When you need to control the instantiation of a class, ensuring only one instance exists.
- When you need a global access point to an instance of a class.
- For logging, caching, thread pools, configuration settings, and other application-wide services.

#### **Key Components**:

- **Private Constructor**: To prevent other objects from using the new operator to create instances of the class.
- **Static Instance Variable**: To hold the single instance of the class.
- **Static Accessor Method**: To provide global access to the instance.

#### **Implementation Approaches**:

1. **Eager Initialization**: Create the single instance when the class is loaded.
2. **Lazy Initialization**: Create the single instance when the `getInstance()` method is first called.
3. **Thread-safe Lazy Initialization**: Use synchronization to ensure thread-safety when creating the single instance.

#### **Benefits**:
- Controlled access to the sole instance.
- Lazily loaded instance to save resources.
- Ability to subclass the Singleton class.

#### **Drawbacks**:

- Can be difficult to unit test due to the global state.
- May introduce hidden dependencies in the code.
- Violates the single responsibility principle.

#### **Example**:  
A common example is a logging class that provides a single, global point of access for logging messages across an application. The singleton pattern ensures there is only one instance of the logging class that all parts of the application can use.