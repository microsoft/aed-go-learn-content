# Knowledge check

1. Can you use variables declared within an `if` statement outside of the `if` statement?
- Yes, variables are global (No, these variables' scope are only available within an `if` block.)
- No, the variable scope works only within the `if` block or nested `if` statements (Correct, you can't use those variables oustide of the `if` block, and you can even declare the "same" variables somewhere else.)
- Yes, as long as you use it within the function (No, you can only use those variables within the `if` block)
- No, you have to declare a variable outside of an `if` statement (Not necessarily, in Go you don't have to declare a variable before you can use it in an `if` block)

2. Do you need to include a `break` keyword at the end of every `case` statement in a `switch` block?

- No, Go doesn't require you to include the `break` keyword (Correct, by default, Go will stop the `switch` statement when finishing a `case` block.)
- Yes, otherwise the following `case` statements will be evaluated (No, by default, Go will stop the `switch` statement when finishing a `case` block.)
- No, doesn't have support for the `break` keyword (Go does has support for the `break` statement, but by default, Go will stop the `switch` statement when finishing a `case` block.)

3. Can you call multiple times a `defer` function within a function?

- No, you can call only once the `defer` function (You can call the `defer` function as many times as you want/need to.)
- Yes, every call is queued, and they run in a last-in-first-out way. (Correct, you can call the `defer` function as many times as you want/need to, and the execution order will be last-in-first-out.)
- Yes, every call is queued, and they run in a first-in-last-out way. (Yes, but the execution order will be last-in-first-out.)
- Yes, but it will run only one time (You can call the `defer` function as many times as you want/need to, and the execution order will be last-in-first-out.)

4. What does the `panic()` function causes?

- Crash a program and prints out the error message and its stack trace (Correct, you can use this function when you explicitly want to make the program to stop running and print out the error and its details.)
- Throws an error that you need to catch; otherwise, the program crashes without any error (No, then `panic` function makes the program to crash and prints out the error and its details, you don't necessarily have to `catch` the error to see it.)
- Prints out a panic message to the console (Yes, but it also makes the program crash.)

5. Can the `recover()` function be called anywhere in your code?

- Yes, but it only makes sense to call it from a deferred function to catch a panic execution (Correct, but if you don't call it within a deferred function you'll get a `nil` response back.)
- No, it only works if a panic statement was executed before (Not necessarily, but the idea is to be able to "recover" a program that is panicking. Otherwise, you'll get a `nil` response back.)
- Yes, but it will return `nil` unless your program panics (Yes, but you need to remember that if you don't include the call to this function in a deferred function, you get a `nil` response back.)