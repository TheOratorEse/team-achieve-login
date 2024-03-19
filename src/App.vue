<template>
  <div id="app">
    <img alt=" logo" src="./assets/logo.png">
    <LoginForm msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import LoginForm from './components/LoginForm.vue'

export default {
  name: 'App',
  components: {
    LoginForm
  }
}
</script>

<style>
#app {
  font-family: Avenir, Lora, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
