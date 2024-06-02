<template>
    <div>
      <h1>Services</h1>
      <div class="service-list">
        <CardComponent v-for="(service, index) in services" :key="index" :image="service.image" :title="service.title" :description="service.description" :link="service.link" />
      </div>
    </div>
  </template>
  
  <script>
  import CardComponent from '~/components/CardComponent.vue'
  import data from '~/static/data.json'
  
  export default {
    components: {
      CardComponent
    },
    data() {
      return {
        services: data.services
      }
    }
  }
  </script>
  
  <style scoped>
  .service-list {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 20px;
  }
  </style>
  
  