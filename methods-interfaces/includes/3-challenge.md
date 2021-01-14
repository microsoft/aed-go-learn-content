# Challenge - Methods and Interfaces
To practice what you've learned about methods and interfaces, here's a challenge for a program that you need to write where you're not only going to practice what you saw in this module, but you'll also practice what you've seen in previous modules like creating your own package and using it.

## Store package
Write a program that uses a custom package that you write to manage an online store. Start by creating a custom type called `Account` with the first and last name of a person and it has to include the functionality to `ChangeName`

Once you're done with the `Account` type, you need to create another custom type called `Employee` with a variable to store the number of credits (`float64`) and that also embeds the `Account` object. Additionally, it has to include the functionality to `AddCredits`, `RemoveCredits`, and `CheckCredits`. You need to demonstrate that you can change the account's name via the Employee object.

Then, write a Stringer method to your Account object so that the Employee name can be printed out in a format that includes the first and last name.

Finally, write a program that consumes the package you created and test all the listed functionality in this challenge. For instance, the main program should change the name, print out the name, add credit, remove credit, and check the balance.
