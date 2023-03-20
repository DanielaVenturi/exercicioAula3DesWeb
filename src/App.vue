<script setup>
import {ref,computed} from "vue";
const contador1 = ref(0)
const contador2= ref(0)
const soma = computed(() => contador1.value + contador2.value) 

</script>

<template>
<div>
  Contador 1: {{ contador1 }}
  <button @click="contador1++">+</button>
  <button @click="contador1--">-</button>

</div>

<div>
  Contador 2: {{ contador2 }}
  <button @click="contador2++">+</button>
  <button @click="contador2--">-</button>
</div>
<div>
  Soma= {{ soma }}
</div>
<div v-if="soma > 10" class="verde">È maior que 10</div>
<div v-else="soma < 10" class="vermelho">é menor que 10</div>
<div ></div>

</template>

<style scoped>

</style>
