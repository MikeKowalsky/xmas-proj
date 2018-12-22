<template>
  <v-container fluid fill-height class="text-all" :class="{'size': isWindowLarge}">
    <v-layout class="my-main" justify-center align-center column p-5 v-if="showIntro">

      <text-one text="I would like to wish you Merry Christmas!" :isRed="true"/>
      <text-one text="That's why I have a" :isRed="true"/>
      <text-one 
        text="CHRISTMAS GIFT" 
        :isRed="true" 
        :isD2="!isWindowLarge" 
        :isD4="isWindowLarge"/>    
      <text-one text="for you!" :isRed="true"/>
      <text-one text="Few links that you can visit during the break"/>
      <text-one text="... or never :-)"/>

      <v-card-actions>
        <v-btn dark @click="changeShow()" class="my-3">Jump IN</v-btn>
      </v-card-actions>
    </v-layout>

    <v-layout class="my-main" justify-center align-center column pa-5 v-else>
      <text-one text="The list:" :isRed="true" :isD2="true"/>

      <ul>
        <list-one
          url="https://medium.freecodecamp.org/how-to-build-a-single-page-application-using-vue-js-vuex-vuetify-and-firebase-838b40721a07"
          txt="medium - vue app tutorial (vuex, vuetify, firebase)">
        </list-one>
        <list-one
          url="https://www.youtube.com/watch?time_continue=2&v=KXPD11CQLGE" 
          txt="youtube - advent Calendar with HTML, CSS, JS">
        </list-one>
        <list-one
          url="https://www.youtube.com/watch?v=VLm3Y7Odb74" 
          txt="youtube - web dev trends for 2019">
        </list-one>
        <list-one
          url="https://syntax.fm/show/043/20-javascript-array-and-object-methods-to-make-you-a-better-developer" 
          txt="syntax - about array and object methods">
        </list-one>
        <list-one
          url="https://syntax.fm/show/066/the-react-episode" 
          txt="syntax - about react in general, but useful for everybody">
        </list-one>
        <list-one
          url="http://www.flexboxdefense.com/" 
          txt="just another CSS flexbox game">
        </list-one>
      </ul>
      <div class="end">
        <p class="text-xs-center">so basically you can read, watch, listen or play - whatever you like ...</p>
        <p>... or just get rest!</p>
        <p class="red--text">Have FUN Guys!</p>
        <p>Again - all the best!</p>
        <p class="name">Mike Kowalsky, Berlin, Dec 2018</p>
      </div>
    </v-layout>
  </v-container>
</template>

<script>
import TextOne from "@/components/TextOne.vue";
import ListOne from "@/components/ListOne.vue";

export default {
  name: "TextAll",
  components: {
    TextOne,
    ListOne
  },
  data() {
    return {
      showIntro: true,
      windowWidth: window.innerWidth
    };
  },
  methods: {
    changeShow() {
      this.showIntro = false;
    },
    handleWindowResize() {
      this.windowWidth = window.innerWidth;
    }
  },
  computed: {
    isWindowLarge() {
      return this.windowWidth > 650;
    }
  },
  beforeDestroy() {
    window.removeEventListener("resize", this.handleWindowResize);
  },
  mounted() {
    window.addEventListener("resize", this.handleWindowResize);
  }
};
</script>

<style>
.my-main {
  padding: 10px !important;
}
.text-all {
  width: 100%;
  height: 100%;
  overflow: scroll;
}
.size p {
  font-size: 22px;
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
  font-weight: bold;
}
.name {
  font-size: 10px !important;
}
</style>
