# Software 1 - Class Exercise 4
## Goals
- Learn how to handle exceptions
- Implement some OOP principles in your program.

## Instructions
### Error Handling
1. Run your program and add a product.  Now use option 2 to get a product that doesn't exist.  The program should have thrown an error and completely stopped.  You generally don't want these kinds of things happening so let's add some error handling to our program.
1. In the `ProductLogic` class in the `GetDogLeashByName` method, _wrap_ `return _dogLeash[name];` with a `try` block. Wrap is a pretty common term that means basically "put inside of the curly braces".  
1. After the try block, add a `catch` block.  The catch keyword takes one argument and that has to be an Exception.  This is a pretty standard way of writing a catch: `catch(Exception ex)`.  What you do inside of the catch block is really up to you and dependent on the situation.  In ours, let's just return `null` and account for that in the class that uses the method.
1. Back in our Program file, check the result of `GetDogLeashByName` to see if it's `null` using an `if`/`else` statment. If it _is_ `null`, write a message saying that the product couldn't be found.  If it _isn't_ `null` have the program do what it was doing before.

### OOP Principles
You will need to work together with someone on this part, so find one or two people close to you
OOP Principles:
- encapsulation
- abstraction
- inheritance
- polymorphism

1. We'll first look at encapsulation.  In our program we've encapsulated our product specific logic in our `ProductLogic` class. Talk with someone else about why you think this could be helpful as the program gets larger.  It is totally okay to look it up on the internet!
1. Next is abstraction.  Abstraction will be expanded on much more in next weeks exercise, but for now discuss with someone what it means and how think it might be used in the future in the Pet Store application.
1. Inheritence is something you've already used.  It is easier to understand using the "is-a" terminology.  So Cat Food _is a_ product.  A dog leash _is a_ product.  Let's take this one step further and add one more level of _is-a_.  Add a new class called `DryCatFood` and have it inherit from `CatFood`.  Let's move the Weight property over to this new class since that would belong more in the dry cat food than it would in something like canned cat food.
1. Polymorphism was used in the `AddProduct` function.  Discuss with someone how this is using the polymorphism principle.

