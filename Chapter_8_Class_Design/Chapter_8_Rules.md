# Rules

## Instance Initialization

### Initialize Instance of X
1. If there is a superclass Y of X, then initialize the instance of Y first.
2. Process all instance variable declarations in the order they appear in the class.
3. Process all instance initializers in the order they appear in the class.
4. Initialize the constructor including any overloaded constructors referenced with this().


### REVIEWING CONSTRUCTOR RULES
1. The first statement of every constructor is a call to an overloaded constructor via this() , or a direct parent constructor via super().
2. If the first statement of a constructor is not a call to this() or super() , then the compiler will insert a no-argument super() as the first statement of the constructor.
3. Calling this() and super() after the first statement of a constructor results in a compiler error.
4. If the parent class doesn’t have a no-argument constructor, then every constructor in the child class must start with an explicit this() or super() constructor call.
5. If the parent class doesn’t have a no-argument constructor and the child doesn’t define any constructors, then the child class will not compile.
6. If a class only defines private constructors, then it cannot be extended by a top-level class.
7. All final instance variables must be assigned a value exactly once by the end of the constructor. Any final instance variables not assigned a value will be reported as a compiler error on the line the constructor is declared.


### Rules Override
1. The method in the child class must have the same signature as the method in the parent class.
2. The method in the child class must be at least as accessible as the method in the parent class.
3. The method in the child class may not declare a checked exception that is new or broader than the class of any exception declared in the parent class method.
4. If the method returns a value, it must be the same or a subtype of the method in the parent class, known as covariant return types.


### DEFINING SUBTYPE AND SUPERTYPE
If we define X to be a subtype of Y, then one of the following is true:
- X and Y are classes, and X is a subclass of Y.
- X and Y are interfaces, and X is a subinterface of Y.
- X is a class and Y is an interface, and X implements Y (either directly or through an inherited class).


### Hiding Static Methods
5. The method defined in the child class must be marked as static if it is marked as static in a parent class.


### INTERFACE PRIMER
- An interface can define abstract methods.
- A class can implement any number of interfaces.
- A class implements an interface by overriding the inherited abstract methods.
- An object that implements an interface can be assigned to a reference for that interface.


### Object vs Reference
1. The type of the object determines which properties exist within the object in memory.
2. The type of the reference to the object determines which methods and variables are accessible to the Java program.


### CASTING OBJECTS
1. Casting a reference from a subtype to a supertype doesn’t require an explicit cast.
2. Casting a reference from a supertype to a subtype requires an explicit cast.
3. The compiler disallows casts to an unrelated class.4. At runtime, an invalid cast of a reference to an unrelated type results in a ClassCastException being thrown.

