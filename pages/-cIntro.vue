<template>
  <section class="c-intro">
    <div class="c-container">
      <div class="c-head">
        <h2 class="c-head__title">
          <span class="c-head__color">働</span>く、学ぶ、成長する
        </h2>
      </div>
      <div class="c-box">
        <div class="c-box__item">
          <div class="c-box__img" />
          <div class="c-box__description">
            <p class="c-box__text">
              chatbox は職場環境を「スキルアップのプラットフォーム」と捉え、
              「働きながら学ぶ」の考え方を大切にしています。
              日々の仕事をこなすだけでなく、常に自分の数年後を見据えた仕事設計を。
              個人が組織に合わせるのではなく、
              それぞれのスタッフのキャリアプランに合わせて組織を変化させていくのが、chatbox
              の考え方です。<br />
              継続的な成長を続けるためには、精神的余裕の確保が必要不可欠です。
              リモートワークや自由な休暇制度、リクエストに応じて開講される技術セミナー等、
              それぞれが高いモチベーションを維持するための工夫を継続的に実施しています。<br />
              日々の「働く」を、楽しく余裕あるものに。自分の未来設計に合わせた意欲ある成長を。
              chatbox は個の成長を軸に、常に新しい形へと変化していきます。
            </p>
          </div>
        </div>
        <div class="c-box__item2">
          <ul class="c-list">
            <li class="c-list__item">
              <p class="c-list__text">
                学びながら働ける環境
              </p>
              <p class="c-list__text">
                個性を重視した環境
              </p>
              <p class="c-list__text">
                多様なコミニケーション
              </p>
            </li>
          </ul>
          <img
            src="@/assets/image/intro/img_02@2x.png"
            alt="社内イメージ画像"
            class="c-box__img2"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.c-intro {
  padding-top: 10.5rem;
  padding-bottom: 10rem;

  @include mobile {
    padding-top: 4.5rem;
    padding-bottom: 4rem;
  }
}

.c-head {
  text-align: center;

  &__title {
    font-family: Yu Mincho Medium, YuMincho, serif;
    font-size: 5rem;
    color: #393739;
    letter-spacing: 0.5rem;

    @include mobile {
      font-size: 2.5rem;
    }
  }

  &__color {
    @include text-accent;
  }
}

.c-box {
  margin-top: 5rem;

  @include mobile {
    margin-top: 2rem;
  }

  &__item {
    display: flex;
    align-items: top;

    @include mobile {
      display: block;
      text-align: center;
    }
  }

  &__item2 {
    display: flex;
    align-items: center;
    justify-content: space-between;

    @include mobile {
      flex-direction: column-reverse;
      margin-top: 2rem;
    }
  }

  &__img2 {
    position: relative;
    top: -2rem;
    left: -3.2rem;

    @include mobile {
      top: 0;
      left: auto;
      width: 20rem;
      height: 15rem;
    }
  }

  &__img {
    width: 70%;
    min-width: 546px;
    height: 708px;
    margin: 0 auto;
    background-image: url("~assets/image/intro/img_01@2x.png");
    background-size: cover;

    @include mobile {
      min-width: 280px;
      height: 317px;
      background-image: url("~assets/image/intro/sp_img_01@2x.png");
    }
  }

  &__description {
    position: relative;
    top: 3rem;
    left: -3.2rem;

    @include mobile {
      top: 0;
      left: auto;
      margin-top: 2rem;
    }
  }

  &__text {
    font-size: 1.5rem;
    line-height: 3rem;

    &:nth-child(2) {
      margin-top: 7rem;
    }

    &:nth-child(3) {
      margin-top: 4rem;
    }

    @include mobile {
      max-width: 280px;
      margin: 0 auto;
      font-size: 1.4rem;
      text-align: left;
    }
  }
}

.c-list {
  margin-left: 10%;

  @include mobile {
    margin-top: 2rem;
    margin-left: 0;
  }

  &__item {
    @include mobile {
      writing-mode: initial;
    }
  }

  &__text {
    @include text-accent;

    margin-top: 4rem;
    margin-left: 2rem;
    font-size: 2rem;
    font-weight: bold;

    &:nth-child(1) {
      margin-top: 0;
    }

    @include mobile {
      margin-left: 0;
      font-size: 1.2rem;

      &:nth-child(n + 2) {
        margin-top: 1.4rem;
      }
    }
  }
}
</style>
