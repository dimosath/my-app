<template>
    <div class="about">
      <h1>About Us</h1>
      <p>This website aims to empower women and promote gender equality through education, advocacy, and community engagement. We strive to provide resources, support, and opportunities to women around the world.</p>
      
      <section>
        <h2>Our Team</h2>
        <TeamCarouselComponent :team="team" />
      </section>
    </div>
  </template>
  
  <script>
  import TeamCarouselComponent from '~/components/TeamCarouselComponent.vue';
  import data from '~/static/data.json';
  
  export default {
    components: {
      TeamCarouselComponent
    },
    data() {
      return {
        team: data.team
      }
    }
  }
  </script>
  
  <style scoped>
  .about {
    padding: 20px;
  }
  
  h1 {
    text-align: center;
    margin-bottom: 40px;
  }
  
  p {
    text-align: justify;
    margin-bottom: 40px;
  }
  
  section {
    margin-bottom: 60px;
  }
  
  h2 {
    text-align: center;
    margin-bottom: 20px;
  }
  </style>
  
  
  
  
  