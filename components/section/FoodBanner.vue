<template>
  <div class="food--banner">
    <!-- <img src="~@/assets/img/food_banner_background.jpg" alt="" /> -->
  </div>
</template>

<script></script>

<style lang="scss">
.food--banner {
  margin-top: 0px;
  transition: all 0.2s;
  background: transparent url(~@/assets/img/food_banner_background.jpg)
    no-repeat center;
  background-size: cover;
  height: 240px;
  @media (max-width: theme('screens.md')) {
    margin-top: 0px;
  }
}
</style>
