# Challenge
For the following challenges you'll get an existing program that you need to improve by making it run faster. As we said initially, try to write the programs by your own, even if you have to go back and check the examples you used to practice. Then, compare your solution with the one we have in the next section. Concurrency in Go is a complex problem that you'll understand better when you practice, so the following are just ideas of what you can do to practice. 

Good luck!

## Fibonacci
Use the following program to calculate Fibonacci numbers in a sequencial manner:

```go
package main

import (
	"fmt"
	"math/rand"
	"time"
)

func fib(number float64) float64 {
	x, y := 1.0, 1.0
	for i := 0; i < int(number); i++ {
		x, y = y, x+y
	}

	r := rand.Intn(3)
	time.Sleep(time.Duration(r) * time.Second)

	return x
}

func main() {
	start := time.Now()

	for i := 1; i < 15; i++ {
		n := fib(float64(i))
		fmt.Printf("Fib(%v): %v\n", i, n)
	}

	elapsed := time.Since(start)
	fmt.Printf("Done! It took %v seconds!\n", elapsed.Seconds())
}
```

You need to build two programs from this existing code:

- An improved version where you imlement concurrency, it should take a few seconds to finish, no more than 15 seconds as it does now. You should use buffered channels.
- Write a new version that calculates fibonacci numbers until the user enters `quit` in the terminal using the `fmt.Scanf()` function. If the user press `Enter` you should calculate a new fibonacci number. In other words, you'll no longer have a loop from 1 to 10. Use two unbuffered channels, one to calculate the fibonacchi number and another that's waiting for the "quit" message from the user. You'll need to use the `select` statement. Below is an example of the interaction with the program:

```output
1

1

2

3

5

8

13
quit
Done calculating Fibonacci!
Done! It took 12.043196415 seconds!
```
