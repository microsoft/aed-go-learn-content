# Knowledge Check

1. What's the correct syntax to create a goroutine?
- `func (){}()` (Incorrect: you need to use the `go` keyword before the method you want to execute as a goroutine)
- `go launch()` (Correct: you need to use the `go` keyword before the method you want to execute as a goroutine)
- `goroutine launch()` (Incorrect: you need to use the `go` keyword before the method you want to execute as a goroutine)
- `thread launch()` (Incorrect: you need to use the `go` keyword before the method you want to execute as a goroutine)

2. What's the purpose of using channels in Go?
- To communicate properly within goroutines and avoid sharing memory for communication purposes (Correct: This is why Go says that we don't have to communicate by sharing memory; instead, we should share memory by communicating)
- It's just another way of creating goroutines (Incorrect: You create a goroutine by using the `go` keyword)
- To send data when doing HTTP calls to another API (Incorrect: Channels are used for communication purposes among goroutines)

3. What's a particular feature from unbuffered channels?
- Channels that are dynamic, they can grow as you need automatically (Incorrect: the main feature from unbuffered channels is that they communicate synchronously, for every data you send, you need to have a way to receive the message; otherwise, the program will get blocked)
- Sending and receiving data in channels are blocking operations (Correct: unbuffered channels communicate synchronously, for every data you send, you need to have a way to receive the message; otherwise, the program will get blocked)
- Channels that you can pass by reference only (Incorrect: the main feature from unbuffered channels is that they communicate synchronously, for every data you send, you need to have a way to receive the message; otherwise, the program will get blocked)

4. How do you send data to a channel?
- `ch = "Hi"` (Incorrect: you need to place the `<-` operator after the channel variable to assign a value)
- `ch <- "Hi"` (Correct: you need to place the `<-` operator after the channel variable to assign a value)
- `send(ch, "Hi")` (Incorrect: you need to place the `<-` operator after the channel variable to assign a value)

5. How do you receive data from a channel?
- `res := <- ch` (Correct: you need to place the `<-` operator before the channel variable to read its value)
- `res := get(ch)` (Incorrect: you need to place the `<-` operator before the channel variable to read its value)
- `res := ch<-` (Incorrect: you need to place the `<-` operator before the channel variable to read its value)

6. When would you use buffered channels?
- When you need to communicate in a synchronous way between goroutines (Incorrect: When you need to control how many goroutines should be running and you want to run as many processes at the same time as possible)
- When you need to guarantee that every time you send data, the program gets blocked until someone is reading from the channel (Incorrect: When you need to control how many goroutines should be running and you want to run as many processes at the same time as possible)
- Buffered channels decouple the send and receive operations, and they don't block a program. When you use unbuffered channels, you can control how many goroutines can run concurrently. (Correct: When you need to control how many goroutines should be running and you want to run as many processes at the same time as possible)