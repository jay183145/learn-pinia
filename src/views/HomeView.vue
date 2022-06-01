
<template>
  <div class="home">
    <div class="count">
      {{ count }}
    </div>
    <div class="buttons">
      <button @click="decreaserCount">Minus-</button>
      <button @click="increaserCount">Plus++</button>
    </div>
  </div>
</template>

<script setup>
import { ref } from "@vue/reactivity"

const count = ref(0)
const increaserCount = () => {
  count.value++
}
const decreaserCount = () => {
  count.value--
}

</script>

<style>
.count{
  font-size: 10rem;
  margin: 3rem;
}
.buttons button {
  font-size: 2rem;
  margin: 1rem;
  border-radius: 2rem;
  padding: 1rem 2rem;
}
</style>
