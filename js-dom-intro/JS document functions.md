An HTML element is defined by a `<tag></tag>`

When we load a page in our browser, the browser creates a JS object called `document` that has a lot of properties and functions to modify and change the HTML page that the user sees.

# Creating elements

We CREATE a new element using `document.createElement('tagname')`

https://developer.mozilla.org/en-US/docs/Web/API/Document/createElement

```js
const p = document.createElement(p)
```

# Modifying elements

We can modify HTML attributes: `<tag attribute="attribute value(s)"></tag>` and the inner text:

https://developer.mozilla.org/en-US/docs/Web/API/Element/setAttribute
https://developer.mozilla.org/en-US/docs/Web/API/HTMLElement/innerText

```js
const p = document.createElement(p)
p.setAttribute('class', 'cssClassName')
p.setAttribute('style', 'font-weight: bold;')
p.setAttribute('id', 'important-paragraph')

p.innerText = "This is an important paragraph!"
```

# Adding elements on a page

We can add an element inside another element using `otherElement.appendChild(newElement)`

https://developer.mozilla.org/en-US/docs/Web/API/Node/appendChild
https://developer.mozilla.org/en-US/docs/Web/API/Element/append

```js
const p = document.createElement(p)

// adding inside the body tag
document.body.appendChild(p)

const img = document.createElement(img)
// adding img inside p
p.appendChild(img)
```

# Selecting elements from a page

We use `document.querySelector('search string')` to get an existing element from a page.

https://developer.mozilla.org/en-US/docs/Web/API/Document/querySelector

We can select:
- by HTML tag name `document.querySelector('img')`
- by CSS class name `document.querySelector('.cssClassName')`
- by ID `document.querySelector('#element-id')`

```js
const selectedP = document.querySelector('p')
const violetElement = document.querySelector('.violet')
const importantParagraph = document.querySelector('#important-paragraph')
```

After you have selected an element and stored it in a variable, you can use that variable to: change attribute values; change the inner text; append more elements, etc...

