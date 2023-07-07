# Tables

### TABLE 17.1 Common module directives
| Derivative                        | Description                                                                                    |
|-----------------------------------|------------------------------------------------------------------------------------------------|
| exports <package>                 | Allows all modules to access the package                                                       |
| exports <package> to <module>     | Allows a specific module to access the package                                                 |
| requires <module>                 | Indicates module is dependent on another module                                                |
| requires transitive <module>      | Indicates the module and that all modules that use this module are dependent on another module |
| uses <interface>                  | Indicates that a module uses a service                                                         |
| provides <interface> with <class> | Indicates that a module provides an implementation of a service                                |


### TABLE 17.2 Practicing with automatic module names
| # | Description                                                         | Example 1                     | Example 2     |
|---|---------------------------------------------------------------------|-------------------------------|---------------|
| 1 | Beginning JAR name                                                  | commons2‐x‐1.0.0‐SNAPSHOT.jar | mod_$‐1.0.jar |
| 2 | Remove file extension                                               | commons2‐x‐1.0.0‐SNAPSHOT     | mod_$‐1.0     |
| 3 | Remove version information                                          | commons2‐x                    | mod_$         |
| 4 | Replace special characters                                          | commons2.x                    | mod..         |
| 5 | Replace sequence of dots                                            | commons2.x                    | mod.          |
| 6 | Remove leading/trailing dots (results in the automatic module name) | commons2.x                    | mod           |



### TABLE 17.3 Properties of modules types
| Property                                                         | Named                         | Atomatic     | Unnamed            |
|------------------------------------------------------------------|-------------------------------|--------------|--------------------|
| A ______ module contains a module‐info file?                     | Yes                           | No           | Ignored if present |
| A ______ module exports which packages to other modules?         | Those in the module‐info file | All packages | No packages        |
| A ______ module is readable by other modules on the module path? | Yes                           | Yes          | No                 |
| A ______ module is readable by other JARs on the classpath?      | Yes                           | Yes          | yes                |


### TABLE 17.4 Common modules
| Module name  | What it contains                                | Coverage in book                       |
|--------------|-------------------------------------------------|----------------------------------------|
| java.base    | Collections, Math, IO, NIO.2, Concurrency, etc. | Most of this book                      |
| java.desktop | Abstract Windows Toolkit (AWT) and Swing        | Not on the exam beyond the module name | 
| java.logging | Logging                                         | Not on the exam beyond the module name | 
| java.sql     | JDBC                                            | Chapter 21, “JDBC”                     |
| java.xml     | Extensible Markup Language (XML)                | Not on the exam beyond the module name |


### TABLE 17.5 Java modules prefixed with java
|                     |                    |                     |
|---------------------|--------------------|---------------------|
| java.base           | java.naming        | java.smartcardio    |
| java.compiler       | java.net .http     | java.sql            |
| java.datatransfer   | java.prefs         | java.sql.rowset     | 
| java.desktop        | java.rmi           | java.transaction.xa |
| java.instrument     | java.scripting     | java.xml            |
| java.logging        | java.se            | java.xml.crypto     |
| java.management     | java.security.jg   |                     |
| java.management.rmi | java.security.sasl |                     |


### TABLE 17.6 Java modules prefixed with jdk
|                     |                      |                        |
|---------------------|----------------------|------------------------|
| jdk.accessiblity    | jdk.jconsole         | jdk.naming.dns         |
| jdk.attach          | jdk.jdeps            | jdk.naming.rmi         |
| jdk.charsets        | jdk.jdi              | jdk.net                |
| jdk.compiler        | jdk.jdwp.agent       | jdk.pack               |
| jdk.crypto.cryptoki | jdk.jfr              | jdk.rmic               |
| jdk.crypto.ec       | jdk.jlink            | jdk.scripting.nash orn |
| jdk.dynalink        | jdk.jshell           | jdk.sctp               |
| jdk.editpad         | jdk.jsobject         | jdk.security.auth      |
| jdk.hotspot.agent   | jdk.jstatd           | jdk.security.jgss      |
| jdk.httpserver      | jdk.localdata        | jdk.xml.dom            |
| jdk.jartool         | jdk.management       | jdk.zipfs              |
| jdk.javadoc         | jdk.management.agent |                        |
| jdk.jcmd            | jdk.management.jfr   |                        |


### TABLE 17.7 Comparing migration strategies
| Category                             | Bottom‐Up                       | Top‐Down                            |
|--------------------------------------|---------------------------------|-------------------------------------|
| A project that depends on all others | Unnamed module on the classpath | Named module on the module path     |
| A project that has no dependencies   | Named module on the module path | Automatic module on the module path |


### TABLE 17.8 Reviewing services
| Artifact                   | Part of the service | Directives required in *module‐info.java* |
|----------------------------|---------------------|-------------------------------------------|
| Service provider interface | Yes                 | exports                                   |
| Service provider           | No                  | requires provides                         |
| Service locator            | Yes                 | exports requires uses                     |
| Consumer                   | No                  | requires                                  | 

