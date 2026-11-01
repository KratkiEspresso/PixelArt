<template>
  <div class="pozadinaStranice">
    <h1>STRANICA U IZRADI....</h1>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
.pozadinaStranice {
  min-height: 100vh;
  background-image: url('@/assets/pozadina.jpg');
  background-size: cover;
  background-position: center;
  display: flex;
  justify-content: center;
  align-items: center;
}

h1 {
  font-size: 2.5rem;
  color: #1f2937;
  background-color: rgba(255, 255, 255, 0.9);
  padding: 15px 40px;
  border-radius: 10px;
  margin: 0; 
}
</style>