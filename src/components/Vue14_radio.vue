<template>
  radio에서 value 값은 v-model로 선택되었을 때 활용됨. 반드시 필요!<br />
  <label for="one">One</label>
  <input
    type="radio"
    name="radio"
    id="one"
    value="one"
    v-model="picked"
  /><br />
  <label for="two">Two</label>
  <input
    type="radio"
    name="radio"
    id="two"
    value="two"
    v-model="picked"
  /><br />
  <span>Picked: {{ picked }}</span>
</template>

<script>
export default {
  data() {
    return {
      picked: "one", //radio는 함 개만 선택되기 때문에 배열이 아니고 문자열
    };
  },
};
</script>

<style>
</style>