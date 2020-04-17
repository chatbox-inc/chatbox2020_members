<template>
  <div class="c-vision">
    <div class="c-container">
      <div class="c-vision__head">
        <h2 class="c-vision__headTitle">
          <span class="c-vision__headColor">C</span>hatboxの理念
        </h2>
      </div>
      <div class="c-vision__description">
        <p class="c-vision__text">
          chatboxの理念は「それぞれがスキルアップするためのプラットフォームをつくる」こと。この理念に沿って、困った事を気軽に相談しあえる環境づくりや新しい技術を身につけるためのイベントの運営など、個々の成長を積極的にサポートしています。
        </p>
      </div>
      <div class="c-vision__box">
        <div class="c-vision__point">
          <img
            src="@/assets/image/vision/img_point01@2x.png"
            alt="社内風景画像"
            class="c-vision__pointImg"
          />
          <div class="c-vision__pointDescription">
            <p class="c-vision__pointTitle">
              コミニケーション
            </p>
            <ul class="c-vision__list">
              <li class="c-vision__listItem">
                <p>リモートOK</p>
              </li>
              <li class="c-vision__listItem">
                <p>slackやgithubの導入</p>
              </li>
              <li class="c-vision__listItem">
                <p>遊び心も忘れない会話</p>
              </li>
            </ul>
          </div>
        </div>
        <div class="c-vision__point">
          <img
            src="@/assets/image/vision/img_point02@2x.png"
            alt="社内風景画像"
            class="c-vision__pointImg"
          />
          <div class="c-vision__pointDescription">
            <p class="c-vision__pointTitle">
              個性重視
            </p>
            <ul class="c-vision__list">
              <li class="c-vision__listItem">
                <p>自由な出勤体制</p>
              </li>
              <li class="c-vision__listItem">
                <p>学生アルバイトも多数在籍</p>
              </li>
              <li class="c-vision__listItem">
                <p>柔軟な組織体制</p>
              </li>
            </ul>
          </div>
        </div>
        <div class="c-vision__point">
          <img
            src="@/assets/image/vision/img_point03@2x.png"
            alt="社内風景画像"
            class="c-vision__pointImg"
          />
          <div class="c-vision__pointDescription">
            <p class="c-vision__pointTitle">
              学び&働く
            </p>
            <ul class="c-vision__list">
              <li class="c-vision__listItem">
                <p>スクールの定期開催</p>
              </li>
              <li class="c-vision__listItem">
                <p>勉強会やコミュニティ運営</p>
              </li>
              <li class="c-vision__listItem">
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

  &__head {
    text-align: center;
  }

  &__headTitle {
    font-family: Yu Mincho Medium, YuMincho, serif;
    font-size: 5rem;
    color: #393739;
    letter-spacing: 0.5rem;

    @include mobile {
      font-size: 2.5rem;
    }
  }

  &__text {
    line-height: 3rem;

    @include mobile {
      font-size: 1.4rem;
    }
  }

  &__headColor {
    @include text-accent;
  }

  &__description {
    margin-top: 6.5rem;

    @include mobile {
      margin-top: 2rem;
    }
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

  &__pointDescription {
    padding: 1rem 0 2rem 0;
    background-color: #f5f1f1;
  }

  &__point {
    position: relative;
    width: 30%;
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
  }

  &__pointTitle {
    font-size: 2rem;
    font-weight: bold;

    @include mobile {
      font-size: 1.5rem;
    }
  }

  &__pointImg {
    @include mobile {
      width: 100%;
    }
  }

  &__listItem {
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
