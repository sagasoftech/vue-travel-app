<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <TheNavigation/>
    <br>
    <div class="container">
      <RouterView v-slot="{Component}">
        <!--<transition name="slide" mode="out-in">-->
        <!--<transition name="moveUp">-->
        <transition name="fade" mode="out-in">  
          <component :is="Component" :key="$route.path"></component>
        </transition>    
      </RouterView>      
    </div>
</template>


<script>
import TheNavigation from '@/components/TheNavigation.vue'

export default {
  components: {TheNavigation}
}
</script>

<!--
<style lang="css">
  .slide-enter-active,
  .slide-leave-active {
    transition: opacity 1s, transform 1s;
  }
  .slide-enter-from,
  .slide-leave-to {
    opacity: 0;
    transform: translateX(-30%);
  }
</style>
-->

<!--
<style lang="css">
  .moveUp-enter-active{
    animation: fadeIn 1s ease-in;
  }

  @keyframes fadeIn {
    0% {opacity: 0;}
    50% {opacity: 0.5;}
    100%{opacity: 1;}
  }

  .moveUp-leave-active{
    animation: moveUp 0.3s ease-in;
  }

  @keyframes moveUp {
    0% {transform: translateY(0);}
    100% {transform: translateY(-400px);}
  }
</style>
-->

<style lang="css">
  .fade-enter-active,
  .fade-leave-active {
    transition: opacity 0.3s;
  }
  .fade-enter-from,
  .fade-leave-to {
    opacity: 0;
  }
</style>