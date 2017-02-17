<template>
  <div class="Singles col-lg-5 col-sm-12">
    <h1>Singles</h1>
    <p class="inner-singles" v-for="single in album.singles">
    {{single}}
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
.Singles {
  margin-top: 5px;
  margin-bottom: 5px;
  border: 5px solid #808080;
  padding: 5px;
}

.inner-singles {
  padding: 5px;
}

h1 {
  font-family: 'Oswald', sans-serif;
  font-size: 2em;
  margin-bottom: 10px;
  color: #D8AEC8;
  font-weight: bold;
}
</style>
