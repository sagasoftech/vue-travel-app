<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <img alt="Vue logo" src="@/assets/logo.svg" width="125" height="125" />
    <br>
    <div>
        <RouterLink to="/">Home</RouterLink> | 
        <RouterLink to="/about">About</RouterLink>
    </div>
    <br>
  <RouterView />
</template>
