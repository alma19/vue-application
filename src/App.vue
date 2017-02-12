<template>
  <div id="app">
    <div class="title">BEYONCÉ</div>
    <p id="title">info here</p>
    <div class="container covers">

    <img src="./assets/dangerously.png" class="cover col-lg-4" id="dangerously" @click="dangerouslyModal=true">

    <img src="./assets/bday.png" class="cover col-lg-4" @click="bdayModal=true">

    <img src="./assets/sashafierce.png" class="cover col-lg-4" @click="sashaFierceModal=true">

    <img src="./assets/4.png" class="cover col-lg-4" @click="showModal=true">

    <img src="./assets/beyonce.png" class="cover col-lg-4" @click="showModal=true">

    <img src="./assets/lemonade.png" class="cover col-lg-4" @click="showModal=true">

    <div class="app-footer"><a href="http://almawashington.com" target="_blank">Alma Washington.</a> 2017. Beyoncé album information & photos obtained from  <a href="https://en.wikipedia.org/wiki/Beyonc%C3%A9_discography" target="_blank">Wikipedia.</a></div>

    </div> <!--COVERS-->

    <!--I used the Bulma framework and this youtube tutorial (https://www.youtube.com/watch?v=Ebk2W3CA-UI) to make modals!!-->
    <Modal v-show="dangerouslyModal" @close="dangerouslyModal=false">
       <Intro :albums="albums"></Intro>

    </Modal>

    <Modal v-show="bdayModal" @close="bdayModal=false">
      <h1 style="color:black">{{ message }}</h1>
    </Modal>

    <Modal v-show="sashaFierceModal" @close="sashaFierceModal=false">
      <h1 style="color:black">{{ message }}</h1>
    </Modal>

    <Modal v-show="showModal" @close="showModal=false">
      <h1 style="color:black">{{ message }}</h1>
    </Modal>

</div><!--APP-->

</template>

<script>
import axios from 'axios'
import Intro from './components/Intro'
import Modal from './components/Modal'

export default {
  name: 'app',
  components: {
    Intro,
    Modal
  },

  data () {
    return {
      albums: [],
      dangerouslyModal: false,
      bdayModal: false,
      sashaFierceModal: false,
      showModal: false,
      message: 'Hi'
    }
  },

  methods: {

  },

  mounted () {
    axios.get('/static/info.json')
    .then((response) => {
      this.albums = response.data
      console.log(this.albums[0].albumName)
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
</style>
