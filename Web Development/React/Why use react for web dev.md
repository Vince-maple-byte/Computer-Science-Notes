React is a frontend javascript framework that allows us to create websites entirely in javascript.
React gives two main advantages: Composability and Declarativity

Composability in react allows for certain chunks of html code to be stored in separate components. These components can be swapped interchangeably when react renders the [[JSX]]. This allows for more readable lines of code and eliminates the need of having multiple html pages. 

React being declarative allows for us to tell react what we want done and it does that for us, while vanilla javascript forces us to explain how to do actions step by step. 

Example of components and declarative
```js
const page = (
	<div>
		<h1>Stranger Things</h1>
	</div>
);
const content = (
	<div>
		<p>is awesome</p>
	</div>
);
const root = react.createRoot(document.getElementByID('root'))
root.render(
	<div>
		page
		content
	</div>
)
```

#React #Frontend