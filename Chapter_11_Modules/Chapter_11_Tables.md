# Tables

### TABLE 11.1 Options you need to know for using modules with javac
| Use for                   | Abbreviation | Long form            | 
|---------------------------|--------------|----------------------|
| Directory for class files | -d <dir>     | n/a                  |
| Module path               | -p <path>    | --module-path <path> |


### TABLE 11.2 Options you need to know for using modules with java
| Use for     | Abbreviation | Long form            |
|-------------|--------------|----------------------|
| Module name | -m <name>    | --module <name>      |
| Module path | -p <path>    | --module-path <path> |


### TABLE 11.3 Access control with modules
| Level                     | Within module code                             | Outside module                                       |
|---------------------------|------------------------------------------------|------------------------------------------------------|
| private                   | Available only within class                    | No access                                            |
| default (package-private) | Available only within package                  | No access                                            |
| protected                 | Available only within package or to subclasses | Accessible to subclasses only if package is exported |
| public                    | Available to all classes                       | Accessible only if package is exported               |


### TABLE 11.4 Modes using jmod
| Operation | Description                                             |
|-----------|---------------------------------------------------------|
| create    | Creates a JMOD file.                                    |
| extract   | Extracts all files from the JMOD. Works like unzipping. |
| describe  | Prints the module details such as requires .            |
| list      | Lists all files in the JMOD file.                       |
| hash      | Shows a long string that goes with the file             |


### TABLE 11.5 Comparing command-line operations
| Description             | Syntax                                                                                                                                                                             |
|-------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Compile nonmodular code | javac -cp classpath -d directory classesToCompile   <br/>javac --class-path classpath -d directory classesToCompile  <br/>javac -classpath classpath -d directory classesToCompile |
| Run nonmodular code     | java -cp classpath package.className <br/>java -classpath classpath package.className <br/>java --class-path classpath package.className                                           |
| Compile a module        | javac -p moduleFolderName -d directory classesToCompileIncludingModuleInfo <br/>javac --module-path moduleFolderName -d directory classesToCompileIncludingModuleInfo              |
| Run a module            | java -p moduleFolderName -m moduleName/package.className <br/> java --module-path moduleFolderName --module moduleName/package.className                                           |
| Describe a module       | java -p moduleFolderName -d moduleName <br/>java --module-path moduleFolderName --describe- module moduleName  <br/>jar --file jarName --describe-module <br/>jar -f jarName -d    |
| List available modules  | java --module-path moduleFolderName --list-modules <br/>java -p moduleFolderName --list-modules <br/>java --list-modules                                                           |
| View dependencies       | jdeps -summary --module-path moduleFolderName jarName <br/>jdeps -s --module-path moduleFolderName jarName                                                                         |
| Show module resolution  | java --show-module-resolution -p moduleFolderName -m moduleName </br>java --show-module-resolution --module-path moduleFolderName --module moduleName                              | 


## TABLE 11.6 Options you need to know for the exam: javac
| Option                                                                    | Description                              |
|---------------------------------------------------------------------------|------------------------------------------|
| -cp <classpath> </br>-classpath <classpath> </br>--class-path <classpath> | Location of JARs in a nonmodular program |
| -d <dir>                                                                  | Directory to place generated class files |
| -p <path> </br>--module-path <path>                                       | Location of JARs in a modular program    |


## TABLE 11.7 Options you need to know for the exam: java
| Option                              | Description                                        |
|-------------------------------------|----------------------------------------------------|
| -p <path> </br>--module-path <path> | Location of JARs in a modular program              |
| -m <name> </br>--module <name>      | Module name to run                                 |
| -d </br>--describe-module           | Describes the details of a module                  |
| --list-modules                      | Lists observable modules without running a program |
| --show-module- resolution           | Shows modules when running program                 |


## TABLE 11.8 Options you need to know for the exam: jar
| Option                    | Description                                             |
|---------------------------|---------------------------------------------------------|
| -c </br>--create          | Create a new JAR file                                   |
| -v </br>--verbose         | Prints details when working with JAR files              |
| -f </br>--file            | JAR filename                                            |
| -C                        | Directory containing files to be used to create the JAR |
| -d </br>--describe-module | Describes the details of a module                       |


## TABLE 11.9 Options you need to know for the exam: jdeps
| Option               | Description                           |
|----------------------|---------------------------------------|
| --module-path <path> | Location of JARs in a modular program |
| -s </br>-summary     | Summarizes output                     |



