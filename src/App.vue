<script setup>
import {ref} from 'vue'
import WatchCard from './components/WatchCard.vue';

// on importe notre dataset qui simule un futur call api
import {userWatchList} from '@/assets/static/js/watchList.js'

const watchList = ref(userWatchList)

console.log(watchList)

</script>

<template>
  <div class='row'>
      <div class='col left'>
          <ul>
              <li>Ici c'est fixe</li>
              <li>Parent (nav, button, etc)</li>
          </ul>
          <span>▶ Lecture en cours: (ep title) </span>
         
      </div>
      <div class='col right'>

        <WatchCard 
          v-for="(episode,idx) in watchList"
          :key="idx"
          :ep-title="episode.title"
          :series="episode.series"
          :episode="episode.episode"
          :season="episode.season"
        />
       
        

      </div>
  </div>
</template>

<style scoped>

</style>
