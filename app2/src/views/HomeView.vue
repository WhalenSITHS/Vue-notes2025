<template>
  <div>
    <h1>{{ count }}</h1>
    <h2>{{ user }}</h2>
    <input type="text" v-model="user" />
    <button @click="increment">Click Me</button>
    <HelloWorld />
  </div>
</template>

<script setup>
import HelloWorld from '@/components/HelloWorld.vue'
import { ref, reactive } from 'vue'
const count = ref(7)
const user = ref('')
function increment() {
  count.value++
}
</script>

<style scoped></style>
