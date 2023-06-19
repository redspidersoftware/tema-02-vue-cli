<template>
  <h1 class="saludo">{{ mensaje }}</h1>
  <button @click="handleClick">Click</button>
  <button v-on:click="handleClick">Otro Click</button>
</template>

<script setup lang="ts">
//composition API
const mensaje = 'Hola desde Compsition API';
const handleClick = () => {
  console.log('click dese handleClick');
};
</script>
//
<script lang="ts">
// options API
// export default {
//   data() {
//     const mensaje = 'Hola desde Option API';
//     return {
//       mensaje,
//     };
//   },
//   methods: {
//     handleClick: () => {
//       console.log('He hecho click');
//     },
//   },
// };
</script>
<style scoped>
.saludo {
  color: green;
}
</style>
