# Props

Props are objects that are passed into a component

## Example
`
function Hello(props)
{
	return(
		<div>
			<h1>Welcome to {props.library}</h1>
			<p>{prop.message}<p>
	)
}
`

`
ReactDOM.render(
	<Hello
		library="React"
		message="Have Fun!"
	/>,
	document.getelementById("root")
)
`

## Destructing Props
Destructing the props allows for more readable code 
`
function Hello(library, message)
{
	return(
		<div>
			<h1>Welcome to {library}</h1>
			<p>{message}<p>
	)
}
`

## Mapping Props 
You can iterate over props or a particular prop data.
For example, to create a list

`
const lakeList = 
[
	"Echo Lake"
	"Maud Lake"
	"Cascade Lake"
];
`

`
function App({lakes})
{
	return 
	(
		<ul>
			{lakes.map(lake => (
				<li>{lake}</li>
			))}
		</ul>
	)
}
`

`ReactDOM.render(
	<App lakes={lakeList} />,
	document.getElementById("root")
)
	`
	
Would return a page with a list of Lakes as

- Echo Lake
- Maud Lake
- Cascade Lake

If the lakeList was a JSON you could render a dynamic list with dot notation.

## Key
When creating items through iteration this way it is important to add a key to the new elements e.g

`
<li key={item.toString()}>
`

Keys function in a similar way as HTML Ids 


## Conditional Rendering
Items can be conditionally rendered depending on the props it is passed using If statements in the function 