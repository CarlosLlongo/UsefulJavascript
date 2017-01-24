# UsefulJavascript

## Index
- [Get the stack trace for an error](#get-the-stack-trace-for-an-error)
- [Invoke a Callback function](#invoke-a-callback-function)
- [Measure code execution time](#measure-code-execution-time)
- [Set a default value for a JavaScript function parameter](#set-a-default-value-for-a-javascript-function-parameter)

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
## Measure code execution time
We can use the `performance.now()` function like this:
```javascript
var t0 = performance.now();
// Some code here to measure its execution time
var t1 = performance.now();
console.log( 'Execution time was: ' + ( t1 - t0 ) + " ms" );
```
## Set a default value for a JavaScript function parameter
In this example we want the default value for the `sampleParamter` to be `false`:
```javascript
function sampleFunction( sampleParameter ) {
    sampleParameter = typeof sampleParameter !== 'undefined' ? sampleParameter : false;
}
```
