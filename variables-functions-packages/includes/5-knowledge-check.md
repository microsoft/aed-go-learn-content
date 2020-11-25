# Knowledge check

1. How would you declare and initialize a variable?
* var firstName string
* firstName := "John" (Correct)
* string firstName = "John"
* firstName = "John"

2. What happens when you've declared variables but don't use them?
* You simply get a warning
* Nothing, there's no problem if you have unused objects
* You get an error; the program doesn't compile (Correct)
* You get a warning, but the next time it won't compile

3. How does data conversion type works in Go?
* You have to do conversion explicitly; implicit conversion doesn't work in Go (Correct)
* You can do implicit casting from `int` to `int32`
* You can only do it through external libraries
* You can't convert from `int` to `string`, or vice-versa

4. Why would you use pointers in Go?
* Go doesn't has support for pointers
* To change variable values from the function caller (Correct)
* To free-up memory

5. How many return values a function can have?
* Only one return value
* No more than two values
* Zero to many (Correct)

6. How do you differentiate between a package and a standalone application?
* You have to run `go create library` and `go create program`
* A standalone application uses the `package main`, and a package (library) use a different name (Correct)
* It doesn't matter; it depends on how you use the code once you've finish programming