<template>
  <section class="c-hero">
    <div class="c-hero__bg">
      <div class="c-container">
        <div class="c-hero__head">
          <h2 class="c-hero__title">
            メンバー紹介
          </h2>
          <p class="c-hero__text">
            株式会社chatboxの<br
              class="c-hero__break"
            />メンバー紹介ページです。
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.c-hero {
  width: 100%;

  &__bg {
    position: relative;
    min-height: 32.5rem;
    background-image: url("~assets/image/member/hero/img_memberTop@2x.png");
    background-position: center;
  }

  &__head {
    position: absolute;
    top: 6.6rem;
  }

  &__title {
    @include text-white;

    font-size: 3.5rem;

    @include mobile {
      font-size: 3rem;
    }
  }

  &__break {
    display: none;

    @include mobile {
      display: initial;
    }
  }

  &__text {
    @include text-white;

    margin-top: 4rem;
    font-size: 1.8rem;

    @include mobile {
      font-size: 1.6rem;
      line-height: 2;
    }
  }
}
</style>
