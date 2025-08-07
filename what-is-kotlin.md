# What is Kotlin?

It's a statically typed, high level language used mainly for Android development. It also has type inference. 
The language fully interoperates with Java,  meaning you can basically have Java code in a Kotlin file, and you can
migrate Java to Kotlin, for example, very effortlessly. Kotlin could be described as being "Java with less boilerplate code", 
boilerplate code meaning code that is repeated that has essentially the same function. Java basically has a lot of that, but
in a way where you must write it in order for the language to work. Kotlin has basically gotten rid of the boilerplate, so that you can focus more 
on writing functional code, and spend more time thinking about how to make the code efficient. The reason the language is mainly used for 
Android dev, is that the language is 'native' to the Android operating system, meaning Kotlin code can run on Android devices without any 
intermediary layers.

## Static typing

In a statically typed language, you have to generally declare the type of each variable. The types of variables are also generally not allowed 
to change in the program, so once you declare a variable as a specific type, the variable's type cannot change after this declaration. Kotlin is a 
statically typed language in the sense that you *can* declare types, but due to its type inference, you don't necessarily have to. Compare this to 
a language like Python, where the type of a variable actually can change in the program, so you could declare a variable with a value that has string 
type, and later change the variable's value to be of type integer, and so, the variable's type would change. This can't happen in Kotlin. Kotlin does 
have type inference though, meaning you don't need to declare the type of the variable explicitly as you're declaring the variable. 