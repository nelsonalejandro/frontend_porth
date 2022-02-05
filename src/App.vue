<template>
  <div id="app">
    <img alt="Vue logo" src="https://porth.app/logo_white.svg" />
    <Message msg="Welcome to Your Vue.js App" />
    <!--  <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  </div>
</template>

<script>
/* import HelloWorld from './components/HelloWorld.vue' */
import Message from "./components/message.vue";

export default {
  name: "App",
  components: {
    /*  HelloWorld, */
    Message,
  },
};
</script>

<style>
body {
  margin: 0;
  margin-top: -100px;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #ffffff;
  margin-top: 60px;
  background: linear-gradient(250deg, #3745a0, #212a64);
  z-index: 1;
  position: relative;
  padding-top: 7em;
  padding-bottom: 9em;
}
</style>
