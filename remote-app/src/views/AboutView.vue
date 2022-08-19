<script setup>
import { useCounterStore } from "../stores/counter";

const store = useCounterStore();
</script>
<template>
  <div class="about">
    <h1>This is an about page</h1>
    <div class="about__increment" @click="store.increment">
      Count: {{ store.counter }}
    </div>
  </div>
</template>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    align-items: center;
  }
}

.about__increment {
  cursor: pointer;
  padding: 1rem;
  margin: 1rem;
  user-select: none;
}
</style>
