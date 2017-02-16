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
     // The player is playing a video.
    },
    stop () {
      this.player.stopVideo()  // stop the video
    },
    pause () {
      this.player.pauseVideo() // pause the video
    },
    getAlbum (album) {
      this.activeAlbum = album // setting album so you can loop through JSON to get the album ids
    }
  }

}
</script>


<style>
/*make youtube videos responsive!*/
iframe {
  width: 100% !important;
}
</style>
