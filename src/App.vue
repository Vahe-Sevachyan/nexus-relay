<script setup>
import CategoryContainer from "./components/CategoryContainer.vue";
import DisplayCategory from "./components/DisplayContainer.vue";
</script>

<template>
  <div class="container">
    <CategoryContainer />
    <DisplayCategory />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  height: 100vh;
  /* padding-top: 0.5rem; */
}
</style>
