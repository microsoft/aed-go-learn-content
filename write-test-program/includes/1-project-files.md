# Project: An Online Bank
Let's talk about what we'll be creating. As we said before, we'll create two projects: one for the program's core logic and another one to expose certain logic through a Web API. Imagine that you're now part of a team building an online bank system where users can create accounts, transfer money, withdraw money, and get an account statement.

## Features and Requirements
The online bank we're about to build is a proof of concept, so most of the interaction with the core package we'll have is similar to what we've done so far: through a CLI program. We won't persist data into a database, and all calls will happen when the program starts. Then, we'll simply expose an endpoint to see the account statement from a customer.

In a nutshell, the online bank system should be able to do the following:

- Create an account.
- Give customers the possibility to withdraw money.
- Customers will be able to transfer money to another account.
- Provide an account statement with customer data and final balance.
- Expose through a Web API an endpoint to print an account statement.

We'll build this together, so don't worry too much about the details for now.

## Project Files
Before we start writing our program, let's create the initial set of files that we'll need. We'll create a Go package for all the bank core logic and a `main` program to initialize the system with a few customers and actions like deposits, transfers, etc. Additionally, this `main` program will start a Web API server to expose an endpoint for the account statement we mentioned before.

Let's create the following files structure in your `$GOPATH` directory:

```output
$GOPATH/
  src/
    bankcore/
      go.mod
      bank.go
    bankapi/
      go.mod
      main.go
```

Then, to make sure we can focus only on writing code in the proper files, let's start writing a `Hello World!` program that will confirm that we can call the `bankcore` package from the `bankapi` main program.

Use the following code snippet for the `src/bankcore/bank.go` file:

```go
package bank

func Hello() string {
    return "Hey! I'm working!"
}
```

We'll use Go modules, so for the `src/bankcore/go.mod` file, use the following content to give this package a proper name so that we can then reference it later:

```go
module github.com/msft/bank

go 1.14
```

Use the following code to call the `bankcore` package in the `src/bankapi/main.go` file:

```go
package main

import (
    "fmt"

    "github.com/msft/bank"
)

func main() {
    fmt.Println(bank.Hello())
}
```

And in the `src/bankapi/go.mod` file, we need to reference the `bankcore` package files locally, like this:

```go
module bankapi

go 1.14

require (
    github.com/msft/bank v0.0.1
)

replace github.com/msft/bank => ../bankcore
```

To make sure everything is working, head over to the terminal in the `$GOPATH/src/bankapi/` location and run the following command:

```sh
go run main.go
```

You should see the following output:

```output
Hey! I'm working!
```

This is a good approach to make sure you write the minimum amount of code before you get excited writting the solution to the main problem.

When you're done with the initial project files set up, move on to the next module. Otherwise, you might need to revisit the section where we discussed how packages work in Go and why you need to use Go modules. For now, you simply need the file structure we showed you before with the exact same content we included here.

See you in the next module to start writing the code we need to implement the initial set of features for our online bank system.