# Rules

### UNDERSTANDING THE PIPELINE FLOW
- Source: Where the stream comes from
- Intermediate operations: Transforms the stream into another one. There can be as few or as many intermediate operations as you'd like. Since streams use lazy evaluation, theintermediate operations do not run until the terminal operation runs.
- Terminal operation: Actually produces a result. Since streams can be used only once, the stream is no longer valid after a terminal operation completes.

### CREATING PRIMITIVE STREAMS
- ***IntStream***: char Used for the primitive types *int*, *short*, *byte*, and
- ***LongStream***: Used for the primitive type *long*
- ***DoubleStream***: Used for the primitive types *double* and *float*.

### Summary statistics include the following:
- Smallest number (minimum): getMin()
- Largest number (maximum): getMax()
- Average: getAverage()
- Sum: getSum()
- Number of values: getCount()

