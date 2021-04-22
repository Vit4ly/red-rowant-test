<template>
  <nav class="navbar">
    <div class="container">
      <div class="navbar__inner">
        <div class="navbar__brand">
          <svg class="icon">
            <use xlink:href="#logo"></use>
          </svg>
          <router-link class="navbar__link" to="page1">земля рф</router-link>
        </div>
        <div class="navbar__menu">
          <transition name="fade" mode="out-in">
            <div class="navbar__burger">
              <div class="icon-inner" v-if="!show">
                <svg @click="show = !show" key="menu" class="icon-menu">
                  <use xlink:href="#menu"></use>
                </svg>
              </div>

              <svg v-else @click="show = !show" class="icon-close">
                <use xlink:href="#close"></use>
              </svg>
            </div>
          </transition>
        </div>
      </div>
      <transition name="fade">
        <ul v-if="show" class="navbar__list">
          <li v-for="item in menu" :key="item" class="navbar__list__item">
            {{ item }}
          </li>
        </ul>
      </transition>
    </div>
  </nav>

  <!-- Sprite  Close-->
  <svg width="0" height="0" class="hidden">
    <symbol xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" id="close">
      <path d="M0 0h24v24H0V0z" fill="none"></path>
      <path
        d="M19 6.41L17.59 5 12 10.59 6.41 5 5 6.41 10.59 12 5 17.59 6.41 19 12 13.41 17.59 19 19 17.59 13.41 12 19 6.41z"
      ></path>
    </symbol>
  </svg>
  <!-- Sprite Menu -->
  <svg width="0" height="0" class="hidden">
    <symbol xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" id="menu">
      <path d="M0 0h24v24H0V0z" fill="none"></path>
      <path d="M3 18h18v-2H3v2zm0-5h18v-2H3v2zm0-7v2h18V6H3z"></path>
    </symbol>
  </svg>
  <!-- Sprite Logo-->
  <svg width="0" height="0" class="hidden">
    <symbol
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      viewBox="0 0 91 91"
      id="logo"
    >
      <title>logo</title>
      <image
        xlink:href="data:image/png;base64,
          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"
        width="91"
        height="91"
      ></image>
    </symbol>
  </svg>
</template>

<script>
export default {
  name: "TheNavBar",
  data() {
    return {
      show: false,
      menu: ["page1", "page2", "page3", "page4"],
    };
  },
};
</script>

<style scoped lang="scss">
.navbar {
  background: rgb(251, 251, 251);
  background: linear-gradient(
    90deg,
    rgba(251, 251, 251, 1) 0%,
    rgba(81, 164, 140, 1) 99%,
    rgba(81, 164, 140, 1) 100%
  );
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  width: 100%;
  z-index: 1000;

  &__inner {
    display: flex;
    align-items: center;
    justify-content: space-between;
  }

  &__brand {
    display: flex;
    align-items: center;
  }

  &__link {
    text-transform: uppercase;
    text-decoration: none;
    color: #000;
  }

  &__list {
    display: flex;
    flex-direction: column;
    align-items: center;
    margin: 0;
    padding: 0;
    position: absolute;
    top: 60px;
    left: 0;
    height: 100vh;
    width: 100%;
    background: rgb(251, 251, 251);
    background: linear-gradient(
      90deg,
      rgba(251, 251, 251, 1) 0%,
      rgba(81, 164, 140, 1) 99%,
      rgba(81, 164, 140, 1) 100%
    );

    &__item {
      display: flex;
      justify-content: center;
      align-items: center;
      font-size: 1.5em;
      font-weight: 700;
      height: 2em;
      padding: 50px;
      cursor: pointer;
      text-transform: uppercase;
      //transition: all .1s ease;

      &:hover {
        width: 100%;
        background-color: rgba(0, 0, 0, 0.1);
        color: rgba(81, 164, 140, 1);
      }
    }
  }
}

.fade-enter-active,
.fade-leave-active {
  transition: opacity 0.3s;
}

.fade-enter,
.fade-leave-to {
  opacity: 0;
}

.icon {
  width: 50px;
  height: 50px;
  margin: 0.5em;
}

.icon-close {
  margin: 0.5em;
}

.icon-menu {
  margin: 0.1em 0.3em;
}

.icon-close,
.icon-menu {
  width: 50px;
  height: 40px;
  cursor: pointer;
  transition: all 0.3s;
  fill: rgba(0, 0, 0, 0.5);
}

.icon-inner {
  display: flex;
  justify-content: center;
  align-items: center;
  border: 1px solid rgba(0, 0, 0, 0.2);
  border-radius: 5px;
}
</style>
