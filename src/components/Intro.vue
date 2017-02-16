<template>
    <div class="Intro">
      <!--getting album overview from JSON-->
      <p>
        {{album.overview}}
      </p>
      <hr />
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
  padding: 10px;
}
p {
  text-align: left;
}

hr {
  background-color: black; 
}
</style>
