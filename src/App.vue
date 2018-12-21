<template>
  <div id="app">
    <text-all/>
    <transition name="fade">
      <hero-image/>
    </transition>
  </div>
</template>

<script>
import TextAll from "./components/TextAll.vue";
import HeroImage from "./components/HeroImage.vue";

export default {
  name: "app",
  components: {
    TextAll,
    HeroImage
  }
};
</script>

<style>
#app {
  font-family: "Open Sans", sans-serif;
  height: 100vh;
  width: 100vw;
}
</style>
