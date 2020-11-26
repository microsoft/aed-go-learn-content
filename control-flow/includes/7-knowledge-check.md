# Knowledge check

1. Can you use variables declared within an `if` statement outside of the `if` statement?
- Yes, variables are global
- No, the variable scope works only within the `if` block or nested `if` statements (Correct)
- Yes, as long as you use it within the function
- No, you have to declare a variable outside of an `if` statement

2. Do you need to include a `break` keyword at the end of every `case` statement in a `switch` block?

- No, Go doesn't require you to include the `break` keyword (Correct)
- Yes, otherwise the following `case` statements will be evaluated
- No, doesn't have support for the `break` keyword

3. Can you call multiple times a `defer` function within a function?

- No, you can call only once the `defer` function
- Yes, every call is queued, and they run in a last-in-first-out way. (Correct)
- Yes, every call is queued, and they run in a first-in-last-out way.
- Yes, but it will run only one time

4. What does the `panic()` function causes?

- Crash a program and prints out the error message and its stack trace (Correct)
- Throws an error that you need to catch; otherwise, the program crashes without any error
- Prints out a panic message to the console

5. Can the `recover()` function can be called anywhere in your code?

- Yes, but it only makes sense to call it from a deferred function to catch a panic execution (Correct)
- No, it only works if a panic statement was executed before
- Yes, but it will return `nil` unless your program panics