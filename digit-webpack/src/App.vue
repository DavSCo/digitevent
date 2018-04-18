<template>
  <div id="app">
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'app',
  components: {
    HelloWorld
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Roboto:500');

body {
  background-color: #d4eee2 !important;
  padding: 50px;
  font: 14px "Lucida Grande", Helvetica, Arial, sans-serif;
}

</style>
