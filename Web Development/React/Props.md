**Props** allow us to use reusable data such as variables, arrays, and objects (json).
props can be used by simply adding (props) into the params of your react function. The name props isn't required, but it is common practice.
Inside of our react function we can pass {props.variableName} to use the data into our jsx and have it running in react.
Example:
```
function example(props){
	return (
		<h1>{props.title}</h1>
		<p>{props.paragraph}</p>
	)
}
```
In order for props values to be passes into the function we need to declare it and set the value in a similar way to json.
Example:
```
function App(){
	<example 
		title="Just in"
		paragraph= "This is some good news."
	/>
}
```
Furthermore if you want to pass in other data types besides strings or even function calls, can simply use { } and pass in the javascript code that we need. 

#Web-Dev #React #Frontend 