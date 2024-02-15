<script setup>
import CreateCategoryBtn from "./CreateCategory/CreateCategoryBtn.vue";
import Search from "./CreateCategory/Search.vue";
</script>

<template>
  <div class="container">
    <CreateCategoryBtn />
    <Search />
  </div>
</template>

<style scoped>
.container {
  display: flex;
  flex-direction: column;
  background-color: lightblue;
}
</style>
