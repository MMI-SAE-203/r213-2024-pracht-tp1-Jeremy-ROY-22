<script setup lang="ts">
  import { ref } from "vue";
  const maVar = ref(true);
  const test = ref(1);
  const test2 = ref(0);
  const test3 = ref(0);
</script>
<template>
  <h1 class="text-2xl">TP</h1>
  <h1 class="text-2xl">tests TD</h1>
  <button @click="maVar = !maVar">caché ou pas caché</button> <br>
  <h1 v-show="maVar" class="text-2xl">Bonjour monde !</h1>
  <br>
  <h1 v-show="test === 1" class="text-2xl">test vaut 1</h1>
  <h1 v-show="test === 2" class="text-2xl">test vaut 2</h1>
  
  
  <br><br>


  <p>test2 : {{ test2 }}</p>
  <button @click="test2 = 1">le premier :</button><br>
  <h1 v-show="test2 === 1" class="text-2xl">ma variable test2 vaut 1</h1>
  <button @click="test2 = 2">le deuxieme :</button><br>
  <h1 v-show="test2 === 2" class="text-2xl">ma variable test2 vaut 2</h1>
  <button @click="test2 = 0">reset</button>


  <br><br>


  <p>test3 : {{ test3 }}</p>
  <button @click="test3 += 1">plus 1</button><br>
  <button @click="test3 -= 1">moins 1</button>

</template>