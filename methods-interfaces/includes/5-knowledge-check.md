# Knowledge Check

1. Is it possible to have methods with the same name and parameters?

- Yes, as long as the receiver is different (Correct: Go allows to have methods with the same name and parameters if the receiver is different)
- Yes, but you have to change the parameter names (Incorrect: Go allows to have methods with the same name and parameters if the receiver is different)
- No, function names in Go are unique (Incorrect: Go allows to have methods with the same name and parameters if the receiver is different)
- No, Go is not an OOP language (Incorrect: Go allows to have methods with the same name and parameters if the receiver is different)

2. Function parameters are passed by value. How can you create a method that allows you to modify any field from the receiver?

- You have to return a value and then modify the object with the new value (Incorrect: You need to use pointers so that you can change the values from a field in the receiver object)
- You can't. Methods are read-only (Incorrect: You need to use pointers so that you can change the values from a field in the receiver object)
- You have to use a pointer in the receiver when you want to modify any field from the receiver (Correct: You need to use pointers so that you can change the values from a field in the receiver object)
- You can't, Go can only pass parameters by value (Incorrect: You need to use pointers so that you can change the values from a field in the receiver object)

3. Is it possible to create methods for native types like `string`?

- No, you'll have a compile error if you try to do it (Incorrect: When you create a new type of the native type you want, you can create methods, but you have to use the new custom type)
- Yes, but you can only create methods for `string` or `int` (Incorrect: When you create a new type of the native type you want, you can create methods, but you have to use the new custom type)
- No, you can only create methods for structs (Incorrect: When you create a new type of the native type you want, you can create methods, but you have to use the new custom type)
- Yes, but you have to create a custom type wrapper (Correct: When you create a new type of the native type you want, you can create methods, but you have to use the new custom type)

4. Interfaces in Go are explicit or implicit?

- Interfaces in Go are implicit. There's no keyword like `implements` or symbols like `:` to explicitly implement an interface (Correct: Interfaces in Go are implemented implicitly, you simply need to create a method with the same signature as the one from the interface)
- Interfaces in Go are explicit. You have to use the `:` symbol (Incorrect: Interfaces in Go are implemented implicitly, you simply need to create a method with the same signature as the one from the interface)
- Interfaces in Go are implicit, but you can only implement interfaces from the current package, not from other packages (Incorrect: Interfaces in Go are implemented implicitly, you simply need to create a method with the same signature as the one from the interface)

5. Can you implement interfaces from standard packages?

- Yes, as long as you figure out which method you need to implement and has the same signature (Correct: Even if the interface is from the standard library, you can implement it)
- No, it will too hard to find out which methods you need to implement (Incorrect: Even if the interface is from the standard library, you can implement it, but you have to find out which methods to implement by reading the source code)
- Yes, but you might need to re-write a lot of code (Incorrect: Even if the interface is from the standard library, you can implement it, but you have to find out which methods to implement by reading the source code)