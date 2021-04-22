<template>
  <the-nav-bar></the-nav-bar>
  <div id="nav">
    <app-page-one></app-page-one>
    <app-page-two></app-page-two>
    <app-page-three></app-page-three>
    <app-page-four></app-page-four>
  </div>
  <!--  <router-view/>-->
</template>
<script>
import TheNavBar from "@/components/TheNavBar";
import AppPageOne from "@/components/AppPageOne";
import AppPageTwo from "@/components/AppPageTwo";
import AppPageThree from "@/components/AppPageThree";
import AppPageFour from "@/components/AppPageFour";

export default {
  components: {
    TheNavBar,
    AppPageOne,
    AppPageTwo,
    AppPageThree,
    AppPageFour,
  },
};
</script>
<style lang="scss">
#nav {
  //padding-top: 20px;
  overflow: hidden;
}
</style>
