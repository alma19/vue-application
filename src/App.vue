<template>
  <div id="app">
    <h1>BEYONCE</h1>
    <p>info here</p>
    <div class="covers">

    <img src="./assets/dangerously.png" class="cover col-lg-4" id="dangerously" @click="openModal">

    <img src="./assets/bday.png" class=" cover col-lg-4">

    <img src="./assets/sashafierce.png" class="cover col-lg-4">

    <img src="./assets/4.png" class="cover col-lg-4">

    <img src="./assets/beyonce.png" class="cover col-lg-4">

    <img src="./assets/lemonade.png" class="cover col-lg-4">
  </div>

  </div>

</template>

<script>
import axios from 'axios'
import Hello from './components/Hello'
import Slider from './components/Slider'
import Intro from './components/Intro'
import BeyAlbums from './components/BeyAlbums'

export default {
  name: 'app',
  components: {
    Hello,
    Slider,
    Intro,
    BeyAlbums
  },

  data () {
    return {
      albums: []
    }
  },

  methods: {
    openModal () {
      console.log('Open')
    }

  },

  mounted () {
    axios.get('/static/info.json')
    .then((response) => {
      console.log(response.data)
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
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.cover {
  padding: 10px;
  cursor: pointer;
}

.cover:hover {
  opacity: 0.7;
}

.modal {
  display: none;
  position: fixed;
  z-index: 1;
  padding-top: 100px;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  overflow: auto;
  background-color: white;
}

.modal-content {
  background-color: #fefefe;
  margin: 15% auto;
  padding: 20px;
  border: 1px solid #888;
  width: 80%;
}

.close {
  color: #aaa;
  float: right;
  font-size: 28px;
  font-weight: bold;
}

.close:hover, .close:focus {
  color: black;
  text-decoration: none;
  cursor: pointer;
}

</style>
