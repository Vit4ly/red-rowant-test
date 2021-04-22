<template>
  <section id="page2" class="problem">
    <div class="container">
      <div class="problem__title">
        <p>Проблемы</p>
        <p>сельского хозяйства</p>
      </div>
      <div class="problem__inner">
        <div class="problem__item">
          <div class="problem__card">
            <p class="problem__card__title">Проблема №1</p>
            <p class="problem__card__text">Истощение и закисление почв</p>
          </div>

          <div class="problem__card">
            <p class="problem__card__title">Проблема №2</p>
            <p class="problem__card__text">
              Короткий период для выращивания и сбора урожая
            </p>
          </div>

          <div class="problem__card">
            <p class="problem__card__title">Проблема №3</p>
            <p class="problem__card__text">
              Недостаток пригодных для обработки земель
            </p>
          </div>
        </div>
      </div>
      <div class="problem__image-block">
        <div class="problem__image-block__text">
          <p>«Земля РФ»</p>
          <p>поможет повысить урожайность и восстановить почву</p>
        </div>
        <img
          src="../assets/page-two/Layer_311.png"
          alt=""
          class="problem__image-block__image"
        />
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "AppPageTwo",
};
</script>

<style scoped lang="scss">
.problem {
  padding-top: 172px;

  &__title {
    font-size: calc(14px + 5vw);
    font-weight: 400;
    text-align: center;
    text-transform: uppercase;
  }

  &__inner {
    display: flex;
    align-items: center;
    justify-content: center;
    padding-top: 111px;
  }

  &__item {
    display: inline-grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 22px;
    padding-bottom: 20px;
  }

  &__card {
    display: flex;
    align-items: center;
    flex-direction: column;
    position: relative;
    box-shadow: 0 5px 10px 2px rgba(34, 60, 80, 0.2);
    border-radius: 10px;
    padding: 0 20px 97px;
    max-width: 287px;

    &__title {
      display: flex;
      align-items: center;
      justify-content: center;
      position: relative;
      top: -25px;
      max-width: 210px;
      padding: 12px 18px;
      border-radius: 10px;
      text-transform: uppercase;
      font-size: 20px;
      font-weight: 600;
      color: #fff;
      background-color: #d80027;
    }

    &__text {
      font-size: 32px;
      font-weight: 500;

      line-height: 36px;
    }
  }

  &__image-block {
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    margin: 0 auto;

    &__image {
      z-index: -100;
    }

    &__text {
      max-width: 532px;
      position: absolute;
      top: 10%;
      left: 20%;
      font-size: 32px;
      font-weight: 400;
      color: #ffffff;
      //padding: 0 50px 0 0;
    }
  }
  @media (max-width: 1024px) {
  }
  @media (max-width: 768px) {
  }
  @media (max-width: 414px) {
    padding-top: 10vw;
    &__item {
      grid-template-columns: 1fr;
    }

    &__card {
      &__title {
        font-size: calc(14px + 1.7vw);
      }

      &__text {
        font-size: calc(14px + 1.5vw);
        font-weight: 700;
        line-height: 6vw;
      }
    }

    &__image-block {
      &__text {
        top: 10%;
        left: 10%;
        font-size: calc(14px + 1vw);
      }
    }
  }
  @media (max-width: 375px) {
    padding-top: 10vw;
    &__item {
      grid-template-columns: 1fr;
    }

    &__card {
      &__title {
        font-size: calc(14px + 1.7vw);
      }

      &__text {
        font-size: calc(14px + 1.5vw);
        font-weight: 700;
        line-height: 6vw;
      }
    }

    &__image-block {
      &__text {
        top: 10%;
        left: 10%;
        font-size: calc(14px + 1vw);
      }
    }
  }
}
</style>
