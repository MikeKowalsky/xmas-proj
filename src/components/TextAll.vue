<template>
  <v-container fluid fill-height class="text-all">
    <v-layout class="my-main" justify-center align-center column p-5 v-if="showIntro">
      <div class="hidden-xs-only">
        <p class="display-1 font-weight-black red--text text-xs-center my-3">
          I would like to wish you Merry Christmas!
        </p>
        <p class="display-1 font-weight-black red--text text-xs-center my-3">
          That's why I have a
        </p>
        <p class="display-4 font-weight-black red--text text-xs-center my-3">
          CHRISTMAS GIFT
        </p>
        <p class="display-1 font-weight-black red--text text-xs-center my-3">for you!</p>
        <p class="display-1 font-weight-black text-xs-center">Few links that you can visit during the break</p>
        <p class="display-1 font-weight-black text-xs-center">... or never :-)</p>
      </div>
      <div class="hidden-sm-and-up">
        <p class="font-weight-black red--text text-xs-center my-3">
          I would like to wish you Merry Christmas!
        </p>
        <p class="font-weight-black red--text text-xs-center my-3">
          That's why I have a
        </p>
        <p class="display-2 font-weight-black red--text text-xs-center my-3">
          CHRISTMAS GIFT
        </p>
        <p class="font-weight-black red--text text-xs-center my-3">for you!</p>
        <p class="font-weight-black text-xs-center">Few links that you can visit during the break</p>
        <p class="font-weight-black text-xs-center">... or never :-)</p>
      </div>
      <v-card-actions>
        <v-btn dark @click="changeShow()" class="my-3">Jump IN</v-btn>
      </v-card-actions>
    </v-layout>
    <v-layout class="my-main" justify-center align-center column pa-5 v-else>
      <p class="display-2 font-weight-black red--text text-xs-center my-3">The list:</p>
      <ul class="hidden-xs-only">
        <li>
          <a 
            href="https://medium.freecodecamp.org/how-to-build-a-single-page-application-using-vue-js-vuex-vuetify-and-firebase-838b40721a07" 
            target="_blank">
            <p class="display-1 text-xs-center">medium - vue app tutorial (vuex, vuetify, firebase)</p>
          </a>
        </li>
        <li>
          <a 
            href="https://www.youtube.com/watch?time_continue=2&v=KXPD11CQLGE" 
            target="_blank">
            <p class="display-1 text-xs-center">youtube - advent Calendar with HTML, CSS, JS</p>
          </a>
        </li>
        <li>
          <a 
            href="https://www.youtube.com/watch?v=VLm3Y7Odb74" 
            target="_blank">
            <p class="display-1 text-xs-center">youtube - web dev trends for 2019</p>
          </a>
        </li>
        <li>
          <a 
            href="https://syntax.fm/show/043/20-javascript-array-and-object-methods-to-make-you-a-better-developer" 
            target="_blank">
            <p class="display-1 text-xs-center">syntax - about array and object methods</p>
          </a>
        </li>
        <li>
          <a 
            href="https://syntax.fm/show/066/the-react-episode" 
            target="_blank">
            <p class="display-1 text-xs-center">syntax - about react in general, but useful for everybody</p>
          </a>
        </li>
        <li>
          <a 
            href="http://www.flexboxdefense.com/" 
            target="_blank">
            <p class="display-1 text-xs-center">just another CSS flexbox game</p>
          </a>
        </li>
      </ul>
      <ul class="hidden-sm-and-up">
        <li>
          <a 
            href="https://medium.freecodecamp.org/how-to-build-a-single-page-application-using-vue-js-vuex-vuetify-and-firebase-838b40721a07" 
            target="_blank">
            <p class="text-xs-center">medium - vue app tutorial (vuex, vuetify, firebase)</p>
          </a>
        </li>
        <li>
          <a 
            href="https://www.youtube.com/watch?time_continue=2&v=KXPD11CQLGE" 
            target="_blank">
            <p class="text-xs-center">youtube - advent Calendar with HTML, CSS, JS</p>
          </a>
        </li>
        <li>
          <a 
            href="https://www.youtube.com/watch?v=VLm3Y7Odb74" 
            target="_blank">
            <p class="text-xs-center">youtube - web dev trends for 2019</p>
          </a>
        </li>
        <li>
          <a 
            href="https://syntax.fm/show/043/20-javascript-array-and-object-methods-to-make-you-a-better-developer" 
            target="_blank">
            <p class="text-xs-center">syntax - about array and object methods</p>
          </a>
        </li>
        <li>
          <a 
            href="https://syntax.fm/show/066/the-react-episode" 
            target="_blank">
            <p class="text-xs-center">syntax - about react in general, but useful for everybody</p>
          </a>
        </li>
        <li>
          <a 
            href="http://www.flexboxdefense.com/" 
            target="_blank">
            <p class="text-xs-center">just another CSS flexbox game</p>
          </a>
        </li>
      </ul>
      <div class="end">
        <p>so basically you can read, watch, listen or play - whatever you like ...</p>
        <p>... or just get rest!</p>
        <p class="red--text">Have FUN Guys!</p>
        <p>Again - all the best!</p>
        <p class="name">Mike Kowalsky, Berlin, Dec 2018</p>
      </div>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  name: "TextAll",
  data() {
    return {
      showIntro: true
    };
  },
  methods: {
    changeShow() {
      this.showIntro = false;
    }
  },
  computed: {
    getWindowSize() {
      console.log(window.width);
      return window.width;
    }
  }
};
</script>

<style scoped>
.my-main {
  padding: 10px !important;
}
.text-all {
  width: 100%;
  height: 100%;
  overflow: scroll;
}
a {
  color: inherit;
  text-decoration: none;
}
ul {
  list-style-type: none;
  display: flex;
  flex-direction: column;
  align-items: center;
}
.liText {
  font-size: 20px;
  font-weight: bold;
}
.liTextMobile {
  font-size: 15px !important;
}
.end {
  margin-top: 50px;
  display: flex;
  flex-direction: column;
  align-items: center;
  font-size: 20px;
  font-weight: bold;
}
.name {
  font-size: 10px;
}
</style>
