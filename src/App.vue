<template>
  <JwtCheck />
  <Login />
</template>
<script>
import Hook from "./components/Hook.vue";
import JwtCheck from "./components/JwtCheck.vue";
import Login from "./components/Login.vue";
export default {
  components: {
    Hook,
    JwtCheck,
    Login,
  },
};
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.login input,
.add input {
  width: 300px;
  height: 40px;
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 30px;
  border: 1px solid black;
  border-radius: 5px;
}

.login button,
.add button {
  width: 300px;
  background: skyblue;
  border: 1px solid skyblue;
  color: #fff;
  height: 40px;
  cursor: pointer;
}
</style>
