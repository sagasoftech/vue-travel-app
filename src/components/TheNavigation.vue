<template>
    <div id="nav">
        <router-link 
            v-for="destination in destinations"
            :key="destination.id"
            :to="{name: 'destination.show', params:{id: destination.id}}"
            >
                {{ destination.name }}
      </router-link>
    </div>
</template>

<script>
import sourceData from '../data.json'

export default{
  data(){
    return{
      destinations: sourceData.destinations
    }
  }
}
</script>
