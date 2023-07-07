# Rules

## Creating and Manipulating Strings

1. If both operands are numeric, + means numeric addition.
2. If either operand is a String , + means concatenation.
3. The expression is evaluated left to right.

```
    System.out.println(1 + 2);          //3
    System.out.println("a" + "b" );     //ab
    System.out.println("a" + "b" + 3);  //ab3 
    System.out.println(1 + 2 + 3);      //3c 
    System.out.println("c" + 1 + 2);    //c12
```

## Comparing
### Compere()
- A negative number means the first array is smaller than the second.
- A zero means the arrays are equal.
- A positive number means the first array is larger than the second.

```
```
- If both arrays are the same length and have the same values in each spot in the same order, return zero.
- If all the elements are the same but the second array has extra elements at the end, return a negative number.
- If all the elements are the same but the first array has extra elements at the end, return a positive number.
- If the first element that differs is smaller in the first array, return a negative number.
- If the first element that differs is larger in the first array, return a positive number.

```
```
### CompareTo()
- null is smaller than any other value.
- For numbers, normal numeric order applies.
- For strings, one is smaller if it is a prefix of another.
- For strings/characters, numbers are smaller than letters.
- For strings/characters, uppercase is smaller than lowercase.