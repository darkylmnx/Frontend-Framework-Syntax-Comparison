---
title: Handling Events
---

## React

```javascript
class Counter extends React.Component {
  constructor(props) {
    super(props);

    this.state = {
      count: 0
    };
    
    // you need this to keep context
    this.plus = this.plus.bind(this);
  },

  // regular with "bind"
  plus() { ... }

  // OR without "bind". Warning: experimental syntax.
  plus = () => { ... }

  render() {
    return (
      <div>
        <p>Value : { this.state.count }</p>
        <p>
          <button onClick={ this.plus }> plus </button>
          { /* OR with anonymous func */ }
          <button onClick={ (e) => this.plus(e) }> plus </button>
        </p>
      </div>
    );
  }
}
```

## Vue

```vue
<script>
export default {
  data() {
    return  {
      count: 0
    };
  },

  // Vue automatically binds the context to each methods
  methods: {
    plus() { ... }
  }
};
</script>

<template>
   <div>
      <p>Value : {{ count }}</p>
      <p>
        <button v-on:click="plus"> plus </button>
        <!-- short hand -->
        <button @click="plus"> plus </button>
        <!-- OR with explicit event passing -->
        <button @click="plus($event)"> plus </button>
      </p>
    </div>
</template>
```
