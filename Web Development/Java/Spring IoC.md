**Def:** Spring IoC ([[Inversion Of Control]]) allows for another way of creating objects in java, and is the preferred method when dealing with [[Spring]] projects.
*Typical way it is done:* Doctor doc = new Doctor();
With Spring IoC, we would state the java classes that we need objects to be made during the runtime of our java application.
When the program is initially created, all of the classes that are stated in the XML configuration file or has an Annotation such as *@Bean* or *@Component*, and then saved in a container.
While the program is running anytime a class needs a specific object (called from [[Dependency Injection]]) we can simply call on the container and ask for the specific object that we need (The objects are called beans in spring).
### Benefits
* The benefit of this is that the code is going to be easier to read and manage objects since all of the objects are going to be created in one class as opposed to all over the project. Which is perfect when dealing with potential future changes in code. 
* This allows for use to implement [[Dependency Injection]] more easily in our application.
* This eliminates the need of having to worry about infrastructure optimization and best practices in our code when creating and managing object since Spring provide that for us.