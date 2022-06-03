<template>
  <h1>form element checkbox</h1>
  <form action="">
    <input placeholder="edit me" v-model="message" />
    <p>Message is {{ message }}</p>
    <label for="checkbox">체크 유무: {{ state }}</label>
    <input
      type="checkbox"
      id="checkbox"
      v-model="checked"
      v-on:change="checkIt"
    /><br />
    <label for="checkbox">바나나:</label>
    <input
      type="checkbox"
      id="banana"
      v-model="selFruit"
      value="banana"
    /><br />
    <label for="checkbox">사과:</label>
    <input
      type="checkbox"
      id="apple"
      v-model="selFruit"
      value="apple"
      name="fruits"
    /><br />
    <label for="checkbox">파인애플:</label>
    <input
      type="checkbox"
      id="pine-apple"
      v-model="selFruit"
      value="pine-apple"
    /><br />
    <span>Multiline message :</span>
    <p style="white-space: pre-line">{{ multiline }}</p>
    <textarea v-model="multiline" cols="30" rows="10"></textarea>
    <!-- <textareacols="30" rows="10"> {{ multiline }} </textarea> vue3.x에서는 적용안됨 -->
  </form>
</template>

<script>
export default {
  data() {
    return {
      message: "누구인가?",
      multiline: "입력양식태그는 v-model을 사용 \n\n",
      checked: true,
      state: "동의함",
      selFruit: ["pine-apple", "banana"],
    };
  },
  methods: {
    checkIt() {
      this.state = this.checked ? "동의함" : "동의 안함";
    },
  },
};
</script>

<style>
</style>