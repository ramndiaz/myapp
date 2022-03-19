<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <div class="row">
      <div class="col"><HelloWorld/></div>
      <div class="col"><Test/></div>
      <div class="col"><User/></div>
    </div>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld'
import Test from './components/Test'
import User from './components/User'

export default {
  name: 'App',
  components: {
    HelloWorld, Test, User
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
