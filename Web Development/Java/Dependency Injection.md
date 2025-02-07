**Def:** Simply the process of passing dependencies (Objects) into a class without having to create them inside of the class.

*Benefits:* 
* This eliminates the need for creating any unnecessary objects during the program's life cycle, which in turn can affect memory management and run time. 
* Dependency injection also allows for easier unit testing since with Mocks, we can set default values for a certain object that might be necessary for multiple different classes that we are testing without having to recreate the object each time. Ex. Making some default values for an object called database since we can't connect to the database that we are using, however, it's still needed in the classes that we need to unit test.
* Another benefit is that spring provides us with [[Inversion of Control]] which eliminates the need of worrying about the infrastructure of our code


#java #backend #Web-Dev #spring 