<template>
  <div id="download" class="bg-white">
    <div
      class="container container-customize"
      style="min-height: unset !important"
    >
      <div
        class="flex flex-wrap justify-center h-full items-start md:items-center md:py-12 py-8 md:pb-16"
      >
        <div
          class="w-full sm:w-6/12 md:w-8/12 lg:w-8/12 flex justify-center items-center md:justify-start download--blob"
        >
          <!-- <div class="download--blob"> -->
          <img src="~@/assets/img/download-1.png" alt="" srcset="" />
          <!-- </div> -->
        </div>
        <div
          class="w-full sm:w-6/12 md:w-4/12 lg:w-4/12 text-center md:text-left"
        >
          <h2
            class="bg-text-gradiant font-bold text-3xl tracking-wide md:text-4.5xl w-auto pt-4 md:pt-8 pb-8 animate"
          >
            Available in <br />
            app stores
          </h2>
          <p class="text-sm md:text-base text-muted animate bg-text-black">
            Download the app now from <br />
            appstores for Android and iOS
          </p>
          <div class="flex pt-8">
            <a
              href="https://apps.apple.com/us/app/frai-tv/id1512784736"
              target="__blank"
              class="mr-4"
            >
              <img
                src="@/assets/img/app-store.png"
                style="height: 48px"
                alt="App store"
              />
            </a>
            <a
              href="https://play.google.com/store/apps/details?id=tv.frai.fraitv"
              target="__blank"
            >
              <img
                src="@/assets/img/google-play.png"
                style="height: 48px"
                alt="Play Store"
              />
            </a>
          </div>
        </div>
      </div>
    </div>
    <div class="w-full">
      <hr class="w-1/6 h-1 rounded-sm bg-black opacity-75 mx-auto" />
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss">
.download--blob {
  img {
    width: 80%;
  }
}
// .download--blob {
//   background-size: contain;
//   background-position: center;
//   background-repeat: no-repeat;
//   position: absolute;
//   left: -16px;
//   transform: translateY(-2%);
//   height: auto;
//   width: 100vw;
//   height: 620px;
//   background-image: url('~@/assets/img/download.png');
// }
// @media (min-width: theme('screens.md')) {
//   .download--blob {
//     left: -16px;
//     transform: translateY(3%);
//     height: 520px;
//     width: 520px;
//   }
// }
// @media (min-width: theme('screens.lg')) {
//   .download--blob {
//     left: -16px;
//     transform: translateY(3%);
//     height: 620px;
//     width: 620px;
//   }
// }
</style>
