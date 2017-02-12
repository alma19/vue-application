<template>
  <div class="Intro">
    <h3>{{album.albumName }}</h3>
    <p>{{album.singles.single1}}</p>
    <p>{{album.released}}</p>
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
.Intro {
}
</style>
