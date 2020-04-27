<template>
  <section class="c-hero">
    <div class="c-container">
      <div class="c-hero__head">
        <h2 class="c-hero__title">
          chatboxでの<br class="c-hero__break" />働き方
        </h2>
        <p class="c-hero__text">
          個人の力でチームが活きる
        </p>
      </div>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.c-hero {
  position: relative;
  width: 100%;
  height: 585px;
  background-image: url("~assets/image/hero/img_top@2x.png");
  background-position: center;
  background-size: cover;

  @include mobile {
    height: 330px;
    background-position: left;
  }

  &::after {
    position: absolute;
    bottom: -8rem;
    left: 50%;
    width: 0.3rem;
    height: 16rem;
    content: "";
    background-color: #c3504f;
    transform: translate(-50%);

    @include mobile {
      bottom: -2.5rem;
      height: 5rem;
    }
  }

  &__head {
    position: absolute;
    bottom: 7rem;

    @include mobile {
      top: 9.2rem;
    }
  }

  &__title {
    @include text-white;

    font-size: 4.5rem;
    font-weight: bold;

    @include mobile {
      font-size: 3rem;
    }
  }

  &__text {
    @include text-white;

    margin-top: 4rem;
    font-size: 1.8rem;

    @include mobile {
      margin-top: 0.3rem;
    }
  }
}
</style>
