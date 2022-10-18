Run the html page using Live server; open Developer Tools and verify that the console messages appear in the `Console` tab of the Developer Tools

`index.html`

```html
<html>
  <head>
    <script src="index.js" defer></script>
  </head>
  <body>
    <p>Page has loaded</p>
  </body>
</html>
```

`index.js`

```js
// when index.js is loaded in the browser,
// the browser JS Engine will "run" this entire file, as if
// we were running `node index.js`
console.log("Hello! This JS comes from index.js");

const numbers = [1, 2, 3, 4, 5];
// for (let i = 0; i < numbers.length; i++) {
//   const num = numbers[i];
//   console.log("i=", i, "num=", num);
// }

function sumNumbers(numbersToAdd) {
  let total = 0;
  numbersToAdd.forEach((num) => {
    total += num; // total = total + num
  });
  return total;
}

console.log("Sum of `numbers` is:", sumNumbers(numbers));
```