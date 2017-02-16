<template>
  <div class="Stats">
    <p v-for="extra in album.extras">
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
}
</style>
