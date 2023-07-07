# Tables

### TABLE 13.1 Values for the @Target annotation
| ElementType value | Applies to                                                        |
|-------------------|-------------------------------------------------------------------|
| TYPE              | Classes, interfaces, enums, annotations                           |
| FIELD             | Instance and static variables, enum values                        |
| METHOD            | Method declarations                                               |
| PARAMETER         | Constructor, method, and lambda parameters                        |
| CONSTRUCTOR       | Constructor declarations                                          |
| LOCAL_VARIABLE    | Local variables                                                   |
| ANNOTATION_TYPE   | Annotations                                                       |
| PACKAGE*          | Packages declared in package‐info.java                            |
| TYPE_PARAMETER    | Parameterized types, generic declarations                         |
| TYPE_USE          | Able to be applied anywhere there is a Java type declared or used |
| MODULE*           | Modules                                                           |


### TABLE 13.2 Values for the @Retention annotation
| RetentionPolicy value | Description                                                                        |
|-----------------------|------------------------------------------------------------------------------------|
| SOURCE                | Used only in the source file, discarded by the compiler                            |
| CLASS                 | Stored in the .class file but not available at runtime (default compiler behavior) |
| RUNTIME               | Stored in the .class file and available at runtime                                 |


### TABLE 13.3 Annotation‐specific annotations
| Annotation  | Marker annotation | Type of value()       | Default compiler behavior (if annotation not present)                             |
|-------------|-------------------|-----------------------|-----------------------------------------------------------------------------------|
| @Target     | No                | Array of Element Type | Annotation able to be applied to all locations except TYPE_USE and TYPE_PARAMETER |
| @Retention  | No                | RetentionPolicy       | RetentionPolicy.CLASS                                                             |
| @Documented | Yes               | —                     | Annotations are not included in the generated Javadoc.                            |
| @Inherited  | Yes               | —                     | Annotations in supertypes are not inherited.                                      |
| @Repeatable | No                | Annotation            | Annotation cannot be repeated.                                                    |


### TABLE 13.4 Common @SuppressWarnings values
| Value         | Description                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------|
| "deprecation" | Ignore warnings related to types or methods marked with the ***@Deprecated*** annotation.          |
| "unchecked"   | Ignore warnings related to the use of raw types, such as ***List*** instead of ***List<String>***. |


### TABLE 13.5 Understanding common annotations
| Annotation           | Marker annotation | Type of value() | Optional members                              |
|----------------------|-------------------|-----------------|-----------------------------------------------|
| @Override            | Yes               | —               | —                                             |
| @FunctionalInterface | Yes               | —               | —                                             |
| @Deprecated          | No                | —               | String since() </br>boolean </br>forRemoval() |
| @SuppressWarnings    | No                | String[]        | -                                             |
| @SafeVarargs         | Yes               | -               | -                                             |


### TABLE 13.6 Applying common annotations
| Annotations           | Applies to             | Compiler error when                                                                                                                         |
|-----------------------|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| @Override             | Methods                | Method signature does not match the signature of an inherited method                                                                        |
| @Functional Interface | Interfaces             | Interface does not contain a single abstract method                                                                                         |
| @Deprecated           | Most Java declarations | —                                                                                                                                           |
| @SuppressWarnings     | Most Java declarations | —                                                                                                                                           |
| @SafeVarargs          | Methods, constructors  | Method or constructor does not contain a varargs parameter or is applied to a method not marked ***private***, ***static***, or ***final*** |



