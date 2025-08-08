# Data types and variables in Kotlin

## Variables

In Kotlin, you can declare variables, but unlike in Python, you have to explicitly say that it's a variable with either the `var` or `val` keyword before the 
variable name, like so:

```kotlin
fun main() {
    var ourVariable = "string"
    val secondVariable = 42
}
```

Now what is the difference between these two? Simply, `var` means that the variable's value can change, and `val` means that the variable's value cannot
change. So you could say that a variable declared with `var` is mutable, while one declared with `val` is immutable. You want to use `val` with variables 
with which you know that their value won't need to be changed in the program, and `var` for values that you want to change later on. 
For instance, let's look at the following code:

```kotlin
fun main() {
    var weather = "Cloudy"
	val pi = 3.1415
}
```

In this code, we have a variable `weather` that stores the current weather somewhere in the world at some time, and pi. We know that pi is a *constant*,
so something that won't change, but the weather on the other hand is something that changes all the time, so if we want to change the state of the weather-variable 
based on the current weather for example, we want to have `weather` declared with the `var` keyword.

I mentioned in 'What is Kotlin' that Kotlin has type inference, meaning you don't have to explicitly declare types on variables, but you can if you want to. 
It's up to personal preference. The way you do so goes as follows: 

```kotlin
var pi: Float = 3.1415
```

So you put a colon after the variable name, then you type the name of the type that the variable's value will be, capitalized. We will get to what data types 
there are in a minute, so that you know which ones you can use.

### Naming convention

I'll briefly touch on variable naming conventions here. In Kotlin, we want to name our variables using camelCase, so you don't capitalize 
the first word in the variable name, but capitalize each subsequent word. You also type the words 'together', so to say, meaning you 
don't use underscores _ or dashes - to separate words.

## Data types

### Integer types

There are a few types of integers in Kotlin, the smallest of which is `Byte`. Its size is 8 bits, so its minimum value is -128, and its maximum value is 127.
Next, the second smallest is `Short`, its size is 16 bits, min value is -32768 and max value is 32767. 
After that, we have `Int`, whose size is 32 bits, min value is -2^31, and max value is 2^31 - 1. Then, the largest type is `Long`, its size is 64 bits, 
min value is -2^63, and max value is 2^63 - 1. By the way, the reason for why the absolute values of the maximum values are one smaller than the minimum values, 
is because of how the numbers are represented in binary format, so how the computer understands them. Numbers are represented in two's complement, 
meaning the leftmost, or the most significant, bit tells us the sign of the number (pos or neg). For instance, if we have the number -8 represented in two's complement, 
it would be 1 0 0 0 in binary. Now, I haven't really explained it properly here, but with two's complement, you have room for one extra negative number in 
the bit representation, and I don't want to prolong is tangent for too long. Let's display the types of integers in a table:

| Type | Size in bits | Min value | Max value |
| :----:  | :----: | :----: | :----: |
| Byte | 8 | -128 | 127 |
| Short | 16 | -32768 | 32767 |
| Int | 32 | -2^31 | 2^31 -1|
| Long | 64 | -2^63 | 2^63 - 1 |

Also, if you declare an integer variable, but don't declare its type, the compiler will infer it as an `int`, so keep that in mind.

### Float types

Next, we have float types, which there are only two, `Float` and `Double`. `Float` is 32 bits in size, and it stores 6-7 decimal digits. `Double` is 
64 bits, and stores 15-16 decimal digits. `Float` is what the compiler infers, if you don't explicitly declare the type of a floating point number. Generally, 
these default types are good for most use cases, but if you need to use another type, then go for it. 

### Booleans, strings and chars

There are the two booleans: `true` and `false`, typed in lowercase, and there are strings, which you are likely familiar with at this point, given the assumption 
you know some programming basics. Strings are denoted with double quotes in Kotlin: `"this is a string"`. Characters are single string characters, denoted 
with single quotes, `'C'`.

## Exercises

As a disclaimer, the two types of exercises there are going to be are: fixing code, and writing code. In 'fixing code' exercises, you copy and paste the code 
in the exercise into the code editor, and fix the code to work without errors, or in the intended way. In 'writing code' exercises, you write the entire solution 
yourself. You can make one new project in the IDE for 'fixing code' exercises, and a folder for 'writing code' exercises, where you create a project 
for every new exercise, for example. But do it how you want. This first exercise is going to be a 'fixing code' exercise:

**1. Fix the following code, so it runs without errors:**
```kotlin 
fun main( {
    val stockValue: Int = 32.15
    stockValue = 32.55
    println(stocValue)
}
```

By the way, in Kotlin error messages, when there is a number, like ":2:29", the first number signifies the line of code the error appears on, and 
the second signifies the character index on the line where the error occurs. 

**2. Write a program, that stores your current name, age, and country you live in. Then, let's say your birthday is today, and you need to update your age, 
so update your age after initially declaring your age. Then, print out the variables.**

**3. Print as many digits of pi as you can remember, without looking anything up.**

## Example solutions

1: 

```kotlin
fun main() {
    var stockValue = 32.15
	stockValue = 32.55
	println(stockValue)
}
```

2: 

```kotlin
fun main() {
    val name = "Alvin"
	var age = 42
	var homeCountry = "Finland"
	
	age = 43
	
	println(name, age, homeCountry)
}
```

3: 

```kotlin
fun main() {
    val pi = 3.14159
	println(pi)
}
```