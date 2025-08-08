# Your first kotlin program

Now we're going to make our very first program in Kotlin. The easiest way to do this is the way https://kotlinlang.org/docs/getting-started.html 
recommends to do it; by installing the IntelliJ IDEA IDE (Integrated Development Environment), and doing our Kotlin programming from there
. You *can* download the Kotlin compiler on its own, but this method avoids the hassle of going that way. Download the IDE using the instructions 
on the website, and let's create a new Kotlin project, not from the command line, if you're used to doing it that way, like I have, but from the IDE itself. 

Click 'New Project', choose Kotlin from the left, name the project 'hello-world', and set the location to wherever you want. Don't create a git repository, and
keep on "Add sample code", since this creates the Kotlin file for us.
Click 'Create'. Now you should have a Kotlin file with everything you need to get the program running. 
You can then go ahead and just remove all the sample code inside the file.

Then, inside the file, the first thing we want to do is create a main function. The program's execution starts in the main function in Kotlin, and if you don't 
have a main function inside your program, the compiler will throw an error your way. So let's do that now:

```kotlin
fun main() {
    
}
```

So, functions are defined with the 'fun'-keyword, as you can see. Very fun! You have to put parentheses after the function name in case of any parameters,
and the scope of the function, or the block that the function defines, is marked by curly braces. Let's print our 'Hello world!' now, and that is done with 
the built-in println()-function, which is equivalent to Python's print() for instance. Let's print hello world:

```kotlin
fun main() {
    println("Hello world!")
}
```

Run the program with the green triangle button at the top, and you should see 'Hello world!' printed out in the terminal. You have officially 
entered the world of Kotlin!

## On syntax

You may have noticed that I indented the println-command by four spaces, and that is how you should do it in Kotlin. You indent by four spaces. Also, 
when it comes to the curly braces, you type the opening brace on the same line as the statement that defines the block of code, at the end of the line, 
formatting it so that there is a space between the curly brace and the statement. Then, the closing curly brace comes on its own, separate line, 
indented so that it's horizontally aligned with the opening statement. You can see this in the above hello world-example.  

## More with printing

Let's also try printing something other than a string. Kotlin supports integer and float values, so let's try those out, strings aren't the only data type we have.

```kotlin
fun main() {
    println("Hello world!")
    println(12345)
	println(3.1415)
}

By the way: integers and floats are divided into different types, and we will get to that in the data types section of the tutorial.