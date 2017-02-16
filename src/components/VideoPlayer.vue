<template>
  <div class="VideoPlayer">

    <!--vue youtube embed component used https://github.com/kaorun343/vue-youtube-embed -->

    <!--setting up youtube player --> 
    <youtube :video-id="videoID" @ready="ready" @playing="playing" @getAlbum(album)></youtube>

  </div> <!--VideoPlayer-->
</template>

<script>
'use strict'
import Vue from 'vue'
import VueYoutubeEmbed from 'vue-youtube-embed'

Vue.use(VueYoutubeEmbed)

export default {
  props: [
    'album'
  ],
  data () {
    return {
      // getting video id from JSON
      videoID: this.album.video
    }
  },
  methods: {
    ready (player) {
      this.player = player
    },
    playing (player) {
     // The player is playing a ideo.
    },
    stop () {
      this.player.stopVideo()
    },
    pause () {
      this.player.pauseVideo()
    },
    getAlbum (album) {
      this.activeAlbum = album
    }
  }

}
</script>


<style scoped>
.VideoPlayer {
}
</style>
