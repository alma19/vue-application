<template>
    <div class="Intro">
      <!--getting album overview from JSON-->
      <ul>
        <li><p><b>Recorded: </b>{{album.recorded}}</p> </li>
        <li><p><b>Released: </b>{{album.released}}</p> </li>
        <li><p><b>Genre: </b>{{album.genre}}</p> </li>
        <li><p><b>Label: </b>{{album.label}}</p> </li>
        <li><p><b>Sales: </b>{{album.sales}}</p> </li>
      </ul>

      <p class="intro-title">
        Background
      </p>
      <p class="intro-text">
        {{album.overview}}
      </p>
      <hr />
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
  padding: 10px;
}
p {
  text-align: left;
}

hr {
  background-color: #808080;
}

.intro-title {
  margin-top: 10px;
  font-weight: bold;
}
</style>
