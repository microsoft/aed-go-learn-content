# Knowledge Check

1. What should be the name of a file that has the test cases in a package?

- `banktests.go` (Incorrect: Files whose names end with `_test.go` are not built by the `go build` command and run the tests with the `go tests` command)
- `bank_test.go` (Correct: Files whose names end with `_test.go` are not built by the `go build` command and run the tests with the `go tests` command)
- `test.go` (Incorrect: Files whose names end with `_test.go` are not built by the `go build` command and run the tests with the `go tests` command)

2. What's the correct signature for a test function?

- `func TestName(t *testing.T) { /* ... */ }` (Correct: The name of a test function should have the `Test` prefix and should include the `t *testing.T` as a parameter)
- `func NameTest(t *testing.T) { /* ... */ }` (Incorrect: The name of a test function should have the `Test` prefix and should include the `t *testing.T` as a parameter)
- `func TestName() { /* ... */ }` (Incorrect: The name of a test function should have the `Test` prefix and should include the `t *testing.T` as a parameter)

3. What's the command to run tests in a package in verbose mode?

- `go run tests` (Incorrect: When you have files that end with `_test.go`, you can run the `go tests -v` to run the tests and get a detailed output of the tests that ran)
- `go test main.go` (Incorrect: When you have files that end with `_test.go`, you can run the `go tests -v` to run the tests and get a detailed output of the tests that ran)
- `go tests -v` (Correct: When you have files that end with `_test.go`, you can run the `go tests -v` to run the tests and get a detailed output of the tests that ran)
