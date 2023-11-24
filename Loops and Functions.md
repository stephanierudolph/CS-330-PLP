# Types of Loops with Examples
## For-In Loops
For each item in variable, do statement.
```
var fruit = [“apple”, “banana”, “kiwi”, “grape”]
for f in fruit{
print(fruit)
}
```
## While Loops
As long as condition is met, do statement.
```
var vegetable = 0
while vegetable < 10 {
vegetable += 1
}
```
## Repeat-While
Repeat statement as long as condition is met.
```
var grain = 0
repeat{
grain += 1
} while grain < 5
```
## Combining For-In and Where
For each item in variable, given that the item meets a condition, do statement.
```
var fruit = [“apple”, “banana”, “kiwi”, “grape”]
for f in fruit where f != “kiwi”{
	print(fruit)
}
```
# Functions
To declare a function, use the following syntax
```
func myFunctionName(variable1: Int, variable2: Int) -> Int{
	//Statement 
return (“Insert returned variable here”)
}
```
Swift accepts multiple parameters and they can be of different data types.
```
func myFunc2( a: Int, b: Double) -> String{
    if Double(a) > b{
        return("nice!")
    } else{
        return("also nice")
    }
}
```
If you want to return multiple values from a function they need to be inside of an array or a tuple. 
```
func myFunc3() -> (width: Int, height: Int){
    return(width: 5, height: 20)
}
print(myFunc3())

```
The parameters take the name of the input variables with their data type. “-> Int” tells the function what type of data the function is returning. If the function is not returning anything, use `Void`. Parameters, arguments, and local variables are all stored in the stack during execution. 
Swift supports recursive functions. Here is an example of a recursive function.
```
func factorial(number: Int) -> Int{
    if number == 0{
        return 1
    }
    else{
        return number * factorial(number: number - 1)
    }
}
```
Swift is both pass by value and pass by reference. Swift defaults to pass by value, unless the `inout` keyword is used in the parameter and & is used before the variable name in the argument. If you try to pass and change variables through the function without using inout and & before the variable name then you will get an error.
### Scope
Swift is statically scoped, meaning if there is no variable with a certain name within the current block of code, it will look for that variable that contains the current block of code. 

# Sources
https://docs.swift.org/swift-book/documentation/the-swift-programming-language/controlflow/
https://www.programiz.com/swift-programming/for-in-loop
https://www.programiz.com/swift-programming/recursion
https://www.programiz.com/swift-programming/library/string/split
https://www.tutorialspoint.com/swift-pass-an-array-by-reference#:~:text=In%20Swift%2C%20you%20can%20pass,that%20copy%20to%20the%20function.
https://www.hackingwithswift.com/quick-start/beginners/how-to-return-multiple-values-from-functions
