# Control Flow Lab

## Instructions for lab submission

1. Fork the assignment repo
1. Clone your Fork to your machine
1. Complete the lab
1. Push your changes to your Fork
1. Submit a Pull Request back to the assignment repo
1. Paste a link to of your Fork on Canvas and submit

## Question 1

What will be printed when the code below is run?  Select all that apply.

```swift
let conditionOne = !(4 < 5) || !(3 > 8) // !(4 < 5) is false ||or !(3 > 8) is true
let conditionTwo = !(!true) // true

if conditionOne {
 print("A")
} else if conditionTwo {
 print("B")
}
if conditionTwo {
 print("C")
}
print("D")
```

- A // <---- will be displayed
- B
- C // <-- will be displayed
- D // <-- will be displayed

conditionOne and conditionTwo are both 'True' so following the logic would allow A to be printed because conditionOne is true and B will not be printed because the Print B line is skipped because its under 'Else If'

since conditionTwo is true then C is printed and D is printed because it requires no condition.

***
## Question 2

What will the code block below print?  Select all that apply:

```swift
let appInfo = (name: "myCoolApp", version: 0.4)
switch appInfo {
 case (_, 0.0..<1.0):
 print("\(appInfo.0) hasn't released yet")
 case ("myCoolApp", _):
 print("Thanks for looking at myCoolApp!")
 default:
 print("I'm not quite sure what you are looking at")
}
```

- appInfo.0 hasn't released yet
- myCoolApp hasn't released yet
- Thanks for looking at myCoolApp!
- I'm not quite sure what you are looking at
- It will give a compile-time error

The only line that would print is "myCoolApp hasn't released yet" because it's current version 0.4 which was declared within appInfo. The case that meets the condition to print "myCoolApp hasn't released yet" and stops there. The default line to print "I'm not quite sure what you are looking at"doesnt execute because the case to execute already satisfies the condition.

***
## Question 3

What will be printed to the console when the code below is run?  Select all that apply.

```swift
let x: Int = 4
switch x {
case 0..<4:
 print("A")
case 5..<10:
 print("B")
case is Double:
 print("C")
default:
 print("D")
}
``
There are 3 cases before the default case is executed. The constant is 4 which does not satisfy the first case which is any number betweeen 0 and <4. The second case does not execute because its looking for the range of 5 and <10, and x is 4. The third condition returns an error because its an incomplete statement. So thus the the default condition is executed.

- A
- B
- C
- D  <------- D will be printed

***
## Question 4

What are the errors in the code below for the switch statement? Select all that apply.

```swift
let candyType : String = "skittles"

switch candyType {
case "mAndM":
 print("Melts in your mouth, not in your hand")
case "skittles":
 print("Taste the rainbow")
case "snickers":
 print("Hungry? Grab a Snickers")
}
```

- No parentheses around the conditions
- No opening and closing brackets in each of the cases
- No default case in the switch statement <------
- No print statement right outside the switch statement

There is no default case which returns an exhaustive error. If a default case exists then the case ends at "skittles" because the string is "skittles".

***
## Question 5

Given the current weather conditions (rain, sunny, snow), use a switch statement to print an appropriate message to the user

```swift
let currentWeather = "rain"

// enter code below
```

switch currentWeather {
case "sunny":
print("incoming sun burns!")
case "snow":
print("don't drive unless you must!")
case "cloudy":
print("fair weather, it's all good!")
case "rain":
print("get your umbrellas out!!")
case "partly cloudy":
print("partly cloudy or partly sunny? Who really knows??")
default:
print("weather people are not reliable!!")
}

***
## Question 6

Given the first name and last name of a Fellow, declare `fullName` variable and use string interpolation to concatenate the Fellow's full name and print to the console e.g The Fellow's full name is John Appleseed

```swift
let firstName = "John"
let lastName = "Appleseed"

// enter code below
```
var fullName = "\(firstName) \(lastName)"
print("The Fellow's full name is \(fullName)")

We can interpolate variables within strings with the backslash with paranthesis
***
