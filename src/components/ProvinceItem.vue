<!-- src/components/ProvinceItem.vue -->
<template>
    <div class="province-item">
      <h3 @click="toggleDetails">{{ province.name }}</h3>
      <div v-if="showDetails">
        <slot></slot>
        <province-detail :province="province"></province-detail>
      </div>
    </div>
  </template>
  
  <script>
  import ProvinceDetail from './ProvinceDetail.vue';
  
  export default {
    components: {
      ProvinceDetail
    },
    props: ['province'],
    data() {
      return {
        showDetails: false
      };
    },
    methods: {
      toggleDetails() {
        this.showDetails = !this.showDetails;
        this.$emit('province-selected', this.province);
      }
    }
  };
  </script>
  
  <style scoped>
  .province-item {
    border: 1px solid #ccc;
    padding: 10px;
    margin: 10px 0;
    cursor: pointer;
  }
  .province-item:hover {
    background-color: #f0f0f0;
  }
  </style>
  