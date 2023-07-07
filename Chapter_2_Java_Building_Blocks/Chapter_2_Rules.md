# Rules

## The Primitive Types
- The float and double types are used for floating-point (decimal) values.
- A float requires the letter f following the number so Java knows it is a float.
- The byte , short , int , and long types are used for numbers without decimal points. In mathematics, these are all referredto as integral values, but in Java, int and Integer refer to specific types.
- Each numeric type uses twice as many bits as the smaller similar type. For example, short uses twice as many bits as byte does.
- All of the numeric types are signed in Java. This means that they reserve one of their bits to cover a negative range. For example, byte ranges from -128 to 127 . You might be surprised that the range is not -128 to 128 . Don’t forget, 0 needs to be accounted for too in the range.


## USING REFERENCE TYPES
- A reference can be assigned to another object of the same or compatible type.
- A reference can be assigned to a new object using the new keyword.


## There are only four rules to remember for legal identifiers:
- Identifiers must begin with a letter, a $ symbol, or a _ symbol.
- Identifiers can include numbers but not start with them.
- Since Java 9, a single underscore _ is not allowed as an identifier.
- You cannot use the same name as a Java reserved word. A reserved word is special word that Java has held aside so that you are not allowed to use it. Remember that Java is case sensitive, so you can use versions of the keywords that only
  differ in case. Please don’t, though.


## Review of var Rules

1. A var is used as a local variable in a constructor, method, or initializer block.
2. A var cannot be used in constructor parameters, method parameters, instance variables, or class variables.
3. A var is always initialized on the same line (or statement) where it is declared
4. The value of a var can change, but the type cannot.
5. A var cannot be initialized with a null value without a type.
6. A var is not permitted in a multiple-variable declaration.
7. A var is a reserved type name but not a reserved word, meaning it can be used as an identifier except as a class, interface, or enum name.

## REVIEWING SCOPE

- Local variables: In scope from declaration to end of block
- Instance variables: In scope from declaration until object eligible for garbage collection
- Class variables: In scope from declaration until program ends

## TRACING ELIGIBILITY

An object will remain on the heap until it is no longer reachable. An object is no longer reachable when one of two situations occurs:

- The object no longer has any references pointing to it.
- All references to the object have gone out of scope.
