# Tables

### TABLE 14.1 Functional interfaces used in this chapter
| Functional interfaces | Return type | Method name  | # parameters |
|-----------------------|-------------|--------------|--------------|
| Supplier<T>           | T           | get()        | 0            |
| Consumer<T>           | void        | accept(T)    | 1 (T)        |
| BiConsumer<T, U>      | void        | accept(T, U) | 2 (T, U)     |
| Predicate<T>          | boolean     | test(T)      | 1 (T)        |
| BiPredicate<T, U>     | boolean     | test(T, U)   | 2 (T, U)     |
| Function<T, R>        | R           | apply(T)     | 1 (T)        |
| BiFunction<T, U, R>   | R           | apply(T, U)  | 2 (T, U)     |
| UnaryOperator<T>      | T           | apply(T)     | 1 (T)        |


### TABLE 14.2 Method references
| Type                                    | Before colon           | After colon | Example           |
|-----------------------------------------|------------------------|-------------|-------------------|
| Static methods                          | Class name             | Method name | Collections::sort |
| Instance methods on a particular object | Instance variable name | Method name | str::startsWith   |
| Instance methods on a parameter         | Class name             | Method name | String::isEmpty   |
| Constructor                             | Class name             | new         | ArrayList::new    |



### TABLE 14.3 Wrapper classes
| Primitive type | Wrapper class | Example of initializing   |
|----------------|---------------|---------------------------|
| boolean        | Boolean       | Boolean.valueOf(true)     |
| byte           | Byte          | Byte.valueOf((byte) 1)    |
| short          | Short         | Short.valueOf((short) 1)  |
| int            | Integer       | Integer.valueOf(1)        |
| long           | Long          | Long.valueOf(1)           |
| float          | Float         | Float.valueOf((float)1.0) |
| double         | Double        | Double.valueOf(1.0)       |
| char           | Character     | Character.valueOf('c')    |


### TABLE 14.4 Factory methods to create a List
| Method                  | Description                                                      | Can add elements? | Can replace element? | Can delete elements? | 
|-------------------------|------------------------------------------------------------------|-------------------|----------------------|----------------------|
| Arrays.asList(varargs)  | Returns fixed size list backed by an array                       | No                | Yes                  | No                   |
| List.of(varargs)        | Returns immutable list                                           | No                | No                   | No                   |
| List.copyOf(collection) | Returns immutable list with copy of original collection's values | No                | No                   | No                   |


### TABLE 14.5 List methods
| Method                               | Description                                                                                                                      |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| boolean add(E element)               | Adds element to end (available on all Collection APIs)                                                                           |
| void add(int index, E element)       | Adds element at index and moves the rest toward the end                                                                          |
| E get(int index)                     | Returns element at index                                                                                                         |
| E remove(int index)                  | Removes element at index and moves the rest toward the front                                                                     |
| void replaceAll(UnaryOperator<E> op) | Replaces each element in the list with the result of the operator                                                                |
| E set(int index, E e)                | Replaces element at index and returns original. Throws IndexOutOfBoundsException if the index is larger than the maximum one set |


### TABLE 14.6 Queue methods
| Method             | Description                                                                      | Throws exception on failure |
|--------------------|----------------------------------------------------------------------------------|-----------------------------|
| boolean add(E e)   | Adds an element to the back of the queue and returns true or throws an exception | Yes                         |
| E element ()       | Returns next element or throws an exception if empty queue                       | Yes                         |
| boolean offer(E e) | Adds an element to the back of the queue and returns whether successful          | No                          |
| E remove()         | Removes and returns next element or throws an exception if empty queue           | Yes                         |
| E poll()           | Removes and returns next element or returns null if empty queue                  | No                          |
| E peek()           | Returns next element or returns null if empty queue                              | No                          |


### TABLE 14.7 Map methods
| Method                                            | Description                                                                                                  |
|---------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| void clear()                                      | Removes all keys and values from the map.                                                                    |
| boolean containsKey(Object key)                   | Returns whether key is in map.                                                                               |
| boolean containsValue(Object value)               | Returns whether value is in map.                                                                             |
| Set<Map.Entry<K,V>> entrySet()                    | Returns a Set of key/value pairs.                                                                            |
| void forEach(BiConsumer (K key, V value))         | Loop through each key/value pair.                                                                            |
| V get(Object key)                                 | Returns the value mapped by key or null if none is mapped.                                                   |
| V getOrDefault(Object key, V defaultValue)        | Returns the value mapped by the key or the default value if none is mapped.                                  |
| boolean isEmpty()                                 | Returns whether the map is empty.                                                                            |
| set<K> keySet()                                   | Returns set of all keys.                                                                                     |
| V merge(K key, V value, Function(<V, V, V> func)) | Sets value if key not set. Runs the function if the key is set to determine the new value. Removes if null . |
| V put(K key, V value)                             | Adds or replaces key/value pair. Returns previous value or null.                                             |
| V putIfAbsent(K key, V value)                     | Adds value if key not present and returns null. Otherwise, returns existing value.                           |
| V remove(Object key)                              | Removes and returns value mapped to key. Returns null if none.                                               |
| V replace(K key, V value)                         | Replaces the value for a given key if the key is set. Returns the original value or null if none.            |
| void replaceAll(BiFunction<K, V, V> func)         | Replaces each value with the results of the function.                                                        | 
| int size()                                        | Returns the number of entries (key/value pairs) in the map.                                                  |
| Collection<V> values()                            | Returns Collection of all values.                                                                            |



