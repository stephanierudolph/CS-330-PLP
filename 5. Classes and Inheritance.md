# Classes
Swift is an object-oriented programming language. This means that you can write classes and create objects. In this example, we will be writing a Person class. Classes are usually written beginning with a capital letter. Objects are written in lowerCamelCase. 
```
class Person{
    var name = ""
    var age = 0
    var job = ""
    
    func about() -> String{
        var personDetails = (name + ", " + String(age) + ", " + job)
        return(personDetails)
    }
    func canDrink() -> Bool{
            if age >= 21{
                return(true)
            }else{
                return(false)
            }
        }
    }

}let myPerson = Person()
myPerson.age = 20
myPerson.name = "Sam"
myPerson.job = "Circus Clown"
print(myPerson.about()) // returns Sam, 20, Circus Clown
print(myPerson.canDrink()) //returns false
```
Here we have written a Person class with the three properties: name, age, and job. These properties have default values of an empty string or 0. We also have two functions. One that returns these three properties in the form of a string, the other return true if the person is old enough to drink. After the class declaration, we create a person object called `myPerson` and we change `myPerson`’s properties to be “Sam”, 20, and “Circus Clown” for each respective property. Then, when we call the `about` method on `myPerson`, we will get a string of these updated properties. 
## Standard Methods
In swift, there are no standard methods for objects. 
## Overloading Methods
If two methods are given the same name (overloaded), Swift is able to differentiate between them based on their number of parameters. As long as methods have different parameters from each other, then they can have the same name. 
# Inheritance
Now lets create a Student Class to inherit the properties of Person. 
```
class Student: Person{
    var gradYear = 2027
    var tuitionPaid = true
    
    override func about() -> String{
        var personDetails = (name + ", " + String(age) + ", " + job + ", " + String(gradYear) + ", " + String(tuitionPaid))
            return(personDetails)
    }
    func tuitionNotice() -> String{
        
        if tuitionPaid{
            return("Tuition has been paid")
        }else{
            return("Please pay tuition.")
        }
    }
}
```

Now we have a Student class that inherits the properties and methods of the Person class, and it has its own properties and methods. If we create a new student and give it some data, we will be able to show how both the Student and Person classes work together on this Student object. 
```
var myStudent = Student()
myStudent.age = 18
myStudent.job = "Student"
myStudent.name = "Bella"
myStudent.tuitionPaid = false
print(myStudent.canDrink()) //returns false
print(myStudent.about()) //returns Bella, 18, Student, 2027, false
print(myStudent.tuitionNotice()) //returns Please pay tuition.
```
When we use the .canDrink() method, you can see that it can be written just as a Person object would call the method. Notice how .about() returns the function from the Student class because it was overridden. 

Note that Swift does not support multiple inheritance. Meaning that a class can only inherit one other class. 

# Structures
Swift also supports Structures which are very similar to classes in the way that they can house properties and functions. The main differences are classes can use inheritance, you can check class types at runtime, and you can have multiple references to a class instance. This is how you would declare and call a structure.
```
struct MyStruct{
    var myInt = 10
}
var structOne = MyStruct()
structOne.myInt = 90
print(structOne.myInt) //returns 90
```
# Sources
https://www.oreilly.com/library/view/swift-3-objectoriented/9781787120396/ch05s04.html#:~:text=Swift%20doesn%27t%20allow%20us,for%20multiple%20inheritance%20of%20classes.
https://docs.swift.org/swift-book/documentation/the-swift-programming-language/inheritance
https://docs.swift.org/swift-book/documentation/the-swift-programming-language/classesandstructures
