<template>
    <div class="Intro">
      <!--getting album overview from JSON--> 
      <p>
        {{album.overview}}
      </p>
    </div>
</template>

<script>

import MusicPlayer from './MusicPlayer'

export default {
  props: [
    'album'
  ],
  components: {
    MusicPlayer
  }
}
</script>

<style scoped>
.Intro {
}
</style>
