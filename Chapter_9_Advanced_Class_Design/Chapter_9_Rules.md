# Rules

### Abstract Class Definition Rules
1. Abstract classes cannot be instantiated.
2. All top-level types, including abstract classes, cannot be marked protected or private.
3. Abstract classes cannot be marked final.
4. Abstract classes may include zero or more abstract and nonabstract methods.
5. An abstract class that extends another abstract class inherits all of its abstract methods.
6. The first concrete class that extends an abstract class must provide an implementation for all of the inherited abstract methods.
7. Abstract class constructors follow the same rules for initialization as regular constructors, except they can be called only as part of the initialization of a subclass.
   

### Abstract Method Definition Rules
1. Abstract methods can be defined only in abstract classes or interfaces.
2. Abstract methods cannot be declared private or final .
3. Abstract methods must not provide a method body/implementation in the abstract class in which they are declared.
4. Implementing an abstract method in a subclass follows the same rules for overriding a method, including covariant return types, exception declarations, etc.

### Rules for class declarations
- A Java file may have at most one public top-level class or interface, and it must match the name of the file.
- A top-level class or interface can only be declared with public or package-private access.

### INHERITING AN INTERFACE
- An interface can be inherited in one of three ways.An interface can extend another interface.
- A class can implement an interface.
- A class can extend another class whose ancestor implements an interface.


### REVIEWING INTERFACE RULES
1. ***Interface Definition Rules*** Interfaces cannot be instantiated.
2. All top-level types, including interfaces, cannot be marked ***protected*** or ***private***.
3. Interfaces are assumed to be abstract and cannot be marked final.
4. Interfaces may include zero or more abstract methods.
5. An interface can extend any number of interfaces.
6. An interface reference may be cast to any reference that inherits the interface, although this may produce an exception at runtime if the classes aren’t related.
7. The compiler will only report an unrelated type error for an ***instanceof*** operation with an interface on the right side if the reference on the left side is a ***final*** class that does not inherit the interface.
8. An interface method with a body must be marked ***default***, ***private***, ***static***, or private static (covered when studying for the 1Z0-816 exam).
   

### Abstract Interface Method Rules
1. Abstract methods can be defined only in abstract classes or interfaces.
2. Abstract methods cannot be declared ***private*** or ***final***.
3. Abstract methods must not provide a method body/implementation in the abstract class in which is it declared.
4. Implementing an abstract method in a subclass follows the same rules for overriding a method, including covariant return types, exception declarations, etc.
5. Interface methods without a body are assumed to be ***abstract*** and ***public***.

### Interface Variables Rules
1. Interface variables are assumed to be ***public***, ***static***, and ***final***.
2. Because interface variables are marked ***final***, they must be initialized with a value when they are declared.