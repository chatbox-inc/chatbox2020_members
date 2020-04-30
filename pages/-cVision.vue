<template>
  <div class="c-vision">
    <div class="c-container">
      <div class="c-head">
        <h2 class="c-head__title">
          <span class="c-head__color">C</span>hatboxの理念
        </h2>
      </div>
      <div class="c-description">
        <p class="c-description__text">
          chatboxの理念は「それぞれがスキルアップするためのプラットフォームをつくる」こと。この理念に沿って、困った事を気軽に相談しあえる環境づくりや新しい技術を身につけるためのイベントの運営など、個々の成長を積極的にサポートしています。
        </p>
      </div>
      <div class="c-vision__box">
        <div class="c-point">
          <img
            src="@/assets/image/vision/img_point01@2x.png"
            alt="社内風景画像"
            class="c-point__img"
          />
          <div class="c-point__description">
            <p class="c-point__title">
              コミニケーション
            </p>
            <ul class="c-list">
              <li class="c-list__item">
                <p>リモートOK</p>
              </li>
              <li class="c-list__item">
                <p>slackやgithubの導入</p>
              </li>
              <li class="c-list__item">
                <p>遊び心も忘れない会話</p>
              </li>
            </ul>
          </div>
        </div>
        <div class="c-point">
          <img
            src="@/assets/image/vision/img_point02@2x.png"
            alt="社内風景画像"
            class="c-point__img"
          />
          <div class="c-point__description">
            <p class="c-point__title">
              個性重視
            </p>
            <ul class="c-list">
              <li class="c-list__item">
                <p>自由な出勤体制</p>
              </li>
              <li class="c-list__item">
                <p>学生アルバイトも多数在籍</p>
              </li>
              <li class="c-list__item">
                <p>柔軟な組織体制</p>
              </li>
            </ul>
          </div>
        </div>
        <div class="c-point">
          <img
            src="@/assets/image/vision/img_point03@2x.png"
            alt="社内風景画像"
            class="c-point__img"
          />
          <div class="c-point__description">
            <p class="c-point__title">
              学び&働く
            </p>
            <ul class="c-list">
              <li class="c-list__item">
                <p>スクールの定期開催</p>
              </li>
              <li class="c-list__item">
                <p>勉強会やコミュニティ運営</p>
              </li>
              <li class="c-list__item">
                <p>いつでも相談可能</p>
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.c-vision {
  padding-top: 9rem;
  padding-bottom: 19rem;

  @include mobile {
    padding-top: 5rem;
    padding-bottom: 8.5rem;
  }

  &__box {
    display: flex;
    justify-content: center;
    margin-top: 11rem;

    @include mobile {
      display: block;
      margin-top: 8.8rem;
    }
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

.c-description {
  margin-top: 6.5rem;

  @include mobile {
    margin-top: 2rem;
  }

  &__text {
    line-height: 3rem;

    @include mobile {
      font-size: 1.4rem;
    }
  }
}

.c-point {
  position: relative;
  width: 33%;
  margin-right: 1rem;
  text-align: center;
  background-color: #f5f1f1;
  border-top: 0.2rem solid #c3504f;

  &:nth-last-child(1) {
    margin-right: 0;
  }

  &::before {
    position: absolute;
    top: -5rem;
    left: 50%;
    z-index: -2;
    width: 10rem;
    height: 10rem;
    padding-top: 1.8rem;
    font-size: 1.8rem;
    color: #fff;
    content: "Point 1";
    background-color: #c3504f;
    border-radius: 10rem;
    transform: translate(-50%);
  }

  &:nth-child(2) {
    &::before {
      content: "Point 2";
    }
  }

  &:nth-child(3) {
    &::before {
      content: "Point 3";
    }
  }

  @include mobile {
    width: 100%;

    &:nth-child(n + 2) {
      margin-top: 8.8rem;
    }
  }

  &__description {
    padding: 1rem 0 2rem 0;
    background-color: #f5f1f1;
  }

  &__title {
    font-size: 2rem;
    font-weight: bold;

    @include mobile {
      font-size: 1.5rem;
    }
  }

  &__img {
    @include mobile {
      width: 100%;
    }
  }
}

.c-list {
  &__item {
    margin-top: 1rem;

    &:nth-child(n + 2) {
      margin-top: 1.6rem;
    }

    @include mobile {
      font-size: 1.4rem;
    }
  }
}
</style>
