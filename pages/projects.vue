<template>
    <div>
      <h1>Projects</h1>
      <div class="project-list">
        <CardComponent v-for="(project, index) in projects" :key="index" :image="project.image" :title="project.title" :description="project.description" :link="project.link" />
      </div>
    </div>
  </template>
  
  <script>
  import CardComponent from '~/components/CardComponent.vue'
  import data from '~/assets/data.json'
  
  export default {
    components: {
      CardComponent
    },
    data() {
      return {
        projects: data.projects
      }
    }
  }
  </script>
  
  <style scoped>
  .project-list {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    gap: 20px;
  }
  </style>
  