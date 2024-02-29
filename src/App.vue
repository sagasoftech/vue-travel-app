<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <div>
        <RouterLink to="/">Home</RouterLink> | 
        <RouterLink to="/about">About</RouterLink>
    </div>
    <br>
  <RouterView />
</template>
