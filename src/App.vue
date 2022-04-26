<script setup>
import { ref, shallowRef } from 'vue';

let person = ref({ name: 'wuyupei' });

let obj = shallowRef({ name: 'liuxu', p: { name: 'p' } });

console.log(person, obj);
console.log(person.value, obj.value);

setTimeout(() => {
  console.log(person);
}, 1000);

console.log('okok');
</script>

<template>
  <div>{{ person.name }}</div>
  <div>{{ obj.name }}</div>
  <div>{{ obj.p.name }}</div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
