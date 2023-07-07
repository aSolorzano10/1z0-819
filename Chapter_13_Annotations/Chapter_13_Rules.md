# Rules

### USING ANNOTATIONS IN DECLARATIONS
- Classes, interfaces, enums, and modules
- Variables ( static , instance, local)
- Methods and constructorsMethod, constructor, and lambda parameters
- Cast expressions
- Other annotations


### CREATING A VALUE() ELEMENT
- The annotation declaration must contain an element named ***value()***, which may be optional or required.
- The annotation declaration must not contain any other elements that are required.
- The annotation usage must not provide values for any other elements.


### rules for declaring a repeatable annotation
- The repeatable annotation must be declared with ***@Repeatable*** and contain a value that refers to the containing type annotation.
- The containing type annotation must include an element named ***value()***, which is a primitive array of the repeatable annotation type.

### JAVABEAN VALIDATION
- @NotNull : Object cannot be null
- @NotEmpty : Object cannot be null or have size of 0
- @Size(min=5,max=10) : Sets minimum and/or maximum sizes
- @Max(600) and @Min(‐5) : Sets the maximum or minimum numeric values
- @Email : Validates that the email is in a valid format


 
