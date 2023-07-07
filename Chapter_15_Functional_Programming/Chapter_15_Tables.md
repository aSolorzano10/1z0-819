# Tables

### TABLE 15.1 Common functional interfaces
| Functional interface | Return type | Method name | # of parameters |
|----------------------|-------------|-------------|-----------------|
| Supplier<T>          | T           | get()       | 0               |
| Consumer<T>          | void        | accept(T)   | 1 (T)           |
| BiConsumer<T, U>     | void        | accept(T,U) | 2 (T,U)         |
| Predicate<T>         | boolean     | test(T)     | 1 (T)           |
| BiPredicate<T,U>     | boolean     | test(T,U)   | 2 (T, U)        |
| Function<T, R>       | R           | apply(T)    | 1 (T)           |
| BiFunction<T, U, R>  | R           | apply(T,U)  | 2 (T, D)        |
| UnaryOperator<T>     | T           | apply(T)    | 1 (T)           |
| BinaryOperator<T>    | T           | apply(T)    | 2(T, T)         |


### TABLE 15.2 Convenience methods
| Interface instance | Method return type | Method name | Method parameters |
|--------------------|--------------------|-------------|-------------------|
| Consumer           | Consumer           | andThen()   | Consumer          |
| Function           | Function           | andThen()   | Function          |
| Function           | Function           | compose()   | Function          | 
| Predicate          | Predicate          | and()       | Predicate         |
| Predicate          | Predicate          | negate()    | -                 |
| Predicate          | Predicate          | or()        | Predicate         |


### TABLE 15.3 Optional instance methods
| Method                  | When Optional is empty                       | When Optional contains a value |
|-------------------------|----------------------------------------------|--------------------------------|
| get()                   | Throws an exception                          | Returns value                  |
| ifPresent(Consumer c)   | Does nothing                                 | Calls Consumer with value      |
| isPresent()             | Returns false                                | Returns true                   |
| orElse(T other)         | Returns other parameter                      | Returns value                  |
| orElseGet(Supplier s)   | Returns result of calling                    | Returns value                  |
| orElseThrow()           | Throws NoSuchElementException                | Returns value                  |
| orElseThrow(Supplier s) | Throws exception created by calling Supplier | Returns value                  |



### TABLE 15.4 Intermediate vs. terminal operations
| Scenario                                | Intermediate operation | Terminal operation |
|-----------------------------------------|------------------------|--------------------|
| Required part of a useful pipeline?     | No                     | Yes                |
| Can exist multiple times in a pipeline? | Yes                    | No                 |
| Return type is a stream type?           | Yes                    | No                 |
| Executed upon method call?              | No                     | Yes                |
| Stream valid after call?                | Yes                    | No                 | 

 
### TABLE 15.5 Creating a source
| Method                                          | Finite or infinite | Notes                                                                                                                                                                    |
|-------------------------------------------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stream.empty()                                  | Finite             | Creates Stream with zero elements                                                                                                                                        |
| Stream.of(varargs)                              | Finite             | Creates Stream with elements listed                                                                                                                                      |
| coll.stream()                                   | Finite             | Creates Stream from a Collection                                                                                                                                         | 
| coll.parallelStream()                           | Finite             | Creates Stream from a Collection where the stream can run in parallel                                                                                                    | 
| Stream.generate(supplier)                       | Finite             | Creates Stream by calling the Supplier for each element upon request                                                                                                     |
| Stream.iterate(seed, unary Operator)            | Infinite           | Creates Stream by using the seed for the first element and then calling the UnaryOperator for each subsequent element upon request                                       |
| Stream.iterate(seed, predicate, unary Operator) | Finite or infinite | Creates Stream by using the seed for the first element and then calling the UnaryOperator for each subsequent element upon request. Stops if the Predicate returns false | 


### TABLE 15.6 Terminal stream operations
| Method                                      | What happens for infinite streams | Return value | Reduction |
|---------------------------------------------|-----------------------------------|--------------|-----------|
| count()                                     | Does not terminate                | long         | Yes       |
| min() </br>max()                            | Does not terminate                | Optional<T>  | Yes       |
| findAny() </br>findFirst()                  | Terminates                        | Optional<T>  | No        |
| allMatch() </br>anyMatch() </br>noneMatch() | Sometimes terminates              | boolean      | No        |
| forEach()                                   | Does not terminate                | void         | No        |
| reduce()                                    | Does not terminate                | Varies       | Yes       |
| collect()                                   | Does not terminate                | Varies       | Yes       | 


