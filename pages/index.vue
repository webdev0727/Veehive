<template>
  <div>
    <Banner ref="banner" />
    <WhiteLine />
    <Features />
    <Channels />
    <Organigation />
    <Download />
    <Contact />
  </div>
</template>

<script>
import Organigation from '~/components/section/Organigation.vue'
import WhiteLine from '~/components/section/WhiteLine.vue'
export default {
  components: { Organigation, WhiteLine },
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
  methods: {},
}
</script>
