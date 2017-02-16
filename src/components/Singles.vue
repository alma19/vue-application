<template>
  <div class="Singles col-lg-6 col-sm-12">
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
  margin-top: 10px;
}

.inner-singles {
  padding: 5px; 
}

</style>
