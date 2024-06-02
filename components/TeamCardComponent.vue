<template>
    <div class="card">
      <img :src="image" alt="Team member image" class="card-img">
      <h3>{{ name }}</h3>
      <p>{{ role }}</p>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      image: {
        type: String,
        required: true
      },
      name: {
        type: String,
        required: true
      },
      role: {
        type: String,
        required: true
      }
    }
  }
  </script>
  
  <style scoped>
  .card {
    border: 1px solid #ccc;
    border-radius: 5px;
    padding: 16px;
    margin: 16px;
    text-align: center;
  }
  .card-img {
    max-width: 100%;
    height: auto;
  }
  </style>
  