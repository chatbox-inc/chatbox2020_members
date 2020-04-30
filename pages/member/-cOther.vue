<template>
  <section class="c-other">
    <div class="c-container">
      <div class="c-other__head">
        <h2 class="c-other__title">
          他のメンバー
        </h2>
        <div class="c-other__box">
          <div
            v-for="(user, index) in memberList"
            :key="index"
            class="c-other__item"
          >
            <nuxt-link :to="`/member/${user.id}`">
              <img :src="user.img" alt="人物画像" class="c-other__img" />
              <p class="c-other__name">
                {{ user.name_jp }}
              </p>
              <p class="c-other__job">
                {{ user.position }}
              </p>
            </nuxt-link>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    memberList: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.c-other {
  padding-top: 8.6rem;
  padding-bottom: 11.7rem;
  text-align: center;
  background-color: #f7dfdf;

  @include mobile {
    padding-top: 4rem;
    padding-bottom: 16.5rem;
  }

  &__title {
    font-size: 2.5rem;

    @include mobile {
      font-size: 2rem;
    }
  }

  &__box {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-top: 4.5rem;

    @include mobile {
      margin-top: 3rem;
    }
  }

  &__img {
    width: 13rem;
    height: 13rem;
    border-radius: 50%;
    object-fit: cover;

    @include mobile {
      width: 12rem;
      height: 12rem;
    }
  }

  &__item {
    width: 25%;

    @include mobile {
      width: 50%;

      &:nth-child(n + 3) {
        margin-top: 4rem;
      }
    }
  }

  &__name {
    @include text-primary;

    margin-top: 2rem;
    font-size: 2rem;
    font-weight: bold;

    @include mobile {
      margin-top: 0.6rem;
      font-size: 1.6rem;
    }
  }

  &__job {
    @include text-primary;

    margin-top: 0.4rem;
    font-size: 1.4rem;

    @include mobile {
      font-size: 1.2rem;
    }
  }
}
</style>
