# Tablas

## TABLE 6.1 Valid lambdas
| Lambda                                       | #parameters |
|----------------------------------------------|-------------|
| () -> true                                   | 0           |
| a -> a.startsWith("test")                    | 1           |
| (String a) -> a.startsWith("test")           | 1           |
| (a, b) -> a.startsWith("test")               | 2           |
| (String a, String b) -> a.startsWith("test") | 2           |


## TABLE 6.2 Invalid lambdas that return boolean
| Invalid lambda                       | Reason              |
|--------------------------------------|---------------------|
| a, b -> a.startsWith("test")         | Missing parentheses |
| a -> { a.startsWith("test"); }       | Missing return      |
| a -> { return a.startsWith("test") } | Missing semicolon   |


## TABLE 6.3 Basic functional interfaces
| Functional interface | # parameters | Return type       |
|----------------------|--------------|-------------------|
| Comparator           | Two          | int               |
| Consumer             | One          | void              |
| Predicate            | One          | boolean           |
| Supplier             | None         | One (type varies) |


## TABLE 6.4 Rules for accessing a variable from a lambda body inside a method
| Variable type     | Rule                         |
|-------------------|------------------------------|
| Instance variable | Allowed                      |
| Static variable   | Allowed                      |
| Local variable    | Allowed if effectively final |
| Method parameter  | Allowed if effectively final |
| Lambda parameter  | Allowed                      |


