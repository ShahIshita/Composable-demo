<!-- src/App.vue -->


<template>
  <div id="app">
    <h1>Vue Composables Demo</h1>
    <p>Counter: {{ counter.count }}</p>
    <button @click="counter.increment">Increment</button>
    <button @click="counter.decrement">Decrement</button>
  </div>
</template>

<script>
import { useCounter } from './useCounter';

export default {
  name: 'App',
  setup() {
    const counter = useCounter();

    return {
      counter,
    };
  },
};
</script>



<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

button {
  margin: 10px;
  padding: 8px 16px;
  font-size: 16px;
}
</style>
