Arrays are a JS data type that allows us to store a list of values.

# Create

We use `const variable = []` to assign a new empty array to `variable`.

When we create a new array, we can add initial values:

```js
// create a new array with 5 initial values
const arr = [2, 4, 6, 8, 10]
```

If we want to copy/clone an existing array, we use the spread `[...original]` operator

```js
const original = [2, 4, 6, 8, 10]
// spread all the values in original into a new
// array
const copyied = [...original] 
```

# Read
To read a value from an array, we use `[index]` notation
```js
const arr = [2, 4, 6, 8, 10]
// read the value 8, which is at index=3
const value = arr[3] // get the value at 3rd index, store into `value`
```

# Update

We might want to add new elements to an existing array.

```js
const arr = [2, 4, 6, 8, 10]
// add 1 more element at the end
arr.push(12)
```

We might want to update the value at a specific index

```js
const arr = [2, 4, 6, 8, 10]
// set the value 6 to 7
// the value 6 has an index of 2
arr[2] = 7 //go to index 2, and assign the value 7
```

# Delete
To remove the last element, use `pop`
```js
const arr = [2, 4, 6, 8, 10]
arr.pop() // removes last element, which is 10
// arr = [2, 4, 6, 8]
```

To remove a number of elements starting from a particular index, use `splice`

```js
const arr = [2, 4, 6, 8, 10]
// remove 4, 6 (2 elements); 4 has an index of 1
arr.pop(1, 2) // from index 1, remove 2 elements
// arr = [2, 8, 10]
```

# Looping through array
```js
const arr = [2, 4, 6, 8, 10]
for(let i = 0; i < arr.length; i++) {
	console.log('i=', i, 'arr[i]=', arr[i])
}
```