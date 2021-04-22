<template>
  <section id="page3" class="advantage">
    <div class="advantage__header">
      <div class="container">
        <div class="advantage__inner__header">
          <p class="advantage__header__title">Биопрепарат</p>
          <p class="advantage__header__text">«ЗеМЛЯ РФ»:</p>
        </div>
      </div>
    </div>

    <div class="advantage__eco">
      <div class="advantage__inner">
        <div class="advantage__eco__item">
          <p class="advantage__eco__title">Экологически чистый продукт</p>
          <p class="advantage__eco__text">
            (торф + переработанный птичий помет)
          </p>
        </div>
      </div>
    </div>

    <div class="advantage__up">
      <div class="advantage__up__item">
        <div class="advantage__up__left">
          <p class="advantage__up__title">Увеличивает на</p>
          <p class="advantage__up__number">30-50%</p>
        </div>
        <div class="advantage__up__right">
          <p>урожайность всех видов с/х культур</p>
        </div>
      </div>
    </div>

    <div class="advantage__down">
      <div class="advantage__inner">
        <div class="advantage__down__wrapper">
          <p class="advantage__down__title">Снижает на</p>
          <p class="advantage__down__number">50-70%</p>
          <div class="advantage__down__text">
            <p>использование</p>
            <p>минеральных</p>
            <p>удобрений</p>
          </div>
        </div>
      </div>
    </div>

    <div class="advantage__ph">
      <div class="advantage__inner">
        <div class="advantage__ph__wrapper">
          <p class="advantage__ph__title">pH препарата</p>
          <p class="advantage__ph__number">7,9-8</p>
          <p class="advantage__ph__text">
            <span>Эффективен</span> в закисленных почвах
          </p>
        </div>
      </div>
    </div>

    <div class="advantage__enhances">
      <div class="advantage__inner">
        <div class="advantage__enhances__wrapper">
          <div class="advantage__enhances__title">
            <p>Повышает</p>
            качество зерна
          </div>
          <p class="advantage__enhances__text">и класс зерновых</p>
        </div>
      </div>
    </div>

    <div class="advantage__soil">
      <div class="advantage__inner">
        <div class="advantage__soil__wrapper">
          <div class="advantage__soil__title">
            <p>Восстанавливает</p>
            гумусный слой
          </div>
          <p class="advantage__soil__text">
            (в т.ч. песчаные почвы и солончаки)
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppPageTree",
};
</script>

