<template>
  <div class="example-modal-content h-full">
    <div class="modal--wrap flex h-full">
      <div class="modal--video w-full md:w-3/5 self-center">
        <video controls>
          <!-- <source :src="getImgUrl(source)" type="video/mp4" /> -->
          <!-- <source :src="source" type="video/mp4" /> -->
          <source src="~@/assets/video/food2.mp4" type="video/mp4" />
        </video>
      </div>
      <div class="modal--description w-full md:w-2/5 p-5">
        <div class="modal--descr-header flex">
          <div class="modal--avatar"></div>
          <div class="modal--header--title p-2">
            <p>{{ channelName }}</p>
            <p>{{ personName }}</p>
          </div>
        </div>
        <div class="modal--description--main pt-5">
          <p>{{ titleVideo }}</p>
          <p>{{ descriptionVideo }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: [
    'source',
    'channelName',
    'personName',
    'titleVideo',
    'descriptionVideo',
  ],
  methods: {
    getImgUrl(url) {
      const res = url.indexOf('~@/') === 0 ? url.replace('~@', '/_nuxt') : url
      return res
    },
  },
}
</script>
<style lang="scss">
.modal {
  &--avatar {
    width: 63px;
    height: 63px;
    border-radius: 50%;
    background-color: #d8d8d8;
  }
  &--description {
    @media (max-width: theme('screens.md')) {
      display: none;
    }
  }
}
.v--modal-overlay div.v--modal-box {
  position: absolute !important;
  top: 50% !important;
  left: 50% !important;
  height: auto !important;
  transform: translate(-50%, -50%);
  @media (max-width: theme('screens.md')) {
    width: 80% !important;
  }
}
.v--modal-overlay {
  background: rgba(0, 0, 0, 0.8) !important;
}
</style>
