Objects are a JS data type that allows us to store a different values. Each value is assigned a key for easy retrieval.

# Create

We use `const variable = {}` to assign a new empty JS object to `variable`.

When we create a new object, we can specify initial values:

```js
// create a new object with some initial properties
const obj = {
	title: 'Some task', // use key: value, as syntax
	isDone: false
}
```

If we want to copy/clone an existing array, we use the spread `{...original}` operator

```js
const original = {
	title: 'Some task',
	isDone: false
}
// spread all the values in original into a new
// array
const copied = {...original} 
```

# Read
To read a value from an array, we use `obj.property` notation
```js
const task = {
	title: 'Some task',
	isDone: false
}

const completed = task.isDone
// or task['isDone']
```

Reading nested properties:

```js
const task = {
	title: 'Some task',
	isDone: false,
	assignedTo: {
		name: 'Carlo',
		email: 'email@example.com'
	}
}

// get the email of who has to do the task
const email = task.assignedTo.email
```

# Update

We might want to add new properties to an existing object.

```js
const task = {
	title: 'Some task',
	isDone: false
}

// add 1 more property
task.dueDate = '2022/10/17' // adds dueDate property with a string value
```

We might want to update an existing value of a property

```js
const task = {
	title: 'Some task',
	isDone: false
}
// set isDone property value to done
task.isDone = true
```

# Delete
To remove a property from an existing js object, we use `delete obj.property`

```js
const task = {
	title: 'Some task',
	isDone: false,
	dueDate: '2022/10/17'
}
// remove the dueDate property
delete task.dueDate
// task now has properties title, isDone only
```
