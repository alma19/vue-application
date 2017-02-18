<template>
  <div id="app">
    <div class="title">BEYONCÉ</div>
    <p id="title" class="container"> The purpose of this site is to provide an interactive look into Beyoncé's illustrious discography and music career. Click on an album to get the full Beyoncé experience. </p>
    <AlbumCovers :albums="albums"></AlbumCovers>

  </div><!--APP-->

</template>

<script>
import axios from 'axios'
import Intro from './components/Intro'
import Modal from './components/Modal'
import MusicPlayer from './components/MusicPlayer'
import AlbumCovers from './components/AlbumCovers'
import VideoPlayer from './components/VideoPlayer'

export default {
  name: 'app',
  components: {
    Intro,
    Modal,
    MusicPlayer,
    AlbumCovers,
    VideoPlayer
  },

  data () {
    return {
      albums: []
    }
  },

  methods: {

  },

  // getting JSON.
  mounted () {
    axios.get('/static/info.json')
    .then((response) => {
      this.albums = response.data
    })
  }

}
</script>

<style>
body {
  background-color: black;
}
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: black;
  padding-top: 60px;
}

  .title, #title {
    color: white;
  }

  .title {
    font-family: 'Oswald', sans-serif;
    font-size: 6em;
    font-weight: bold;
    color: #D8AEC8;
  }

.cover {
  padding: 15px;
  margin-bottom: 10px;
  cursor: pointer;
}

.cover:hover {
  opacity: 0.7;
}

.app-footer {
  margin: 20px;
  color: white;
}

a {
  color: #D8AEC8;
}

a:hover {
  color: white;
}

p {
  font-family: 'Droid Sans', sans-serif;
  font-size: 1.1em;
}
</style>
