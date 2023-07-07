# Rules

## While it is possible to run SQL directly with Statement, you
shouldn't. PreparedStatement is far superior for the following
reasons:

- Performance: In most programs, you run similar queries multiple times. A PreparedStatement figures out a plan to run the SQL well and remembers it.
- Security: As you will see in Chapter 22, “Security,” you are protected against an attack called SQL injection when using a PreparedStatement correctly.
- Readability: It's nice not to have to deal with string concatenation in building a query string with lots of parameters.
- Future use: Even if your query is being run only once or doesn't have any parameters, you should still use a PreparedStatement . That way future editors of the code won't add a variable and have to remember to change to PreparedStatement then.


### TABLE 21.2 SQL runnable by the execute method
| Method             | DELETE | INSERT | SELECT | UPDATE |
|--------------------|--------|--------|--------|--------|
| ps.execute()       | Yes    | Yes    | Yes    | Yes    |
| ps.executeQuery()  | No     | No     | Yes    | No     |
| ps.executeUpdate() | Yes    | Yes    | No     | Yes    |


### TABLE 21.3 Return types of execute methods
| Method             | Return Type | What is returned for type SELECT | What is returned for DELETE/INSERT/UPDATE |
|--------------------|-------------|----------------------------------|-------------------------------------------|
| ps.execute()       | boolean     | true                             | false                                     |
| ps.executeQuery()  | ResultSet   | The rows and columns returned    | n/a                                       |
| ps.executeUpdate() | int         | n/a                              | Number of rows added/changed/removed      |
 

### TABLE 21.4 PreparedStatement methods
| Method name | Parameter type | Example database type |
|-------------|----------------|-----------------------|
| setBoolean  | Boolean        | BOOLEAN               |
| setDouble   | Double         | DOUBLE                |
| setInt      | Int            | INTEGER               |
| setLong     | Long           | BIGINT                |
| setObject   | Object         | Any type              |
| setString   | String         | CHAR , VARCHAR        |


### TABLE 21.5 ResultSet get methods
| Method name | Return type |
|-------------|-------------|
| getBoolean  | boolean     |
| getDouble   | double      |
| getInt      | int         |
| getLong     | long        |
| getObject   | Object      |
| getString   | String      |


### TABLE 21.6 Sample stored procedures
| Name                   | Parameter name | Parameter type | Description                                                                                 |
|------------------------|----------------|----------------|---------------------------------------------------------------------------------------------|
| read_e_names()         | n/a            | n/a            | Returns all rows in the names table that have a name beginning with an E                    |
| read_names_by_letter() | prefix         | IN             | Returns all rows in the names table that have a name beginning with the specified parameter |
| magic_number()         | Num            | OUT            | Returns the number 42                                                                       |
| double_number()        | Num            | INOUT          | Multiplies the parameter by two and returns that number                                     |


### TABLE 21.7 Stored procedure parameter types
|                                  | IN  | OUT | INOUT |
|----------------------------------|-----|-----|-------|
| Used for input                   | Yes | No  | Yes   |
| Used for output                  | No  | Yes | Yes   |
| Must set parameter value         | Yes | No  | Yes   |
| Must call registerOutParameter() | No  | Yes | Yes   |
| Can include ?=                   | No  | Yes | Yes   |










