<template>
  <div class="example-modal-content h-full p-8">
    <Logo class="modal--logo mb-2 md:mb-4" />
    <div class="modal--descript">
      <p class="modal--text">
        This channel is a paid subscription. To continue viewing the content,
        subscribe by paying AED 00.00.
      </p>
    </div>
    <div class="modal--marks flex py-5 justify-between">
      <button class="modal--button">continue to pay</button>
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
