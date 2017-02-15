<template>
    <div>
      <div class="container covers">

        <!--looping through my JSON to place album covers-->
        <!--when you click on the album cover, the modal opens-->
        <!--also shoutout to kate she helped me alot with this if anyone deserves extra credit points its her -->
        
        <div v-for="album in albums">
          <img :src="album.albumCover" @click="add(album)" class="col-lg-4 cover" />
        </div>

        <Modal v-if="showModal" @close="showModal=false" :album="activeAlbum">
          <Intro :album="activeAlbum"></Intro>
        </Modal>

      </div> <!--covers-->
    </div> <!--AlbumCovers-->
</template>

<script>

import Intro from './Intro'
import MusicPlayer from './MusicPlayer'
import Modal from './Modal'

export default {
  props: [
    'albums'
  ],
  components: {
    Intro,
    MusicPlayer,
    Modal
  },
  data () {
    return {
      showModal: false,
      activeAlbum: ''
    }
  },
  methods: {
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
