# Tables

### PROTECTING DATA IN MEMORY
- It is not stored as a String , so Java won't place it in the String
  pool, where it could exist in memory long after the code that
  used it is run.
- You can null out the value of the array element rather than
  waiting for the garbage collector to do it.


### making a class immutable.
1. Mark the class as final.
2. Mark all the instance variables private.
3. Don't define any setter methods and make fields final.
4. Don't allow referenced mutable objects to be modified.
5. Use a constructor to set all properties of the object, making a copy if needed.


### TABLE 22.1 Types of confidential data
| Category                                | Examples                                                                                                 | 
|-----------------------------------------|----------------------------------------------------------------------------------------------------------|
| Login information                       | Usernames </br>Passwords </br>Hashes of passwords                                                        |
| Banking                                 | Credit card numbers </br>Account balances </br>Credit score                                              |
| PII (Personal identifiable information) | Social Security number (or other government ID) </br>Mother's maiden name</br>Security questions/answers |


### TABLE 22.2 Methods for serialization and deserialization
| Return type | Method         | Parameters         | Description                                         | 
|-------------|----------------|--------------------|-----------------------------------------------------|
| Object      | writeReplace() | None               | Object                                              |Allows replacement of object after deserialization | 
| void        | writeObject()  | ObjectInputStream  | serializes optionally using PutField                | 
| void        | readObject()   | ObjectOutputStream | Deserializes optionally using GetField              |
| Object      | readResolve()  | None               | Allows replacement of object before deserialization |













