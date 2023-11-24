# If-Else Statements
An if-else statement is a statement where, if a condition is true, the code will execute a block of code. Code blocks are wrapped in curly brackets `{ }`. You can always tell what else statements match to which if statements because all of the if statements require curly brackets. So, you know that the else will immediately follow the if statement it belongs to. If-else statements in Swift are written as follows:
## One-condition If-Else Statement
If condition is true, do statement. 
```
if a > b{
	<statement>
}
```
## Multi-conditional If-Else
If condition is true or/and another condition is true, do statement. 
```
If a > b || c > a{
	<statement>
}
```

## If-Else If-Else Statements
If a condition is met, do something, if a condition is not met but another condition is, do something else. If both of those conditions were not met, then do a separate thing. 
```
if a > b{
    print("a > b")//false
}else if b > c{
    print("b > c")//false
}else{//executes this line
    print("a < b and b < c")
}
```
### Guard Statements
A guard statement is similar to an if-else statement, however the if condition comes outside and after the else condition and guard statements require an else statement. 
```
var temp = 5
func testGuard(temp: Int) -> Void{

guard temp == 5 else{
	print(“temp is not 5”)
	return
}

print(“temp is 5”)
}
```

## Short Circuiting
When using && (and) or || (or) operators, they use short circuiting. This means that if by evaluating the first condition Swift can tell the answer regardless of what the second condition says, then Swift will not bother evaluating the second condition. This is useful because it improves performance. 

```
if a > b && b < a{
    print("yes")
}else{
    print("no")
}

```

## Switch Case
Switch case can be used to execute a statement when a variable matches a case. Switch cases are written as follows:
```
for r in 0...10{
    switch r{
    case 1: continue
    case 2: continue
    case 4: print("4")
    case 5: break
    case 6: print("5")
    default: continue
    }
}
}
```
For switch cases, you can use break, but it is not required. You would want to use it if you want a specific case to be ignored. If the switch case is within a loop, the keyword `continue` can be used to continue going through the loop. 

## Boolean Values
Note that when using boolean values in these statements, a boolean value is equal to `true` or `false`. You will receive errors if you attempt to compare values to `True` `False` `1` or `0`. 

# Sources
https://docs.swift.org/swift-book/documentation/the-swift-programming-language/controlflow/
