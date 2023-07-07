# Rules

### There are four formats for method references:
- Static methods
- Instance methods on a particular instance
- Instance methods on a parameter to be determined at runtime
- Constructors


### Using Lists, Sets, Maps, and Queues
- ***List***: A list is an ordered collection of elements that allows duplicate entries. Elements in a list can be accessed by an int index.
- ***Set***: A set is a collection that does not allow duplicate entries.
- ***Queue***: A queue is a collection that orders its elements in a specific order for processing. A typical queue processes its elements in a first‐in, first‐out order, but other orderings are possible.
- ***Map***: A map is a collection that maps keys to values, with no duplicate keys allowed. The elements in a map are key/value pairs.


### Three rules to know.
- The number 0 is returned when the current object is equivalent to the argument to ***compareTo()***.
- A negative number (less than 0) is returned when the current object is smaller than the argument to ***compareTo()***.
- A positive number (greater than 0) is returned when the current object is larger than the argument to ***compareTo()***.

### NAMING CONVENTIONS FOR GENERICS
- E for an element
- K for a map key
- V for a map value
- N for a number
- T for a generic data type
- S , U , V , and so forth for multiple generic types

### WHAT YOU CAN'T DO WITH GENERIC TYPES
- Calling a constructor: Writing new T() is not allowed  because at runtime it would be new Object() .
- Creating an array of that generic type: This one is the most annoying, but it makes sense because you'd be creating an array of Object values.
- Calling instanceof : This is not allowed because at runtime List<Integer> and List<String> look the same to Java thanks to type erasure.
- Using a primitive type as a generic type parameter: This isn't a big deal because you can use the wrapper class instead. If you want a type of int , just use Integer .
- Creating a static variable as a generic type parameter: This is not allowed because the type is linked to the instance of the class.

