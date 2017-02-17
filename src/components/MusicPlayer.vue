<template>
  <div class="MusicPlayer">
    {{album.disclaimer}}
    <!--calling spotify playlist from the JSON file-->
    <iframe :src="album.link.href" width="300" height="380" frameborder="0" allowtransparency="true"></iframe>

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
.MusicPlayer {
  text-align: left; 
}
</style>
