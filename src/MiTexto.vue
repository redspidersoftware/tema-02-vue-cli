<template>
  <div>
    <p>Mi texto</p>
    <input type="text" @input="handleInput" v-bind:value="valorInput" />
    <input type="text" v-model="valorInput" />
    <button>Enviar</button>
    <p>El valor del input es: {{ valorInput }}</p>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const valorInput = ref('valor inicial');
const handleInput = (event: Event) => {
  //console.log(event);
  //console.log('He cambiado');
  console.log((event.target as HTMLInputElement).value);
  valorInput.value = (event.target as HTMLInputElement).value;
};
</script>
