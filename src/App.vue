<template>
  <img alt="Vue logo" src="./assets/logo.png" width="50" /><br />
  <hr />
  <h1>Vue 3 Exercise</h1>
  <div v-bind:class="classCard" v-for="(component, i) in arrList" :key="i">
    <component v-bind:is="component"></component>
  </div>
  <Footer class="classFooter" msg="Footer for Your Vue.js App" />
</template>

<script>
import Exercise01 from "./components/Vue01_data.vue";
import Exercise02 from "./components/Vue02_declaritive_rendering.vue";
import Exercise03 from "./components/Vue03_vbind.vue";
import Exercise04 from "./components/Vue04_vonce.vue";
import Exercise05 from "./components/Vue05_vshow.vue";
import Exercise06 from "./components/Vue06_vif.vue";
import Exercise07 from "./components/Vue07_vfor.vue";
import Exercise08 from "./components/Vue08_von.vue";
import Exercise09 from "./components/Vue09_von_Event.vue";
import Exercise10 from "./components/Vue10_von_keyEvent.vue";
import Exercise11 from "./components/Vue11_von_mouseEvent.vue";
import Exercise12 from "./components/Vue12_von_capture_self.vue";
import Exercise13 from "./components/Vue13_checkbox.vue";
import Exercise14 from "./components/Vue14_radio.vue";
import Exercise15 from "./components/Vue15_select.vue";
import Exercise16 from "./components/Vue16_checkbox2.vue";
import Exercise17 from "./components/Vue17_radio_binding.vue";
import Exercise18 from "./components/Vue18_select_binding.vue";
import Exercise19 from "./components/Vue19_form_element_join.vue";
import Footer from "./components/Vue_Footer.vue";
export default {
  name: "App",
  components: {
    Exercise01,
    Exercise02,
    Exercise03,
    Exercise04,
    Exercise05,
    Exercise06,
    Exercise07,
    Exercise08,
    Exercise09,
    Exercise10,
    Exercise11,
    Exercise12,
    Exercise13,
    Exercise14,
    Exercise15,
    Exercise16,
    Exercise17,
    Exercise18,
    Exercise19,

    Footer,
  },
  data() {
    return {
      arrList: [
        Exercise01,
        Exercise02,
        Exercise03,
        Exercise04,
        Exercise05,
        Exercise06,
        Exercise07,
        Exercise08,
        Exercise09,
        Exercise10,
        Exercise11,
        Exercise12,
        Exercise13,
        Exercise14,
        Exercise15,
        Exercise16,
        Exercise18,
        Exercise19,
      ],
      classCard: "card",
      classFooter: "footer",
    };
  },
};
</script>

<style>
* {
  color: white;
}
body {
  background: #5ac095;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
#app > div {
  margin-left: 10px;
  margin-right: 10px;
  background: rgb(76, 64, 76);
}
#app > div:focus,
#app > div:hover {
  box-shadow: rgba(0, 0, 0, 0.7) 0px 4px 12px;
}

#app > div > h1 {
  text-align: center;
}
.card {
  padding: 10px;
  margin-bottom: 55px;
  background-color: white;
  border: 1px solid rgba(0, 0, 0, 0.144);
  border-radius: 5px;
  box-shadow: rgba(0, 0, 0, 0.1) 0px 4px 12px;
  transition: 0.3s all ease-in-out;
  /* width: 400px; */
}
h1:focus,
h1:hover {
  -webkit-animation: jello-horizontal 0.9s both;
  animation: jello-horizontal 0.9s both;
}

.footer {
  height: 200px;
  margin: 0;
  background-color: white;
  line-height: 90px;
  padding-left: 50px;
  font-weight: bold;
  clear: both;
}

@-webkit-keyframes jello-horizontal {
  0% {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }
  30% {
    -webkit-transform: scale3d(1.25, 0.75, 1);
    transform: scale3d(1.25, 0.75, 1);
  }
  40% {
    -webkit-transform: scale3d(0.75, 1.25, 1);
    transform: scale3d(0.75, 1.25, 1);
  }
  50% {
    -webkit-transform: scale3d(1.15, 0.85, 1);
    transform: scale3d(1.15, 0.85, 1);
  }
  65% {
    -webkit-transform: scale3d(0.95, 1.05, 1);
    transform: scale3d(0.95, 1.05, 1);
  }
  75% {
    -webkit-transform: scale3d(1.05, 0.95, 1);
    transform: scale3d(1.05, 0.95, 1);
  }
  100% {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }
}
@keyframes jello-horizontal {
  0% {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }
  30% {
    -webkit-transform: scale3d(1.25, 0.75, 1);
    transform: scale3d(1.25, 0.75, 1);
  }
  40% {
    -webkit-transform: scale3d(0.75, 1.25, 1);
    transform: scale3d(0.75, 1.25, 1);
  }
  50% {
    -webkit-transform: scale3d(1.15, 0.85, 1);
    transform: scale3d(1.15, 0.85, 1);
  }
  65% {
    -webkit-transform: scale3d(0.95, 1.05, 1);
    transform: scale3d(0.95, 1.05, 1);
  }
  75% {
    -webkit-transform: scale3d(1.05, 0.95, 1);
    transform: scale3d(1.05, 0.95, 1);
  }
  100% {
    -webkit-transform: scale3d(1, 1, 1);
    transform: scale3d(1, 1, 1);
  }
}
select,
option, div>input, button {
  color: black;
}
</style>
