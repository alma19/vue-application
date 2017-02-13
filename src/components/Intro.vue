<template>
  <div>
    <div :albums="albums" class="Intro">
       <h3>Intro Test</h3>
    </div>
    <MusicPlayer></MusicPlayer>
</div>
</template>

<script>

import MusicPlayer from './MusicPlayer'

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
