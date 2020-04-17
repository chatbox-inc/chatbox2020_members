<template>
  <section class="c-members">
    <div class="c-container">
      <div class="c-members__head">
        <h2 class="c-members__headTitle">
          <span class="c-members__headColor">M</span>ember
        </h2>
      </div>
      <div class="c-members__box">
        <div
          v-for="member in getSomeMember"
          :key="member.id"
          class="c-members__item"
        >
          <nuxt-link :to="`/member/${member.id}`" class="c-members__link">
            <img :src="member.img" class="c-members__itemImg" alt="社員写真" />
            <div class="c-members__info">
              <p class="c-members__job">
                {{ member.position }}
              </p>
              <p class="c-members__name--jp">
                {{ member.name_jp }}
              </p>
              <p class="c-members__name--en">
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
  padding-bottom: 146px;
  background-color: #fcf3f3;

  @include mobile {
    padding-bottom: 110px;
  }

  &__head {
    position: relative;
    top: -65px;
    text-align: center;

    @include mobile {
      top: -20px;
    }
  }

  &__headTitle {
    font-family: Yu Mincho Medium, YuMincho, serif;
    font-size: 60px;
    color: #393739;
    letter-spacing: 5px;

    @include mobile {
      font-size: 25px;
    }
  }

  &__headColor {
    @include text-accent;

    font-size: 82px;

    @include mobile {
      font-size: 25px;
    }
  }

  &__box {
    display: flex;
    flex-wrap: wrap;
  }

  &__item {
    width: 25%;
    padding: 15px;
    text-align: center;

    @include mobile {
      width: 50%;
    }
  }

  &__itemImg {
    width: 203px;
    height: 205px;
    border-radius: 50%;
    object-fit: cover;
  }

  &__info {
    text-align: center;
  }

  &__job {
    @include text-primary;

    margin-top: 10px;
    font-size: 12px;
  }

  &__name--jp {
    @include text-primary;

    margin-top: 5px;
    font-size: 20px;

    @include mobile {
      font-size: 16px;
    }
  }

  &__name--en {
    padding-bottom: 20px;
    margin-top: 5px;
    font-size: 12px;
    color: #ccc4cb;
    border-bottom: 2px solid #c3504f;
  }
}
</style>
