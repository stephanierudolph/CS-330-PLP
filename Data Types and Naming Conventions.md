### In Swift, there are 7 different data types. 
-Integer: an integer number
`var intExample: Integer = 5`

-String: a series of characters
`var strExample: String = “hello”`

-Float: a 32-bit decimal number (up to 6 decimal places)
`var floatExample: Float = 1.2` 

-Double: a 64-bit decimal number (up to 15 decimal places)
`var doubleExample: Double = 10.6338478`

-Boolean: having the value of true or false
`var boolExample: Boolean = true`

-Array: a data type that can contain multiple data types
`var arrayExample: Array<String> = [“itemOne”, “itemTwo”]`

-Dictionary: a data type that has a key-value pairing
`var dictionaryExample: Dictionary<String, Int> = [“keyOne”: 0, “keyTwo”: 1]

### Here are some important things to know about data types:

Variable names can start with a letter, underscore, or dollar sign.
Variable names can NOT start with a number.
Types and protocols use UpperCamelCase, whereas everything else, including variable names, use lowerCamelCase. 
Boolean values are declared with a lowercase true or false.
Data types can be declared either implicitly or explicitly. 
You cannot reassign a variable to a different data type than the one it was originally declared as.

```
var name: String = “Sarah” //declared explicitly, notice how String is capitalized 
var name = “Sarah” //declared implicitly 
```
