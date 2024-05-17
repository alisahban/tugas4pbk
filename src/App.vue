<!-- src/App.vue -->
<template>
  <div id="app">
    <province-list></province-list>
  </div>
</template>

<script>
import ProvinceList from './components/ProvinceList.vue';

export default {
  components: {
    ProvinceList
  }
};
</script>

<style>
/* Tambahkan gaya CSS di sini jika perlu */
</style>
