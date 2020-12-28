<template>
  <div
    class="food__description food__container flex description py-0 md:py-5 pt-5 md:pt-0"
  >
    <div class="food__description--image">
      <div class="food-wrap">
        <div class="r-hex">
          <div class="r-hex-inner">
            <div class="r-hex-inner-2"></div>
          </div>
        </div>
      </div>
    </div>
    <div class="food__description--content p-5">
      <div class="text pb-5">
        <h2 class="food--title">Food</h2>
        <p class="food--description">
          Description of the channel comes here. Lorem ipsum dolor sit amet,
          consectetur adipiscing elit. Proin efficitur ex id nulla bibendum,
          malesuada bibendum dolor vestibulum. Mauris vitae turpis quis ex
          lacinia tristique sit amet id enim.
        </p>
      </div>
      <div class="food--button pt-5">
        <button type="button" class="mr-0 md:mr-5">subscribe</button>
        <button type="button">contact</button>
      </div>
    </div>
  </div>
</template>

<script></script>

<style lang="scss">
.food {
  &--title {
    font-size: 32px;
  }
  &__description {
    font-size: 16px;
    .hex__center {
      left: 50%;
      top: 0%;
      transform: translate(-50%, -30%);
      @media (max-width: theme('screens.md')) {
        transform: translate(-0%, -0%);
      }
    }
    @media (max-width: theme('screens.lg')) {
      flex-direction: column;
    }
  }
  &--button {
    @media (max-width: theme('screens.md')) {
      display: flex;
      justify-content: space-around;
    }
  }
}
.modal--button,
.food--button button {
  width: 152px;
  height: 36px;
  border-radius: 18px;
  border: 1px solid #355de9;
  font-size: 16px;
  text-transform: uppercase;
  color: #355de9;
  background-color: white;
  transition: all 0.3s;
  &:hover {
    background-color: #355de9;
    color: white;
    transition: all 0.3s;
  }
}
.food--button button {
  @media (max-width: theme('screens.md')) {
    width: 35%;
    font-size: 12px;
  }
}
</style>
