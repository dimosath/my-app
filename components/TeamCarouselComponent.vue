<template>
    <div class="carousel">
      <div class="carousel-inner">
        <TeamCardComponent
          v-for="(member, index) in team"
          :key="index"
          :image="member.image"
          :name="member.name"
          :role="member.role"
        />
      </div>
    </div>
  </template>
  
  <script>
  import TeamCardComponent from './TeamCardComponent.vue'
  
  export default {
    components: {
      TeamCardComponent
    },
    props: {
      team: {
        type: Array,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .carousel {
    display: flex;
    overflow-x: scroll;
    scroll-snap-type: x mandatory;
  }
  .carousel-inner {
    display: flex;
  }
  .carousel-inner > * {
    scroll-snap-align: start;
    flex: 0 0 auto;
  }
  </style>
  