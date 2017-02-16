<template>
  <div class="Singles">
    <p v-for="single in album.singles">
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
}

</style>
