<template>
  <div class="example-modal-content h-full p-8">
    <Logo class="modal--logo mb-2 md:mb-4" />
    <div class="modal--descript">
      <p class="modal--text">
        Log in to the app to see all videos.<br />
        To dowload the app, click on the following link:
      </p>
    </div>
    <div class="modal--marks flex py-5 justify-between">
      <a
        href="https://apps.apple.com/us/app/frai-tv/id1512784736"
        target="__blank"
        class="mr-4"
      >
        <img src="@/assets/img/app-store.png" alt="App store" />
      </a>
      <a
        href="https://play.google.com/store/apps/details?id=tv.frai.fraitv"
        target="__blank"
      >
        <img src="@/assets/img/google-play.png" alt="Play Store" />
      </a>
    </div>
  </div>
</template>

<script>
export default {
  // props: ['channelName', 'personName', 'titleVideo', 'descriptionVideo'],
}
</script>
<style lang="scss">
.modal {
  &--logo {
    svg {
      width: 64px;
      height: 64px;
    }
    .logo-text {
      font-size: 32px;
    }
  }
  &--text {
    font-size: 16px;
  }
  &--marks {
    a {
      width: 47%;
    }
    img {
      width: 100%;
    }
  }
}
</style>
