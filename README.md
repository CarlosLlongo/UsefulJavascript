# UsefulJavascript

## Get the stack trace for an error
```javascript
try {
	...
}
catch( oEx ) {
	console.log( oEx.message )
	console.log( oEx.stack );
}
```
## Invoke a Callback function
If we have a callback function:
```javascript
var fCallback = function () {};
```
Instead of invoking the function directly:
```javascript
fCallback();
```
We use the [.call()](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Function/call) function to pass the current object to the function, making it available inside the callback:
```javascript
fCallback.call( this );
```