<style scoped lang="scss">
.advantage {
  width: 100vw;
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-areas:
    "header header header  header"
    "eco up up  down"
    "ph enhances soil down";

  &__inner {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    &__header {
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      padding: 119px 0 89px 0;
    }
  }

  &__header {
    grid-area: header;
    font-weight: 700;

    &__title {
      font-size: calc(14px + 3.125vw);
      line-height: 4.6875vw;
    }

    &__text {
      font-size: calc(14px + 4.166666666666666vw);
      text-transform: uppercase;
    }
  }

  &__eco {
    grid-area: eco;
    background-image: url("../assets/page-three/leaf.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    display: flex;
    align-items: center;
    justify-content: center;

    &__item {
      padding: 88px 65px 88px 65px;
    }

    &__title {
      text-align: center;
      font-size: calc(14px + 1.5625vw);
      font-weight: 700;
      color: #fff;
      line-height: 1;
      padding-bottom: 26px;
    }

    &__text {
      font-size: calc(14px + 1.0416666666666665vw);
      font-weight: 300;
      color: #ffffff;
      text-align: center;
    }
  }

  &__up {
    grid-area: up;
    background-image: url("../assets/page-three/Layer_318.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;

    &__item {
      padding: 60px 55px 60px 74px;
      display: flex;
      align-items: center;
      justify-content: space-around;
    }

    &__left {
      flex: 0 1 330px;
    }

    &__title {
      font-size: calc(14px + 1.0416666666666665vw);
      font-weight: 700;
    }

    &__number {
      font-size: calc(14px + 2.604166666666667vw);
      color: #029352;
      font-weight: 700;
    }

    &__right {
      font-size: calc(14px + 1.0416666666666665vw);
      flex: 0 1 250px;

      p {
        max-width: 200px;
      }
    }
  }

  &__down {
    grid-area: down;
    background-image: url("../assets/page-three/Curves_3.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;

    &__wrapper {
      display: flex;
      flex-direction: column;
      align-items: center;
      padding: 95px 40px 0;
    }

    &__title {
      color: #ffffff;
      font-size: calc(14px + 1.8229166666666667vw);
      font-weight: 600;
    }

    &__number {
      font-size: calc(14px + 2.604166666666667vw);
      color: #1bce7e;
      font-weight: 600;
    }

    &__text {
      font-size: calc(14px + 1.0416666666666665vw);
      font-weight: 400;
      color: #ffffff;
      text-align: center;
      flex: 0 1 250px;
    }
  }

  &__ph {
    grid-area: ph;
    background-image: url("../assets/page-three/pH.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    &__wrapper {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 30px 30px;
    }

    &__title {
      font-size: calc(14px + 2.3958333333333335vw);
    }

    &__number {
      font-size: calc(14px + 4.6875vw);
      font-weight: 800;
      color: #029352;
    }

    &__text {
      font-size: calc(14px + 1.7708333333333333vw);
      font-weight: 300;
      text-align: center;

      span {
        display: block;
      }
    }
  }

  &__enhances {
    grid-area: enhances;
    color: #ffffff;
    background-image: url("../assets/page-three/Rectangle_2.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;

    &__wrapper {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 30px 30px;
    }

    &__title {
      font-size: calc(14px + 1.5625vw);
      font-weight: 800;

      p {
        text-align: center;
      }
    }

    &__text {
      font-weight: 300;
    }
  }

  &__soil {
    grid-area: soil;
    background-image: url("../assets/page-three/Layer_322.png");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: center;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    color: #ffffff;

    &__wrapper {
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      padding: 30px;
    }

    &__title {
      font-size: calc(14px + 1.5625vw);
      font-weight: 800;
      text-align: center;
      p {
        text-align: center;
      }
    }

    &__text {
      font-weight: 300;
    }
  }

  @media (max-width: 1024px) {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    grid-template-areas:
      "header header"
      "eco up  "
      "ph enhances"
      "soil down";
  }
  @media (max-width: 414px) {
    //width: 100vw;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-areas: "header" "eco" "up" "ph" "enhances" "soil" "down";

    &__inner {
      //display: flex;
      //flex-direction: column;
      //justify-content: center;
      //align-items: center;

      &__header {
        //display: flex;
        //flex-direction: column;
        //justify-content: flex-start;
        padding: 60px 0 89px 0;
      }
    }

    &__header {
      //grid-area: header;
      //font-weight: 700;

      &__title {
        //font-size: calc(14px + 3.125vw);
        //line-height: 4.6875vw;
      }

      &__text {
        //font-size: calc(14px + 4.166666666666666vw);
        //text-transform: uppercase;
      }
    }

    &__eco {
      //grid-area: eco;
      //background-image: url("../assets/page-three/leaf.png");
      //background-size: cover;
      //background-repeat: no-repeat;
      //background-position: center;
      //display: flex;
      //align-items: center;
      //justify-content: center;

      &__item {
        padding: 40px 50px;
      }

      &__title {
        padding-bottom: 10px;
      }

      &__text {
        display: none;
      }
    }

    &__up {
      &__item {
        padding: 20px;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
      }

      &__left {
        flex: 0 1 20px;
      }

      &__number {
        text-align: center;
      }

      &__right {
        text-align: center;
        flex: 0 1 20px;
      }
    }

    &__down {
      //grid-area: down;
      //background-image: url("../assets/page-three/Curves_3.png");
      //background-size: cover;
      //background-repeat: no-repeat;
      //background-position: center;

      &__wrapper {
        //display: flex;
        //flex-direction: column;
        //align-items: center;
        padding: 20px;
      }

      &__title {
        //color: #ffffff;
        //font-size: calc(14px + 1.8229166666666667vw);
        //font-weight: 600;
      }

      &__number {
        //font-size: calc(14px + 2.604166666666667vw);
        //color: #1bce7e;
        //font-weight: 600;
      }

      &__text {
        //font-size: calc(14px + 1.0416666666666665vw);
        //font-weight: 400;
        //color: #ffffff;
        //text-align: center;
        flex: 0 1 20px;
      }
    }

    &__ph {
      &__wrapper {
        padding: 10px;
      }
    }

    &__enhances {
      &__wrapper {
        padding: 10px;
      }
    }

    &__soil {
      &__wrapper {
        padding: 10px;
      }
    }
  }
}
</style>
