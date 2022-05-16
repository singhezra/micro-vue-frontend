<template>
  <div>
    <h1> Vue Micro Frontend </h1>
    <p>
      <span>
        Example app, built with
        <a href="https://vuejs.org/guide/introduction.html" target="_blank" rel="noopener noreferrer">Vue
        </a> and
        <a href="https://vuex.vuejs.org/" target="_blank" rel="noopener noreferrer">
          Vuex
        </a>
      </span>
    </p>
    <h3 class="counter">{{ counter }}</h3>
    <button @click="subtractFromCounter(parseInt(value))">-</button>
    <input type="number" v-model="value">
    <button @click="addToCounter(parseInt(value))">+</button>
    <div>
      <button class="btn" @click="addRandomNumber">
        Add by Random Number
      </button>
    </div>
  </div>
</template>

<script>
import { mapState, mapMutations, mapActions } from "vuex"
export default {
  data() {
    return {
      value: 1,
    }
  },
  computed: {
    ...mapState(["counter"])
  },
  methods: {
    ...mapMutations(["addToCounter", "subtractFromCounter"]),
    ...mapActions(["addRandomNumber"])
  }
}
</script>

<style>
.counter {
  font-size: 5rem
}

button {
  border-radius: 100%;
  border: none;
  width: 2rem;
  height: 2rem;
  font-weight: 700;
  cursor: pointer;
}

input {
  padding: 0.4rem;
  margin: 0 0.5rem;
  text-align: center;
}

.btn {
  border-radius: 0.5rem;
  width: auto;
  background-color: #41B983;
  margin-top: 1rem;
  color: white;
  cursor: pointer;
}
</style>