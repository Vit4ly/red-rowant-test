<template>
  <section id="page1" class="home">
    <div class="container">
      <div class="home__inner">
        <div class="home__inner__label">
          <img
            class="home__inner__label__img"
            src="../assets/page-one/2-layers.png"
            alt="img"
          />
        </div>
        <p class="home__title home__title__green">Повысьте</p>
        <p class="home__title home__title__center">урожайность</p>
        <p class="home__title home__title__bottom">при тех же затратах</p>
      </div>
      <ul class="home__list">
        <li class="home__list__item">
          <p class="home__list__text__top">Повышает</p>
          <p class="home__list__text__bottom">урожайность</p>
        </li>
        <li class="home__list__item">
          <p class="home__list__text__top">Экологически</p>
          <p class="home__list__text__bottom">чистый продукт</p>
        </li>
        <li class="home__list__item">
          <p class="home__list__text__top">Улучшает</p>
          <p class="home__list__text__bottom">качество плодов</p>
        </li>
      </ul>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppPageOne",
};
</script>

<style scoped lang="scss">
.home {
  //width: 100vw;
  background-image: url("../assets/page-one/bg1.png");
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
  position: relative;
  //height: 100vh;

  &__inner {
    position: relative;
    display: flex;
    flex-direction: column;
    align-items: center;

    &__label {
      margin: 0 auto;

      &__img {
        position: absolute;
        top: 62%;
        right: -9%;
        bottom: 0;
        width: 45%;
        height: auto;
      }
    }
  }

  &__title {
    font-weight: 700;
    text-transform: uppercase;

    &__green {
      font-size: 9vw;
      padding-top: 100px;
      line-height: 9vw;
      //letter-spacing: 0;
      color: #029352;
    }

    &__center {
      font-size: 10vw;
      line-height: 10vw;
      padding-top: 5px;
    }

    &__bottom {
      font-size: 5vw;
      font-weight: 600;
      line-height: 7vw;
      padding-top: 30px;
      text-transform: lowercase;
    }
  }

  &__list {
    display: grid;
    grid-template-columns: repeat(3, 1.2fr);
    grid-gap: 78px;
    align-items: flex-end;
    padding-bottom: 460px;

    &__item {
      line-height: 2.5vw;

      &:before {
        content: ".";
        font-size: 46px;
        color: #029352;
        position: relative;
        right: 40px;
        top: 3vw;
      }
    }

    &__text {
      &__top {
        font-size: calc(14px + 1vw);
        font-weight: 700;
      }

      &__bottom {
        font-size: calc(14px + 1vw);
        font-weight: 500;
      }
    }
  }
  @media (max-width: 1024px) {
    &__list {
      grid-gap: 2vw;
    }
  }
  @media (max-width: 768px) {
    background-image: url("../assets/page-one/bg/bg-mobile.png");
    &__inner {
      &__label {
        &__img {
          position: absolute;
          top: 65%;
          right: -7%;
        }
      }
    }

    &__list {
      display: grid;
      grid-template-columns: 1fr;
      grid-gap: 3vw;
      padding-bottom: 15vw;

      &__item {
        text-align: center;
        line-height: 8vw;

        &:before {
          font-size: 80px;
          right: 200px;
          top: 90px;
        }
      }

      &__text {
        &__bottom {
          font-weight: 700;
        }
      }
    }
  }

  @media (max-width: 414px) {
    //height: 100vh;
    &__inner {
      &__label {
        &__img {
          position: absolute;
          top: 67%;
          right: -7%;
        }
      }
    }

    &__list {
      display: grid;
      grid-template-columns: 1fr;
      grid-gap: 5vw;
      padding-bottom: 5vw;

      &__item {
        text-align: center;
        line-height: 8vw;

        &:before {
          font-size: 70px;
          right: 130px;
          top: 10vw;
        }
      }

      &__text {
        &__bottom {
          font-weight: 700;
        }
      }
    }
  }
}
</style>
