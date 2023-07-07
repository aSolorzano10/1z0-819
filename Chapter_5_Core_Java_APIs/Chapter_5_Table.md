# Tables

## TABLE 5.1 Binary search rules

| Scenario                                 | Result                                                                                                                         |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| Target element found in sorted array     | Index of match                                                                                                                 |
| Target element not found in sorted array | Negative value showing one smaller than the negative of the index, where a match needs to be inserted to preserve sorted order |
| Unsorted array                           | A surprise—this result isn’t predictable                                                                                       |

```
int[] numbers = {2,4,6,8};
4: System.out.println(Arrays.binarySearch(numbers, 2)); //0
5: System.out.println(Arrays.binarySearch(numbers, 4)); //1
6: System.out.println(Arrays.binarySearch(numbers, 1)); //-1
7: System.out.println(Arrays.binarySearch(numbers, 3)); //-2
8: System.out.println(Arrays.binarySearch(numbers, 9)); //-5
```

## TABLE 5.2 Arrays.compare() examples
| First array        | Second array        | Result          | Reason                                                        |
|--------------------|---------------------|-----------------|---------------------------------------------------------------|
| new int[] {1, 2}   | new int[] {1}       | Positive number | The first element is the same, but the first array is longer. |
| new int[] {1, 2}   | new int[] {1, 2}    | Zero            | Exact match                                                   |
| new String[] {"a"} | new String[] {"aa"} | Negative number | The first element is a substring of the second.               |
| new String[] {"a"} | new String[] {"A"}  | Positive number | Uppercase is smaller than lowercase.                          |
| new String[] {"a"} | new String[] {null} | Positive number | null is smaller than a letter.                                |


## TABLE 5.3 Equality vs. comparison vs. mismatch
| Method      | When arrays are the same | When arrays are different   |
|-------------|--------------------------|-----------------------------|
| equals()    | true                     | false                       |
| compare()   | 0                        | Positive or negative number |
| mismatch () | -1                       | Zero or positive index      |


## TABLE 5.4 Wrapper classes
| Primitive type | Wrapper class | Example of creating       |
|----------------|---------------|---------------------------|
| boolean        | Boolean       | Boolean.valueOf(true)     |
| byte           | Byte          | Byte.valueOf((byte) 1)    |
| short          | Short         | Short.valueOf((short) 1)  |
| int            | Integer       | Integer.valueOf(1)        |
| long           | Long          | Long.valueOf(1)           |
| float          | Float         | Float.valueOf((float)1.0) |
| double         | Double        | Double.valueOf(1.0)       |
| char           | Character     | Character.valueOf('c')    |

## TABLE 5.5 Converting from a String
| Wrapper class | Converting String to a primitive | Converting String to a wrapper class |
|---------------|----------------------------------|--------------------------------------|
| Boolean       | Boolean.parseBoolean("true")     | Boolean.valueOf("TRUE")              |
| Byte          | Byte.parseByte("1")              | Byte.valueOf("2")                    |
| Short         | Short.parseShort("1")            | Short.valueOf("2")                   |
| Integer       | Integer.parseInt("1")            | Integer.valueOf("2")                 |
| Long          | Long.parseLong("1")              | Long.valueOf("2")                    |
| Float         | Float.parseFloat("1")            | Float.valueOf("2.2")                 |
| Double        | Double.parseDouble("1")          | Double.valueOf("2.2)                 |
| Character     | None                             | None                                 |

## TABLE 5.6 Array and list conversions
|                                                                           | toArray() | Arrays.asList()   | List.of()          |
|---------------------------------------------------------------------------|-----------|-------------------|--------------------|
| Type converting from                                                      | List      | Array (orvarargs) | Array (or varargs) |
| Type created                                                              | Array     | List              | List               |
| Allowed to remove values from created object                              | No        | No                | No                 |
| Allowed to change values in the created object                            | Yes       | Yes               | No                 |
| Changing values in the created object affects the original or vice versa. | No        | Yes               | N/A                |

## TABLE 5.7 Common Map methods
| Method                               | Description                                                     |
|--------------------------------------|-----------------------------------------------------------------|
| V get(Object key)                    | Returns the value mapped by key or null if none is mapped       |
| V getOrDefault(Objectkey, V other)   | Returns the value mapped by key or other if none is mapped      |
| V put(K key, V value)                | Adds or replaces key/value pair. Returns previous value or null |
| V remove(Object key)                 | Removes and returns value mapped to key. Returns null if none   |
| boolean containsKey(Object key)      | Returns whether key is in map                                   |
| boolean containsValue(Objec t value) | Returns whether value is in map                                 |
| Set<K> keySet()                      | Returns set of all keys                                         |
| Collection<V> values()               | Returns Collection of all values                                |

