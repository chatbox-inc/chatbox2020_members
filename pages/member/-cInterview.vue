<template>
  <section v-if="interview" class="c-interview">
    <div class="c-container">
      <div class="c-interview__head">
        <h2 class="c-interview__title">
          ミニインタビュー
        </h2>
      </div>
      <div class="c-interview__questions">
        <ul class="c-interview__list">
          <li
            v-for="data in interview"
            :key="data.id"
            class="c-interview__listItem"
          >
            <div class="c-interview__numberBox">
              <p class="c-interview__number" v-html="`0${data.id}`"></p>
            </div>
            <div class="c-interview__question">
              <p class="c-interview__q">
                {{ data.question }}
              </p>
              <p class="c-interview__a">
                {{ data.answer }}
              </p>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  props: {
    interview: {
      type: Array,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.c-interview {
  padding-top: 9rem;
  padding-bottom: 16.7rem;

  @include mobile {
    padding-top: 4rem;
    padding-bottom: 7rem;
  }

  &__head {
    @include text-h2;

    text-align: center;

    @include mobile {
      font-size: 2rem;
    }
  }

  &__listItem {
    display: flex;
    margin-top: 6.8rem;

    @include mobile {
      margin-top: 4rem;
    }
  }

  &__number {
    line-height: 5.4rem;

    @include mobile {
      line-height: 4rem;
    }
  }

  &__numberBox {
    @include text-white;

    width: 5.4rem;
    height: 5.4rem;
    margin-right: 4.5rem;
    text-align: center;
    background-color: $clr-primary;

    @include mobile {
      width: 4rem;
      min-width: 4rem;
      max-height: 4rem;
      margin-right: 1.5rem;
    }
  }

  &__q {
    font-size: 2rem;
    font-weight: bold;

    @include mobile {
      font-size: 1.6rem;
    }
  }

  &__a {
    margin-top: 1.6rem;

    @include mobile {
      margin-top: 1rem;
      font-size: 1.4rem;
    }
  }
}
</style>
