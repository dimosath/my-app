<template>
    <div class="card">
      <img :src="image" alt="Card image" class="card-img">
      <h3>{{ title }}</h3>
      <p>{{ description }}</p>
      <a :href="link" class="card-link">Learn more</a>
    </div>
  </template>
  
  <script>
  export default {
    props: {
      image: {
        type: String,
        required: true
      },
      title: {
        type: String,
        required: true
      },
      description: {
        type: String,
        required: true
      },
      link: {
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
  .card-link {
    display: block;
    margin-top: 8px;
    color: #007bff;
    text-decoration: none;
  }
  .card-link:hover {
    text-decoration: underline;
  }
  </style>
  