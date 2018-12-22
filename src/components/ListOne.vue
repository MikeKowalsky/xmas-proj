<template>
  <li>
    <a 
      href="url" 
      target="_blank">
      <p class="text-xs-center">{{txt}}</p>
    </a>
    <!-- <a 
      href="https://medium.freecodecamp.org/how-to-build-a-single-page-application-using-vue-js-vuex-vuetify-and-firebase-838b40721a07" 
      target="_blank">
      <p class="text-xs-center">medium - vue app tutorial (vuex, vuetify, firebase)</p>
    </a> -->
  </li>
</template>

<script>
export default {
  name: "ListOne",
  props: ["url", "txt"]
};
</script>

