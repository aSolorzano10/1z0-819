# Tables

### TABLE 10.1 Types of exceptions and errors

| Type              | How to recognize                          | Okay for program to catch? | Is program required to handle or declare? |
|-------------------|-------------------------------------------|----------------------------|-------------------------------------------|
| Runtime exception | Subclass of RuntimeException              | Yes                        | No                                        |
| Checked exception | Subclass of Exception but not subclass of | Yes                        | Yes                                       | 
| Error             | Subclass of Error                         | No                         | No                                        |

### TABLE 10.2 Legal vs. illegal configurations with a traditional try statement
|                        | 0 finally blocks | 1 finally block | 2 or more finally blocks |
|------------------------|------------------|-----------------|--------------------------|
| 0 catch blocks         | Not legal        | Legal           | Not legal                |
| 1 or more catch blocks | Legal            | Legal           | Not legal                |


### TABLE 10.3 Legal vs. illegal configurations with a try-with-resources statement
|                        | 0 finally blocks | 1 finally block | 2 or more finally blocks |
|------------------------|------------------|-----------------|--------------------------|
| 0 catch blocks         | Legal            | Legal           | Not legal                |
| 1 or more catch blocks | Legal            | Legal           | Not legal                |


