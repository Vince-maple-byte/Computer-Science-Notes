**Def:** Dependency Injection allows for another way of creating objects in java, and is the preferred method when dealing with [[Spring]] projects.
Typical way it is done: Doctor doc = new Doctor();
With Dependency injection we would create the objects in a java class, and when the java project is run, the spring class would first go to the class where we created the objects that we are going to use in our project and holds them in a container.
While the program is running anytime a class needs a specific container we can simply call on the container and ask for the specific object that we need (The objects are called beans in spring).
### Benefits
The benefit of this is that the code is going to be easier to read and manage objects since all of the objects are going to be created in one class as opposed to all over the project. Which is perfect when dealing with potential future changes in code. 
Dependency injection also allows for easier unit testing since we can set default values for certain classes that might be necessary for the class that we are testing. Ex. Making some default values for an object called database since we can't connect to the database that we are using, however, it's still needed in the classes that we need to unit test.
Another benefit is that spring provides us with [[Inversion of Control]]
#java #backend #Web-Dev #spring 