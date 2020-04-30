<template>
  <section class="c-members">
    <div class="c-container">
      <div class="c-head">
        <h2 class="c-head__title">
          <span class="c-head__color">M</span>
          ember
        </h2>
      </div>
      <div class="c-box">
        <div
          v-for="member in getSomeMember"
          :key="member.id"
          class="c-box__item"
        >
          <nuxt-link :to="`/member/${member.id}`" class="c-box__link">
            <img :src="member.img" class="c-box__img" alt="社員写真" />
            <div class="c-box__info">
              <p class="c-box__job">
                {{ member.position }}
              </p>
              <p class="c-box__name--jp">
                {{ member.name_jp }}
              </p>
              <p class="c-box__name--en">
                {{ member.name_en }}
              </p>
            </div>
          </nuxt-link>
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
  computed: {
    getSomeMember() {
      return this.memberList.slice(0, 8)
    },
  },
}
</script>

<style lang="scss" scoped>
.c-members {
  position: relative;
  padding-bottom: 14.6rem;
  background-color: #fcf3f3;

  @include mobile {
    padding-bottom: 11rem;
  }
}

.c-head {
  position: relative;
  top: -6.5rem;
  text-align: center;

  @include mobile {
    top: -2rem;
  }

  &__title {
    font-family: Yu Mincho Medium, YuMincho, serif;
    font-size: 6rem;
    color: #393739;
    letter-spacing: 0.5rem;

    @include mobile {
      font-size: 2.5rem;
    }
  }

  &__color {
    @include text-accent;

    position: relative;
    left: 1.7rem;
    display: inline-block;
    font-size: 8.2rem;

    @include mobile {
      left: 1rem;
      font-size: 2.5rem;
    }
  }
}

.c-box {
  display: flex;
  flex-wrap: wrap;

  &__item {
    width: 25%;
    padding: 1.5rem;
    text-align: center;

    @include mobile {
      width: 50%;
    }
  }

  &__img {
    width: 20.5rem;
    height: 20.5rem;
    border-radius: 50%;
    object-fit: cover;

    @include mobile {
      width: 12rem;
      height: 12rem;
    }
  }

  &__info {
    text-align: center;
  }

  &__job {
    @include text-primary;

    margin-top: 1rem;
    font-size: 1.2rem;
  }

  &__name--jp {
    @include text-primary;

    margin-top: 0.5rem;
    font-size: 2rem;

    @include mobile {
      font-size: 1.6rem;
    }
  }

  &__name--en {
    padding-bottom: 2rem;
    margin-top: 0.5rem;
    font-size: 1.2rem;
    color: #ccc4cb;
    border-bottom: 0.2rem solid #c3504f;
  }
}
</style>
