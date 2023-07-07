# Tables

### TABLE 16.1 Unchecked exceptions
| ArithmeticException      | ArrayIndexOutOfBoundsException |
|--------------------------|--------------------------------|
| ArrayStoreException      | ClassCastException             |
| IllegalArgumentException | IllegalStateException          |
| MissingResourceException | NullPointerException           |
| NumberFormatException    | UnsupportedOperationException  |


### TABLE 16.2 Checked exceptions
| FileNotFoundException    | IOException    |
|--------------------------|----------------|
| NotSerializableException | ParseException |
| SQLException             |                |


### TABLE 16.3 Assertion applications
| Usage                   | Description                                                                                                                          |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| Internal invariants     | Assert that a value is within a certain constraint, such as *assert x < 0*.                                                          |
| Class invariants        | Assert the validity of an object's state. Class invariants are typically *private* methods within the class that return a *boolean*. |
| Control flow invariants | Assert that a line of code you assume is unreachable is never reached.                                                               |
| Pre‐conditions          | Assert that certain conditions are met before a method is invoked.                                                                   |
| Post‐conditions         | Assert that certain conditions are met after a method executes successfully                                                          |


### TABLE 16.4 Date and time types
| Class                   | Description                             | Example                 |
|-------------------------|-----------------------------------------|-------------------------|
| java.time.LocalDate     | Date with day, month, year              | Birth date              |
| java.time.LocalTime     | Time of day                             | Midnight                | 
| java.time.LocalDateTime | Day and time with no time zone          | 10 a.m. next Monday     |
| java.time.ZonedDateTime | Date and time with a specific time zone | 9 a.m. EST on 2/20/2021 | 


### TABLE 16.5 Common date/time symbols
| Symbol | Meaning          | Examples                    |
|--------|------------------|-----------------------------|
| y      | Year             | 20 , 2020                   |
| M      | Month            | 1 , 01 , Jan , January      |
| d      | Day              | 5 , 05                      |
| h      | Hour             | 9 , 09                      |
| m      | Minute           | 45                          |
| s      | Second           | 52                          |
| a      | a.m./p.m.        | AM , PM                     |
| z      | Time Zone Name   | Eastern Standard Time , EST |
| z      | Time Zone Offset | ‐0400                       |


### TABLE 16.6 Supported date/time symbols
| Symbol | LocalDate | LocalTime | LocalDateTime | ZonedDateTime |
|--------|-----------|-----------|---------------|---------------|
| y      | √         |           | √             | √             |
| M      | √         |           | √             | √             |
| d      | √         |           | √             | √             |
| h      |           | √         | √             | √             |
| m      |           | √         | √             | √             |
| s      |           | √         | √             | √             |
| a      |           | √         | √             | √             |
| z      |           |           |               | √             |
| z      |           |           |               | √             |


### TABLE 16.7 Factory methods to get a NumberFormat
| Description                             | Using default Locale and a specified Locale                                      |
|-----------------------------------------|----------------------------------------------------------------------------------|
| A general‐purpose formatter             | NumberFormat.getInstance() </br>NumberFormat.getInstance(locale)                 |
| Same as getInstance                     | NumberFormat.getNumberInstance() </br>NumberFormat.getNumberInstance(local e)    |
| For formatting monetary amounts         | NumberFormat.getCurrencyInstance() </br>NumberFormat.getCurrencyInstance(locale) |
| For formatting percentages              | NumberFormat.getPercentInstance() </br>NumberFormat.getPercentInstance(locale)   |
| Rounds decimal values before displaying | NumberFormat.getIntegerInstance() </br>NumberFormat.getIntegerInstance(locale)   |


### TABLE 16.8 DecimalFormat symbols
| Symbol | Meaning                                            | Examples |
|--------|----------------------------------------------------|----------|
| #      | Omit the position if no digit exists for it.       | $2.2     |
| 0      | Put a 0 in the position if no digit exists for it. | $002.20  | 


### TABLE 16.9 Factory methods to get a DateTimeFormatter
| Description                    | Using default *Locale*                                                                                                |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| For formatting dates           | DateTimeFormatter.ofLocalizedDate(dateStyle)                                                                          |
| For formatting times           | DateTimeFormatter.ofLocalizedTime(timeStyle)                                                                          |
| For formatting dates and times | DateTimeFormatter.ofLocalizedDateTime(dateStyle, timeStyle) </br>DateTimeFormatter.ofLocalizedDateTime(dateTimeStyle) |


### TABLE 16.10 Locale.Category values
| Value   | Description                                                |
|---------|------------------------------------------------------------|
| DISPLAY | Category used for displaying data about the locale         |
| FORMAT  | Category used for formatting dates, numbers, or currencies |


### TABLE 16.11 Picking a resource bundle for French/France with default locale English/US
| Step | Looks for file                                        | Reason                                        |
|------|-------------------------------------------------------|-----------------------------------------------|
| 1    | Zoo_fr_FR.properties                                  | The requested locale                          |
| 2    | Zoo_fr.properties                                     | The language we requested with no country     |
| 3    | Zoo_en_US.properties                                  | The default locale                            |
| 4    | Zoo_en.properties                                     | The default locale's language with no country |
| 5    | Zoo.properties                                        | No locale at all—the default bundle           |
| 5    | If still not found, throw *MissingResourceException*. | No locale or default bundle available         |


### TABLE 16.12 Selecting resource bundle properties
| Matching resource bundle | Properties files keys can come from                             |
|--------------------------|-----------------------------------------------------------------|
| Zoo_fr_FR                | Zoo_fr_FR.properties </br>Zoo_fr.properties </br>Zoo.properties |

