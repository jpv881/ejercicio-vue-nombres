<template>
  <div id="app">
    <img src="./assets/logo.png">
    <avatar v-for="nombre in nombres" :name="nombre"></avatar>
  </div>
</template>

<script>
import avatar from "./components/avatar.vue"

export default {
  name: 'app',
  data () {
    return {
      nombres: ['juan', 'pepe', 'carlos']
    }
  },
  components: {
    avatar,
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
