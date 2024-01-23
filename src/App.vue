<template>
  <main>
    <h1 class="title">Counter App</h1>
    <div>
      <h4>The current count is ...</h4>
      <h1>{{ count }}</h1>
      <button @click="count--" id="subtract">-</button>
      <button @click="count++" id="add">+</button>
    </div>
  </main>
</template>

<script setup>
import { ref } from "vue";
const count = ref(0);
</script>

<style scoped>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

main {
  max-width: 100vw;
  height: 98vh;
  max-height: 100vh;
  background-color: aliceblue;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
}

.title {
  position: fixed;
  top: 1rem;
}

div {
  text-align: center;
}

button {
  border-style: none;
  border: 2px solid black;
  width: 2.5rem;
  height: 2rem;
  border-radius: 0.3rem;
  font-size: 1.5rem;
  cursor: pointer;
  margin: 0.5rem;
}

#add:hover {
  background-color: rgba(0, 128, 0, 0.8);
}

#add,
#add:active {
  background-color: green;
}

#subtract:hover {
  background-color: rgba(255, 0, 0, 0.6);
}

#subtract,
#subtract:active {
  background-color: red;
}
</style>
