# Tables

### TABLE 19.1 Commonly used java.io.File methods
| Method  Name                | Description                                                                                                                                                       |
|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| boolean delete()            | Deletes the file or directory and returns true only if successful. If this instance denotes a directory, then the directory must be empty in order to be deleted. |
| boolean exists()            | Checks if a file exists                                                                                                                                           |
| String getAbsolutePath()    | Retrieves the absolute name of the file or directory within the file system                                                                                       |
| String getName()            | Retrieves the name of the file or directory.                                                                                                                      |
| String getParent()          | Retrieves the parent directory that the path is contained in or *null* if there is none                                                                           |
| boolean isDirectory()       | Checks if a File reference is a directory within the file system                                                                                                  |
| boolean isFile()            | Checks if a *File* reference is a file within the file system                                                                                                     |
| long lastModified()         | Returns the number of milliseconds since the epoch (number of milliseconds since 12 a.m. UTC on January 1, 1970) when the file was last modified                  |
| long length()               | Retrieves the number of bytes in the file                                                                                                                         |
| File[] listFiles()          | Retrieves a list of files within a directory                                                                                                                      |
| boolean mkdir()             | Creates the directory named by this path                                                                                                                          |
| boolean mkdirs()            | Creates the directory named by this path including any nonexistent parent directories                                                                             |
| boolean renameTo(File dest) | Renames the file or directory denoted by this path to dest and returns true only if successful                                                                    |


### TABLE 19.2 The java.io abstract stream base classes
| Class Name   | Description                                     |
|--------------|-------------------------------------------------|
| InputStream  | Abstract class for all input byte streams       |
| OutputStream | Abstract class for all output byte streams      |
| Reader       | Abstract class for all input character streams  |
| Writer       | Abstract class for all output character streams |


### TABLE 19.3 The java.io concrete stream classes
| Class Name           | Low/High Level | Description                                                                                                    |
|----------------------|----------------|----------------------------------------------------------------------------------------------------------------|
| FileInputStream      | Low            | Reads file data as bytes                                                                                       |
| FileOutputStream     | Low            | Writes file data as bytes                                                                                      |
| FileReader           | Low            | Reads file data as characters                                                                                  |
| FileWriter           | Low            | Writes file data as characters                                                                                 |
| BufferedInputStream  | High           | Reads byte data from an existing *InputStream* in a buffered manner, which improves efficiency and performance |
| BufferedOutputStream | High           | Writes byte data to an existing *OutputStream* in a buffered manner, which improves efficiency and performance | 
| BufferedReader       | High           | Reads character data from an existing *Reader* in a buffered manner, which improves efficiency and performance |
| BufferedWriter       | High           | Writes character data to an existing Writer in a buffered manner, which improves efficiency and performance    |
| ObjectInputStream    | High           | Deserializes primitive Java data types and graphs of Java objects from an existing *InputStream*               |
| ObjectOutputStream   | High           | Serializes primitive Java data types and graphs of Java objects to an existing *OutputStream*                  |
| PrintStream          | High           | Writes formatted representations of Java objects to a binary stream                                            |
| PrintWriter          | High           | Writes formatted representations of Java objects to a character stream                                         |


### TABLE 19.4 Common I/O stream methods 
| Stream Class                  | Method Name                                                                                     | Description                                                                                             |
|-------------------------------|-------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| All streams                   | void close()                                                                                    | Closes stream and releases resources                                                                    |
| All input streams             | int read()                                                                                      | Reads a single byte or returns ‐1 if no bytes were available                                            |
| InputStream  </br>Reader      | int read(byte[] b)      </br>int read(char[] c)                                                 | Reads values into a buffer. Returns number of bytes read                                                |  
| InputStream   </br>Reader     | int read(byte[] b, int offset, int length)  </br>int read(char[] c, int offset, int length)     | Reads up to *length* values into a buffer starting from position *offset*. Returns number of bytes read |
| All output streams            | void write(int)                                                                                 | Writes a single byte                                                                                    |
| OutputStream      </br>Writer | void write(byte[] b)      </br>void write(char[]c)                                              | Writes an array of values into the stream                                                               |
| OutputStream   </br>Writer    | void write(byte[] b, int offset, int length)   </br>void write(char[]c, int offset, int length) | Writes length *values* from an array into the stream, starting with an *offset* index                   |
| All input streams             | boolean markSupported()                                                                         | Returns *true* if the stream class supports *mark()*                                                    |
| All input streams             | mark(int readLimit)                                                                             | Marks the current position in the stream                                                                |
| All input streams             | void reset()                                                                                    | Attempts to reset the stream to the mark() position                                                     |
| All input streams             | long skip(long n)                                                                               | Reads and discards a specified number of characters                                                     |
| All input streams             | void flush()                                                                                    | Flushes buffered data through the stream                                                                |

 
### TABLE 19.5 Common print stream format() symbols
| Symbol | Description                                                    |
|--------|----------------------------------------------------------------|
| %s     | Applies to any type, commonly String values                    |
| %d     | Applies to integer values like int and long                    |
| %f     | Applies to floating‐point values like float and double         |
| %n     | Inserts a line break using the system‐dependent line separator |



