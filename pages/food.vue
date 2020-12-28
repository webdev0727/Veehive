<template>
  <div class="food">
    <FoodBanner />
    <FoodDescription />
    <FoodMain
      @playVideo="playVideo"
      @displayDetail="displayDetail"
      @displayDetail1="displayDetail1"
    />
  </div>
</template>

<script>
import FoodBanner from '~/components/section/FoodBanner.vue'
import VideoPalyModal from '~/components/global/VideoPalyModal.vue'
import DetailModal from '~/components/global/DetailModal.vue'
export default {
  components: { FoodBanner },
  //
  data() {
    return {
      isModalVisible: false,
    }
  },
  //
  mounted() {
    if (this.$route.hash)
      setTimeout(() => {
        try {
          this.$scrollTo(this.$route.hash)
        } catch {
          //
        }
      }, 200)
  },
  methods: {
    playVideo($event) {
      this.$modal.show(VideoPalyModal, {
        source: $event,
        channelName: 'Food',
        personName: 'Raheela Taj',
        titleVideo: 'Title of video',
        descriptionVideo: 'Description of the video',
      })
    },
    displayDetail() {
      this.$modal.show(DetailModal, {})
    },
    displayDetail1() {
      this.$modal.show(DetailModal, {})
    },
  },
}
</script>

<style lang="scss">
.food {
  background-color: white !important;
  &__container {
    max-width: 1110px;
    margin: auto;
  }
}
</style>
