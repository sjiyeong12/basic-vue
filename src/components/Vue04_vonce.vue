<template>
  <h1 class="rotate-center">v-once</h1>
  <span v-once>다시는 변경되지 않습니다.{{ msg }} </span><br />
  <span>변경이 잘 됩니다.{{ msg }}</span
  ><br />
  <input type="text" v-model="msg" />
</template>

<script>
export default {
  data: () => ({ msg: "v-once이기 때문이죠" }),
};
</script>

<style>
/* @-webkit-keyframes rotate-center {
  0% {
    -webkit-transform: rotate(0);
    transform: rotate(0);
  }
  100% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}
@keyframes rotate-center {
  0% {
    -webkit-transform: rotate(0);
    transform: rotate(0);
  }
  100% {
    -webkit-transform: rotate(360deg);
    transform: rotate(360deg);
  }
}
.rotate-center {
  -webkit-animation: rotate-center 0.6s ease-in-out both;
  animation: rotate-center 0.6s 1s infinite alternate;
}

@-webkit-keyframes tracking-out-expand-fwd-top {
  0% {
    -webkit-transform: translateZ(0) translateY(0);
    transform: translateZ(0) translateY(0);
    opacity: 1;
  }
  60% {
    opacity: 0.8;
  }
  100% {
    letter-spacing: 1em;
    -webkit-transform: translateZ(300px) translateY(-200px);
    transform: translateZ(300px) translateY(-200px);
    opacity: 0;
  }
}
@keyframes tracking-out-expand-fwd-top {
  0% {
    -webkit-transform: translateZ(0) translateY(0);
    transform: translateZ(0) translateY(0);
    opacity: 1;
  }
  60% {
    opacity: 0.8;
  }
  100% {
    letter-spacing: 1em;
    -webkit-transform: translateZ(300px) translateY(-200px);
    transform: translateZ(300px) translateY(-200px);
    opacity: 0;
  }
}
span {
  font-size: 20px;
  font-weight: bold;
  -webkit-animation: tracking-out-expand-fwd-top 0.8s
    cubic-bezier(0.55, 0.085, 0.68, 0.53) both;
  animation: tracking-out-expand-fwd-top 0.8s infinite
    cubic-bezier(0.55, 0.085, 0.68, 0.53) both;
  animation-direction: normal;
  animation-direction: reverse;
  animation-direction: alternate;
  animation-direction: alternate-reverse;
} */
</style>