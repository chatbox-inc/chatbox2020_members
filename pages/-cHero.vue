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
    bottom: -80px;
    left: 50%;
    width: 3px;
    height: 160px;
    content: "";
    background-color: #c3504f;
    transform: translate(-50%);

    @include mobile {
      bottom: -25px;
      height: 50px;
    }
  }

  &__head {
    position: absolute;
    bottom: 70px;

    @include mobile {
      top: 92px;
    }
  }

  &__title {
    @include text-white;

    font-size: 45px;
    font-weight: bold;

    @include mobile {
      font-size: 30px;
    }
  }

  &__text {
    @include text-white;

    margin-top: 40px;
    font-size: 18px;

    @include mobile {
      margin-top: 3px;
    }
  }
}
</style>
