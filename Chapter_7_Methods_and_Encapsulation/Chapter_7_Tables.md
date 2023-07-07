# Tables

## TABLE 7.1 Parts of a method declaration

| Element                 | Value in nap() example      | Required?                         |
|-------------------------|-----------------------------|-----------------------------------|
| Access modifier         | public                      | No                                |
| Optional specifier      | final                       | No                                |
| Return type             | void                        | Yes                               |
| Method name             | nap                         | Yes                               |
| Parameter list          | (int minutes)               | Yes, but can be empty parentheses |
| Optional exception list | throws InterruptedException | No                                |
| Method body*            | { //take nap}               | Yes, but can be empty braces      |


## TABLE 7.2 Access modifiers
| A method in _________ can access a _________ member | private | Default (package-private) | protected | public |
|-----------------------------------------------------|---------|---------------------------|-----------|--------|
| the same class                                      | Yes     | Yes                       | Yes       | Yes    |
| another class in the same package                   | No      | Yes                       | Yes       | Yes    |
| in a subclass in a different package                | No      | No                        | Yes       | Yes    |
| an unrelated class in a different package           | No      | No                        | No        | Yes    |


## TABLE 7.4 The order that Java uses to choose the right overloaded method
| Rule                  | Example of what will be chosen for glide(1,2) |
|-----------------------|-----------------------------------------------|
| Exact match by type   | String glide(int i, int j)                    |
| Larger primitive type | String glide(long i, long j)                  |
| Autoboxed type        | String glide(Integer i, Integer j)            |
| Varargs               | String glide(int... nums)                     |