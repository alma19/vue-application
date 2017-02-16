<template>
    <div class="AlbumCovers">
      <div class="container covers">

        <!--looping through my JSON to place album covers-->
        <!--when you click on the album cover, the modal opens-->
        <!--also shoutout to kate she helped me alot with this if anyone deserves extra credit points its her -->

        <div v-for="album in albums">
          <img :src="album.albumCover" @click="add(album)" class="col-lg-4 cover" />
        </div>

        <Modal v-if="showModal" @close="showModal=false" :album="activeAlbum">
          <Intro :album="activeAlbum"></Intro>
          <MusicPlayer :album="activeAlbum"></MusicPlayer>
          <VideoPlayer :album="activeAlbum"></VideoPlayer>
        </Modal>

        <div class="app-footer"><a href="http://almawashington.com" target="_blank">Alma Washington.</a> 2017. Beyoncé album information & photos obtained from  <a href="https://en.wikipedia.org/wiki/Beyonc%C3%A9_discography" target="_blank">Wikipedia.</a></div>



      </div> <!--covers-->
    </div> <!--AlbumCovers-->
</template>

<script>

import Intro from './Intro'
import MusicPlayer from './MusicPlayer'
import Modal from './Modal'
import VideoPlayer from './VideoPlayer'

export default {
  props: [
    'albums'
  ],
  components: {
    Intro,
    MusicPlayer,
    Modal,
    VideoPlayer
  },
  data () {
    return {
      showModal: false,
      activeAlbum: ''
    }
  },
  methods: {
    // setting activeAlbum so you can loop through JSON
    add: function (album) {
      this.activeAlbum = album
      this.showModal = true
    }
  }
}
</script>

<style scoped>
.AlbumCovers {

}
</style>
