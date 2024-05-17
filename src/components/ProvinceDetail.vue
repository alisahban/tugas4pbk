<!-- src/components/ProvinceDetail.vue -->
<template>
  <div class="province-detail">
    <h4>{{ province.name }}</h4>
    <p>Ibu Kota: {{ province.capital }}</p>
    <p>Jumlah Penduduk: {{ province.population }}</p>
    <p>Luas Wilayah: {{ province.area }} km²</p>
  </div>
</template>

<script>
export default {
  props: ['province']
};
</script>

<style scoped>
.province-detail {
  border: 1px solid #ddd;
  padding: 10px;
  margin: 10px 0;
}
</style>
