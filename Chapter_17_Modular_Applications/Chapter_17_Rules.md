# Rules

### EXPLORING A BOTTOM ‐ UP MIGRATION STRATEGY
This approach works best when you have the power to convert any JAR files that aren't already modules

1. Pick the lowest‐level project that has not yet been migrated. 
2. Add a *module‐info.java* file to that project. Be sure to add any *exports* to expose any package used by higher‐level JAR files. Also, add a *requires* directive for any modules it depends on.
3. Move this newly migrated named module from the classpath to the module path.
4. Ensure any projects that have not yet been migrated stay as unnamed modules on the classpath.
5. Repeat with the next‐lowest‐level project until you are done.

### EXPLORING A TOP ‐ DOWN MIGRATION STRATEGY
A top‐down migration strategy is most useful when you don't have control of every JAR file used by your application

1. Place all projects on the module path.
2. Pick the highest‐level project that has not yet been migrated.
3. Add a *module‐info* file to that project to convert the automatic module into a named module. Again, remember to add any *exports* or *requires* directives. You can use the automatic module name of other modules when writing the *requires* directive since most of the projects on the module path do not have names yet.
4. Repeat with the next‐lowest‐level project until you are done.


