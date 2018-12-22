<template>
  <p 
    class="font-weight-black text-xs-center my-3"
    :class="{'red--text': isRed, 'display-2': isD2, 'display-4': isD4}">
    {{text}}
  </p>
</template>

<script>
export default {
  name: "TextOne",
  props: ["text", "isRed", "isD2", "isD4"]
};
</script>

<style scoped>
</style>


