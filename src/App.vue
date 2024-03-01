<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <TheNavigation/>
    <br>
    <div class="container">
      <RouterView />
    </div>
</template>


<script>
import TheNavigation from '@/components/TheNavigation.vue'

export default {
  components: {TheNavigation}
}
</script>

