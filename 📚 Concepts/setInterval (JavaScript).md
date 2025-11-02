# setInterval()

`setInterval(callback, delay)`  
Calls the given **callback function** every **delay** milliseconds until it’s stopped with `clearInterval()`.

**Example**
```js
const id = setInterval(() => {
  console.log("tick");
}, 1000);

// To stop:
clearInterval(id);
