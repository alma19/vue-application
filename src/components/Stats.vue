<template>
  <div class="Stats col-lg-5 col-sm-12">
    <h1>Stats</h1>
    <p class="inner-stats" v-for="extra in album.extras">
    {{extra}}
    </p>
  </div>
</template>

<script>
export default {
  props: [
    'album'
  ]
}
</script>

<style scoped>
.Stats {
  margin-top: 5px;
  margin-bottom: 10px;
  border: 5px solid #808080;
  padding: 10px 5px 5px 5px;
}

.inner-stats {
  padding: 10px;
}

h1 {
  font-family: 'Oswald', sans-serif;
  font-size: 2em;
  margin-bottom: 10px;
  color: #D8AEC8;
  font-weight: bold;
}
</style>
