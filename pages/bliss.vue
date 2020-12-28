<template>
  <div class="food">
    <BlissBanner />
    <BlissDescription />
    <BlissMain
      @playVideo="playVideo"
      @displayDetail="displayDetailBliss"
      @displayDetail1="displayDetailBliss1"
    />
  </div>
</template>

<script>
import BlissBanner from '~/components/section/BlissBanner.vue'
import VideoPalyModal from '~/components/global/VideoPalyModal.vue'
import DetailModalBliss from '~/components/global/DetailModalBliss.vue'
export default {
  components: { BlissBanner },
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
        channelName: 'Bliss',
        personName: 'Colinz',
        titleVideo: 'Title of video',
        descriptionVideo: 'Description of the video',
      })
    },
    displayDetailBliss() {
      this.$modal.show(DetailModalBliss, {})
    },
    displayDetailBliss1() {
      this.$modal.show(DetailModalBliss, {})
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
