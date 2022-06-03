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
</style>