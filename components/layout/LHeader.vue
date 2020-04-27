<template>
  <Header class="l-header">
    <div class="l-header__container">
      <nuxt-link to="/" class="l-header__triangle"></nuxt-link>
      <h1>
        <img
          src="@/assets/image/header/img_logo_chatbox@2x.png"
          alt="株式会社chatboxロゴ"
          class="l-header__logoImg"
        />
      </h1>
    </div>
  </Header>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.l-header {
  &__container {
    max-height: 14rem;
    padding: 3.7rem 0;
    text-align: center;

    @include mobile {
      max-height: 6rem;
      padding: 1rem 0;
    }
  }

  &__link {
    display: inline-block;
    width: 11rem;
    height: 11rem;
  }

  &__triangle {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 99;
    display: inline-block;
    width: 11rem;
    height: 11rem;
    border: 5.5rem solid transparent;
    border-top: 5.5rem solid #c2504f;
    border-left: 5.5rem solid #c2504f;

    @include mobile {
      width: 6rem;
      height: 6rem;
      border: 3rem solid transparent;
      border-top: 3rem solid #c2504f;
      border-left: 3rem solid #c2504f;
    }

    &::after {
      position: absolute;
      top: -4rem;
      left: -4rem;
      display: inline-block;
      width: 2.8rem;
      height: 2.8rem;
      content: "";
      background-image: url("~assets/image/header/icon_chatbox-white@2x.png");
      background-repeat: no-repeat;
      background-size: contain;

      @include mobile {
        top: -2rem;
        left: -2rem;
        width: 1.5rem;
        height: 1.5rem;
      }
    }
  }

  &__logoImg {
    width: 9rem;
    height: 6rem;

    @include mobile {
      width: 6.4rem;
      height: auto;
    }
  }
}
</style>
