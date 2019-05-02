<template>
  <div id="app">
    <Calculator></Calculator>
  </div>
</template>

<script>
import Calculator from './components/Calculator.vue';
export default {
  name: 'app',
  components: {
    Calculator,
  },
  data() {
    return {
    }
  }
}
</script>

<style lang="scss">
#app {
  background-image: url("assets/back1.jpg");
  height: 100vh;
  width: 100vw;
  padding: 0;
  margin: 0;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
