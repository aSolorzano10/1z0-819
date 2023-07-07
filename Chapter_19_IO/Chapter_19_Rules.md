# Rules

### Differences between Byte and Character Streams

- Byte streams read/write binary data (0s and 1s) and have class names that end in *InputStream* or *OutputStream*.
- Character streams read/write text data and have class names that end in *Reader* or *Writer*.


### Review of java.io Class Name Properties

- A class with the word *InputStream* or *OutputStream* in its name is used for reading or writing binary or byte data, respectively.
- A class with the word *Reader* or *Writer* in its name is used for reading or writing character or string data, respectively.
- Most, but not all, input classes have a corresponding output class.
- A low‐level stream connects directly with the source of the data.
- A high‐level stream is built on top of another stream using wrapping.
- A class with *Buffered* in its name reads or writes data in groups of bytes or characters and often improves performance in sequential file systems.
- With a few exceptions, you only wrap a stream with another stream if they share the same abstract parent.


### How to Make a Class Serializable
- The class must be marked Serializable .
- Every instance member of the class is serializable, marked transient , or has a null value at the time of serialization.

