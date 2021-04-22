<template>
  <section id="page4" class="structure">
    <div class="structure__container">
      <div class="structure__inner__header">
        <div class="structure__header">
          <p class="structure__header__title">«Земля РФ»</p>
          <p class="structure__header__text">Состав препарата:</p>
        </div>
        <div class="structure__useful">
          <img
            src="../assets/page-four/bacteria.png"
            alt="bacteria"
            class="structure__img__bacteria"
          />
          <p class="structure__useful__title">
            Полезные почвенные и флавобактерии
          </p>
          <ul class="structure__useful__inner">
            <li class="structure__useful__list structure__list">
              Антагонисты патогенной флоры
            </li>
          </ul>
        </div>
      </div>

      <div class="structure__wrapper">
        <div class="structure__inner__left">
          <div class="structure__humates">
            <img
              src="../assets/page-four/molecule.png"
              alt="molecule"
              class="structure__img__molecule"
            />
            <p class="structure__humates__title">Гуматы и фульваты</p>
            <ul class="structure__humates__item">
              <li class="structure__humates__list structure__list">
                Комкуют и структурируют почву
              </li>
              <li class="structure__humates__list structure__list">
                Обеспечивают доставку питательных веществ к корням растений
              </li>
            </ul>
          </div>
          <div class="structure__water">
            <img
              src="../assets/page-four/water.png"
              alt="water"
              class="structure__img__water"
            />
            <p class="structure__water__title">Вихревая вода</p>
            <ul class="structure__water__item">
              <li class="structure__water__list structure__list">
                Повышает иммунитет растений
              </li>
              <li class="structure__water__list structure__list">
                Обеспечивает жизнедеятельность полезных почвенных бактерий
              </li>
            </ul>
          </div>
        </div>
        <div class="structure__inner__right">
          <div class="structure__peat">
            <img
              src="../assets/page-four/peat.png"
              alt="peat"
              class="structure__img__peat"
            />
            <p class="structure__peat__title">Торф</p>
            <ul class="structure__peat__item">
              <li class="structure__peat__list structure__list">
                Удерживает влагу
              </li>
              <li class="structure__peat__list structure__list">
                Задерживает питательные вещества
              </li>
              <li class="structure__peat__list structure__list">
                Является питанием для растений
              </li>
            </ul>
          </div>
          <div class="structure__mineral">
            <img
              src="../assets/page-four/corn.png"
              alt="corn"
              class="structure__img__corn"
            />

            <p class="structure__mineral__title">
              Минеральные удобрения и микроэлементы
            </p>
            <ul class="structure__mineral__item">
              <li
                v-for="item in mineral"
                :key="item"
                class="structure__mineral__list"
              >
                {{ item }}
              </li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppPageFour",
  data() {
    return {
      mineral: [
        "P",
        "K",
        "Na",
        "S",
        "Mg",
        "Fe",
        "Cu",
        "Mn",
        "B",
        "Zn",
        "Ma",
        "Co",
        "Si",
      ],
    };
  },
};
</script>

<style scoped lang="scss">
@mixin title {
  font-size: calc(14px + 1vw);
  font-weight: 800;
  line-height: calc(14px + 1vw);
}

@mixin img-circle {
  width: 8%;
  max-width: 150px;
  height: auto;
  position: absolute;
}

@mixin list {
  padding: 0 0 0 20px;
  //line-height: 50px;
  font-weight: 400;
  &:before {
    content: ".";
    font-size: 40px;
    color: #029352;
    border-radius: 50%;
    position: relative;
    left: -10px;
    bottom: 2px;
  }
}

