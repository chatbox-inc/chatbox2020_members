<template>
  <section class="c-skill">
    <div class="c-container">
      <div class="c-head">
        <h2 class="c-head__title">
          <span class="c-head__color">ス</span>キルアップ施策
        </h2>
      </div>
      <div class="c-description">
        <p class="c-description__text">
          chatboxでは自分で決めた目標に対して、積極的にスキルアップを目指していく人を応援しています。「自ら学び、教え合う」ことがごく自然に受け入れられている社内なので、得意分野をどんどん伸ばし、苦手分野は得意な人に教えてもらいながら補強していくことが可能です。
        </p>
      </div>
      <div class="c-box">
        <div class="c-box__item">
          <img
            src="@/assets/image/skill/img_skill@2x.png"
            class="c-box__img"
            alt="社内風景画像"
          />
          <div class="c-box__description">
            <h3 class="c-box__title">
              コミニケーション能力の育成
            </h3>
            <p class="c-box__text">
              制作現場における円滑なコミュニケーションは、良い仕事を生み出すだけでなく、
              携わるスタッフ全員の働きやすさにも良い効果をもたらします。
              chatboxでは、プロジェクトごとに異なる組織体制を組む柔軟なチーム制作を行っており、
              タスクの依頼方法や報告の仕方などにも日々工夫を重ねています。
              学生スタッフも含めたそれぞれのスタッフが、互いに円滑な相談・報告を行い、
              より良い環境づくりに社内全体で取り組んでいます。
            </p>
          </div>
        </div>
        <div class="c-box__item">
          <img
            src="@/assets/image/skill/img_skill@2x.png"
            class="c-box__img"
            alt="社内風景画像"
          />
          <div class="c-box__description">
            <h3 class="c-box__title">
              自己管理能力の向上
            </h3>
            <p class="c-box__text">
              chatboxでは各々が無理せず、適切な休暇を取れるよう、
              Backlogなどのプロジェクト管理ツールを使ったタスク管理が実施されています。
              毎週の全体ミーティングでタスクを可視化し、全体報告を行うといった習慣を徹底することで、
              繁忙時に応援を依頼したり、体調に合わせて休暇を取得する、といった事が可能になっています。
              柔軟な出勤時間やリモートワークの利用などで、個々が最大限のパフォーマンスを発揮できる環境で、
              それぞれがライフスタイルのニーズに合わせて仕事を設計することが出来るようになっています。
            </p>
          </div>
        </div>
        <div class="c-box__item">
          <img
            src="@/assets/image/skill/img_skill@2x.png"
            class="c-box__img"
            alt="社内風景画像"
          />
          <div class="c-box__description">
            <h3 class="c-box__title">
              スクール勉強会の開催
            </h3>
            <p class="c-box__text">
              chatbox 主催の Lec Café
              では「現場で使える最新技術」をテーマに毎月様々なセミナーを開催しています。
              プロ向けの高品質なセミナー講座に、アルバイトを含めた各スタッフは無償で参加する事ができます。
              また各種技術系コミュニティイベントの主催・参加も積極的に行われており、社外の様々なクリエイターとの交流の機会が用意されています。
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
.c-skill {
  padding-bottom: 24.4rem;

  @include mobile {
    padding-bottom: 11.2rem;
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

.c-box {
  margin-top: 4.4rem;

  @include mobile {
    margin-top: 4rem;
  }

  &__imf {
    object-fit: cover;
  }

  &__description {
    padding: 3rem 4rem;
    background-color: #faf7f7;
    border-right: 0.2rem solid #c3504f;

    @include mobile {
      padding: 2rem 3.5rem;
    }
  }

  &__item {
    display: flex;

    &:nth-child(2) {
      .c-box__description {
        border-right: 0;
        border-left: 0.2rem solid #c3504f;
      }
    }

    &:nth-child(even) {
      flex-direction: row-reverse;
    }

    &:nth-child(n + 2) {
      margin-top: 3rem;
    }

    @include mobile {
      flex-direction: column;

      &:nth-child(even) {
        flex-direction: column;

        .c-skill__boxDescription {
          border-right: 0;
          border-left: 0.2rem solid #c3504f;
        }
      }
    }
  }

  &__title {
    font-size: 2rem;
    font-weight: bold;

    @include mobile {
      font-size: 1.8rem;
    }
  }

  &__text {
    margin-top: 2rem;
    line-height: 3rem;

    @include mobile {
      font-size: 1.4rem;
    }
  }
}
</style>
