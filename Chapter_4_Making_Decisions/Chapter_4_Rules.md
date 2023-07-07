# Rules

## Switch Data Types
The following is a list of all data types supported by switch statements:
- int and Integer
- byte and Byte
- short and Short
- char and Character
- String
- enum values
- var (if the type resolves to one of the preceding types)

## Working with for Loops "for"

1. Creating an Infinite Loop
```
   for( ; ; )
   System.out.println("Hello World");
```

2. Adding Multiple Terms to the for Statement
```
    int x = 0;
        for(long y = 0, z = 4; x < 5 && y < 10; x++, y++) {System.out.print(y + " "); }
    System.out.print(x + " ");
```

3. Redeclaring a Variable in the Initialization Block
```
   int x = 0;
   for(int x = 4; x < 5; x++) {
   System.out.print(x + " ");
```

4. Using Incompatible Data Types in the Initialization Block
```
    int x = 0;
        for(long y = 0, int z = 4; x < 5; x++) {   // DOES NOT COMPILE
        System.out.print(y + " ");
    }
   
```

5. Using Loop Variables Outside the Loop
```
    for(long y = 0, x = 4; x < 5 && y < 10; x++, y++) {
        System.out.print(y + " ");
    }
    System.out.print(x); // DOES NOT COMPILE
```

