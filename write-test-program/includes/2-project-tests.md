# Writting Tests in Go
Before we jump into writing our program, let's talk about how testing in Go works. The reason for this is that we'd like to start coding using the Test Driven Development (TDD) approach. This means we'll write our tests first, then we'll write the code that satisfies that test.

# Create the test file

First, we need to create the Go file to put all of our tests for the `bankcore` package. To create a test file, the file's name has to finish with `_test.go`. You can put whatever you want before, but the pattern is to use the name of the file you're testing. Additionally, every test you want to write has to be a function that starts with `Test`, and then you usually write a descriptive name for the test you're writing like `TestDeposit`.

Head over to the `$GOPATH/src/bankcore/` location and create a file called `bank_test.go` with the following content:

```go
package bank

import "testing"

func TestAccount(t *testing.T) {

}
```

Open a terminal, and make sure at the `$GOPATH/src/bankcore/` location, then run the following command:

```sh
go test -v
```

And Go will look for all the `*_test.go` files to run the tests, so you should see the following output:

```output
=== RUN   TestAccount
--- PASS: TestAccount (0.00s)
PASS
ok      github.com/msft/bank    0.391s
```

Let's leave it here for now; we'll complete this test and create new tests as we write the logic for our online bank system.
