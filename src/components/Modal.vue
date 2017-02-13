<template>
  <div class="Modal">

    <div class="modal is-active">
      <div class="modal-background"></div>
      <div class="modal-card">
        <header class="modal-card-head">
          <p class="modal-card-title">Modal Title</p>
        </header>
        <section class="modal-card-body">
          <slot></slot>
        </section>
        <footer class="modal-card-foot"> </footer>
        <button class="modal-close" @click="$emit('close')" ></button>
      </div>
    </div>

  </div>
</template>

<script>
export default {

  data () {
    return {

    }
  }

}
</script>

<style scoped>

</style>
