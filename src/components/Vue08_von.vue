<template>
  <h1>v-on</h1>
  <!-- <button v-on:click="count++">Add 1</button> -->
  <!-- <button v-on:click="doThis">Add 1</button> -->
  <button @click="count++"><span>Add 1</span></button>
  <p class="text-focus-in">위 버튼을 클릭한 횟수는 {{ count }}</p>
  <!-- <input
    type="text"
    name="txt"
    id="txt"
    @mouseout="reverse"
    @mouseenter="reverse"
    v-bind:value="msg"
  /> -->
  <input
    type="text"
    name="txt"
    id="txt"
    v-bind:value="msg"
    v-on="{ mouseout: reverse, mouseenter: reverse }"
  />

  <form action="http://127.0.0.1:8080" method="post">
    <!-- ref : 엘리먼트나 자식 컴포넌트에 대한 참조를 등록할 때 사용 -->
    <input type="text" name="name" ref="yourName" />
    <!-- prevent, stap, once는 각각 적용 가능 -->
    <button @click.prevent.once="isName" type="submit">확인</button>
  </form>
</template>

<script>
export default {
  data() {
    return { count: 0, msg: "Hello Vue3", nameStr: "" };
  },
  methods: {
    doThis() {
      this.count++;
    },
    reverse() {
      this.msg = this.msg.split("").reverse().join("");
    },
    isName() {
      const name = this.$refs.yourName;
      if (name.value == "") {
        alert("name을 확인하여 주세요");
        name.focus();
        return;
      }
    },
  },
};
</script>

<style>
</style>