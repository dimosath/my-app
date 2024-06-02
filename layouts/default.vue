<template>
    <div class="layout">
      <header>
        <h1>Women's Rights Website</h1>
        <NavbarComponent />
      </header>
      <main>
        <slot />
        <Nuxt />
      </main>
      <footer>
        <p>&copy; 2024 Women's Rights Website. All rights reserved.</p>
      </footer>
    </div>
  </template>
  
  <script>
  import NavbarComponent from '~/components/NavbarComponent.vue'
  
  export default {
    components: {
      NavbarComponent
    }
  }
  </script>
  
  <style scoped>
  .layout {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
  }
  
  header {
    text-align: center;
    background-color: #f8f8f8;
    padding: 20px 0;
  }
  
  main {
    flex: 1;
    padding: 20px;
  }
  
  footer {
    text-align: center;
    background-color: #333;
    color: white;
    padding: 10px 0;
  }
  </style>
  