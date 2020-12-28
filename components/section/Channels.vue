<template>
  <div id="channels" class="bg-white">
    <!-- <div class="w-full">
      <hr class="w-1/6 h-1 rounded-sm bg-black opacity-75 mx-auto" />
    </div> -->
    <div class="py-4 md:pt-12 container container-customize">
      <h2
        class="text-center text-sm text-gray-800 font-bold tracking-widest my-6"
      >
        We provide these services:
      </h2>
      <div class="flex text-center justify-center flex-wrap mt-4 mb-5 md:mb-8">
        <div
          class="p-5 w-full md:w-1/3 flex flex-col justify-center items-center"
        >
          <div class="w-full md:w-2/3 flex justify-center items-center">
            <img
              src="~@/assets/img/saas-platform.svg"
              class="object-cover rounded-md"
              alt=""
            />
          </div>
          <!-- <h3 class="features--title no-mb pt-4">A SaaS Platform to host content to a closed group</h3> -->
          <p class="features--subtext">
            A SaaS Platform<br />to host content to a closed group
          </p>
        </div>
        <div
          class="p-5 w-full md:w-1/3 flex flex-col justify-center items-center"
        >
          <div class="w-full md:w-2/3 flex justify-center items-center">
            <img
              src="~@/assets/img/market-place.svg"
              class="object-cover rounded-md"
              alt=""
            />
          </div>
          <!-- <h3 class="features--title no-mb pt-4">Bliss</h3> -->
          <p class="features--subtext">
            A Marketplace<br />to showcase content
          </p>
        </div>
        <div
          class="p-5 w-full md:w-1/3 flex flex-col justify-center items-center"
        >
          <div class="w-full md:w-2/3 flex justify-center items-center">
            <img
              src="~@/assets/img/creative-service.svg"
              class="object-cover rounded-md"
              alt=""
            />
          </div>
          <!-- <h3 class="features--title no-mb pt-4">Bliss</h3> -->
          <p class="features--subtext">
            Creative Services<br />like branding and content creation
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.features {
  &--group-img,
  &--monotize-img {
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    height: 230px;
    width: 230px;
    padding-top: 100%; /* 1:1 Aspect Ratio */
    position: relative; /* If you want text inside of it */

    &:after {
      position: absolute;
      content: '';
      height: 50px;
      width: 50px;
    }
  }

  &--group-img {
    border-top-left-radius: 50%;
    background-image: url('~@/assets/img/closedgroup.png');
    &:after {
      right: -25px;
      bottom: 15%;
      border-bottom-right-radius: 50%;
      background-color: #336cea;
    }
  }

  &--monotize-img {
    border-bottom-left-radius: 50%;
    border-top-right-radius: 50%;
    background-image: url('~@/assets/img/monotize.png');
    &:after {
      right: -25px;
      bottom: 15%;
      height: 50px;
      border-bottom-left-radius: 50%;
      border-top-right-radius: 50%;
      background-color: #fc373c;
      width: 50px;
    }
  }

  &--title {
    @apply text-xl;
    @apply text-gray-900;
    font-weight: 600;
    margin-bottom: 1rem;
    &.no-mb {
      margin-bottom: 0.25rem;
    }
  }
  &--subtext {
    // @apply text-muted;
    // @apply text-xs;
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
