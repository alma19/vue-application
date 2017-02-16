<template>
  <div class="VideoPlayer">

    <!--vue youtube embed component used https://github.com/kaorun343/vue-youtube-embed -->

    <youtube :video-id="videoID" @ready="ready" @playing="playing"></youtube>

  </div> <!--VideoPlayer-->
</template>

<script>
'use strict'
import Vue from 'vue'
import VueYoutubeEmbed from 'vue-youtube-embed'

Vue.use(VueYoutubeEmbed)

export default {
  props: [
    'albums'
  ],
  data () {
    return {
      videoID: 'ViwtNLUqkMY'
    }
  },
  methods: {
    ready (player) {
      this.player = player
    },
    playing (player) {
      // The player is playing a video.
    },
    stop () {
      this.player.stopVideo()
    },
    pause () {
      this.player.pauseVideo()
    }

  }

}
</script>

<style scoped>
.VideoPlayer {
}
</style>
