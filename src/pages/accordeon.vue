<script setup lang="ts">
  import { ref } from "vue";
  const sectionOpen = ref(1);
</script>

<template >
    <h1>ici page de l'accordeon</h1>
    <br>
    <section>
        <button class="text-xl rounded-md bg-blue-300 px-1 mb-2" @pointerdown="sectionOpen = 1">bouton 1</button>
        <p v-show="sectionOpen === 1">Lorem ipsum dolor sit amet consectetur adipisicing elit. Assumenda veniam ut optio numquam quaerat ab quasi, nobis molestiae debitis ratione modi natus unde, vero, quod doloremque porro maiores hic eum!</p>
    </section>
    <section>
        <button class="text-xl rounded-md bg-blue-300 px-1 mb-2" @pointerdown="sectionOpen = 2">bouton 2</button>
        <p v-show="sectionOpen === 2">Eveniet quis facilis asperiores rerum sed iure, ut vel culpa unde eius dolorum velit eos. Recusandae rerum commodi cumque pariatur, incidunt consequatur iste, quaerat aperiam eaque necessitatibus nihil ullam sunt.</p>
    </section>
    <section>
        <button class="text-xl rounded-md bg-blue-300 px-1 mb-2" @pointerdown="sectionOpen = 3">bouton 3</button>
        <p v-show="sectionOpen === 3">Quam eos, labore et dicta at est cupiditate vitae omnis ex dignissimos totam aperiam! Ipsum atque illum, corrupti aliquid dolorum praesentium, obcaecati assumenda quos magnam iusto tenetur accusamus, rerum soluta?</p>
    </section>
    <section>
        <button class="text-xl rounded-md bg-blue-300 px-1 mb-2" @pointerdown="sectionOpen = 0">reset variable</button>
    </section>
</template>