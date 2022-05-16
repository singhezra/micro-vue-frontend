<template>
  <img class="logo" alt="Vue logo" src="./assets/logo.png">
  <CounterExample />
</template>

<script>
import CounterExample from "./components/CounterExample"


export default {
  name: 'App',
  components: {
    CounterExample
  }
}
</script>

<style>
#micro-vue-frontend {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#micro-vue-frontend .logo {
  margin: 0 auto;
}
</style>