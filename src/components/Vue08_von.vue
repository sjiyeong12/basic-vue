<template>
  <h1>v-on</h1>
  <!-- <button v-on:click="count++">Add 1</button> -->
  <!-- <button v-on:click="doThis">Add 1</button> -->
  <button @click="count++"><span>Add 1</span></button>
  <p class="text-focus-in">위 버튼을 클릭한 횟수는 {{ count }}</p>
  <input
    type="text"
    name="txt"
    id="txt"
    @mouseout="reverse"
    @mouseenter="reverse"
    v-bind:value="msg"
  />
  <form action="http://127.0.0.1:8080" method="post">
    <input type="text" name="name" id="name" v-bind="nameStr" />
    <button @click="isName" type="submit">확인</button>
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
      if (this.nameStr === "") {
      }
    },
  },
};
</script>

<style>
.text-focus-in {
  -webkit-animation: text-focus-in 1s cubic-bezier(0.55, 0.085, 0.68, 0.53) both;
  animation: text-focus-in 1s cubic-bezier(0.55, 0.085, 0.68, 0.53) both;
}

@-webkit-keyframes text-focus-in {
  0% {
    -webkit-filter: blur(12px);
    filter: blur(12px);
    opacity: 0;
  }
  100% {
    -webkit-filter: blur(0px);
    filter: blur(0px);
    opacity: 1;
  }
}
@keyframes text-focus-in {
  0% {
    -webkit-filter: blur(12px);
    filter: blur(12px);
    opacity: 0;
  }
  100% {
    -webkit-filter: blur(0px);
    filter: blur(0px);
    opacity: 1;
  }
}
</style>