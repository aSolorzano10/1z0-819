# Tables

### TABLE 12.1 Modifiers in nested classes
| Permitted Modifiers | Inner class | static nested class | Local class | Anonymous class |
|---------------------|-------------|---------------------|-------------|-----------------|
| Access modifiers    | All         | All                 | None        | None            |
| abstract            | Yes         | Yes                 | Yes         | No              |
| Final               | Yes         | Yes                 | Yes         | No              |


### TABLE 12.2 Members in nested classes
| Permitted  Members | Inner class   | static nested class | Local class   | Anonymous class |
|--------------------|---------------|---------------------|---------------|-----------------|
| Instance methods   | Yes           | Yes                 | Yes           | Yes             |
| Instance variables | Yes           | Yes                 | Yes           | Yes             |
| static methods     | No            | Yes                 | No            | No              |
| static varibale    | Yes(if final) | Yes                 | Yes(if final) | Yes(if final)   |


### TABLE 12.3 Nested class access rules
|                                                                    | Inner Class | static nested class | Local class                                                             | Anonymous class                                                          |
|--------------------------------------------------------------------|-------------|---------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------|
| Can extend any class or implement any number of interfaces         | Yes         | Yes                 | Yes                                                                     | No—must have exactly one superclass or one interface                     |
| Can access instance members of enclosing class without a reference | Yes         | No                  | Yes (if declared in an instance method)                                 | Yes (if declared in an instance method)                                  |
| Can access local variables of enclosing method                     | N/A         | N/A                 | Yes (if final or effectively final) Yes (if final or effectively final) | Yes (if final or effectively fihnal) Yes (if final or effectively final) |


### TABLE 12.4 Interface member types
|                       | Since Java version | Membership type | Required modifiers  | Implicit modifiers            | Has  value or | 
|-----------------------|--------------------|-----------------|---------------------|-------------------------------|---------------|
| Constant variable     | 1.0                | Class           | -                   | public </br>static </br>final | Yes           |
| Abstract method       | 1.0                | Instance        | -                   | public </br>abstract          | No            |
| Default method        | 8                  | Instance        | default             | public                        | Yes           |
| Static method         | 8                  | Class           | static              | public                        | Yes           |
| Private method        | 9                  | Instance        | private             | -                             | Yes           |
| Private static method | 9                  | Class           | Private </br>static | -                             | Yes           |


### TABLE 12.5 Interface member access
|                       | Accessible from default and private methods within the interface definition? | Accessible Accessible from static static within the interface definition? | Accessible from instance methods implementing or extending the interface? | Accesible outisde the interface whitout an instance of interface? | 
|-----------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------|
| Constant variable     | Yes                                                                          | Yes                                                                       | Yes                                                                       | Yes                                                               |
| abstract method       | Yes                                                                          | No                                                                        | Yes                                                                       | No                                                                |
| default method        | Yes                                                                          | No                                                                        | Yes                                                                       | No                                                                |
| private method        | Yes                                                                          | No                                                                        | No                                                                        | No                                                                |
| static method         | Yes                                                                          | Yes                                                                       | Yes                                                                       | Yes                                                               |
| private static method | Yes                                                                          | Yes                                                                       | No                                                                        | No                                                                |


### 