### TABLE 14.8 Behavior of the merge() method
| If the requested key ________ | And mapping function returns ________ | Then:                                                                          |
|-------------------------------|---------------------------------------|--------------------------------------------------------------------------------|
| Has a null value in map       | N/A (mapping function not called)     | Update key's value in map with value parameter.                                |
| Has a non‐null value in map   | null                                  | Remove key from map.                                                           |
| Has a non‐null value in map   | A non‐null value                      | Set key to mapping function result.                                            |
| Is not in map                 | N/A (mapping function not called)     | Add key with value parameter to map directly without calling mapping function. |


## TABLE 14.9 Java Collections Framework types
| Type  | Can contain duplicate elements? | Elements always ordered?        | Has key and values? | Must add/remove in specific order? |
|-------|---------------------------------|---------------------------------|---------------------|------------------------------------|
| List  | Yes                             | Yes(by index)                   | No                  | No                                 |
| Map   | Yes(for values)                 | No                              | Yes                 | No                                 |
| Queue | Yes                             | Yes(retrieved in defined order) | No                  | Yes                                |
| set   | No                              | No                              | No                  | No                                 |


## TABLE 14.10 Collection attributes
| Type        | Java Collections Framework interface | Sorted? | Calls hashCode? Calls compareTo |
|-------------|--------------------------------------|---------|---------------------------------|
| Array List  | List                                 | No      | No                              | No|
| HashMap     | Map                                  | No      | Yes                             | No |
| HashSet     | Set                                  | No      | Yes                             | No |
| Linked List | List, Queue                          | No      | No                              | No |
| TreeMap     | Map                                  | Yes     | No                              | Yes |
| TreeSet     | Set                                  | Yes     | No                              | Yes |


### TABLE 14.11 Comparison of Comparable and Comparator
| Difference                                        | Comparable  | Comparator |
|---------------------------------------------------|-------------|------------|
| Package name                                      | java.lang   | java.util  |
| Interface must be implemented by class comparing? | Yes         | No         |
| Method name in interface                          | compareTo() | compare()  |
| Number of parameters                              | 1           | 2          | 
| Common to declare using a lambda                  | No          | Yes        |


### TABLE 14.12 Helper static methods for building a Comparator
| Method                    | Description                                                                                          |
|---------------------------|------------------------------------------------------------------------------------------------------|
| comparing(function)       | Compare by the results of a function that returns any Object (or object autoboxed into an Object ).  | 
| comparingDouble(function) | Compare by the results of a function that returns a double .                                         |
| comparingInt(function)    | Compare by the results of a function that returns an int .                                           |
| comparingLong(function)   | Compare by the results of a function that returns a long .                                           | 
| naturalOrder()            | Sort using the order specified by the Comparable implementation on the object itself.                |
| reverseOrder()            | Sort using the reverse of the order specified by the Comparable implementation on the object itself. |


### TABLE 14.13 Helper default methods for building a Comparator
| Method                        | Description                                                                                                                                   |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| reversed()                    | Reverse the order of the chained Comparator .                                                                                                 |
| thenComparing(function)       | If the previous Comparator returns 0 , use this comparator that returns an Object or can be autoboxed into one.                               |
| thenComparingDouble(function) | If the previous Comparator returns 0 , use this comparator that returns a double . Otherwise, return the value from the previous Comparator . |
| thenComparingInt(function)    | If the previous Comparator returns 0 , use this comparator that returns an int . Otherwise, return the value from the previous Comparator .   |
| thenComparingLong(function)   | If the previous Comparator returns 0 , use this comparator that returns a long . Otherwise, return the value from the previous Comparator .   |


### TABLE 14.14 Types of bounds
| Type of bound                | Syntax          | Example                                                          |
|------------------------------|-----------------|------------------------------------------------------------------|
| Unbounded wildcard           | ?               | List<?> a = new ArrayList<String>();                             |
| Wildcard with an upper bound | ? extend s type | List<? extends Exception> a = new ArrayList<RuntimeException>(); |
| Wildcard with a lower bound  | ? super type    | List<? super Exception> a = new ArrayList<Object>();             |


### TABLE 14.15 Why we need a lower bound
| public static void addSound(______list) {list.add("quack");} | Method compiles                           | Can pass a List<String>                   | Can pass a List<Object> | 
|--------------------------------------------------------------|-------------------------------------------|-------------------------------------------|-------------------------|
| List<?>                                                      | No (unbounded generics are immutable)     | Yes                                       | Yes                     |
| List<? extends Object>                                       | No (upper‐bounded generics are immutable) | Yes                                       | Yes                     |
| List<Object>                                                 | Yes                                       | No (with generics, must pass exact match) | Yes                     |
| List<? super String>                                         | Yes                                       | Yes                                       | Yes                     |


