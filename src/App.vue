<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <nav>
    <div class="navBar">
        <RouterLink to="/">Home</RouterLink>
        <RouterLink to="/gallery">Gallery</RouterLink>
        <RouterLink to="/crtanje">New</RouterLink>
    </div>
    <div class="navBar">
        <RouterLink to="/login">Login</RouterLink>
        <RouterLink to="/register">Register</RouterLink>
        <a href="#">Logout</a>
    </div>
  </nav>
  <RouterView />
</template>

<style>
html, body, #app {
  margin: 0;
  padding: 0;
  width: 100%;
  max-width: 100%;
  display: block; 
}

header {
  width: 100%;
  max-height: none;
  line-height: 1.5;
}

nav {
  display: flex;
  justify-content: space-between; 
  align-items: center;
  width: 100%;
  padding: 15px 24px;
  background-color: #f0f0f0;
  border-bottom: 2px solid #ccc;
}

.navBar {
  display: flex;
  gap: 15px;
}

a {
  text-decoration: none;
  color: black;
  font-weight: bold;
}

a:hover {
  color: #42b883;
}

a.router-link-active {
    color: #42b883;
}
</style>