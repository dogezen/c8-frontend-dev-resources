The browser uses an event loop to wait for user interaction. When the user interacts with the page, the browser captures that information in the form of Event objects and makes that information available to the developer.

As a developer, we can register to receive events and run function code when these events occur.

```js

// we need an HTML element to target so that we can listen for events
// and have a function run when the event is fired up by the user
const targetHTMLElement = document.querySelector('button')

targetHTMLElement.addEventListener('click', () => {
	console.log('target html element has been clicked')
})

```

https://developer.mozilla.org/en-US/docs/Web/API/EventTarget/addEventListener

There are many types of events we can listen for: `click`, `submit` (when a form is submitted), `input` when an input in a form field is modified.

https://www.w3schools.com/jsref/dom_obj_event.asp

 `addEventListener` takes 2 parameters; 
 - Paramenter 1: is the name of the event to listen for, in the example above that is the click. 
 - Parameter 2: is a function that takes 0 or 1 arguments. This function is called a `callback` because it is called in response to the event. The function's optional parameter is the Event JS Object.

The Event JS object has a lot of intersting and useful properties, like the `event.target`. The `target` is the HTML element where the event was fired.

https://developer.mozilla.org/en-US/docs/web/api/event

## Note: adding multiple event listeners

You can add multiple event liseners to a JS object

```js
const button = ...
button.addEventListener('click', incrementCount)
button.addEventLisener('click', showCountAlertToUser)

// both functions, incrementCount and showCOuntAlertToUser will be called on a signle click
```

## Prevent default behaviour

Certain JS Events come with default behaviour in the browser. For example, when a user submits a form, the `submit` event is created. The browser will then handle it by refreshing the page. If we don't want this to happen, we can tell the browser to not perform the default behaviour.

```js
form.addEventListener('submit', (event) => {
	event.preventDefault() // page won't be reloaded after submit
})
```