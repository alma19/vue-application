<template>
  <div class="Singles">
    <p>
    {{album.singles}}
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
}
</style>
