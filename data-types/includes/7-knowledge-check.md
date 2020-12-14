# Knowledge Check

1. Arrays are a fixed-length data type, but how can you define their size based on the data you used to initialize them?
* You can't. You have to determine the number of elements when declaring it (Incorrect, you can use ellipsis `...` to determine its size based on the data you use to initialize it)
* You can use an ellipsis (`...`), like this `q := [...]int{1, 2, 3}` (Correct, when you use an ellipsis, the data you use to initialize an array defines its size)
* You can't. You have to create a slice (Incorrect, slices are dynamic, but this question was specific to arrays, and you can use ellipsis `...` to define its size based on the data you use to initialize it)

2. A slice works with an underlying array, and arrays are fixed-sized length. What happens when you add an element to the slice and the underlying array is full?
* You get a panic error Go (Incorrect, Go will create a new array and double its size to hold more elements in case it's needed)
* You don't get an error, but the new element is not added to the slice (Incorrect, Go will create a new array and double its size to hold more elements in case it's needed)
* Go doubles the size of the underlying array (Correct, Go will create a new array and double its size to hold more elements in case it's needed)

3. What happens when you create another slice using the slice operator `s[i:j]` and you make a change to an element in the new slice?
* The original slice changes too as a slice is simply a pointer to an underlying array (Correct, a slice is merely pointing to an underlying array, so you need to create a copy of the slice if you don't want to affect others)
* Only the slice you created gets affected as when you make a sub slice points to a new memory address (Incorrect, a slice is merely pointing to an underlying array, so you need to create a copy of the slice if you don't want to affect others)
* You can't make a sub slice. You'd have to create a new one (Incorrect, you can create slice a slice using the slice operator `s[i:j]`)

4. How can you remove elements from a slice?
* You have to use the `delete()` built-in function (Incorrect, this function only works for maps)
* You have to use the slice operator `s[i:j]`, and create a new slice without the element you'd like to remove (Correct, you could create a new slice using the slice operator to ignore the element you want to remove or replace the last element with the one you want to remove and make a new slice without the last element)
* You can't. You'd have to make a new slice by iterating all its elements and ignoring the one you'd like to remove (Incorrect, you can use the slice operator to create a new slice using the slice operator to ignore the element you want to remove or replace the last element with the one you want to remove and make a new slice without the last element)

5. When you're iterating the elements from a map, can you access the key and its value simultaneously?
* Yes, you could use the `for key, value := range map` syntax (Correct, when you loop the elements from a map, you can access the key and its value)
* No, you can only access its values (Incorrect, when you loop the elements from a map, you can access the key and its value)
* Yes, but only when the key and the value are from the same type (Incorrect, the key and the value can have a different type, and when you loop the elements from a map, you can access the key and its value)

6. Can you embed one struct into another struct?
* No, Go doesn't have support for inheritance (Incorrect, Go doesn't support inheritance, but you can embed one struct into another)
* Yes, and you can even access the parent properties as if it was part of the child struct (Correct, when you create a field with the same name as the name of the parent struct, you're embedding a struct into another struct)
* No, you have to use two structs and repeat code when needed (Incorrect, when you create a field with the same name as the name of the parent struct, you're embedding a struct into another struct)