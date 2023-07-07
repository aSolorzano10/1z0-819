#

## TABLE 3.1 Order of operator precedence
| Operator                        | Symbols and examples                                            |
|---------------------------------|-----------------------------------------------------------------|
| Post-unary operators            | expression++ , expression--                                     |
| Pre-unary operators             | ++expression , --expression                                     |
| Other unary operators           | - , ! , ~ , + , (type)                                          |
| Multiplication/division/modulus | * , / , %                                                       |
| Addition/subtraction            | + , -                                                           |
| Shift operators                 | << , >> , >>>                                                   |
| Relational operators            | < , > , <= , >= , instance of                                   |
| Equal to/not equal to           | == , !=                                                         |
| Logical operators               | & , ^ ,                                                         |
| Short-circuit logical operators | &&,`\|\|`                                                       | 
| Ternary operators               | boolean expression ? expression1 : expression2                  |
| Assignment operators            | = , += , -= , *= , /= , %= , &= , ^= , `\| = , <<= , >>= , >>>= |


## TABLE 3.2 Unary operators
| Operator | Description                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------------------|
| !        | Inverts a boolean’s logical value                                                                                                   |
| +        | Indicates a number is positive, although numbers are assumed to be positive in Java unless accompanied by a negative unary operator |
| -        | Indicates a literal number is negative or negates an expression                                                                     |
| ++       | Increments a value by 1                                                                                                             |
| --       | Decrements a value by 1                                                                                                             | 
| (type)   | Casts a value to a specific type.                                                                                                   |


## TABLE 3.3 Binary arithmetic operators
| Operator | Description                                                                           |
|----------|---------------------------------------------------------------------------------------|
| +        | Adds two numeric values                                                               |
| -        | Subtracts two numeric values                                                          |
| *        | Multiplies two numeric values                                                         |
| /        | Divides one numeric value by another                                                  |
| %        | Modulus operator returns the remainder after division of one numeric value by another |


## TABLE 3.4 Simple assignment operator
| Operator | Description                                                |
|----------|------------------------------------------------------------|
| =        | Assigns the value on the right to the variable on the left | 


## TABLE 3.5 Compound assignment operators
| Operator | Description                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------|
| +=       | Adds the value on the right to the variable on the left and assigns the sum to the variable               |
| -=       | Subtracts the value on the right from the variable on the left and assigns the difference to the variable |
| *=       | Multiplies the value on the right with the variable on the left and assigns the product to the variable   |
| /=       | Divides the variable on the left by the value on the right and assigns the quotient to the variable       |

## TABLE 3.6 Equality operators
| Operator | Apply to primitives                                       | Apply to objects                                                |
|----------|-----------------------------------------------------------|-----------------------------------------------------------------|
| ==       | Returns true if the two values represent the same value   | Returns true if the two values reference the same object        |
| !=       | Returns true if the two values represent different values | Returns true if the two values do not reference the same object |


## TABLE 3.7 Relational operators
| Operator        | Description                                                                                                                                        |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <               | Returns true if the value on the left is strictly less than the value on the right                                                                 |
| <=              | Returns true if the value on the left is less than or equal to the value on the right                                                              |
| >               | Returns true if the value on the left is strictly greater than the value on the right                                                              |
| >=              | Returns true if the value on the left is greater than or equal to the value on the right                                                           |
| a instance of b | Returns true if the reference that a points to is an instance of a class, subclass, or class that implements a particular interface, as named in b |


## TABLE 3.8 Logical operators
| Operator | Description                                                             |
|----------|-------------------------------------------------------------------------|
| &        | Logical AND is true only if both values are true.                       |
| `\|      | Inclusive OR is true if at least one of the values is true.             |
| ^        | Exclusive XOR is true only if one value is true and the other is false. |


## TABLE 3.9 Short-circuit operators
| Operator | Description                                                                                                                            |
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| &&       | Short-circuit AND is true only if both values are true . If the left side is false , then the right side will not be evaluated.        |
| `\| `\|  | Short-circuit OR is true if at least one of the values is true . If the left side is true , then the right side will not be evaluated. |


