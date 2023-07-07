# Rules

### ABSOLUTE VS. RELATIVE PATHS

- If a path starts with a forward slash (/), it is absolute, with / as the root directory. Examples: /bird/parrot.png and /bird/../data/./info
- If a path starts with a drive letter (c:), it is absolute, with the drive letter as the root directory. Examples: c:/bird/parrot.png and d:/bird/../data/./info
- Otherwise, it is a relative path. Examples: bird/parrot.png and bird/../data/./info

### Handling Methods That Declare IOException
Many of the methods presented in this chapter declare IOException . Common causes of a method throwing this exception include the following:

- Loss of communication to underlying file system.
- File or directory exists but cannot be accessed or modified.
- File exists but cannot be overwritten.
- File or directory is required but does not exist.



