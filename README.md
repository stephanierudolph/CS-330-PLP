# CS-330-PLP
For this Programming Language Project, I will going through the basics of the programming language Swift.

## An Introduction to Swift
### History
Swift is an open-source programming language, first released in 2014. Its development was led by Chris Lattner at the company Apple. The language was designed to be used for Apple software development, however, it is also compatible with other operating systems. Swift was designed to replace Objective-C, which was an older programming language that Apple was using at the time. Swift was built to be easier, faster, and more resistant to errors. Swift is primarily used to develop applications within the apple ecosystem, however Swit can be used to write programs for other purposes such as command line tools, web services,  and cross-platform libraries for code.  For this project, I plan on using various articles and video tutorials as resources. Fortunately, Swift, as well as the Apple Developer website both have countless articles on the subject. 

### Resources
https://www.educative.io/courses/swift-programming-mobile-app/history-of-swift
https://www.swift.org/getting-started/
https://www.youtube.com/watch?v=EJQW864XpmA&t=1174s
https://developer.apple.com/tutorials/swiftui/creating-and-combining-views
https://docs.swift.org/swift-book/documentation/the-swift-programming-language/thebasics

### Getting Started
#### Installation 
In order to get swift running, I downloaded [Xcode](https://itunes.apple.com/app/xcode/id497799835) from the app store on MacOS. I recommend that Mac users use Xcode. Xcode is the easiest to set up and does not require any additional downloads. For Windows users, Xcode is not available, so I recommend using another programming environment such as VScode and downloading the appropriate developer package from the [Swift website](https://www.swift.org/install/windows/#installation-via-windows-package-manager). 

#### Running a Program
To run a program in Swift on Xcode, you can view a preview from the canvas. Alternatively, you can run it by using command R or clicking the play button on the top left of the page. This will open up a simulation of a device running the application. 

#### Comments
To make comments, you can use // for single line comments and /* */ for multi-line comments.

```
// single line comment
/* multi-line
comment */
```

## Data Types
### In Swift, there are 8 different data types. 
-Integer: an integer number
`var intExample: Int = 5`

-String: a series of characters
`var strExample: String = “hello”`

-Float: a 32-bit decimal number (up to 6 decimal places)
`var floatExample: Float = 1.2`

-Double: a 64-bit decimal number (up to 15 decimal places)
`var doubleExample: Double = 10.6338478`

-Boolean: having the value of true or false
`var boolExample: Bool = true`

-Array: a data type that can contain multiple data types
```
var arrayExample: Array<String> = [“itemOne”, “itemTwo”]`
var aList: [Int] = [0, 8, 900]
var _grades = [90, 88, 60, 74]
```

-Dictionary: a data type that has a key-value pairing
`var dictionaryExample: Dictionary<String, Int> = [“keyOne”: 0, “keyTwo”: 1]`

-Set: an array where the order of the data types does not matter
`var emotions: Set<String> = ["happy", "sad", "angry", "bored"]`

## Naming Conventions
### Here are some important things to know about data types:

1. Variable names can start with a letter, underscore, or dollar sign.
2. Variable names can NOT start with a number.
3. Swift uses the naming convention of UpperCamelCase for types and protocols and everything else, including variable names, use lowerCamelCase. 
4. Boolean values are declared with a lowercase `true` or `false`.
5. Data types can be declared either implicitly or explicitly. 
6. You cannot reassign a variable to a different data type than the one it was originally declared as.

```
var name: String = “Sarah” //declared explicitly, notice how String is capitalized 
var name = “Sarah” //declared implicitly 
```

### More Information on How Data Types Work
Swift is statically and strongly typed, meaning that the data type is checked at compile time and Swift does not implicitly convert data types. Swift is immutable, meaning that variables cannot change types after they are declared. 

`​num = num + "five" //does not work because Swift is strongly typed`

```
var test = 5
test = "hello" // does not work because Swift is immutable
```

Swift can be typed explicitly, but it can also be typed implicitly. There are certain situations where a variable needs to be explicitly declared, however, most of the time this is not the case.

`var anotherArray: Array<Any> = ["red", 20.5, true, 5] //variable type needs to be explicitly declared because Array has multiple different types of data`

`var _grades = [90, 88, 60, 74] //variable type does not need to be explicitly typed because Swift can imply the Array takes integers`

Mixed type operations are not allowed. To get around this, you must convert the data type. 
```
var num1 = 5
var num2 = 10.6
var num3 = num1 + num2 //does not work
var num3 = Double(num1) + num2
```
Identifier names and operator symbols are bound at compile time. 

### Reserved words
#### These words cannot be used as variable names in Swift. 
Any, as, associatedtype, break, case, catch, class, continue, default, defer, deinit, do, else, enum, extension, false, fileprivate, for, func, guard, import, if, in, init, internal, is, let, nil, open, operator, private, precendencegroup, protocol, public, repeat, rethrows, return
static, self, Self, struct, subscript, super, switch, throw, throws, true, try, typealias, var, where, while

### Available Operators
##### Arithmetic Operators
+, -, /, *, %
##### Assignment Operators
=, +=, -=, /=, *=, %=, 
##### Bitwise Operators
<< (left shift), >> (right shift), & (and), | (or), ^ (xor), ~ (compliment)
##### Comparison Operators
<, >, ==, !=, >=, <=, 
##### Logical Operators
&&, ||, !
##### Other Operators
condition ? a : b (if condition true then a, else b), a ?? b (default value is nil if no value passed by user), ++ (increment by 1), – (decrement by 1)
##### Range Operators
a…b (closed range), a..<b (from a to b but does not include b), [a…] (runs for as long as is possible)

### Sources
https://medium.com/@bkryslky/types-in-swift-212676e01e9d
https://www.programiz.com/swift-programming/data-types
https://www.swift.org/documentation/api-design-guidelines/
https://swiftbydeya.com/swift-keywords/
https://www.geeksforgeeks.org/swift-operators/
