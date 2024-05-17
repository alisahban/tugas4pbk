<!-- src/components/ProvinceList.vue -->
<template>
    <div class="province-list">
      <h2>Daftar Provinsi di Indonesia</h2>
      <province-item
        v-for="province in provinces"
        :key="province.id"
        :province="province"
        @province-selected="handleProvinceSelected"
      >
        <template v-slot>
          <p>Ini adalah detail untuk {{ province.name }}</p>
        </template>
      </province-item>
      <p v-if="selectedProvince">
        Provinsi terpilih: {{ selectedProvince.name }}
      </p>
    </div>
  </template>
  
  <script>
  import ProvinceItem from './ProvinceItem.vue';
  
  export default {
    components: {
      ProvinceItem
    },
    data() {
      return {
        provinces: [
          { id: 1, name: 'Aceh', capital: 'Banda Aceh', population: '5,274,871', area: '57,956' },
          { id: 2, name: 'Bali', capital: 'Denpasar', population: '4,317,404', area: '5,780' },
          { id: 3, name: 'Banten', capital: 'Serang', population: '12,959,169', area: '9,662' },
          { id: 4, name: 'Bengkulu', capital: 'Bengkulu', population: '2,010,670', area: '19,919' },
          // Tambahkan data provinsi lainnya di sini
        ],
        selectedProvince: null,
      };
    },
    methods: {
      handleProvinceSelected(province) {
        this.selectedProvince = province;
      }
    }
  };
  </script>
  
  <style scoped>
  .province-list {
    width: 300px;
    margin: 0 auto;
  }
  </style>
  