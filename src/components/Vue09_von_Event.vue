<template>
  <h1>v-on keyEvent</h1>
  <form action="http://127.0.0.1:8080" method="post">
    <div class="container">
      <button
        class="btn btn-3"
        type="submit"
        @click="warning('Warning!!', $event)"
      >
        warning
      </button>
    </div>
  </form>
</template>

<script>
export default {
  methods: {
    warning(msg, e) {
      // e가 존재한다 => $event 를 통해서 native Event에 접근 가능
      if (e) e.preventDefault();
      alert(e);
      alert(msg);
    },
  },
};
</script>

<style>
body {
  font-family: "Montserrat", sans-serif;
  margin: 0;
}

h1 {
  color: #41b783;
  text-shadow: #35485e;
}

.container {
  justify-content: center;
  align-items: center;
  align-content: center;
  flex-wrap: wrap;
  width: 80vw;
  margin: 0 auto;
  min-height: 100vh;
}
.btn {
  flex: 1 1 auto;
  margin: 10px;
  padding: 30px;
  text-align: center;
  text-transform: uppercase;
  transition: 0.5s;
  background-size: 200% auto;
  color: white;
  /* text-shadow: 0px 0px 10px rgba(0,0,0,0.2);*/
  box-shadow: 0 0 20px #eee;
  border-radius: 10px;
}

.btn:hover {
  background-position: right center; /* change the direction of the change here */
}
.btn-3 {
  background-image: linear-gradient(
    to right,
    #84fab0 0%,
    #8fd3f4 51%,
    #84fab0 100%
  );
}
</style>