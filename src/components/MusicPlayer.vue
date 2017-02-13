<template>
  <div>
    <h2>MusicPlayer Test</h2>
   <!-- <iframe :src="this.albums[0].link.href" width="300" height="380" frameborder="0" allowtransparency="true"></iframe> -->
  </div>
</template>

<script>

export default {
  props: [
    'albums'
  ]
}
</script>

<style scoped>
.MusicPlayer {
}
</style>
