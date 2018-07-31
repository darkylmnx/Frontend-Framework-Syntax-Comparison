---
title: State
---

## React

```javascript
class Clock extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      now: Date.now()
    };
  }

  render() {
    return (
      <div>
        It is { this.state.now }.
      </div>
    );
  }
}
```

## Vue

```vue
<script>
export default {
  name: 'Clock',

  data() {
    return  {
      now: Date.now()
    };
  }
};
</script>

<template>
  <div>
    It is {{ now }}.
  </div>
</template>
```
