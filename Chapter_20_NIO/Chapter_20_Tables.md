# Tables

### TABLE 20.1 File system symbols
| Symbol | Description                                        |
|--------|----------------------------------------------------|
| .      | A reference to the current directory               |
| ..     | A reference to the parent of the current directory |

### TABLE 20.2 Common NIO.2 method arguments
| Enum type          | Interface Inherited        | Enum value                                                                      | Details                                                                                                                                                                                                                                                                                                           |
|--------------------|----------------------------|---------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| LinkOption         | CopyOption </br>OpenOption | NOFOLLOW_LINKS                                                                  | Do not follow symbolic links.                                                                                                                                                                                                                                                                                     |
| StandardCopyOption | CopyOption                 | ATOMIC_MOVE </br>COPY_ATTRIBUTS </br>REPLACE_EXISTING                           | Move file as atomic file system operation. </br>Copy existing attributes to new file. </br>Overwrite file if it already exists.                                                                                                                                                                                   |
| StandardOpenOption | OpenOption                 | APPEND </br>CREATE </br>CREATE_NEW  </br>READ </br>TRUNCATE_EXISTING </br>WRITE | If file is already open for write, then append to the end. </br>Create a new file if it does not exist. </br>Create a new file only if it does not exist, fail otherwise. </br>Open for read access. </br>If file is already open for write, then erase file and append to beginning. </br>Open for write access. |
| FileVisitOption    | N/A                        | FOLLOW_LINKS                                                                    | Follow symbolic links.                                                                                                                                                                                                                                                                                            |


### TABLE 20.3 Path methods
|                            |                                |
|----------------------------|--------------------------------|
| Path of(String, String...) | Path getParent()               |
| URI toURI()                | Path getRoot()                 |
| File toFile()              | boolean isAbsolute()           |
| String toString()          | Path toAbsolutePath()          |
| int getNameCount()         | Path relativize()              |
| Path getName(int)          | Path resolve(Path)             |
| Path subpath(int, int)     | Path normalize()               |
| Path getFileName()         | Path toRealPath(LinkOption...) |


### TABLE 20.4 Files methods
|                                                  |                                                       |
|--------------------------------------------------|-------------------------------------------------------|
| boolean exists(Path, LinkOption...)              | Path move(Path, Path, CopyOption...)                  |
| boolean isSameFile(Path,Path)                    | void delete(Path)                                     |
| Path createDirectory(Path,FileAttribute<?>...)   | boolean deleteIfExists(Path)                          |
| Path createDirectories(Path,FileAttribute<?>...) | BufferedReader newBufferedReader(Path)                |
| Path copy(Path, Path, CopyOption...)             | BufferedWriter newBufferedWriter(Path, OpenOption...) |
| long copy(InputStream, Path,CopyOption...)       | List<String> readAllLines(Path)                       |
| long copy(Path,OutputStream)                     |                                                       |


### TABLE 20.5 The attributes and view types
| Attributes interface | View interface         | Description                                                                                         |
|----------------------|------------------------|-----------------------------------------------------------------------------------------------------|
| BasicFileAttributes  | BasicFileAttributeView | Basic set of attributes supported by all file systems                                               |
| DosFileAttributes    | DosFileAttributeView   | Basic set of attributes along with those supported by DOS/Windows‐based systems                     |
| PosixFileAttributes  | PosixFileAttributeView | Basic set of attributes along with those supported by POSIX systems, such as UNIX, Linux, Mac, etc. |


### TABLE 20.6 Walking a directory with a cycle using breadth‐first search

### TABLE 20.7 Comparison of java.io.File and NIO.2 methods
| Legacy I/O File method   | NIO.2 method                    |
|--------------------------|---------------------------------|
| file.delete()            | Files.delete(path)              |
| file.exists()            | Files.exists(path)              |
| file.getAbsolutePath()   | path.toAbsolutePath()           |
| file.getName()           | path.getFileName()              |
| file.getParent()         | path.getParent()                |
| file.isDirectory()       | Files.isDirectory(path)         |
| file.isFile()            | Files.isRegularFile(path)       |
| file.lastModified()      | Files.getLastModifiedTime(path) |
| file.length()            | Files.size(path)                |
| file.listFiles()         | Files.list(path)                |
| file.mkdir()             | Files.createDirectory(path)     |
| file.mkdirs()            | Files.createDirectories(path)   |
| file.renameTo(otherFile) | Files.move(path,otherPath)      |


