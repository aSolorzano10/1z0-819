# Rules

### Understanding Exceptions
- The code tries to connect to a website, but the Internet connection is down.
- You made a coding mistake and tried to access an invalid index in an array.
- One method calls another with a value that the method doesn’t support.

### TABLE 10.1 Types of exceptions and errors
| Type              | How to recognize                                           |
|-------------------|------------------------------------------------------------|
| Runtime exception | Subclass of RuntimeException                               | Yes|Yes|
| Checked exception | Subclass of Exception but not subclass of RuntimeException | Yesy | Yes|
| Error             | Subclass of Error                                          | No |No|


### Recognizing Exception Classes

### RUNTIMEEXCEPTION CLASSES
RuntimeException and its subclasses are unchecked exceptions
that don’t have to be handled or declared. They can be thrown
by the programmer or by the JVM. Common RuntimeException
classes include the following:

RuntimeException
- ArithmeticException Thrown when code attempts to divide by zero
- ArrayIndexOutOfBoundsException Thrown when code uses an illegal index to access an array
- ClassCastException Thrown when an attempt is made to cast an object to a class of which it is not an instance
- NullPointerException Thrown when there is a null reference where an object is required
- IllegalArgumentException Thrown by the programmer to indicate that a method has been passed an illegal or inappropriate argument
- NumberFormatException Subclass of IllegalArgumentException thrown when an attempt is made to convert a string to a numeric type but the string doesn’t have an appropriate format


### Following Order of Operation
- Resources are closed after the try clause ends and before any catch / finally clauses.
- Resources are closed in the reverse order from which they were created.


