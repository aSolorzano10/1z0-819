# Rules

### PROTECTING DATA IN MEMORY
- It is not stored as a String , so Java won't place it in the String pool, where it could exist in memory long after the code that used it is run.
- You can null out the value of the array element rather than waiting for the garbage collector to do it.