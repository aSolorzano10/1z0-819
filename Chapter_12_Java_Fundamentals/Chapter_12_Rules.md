# Rules

### Creating Nested Classes
- ***Inner class***: A non‐ ***static*** type defined at the member level of a class
- ***Static nested class***: A ***static*** type defined at the member level of a class
- ***Local class***: A class defined within a method body
- ***Anonymous class***: A special case of a local class that does not have a name


### DECLARING AN INNER CLASS
- Can be declared ***public***, ***protected***, package‐private (default), or ***private***.
- Can extend any class and implement interfaces
- Can be marked ***abstract*** or ***final***.
- Cannot declare ***static*** fields or methods, except for ***static final*** fields
- Can access members of the outer class including ***private*** members


### CREATING A STATIC NESTED CLASS
- The nesting creates a namespace because the enclosing class name must be used to refer to it.
- It can be made ***private*** or use one of the other access modifiers to encapsulate it.
- The enclosing class can refer to the fields and methods of the ***static*** nested class.


### Local classes have the following properties:
- They do not have an access modifier.
- They cannot be declared static and cannot declare static fields or methods, except for static final fields.
- They have access to all fields and methods of the enclosing class (when defined in an instance method).
- They can access local variables if the variables are final or effectively final

### DEFAULT INTERFACE METHOD DEFINITION RULES
1. A ***default*** method may be declared only within an interface.
2. A ***default*** method must be marked with the ***default*** keyword and include a method body.
3. A ***default*** method is assumed to be ***public***.
4. A ***default*** method cannot be marked ***abstract***, ***final***, or ***static***.
5. A ***default*** method may be overridden by a class that implements the interface.
6. If a class inherits two or more ***default*** methods with the same method signature, then the class must override the method.


### Static Interface Method Definition Rules
1. A ***static*** method must be marked with the ***static*** keyword and include a method body.
2. A ***static*** method without an access modifier is assumed to be public .
3. A ***static*** method cannot be marked ***abstract*** or ***final***.
4. A ***static*** method is not inherited and cannot be accessed in a class implementing the interface without a reference to the interface name.


### Private Interface Method Definition Rules
1. A ***private*** interface method must be marked with the ***private*** modifier and include a method body.
2. A ***private*** interface method may be called only by ***default*** and ***private*** (non‐***static***) methods within the interface definition.


### Private Static Interface Method Definition Rules
1. A ***private static*** method must be marked with the ***private*** and ***static*** modifiers and include a method body.
2. A ***private static*** interface method may be called only by other
   methods within the interface definition.

### DECLARING A FUNCTIONAL INTERFACE WITH OBJECT METHODS
- String toString()
- boolean equals(Object)
- int hashCode()

If a functional interface includes an abstract method with the same signature as a public method found in Object , then those methods do not count toward the single abstract method test.


### OVERRIDING TOSTRING(), EQUALS(OBJECT), AND HASHCODE()
- ***toString()***: The ***toString()*** method is called when you try to print an object or concatenate the object with a ***String***. It is commonly overridden with a version that prints a unique description of the instance using its instance fields.
- ***equals(Object)***: The ***equals(Object)*** method is used to compare objects, with the default implementation just using the ***==*** operator. You should override the ***equals(Object)***: method anytime you want to conveniently compare elements for equality, especially if this requires checking numerous fields.
- ***hashCode()***: Any time you override ***equals(Object)***, you must override ***hashCode()*** to be consistent. This means that for any two objects, if ***a.equals(b)*** is ***true***, then ***a.hashCode()==b.hashCode()*** must also be ***true***. If they are not consistent, then this could lead to invalid data and side effects in hash‐based collections such as ***HashMap*** and ***HashSet***.

