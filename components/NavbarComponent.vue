<template>
  <nav class="navbar">
    <ul>
      <li><nuxt-link to="/">Home</nuxt-link></li>
      <li><nuxt-link to="/about">About Us</nuxt-link></li>
      <li><nuxt-link to="/projects">Projects</nuxt-link></li>
      <li><nuxt-link to="/services">Services</nuxt-link></li>
      <li><nuxt-link to="/contact">Contact Us</nuxt-link></li>
      <li><nuxt-link to="/chatbot">Chatbot</nuxt-link></li>
    </ul>
  </nav>
</template>

<script>
export default {
}
</script>

<style scoped>
.navbar {
  background-color: #333;
  padding: 1rem;
}
.navbar ul {
  list-style: none;
  display: flex;
  justify-content: space-around;
  margin: 0;
  padding: 0;
}
.navbar li {
  margin: 0;
}
.navbar a {
  color: white;
  text-decoration: none;
}
.navbar a:hover {
  text-decoration: underline;
}
.navbar a:active {
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.3);
}
</style>
