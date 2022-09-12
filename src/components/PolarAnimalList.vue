<script setup>
import { ref } from "vue";
import PolarAnimalDetails from "./PolarAnimalDetails.vue";

const animalsList = ref([
  { name: "Polar Bear", isFav: false },
  { name: "Arctic Fox", isFav: true },
  { name: "Reindeer", isFav: false },
]);

const toggleFav = (animal) => {
  animal.isFav = !animal.isFav;
};
</script>

<template>
  <div>Hello Polar Animals!🐻</div>
  <ul>
    <li v-for="animal in animalsList" v-on:click="toggleFav(animal)">
      <h1 :class="{ fav: animal.isFav }">{{ animal.name }}</h1>
    </li>
  </ul>
  <PolarAnimalDetails msg="This is a parental message">
    <p>Hello, I'm some slotted content!</p>
  </PolarAnimalDetails>
</template>

<style scoped>
.fav {
  color: red;
}
</style>
