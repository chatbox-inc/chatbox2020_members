<template>
  <section v-if="timeline" class="c-timeline">
    <div class="c-container">
      <div class="c-timeline__head">
        <h2 class="c-timeline__title">
          実績タイムライン
        </h2>
      </div>
      <div class="c-timeline__box">
        <div class="c-timeline__item">
          <time class="c-timeline__date">{{ timeline.joined }}</time>
          <div class="c-timeline__start"></div>
          <div class="c-timeline__event">
            <h3 class="c-timeline__subTitle">
              chatbox入社
            </h3>
          </div>
        </div>
        <div
          v-for="event in timeline.event"
          :key="event.id"
          class="c-timeline__item"
        >
          <time class="c-timeline__date">2020.04</time>
          <div class="c-timeline__img">
            <img :src="event.img" alt="実績画像" class="c-timeline__img" />
          </div>
          <div class="c-timeline__event">
            <h3 class="c-timeline__subTitle">
              {{ event.title }}
            </h3>
            <div class="c-timeline__info">
              <p class="c-timeline__work">
                <span class="c-timeline__infoTitle">案件内容</span>
                {{ event.work }}
              </p>
              <p class="c-timeline__part">
                <span class="c-timeline__infoTitle">担当範囲</span>
                {{ event.part }}
              </p>
            </div>
            <p class="c-timeline__text">
              {{ event.body }}
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
    timeline: {
      type: Object,
      required: true,
    },
  },
}
</script>

<style lang="scss" scoped>
.c-timeline {
  padding-top: 8.2rem;
  padding-bottom: 9.5rem;
  background-color: #faf7f7;

  @include mobile {
    padding-top: 4rem;
    padding-bottom: 10.3rem;
  }

  &__head {
    text-align: center;
  }

  &__date {
    font-size: 2.2rem;
    font-weight: bold;

    @include mobile {
      margin: 0 auto 0 0;
      font-size: 1.8rem;
    }
  }

  &__title {
    @include text-h2;

    @include mobile {
      font-size: 2rem;
    }
  }

  &__box {
    margin-top: 7rem;

    @include mobile {
      margin-top: 4rem;
    }
  }

  &__img {
    position: relative;
    z-index: 2;

    &::before {
      position: absolute;
      top: -17.5rem;
      left: 6.5rem;
      z-index: -3;
      display: inline-block;
      width: 1.1rem;
      height: 20rem;
      content: "";
      background-color: #f7dfdf;
    }
  }

  &__item {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 7.4rem;

    @include mobile {
      flex-direction: column;
      margin-top: 10rem;

      &:nth-child(1) {
        margin-top: 0;
      }
    }
  }

  &__start {
    z-index: 1;
    display: inline-block;
    width: 3.8rem;
    height: 3.8rem;
    background-color: #f7dfdf;
    border-radius: 8.3rem;

    @include mobile {
      display: none;
    }
  }

  &__event {
    z-index: 3;
    width: 56.4rem;
    padding: 1.5rem 4rem;
    background-color: #fff;
    border: 0.4rem solid #f7dfdf;
    border-radius: 0.5rem;

    @include mobile {
      width: 100%;
      padding: 2.5rem 1rem;
    }
  }

  &__subTitle {
    font-size: 2.2rem;
    font-weight: bold;

    @include mobile {
      font-size: 1.6rem;
      text-align: center;
    }
  }

  &__info {
    margin-top: 1.1rem;

    @include mobile {
      margin-top: 1.6rem;
    }
  }

  &__infoTitle {
    margin-right: 1rem;
    font-weight: bold;

    @include mobile {
      font-size: 1.4rem;
    }
  }

  &__part {
    margin-top: 0.5rem;

    @include mobile {
      font-size: 1.4rem;
    }
  }

  &__text {
    margin-top: 1.1rem;

    @include mobile {
      margin-top: 2.5rem;
      font-size: 1.4rem;
    }
  }
}
</style>
