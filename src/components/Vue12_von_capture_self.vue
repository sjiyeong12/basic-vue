<template>
  <h1>v-on capture, self</h1>
  <div v-on:click.capture="doTop" id="top">
    <div v-on:click.self="doMiddle" id="middle">
      <button type="button" v-on:click="doBottom">Bubble</button>
    </div>
  </div>
  <span
    >stop은 자신만 이벤트를 실행할 경우<br />
    capture는 자신보다 자신의 parent의 이벤트를 먼저 실행, 이럴 경우 parent에
    capture를 붙임<br />
    상위 노드에 capture가 연속적ㅇ리 경우 마지막으로 적용된 노드가 먼저 시작.<br />
    self는 자신이 직접 발생한 이벤트만 처리.
  </span>
</template>

<script>
export default {
  methods: {
    doTop() {
      console.log("top 이벤트 발생");
    },
    doMiddle() {
      console.log("Middle 이벤트 발생");
    },
    doBottom() {
      console.log("Bottom 이벤트 발생");
    },
  },
};
</script>

<style>
/* body {
  background: rgb(51, 44, 61);
} */
#top {
  width: 200px;
  height: 200px;
  background: #41b783;
}
#middle {
  width: 100px;
  height: 100px;
  background: #35485e;
}
h1 {
  color: #41b783;
}
/* span {
  color: whitesmoke;
} */
</style>