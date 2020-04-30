<template>
  <footer class="l-footer">
    <div class="l-contact">
      <div class="l-contact__bg">
        <div class="l-head">
          <img
            class="l-head__icon"
            src="@/assets/image/footer/icon_mail.svg"
            alt="手紙のアイコン"
          />
          <h2 class="l-head__title">
            お問い合わせはこちら
          </h2>
        </div>
        <div class="c-container">
          <div class="l-box">
            <p class="l-box__text">
              Webにまつわるお悩み、<br />
              ご相談はお気軽にchatboxまで。
            </p>
            <div class="l-buttons">
              <nuxt-link to="/" class="c-footerButton">
                お問い合わせフォームへ
                <img
                  class="l-button__icon"
                  src="@/assets/image/footer/keyboard_arrow_right-24px.svg"
                  alt="右シェブロン"
                />
              </nuxt-link>
              <div class="l-call">
                <p class="l-call__text">
                  電話でのお問い合わせ<br />
                  <span class="l-call__number">050-3555-1212</span>
                </p>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="l-navi__container">
      <ul class="l-navi__list">
        <li class="l-navi__listItem">
          <nuxt-link to="/" class="l-footer__listLink">
            chatboxについて
          </nuxt-link>
        </li>
        <li class="l-navi__listItem">
          <nuxt-link to="/" class="l-footer__listLink">
            サービス
          </nuxt-link>
        </li>
        <li class="l-navi__listItem">
          <nuxt-link to="/" class="l-footer__listLink">
            メンバー
          </nuxt-link>
        </li>
        <li class="l-navi__listItem">
          <nuxt-link to="/" class="l-footer__listLink">
            お問い合わせ
          </nuxt-link>
        </li>
      </ul>
      <hr class="l-footer__divider" />
      <div class="l-footer__infos">
        <div class="l-footer__info">
          <img
            src="@/assets/image/footer/img_logo@2x.png"
            alt="株式会社chatboxロゴ"
            class="l-footer__infoLogo"
          />
          <small class="l-footer__copyright">
            Copyright © chatbox.inc All Rights Reserved.
          </small>
        </div>
        <div class="l-footer__info">
          <a href="#" class="l-footer__snsLink">
            <img
              src="@/assets/image/footer/facebook-square-brands.svg"
              alt="facebookロゴ"
              class="l-footer__sns"
            />
          </a>
          <a href="#" class="l-footer__snsLink">
            <img
              src="@/assets/image/footer/twitter-square-brands.svg"
              alt="facebookロゴ"
              class="l-footer__sns"
            />
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.l-contact {
  &__bg {
    background-color: #c3504f;
  }

  &__buttons {
    display: flex;
    align-items: center;
    margin-top: 6.6rem;

    @include mobile {
      flex-direction: column;
      margin-top: 6rem;
    }
  }
}

.l-footer {
  background-color: #fffcfc;

  &__callNumber {
    margin-top: 2rem;
    font-size: 3.2rem;
    font-weight: bold;

    @include mobile {
      font-size: 2.5rem;
    }
  }

  &__list {
    display: flex;

    @include mobile {
      justify-content: center;
    }
  }

  &__listItem {
    margin-right: 4.2rem;

    @include mobile {
      margin-right: 1rem;
      font-size: 1rem;
    }
  }

  &__listLink {
    @include text-accent;
  }

  &__divider {
    margin: 2.6rem 0 0 0;
    border-color: #c3504f80;
  }

  &__infos {
    display: flex;
    justify-content: space-between;
    margin-top: 1.8rem;

    @include mobile {
      margin-top: 4.3rem;
    }
  }

  &__info {
    display: flex;
    align-items: center;

    &:nth-child(1) {
      margin-right: 1.5rem;
    }
  }

  &__infoLogo {
    margin-right: 2rem;

    @include mobile {
      margin-right: 1rem;
    }
  }

  &__copyright {
    @include text-accent;

    @include mobile {
      font-size: 1rem;
    }
  }

  &__logoText {
    @include text-white;

    margin-top: 6rem;

    @include mobile {
      margin-top: 5rem;
      font-size: 1.2rem;
    }
  }

  &__snsLink {
    &:nth-child(1) {
      margin-right: 1.5rem;
    }
  }
}

.l-navi {
  &__container {
    max-width: 159rem;
    padding: 4.7rem 2.2rem 11.1rem 2.2rem;
    margin: 0 auto;

    @include mobile {
      padding-bottom: 1.5rem;
    }
  }

  &__list {
    display: flex;

    @include mobile {
      justify-content: center;
    }
  }

  &__listItem {
    margin-right: 4.2rem;

    @include mobile {
      margin-right: 1rem;
      font-size: 1rem;
    }
  }
}

.c-container {
  position: relative;
  padding-top: 9rem;
  padding-bottom: 7rem;

  @include mobile {
    padding-top: 7.9rem;
    padding-bottom: 9.9rem;
  }

  &::after {
    position: absolute;
    top: -0.1rem;
    left: 50%;
    width: 0;
    height: 0;
    content: "";
    border-color: #fff transparent transparent transparent;
    border-style: solid;
    border-width: 4rem 3.5rem 0 3.5rem;
    transform: translate(-50%);
  }
}

.l-head {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2.2rem 0;
  text-align: center;
  background-color: #fff;

  @include mobile {
    padding: 1.7rem 0;
  }

  &__icon {
    margin-right: 1rem;
  }
}

.l-buttons {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  margin-top: 6.6rem;

  @include mobile {
    flex-direction: column;
    margin-top: 6rem;
  }
}

.l-button {
  &__icon {
    position: relative;
    top: 1.2rem;
    margin-left: 3rem;

    @include mobile {
      position: absolute;
      top: 50%;
      width: 2.5rem;
      margin-left: 2rem;
      transform: translateY(-50%);
    }
  }
}

.l-box {
  text-align: center;
  background-color: #c3504f;

  &__text {
    @include text-white;

    font-size: 3rem;
    font-weight: bold;

    @include mobile {
      font-size: 1.6rem;
    }
  }
}

.l-call {
  margin-left: 9rem;
  text-align: left;

  @include mobile {
    margin-top: 5rem;
    margin-left: 0;
  }

  &__info {
    margin-left: 2rem;
    text-align: left;

    @include mobile {
      margin-top: 4rem;
      margin-left: 0;
    }
  }

  &__text {
    @include text-white;

    margin-top: 1rem;
    font-size: 2rem;
    font-weight: bold;
    letter-spacing: 0.375rem;
    appearance: none;

    @include mobile {
      margin-top: 0;
      font-size: 1.6rem;
      text-align: center;
    }
  }
}
</style>
