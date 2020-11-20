# Declare and Use Variables
Let's start this module by learning how to declare and use variables in Go. There are different ways to declare a variable, and we'll discover each of them, and you'll choose the one that best suits your needs or style. As we explain the core concepts for variables, we'll note some things specific to Go and that you don't typically find in other programming languages.

## Declaring Variables
To declare a variable, you need to use the `var` keyword, like this:

```
var firstName string
```

The above statement declares a variable named `firstName` of type `string`–we'll talk about data types in the upcoming section. This is the most basic way of declaring a variable. If you want to declare another variable, you simply add a similar statement to the previous one. However, you could declare more than one variable in a single line if they're the same type, like this:

```
var firstName, lastName string
```

By adding a comma (`,`) after a variable name, you're saying that you're about to declare another variable. In this case, the above statement declares two variables named `firstName` and `lastName` of type `string`. If you want to add a third variable of type `int`, the code will look like this:

```
var firstName, lastName string
var age int
```

Another way of writing the above statement is by using parenthesis after the `var` keyword, as if you had a dedicated block to declare variables, like this:

```
var (
    firstName, lastName string
    age int
)
```

## Initializing Variables
You've only declared variables at this point, but there are going to be times when you need them to have an initial value. In Go, this can be done in different ways. For instance, following the same example from above, you could initialize each variable like this:

```
var (
    firstName string = "John"
    lastName  string = "Doe"
    age       int    = 32
)
```

If you decide to initialize a variable, you don't need to specify its type as Go will infer its type when you initialize a variable with a value. For instance, you could declare and initialize variables like this:

```
var (
    firstName = "John"
    lastName  = "Doe"
    age       = 32
)
```

Go will infer that the `firstName` and `lastName` variables are `string` type, and the variable `age` is an `int` type. 

## Different Ways to Initialize Variables
In Go, you can declare and initialize variables in a single line. You separate by a comma each variable name and do the same for every value (in the same order), like this:

```
var (
    firstName, lastName, age = "John", "Doe", 32
)
```

There's another way you can declare and initialize a variable, which will be the most common way in Go. The same example we've been using could look like this:

```
func main() {
    firstName, lastName := "John", "Doe"
    age := 32
    println(firstName, lastName, age)
}
```

Notice that the difference now is that right after you define the variable name, you need to write a colon equal sign (`:=`) and its corresponding value. One important aspect here is that when you use the colon equal sign, **the variable you're declaring has to be a new one**. If you use a colon equal sign, and the variable has been declared already, the program won't compile. Go ahead and give it a try.

Lastly, **you can only use the colon equal sign inside a function**. When you declare variables outside a function, you must do it using the `var` keyword.

## Declaring Constants
There will be times when you need to have static values in your code; these are known as constants. Go has support for using constants, and the keyword to declare one is `const`. 

For instance, you can declare a constant like this:

```
const HTTPSatusOK = 200
```

Like variables, the type of a constant is inferred from the value assigned to it. Also, in Go, constants names are typically written in MixedCased or all caps.

If you need to declare multiple constants in the same block, you could do it in blocks, like this:

```
const (
    StatusOK              = 0
    StatusConnectionReset = 1
    StatusOtherError      = 2
)
```

**> [!NOTE]**
> Go has an interesting topic around constants called `iota`, which we're not covering in this module. But you can learn more about this concept by looking at the [Go's wiki on GitHub](https://github.com/golang/go/wiki/Iota). Just keep in mind that `iota` is a keyword Go uses to simplify constant definitions where the values are sequential.

Although there are similarities in constants with variables, there are some key differences. For instance, you can declare constants and not use them. Go won't complain about it. And, you can't use the colon equal sign to declare constants. Go will complain about it.

## Go Doesn't Like You to Declare Variables And Not Use Them
Something fundamental you need to keep in mind in Go is that unlike other programming languages when you declare a variable, don't use it. In Go, this is an error, not a warning.

For instance, let's go back to one of our previous examples, and remove the `println` call, like this:

```
func main() {
    firstName, lastName := "John", "Doe"
    age := 32
}
```

VS Code immediately tells you that there's an error in the lines where you're declaring the variables by underlining the lines in red. But if for some reason you ignore that error and decide to run the program, you'll get the following error:

```
# command-line-arguments
./main.go:4:2: firstName declared but not used
./main.go:4:13: lastName declared but not used
./main.go:5:2: age declared but not used
```

Clearly, Go didn't like that you declared variables that you didn't use. So keep in mind that for every variable you declare in Go, you must use it somewhere.