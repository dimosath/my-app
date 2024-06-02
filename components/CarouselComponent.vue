<template>
    <div class="carousel">
      <div class="carousel-inner">
        <CardComponent
          v-for="(card, index) in cards"
          :key="index"
          :image="card.image"
          :title="card.title"
          :description="card.description"
          :link="card.link"
        />
      </div>
    </div>
  </template>
  
  <script>
  import CardComponent from './CardComponent.vue'
  
  export default {
    components: {
      CardComponent
    },
    props: {
      cards: {
        type: Array,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .carousel {
    overflow-x: auto; /* Enable horizontal scrolling */
  white-space: nowrap;
  }
  .carousel-inner {
    display: inline-flex;
  }
  .carousel-inner > * {
    scroll-snap-align: start;
    flex: 0 0 auto;
  }
  </style>
  
  