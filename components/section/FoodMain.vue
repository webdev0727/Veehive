<template>
  <div class="food__main food__container">
    <div>
      <div class="food__main--header flex align-center mt-5">
        <div class="food--image">
          <img src="~@/assets/img/xeson.svg" alt="" />
        </div>
        <div class="food--text p-5">
          <p class="food--name">Raheela Taj</p>
          <p class="food--content">Food Category Name</p>
        </div>
      </div>
      <div class="food__main--video flex flex-wrap">
        <div
          @click="clickedVideo('~@/assets/video/food1.mp4')"
          class="food--video-wrap w-full md:w-1/3"
        >
          <div>
            <img src="~@/assets/img/food-port-5.jpg" alt="" />
          </div>
        </div>
        <div @click="clickedDetail" class="food--video-wrap w-full md:w-1/3">
          <div>
            <img src="~@/assets/img/food-port-5.jpg" alt="" />
          </div>
        </div>
        <div @click="clickedDetail1" class="food--video-wrap w-full md:w-1/3">
          <div>
            <img src="~@/assets/img/food-port-5.jpg" alt="" />
          </div>
        </div>
      </div>
    </div>
    <div>
      <div class="food__main--header flex align-center mt-5">
        <div class="food--image">
          <img src="~@/assets/img/xeson.svg" alt="" />
        </div>
        <div class="food--text p-5">
          <p class="food--name">Raheela Taj</p>
          <p class="food--content">Food Category Name</p>
        </div>
      </div>
      <div class="food__main--video flex flex-wrap mb-10">
        <div
          @click="clickedVideo('~@/assets/video/food2.mp4')"
          class="food--video-wrap w-full md:w-1/3"
        >
          <div>
            <img src="~@/assets/img/food-port-6.jpg" alt="" />
          </div>
        </div>
        <div @click="clickedDetail" class="food--video-wrap w-full md:w-1/3">
          <div>
            <img src="~@/assets/img/food-port-6.jpg" alt="" />
          </div>
        </div>
        <div @click="clickedDetail1" class="food--video-wrap w-full md:w-1/3">
          <div>
            <img src="~@/assets/img/food-port-6.jpg" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  },
  mounted() {},
  destroyed() {},
  methods: {
    clickedVideo(index) {
      this.$emit('playVideo', index)
    },
    clickedDetail() {
      this.$emit('displayDetail')
    },
    clickedDetail1() {
      this.$emit('displayDetail1')
    },
  },
}
</script>

<style lang="scss">
.food {
  &__main--header {
    padding: 25px 0px;
    img {
      max-height: 82px;
    }
    @media (max-width: theme('screens.md')) {
      padding: 15px 15px;
    }
  }
  &--video {
    padding: 0px 0px 25px;
    @media (max-width: theme('screens.md')) {
      padding: 0px 0px 15px;
    }
    &-wrap {
      &:nth-child(1) {
        padding: 0px 80px 0px 0px;
      }
      &:nth-child(2) {
        padding: 0px 40px;
      }
      &:nth-child(3) {
        padding: 0px 0px 0px 80px;
      }
      @media (max-width: theme('screens.md')) {
        padding: 10px !important;
      }
      div {
        img {
          width: 100%;
        }
      }
    }
  }
}
</style>