### TABLE 15.7 Common primitive stream methods
| Method                                                                                                                                    | Primitive Stream                            | Description                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|---------------------------------------------------------------------------------------------|
| OptionalDouble average()                                                                                                                  | IntStream </br>LongStream </br>DoubleStream | The arithmetic mean of the elements                                                         |
| Stream<T> boxed()                                                                                                                         | IntStream </br>LongStream </br>DoubleStream | A *Stream<T>* where T is the wrapper class associated with the primitive value              | 
| OptionalInt max()  </br>OptionalLong max() </br>OptionalInt max()                                                                         | IntStream </br>LongStream </br>DoubleStream | The maximum element of the stream                                                           |
| OptionalInt min() </br>OptionalLong min() </br>OptionalDouble min()                                                                       | IntStream </br>LongStream </br>DoubleStream | The minimum element of the stream                                                           |
| IntStream range(int a, int b) </br>LongStream range(long a, long b)                                                                       | IntStream </br>LongStream                   | Returns a primitive stream from a (inclusive) to b (exclusive)                              | 
| IntStream rangeClosed(int a, int b) </br>LongStream rangeClosed(long a, long b)                                                           | IntStream </br>LongStream                   | Returns a primitive stream from (inclusive) to b (inclusive)                                |
| int sum() </br>long sum() </br>double sum()                                                                                               | IntStream </br>LongStream </br>DoubleStream | Returns the sum of the elements in the stream                                               |
| IntSummaryStatistics  summaryStatistics() </br>LongSummaryStatistics summaryStatistics() </br>DoubleSummaryStatistics summaryStatistics() | IntStream </br>LongStream </br>DoubleStream | Returns an object containing numerous stream statistics such as the average, min, max, etc. |


### TABLE 15.8 Mapping methods between types of streams
| Source stream class | To create *stream* | To create *DoubleStream* | To create *IntStream* | To create *LongStream* |
|---------------------|--------------------|--------------------------|-----------------------|------------------------|
| Stream<T>           | map()              | mapToDouble()            | mapToInt()            | mapToLong()            |
| DoubleStream        | mapToObj()         | map()                    | mapToInt()            | mapToLong()            |
| IntStream           | mapToObj()         | mapToDouble()            | map()                 | mapToLong()            |
| LongStream          | mapToObj()         | mapToDouble()            | mapToInt()            | map()                  |


### TABLE 15.9 Function parameters when mapping between types of streams
| Source stream class | To create *Stream*  | To create *DoubleStream* | To create *IntStream* | To create *LongStream* |
|---------------------|---------------------|--------------------------|-----------------------|------------------------|
| Stream<T>           | Function <T,R>      | ToDoubleFunction<T>      | ToIntFunction<T>      | ToLongFunction<T>      |
| DoubleStream        | Double Function <R> | DoubleUnar y Operator    | DoubleToInt Function  | DoubleToLong Function  |
| IntStream           | IntFunction<R>      | IntToDouble Function     | IntUnary Operator     | IntToLong Function     |
| LongStream          | Long Function<R>    | LongToDouble Function    | LongToInt Function    | LongUnary Operator     | 


### TABLE 15.10 Optional types for primitives
|                                | OptionalDouble | OptionalInt    | OptionalLong   |
|--------------------------------|----------------|----------------|----------------|
| Getting as a primitive         | getAsDouble()  | getAsInt()     | getAsLong()    |
| orElseGet() parameter type     | DoubleSupplier | IntSupplier    | LongSupplier   |
| Return type of max() and min() | OptionalDouble | OptionalInt    | OptionalLong   |
| Return type of sum()           | double         | int            | long           |
| Return type of average()       | OptionalDouble | OptionalDouble | OptionalDouble |


### TABLE 15.11 Common functional interfaces for primitives

### TABLE 15.12 Primitive‐specific functional interfaces

### TABLE 15.13 Examples of grouping/partitioning collectors


