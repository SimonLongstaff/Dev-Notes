# React Components

![[Pasted image 20210825092652.png]]

## Arguments
- [[Props]]

React elements are Functions

Functions can return JSX HTML to be rendered 

Component MUST be captalisied.

### Example
`function Hello() 
	{
		return <h1>Welcome To React</h1>;
	}
`

Could be used via

`
ReactDOM.render
(
	<Hello></Hello>,
	document.getElementByID("root")
)
`

or just

`
ReactDOM.render
(
	<Hello />,
	document.getElementByID("root")
)
`


## Fragment
`<></>`

Allows the wrapping of elements in a react component without using divs
