//JS
<script setup>
import { ref } from 'vue';
import HelloComponent from './components/HelloComponent.vue';
let count = ref(0);

const incriment = (v) => {
  count.value += v;
};
const dicriment = (v) => {
  count.value -= v;
};

</script>

// HTML
<template>
  <HelloComponent />
  <!-- Dinamic Binding -->
    <!-- <a v-bind:href="link">Google</a> -->
    <a :href="link">Google</a>
    <h2>Count {{ count }}</h2>
    <!-- Event Binding -->
    <!-- <button v-on:click="incriment(2)">Incriment</button> -->
    <button @:click="incriment(2)">Incriment</button>
    <button @click="dicriment(1)">Dicriment</button>
</template>

// CSS
<style scoped>

</style>
