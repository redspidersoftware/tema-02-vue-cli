<template>
  <h1>Mi contador</h1>
  <p>Valor del contador: ...valor: {{ i }}</p>
  <button @click="incrementa">incrementa</button>
  <button @click="guardarDatos">guardar Datos</button>
</template>

<script setup lang="ts">
import { ref, reactive } from 'vue';

type EstadoContador = {
  contador: number;
  nombre: string;
};

const estado = reactive<EstadoContador>({
  contador: 15,
  nombre: 'Lucas',
});
const i = ref(0);
const incrementa = () => {
  i.value++;
};

const guardarDatos = () => {
  localStorage.setItem('valor-vue', i.value.toString());
  alert(
    `Se gurdo correctamente un ${
      localStorage.getItem('valor-vue') | 'Nada guardado'
    }`
  );
};
</script>
