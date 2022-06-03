<template>
  <h1>v-for</h1>
  <ul>
    <li v-for="(item, idx) in list" :key="idx">{{ idx + 1 }}. {{ item }}</li>
  </ul>
  <ul v-for="(i, k) in str" :key="k">
    <li v-for="(item, idx) in num" :key="idx">
      {{ i }} * {{ idx + 1 }} = {{ i * item }};
    </li>
  </ul>
</template>

<script>
export default {
  data() {
    return {
      list: ["Busan", "Seoul", "Changwon", "Pohang", "Incheon"],
      str: ["2", "3", "4", "5", "6", "7", "8", "9"],
      num: ["1", "2", "3", "4", "5", "6", "7", "8", "9"],
    };
  },
};
</script>

<style>
/* @-webkit-keyframes vibrate-1 {
  0% {
    -webkit-transform: translate(0);
    transform: translate(0);
  }
  20% {
    -webkit-transform: translate(-2px, 2px);
    transform: translate(-2px, 2px);
  }
  40% {
    -webkit-transform: translate(-2px, -2px);
    transform: translate(-2px, -2px);
  }
  60% {
    -webkit-transform: translate(2px, 2px);
    transform: translate(2px, 2px);
  }
  80% {
    -webkit-transform: translate(2px, -2px);
    transform: translate(2px, -2px);
  }
  100% {
    -webkit-transform: translate(0);
    transform: translate(0);
  }
}
@keyframes vibrate-1 {
  0% {
    -webkit-transform: translate(0);
    transform: translate(0);
  }
  20% {
    -webkit-transform: translate(-2px, 2px);
    transform: translate(-2px, 2px);
  }
  40% {
    -webkit-transform: translate(-2px, -2px);
    transform: translate(-2px, -2px);
  }
  60% {
    -webkit-transform: translate(2px, 2px);
    transform: translate(2px, 2px);
  }
  80% {
    -webkit-transform: translate(2px, -2px);
    transform: translate(2px, -2px);
  }
  100% {
    -webkit-transform: translate(0);
    transform: translate(0);
  }
} */

h1 {
  -webkit-animation: vibrate-1 0.3s linear infinite both;
  animation: vibrate-1 0.3s linear infinite both;
}
</style>