.structure {
  position: relative;
  background-image: url("../assets/page-four/bg2.png");
  background-repeat: no-repeat;
  background-size: cover;
  background-position: center;
  z-index: -1000;

  &__list {
    @include list;
  }

  &__container {
    width: 95%;
    margin: 0 auto;
  }

  &__img {
    margin: 0 auto;
    width: 100%;

    &__water {
      @include img-circle;
      bottom: 22%;
      left: 33%;
      z-index: -1;
    }

    &__molecule {
      @include img-circle;
      bottom: 48%;
      left: 33%;
      z-index: -1;
    }

    &__bacteria {
      @include img-circle;
      bottom: 60%;
      left: 47%;
      z-index: -1;
    }

    &__peat {
      @include img-circle;
      bottom: 48%;
      right: 33%;
      z-index: -1;
    }

    &__corn {
      @include img-circle;
      bottom: 22%;
      right: 35%;
      z-index: -1;
    }
  }

  &__wrapper {
    display: flex;
    justify-content: space-between;
    margin: 0 -10vw;
  }

  &__header {
    &__title {
      font-size: calc(14px + 2.5vw);
    }

    &__text {
      font-size: calc(14px + 3vw);
      font-weight: 400;
      line-height: 7vw;
      text-transform: uppercase;
    }
  }

  &__useful {
    margin-top: 50px;
    max-width: 417px;

    &__title {
      @include title;
    }
  }

  &__humates {
    &__title {
      @include title;
    }

    &__list {
      max-width: 250px;
    }
  }

  &__water {
    &__title {
      @include title;
    }

    &__list {
      max-width: 329px;
    }
  }

  &__peat {
    &__title {
      @include title;
    }

    &__list {
      max-width: 299px;
    }
  }

  &__mineral {
    &__title {
      @include title;
      max-width: 310px;
      margin-bottom: 16px;
    }

    &__item {
      display: inline-grid;
      max-width: 410px;
      grid-template-columns: repeat(7, 1fr);
      grid-gap: 1vw;
    }

    &__list {
      display: flex;
      align-items: center;
      justify-content: center;
      flex: 0 1 32px;
      color: #82898b;
      font-weight: 600;
      padding: 5px;
      height: auto;
      border-radius: 50%;
      box-shadow: -5px -5px 5px -5px rgba(34, 60, 80, 0.6) inset;
      background-image: linear-gradient(
        to bottom left,
        rgb(255, 255, 255),
        rgb(247, 247, 247),
        rgb(240, 240, 240),
        rgb(232, 232, 232),
        rgb(224, 224, 224),
        rgb(217, 217, 217),
        rgb(209, 209, 209),
        rgb(202, 202, 202),
        rgb(194, 194, 194),
        rgb(186, 186, 186),
        rgb(179, 179, 179),
        rgb(171, 171, 171)
      );
    }
  }

  &__inner {
    &__header {
      margin: 118px 0 75px;
      display: grid;
      grid-template-columns: 1fr 0.7fr;
    }

    &__left {
      display: grid;
      grid-gap: 3vw;
      grid-auto-rows: 1fr 1fr;
      padding: 0 10vw;
    }

    &__right {
      display: grid;
      grid-gap: 3vw;
      grid-auto-rows: 1fr 1fr;
      padding: 0 10vw;
    }
  }

  @media (max-width: 768px) {
    position: relative;
    background-image: url("../assets/page-four/bg-mobile.png");
    background-repeat: no-repeat;
    background-size: cover;
    background-position: center;
    z-index: -1000;

    &__list {
      @include list;
    }

    &__container {
      width: 95%;
      margin: 0 auto;
    }

    &__img {
      margin: 0 auto;
      width: 100%;

      &__water {
        @include img-circle;
        bottom: 22%;
        left: 33%;
        z-index: -1;
      }

      &__molecule {
        @include img-circle;
        bottom: 48%;
        left: 33%;
        z-index: -1;
      }

      &__bacteria {
        @include img-circle;
        bottom: 60%;
        left: 47%;
        z-index: -1;
      }

      &__peat {
        @include img-circle;
        bottom: 48%;
        right: 33%;
        z-index: -1;
      }

      &__corn {
        @include img-circle;
        bottom: 22%;
        right: 35%;
        z-index: -1;
      }
    }

    &__wrapper {
      display: flex;
      justify-content: space-between;
      margin: 0 -10vw;
    }

    &__header {
      &__title {
        //font-size: calc(14px + 2.5vw);
      }

      &__text {
        //font-size: calc(14px + 3vw);
        //font-weight: 400;
        //line-height: 7vw;
        //text-transform: uppercase;
      }
    }

    &__useful {
      margin-top: 50px;
      max-width: 417px;
      position: relative;

      &__title {
        @include title;
      }
    }

    &__humates {
      //grid-area: humates;
      position: relative;

      &__title {
        @include title;
      }

      &__list {
        max-width: 250px;
      }
    }

    &__water {
      //grid-area: water;
      position: relative;

      &__title {
        @include title;
      }

      &__list {
        max-width: 329px;
      }
    }

    &__peat {
      //grid-area: peat;

      &__title {
        @include title;
      }

      &__list {
        max-width: 299px;
      }
    }

    &__mineral {
      &__title {
        @include title;
        max-width: 310px;
        margin-bottom: 16px;
      }

      &__item {
        display: inline-grid;
        max-width: 410px;
        grid-template-columns: repeat(7, 1fr);
        grid-gap: 1vw;
      }

      &__list {
        display: flex;
        align-items: center;
        justify-content: center;
        flex: 0 1 32px;
        color: #82898b;
        font-weight: 600;
        padding: 5px;
        //width: 32px;
        height: auto;
        border-radius: 50%;
        box-shadow: -5px -5px 5px -5px rgba(34, 60, 80, 0.6) inset;
        background-image: linear-gradient(
          to bottom left,
          rgb(255, 255, 255),
          rgb(247, 247, 247),
          rgb(240, 240, 240),
          rgb(232, 232, 232),
          rgb(224, 224, 224),
          rgb(217, 217, 217),
          rgb(209, 209, 209),
          rgb(202, 202, 202),
          rgb(194, 194, 194),
          rgb(186, 186, 186),
          rgb(179, 179, 179),
          rgb(171, 171, 171)
        );
      }
    }

    &__inner {
      &__header {
        margin: 118px 0 75px;
        display: grid;
        grid-template-columns: 1fr 0.7fr;
      }

      &__left {
        display: grid;
        grid-gap: 3vw;
        grid-auto-rows: 1fr 1fr;
        padding: 0 10vw;
      }

      &__right {
        display: grid;
        grid-gap: 3vw;
        grid-auto-rows: 1fr 1fr;
        padding: 0 10vw;
      }
    }
  }
}
</style>
