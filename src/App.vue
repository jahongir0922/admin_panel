<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <div id="root">
    <div><RouterLink to="/">Home</RouterLink> <RouterLink to="/about">About</RouterLink></div>
    <RouterView />
  </div>
</template>

<style scoped></style>
