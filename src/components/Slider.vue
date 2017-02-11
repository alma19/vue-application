<template>
  <div class="Slider" id="slider">
    <div class="tabs-container">
      <div class="tabs-holder" :style="{ left: computedLeftPosition }" >
        <div class="tab" id="tab1" :style="{ left: computedLeftPosition }"> dangerously in love
        </div>
        <div class="tab" id="tab2" :style="{ left: computedLeftPosition }"> b day
        </div>
        <div class="tab" id="tab3" :style="{ left: computedLeftPosition }"> i am sasha fierce
        </div>
        <div class="tab" id="tab4" :style="{ left: computedLeftPosition }"> 4
        </div>
        <div class="tab" id="tab5" :style="{ left: computedLeftPosition }"> beyonce
        </div>
        <div class="tab" id="tab6" > lemonade
        </div>
    </div>
  </div>


  <ul class="slider-nav">
    <li @click="currentTab = 1">Dangerously in Love</li>
    <li @click="currentTab = 2">B'Day</li>
    <li @click="currentTab = 3">I Am Sasha Fierce</li>
    <li @click="currentTab = 4">4</li>
    <li @click="currentTab = 5">Beyoncé</li>
    <li @click="currentTab = 6">Lemonade</li>
  </ul>
  </div>
</template>

<script>
export default {
  data () {
    return {
      currentTab: 1
    }
  },
  computed: {
    computedLeftPosition () {
      return ((this.currentTab - 1) * -100) + '%'
    }
  }

}

</script>


<style scoped>

  #slider {

  }

  .tabs-container {
  position: relative;
  height: 400px;
  width: 800px;
  overflow: hidden;
  border: 1px solid #ccc;
  display: flex;
  align-items: center;
  }

  .tabs-holder {
  position: absolute;
  width: 4800px;
  top: 0;
  left: 0;
  transition: left 0.75s;
  }

  .tab {
  width: 800px;
  height: 400px;
  float: left;
  }

  ul {
  display: flex;
  }

  li {
  cursor: pointer;
  margin: 10px;
  }

  li:hover {
  color: #777;
  }

  #tab1, #tab2, #tab3, #tab4, #tab5, #tab6 {
    background-color: white;
    font-size: 50px;
  }

  ul {
    list-style: none;
  }

  li {
    color: white;
  }

</style>
