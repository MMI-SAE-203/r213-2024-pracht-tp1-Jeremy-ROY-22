<script setup lang="ts">
import { onErrorCaptured } from 'vue'
import { RouterLink, RouterView } from 'vue-router/auto'
import { ref } from "vue";
const menuIsOpen = ref(false)

onErrorCaptured((err, instance, info) => {
  console.error('erreur : ', err, '\ninfo : ', info, '\ncomposant : ', instance)
  return true
})
</script>

<template>
  <header >
    <button
    aria-controls="mainNav"
    aria-expanded="true"
    class="rounded-full border-2 border-green-600 bg-green-300 px-2"
    @pointerdown="menuIsOpen = !menuIsOpen"
    >
    menu
    </button>
  <!-- nav#mainNav>ul>li*3>a[href="#"]{item $} -->
  <Transition
  class="transition-transform duration-1000"
  enter-from-class="-translate-x-full"
  enter-to-class="translate-x-0"
  leave-active-class="-translate-x-full"
>
  <nav id="mainNav" v-show="menuIsOpen" class="ml-3">
    <ul>
      <li>
        <RouterLink to="App.vue" class="text-blue-500 underline"> Accueil </RouterLink>
      </li>
      <li>
        <RouterLink to="/" class="text-blue-500 underline"> index </RouterLink>
      </li>
      <li>
        <RouterLink to="/accordeon" class="text-blue-500 underline"> accordeon </RouterLink>
      </li>
      <li>
        <RouterLink to="/boucle" class="text-blue-500 underline"> boucle </RouterLink>
      </li>
    </ul>
  </nav>
  </Transition>
  </header>
  <RouterView v-slot="{ Component }">
    <Suspense>
      <component :is="Component" />
    </Suspense>
  </RouterView>
</template>
