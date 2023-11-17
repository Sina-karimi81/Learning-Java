# Learning-Java
a summary of Learning Java book<br />
since chapters 1-4 were just history of the language and some common syntaxes like expression and statements they are ommitted. we'll be starting from chapter 5

## Objects in java
* the term object oriented design refers to the art of decomposing our application to some number of objects which represent real life entities. objects are self contained components that can work together
* the goal here os to break our problem into sub problomes that are easier to handle and maintain
### Classes
* classes are the building blocks of a java application. a class can contain methods, variables, initialization code and even other classes
* a class serves as a blueprint for making instances, which are runtime objects that implement the class structure
* in a class we can declare variables to store information and we can implement methods that describe what we can do with an instance of this class<br />
![Learning java](https://github.com/Sina-karimi81/Learning-Java/assets/83176938/4b52f5ea-54df-4f06-841c-67737eb7933e)
* our apple class has four variables and a method that returns a boolean value
* variables and method declarations can appear in any order but variable initialization cannot take references that variables that come after them. in our code snippet for example mass variable cannot use diameter varialbe to initialze itself since the program has not already recognized diameter variable
* once we've defined a class we can create objects of that class
![Learning java](https://github.com/Sina-karimi81/Learning-Java/assets/83176938/aba1d843-6b82-416a-8298-979882ae7e1c)
* when we create an object the declaration part which is "Apple a1" creates a variable that takes a reference to an object of type Apple and it is the "new Apple()" part that creates the object and then the reference to that object is assigned to a1
* once we have a reference to an object we can access it's variables and methods using the "." (dot) operator
![Learning java](https://github.com/Sina-karimi81/Learning-Java/assets/83176938/207858e5-b0b8-4506-9c42-cea13da49100)
* in the code snippet above we used a method called "main". this method is where a java application starts from. when we write the "*java -jar app.java*" in our console this method is called.if you take a closer look in takes an array of strings as input which are variables that we can pass to the main fucntion when writing the "*java -jar*" command
* another thing is that we used a method named *println* from the System package of java libraries. this method write a message to the console<br />
![Learning java](https://github.com/Sina-karimi81/Learning-Java/assets/83176938/1e9868a1-593e-4a79-9dd1-5cd60fe3147e)
* as you can see since we didn't initialize the mass, x and y variables a default values is assigned to them. for numeric values the default is 0, for boolean is false and for objects it is null
* as we said earlier we can declare methods inside class which tell us what we can do with an object. in other word methods allow us to "do stuff" inside class. for example we will take the print calls and use them as method inside in our Apple class
![Learning java](https://github.com/Sina-karimi81/Learning-Java/assets/83176938/c9f73008-9d7e-449d-8d85-c5d6353050c5)
* as you can see since we are inside the class we can access it's variables and methods directly with their names and there is no need to use a reference variable and dot operator
* there are several factors that affect whether we can access class members from another class or not
* we can use access modifiers to control access to class members:
    - private: makes the class members only accessible by class itself
    - protected: makes the class members accessible by the class itself, it subTypes (discussed later) and classes that are in the same package (discussed later)
    - public: makes class members accessible by any other object
* when we define our class members as private we still need a way to access them. that is where we use getters and setters
![Learning java](https://github.com/Sina-karimi81/Learning-Java/assets/83176938/35172942-d416-4ebf-b026-4a190d13d749)
### Static Members
* as we said before instance variables and methods are associated and accessed through an instance of the class like the a1 object in previous examples
* in contrast, members that are marked with *static* keyword, live in the class and are shared by all instances of the class. this way we get static variables and static methods (aka class variables and class methods)
* static members can be accessed through the class directly or through the instance. either way we get the same value and we can change it through both
* if a static variable is changed, this change is reflected to all other instances as well. this makes them useful for situation were a resource must be shared among instances at runtime
* other than this static members work any other variable or method
* by using the final keyword along side the static keyword we can create constant values in classes which values cannot be changed after initialization<br />
![Learning java](https://github.com/Sina-karimi81/Learning-Java/assets/83176938/c7fc41e6-9bcd-4af1-b446-acfab306d386)
### Methods
* methods in java are blocks of code that are bundled together to perform a specific action
* they can take in paramters as inputs, they can return values as primitive data types, object reference or void which mean no return value. they can have their own local variables
* the main advantage of methods is code reusability. we define it once and we can use it how many times we want to without the need to implement the same logic many times
* the local variables inside a method are temporary. meaning that they are created each time the method is called and then they are destroyed when the method has finished it's job. this means that local variables are bound to the scope (or the block) of the method
* a method's input parameters also serve as local variables of that method the difference being that they are initialized by the caller and then passed to the method
![Learning java](https://github.com/Sina-karimi81/Learning-Java/assets/83176938/41224226-d547-4a1c-9e49-8b73811460e0)
