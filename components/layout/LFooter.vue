<template>
  <footer class="l-footer">
    <div class="l-contact">
      <div class="l-contact__bg">
        <div class="l-contact__head">
          <img
            class="l-contact__icon"
            src="@/assets/image/footer/icon_mail.svg"
            alt="手紙のアイコン"
          />
          <h2 class="l-contact__title">
            お問い合わせはこちら
          </h2>
        </div>
        <div class="c-container">
          <div class="l-contact__box">
            <p class="l-contact__text">
              Webにまつわるお悩み、<br />
              ご相談はお気軽にchatboxまで。
            </p>
            <div class="l-contact__buttons">
              <nuxt-link to="/" class="c-footerButton">
                お問い合わせフォームへ
                <img
                  class="l-contact__buttonIcon"
                  src="@/assets/image/footer/keyboard_arrow_right-24px.svg"
                  alt="右シェブロン"
                />
              </nuxt-link>
              <div class="l-contact__callInfo">
                <p class="l-contact__callText">
                  電話でのお問い合わせ<br />
                  <span class="l-contact__callNumber">050-3555-1212</span>
                </p>
              </div>
            </div>
            <hr class="l-contact__divider--white" />
            <div class="l-contact__logos">
              <img
                src="@/assets/image/footer/img_chatbox_logo@2x.png"
                alt="chatbox.inc webの「これから」を語り合う"
              />
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="l-footer__container">
      <ul class="l-footer__list">
        <li class="l-footer__listItem">
          <nuxt-link to="/" class="l-footer__listLink">
            chatboxについて
          </nuxt-link>
        </li>
        <li class="l-footer__listItem">
          <nuxt-link to="/" class="l-footer__listLink">
            サービス
          </nuxt-link>
        </li>
        <li class="l-footer__listItem">
          <nuxt-link to="/" class="l-footer__listLink">
            メンバー
          </nuxt-link>
        </li>
        <li class="l-footer__listItem">
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

  &__head {
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 2.2rem 0;
    text-align: center;
    background-color: #fff;

    @include mobile {
      padding: 1.7rem 0;
    }
  }

  &__text {
    @include text-white;

    font-size: 3rem;
    font-weight: bold;

    @include mobile {
      font-size: 1.7rem;
    }
  }

  &__icon {
    margin-right: 1rem;
  }

  &__box {
    text-align: center;
    background-color: #c3504f;
  }

  &__buttonIcon {
    position: relative;
    top: 1.2rem;

    @include mobile {
      top: 0.8rem;
      width: 2.8rem;
    }
  }

  &__callInfo {
    margin-left: 9rem;
    text-align: left;

    @include mobile {
      margin-top: 5rem;
      margin-left: 0;
    }
  }

  &__logos {
    margin-top: 5.5rem;
  }

  &__callText {
    @include text-white;

    font-size: 2rem;
    font-weight: bold;
    letter-spacing: 0.375rem;

    @include mobile {
      font-size: 1.6rem;
      text-align: center;
    }
  }
}

.l-footer {
  background-color: #fffcfc;

  &__buttons {
    display: flex;
    align-items: center;
    margin-top: 6.6rem;

    @include mobile {
      flex-direction: column;
      margin-top: 6rem;
    }
  }

  &__callNumber {
    margin-top: 2rem;
    font-size: 3.2rem;
    font-weight: bold;

    @include mobile {
      font-size: 2.5rem;
    }
  }

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

  &__listLink {
    @include text-accent;
  }

  &__divider {
    margin: 2.6rem 0 0 0;
    border-color: #c3504f80;
  }

  &__divider--white {
    margin-top: 12.7rem;
    border-color: white;

    @include mobile {
      margin-top: 5rem;
    }
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
</style>
