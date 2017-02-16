<template>
  <div class="Stats col-lg-6 col-sm-12">
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
  margin-top: 10px;
}

.inner-stats {
  padding: 10px; 
}
</style>
