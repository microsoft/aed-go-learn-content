# Knowledge Check

1. What's the idiomatic way of handling errors in Go?

- Using a try/catch block (Incorrect, Go doesn't support the try/catch block)
- Using an `if` condition for a function that returns multiple values, in which case the last value would be the error (Correct, the simplest way in Go for handling an error is by using an `if` condition)
- Using an `if` condition and check if the response is `nil` (Incorrect, you should check if the error value is `nil` which is usually the last return value)
- Simply letting the program to terminate (Incorrect, you should always check for errors)

2. What's the function you could use to create an error variable?

- fmt.Errorf("Employee not found!") (Incorrect, the proper way to create an error variable is with errors.New("error message"))
- errors.New("Employee not found!") (Correct, you should create an error variable if you're planning to re-use the error message)
- error.New("Employee not found!") (Incorrect, the proper way to create an error variable is with errors.New("error message"))
- log.Error("Employee not found!") (Incorrect, the proper way to create an error variable is with errors.New("error message"))

3. Which are the functions from the log package?

- log.Print, log.Error, log.Info (Incorrect, log.Error and log.Info doesn't exist)
- log.Fatal, log.Print, log.Panic (Correct, these are functions that exist in the log package)
- log.Info, log.Warn, log.Fatal (Incorrect, log.Info and log.Warn doesn't exist)
- log.Printf, log.Warning, log.Error (Incorrect, log.Warning and log.Error doesn't exist)

4. What's the function you could use to configure logging to a file?

- log.SetOutput(file) (Correct, the function to configure the output file is log.SetOutput(file))
- log.SetOutputFile(file) (Incorrect, the function to configure the output file is log.SetOutput(file))
- log.SetFilePath(file) (Incorrect, the function to configure the output file is log.SetOutput(file))
- log.SetPath(file) (Incorrect, the function to configure the output file is log.SetOutput(file))

5. Why would you want to use a logging framework?

- To configure logging levels, multiple outputs, global contexts (Correct, the standard log package doesn't offer this type of functionality that you might need as your codebase grows)
- To make your programs run slower (Incorrect, although this might be true to some extent, this is not accurate)
- To simply configure structured logging (Incorrect, although you can structure logs, this is not the primary purpose)
- To write less code (Incorrect, although you might end up writing less code, this is not the primary purpose)