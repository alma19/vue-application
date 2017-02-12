<template>
  <div>
    <div :albums="albums" class="Intro">
      <h3>{{ this.albums[0].albumName }}</h3>
      <h1>hello</h1>
    </div>
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
.Intro {
}
</style>
