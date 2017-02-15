<template>
  <div>
    <div :albums="albums" class="Intro">
       <h3>Intro Test</h3>
       <h1></h1>
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
