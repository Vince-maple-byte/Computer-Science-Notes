For a review of .maps() [[Array.map()]]
When can use .maps() in order to pass in props values into our react components.
```
const arr = [
	{
		comment:"I need help",
		response:"Of course you do."
	},
	{
		comment:"I need cheese",
		response:"Somebody to go walmart."
	},
	{
		comment:"I need to learn to kickflip",
		response:"Wish I could help you there."
	}
]
const arrMap = arr.map(x => <Joke comment={x.comment} response={x.response} />)
```
In the code above the arrMap array can simply be returned into the react function and it would be rendered because react automatically renders out arrays for us. All we need to do is call {arrMap} inside of a <div> and it should work. 
The reason to do this is becasue it allows for us to change data in our components without much work, so that in the future all we need to change whenever we need new data to appear in our components is changing the original array. 
This also makes it easier to make multiple of the same components, but with different props values.

#Web-Dev #React 