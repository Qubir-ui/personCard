<script setup>
import Header from "@/components/Header.vue";
import { ref } from 'vue';

const person = ref([]);

async function getData() {
    const res = await fetch("https://that-way.ru/test/api/test.php");
    person.value = await res.json();
}
getData()
</script>

<template>
  <Header/>

  <main>
      <h1 class="name">{{person.name}}</h1>
  </main>
</template>

<style scoped>

</style>
