<script setup>
import { ref, computed } from "vue";
const contador1 = ref(0)
const contador2 = ref(0)
const soma = computed(() => contador1.value + contador2.value)

</script>

<template>
  <div class="col-6">
    Contador 1: {{ contador1 }}
    <button class="btn btn-primary" @click="contador1++">+</button>
    <button class="btn btn-primary" @click="contador1--">-</button>

  </div>

  <div>
    Contador 2: {{ contador2 }}
    <button class="btn btn-primary" @click="contador2++">+</button>
    <button class="btn btn-primary" @click="contador2--">-</button>
  </div>
  <div>
    Soma= {{ soma }}
  </div>
  <div>A soma é: {{ soma }}</div>
  <div v-if="soma % 2 === 0">È par</div>
  <div v-else>È impar</div>
</template>

<style scoped></style>
