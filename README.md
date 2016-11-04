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
````
