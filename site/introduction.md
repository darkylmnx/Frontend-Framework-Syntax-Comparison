---
title: Introduction
---

::: tip
A basic understanding of **JavaScript** is necessary to continue.

If you are still **new to JavaScript**, consider learning the basics first.
:::

## What is Vue

Vue (pronounced /vjuː/, like view) is a progressive framework for building user interfaces.

Quick code example :
```html
<div id="app">
  {{ message }}
</div>
```

```js
var app = new Vue({
  el: '#app',
  data: {
    message: 'Hello Vue!'
  }
})
```

## What is React

React is a declarative, efficient, and flexible JavaScript library for building user interfaces.

Quick code example :
```html
<div id="root"></div>
```

```js
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```
