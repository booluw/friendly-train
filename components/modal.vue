<template>
  <section class="modal-container">
    <button class="modal__btn" @click="$emit('close')">
      <i class="lni lni-close" />
    </button>
    <div class="modal">
      <div class="row m-0">
        <div class="col-md-4 p-0">
          <img :src="require(`~/assets/img/${data.img}`)" class="responsive-img" alt>
        </div>
        <div class="col-md-8 p-0">
          <div class="modal__text">
            <h2 class="modal__heading heading heading--sub">
              {{ data.name }}
            </h2>
            <h3 class="modal__heading--sub heading heading--sub mb-3">
              {{ data.portfolio }}
            </h3>
            <p class="paragraph" v-html="data.text" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    data: {
      type: Object,
      required: true
    }
  }
}
</script>

<style>

</style>
