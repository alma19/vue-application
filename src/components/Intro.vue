<template>
  <div>
    <div :albums="albums" class="Intro">
       <h3>Intro Test</h3>
       <h1></h1>
    </div>
    <MusicPlayer></MusicPlayer>
</div>
</template>

<script>

import MusicPlayer from './components/MusicPlayer'

export default {
  props: [
    'albums'
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
