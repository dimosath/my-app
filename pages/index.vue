<template>
  <div class="home">
    <h1>Welcome to Women's Rights Website</h1>
    
    <section>
      <h2>Latest Projects</h2>
      <CarouselComponent :cards="projects" />
    </section>
    
    <section>
      <h2>Our Services</h2>
      <CarouselComponent :cards="services" />
    </section>
    
    <section>
      <h2>Our Team</h2>
      <TeamCarouselComponent :team="team" />
    </section>
  </div>
</template>

<script>
import CarouselComponent from '~/components/CarouselComponent.vue';
import TeamCarouselComponent from '~/components/TeamCarouselComponent.vue';
import data from '~/static/data.json';

export default {
  components: {
    CarouselComponent,
    TeamCarouselComponent
  },
  data() {
    return {
      projects: data.projects,
      services: data.services,
      team: data.team
    }
  }
}
</script>

<style scoped>
.home {
  padding: 20px;
}

h1 {
  text-align: center;
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
