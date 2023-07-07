# Rules

### There are a few key differences between a ***module-info file*** and a regular Java class:
- The ***module-info*** file must be in the root directory of your module. Regular Java classes should be in packages.
- The ***module-info*** file must use the keyword ***module*** instead of ***class***, ***interface***, or ***enum***.
- The module name follows the naming rules for package names. It often includes periods ( . ) in its name. Regular class and package names are not allowed to have dashes ( - ). Module names follow the same rule.
