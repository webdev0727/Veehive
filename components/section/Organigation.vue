<template>
  <div id="organization" class="organization bg-white">
    <div class="container container-customize flex justify-between flex-wrap">
      <div class="organization--background"></div>
      <div
        class="organization--text w-full md:w-1/2 flex justify-center p-5 py-8"
        style="flex-direction: column"
      >
        <h2 class="organization--title">Currently on <br />Veehive</h2>
        <p class="bg-text-black mt-5">
          Browse to see the organisations on our platform.
        </p>
      </div>
      <div class="py-4 w-full md:w-1/2">
        <div
          class="flex text-center justify-center flex-wrap mt-4 mb-5 md:mb-8"
        >
          <div
            class="p-5 w-full md:w-1/2 flex flex-col justify-center items-center"
          >
            <NuxtLink to="/food" class="w-full md:w-2/3">
              <div class="food-wrap flex justify-center">
                <img
                  src="~@/assets/img/xeson.svg"
                  alt=""
                  style="max-height: 202px"
                />
              </div>
            </NuxtLink>
            <h3 class="features--title no-mb pt-4">Food</h3>
          </div>
          <div
            class="p-5 w-full md:w-1/2 flex flex-col justify-center items-center"
          >
            <NuxtLink to="/bliss" div class="w-full md:w-2/3">
              <div class="food-bliss flex justify-center">
                <img
                  src="~@/assets/img/xeson.svg"
                  alt=""
                  style="max-height: 202px"
                />
              </div>
            </NuxtLink>
            <h3 class="features--title no-mb pt-4">Blyss</h3>
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
  // methods: {
  //   displayBliss() {
  //     this.$emit('displayBliss')
  //   },
  // },
}
</script>

<style lang="scss">
.organization {
  position: relative;
  z-index: 1;
  &--background {
    background-image: linear-gradient(
      to right,
      rgba(48, 122, 233, 0.55),
      rgba(62, 48, 233, 0.55),
      rgba(177, 29, 162, 0.55),
      rgba(255, 24, 24, 0.47),
      rgba(255, 127, 55, 0.55),
      rgba(255, 153, 0, 0.55)
    );
    opacity: 0.1;
    position: absolute;
    z-index: -1;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    width: 100%;
    height: 100%;
  }
  &--title {
    font-size: 60px;
    line-height: 60px;
    @media (max-width: theme('screens.md')) {
      font-size: 40px;
      line-height: 40px;
      text-align: center;
    }
  }
  .hex__center img:hover {
    cursor: pointer;
    opacity: 0.7;
    transition: all 0.3s;
  }
}
@media (min-width: theme('screens.md')) {
  .features {
    &--group-img,
    &--monotize-img {
      width: 100%;
      &:after {
        right: -40px;
        height: 80px;
        width: 80px;
      }
    }
    &--title {
      @apply text-2xl;
    }
    &--subtext {
      @apply text-base;
    }
  }
}
</style>
