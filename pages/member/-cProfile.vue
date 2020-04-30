<template>
  <section class="c-profile">
    <div class="c-container">
      <div class="c-profile__box">
        <div class="c-profile__item">
          <img :src="profile.img" alt="メンバーの写真" class="c-profile__img" />
        </div>
        <div class="c-profile__item">
          <div class="c-profile__info">
            <h2 class="c-profile__name">
              {{ profile.name_jp }}
              <span class="c-profile__name--small">
                / {{ profile.name_en }}
              </span>
            </h2>
          </div>
          <div class="c-profile__info">
            <p class="c-profile__job">
              {{ profile.position }}
            </p>
          </div>
          <div class="c-profile__info">
            <p class="c-profile__text">
              {{ profile.body }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    profile: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.c-profile {
  width: 100%;
  padding-top: 7.5rem;
  padding-bottom: 8.5rem;

  @include mobile {
    padding-top: 4.5rem;
    padding-bottom: 5rem;
  }

  &__box {
    display: flex;
    align-items: center;
    justify-content: center;

    @include mobile {
      flex-direction: column;
    }
  }

  &__item {
    width: 50%;

    @include mobile {
      width: 100%;
    }
  }

  &__img {
    @include mobile {
      width: 100%;
    }
  }

  &__name {
    @include text-primary;

    position: relative;
    font-size: 3rem;
    font-weight: bold;
    letter-spacing: 0.25rem;

    &::before {
      position: relative;
      top: 0.4rem;
      display: inline-block;
      width: 1.3rem;
      height: 3rem;
      content: "";
      background-color: #c3504f;
    }

    @include mobile {
      font-size: 2.5rem;

      &::before {
        width: 1rem;
        height: 2.3rem;
      }
    }
  }

  &__name--small {
    position: absolute;
    right: 0;
    bottom: 7px;
    font-size: 1.6rem;
    letter-spacing: 0;

    @include mobile {
      font-size: 1.2rem;
    }
  }

  &__job {
    margin-top: 1.4rem;
    font-size: 1.6rem;
    font-weight: bold;
  }

  &__text {
    margin-top: 1rem;

    @include mobile {
      font-size: 1.4rem;
    }
  }
}
</style>
