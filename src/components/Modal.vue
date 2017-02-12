<template>
  <div class="Modal">

    <div class="modal is-active">
      <div class="modal-background"></div>
        <div class="modal-content">
            <div class="box">
              <slot></slot>
            </div>
        </div>
    <button class="modal-close" @click="$emit('close')" ></button>
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
