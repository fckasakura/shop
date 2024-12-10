<template>
    <header class="header">
      <h1 class="logo">Ecommerce</h1>
      <div class="icon" @click="goToProfile"></div>
    </header>
  </template>
  
  <script>
  export default {
    name: 'AppHeader',
    methods: {
      goToProfile() {
       this.$router.push(); 
      },
    },
  };
  </script>
  
  <style scoped>
  .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 3rem 0;
    margin: 0 auto;
    width: 100%;
    max-width: 1200px; 
  }
  
  .logo {
    font-size: 1.5rem;
    font-weight: bold;
    margin: 0;
  }
  
  .icon {
    width: 20px;
    height: 20px;
    background-image: url('@/assets/user-icon.png');
    background-size: contain;
    background-repeat: no-repeat;
    cursor: pointer;
  }
  </style>
  