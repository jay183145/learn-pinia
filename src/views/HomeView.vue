
<template>
  <div class="home">
    <div class="count">
      {{ stoerCounter.count }}
    </div>
    <div class="buttons">
      <button @click="decreaserCount">Minus-</button>
      <button @click="increaserCount">Plus++</button>
    </div>
    <hr>
    <div>
      This counter is: {{ oddOrEven }}
    </div>
  </div>
</template>

<script setup>
import { ref } from "@vue/reactivity"
import { computed } from "@vue/runtime-core"
import { useCounterStore } from "@/stores/counter"

const stoerCounter = useCounterStore()

const count = ref(0)
const increaserCount = () => {
  count.value++
}
const decreaserCount = () => {
  count.value--
}

const oddOrEven = computed(() => {
  if(count.value % 2 === 0) {
    return "Even"
  } else {
    return "Odd"
  }
})

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
