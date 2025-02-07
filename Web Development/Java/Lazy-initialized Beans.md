This tells the [[ApplicationContext]] to not create the singleton bean as part of the initialization process. Instead the bean would be created when the bean instance when the bean is first requested.

**How it is created?**
```
@Bean 
@Lazy 
ExpensiveToCreateBean lazy() { 
	return new ExpensiveToCreateBean(); 
} 

@Bean 
AnotherBean notLazy() { 
	return new AnotherBean(); 
}
```
****
*Important Note:* If the lazy bean is a dependency of another singleton bean that is not lazy the [[ApplicationContext]] would still create the lazy bean instance at start up to satisfy the context of the non-lazy bean.

#spring #java 