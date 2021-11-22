<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <Titulo texto="BANCO DEL REAL MADRID"/>
  <Cuenta />
</template>

<script>
import Cuenta from './components/Cuenta.vue'
import Titulo from './components/Titulo.vue'
export default {
  name: 'App',
  components: {
    Titulo,
    Cuenta
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
